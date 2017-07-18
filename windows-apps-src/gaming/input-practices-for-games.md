---
author: mithom
title: Input practices for games
description: Learn patterns and techniques for using input devices effectively.
ms.assetid: CBAD3345-3333-4924-B6D8-705279F52676
ms.author: wdg-dev-content
ms.date: 02/08/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, games, input
---

# Input practices for games

This page describes patterns and techniques for effectively using input devices in Universal Windows Platform (UWP) games.

By reading this page, you'll learn:
* how to track players and which input and navigation devices they're currently using
* how to detect button transitions (pressed-to-released, released-to-pressed)
* how to detect complex button arrangements with a single test

## Choosing an input device class

There are many different types of input APIs available to you, such as [ArcadeStick](https://docs.microsoft.com/uwp/api/windows.gaming.input.arcadestick), [FlightStick](https://docs.microsoft.com/uwp/api/windows.gaming.input.flightstick), and [Gamepad](https://docs.microsoft.com/uwp/api/windows.gaming.input.gamepad). How do you decide which API to use for your game?

You should choose whichever API gives you the most appropriate input for your game. For example, if you're making a 2D platform game, you can probably just use the **Gamepad** class and not bother with the extra functionality available via other classes. This would restrict the game to supporting gamepads only and provide a consistent interface that will work across many different gamepads with no need for additional code.

On the other hand, for complex flight and racing simulations, you might want to enumerate all of the [RawGameController](https://docs.microsoft.com/uwp/api/windows.gaming.input.rawgamecontroller) objects as a baseline to make sure they support any niche device that enthusiast players might have, including devices such as separate pedals or throttle that are still used by a single player. 

From there, you can use an input class's **FromGameController** method, such as [Gamepad.FromGameController](https://docs.microsoft.com/uwp/api/windows.gaming.input.gamepad#Windows_Gaming_Input_Gamepad_FromGameController_Windows_Gaming_Input_IGameController_), to see if each device has a more curated view. For example, if the device is also a **Gamepad**, then you might want to adjust the button mapping UI to reflect that, and provide some sensible default button mappings to choose from. (This is in contrast to requiring the player to manually configure the gamepad inputs if you're only using **RawGameController**.) 

Alternatively, you can look at the vendor ID (VID) and product ID (PID) of a **RawGameController** (using [HardwareVendorId](https://docs.microsoft.com/uwp/api/windows.gaming.input.rawgamecontroller#Windows_Gaming_Input_RawGameController_HardwareVendorId) and [HardwareProductId](https://docs.microsoft.com/uwp/api/windows.gaming.input.rawgamecontroller#Windows_Gaming_Input_RawGameController_HardwareProductId), respectively) and provide suggested button mappings for popular devices while still remaining compatible with unknown devices that come out in the future via manual mappings by the player.

## Tracking users and their devices

All input devices are associated with a [User](https://docs.microsoft.com/uwp/api/windows.system.user) so that their identity can be linked to their gameplay, achievements, settings changes, and other activities. Users can sign in or sign out at will, and it's common for a different user to sign in on an input device that remains connected to the system after the previous user has signed out. When a user signs in or out, the [IGameController.UserChanged](https://docs.microsoft.com/uwp/api/windows.gaming.input.igamecontroller#Windows_Gaming_Input_IGameController_UserChanged) event is raised. You can register an event handler for this event to keep track of players and the devices they're using.

User identity is also the way that an input device is associated with its corresponding [UI navigation controller](ui-navigation-controller.md).

For these reasons, player input should be tracked and correlated with the [User](https://docs.microsoft.com/uwp/api/windows.gaming.input.igamecontroller#Windows_Gaming_Input_IGameController_User) property of the device class (inherited from the [IGameController](https://docs.microsoft.com/uwp/api/windows.gaming.input.igamecontroller) interface).

The [UserGamepadPairingUWP (GitHub)](
https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/Samples/System/UserGamepadPairingUWP) sample demonstrates how you can keep track of users and the devices they're using.

## Detecting button transitions

Sometimes you want to know when a button is first pressed or released; that is, precisely when the button state transitions from released to pressed or from pressed to released. To determine this, you need to remember the previous device reading and compare the current reading against it to see what's changed.

The following example demonstrates a basic approach for remembering the previous reading; gamepads are shown here, but the principles are the same for arcade stick, racing wheel, and the other input device types.

```cpp
Gamepad gamepad;
GamepadReading newReading();
GamepadReading oldReading();

// Called at the start of the game.
void Game::Start()
{
    gamepad = Gamepad::Gamepads[0];
}

// Game::Loop represents one iteration of a typical game loop
void Game::Loop()
{
    // move previous newReading into oldReading before getting next newReading
    oldReading = newReading, newReading = gamepad.GetCurrentReading();

    // process device readings using buttonJustPressed/buttonJustReleased (see below)
}
```

Before doing anything else, `Game::Loop` moves the existing value of `newReading` (the gamepad reading from the previous loop iteration) into `oldReading`, then fills `newReading` with a fresh gamepad reading for the current iteration. This gives you the information you need to detect button transitions.

The following example demonstrates a basic approach for detecting button transitions:

```cpp
bool buttonJustPressed(const GamepadButtons selection)
{
	bool newSelectionPressed = (selection == (newReading.Buttons & selection));
    bool oldSelectionPressed = (selection == (oldReading.Buttons & selection));

	return newSelectionPressed && !oldSelectionPressed;
}

bool buttonJustReleased(gamepadButtons selection)
{
	bool newSelectionReleased = (GamepadButtons.None == (newReading.Buttons & selection));
    bool oldSelectionReleased = (GamepadButtons.None == (oldReading.Buttons & selection));

	return newSelectionReleased && !oldSelectionReleased;
}
```

These two functions first derive the Boolean state of the button selection from `newReading` and `oldReading`, then perform Boolean logic to determine whether the target transition has occurred. These functions return **true** only if the new reading contains the target state (pressed or released, respectively) *and* the old reading does not also contain the target state; otherwise, they return **false**.


## Detecting complex button arrangements

Each button of an input device provides a digital reading that indicates whether it's pressed (down) or released (up). For efficiency, button readings aren't represented as individual boolean values; instead, they're all packed into bitfields represented by device-specific enumerations such as [GamepadButtons](https://docs.microsoft.com/uwp/api/windows.gaming.input.gamepadbuttons). To read specific buttons, bitwise masking is used to isolate the values that you're interested in. A button is pressed (down) when its corresponding bit is set; otherwise, it's released (up).

Recall how single buttons are determined to be pressed or released; gamepads are shown here, but the principles are the same for arcade stick, racing wheel, and the other input device types.

```cpp
GamepadReading reading = gamepad.GetCurrentReading();

// Determines whether gamepad button A is pressed.
if (GamepadButtons::A == (reading.Buttons & GamepadButtons::A))
{
    // The A button is pressed.
}

// Determines whether gamepad button A is released.
if (GamepadButtons::None == (reading.Buttons & GamepadButtons::A))
{
    // The A button is released (not pressed).
}
```

As you can see, determining the state of a single button is straight-forward, but sometimes you might want to determine whether multiple buttons are pressed or released, or if a set of buttons are arranged in a particular way&mdash;some pressed, some not. Testing multiple buttons is more complex than testing single buttons&mdash;especially with the potential of mixed button state&mdash;but there's a simple formula for these tests that applies to single and multiple button tests alike.

The following example determines whether gamepad buttons A and B are both pressed:

```cpp
if ((GamepadButtons::A | GamepadButtons::B) == (reading.Buttons & (GamepadButtons::A | GamepadButtons::B))
{
    // The A and B buttons are both pressed.
}
```

The following example determines whether gamepad buttons A and B are both released:

```cpp
if ((GamepadButtons::None == (reading.Buttons & GamepadButtons::A | GamepadButtons::B))
{
    // The A and B buttons are both released (not pressed).
}
```

The following example determines whether gamepad button A is pressed while button B is released:

```cpp
if (GamepadButtons::A == (reading.Buttons & (GamepadButtons::A | GamepadButtons::B))
{
    // The A button is pressed and the B button is released (B is not pressed).
}
```

The formula that all five of these examples have in common is that the arrangement of buttons to be tested for is specified by the expression on the left-hand side of the equality operator while the buttons to be considered are selected by the masking expression on the right-hand side.

The following example demonstrates this formula more clearly by rewriting the previous example:

```cpp
auto buttonArrangement = GamepadButtons::A;
auto buttonSelection = (reading.Buttons & (GamepadButtons::A | GamepadButtons::B));

if (buttonArrangement == buttonSelection)
{
    // The A button is pressed and the B button is released (B is not pressed).
}
```

This formula can be applied to test any number of buttons in any arrangement of their states.

## See also

* [Windows.System.User class](https://docs.microsoft.com/uwp/api/windows.system.user)
* [Windows.Gaming.Input.IGameController interface](https://docs.microsoft.com/uwp/api/windows.gaming.input.igamecontroller)
* [Windows.Gaming.Input.GamepadButtons enum](https://docs.microsoft.com/uwp/api/windows.gaming.input.gamepadbuttons)
