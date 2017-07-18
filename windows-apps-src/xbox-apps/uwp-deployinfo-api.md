---
author: WilliamsJason
title: Device Portal deploy info API reference
description: Learn how to access the deploy info API programatically.
---

# Requests deployment information for one or more installed packages.

**Request**

Method      | Request URI
:------     | :------
POST | /ext/app/deployinfo
<br />
**URI parameters**

 - None

**Request headers**

- None

**Request body**

A JSON array in the following format:

* DeployInfo
  * PackageFullName - Name of the package that we are requesting information about.

###Response

**Response body**

A JSON array in the following format:

* DeployInfo
  * PackageFullName - Name of the package that we are receiving information about.
  * DeployType - The type of deployment.
  * DeployPathOrSpecifiers - A deploy path for loose deployments or installed specifiers for packaged deployments.

**Status code**

This API has the following expected status codes.

HTTP status code      | Description
:------     | :-----
200 | Success
4XX | Error codes
5XX | Error codes
<br />

**Available device families**

* Windows Xbox