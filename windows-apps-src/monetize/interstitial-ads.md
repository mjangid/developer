---
author: mcleanbyron
ms.assetid: 1f970d38-2338-470e-b5ba-811402752fc4
description: Learn how to include interstitial ads in a Windows 10, Windows 8.1, or Windows Phone 8.1 app using the Microsoft advertising libraries.
title: Interstitial ads
ms.author: mcleans
ms.date: 06/26/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, ads, advertising, ad control, interstitial
---

# Interstitial ads

This walkthrough shows how to include interstitial ads in Universal Windows Platform (UWP) apps and games for Windows 10 and in apps for Windows 8.1 or Windows Phone 8.1. For complete sample projects that demonstrate how to add interstitial ads to JavaScript/HTML apps and XAML apps using C# and C++, see the [advertising samples on GitHub](http://aka.ms/githubads).

<span id="whatareinterstitialads10"/>
## What are interstitial ads?

Unlike standard banner ads, which are confined to a portion of a UI in an app or game, interstitial ads are shown on the entire screen. Two basic forms are frequently used in games.

* With *Paywall* ads, the user must watch an ad at some regular interval. For example between game levels:

    ![whatisaninterstitial](images/13-ed0a333b-0fc8-4ca9-a4c8-11e8b4392831.png)

* With *Rewards Based* ads the user is explicitly seeking some benefit, such as a hint or extra time to complete the level, and initializes the ad through the app’s user interface.

We provide two types of interstitial ads to use in your apps and games:

* **Interstitial video ads**: These are available for Universal Windows Platform (UWP) apps for Windows 10 and in apps for Windows 8.1 or Windows Phone 8.1.

* **Interstitial banner ads**: These are only available for UWP apps for Windows 10.

