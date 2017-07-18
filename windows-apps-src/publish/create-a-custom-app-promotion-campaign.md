﻿---
author: JnHs
Description: In addition to creating an ad campaign for your app that will run in Windows apps, you can also promote your app using other channels.
title: Create a custom app promotion campaign
ms.assetid: 7C9BF73E-B811-4FC7-B1DD-4A0C2E17E95D


ms.topic: article


keywords: windows 10, uwp, custom, app, promotion, campaign








There are two main types of data associated with custom campaigns: *page views* for your app's Store listing, and *conversions*. A conversion is an app acquisition that results from a customer viewing your app's Store listing page from a URL that includes a custom campaign ID. For more details about conversions, see [Understanding how app acquisitions qualify as conversions](#understanding-how-app-acquisitions-qualify-as-conversions) in this topic.

You can retrieve custom campaign performance data for your app in the following ways:










Consider a game developer who has finished building a new game and would like to promote it to players of her existing games. She posts the announcement of the new game release on her Facebook page, including a link to the Windows Store page for the game. Many of her players also follow her on Twitter, so she also tweets the announcement with the link to the Windows Store page for the game.

To track the success of each of these promotion channels, the developer creates two variants of the URL for the Windows Store page for the game:

* The URL she will post to her Facebook page includes the custom campaign ID `my-facebook-campaign`.





<span id="conversions" />


A custom campaign *conversion* is an acquisition that results from a customer clicking a URL that is promoted via a custom campaign. There are different scenarios for qualifying as a conversion for the **App page views and conversions by campaign ID** and **Total campaign conversions** charts in the [Acquisitions report](acquisitions-report.md) in the Dev Center dashboard and for qualifying as a conversion for [programmatically retrieving the campaign ID](#programmatically).





* A customer *with or without a recognized Microsoft account* clicks an app URL that contains a custom campaign ID and is redirected to the Store listing for the app. Then, that same customer acquires the app within 24 hours after they first clicked the Windows Store URL with the custom campaign ID.


> [!NOTE]
> For app acquisitions that are counted as conversions for a custom campaign, any add-on purchases in that app are also counted as conversions for the same custom campaign.







* On a device running **Windows 10, version 1511, or earlier**: A customer (who must be signed in with a recognized Microsoft account) clicks a URL that contains a custom campaign ID and is redirected to the Store listing page for the app. The customer acquires the app while viewing the Store listing as a result of clicking the URL.





## Embed a custom campaign ID to your app's Windows Store page URL




   > [!NOTE]
   > The campaign ID string may be visible to other developers when they view the [Acquisitions report](acquisitions-report.md) for their apps. This can occur when a customer clicks your custom campaign ID to enter the Store and purchases another developer’s app within the same session, thus attributing that conversion to your campaign ID. That developer will see how many conversions of their own app resulted from an initial click on your campaign ID, including the name of the campaign ID, but they will not see any data about how many users purchased your own apps (or apps from any other developers) after clicking your campaign ID.

2.  Get the Windows Store link for your app in HTML or protocol format.

    * Use the HTML URL if you want customers to navigate to your app's web-based Store listing in a browser on any operating system. On Windows devices, the Store app will also launch and display your app's listing. This URL has the format **`https://www.microsoft.com/store/apps/*your app ID*`**. For example, the HTML URL for Skype is `https://www.microsoft.com/store/apps/9wzdncrfj364`. You can find this URL on your [App identity](https://docs.microsoft.com/en-us/windows/uwp/publish/view-app-identity-details.md#link-to-your-apps-listing) page.

    * Use the protocol format if you are promoting your app from within other Windows apps that are running on a device or computer with the Windows Store app installed, or when you know that your customers are on a device which supports the Windows Store. This link will go directly to your app's Store listing without opening a browser. This URL has the format **`ms-windows-store://pdp/?PRODUCTID=*your app id*`**. For example, the protocol URL for Skype is `ms-windows-store://pdp/?PRODUCTID=9wzdncrfj364`.

3.  Append the following string to the end of the URL for your app:

    * For an HTML format URL, append **`?cid=*my custom campaign ID*`**. For example, if Skype introduces a campaign ID with the value **custom\_campaign**, the new URL including the campaign ID would be: `https://www.microsoft.com/store/apps/skype/9wzdncrfj364?cid=custom\_campaign`.

    * For a protocol format URL, append **`&cid=*my custom campaign ID*`**. For example, if Skype introduces a campaign ID with the value **custom\_campaign**, the new protocol URL including the campaign ID would be: `ms-windows-store://pdp/?PRODUCTID=9wzdncrfj364&cid=custom\_campaign`.






These APIs will return a campaign ID string only if the customer clicked your URL with the embedded campaign ID, viewed the Windows Store page for your app, and then acquires your app without leaving the Store listing page. If the user leaves the page and then later returns and acquires the app, this will not [qualify as a conversion](#conversions) when using these APIs.

There are different APIs for you to use depending on the version of Windows 10 that your app targets:

* Windows 10, version 1607, or later: Use the [**StoreContext**](https://docs.microsoft.com/uwp/api/windows.services.store.storecontext) class in the **Windows.Services.Store** namespace. When using this API, you can retrieve custom campaign IDs for any [qualified acquisitions](#conversions), whether or not the user is signed in with a recognized Microsoft account.
* Windows 10, version 1511, or earlier: Use the [**CurrentApp**](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.store.currentapp.aspx) class in the **Windows.ApplicationModel.Store** namespace. When using this API, you can only retrieve custom campaign IDs for [qualified acquisitions](#conversions) where the user is signed in with a recognized Microsoft account.


> Although the **Windows.ApplicationModel.Store** namespace is available in all versions of Windows 10, we recommend that you use the APIs in the **Windows.Services.Store** namespace if your app targets Windows 10, version 1607, or later. For more information about the differences between these namespaces, see [In-app purchases and trials](../monetize/in-app-purchases-and-trials.md#choose-namespace). The following code example shows how to structure your code to use both APIs in the same project.





``` csharp

This code does the following:
1. First, it checks to see if the [**StoreContext**](https://docs.microsoft.com/uwp/api/windows.services.store.storecontext) class in the **Windows.Services.Store** namespace is available on the current device (this means the device is running Windows 10, version 1607, or later). If so, the code proceeds to use this class.
2. Next, it attempts to get the custom campaign ID for the case where the current user has a recognized Microsoft account. To do this, the code gets a [**StoreSku**](https://docs.microsoft.com/uwp/api/Windows.Services.Store.StoreSku) object that represents the current app SKU, and then it accesses the [**CampaignId**](https://docs.microsoft.com/uwp/api/windows.services.store.storecollectiondata#Windows_Services_Store_StoreCollectionData_CampaignId) property to retrieve the campaign ID, if one is available.
3. The code then attempts to retrieve the campaign ID for the case where the current user does not have a recognized Microsoft account. In this case, the campaign ID is embedded in the app license. The code retrieves the license by using the [**GetAppLicenseAsync**](https://docs.microsoft.com/uwp/api/windows.services.store.storecontext#Windows_Services_Store_StoreContext_GetAppLicenseAsync) method and then parses the JSON contents of the license for the value of a key named *customPolicyField1*. This value contains the campaign ID.
4. If the [**StoreContext**](https://docs.microsoft.com/uwp/api/windows.services.store.storecontext) class in the **Windows.Services.Store** namespace is not available, the code then falls back to using the [**GetAppPurchaseCampaignIdAsync**](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.store.currentapp.getapppurchasecampaignidasync.aspx) method in the **Windows.ApplicationModel.Store** namepsace to retrieve the custom campaign ID (this namespace is available in all versions of Windows 10, including version 1511 and earlier). Note that when using this method, you can only retrieve custom campaign IDs for [qualified acquisitions](#conversions) where the user has a recognized Microsoft account.

  > [!NOTE]



  > [!NOTE]
  > The **Windows.Services.Store** namespace does not provide a class that you can use to simulate license info during testing. Instead, you must publish an app to the Store and download that app to your development device to use its license for testing. For more information, see [In-app purchases and trials](../monetize/in-app-purchases-and-trials.md#testing).




Before you promote a custom campaign URL, we recommend that you test your custom campaign by doing the following:
1.  Sign in to a Microsoft account on the device you are using for testing.


