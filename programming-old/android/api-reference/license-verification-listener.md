---
layout: default-layout
title: Interface LicenseVerificationListener - Dynamsoft Core Module Android API Reference
description: This page shows interface LicenseVerificationListener of Dynamsoft Core Module for Android SDK.
keywords: initLicense, LicenseVerificationListener, api reference, android
needAutoGenerateSidebar: true
noTitleIndex: true
pageStartVer: 1.0
permalink: /programming/android/api-reference/license-verification-listener.html
---

# LicenseVerificationListener

`LicenseVerificationListener` is the interface to handle callback when message is output by license server.

```java
interface com.dynamsoft.core.LicenseVerificationListener
```

## Methods

| Method               | Description |
|----------------------|-------------|
| [`licenseVerificationCallback`](#licenseverificationcallback) | The callback of license server. It contains error message when license verification is failed. |

### LicenseVerificationCallback

The callback of license server. It contains error message when license verification is failed.

```java
void licenseVerificationCallback(boolean isSuccess, CoreException error);
```

**Parameters**

`[in] isSuccess`: Whether the license verification was successful.  
`[in out] error`: The error message from license server.

**Code Snippet**

```java
LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", MainActivity.this, new LicenseVerificationListener() {
   @Override
   public void licenseVerificationCallback(boolean isSuccess, CoreException error) {
      if(!isSuccess){
         error.printStackTrace();
      }
   }
});
```
