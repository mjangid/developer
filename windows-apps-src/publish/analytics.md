---
author: JnHs
Description: Get detailed analytics for your Windows apps, in the dashboard or via other methods.
title: Analyze app performance
ms.assetid: 3A3C6F10-0DB1-416D-B632-CD388EA66759
ms.author: wdg-dev-content
ms.date: 06/28/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, analytics, reports, dashboard, apps
---

# Analyze app performance

You can view detailed analytics for your apps in the Windows Dev Center dashboard. Statistics and charts let you know how your apps are doing, from how many customers you've reached to how they're using your app and what they have to say about it. You can also find metrics on app health, ad usage, and more.

You can view analytic reports in the dashboard, or [download the reports you need](download-analytic-reports.md) to analyze your data offline. We also provide several ways for you to [access your analytics data without using the dashboard](#no-dashboard).

## View key analytics for all your apps

To view key analytics about your most downloaded apps, expand **Analyze** and select **Overview**. By default, the **Analytics overview** page shows info about your five apps that have the most lifetime acquisitions. To choose different published apps to show, select **Filters**.

## View individual reports for each app

In this section you'll find details about the info presented in each of the following reports:

-   [Acquisitions report](acquisitions-report.md)
-   [Add-on acquisitions report](add-on-acquisitions-report.md)
-   [Usage report](usage-report.md)
-   [Health report](health-report.md)
-   [Reviews report](reviews-report.md)
-   [Feedback report](feedback-report.md)
-   [Advertising performance report](advertising-performance-report.md)
-   [Ad campaign report](promote-your-app-report.md)

> [!NOTE]
> You may not see data in all of these reports, depending on your app's specific features and implementation.

<span id="no-dashboard"/>
## Access analytics data without using the Dev Center dashboard

In addition to the analytic reports in the dashboard, there are several other ways to access your analytic data.

### Windows Store analytics API

Use the [Windows Store analytics API](../monetize/access-analytics-data-using-windows-store-services.md) to programmatically retrieve analytics data for your apps. This REST API enables you to retrieve data for app and add-on acquisitions, errors, app ratings and reviews. This API uses Azure Active Directory (Azure AD) to authenticate the calls from your app or service.

### Windows Dev Center content pack for Power BI

Use the [Windows Dev Center content pack for Power BI](https://powerbi.microsoft.com/documentation/powerbi-content-pack-windows-dev-center/) to explore and monitor your Dev Center analytics data in Power BI. Power BI is a cloud-based business analytics service that gives you a single view of your business data.

Use the following resources to get started using Power BI to access your analytics data.

* [Sign up for Power BI](https://powerbi.microsoft.com/documentation/powerbi-service-self-service-signup-for-power-bi/)
* [Learn how to use Power BI](https://powerbi.microsoft.com/guided-learning/)
* [Learn how to use the Windows Dev Center content pack for Power BI to connect to your analytics data](https://powerbi.microsoft.com/documentation/powerbi-content-pack-windows-dev-center/)

> [!NOTE]
> To connect to the Windows Dev Center content pack for Power BI, we recommend that you specify credentials from an Azure AD directory that is associated with your Dev Center account. If you use your Microsoft account credentials, your analytics data in Power BI does not refresh automatically, and you will need to sign in to Power BI to refresh your data. If your organization already uses Office 365 or other business services from Microsoft, you already have Azure AD. Otherwise, you can [get it for free](http://go.microsoft.com/fwlink/p/?LinkId=703757). For more information about associating your Dev Center account with an Azure AD, see [Manage account users](manage-account-users.md).

### Dev Center app

Install the [Dev Center](https://www.microsoft.com/store/apps/dev-center/9nblggh4r5ws) app to quickly view details about the health and performance of your apps on any Windows 10 device.