> [!NOTE]
> The API for interstitial ads does not handle any user interface except at the time of video playback. Refer to the [interstitial best practices](ui-and-user-experience-guidelines.md#interstitialbestpractices10) for guidelines on what to do, and avoid, as you consider how to integrate interstitial ads in your app.

## Build an app with interstitial ads

To show interstitial ads in your app, follow the instructions for project type:

* [XAML/.NET](#interstitialadsxaml10)
* [HTML/JavaScript](#interstitialadshtml10)
* [C++ (DirectX Interop)](#interstitialadsdirectx10)

<span/>
### Prerequisites

* For UWP apps: install the [Microsoft Advertising SDK](http://aka.ms/ads-sdk-uwp) with Visual Studio 2015 or a later release.

* For Windows 8.1 or Windows Phone 8.1 apps: install the [Microsoft Advertising SDK for Windows and Windows Phone 8.x](http://aka.ms/store-8-sdk) with Visual Studio 2015 or Visual Studio 2013.

<span id="interstitialadsxaml10"/>
### XAML/.NET

This section provides C# examples, but Visual Basic and C++ are also supported for XAML/.NET projects. For a complete C# code example, see [Interstitial ad sample code in C#](interstitial-ad-sample-code-in-c.md).

1. Open your project in Visual Studio.

2. In **Reference Manager**, select one of the following references depending on your project type:

  * For a Universal Windows Platform (UWP) project: Expand **Universal Windows**, click **Extensions**, and then select the check box next to **Microsoft Advertising SDK for XAML** (Version 10.0).

  * For a Windows 8.1 project: Expand **Windows 8.1**, click **Extensions**, and then select the check box next to **Ad Mediator SDK for Windows 8.1 XAML**. This option will add both the Microsoft advertising and ad mediator libraries to your project, but you can ignore the ad mediator libraries.

  * For a Windows Phone 8.1 project: Expand **Windows Phone 8.1**, click **Extensions**, and then select the check box next to **Ad Mediator SDK for Windows Phone 8.1 XAML**. This option will add both the Microsoft advertising and ad mediator libraries to your project, but you can ignore the ad mediator libraries.

3.  In the appropriate code file in your app (for example, in MainPage.xaml.cs or a code file for some other page), add the following namespace reference.

  [!code-cs[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cs/MainPage.xaml.cs#Snippet1)]

4.  In an appropriate location in your app (for example, in ```MainPage``` or some other page), declare an [InterstitialAd](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.aspx) object and several string fields that represent the application ID and ad unit ID for your interstitial ad. The following code example assigns the `myAppId` and `myAdUnitId` fields to the test values for interstitial video ads provided in [Test mode values](test-mode-values.md).

  > [!NOTE]
  > Every **InterstitialAd** has a corresponding *ad unit* that is used by our services to serve ads to the control, and every ad unit consists of an *ad unit ID* and *application ID*. In these steps, you assign test ad unit ID and application ID values to your control. These test values can only be used in a test version of your app. Before you publish your app to the Store, you must [replace these test values with live values](#release) from Windows Dev Center.

  [!code-cs[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cs/MainPage.xaml.cs#Snippet2)]

5.  In code that runs on startup (for example, in the constructor for the page), instantiate the **InterstitialAd** object and wire up event handlers for events of the object.

  [!code-cs[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cs/MainPage.xaml.cs#Snippet3)]

6.  If you want to show an *interstitial video* ad: Approximately 30-60 seconds before you need the ad, use the [RequestAd](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.requestad.aspx) method to pre-fetch the ad. This allows enough time to request and prepare the ad before it should be shown. Be sure to specify **AdType.Video** for the ad type.

  [!code-cs[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cs/MainPage.xaml.cs#Snippet4)]

  If you want to show an *interstitial banner* ad (for UWP apps only): Approximately 5-8 seconds before you need the ad, use the [RequestAd](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.requestad.aspx) method to pre-fetch the ad. This allows enough time to request and prepare the ad before it should be shown. Be sure to specify **AdType.Display** for the ad type.

  ```csharp
  myInterstitialAd.RequestAd(AdType.Display, myAppId, myAdUnitId);
  ```

6.  At the point in your code where you want to show the interstitial video or interstitial banner ad, confirm that the **InterstitialAd** is ready to be shown and then show it by using the [Show](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.show.aspx) method.

  [!code-cs[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cs/MainPage.xaml.cs#Snippet5)]

7.  Define the event handlers for the **InterstitialAd** object.

  [!code-cs[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cs/MainPage.xaml.cs#Snippet6)]

8.  Build and test your app to confirm it is showing test ads.

<span id="interstitialadshtml10"/>
### HTML/JavaScript

The following instructions assume you have created a Universal Windows project for JavaScript in Visual Studio and are targeting a specific CPU. For a complete code sample, see [Interstitial ad sample code in JavaScript](interstitial-ad-sample-code-in-javascript.md).

1. Open your project in Visual Studio.

2.  In **Reference Manager**, select one of the following references depending on your project type:

  * For a Universal Windows Platform (UWP) project: Expand **Universal Windows**, click **Extensions**, and then select the check box next to **Microsoft Advertising SDK for JavaScript** (Version 10.0).

  * For a Windows 8.1 project: Expand **Windows 8.1**, click **Extensions**, and then select the check box next to **Microsoft Advertising SDK for Windows 8.1 Native (JS)**.

  * For a Windows 8.1 project: Expand **Windows Phone 8.1**, click **Extensions**, and then select the check box next to **Microsoft Advertising SDK for Windows Phone 8.1 Native (JS)**.

3.  In the **&lt;head&gt;** section of the HTML file in the project, after the project’s JavaScript references of default.css and default.js, add the reference to ad.js. In a UWP project, add the following reference.

  ``` HTML
  <script src="//Microsoft.Advertising.JavaScript/ad.js"></script>
  ```

  In a Windows 8.1 or Windows Phone 8.1 project, add the following reference.

  ``` HTML
  <script src="/MSAdvertisingJS/ads/ad.js"></script>
  ```

4.  In a .js file in your project, declare an [InterstitialAd](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.aspx) object and several fields that contain the application ID and ad unit ID for your interstitial ad. The following code example assigns the `applicationId` and `adUnitId` fields to the test values for interstitial video ads provided in [Test mode values](test-mode-values.md).

  > [!NOTE]
  > Every **InterstitialAd** has a corresponding *ad unit* that is used by our services to serve ads to the control, and every ad unit consists of an *ad unit ID* and *application ID*. In these steps, you assign test ad unit ID and application ID values to your control. These test values can only be used in a test version of your app. Before you publish your app to the Store, you must [replace these test values with live values](#release) from Windows Dev Center.

  [!code-javascript[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/js/script.js#Snippet1)]

5.  In code that runs on startup (for example, in the constructor for the page), instantiate the **InterstitialAd** object and wire up event handlers for the object.

  [!code-javascript[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/js/script.js#Snippet2)]

5. If you want to show an *interstitial video* ad: Approximately 30-60 seconds before you need the ad, use the [RequestAd](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.requestad.aspx) method to pre-fetch the ad. This allows enough time to request and prepare the ad before it should be shown. Be sure to specify **InterstitialAdType.video** for the ad type.

  [!code-javascript[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/js/script.js#Snippet3)]

  If you want to show an *interstitial banner* ad (for UWP apps only): Approximately 5-8 seconds before you need the ad, use the [RequestAd](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.requestad.aspx) method to pre-fetch the ad. This allows enough time to request and prepare the ad before it should be shown. Be sure to specify **InterstitialAdType.display** for the ad type.

  ```js
  if (interstitialAd) {
      interstitialAd.requestAd(MicrosoftNSJS.Advertising.InterstitialAdType.display, applicationId, adUnitId);
  }
  ```

6.  At the point in your code where you want to show the ad, confirm that the **InterstitialAd** is ready to be shown and then show it by using the [Show](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.show.aspx) method.

  [!code-javascript[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/js/samples.js#Snippet4)]

7.  Define the event handlers for the **InterstitialAd** object.

  [!code-javascript[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/js/samples.js#Snippet5)]

9.  Build and test your app to confirm it is showing test ads.

<span id="interstitialadsdirectx10"/>
### C++ (DirectX Interop)

This sample assumes you have created a C++ **DirectX and XAML App (Universal Windows)** project in Visual Studio and are targeting a specific CPU architecture.
 
1. Open your project in Visual Studio.

1.  In **Reference Manager**, select one of the following references depending on your project type:

  * For a Universal Windows Platform (UWP) project: Expand **Universal Windows**, click **Extensions**, and then select the check box next to **Microsoft Advertising SDK for XAML** (Version 10.0).

  * For a Windows 8.1 project: Expand **Windows 8.1**, click **Extensions**, and then select the check box next to **Ad Mediator SDK for Windows 8.1 XAML**. This option will add both the Microsoft advertising and ad mediator libraries to your project, but you can ignore the ad mediator libraries.

  * For a Windows Phone 8.1 project: Expand **Windows Phone 8.1**, click **Extensions**, and then select the check box next to **Ad Mediator SDK for Windows Phone 8.1 XAML**. This option will add both the Microsoft advertising and ad mediator libraries to your project, but you can ignore the ad mediator libraries.

2.  In an appropriate header file for your app (for example, DirectXPage.xaml.h), declare an [InterstitialAd](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.aspx) object and related event handler methods.  

  [!code-cpp[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cpp/DirectXPage.xaml.h#Snippet1)]

3.  In the same header file, declare several string fields that represent the application ID and ad unit ID for your interstitial ad. The following code example assigns the `myAppId` and `myAdUnitId` fields to the test values for interstitial video ads provided in [Test mode values](test-mode-values.md).

  > [!NOTE]
  > Every **InterstitialAd** has a corresponding *ad unit* that is used by our services to serve ads to the control, and every ad unit consists of an *ad unit ID* and *application ID*. In these steps, you assign test ad unit ID and application ID values to your control. These test values can only be used in a test version of your app. Before you publish your app to the Store, you must [replace these test values with live values](#release) from Windows Dev Center.

  [!code-cpp[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cpp/DirectXPage.xaml.h#Snippet2)]

4.  In the .cpp file where you want to add code to show an interstitial ad, add the following namespace reference. The following examples assume you are adding the code to DirectXPage.xaml.cpp file in your app.

  [!code-cpp[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cpp/DirectXPage.xaml.cpp#Snippet3)]

6.  In code that runs on startup (for example, in the constructor for the page), instantiate the **InterstitialAd** object and wire up event handlers for events of the object. In the following example, ```InterstitialAdSamplesCpp``` is the namespace for your project; change this name as necessary for your code.

  [!code-cpp[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cpp/DirectXPage.xaml.cpp#Snippet4)]

7. If you want to show an *interstitial video* ad: Approximately 30-60 seconds before you need the interstitial ad, use the [RequestAd](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.requestad.aspx) method to pre-fetch the ad. This allows enough time to request and prepare the ad before it should be shown. Be sure to specify **AdType::Video** for the ad type.

  [!code-cpp[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cpp/DirectXPage.xaml.cpp#Snippet5)]

  If you want to show an *interstitial banner* ad (for UWP apps only): Approximately 5-8 seconds before you need the ad, use the [RequestAd](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.requestad.aspx) method to pre-fetch the ad. This allows enough time to request and prepare the ad before it should be shown. Be sure to specify **AdType::Display** for the ad type.

  ```cpp
  m_interstitialAd->RequestAd(AdType::Display, myAppId, myAdUnitId);
  ```

7.  At the point in your code where you want to show the ad, confirm that the **InterstitialAd** is ready to be shown and then show it by using the [Show](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.interstitialad.show.aspx) method.

  [!code-cpp[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cpp/DirectXPage.xaml.cpp#Snippet6)]

8.  Define the event handlers for the **InterstitialAd** object.

  [!code-cpp[InterstitialAd](./code/AdvertisingSamples/InterstitialAdSamples/cpp/DirectXPage.xaml.cpp#Snippet7)]

9. Build and test your app to confirm it is showing test ads.

<span id="release" />
## Release your app with live ads using Windows Dev Center

1.  In the Dev Center dashboard, go to the [Monetize with ads](../publish/monetize-with-ads.md) page for your app and [create an ad unit](../monetize/set-up-ad-units-in-your-app.md). For the ad unit type, choose **Video interstitial** or **Banner interstitial**, depending on what type of interstitial ad you are showing. Make note of both the ad unit ID and the application ID.

2. If your app is a UWP app for Windows 10, you can optionally enable ad mediation for the **InterstitialAd** by configuring the settings in the [Ad mediation](../publish/monetize-with-ads.md#mediation) section on the [Monetize with ads](../publish/monetize-with-ads.md) page. Ad mediation enables you to maximize your ad revenue and app promotion capabilities by displaying ads from multiple ad networks, including ads from other paid ad networks such as Taboola and Smaato and ads for Microsoft app promotion campaigns.

3.  In your code, replace the test ad unit values with the live values you generated in Dev Center.

4.  [Submit your app](../publish/app-submissions.md) to the Store using the Windows Dev Center dashboard.

5.  Review your [advertising performance reports](../publish/advertising-performance-report.md) in the Dev Center dashboard.

<span id="manage" />
## Manage ad units for multiple interstitial ad controls in your app

You can use multiple **InterstitialAd** controls in a single app. In this scenario, we recommend that you assign a different ad unit to each control. Using different ad units for each control enables you to separately [configure the mediation settings](../publish/monetize-with-ads.md#mediation) and get discrete [reporting data](../publish/advertising-performance-report.md) for each control. This also enables our services to better optimize the ads we serve to your app.

> [!IMPORTANT]
> You can use each ad unit in only one app. If you use an ad unit in more than one app, ads will not be served for that ad unit.

<span id="interstitialbestpractices10"/>
## Interstitial best practices and policies


For more information about how to use interstitial ads effectively and policies that you must follow, see [Interstitial best practices and policies](ui-and-user-experience-guidelines.md#interstitialbestpractices10).

<span id="targetplatform10"/>
## Remove reference errors: target a specific CPU platform (XAML and HTML)


When using the Microsoft advertising libraries, you cannot target **Any CPU** in your project. If your project targets the **Any CPU** platform, you may see a warning in your project after you add a reference to the Microsoft advertising libraries. To remove this warning, update your project to use an architecture-specific build output (for example, **x86**). For more information, see [Known issues](known-issues-for-the-advertising-libraries.md).

## Related topics


* [Interstitial ad sample code in C#](interstitial-ad-sample-code-in-c.md)
* [Interstitial ad sample code in JavaScript](interstitial-ad-sample-code-in-javascript.md)
* [Advertising samples on GitHub](http://aka.ms/githubads)
* [Set up ad units for your app](../monetize/set-up-ad-units-in-your-app.md)
