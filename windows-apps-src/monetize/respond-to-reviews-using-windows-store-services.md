---
author: mcleanbyron
ms.assetid: c92c0ea8-f742-4fc1-a3d7-e90aac11953e
description: Use the Windows Store reviews API to programmatically submit responses to reviews of your app in the Store.
title: Respond to reviews using Store services
ms.author: mcleans
ms.date: 02/08/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, Windows Store reviews API, respond to reviews
---

# Respond to reviews using Store services

Use the *Windows Store reviews API* to programmatically respond to reviews of your app in the Store. This API is especially useful for developers who want to bulk respond to many reviews without using the Windows Dev Center dashboard. This API uses Azure Active Directory (Azure AD) to authenticate the calls from your app or service.

The following steps describe the end-to-end process:

1.  Make sure that you have completed all the [prerequisites](#prerequisites).
2.  Before you call a method in the Windows Store reviews API, [obtain an Azure AD access token](#obtain-an-azure-ad-access-token). After you obtain a token, you have 60 minutes to use this token in calls to the Windows Store reviews API before the token expires. After the token expires, you can generate a new token.
3.  [Call the Windows Store reviews API](#call-the-windows-store-reviews-api).

> [!NOTE]
> In addition to using the Windows Store reviews API to programmatically respond to reviews, you can alternatively respond to reviews [using the Windows Dev Center dashboard](../publish/respond-to-customer-reviews.md).

<span id="prerequisites" />
## Step 1: Complete prerequisites for using the Windows Store reviews API

Before you start writing code to call the Windows Store reviews API, make sure that you have completed the following prerequisites.

* You (or your organization) must have an Azure AD directory and you must have [Global administrator](http://go.microsoft.com/fwlink/?LinkId=746654) permission for the directory. If you already use Office 365 or other business services from Microsoft, you already have Azure AD directory. Otherwise, you can [create a new Azure AD in Dev Center](../publish/associate-azure-ad-with-dev-center.md#create-a-brand-new-azure-ad-to-associate-with-your-dev-center-account) for no additional charge.

* You must associate an Azure AD application with your Dev Center account, retrieve the tenant ID and client ID for the application and generate a key. The Azure AD application represents the app or service from which you want to call the Windows Store reviews API. You need the tenant ID, client ID and key to obtain an Azure AD access token that you pass to the API.
    > [!NOTE]
    > You only need to perform this task one time. After you have the tenant ID, client ID and key, you can reuse them any time you need to create a new Azure AD access token.

To associate an Azure AD application with your Dev Center account and retrieve the required values:

1.  In Dev Center, go to your **Account settings**, click **Manage users**, and [associate your organization's Dev Center account with your organization's Azure AD directory](../publish/associate-azure-ad-with-dev-center.md).

2.  In the **Manage users** page, click **Add Azure AD applications**, add the Azure AD application that represents the app or service that you will use to manage promotion campaigns for your Dev Center account, and assign it the **Manager** role. If this application already exists in your Azure AD directory, you can select it on the **Add Azure AD applications** page to add it to your Dev Center account. Otherwise, you can create a new Azure AD application on the **Add Azure AD applications** page. For more information, see [Add Azure AD applications to your Dev Center account](../publish/add-users-groups-and-azure-ad-applications.md#azure-ad-applications).

3.  Return to the **Manage users** page, click the name of your Azure AD application to go to the application settings, and copy down the **Tenant ID** and **Client ID** values.

4. Click **Add new key**. On the following screen, copy down the **Key** value. You won't be able to access this info again after you leave this page. For more information, see [Manage keys for an Azure AD application](../publish/add-users-groups-and-azure-ad-applications.md#manage-keys).

<span id="obtain-an-azure-ad-access-token" />
## Step 2: Obtain an Azure AD access token

Before you call any of the methods in the Windows Store reviews API, you must first obtain an Azure AD access token that you pass to the **Authorization** header of each method in the API. After you obtain an access token, you have 60 minutes to use it before it expires. After the token expires, you can refresh the token so you can continue to use it in further calls to the API.

To obtain the access token, follow the instructions in [Service to Service Calls Using Client Credentials](https://azure.microsoft.com/documentation/articles/active-directory-protocols-oauth-service-to-service/) to send an HTTP POST to the ```https://login.microsoftonline.com/<tenant_id>/oauth2/token``` endpoint. Here is a sample request.

```syntax
POST https://login.microsoftonline.com/<tenant_id>/oauth2/token HTTP/1.1
Host: login.microsoftonline.com
Content-Type: application/x-www-form-urlencoded; charset=utf-8

grant_type=client_credentials
&client_id=<your_client_id>
&client_secret=<your_client_secret>
&resource=https://manage.devcenter.microsoft.com
```

For the *tenant\_id* value in the POST URI and the *client\_id* and *client\_secret* parameters, specify the tenant ID, client ID and the key for your application that you retrieved from Dev Center in the previous section. For the *resource* parameter, you must specify ```https://manage.devcenter.microsoft.com```.

After your access token expires, you can refresh it by following the instructions [here](https://azure.microsoft.com/documentation/articles/active-directory-protocols-oauth-code/#refreshing-the-access-tokens).

<span id="call-the-windows-store-reviews-api" />
## Step 3: Call the Windows Store reviews API

After you have an Azure AD access token, you are ready to call the Windows Store reviews API. You must pass the access token to the **Authorization** header of each method.

The Windows Store reviews API contains several methods you can use to determine whether you are allowed to respond to a given review and to submit responses to one or more reviews. Follow this process to use this API:

1. Get the IDs of the reviews you want to respond to. Review IDs are available in the response data of the [get app reviews](get-app-reviews.md) method in the Windows Store analytics API and in the [offline download](../publish/download-analytic-reports.md) of the [Reviews report](../publish/reviews-report.md).
2. Call the [get response info for app reviews](get-response-info-for-app-reviews.md) method to determine whether you are allowed to respond to the reviews. When a customer submits a review, they can choose not to receive responses to their review. You cannot respond to reviews submitted by customers who have chosen not to receive review responses.
3. Call the [submit responses to app reviews](submit-responses-to-app-reviews.md) method to programmatically respond to the reviews.


## Related topics

* [Get app reviews](get-app-reviews.md)
* [Get response info for app reviews](get-response-info-for-app-reviews.md)
* [Submit responses to app reviews](submit-responses-to-app-reviews.md)

 
