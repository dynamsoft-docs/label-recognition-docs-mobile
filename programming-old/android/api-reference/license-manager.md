---
layout: default-layout
title: Dynamsoft Core Module Android API Reference - LicenseManager class
description: This page shows LicenseManager class of Dynamsoft Core Module for Android SDK.
keywords: initLicense, LicenseManager, api reference, android
needAutoGenerateSidebar: true
noTitleIndex: true
pageStartVer: 1.0
permalink: /programming/android/api-reference/license-manager.html
---

# LicenseManager

> You are viewing a history document page of Dynamsoft Label Recognizer Android v2.2.20.

The LicenseManager class unlocks the Dynamsoft SDK with a purchased full license or a provided trial license to allow you to develop your application.

```java
class com.dynamsoft.core.LicenseManager
```

## Methods

  | Method               | Description |
  |----------------------|-------------|
  | [`initLicense`](#initlicense) | Read the license key and activate the SDK. |

  ---

### initLicense

Read the license key and activate the SDK.

```java
static void initLicense(String license, android.content.Context context, LicenseVerificationListener listener)
```

**Parameters**

`[in] license` The license key.  
`[in] context` The interface to global information about an application environment.  
`[in] listener` The listener that handles callback when the license server returns.  

**Code Snippet**

```java
LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", MainActivity.this, new LicenseVerificationListener() {
   @Override
   public void LicenseVerificationCallback(boolean isSuccess, Exception error) {
      if(!isSuccess){
         error.printStackTrace();
      }
   }
});
```
