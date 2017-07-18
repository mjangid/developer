﻿---
author: jnHs
Description: When you create a new add-on in the Windows Dev Center dashboard, you need to specify a product type and assign it a product ID.
title: Set your add-on product type and product ID
ms.assetid: 59497B0F-82F0-4CEE-B628-040EF9ED8D3D
ms.author: wdg-dev-content
ms.date: 06/28/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp
---

# Set your add-on product type and product ID

An add-on must be associated with an app that you've created in the dashboard already (even if you haven't submitted it yet). You can find the button to **Create a new add-on** on your app's **Overview** page or on its **Add-ons** page.

After you select **Create a new add-on**, you'll be prompted to specify a product type and assign a product ID for your add-on.

## Product type

First, you'll need to indicate which type of add-on you are offering. This selection refers to how the customer can use your add-on.

> [!NOTE] 
> You won't be able to change the product type after you save this page to create the add-on. If you choose the wrong product type, you can always delete your in-progress add-on submission and start over by creating a new add-on.

Select **Durable** as your proudct type if the add-on is typically purchased only once. Durable add-ons are often used to unlock additional functionality in an app. Durable add-ons are not consumed, but you can set the **Product lifetime** so that they expire after a set duration (with options from 1-365 days), in which case a customer could purchase the add-on again after it expires. The default **Product lifetime** for a durable add-on is **Forever**, which means the add-on never expires. You can change this to a different duration in the [Properties](enter-add-on-properties.md) step of the add-on submission process.

If the add-on can be purchased, used (consumed), and then purchased again, you'll want to select one of the **consumable** product types. Consumable add-ons are often used for things like in-game currency (gold, coins, etc.) which can be purchased in set amounts and then used up by the customer. For more info on including consumable add-ons in your app, see [Enable consumable add-on purchases](../monetize/enable-consumable-add-on-purchases.md).

There are two types of consumable add-ons that you can select:

- **Developer-managed consumable**: Supported on all OS versions. Balance and fulfillment must be managed within your app. 
- **Store-managed consumable:** Balance will be tracked by Microsoft across all of the customer’s devices running Windows 10, version 1607 or later; not supported on any earlier OS versions. To use this option, the parent product must be compiled using Windows 10 SDK version 14393 or later. Also note that you cannot submit a Store-managed consumable add-on to the Store until the parent product has been published (though you can create the submission in your dashboard and begin working on it at any time). You'll need to enter the quantity for your Store-managed consumable add-on in the **Properties** page.


## Product ID

Enter a unique product ID for your add-on. This name will be used to identify your add-on in the dashboard, and you can use this identifier to [refer to the add-on in your code](../monetize/in-app-purchases-and-trials.md#how-to-use-product-ids-for-add-ons-in-your-code).

Here are a few things to keep in mind when choosing a product ID:

-   Customers won't see this product ID. (Later, you can enter a [title and description](create-add-on-descriptions.md) to be displayed to customers.)
-   You can’t change or delete an add-on's product ID after it's been published.
-   A product ID can't be more than 100 characters in length.
-   A product ID cannot include any of the following characters: **&lt; &gt; \* % & : \\ ? + ,**
-   To offer your add-on in all OS versions, you must only use alphanumeric characters, periods, and/or underscores. If you use any other types of characters, the add-on will not be available for purchase to customers running Windows Phone 8.1 or earlier.
-   A product ID doesn't have to be unique within the Windows Store, but it must be unique to your developer account.
 




