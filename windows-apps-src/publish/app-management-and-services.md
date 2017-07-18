﻿---
author: jnHs
Description: Manage and view details related to each of your apps in the Windows Dev Center dashboard, and configure services such as notifications, A/B testing, and maps.
title: App management and services
ms.assetid: 99DA2BC1-9B5D-4746-8BC0-EC723D516EEF
ms.author: wdg-dev-content
ms.date: 06/19/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp
---

# App management and services

You can manage and view details related to each of your apps in the Windows Dev Center dashboard, and configure services such as notifications, A/B testing, and maps.

When working with an app in your dashboard, you'll see sections in the left navigation menu for **Services** and **App management**. You can expand these sections to access the functionality described below.

## Services

The **Services** section lets you manage several different services for your apps.

## Push notifications

The **Push notifications** section lets you create and send notifications to your app's customers. You can send them to all of your app's customers, or you can target a subset of your Windows 10 customers who meet the criteria you’ve defined in a [customer segment](create-customer-segments.md). For more info, see [Send notifications to your app's customers](send-push-notifications-to-your-apps-customers.md).

Depending on your app's package type and its specific requirements, you can also use one of the following options for push notifications by clicking **WNS/MPNS** in the left navigation menu: 

-   **Windows Push Notification Services (WNS)** lets you send toast, tile, badge, and raw updates from your own cloud service. For more info, see [Windows Push Notification Services (WNS) overview](https://msdn.microsoft.com/library/windows/apps/mt187203).

-   **Microsoft Azure Mobile Apps** lets you send push notifications, authenticate and manage app users, and store app data in the cloud. For more info, see the [Mobile Apps documentation](http://go.microsoft.com/fwlink/p/?LinkId=221116).

-   **Microsoft Push Notifications Service (MPNS)** can be used with your .xap packages for Windows Phone. You can send a limited number of unauthenticated notifications without doing any configuration here, although we recommend using authenticated notifications to avoid throttling limits. If you're using MPNS, you'll need to upload a certificate to the field provided on the **Push notifications** page. For more info, see [Setting up an authenticated web service to send push notifications for Windows Phone 8](http://go.microsoft.com/fwlink/p/?LinkId=528736).

## Experimentation

Use the **Experimentation** page to create and run experiments for your Universal Windows Platform (UWP) apps with A/B testing. In an A/B test, you measure the effectiveness of feature changes (or variations) in your app on some customers before you enable the changes for everyone.

For more info, see [Run app experiments with A/B testing](../monetize/run-app-experiments-with-a-b-testing.md).

## Maps

To use map services in apps for Windows Phone 8.1 and earlier, you need a map service application ID and a token to include in your app's code. You can get this token on the **Maps** page in the **Services** section.

> [!NOTE]
> To use map services in apps targeting Windows 10 or Windows 8.x, visit the [Bing Maps Dev Center](http://go.microsoft.com/fwlink/p/?LinkId=614880). See [Request a maps authentication key](https://msdn.microsoft.com/library/windows/apps/mt219694) for more info.

For more info, see [Use map services](use-map-services.md).

## Product collections and purchases

To use the Windows Store collection API and the Windows Store purchase API to access ownership information for apps and add-ons, you need to enter the associated Azure AD client IDs here. Note that it may take up to 16 hours for these changes to take effect.

For more info, see [Manage product entitlements from a service](../monetize/view-and-grant-products-from-a-service.md).

## App management

The **App management** section lets you view identity and package details and manage names for your app.

## App identity

This page shows you details related to your app's unique identity within the Store, including the URL(s) to link to your app's listing.

For more info, see [View app identity details](view-app-identity-details.md).

## Manage app names

This is where you can view all of the names that you've reserved for your app. You can reserve additional names here, or delete names you're no longer using.

For more info, see [Manage app names](manage-app-names.md).

## Current packages

This page lets you view details related to all of your published packages.

> [!NOTE]
> You won't see any info here until your app has been published.

The name, version, and architecture of each package is shown. Click **Details** to show additional info such as supported language, app capabilities, and file sizes. The info you see for each package may vary depending on its targeted operating system and other factors. 

Developers with OEM permissions can also [generate preinstall packages](generate-preinstall-packages-for-oems.md) from the **Current packages** page.

 

 
