﻿---
author: JnHs
Description: Target specific segments of your customers with personalized content to increase engagement, retention, and monetization.
title: Use targeted offers to maximize engagement and conversions
ms.author: wdg-dev-content
ms.date: 07/17/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, targeted offers, offers, notifications
---

# Use targeted offers to maximize engagement and conversions

Target specific segments of your customers with attractive, personalized content to increase engagement, retention, and monetization. In some cases, targeted offers may be associated with a Microsoft-sponsored promotion that pays a bonus to developers for each successful conversion, allowing you to earn even more.

> [!IMPORTANT]
> Targeted offers can only be used with UWP apps that include add-ons.

## Targeted offer overview

At a high level, you need to do three things to use targeted offers:

1. **Create the offer in your dashboard.** Navigate to the **Engage > Targeted offers** page to create offers. More info about this process is described below.
2. **Implement the in-app offer experience.** Use the *Windows Store targeted offers API* in your app's code to retrieve the available offers for a given user, and to claim the offer (if associated with a promotion). You'll also need to create the in-app experience for the targeted offer. For more info, see [Manage targeted offers using Store services](../monetize/manage-targeted-offers-using-windows-store-services.md).
3. **Submit your app to the Store.** Your app must be published with the in-app offer experience in place in order for the offer(s) be made available to customers.

After you complete these steps, customers using your app will see the offers that are available to them at that time, based in their membership in the segment(s) associated with your offers. Please note that while we’ll make every effort to show all available offers to your customers, there may occasionally be issues that impact offer availability.


## To create and send a targeted offer

Follow these steps to create a targeted offer in the dashboard. 

1.  In the Windows Dev Center dashboard, expand **Engage** in the left navigation menu, then select **Targeted offers**.
2.  On the **Targeted offers** page, review the available offers. Select **Create new offer** for any offer you wish to implement. 

    > [!NOTE]
    > The available offers you will see may vary over time and based on account criteria. Initially, you will see one or more offers using predefined segment criteria. Soon, we'll allow you to create targeted offers based on [customer segments that you define](create-customer-segments.md).

3.  In the new row that appears below the available offers, choose the product (app) in which the offer will be available. Then, select the add-on that you want to associate with the offer. 
4.  Repeat steps 2 and 3 if you'd like to create additional offers. You can implement the same offer type more than once for the same app, as long as you select different add-ons for each offer. Additionally, you can associate the same add-on with more than one offer type.
5.  When you are finished creating offers, click **Save**.

After you've implemented your offers, you can return to the **Targeted offers** page in your dashboard to view the total conversions for each offer. 

If you decide not to use an offer (or if you no longer want to keep using it, click **Delete.**

> [!IMPORTANT]
> Be sure you have published the code to retrieve the available offers for a given user, and to create the in-app experience. For more info, see [Manage targeted offers using Store services](../monetize/manage-targeted-offers-using-windows-store-services.md).
> 
> When considering the content of your targeted offers, keep in mind that, as with all app content, the content in your offers must comply with the Store [Content Policies](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#content_policies).
> 
> Also be aware that if a customer who uses your app (and is signed in with their Microsoft account at the time the segment membership is determined) gives their device to someone else to use, the other person may see offers that were targeted at the original customer. 

