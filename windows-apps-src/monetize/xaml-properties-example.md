---
author: mcleanbyron
ms.assetid: d074e9d5-b3e0-4f16-b1e4-02b32ac99b2c
description: Learn how to assign **AdControl** properties to values.
title: AdControl XAML properties example
ms.author: mcleans
ms.date: 02/08/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, ads, advertising, AdControl, XAML, properties
---

# AdControl XAML properties example

The following XAML example demonstrates how to assign [AdControl](https://msdn.microsoft.com/library/windows/apps/microsoft.advertising.winrt.ui.adcontrol.aspx) properties to values. If a property is not set, the **AdControl** will use default values to create an ad that is consistent with the user experience of the app.

The values are examples. In your code you will set the values of these functions and properties appropriate for your app.

> [!div class="tabbedCodeSnippets"]
``` xml
<UI:AdControl Width="300",
    Height="250",
    AdUnitId="test",
    ApplicationId="3f83fe91-d6be-434d-a0ae-7351c5a997f1",
    IsAutoRefreshEnabled="false",
    AdRefreshed="OnAdRefresh",
    ErrorOcurred="OnAdError",
    IsEngagedChanged="OnAdEngagedChanged" />
```

## Related topics

* [AdControl in XAML and .NET](adcontrol-in-xaml-and--net.md)
* [Advertising samples on GitHub](http://aka.ms/githubads)

 
