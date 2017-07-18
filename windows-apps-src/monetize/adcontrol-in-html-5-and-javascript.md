---
author: mcleanbyron
ms.assetid: adb2fa45-e18f-4254-bd8b-a749a386e3b4
description: Learn how to use the AdControl class to display banner ads in a JavaScript/HTML app for Windows 10 (UWP), Windows 8.1, or Windows Phone 8.1.
title: AdControl in HTML 5 and JavaScript
ms.author: mcleans
ms.date: 06/26/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, ads, advertising, AdControl, ad control, javascript, HTML
---

# AdControl in HTML 5 and JavaScript

This walkthrough shows how to use the [AdControl](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.adcontrol.aspx) class to display banner ads in a JavaScript/HTML app for Windows 10 (UWP), Windows 8.1, or Windows Phone 8.1.

For a complete sample project that demonstrates how to add banner ads to a JavaScript/HTML app, see the [advertising samples on GitHub](http://aka.ms/githubads).

## Prerequisites


* For UWP apps: install the [Microsoft Advertising SDK](http://aka.ms/ads-sdk-uwp) with Visual Studio 2015 or a later release.
* For Windows 8.1 or Windows Phone 8.1 apps: install the [Microsoft Advertising SDK for Windows and Windows Phone 8.x](http://aka.ms/store-8-sdk) with Visual Studio 2015 or Visual Studio 2013.

> [!NOTE]
> If you are adding banner ads to a UWP app and you have installed the Windows 10 SDK version 10.0.14393 (Anniversary Update) or a later version of the Windows SDK, you must also install the WinJS library. This library used to be included in previous versions of the Windows SDK for Windows 10, but starting with the Windows 10 SDK version 10.0.14393 (Anniversary Update) this library must be installed separately. To install WinJS, see [Get WinJS](http://try.buildwinjs.com/download/GetWinJS/).

## Code development

1. In Visual Studio, open your project or create a new project.

2. If your project targets **Any CPU**, update your project to use an architecture-specific build output (for example, **x86**). If your project targets **Any CPU**, you will not be able to successfully add a reference to the Microsoft advertising library in the following steps. For more information, see [Reference errors caused by targeting Any CPU in your project](known-issues-for-the-advertising-libraries.md#reference_errors).

3.  From the **Solution Explorer** window, right click **References**, and select **Add Reference…**

4.  In **Reference Manager**, select one of the following references depending on your project type:

    -   For a Universal Windows Platform (UWP) project: Expand **Universal Windows**, click **Extensions**, and then select the check box next to **Microsoft Advertising SDK for JavaScript** (Version 10.0).

    -   For a Windows 8.1 project: Expand **Windows 8.1**, click **Extensions**, and then select the check box next to **Microsoft Advertising SDK for Windows 8.1 Native (JS)**.

    -   For a Windows Phone 8.1 project: Expand **Windows Phone 8.1**, click **Extensions**, and then select the check box next to **Microsoft Advertising SDK for Windows Phone 8.1 Native (JS)**.

    ![javascriptaddreference](images/13-f7f6d6a6-161e-4f17-995d-1236d0b5d9f2.png)

5.  In **Reference Manager**, click OK.

6.  Open the index.html file (or other html file as appropriate for your project).

7.  In the **&lt;head&gt;** section, after the project’s JavaScript references of default.css and main.js, add the reference to ad.js.

    In a UWP project, add the following code.

    ``` HTML
    <!-- Advertising required references -->
    <script src="//Microsoft.Advertising.JavaScript/ad.js"></script>
    ```

    In a Windows 8.1 or Windows Phone 8.1 project, add the following code.

    ``` HTML
    <!-- Advertising required references -->
    <script src="/MSAdvertisingJS/ads/ad.js"></script>
    ```

    > [!NOTE]
    > This line must be placed in the **&lt;head&gt;** section after the include of main.js; otherwise, you will encounter an error when you build your project. If your project targets Windows 8.1 or Windows Phone 8.1, the default HTML file in your project is named default.html instead of index.html, and the default JavaScript file in your project is named default.js instead of main.js.

8.  Modify the **&lt;body&gt;** section in the default.html file (or other html file as appropriate for your project) to include the div for the **AdControl**. Assign the **applicationId** and **adUnitId** properties in the **AdControl** to the test values provided in [Test mode values](test-mode-values.md). Also adjust the height and width of the control so it is one of the [supported ad sizes for banner ads](supported-ad-sizes-for-banner-ads.md).

    > [!NOTE]
    > Every **AdControl** has a corresponding *ad unit* that is used by our services to serve ads to the control, and every ad unit consists of an *ad unit ID* and *application ID*. In these steps, you assign test ad unit ID and application ID values to your control. These test values can only be used in a test version of your app. Before you publish your app to the Store, you must [replace these test values with live values](#release) from Windows Dev Center.

    ``` HTML
    <div id="myAd" style="position: absolute; top: 50px; left: 0px; width: 300px; height: 250px; z-index: 1"
        data-win-control="MicrosoftNSJS.Advertising.AdControl"
        data-win-options="{applicationId: '3f83fe91-d6be-434d-a0ae-7351c5a997f1', adUnitId: 'test'}">
    </div>
    ```

9.  Compile and run the app to see it with an ad.

The following example shows the complete index.html for a simple UWP app.

``` HTML
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <title>AdControlExampleApp</title>
    <!-- WinJS references -->
    <link href="lib/winjs-4.0.1/css/ui-light.css" rel="stylesheet" />
    <script src="lib/winjs-4.0.1/js/base.js"></script>
    <script src="lib/winjs-4.0.1/js/ui.js"></script>
    <!-- AdControlExampleApp references -->
    <link href="css/default.css" rel="stylesheet" />
    <script src="js/main.js"></script>
    <!-- Required reference for AdControl -->
    <script src="//Microsoft.Advertising.JavaScript/ad.js"></script>
</head>
<body>
    <div id="myAd" style="position: absolute; top: 50px; left: 0px; width: 300px; height: 250px; z-index: 1"
      data-win-control="MicrosoftNSJS.Advertising.AdControl"
      data-win-options="{applicationId: '3f83fe91-d6be-434d-a0ae-7351c5a997f1', adUnitId: 'test'}">
    </div>
    <p>Content goes here</p>
</body>
</html>
```

<span id="release" />
## Release your app with live ads using Windows Dev Center

1.  In the Dev Center dashboard, go to the [Monetize with ads](../publish/monetize-with-ads.md) page for your app and [create an ad unit](../monetize/set-up-ad-units-in-your-app.md). For the ad unit type, specify **Banner**. Make note of both the ad unit ID and the application ID.

2. If your app is a UWP app for Windows 10, you can optionally enable ad mediation for the **AdControl** by configuring the settings in the [Ad mediation](../publish/monetize-with-ads.md#mediation) section on the [Monetize with ads](../publish/monetize-with-ads.md) page. Ad mediation enables you to maximize your ad revenue and app promotion capabilities by displaying ads from multiple ad networks, including ads from other paid ad networks such as Taboola and Smaato and ads for Microsoft app promotion campaigns.

3.  In your code, replace the test ad unit values (**applicationId** and **adUnitId**) with the live values you generated in Dev Center.

4.  [Submit your app](../publish/app-submissions.md) to the Store using the Dev Center dashboard.

5.  Review your [advertising performance reports](../publish/advertising-performance-report.md) in the Dev Center dashboard.             

<span id="manage" />
## Manage ad units for multiple ad controls in your app

You can use multiple **AdControl** objects in a single app (for example, each page in your app might host a different **AdControl** object). In this scenario, we recommend that you assign a different ad unit to each control. Using different ad units for each control enables you to separately [configure the mediation settings](../publish/monetize-with-ads.md#mediation) and get discrete [reporting data](../publish/advertising-performance-report.md) for each control. This also enables our services to better optimize the ads we serve to your app.

> [!IMPORTANT]
> You can use each ad unit in only one app. If you use an ad unit in more than one app, ads will not be served for that ad unit.

## Related topics

* [Advertising samples on GitHub](http://aka.ms/githubads)
* [Set up ad units for your app](../monetize/set-up-ad-units-in-your-app.md)
