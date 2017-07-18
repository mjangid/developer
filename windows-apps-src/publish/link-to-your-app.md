﻿---
author: jnHs
Description: You can help customers discover your app by linking to your app's Store listing.
title: Link to your app
ms.assetid: 5420B65C-7ECE-4364-8959-D1683684E146
ms.author: wdg-dev-content
ms.date: 06/19/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, link, windows store protocol, linking to an app, link to app
---

# Link to your app


You can help customers discover your app by linking to your app's Store listing.

## Getting the link to your app's Store listing

To get the URL for your app's Store listing, navigate to the app's [App identity](view-app-identity-details.md) page in the **App management** section. The URL is in the format **`https://www.microsoft.com/store/apps/<your app's Store ID>`**.

When a customer clicks this link, it opens the web-based listing page for your app. On Windows devices, the Store app will also launch and display your app's listing.


## Linking to your app's Store listing with the Windows Store badge

You can link directly to your app's listing with a custom badge to let customers know your app is in the Windows Store.

To create your badge, visit the [Windows Store badges](http://go.microsoft.com/fwlink/p/?LinkID=534236) page. You'll need to have your app's 12-character **Store ID** in order to generate the badge and link. You can find your app's **Store ID** on the [App identity](view-app-identity-details.md) page in the **App management** section.

> [!NOTE]
> See [App marketing guidelines](app-marketing-guidelines.md) for info and requirements related to your use of the Windows Store badge.


## Linking directly to your app in the Windows Store

You can create a link that launches the Windows Store and goes directly to your app's listing page without opening a browser by using the **ms-windows-store:** URI scheme.

These links are useful if you know your users are on a Windows device and you want them to arrive directly at the listing page in the Store. For example, you might want to use this link after checking user agent strings in a browser to confirm that the user's operating system supports the Store, or when you are already communicating via a UWP app.

To use the Windows Store protocol to link directly to your app's Store listing, append your app's Store ID to this link:

`ms-windows-store://pdp/?ProductId=`

For more about using the Windows Store protocol, see [Launch the Windows Store app](../launch-resume/launch-store-app.md).

 

 




