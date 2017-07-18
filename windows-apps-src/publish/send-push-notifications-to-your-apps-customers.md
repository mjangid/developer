﻿---
author: JnHs
Description: Learn how to send notifications from Windows Dev Center to your app to encourage groups of customers to take an action, such as rating an app or buying an add-on.
title: Send targeted push notifications to your app's customers
ms.author: wdg-dev-content
ms.date: 06/19/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp
ms.assetid: 16386c81-702d-47cd-9f91-67659f5dca73
---

# Send notifications to your app's customers

Engaging with your customers at the right time and with the right message is key to your success as an app developer. Windows Dev Center provides a data-driven customer engagement platform you can use to send notifications to all of your customers, or only targeted to a subset of your Windows 10 customers who meet the criteria you’ve defined in a [customer segment](create-customer-segments.md).

You can use notifications to encourage your customers to take an action, such as rating an app, buying an add-on, trying a new feature, or downloading another app (perhaps for free with a [promotional code](generate-promotional-codes.md) that you provide).

> [!IMPORTANT]
> These notifications can only be used with UWP apps.

When considering the content of your notifications, keep in mind:
- The content in your notifications must comply with the Store [Content Policies](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#content_policies).
- Your notification content should not include confidential or potentially sensitive info.
- While we’ll make every effort to deliver your notification as scheduled, there may occasionally be latency issues that impact delivery.
- Be sure not to send notifications too often. More than once every 30 minutes can seem intrusive (and for many scenarios, less frequently than that is preferable).
- Be aware that if a customer who uses your app (and is signed in with their Microsoft account at the time the segment membership is determined) later gives their device to someone to use, the other person may see the notification that was targeted at the original customer. For more info, see [Configure your app for targeted push notifications](../monetize/configure-your-app-to-receive-dev-center-notifications.md#notification-customers).

## Getting started with notifications

At a high-level, you need to do three things to use notifications to engage with your customers.
1. **Register your app to receive push notifications.** You do this by adding a reference to the Microsoft Store Services SDK in your app and then adding a few lines of code that registers a notification channel between the Dev Center and your app. We’ll use that channel to deliver your notifications to your customers. For details, see [Configure your app for targeted push notifications](../monetize/configure-your-app-to-receive-dev-center-notifications.md).
2. **Create one or more customer segments that you want to target.** You can group your customers into segments based on demographic or revenue criteria. For more info, see [Create customer segments](create-customer-segments.md). You can also send a notification to all of your app's customers, if you prefer.
3. **Create a push notification and send it to a particular customer segment.** For example, send a notification to encourage new customers to rate your app or send a notification with a special deal to purchase an add-on.

## To create and send a notification

Follow these steps to create a notification in the dashboard and send it to a particular customer segment.

> [!NOTE]
> Before your app can receive notifications from Dev Center, you must first call the [RegisterNotificationChannelAsync](https://msdn.microsoft.com/library/windows/apps/mt771190.aspx) method in your app to register your app to receive notifications. This method is available in the [Microsoft Store Services SDK](http://aka.ms/store-em-sdk). For more information about how to call this method, including a code example, see [Configure your app for targeted push notifications](../monetize/configure-your-app-to-receive-dev-center-notifications.md).

1.	In the [Windows Dev Center dashboard](https://developer.microsoft.com/dashboard/overview), expand the **Engage** section, and then select **Notifications**.
2.	On the **Notifications** page, select **New notification**.
3.      From the drop-down menu, select the app for which you want to generate a notification.
4.	In the **Select a template** section, choose the type of notification you want to send. For details, see [Notification template types](#notification-template-types).
  ![Notification templates](images/push-notifications-template.png)
5.	In the **Notification settings** section, choose a **Name** for your notification and choose the **Customer group** you want to send the notification to.
If you haven’t created a segment yet, select **Create new customer group**. Note that it takes 24 hours for a new segment to be available to use for notifications. For more info, see [Create customer segments](create-customer-segments.md).
6.	If you want to specify when to send the notification, clear the **Send notification immediately** checkbox and choose a specific date and time.
7.	If you want the notification to expire at some point, clear the **Notification never expires** checkbox and choose a specific expiration date and time.
8.	If you want to filter the recipients so that your notification is only delivered to people who use certain languages, or who are in specific time zones, check the **Filters** checkbox. You can then select the languages and/or time zones by which you want to filter your recipients.
9.	In the **Notification content** section, in the **Language** menu, choose the languages in which you want your notification to be displayed. For more info, see [Translate your notifications](#translate-your-notifications).
10.	In the **Options** section, enter text and configure any other options you’d like. If you started with a template, some of this is provided by default, but you can make any changes you'd like.
   The available options vary, depending on which notification type you are using. Some of the options are:
   - **Activation type** (interactive toast type). You can choose **Foreground**, **Background**, or **Protocol**.
   - **Launch** (interactive toast type). You can choose to have the notification open an app or website.
   - **Track app launch rate** (interactive toast type). If you want to measure how well you’re engaging with your customers through each notification, select this checkbox. For more details, see [Measure notification performance](#measure-notification-performance).
   - **Duration** (interactive toast type). You can choose **Short** or **Long**.
   - **Scenario** (interactive toast type). You can choose **Default**, **Alarm**, **Reminder**, or **Incoming call**.
   - **Base URI** (interactive toast type). For more details, see [BaseUri](https://msdn.microsoft.com/library/windows/apps/br208712).
   - **Add image query** (interactive toast type). For more details, see [addImageQuery](https://msdn.microsoft.com/library/windows/apps/br230847).
   - **Visual**. An image, video, or sound. For more details, see [visual](https://msdn.microsoft.com/library/windows/apps/br230847).
   - **Input**/**Action**/**Selection** (interactive toast type). Allows you to let users interact with the notification. For more info, see [Adaptive and interactive toast notifications](../controls-and-patterns/tiles-and-notifications-adaptive-interactive-toasts.md).
   - **Binding** (interactive tile type). The toast template. For more details, see [binding](https://msdn.microsoft.com/library/windows/apps/br230843).

   > [!TIP]
   > Try using the [Notifications Visualizer](https://www.microsoft.com/store/apps/9nblggh5xsl1) app to design and test your adaptive tiles and interactive toast notifications.

11.	Select **Save as draft** to continue working on the notification later, or select **Send** if you’re all done.

## Notification template types

You can choose from a variety of notification templates.

-	**Blank (Toast).** Start with an empty toast notification that you can customize. A toast notification is a pop-up UI that appears on your screen to allow your app to communicate with the customer when the customer is in another app, on the Start screen, or on the desktop.
-	**Blank (Tile).** Start with an empty tile notification that you can customize. Tiles are an app's representation on the Start screen. Tiles can be “live,” which means that the content that they display can change in response to notifications.
-	**Ask for ratings (Toast).** A toast notification that asks your customers to rate your app. When the customer selects the notification, the Store ratings page for your app is displayed.
-	**Ask for feedback (Toast).** A toast notification that asks your customers to provide feedback for your app. When the customer selects the notification, the Feedback Hub page for your app is displayed.

   > [!NOTE]
   > If you choose this template type, in the **Launch** box, remember to replace the {PACKAGE_FAMILY_NAME} placeholder value with your app’s actual Package Family Name (PFN). You can find your app’s PFN on the [App identity](view-app-identity-details.md) page (**App management** > **App identity**).

   ![Feedback toast Launch box](images/push-notifications-feedback-toast-launch-box.png)
-	**Cross-promote (Toast).** A toast notification to promote a different app of your choosing. When the customer selects the notification, the other app’s Store listing is displayed.
   > [!NOTE]
   > If you choose this template type, in the **Launch** box, remember to replace the **{ProductId you want to promote here}** placeholder value with the actual Store ID of the item you want to cross promote. You can find the Store ID on the [App identity](view-app-identity-details.md) page (**App management** > **App identity**).

  ![Cross-promote toast Launch box](images/push-notifications-promote-toast-launch-box.png)
-	**Promote a sale (Toast).** A toast notification that you can use to announce a deal for your app. When the customer selects the notification, your app’s Store listing is displayed.
-	**Prompt for update (Toast).** A toast notification that encourages customers who are running an older version of your app to install the latest version. When the customer selects the notification, the **Downloads and updates** list in the Store app is displayed. Note that you don't need to create a customer segment to use this template. We’ll schedule this notification within 24 hours and we’ll make our best effort to target all users who are not yet running the latest version of your app.

## Measure notification performance

You can measure how well you’re engaging with your customers through each notification.

###To measure notification performance

1.	When you create a notification, in the **Notification content** section, select the **Track app launch rate** checkbox.
2.	In your app, call the [ParseArgumentsAndTrackAppLaunch](https://msdn.microsoft.com/library/windows/apps/microsoft.services.store.engagement.storeservicesengagementmanager.parseargumentsandtrackapplaunch.aspx) method to notify Dev Center that your app was launched in response to a targeted notification. This method is provided by the Microsoft Store Services SDK. For more information about how to call this method, see [Configure your app to receive Dev Center notifications](../monetize/configure-your-app-to-receive-dev-center-notifications.md).

###To view notification performance

When you’ve configured the notification and your app to [measure notification performance](#measure-notification-performance) as described above, you can use the dashboard to see how well your notifications are performing.

1.  In the dashboard, select one of your apps.
2.  Expand the **Services** section on the left menu, then select **Push notifications** to see the notifications associated with that app.
3.	On the **Targeted push notifications** page, select **In progress** or **Completed**, and then look at the **Delivery rate** and **App launch rate** columns to see the high-level performance of each notification.
4.  To see more granular performance details, select a notification name. The **Delivery statistics** section appears and shows **Count** and **Percentage** info for the following notification **Status** types:
 - **Failed**: The notification was not delivered for some reason. This can happen, for example, if an issue occurs in the Windows Notification Service.
 - **Channel expiration failure**: The notification could not be delivered because the channel between the app and Dev Center has expired. This can happen, for example, if the customer has not opened your app in a long time.
 - **Sending**: The notification is in the queue to be sent.
 - **Sent**: The notification was sent.
 - **Launches**: The notification was sent, the customer clicked it, and your app was opened as a result. Note that this only tracks app launches. Notifications that invite the customer to take other actions, such as launching the Store to leave a rating, are not included in this status.
 - **Unknown**: We weren’t able to determine the status of this notification.

## Translate your notifications

To maximize the impact of your notifications, consider translating them into the languages that your customers prefer. Dev Center makes it easy for you to translate your notifications automatically by leveraging the power of the [Microsoft Translator](https://msdn.microsoft.com/library/dd576287.aspx) service.

1.	After you’ve written your notification in your default language, select **Add languages** (beneath the **Languages** menu in the **Notification content** section).
2.	In the **Add languages** window, select the additional languages that you want your notifications to appear in, and then select **Update**.
Your notification will be automatically translated into the languages you chose in the **Add languages** window and those languages will be added to the **Language** menu.
3.	To see the translation of your notification, in the **Language** menu, select the language that you just added.

Things to keep in mind about translation:
 - You can override the automatic translation by entering something different in the **Content** box for that language.
 - If you add another text box to the English version of the notification after you’ve overridden an automatic translation, the new text box will not be added to translated notification. In that case, you would need to manually add the new text box to each of translated notifications.
 - If you change the English text after the notification has been translated, we’ll automatically update the translated notifications to match the change. However, this won’t happen if you previously chose to override the initial translation.

## Related topics
- [Tiles, badges, and notifications for UWP apps](../controls-and-patterns/tiles-badges-notifications.md)
- [Windows Push Notification Services (WNS) overview](../controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md)
- [Notifications Visualizer app](https://www.microsoft.com/store/apps/9nblggh5xsl1)
- [StoreServicesEngagementManager.RegisterNotificationChannelAsync() | registerNotificationChannelAsync() method](https://msdn.microsoft.com/library/windows/apps/mt771190.aspx)
- [Customer segmentation and push notifications: a new Windows Dev Center Insider Program feature (blog post)](https://blogs.windows.com/buildingapps/2016/08/17/customer-segmentation-and-push-notifications-a-new-windows-dev-center-insider-program-feature/#XTuCqrG8G5IMgWew.97)
