---
author: mcleanbyron
ms.assetid: 3D6EE7D7-7D75-499D-AA7A-55DA1C485BA6
description: Use this method in the Windows Store analytics API to download the CAB file for a Windows 10 driver error. This method is intended only for IHVs.
title: Download the CAB file for a Windows 10 driver error
ms.author: mcleans
ms.date: 03/17/2017
ms.topic: article
ms.prod: windows
ms.technology: uwp
keywords: windows 10, uwp, Windows Store analytics API, download CAB
---

# Download the CAB file for a Windows 10 driver error

Use this method in the Windows Store analytics API to download the CAB file that is associated with a particular Windows 10 driver error. Before you can use this method, you must first use the [get details for a Windows 10 driver error](get-details-for-a-windows-10-driver-error.md) method to retrieve the ID of the CAB file you want to download.

You can get other info about OEM hardware errors by using the [get error reporting data for Windows 10 drivers](get-error-reporting-data-for-windows-10-drivers.md) and [get details for a Windows 10 driver error](get-details-for-a-windows-10-driver-error.md) methods in the Windows Store analytics API.

> [!NOTE]
> This method can only be used by developer accounts that belong to the [Windows Hardware Dev Center program](https://msdn.microsoft.com/windows/hardware/drivers/dashboard/get-started-with-the-hardware-dashboard).

## Prerequisites

To use this method, you need to first do the following:

* If you have not done so already, complete all the [prerequisites](access-analytics-data-using-windows-store-services.md#prerequisites) for the Windows Store analytics API.
* [Obtain an Azure AD access token](access-analytics-data-using-windows-store-services.md#obtain-an-azure-ad-access-token) to use in the request header for this method. After you obtain an access token, you have 60 minutes to use it before it expires. After the token expires, you can obtain a new one.
* Get the ID of the CAB file you want to download. To get this ID, use the [get details for a Windows 10 driver error](get-details-for-a-windows-10-driver-error.md) method to retrieve details for a specific driver error, and use the **cabIdHash** value in the response body of that method.

## Request


### Request syntax

| Method | Request URI                                                          |
|--------|----------------------------------------------------------------------|
| GET    | ```https://manage.devcenter.microsoft.com/v1.0/my/analytics/driver/cabdownload``` |

<span/> 

### Request header

| Header        | Type   | Description                                                                 |
|---------------|--------|-----------------------------------------------------------------------------|
| Authorization | string | Required. The Azure AD access token in the form **Bearer** &lt;*token*&gt;. |

<span/> 

### Request parameters

| Parameter        | Type   |  Description      |  Required  |
|---------------|--------|---------------|------|
| applicationId | string | The product ID value of the driver for which you want to retrieve error data. |  Yes  |
| cabIdHash | string | The unique ID of the CAB file you want to download. To get this ID, use the [get details for a Windows 10 driver error](get-details-for-a-windows-10-driver-error.md) method to retrieve details for a specific error in your app, and use the **cabIdHash** value in the response body of that method. |  Yes  |

<span/>
 
### Request example

The following example demonstrates how to download a CAB file using this method.

```syntax
GET https://manage.devcenter.microsoft.com/v1.0/my/analytics/driver/cabdownload?applicationId=18430592857500421&cabIdHash=c1a51104-d682-4230-be14-7278b18e3555 HTTP/1.1
Authorization: Bearer <your access token>
```

## Response

This method returns a 302 (redirect) response code, and the **Location** header in the response is assigned to the shared access signature (SAS) URI of the CAB file. The caller is redirected to this URI to automatically download the CAB file.

## Related topics

* [Get error reporting data for Windows 10 drivers](get-error-reporting-data-for-windows-10-drivers.md)
* [Get details for a Windows 10 driver error](get-details-for-a-windows-10-driver-error.md)
