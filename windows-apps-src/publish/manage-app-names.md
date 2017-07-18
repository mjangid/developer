﻿---
author: jnHs
Description: View the names that you've reserved for your app, reserve additional names (for other languages or to change your app's name), and delete reserved names that you don't need anymore.
title: Manage app names
ms.assetid: D95A6227-746E-4729-AE55-648A7102401C
ms.author: wdg-dev-content
ms.date: 06/28/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp
---

# Manage app names


You can view all of the names that you've reserved for your app, reserve additional names (for other languages or to change your app's name), and delete names you don't need. To do this, go to the **Manage app names** page in the **App management** section for any of your apps in the Windows Dev Center dashboard.

## Reserve additional names for your app

You can reserve multiple app names to use for the same app. This is especially useful if you are offering your app in multiple languages and want to use different names for different languages. You can also reserve a new name in order to change the name of an app.

In the **Reserve more names** section of the **Manage app names** page, you'll see a text box. Enter the name you'd like to reserve, then click **Check availability**. If the name is available, click **Reserve product name**.

> [!NOTE]
> For more info about reserving app names, and why a certain name may not be available, see [Create your app by reserving a name](create-your-app-by-reserving-a-name.md).

You can continue reserving additional app names here if desired.

## Delete app names

If you no longer want to use a name you've previously reserved, you can release it by deleting it here. Make sure you're certain before you do so, since this means that the name will immediately become available for someone else to reserve and use.

To delete one of your app's reserved names, find the name you no longer want to use and then click **Delete**. In the confirmation dialog, click **Delete** again to confirm.

Note that your app needs to have at least one reserved name. To completely remove an app from your dashboard (and release all the names you've reserved for that app), click **Delete this app** from the **App overview** page. If you have a submission for the app in progress, you'll need to delete that submission first. If you've already published the app to the Store, you can't delete it from your dashboard (though you can use the **Show/hide products** functionality on your **Overview** page to hide it). 

## Rename an app that has already been published

If your app is already in the Store and you want to rename it, you can do so by reserving a new name for it (by following the steps described above) and then creating a new submission for the app.

You must update your app's package(s) to include the new name in order for the Store to display it under the new name. First, update the Package.StoreAssociation.xml file to use the new name, either manually or by using Visual Studio (**Project > Store > Associate App with the Store...**). For more info, see [Packaging UWP apps](../packaging/packaging-uwp-apps.md).

You'll also need to update the [**Package/Properties/DisplayName**](https://docs.microsoft.com/uwp/schemas/appxpackage/appxmanifestschema/element-1-displayname) element in your app manifest, and update any graphics or text that includes the app's name. 

> [!IMPORTANT]
> Be sure to update the Package.StoreAssociation.xml file before you change the **Package/Properties/DisplayName** in the app manifest, or you may get an error.

You'll also want to review your app's Store listing, and change the name if you mention it there. Once your app has been published with the new name, you can delete the old name that you no longer need to use.

 

 




