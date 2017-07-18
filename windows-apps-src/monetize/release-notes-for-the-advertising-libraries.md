---
author: mcleanbyron
ms.assetid: ca92bed1-ad9e-4947-ad91-87d12de727c0
description: Review the release notes for the Microsoft advertising libraries.
title: Release notes for the advertising libraries
ms.author: mcleans
ms.date: 02/08/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, ads, advertising, release notes
---

# Release notes for the advertising libraries




This section provides release notes for the current release of the Microsoft advertising libraries. These libraries support XAML and JavaScript/HTML apps for Windows 10, Windows 8.1, Windows Phone 8.1 and Windows Phone 8.

## Installation


The Microsoft advertising libraries are available as part of the [Microsoft Advertising SDK](http://aka.ms/ads-sdk-uwp) (for UWP apps) and the [Microsoft Advertising SDK for Windows and Windows Phone 8.x](http://aka.ms/store-8-sdk) (for Windows 8.1 and Windows Phone 8.x apps). For more information about installing the SDKs and the libraries that are included in them, see [Install the Microsoft Advertising SDK](install-the-microsoft-advertising-libraries.md).

## Uninstall previous versions

Before you install the latest Microsoft Advertising SDK (for UWP apps) or the Microsoft Advertising SDK for Windows and Windows Phone 8.x (for Windows 8.1 and Windows Phone 8.x apps), it is highly recommended that you uninstall all prior instances of the Microsoft Universal Ad Client SDK or the Microsoft Advertising SDK.

## Target architecture-specific build outputs

When using the Microsoft advertising libraries, you cannot target **Any CPU** in your project. If your project targets the **Any CPU** platform, you may see a warning in your project after you add a reference to the Microsoft advertising libraries. To remove this warning, update your project to use an architecture-specific build output (for example, **x86**). For more information, see [Known issues](known-issues-for-the-advertising-libraries.md).

## C++ Support

The Microsoft advertising libraries (which include the **AdControl** and **InterstitialAd** classes) support apps written in C++ and DirectX using Windows Runtime Interoperability (*interop*). For more information and examples about programming using XAML and C++, see [Type System](https://msdn.microsoft.com/library/windows/apps/xaml/hh755822.aspx).

## No toolbox control

In the current release of the Microsoft advertising libraries in the [Microsoft Advertising SDK](http://aka.ms/ads-sdk-uwp) or the [Microsoft Advertising SDK for Windows and Windows Phone 8.x](http://aka.ms/store-8-sdk), there is no toolbox control for dragging an **AdControl** or **InterstitialAd** to a design surface in your app. For instructions about adding these controls in your markup and code, see the [developer walkthroughs](developer-walkthroughs.md).

## Latitude and longitude properties no longer available

The **AdControl** class no longer has **Latitude** and **Longitude** properties for UWP apps. Instead, code built into the ad control will detect and send these values to the ad servers on the app’s behalf.


 

 
