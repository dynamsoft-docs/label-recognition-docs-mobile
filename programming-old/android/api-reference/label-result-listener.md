---
layout: default-layout
title: Interface LabelResultListener - Dynamsoft Label Recognizer Android API Reference
description: This the interface LabelResultListener page of Dynamsoft Label Recognizer for Android SDK.
keywords: LabelResultListener, interface, android
needAutoGenerateSidebar: true
needGenerateH3Content: false
noTitleIndex: true
permalink: /programming/android/api-reference/label-result-listener.html
---

# LabelResultListener

`LabelResultListener` is the interface to handle callbacks when the detection results are returned.

```java
interface com.dynamsoft.dlr.LabelResultListener
```

| Method | Description |
| ------ | ----------- |
| `labelResultCallback` | The callback method to handle the recognized label results returned by the library. |

## labelResultCallback

The callback method to handle the recognized label results returned by the library.

```java
void labelResultCallback(int frameId, ImageData imageData, DLRResult[] labelResults);
```

**Parameters**

`[in] frameId` The ID of the frame.  
`[in] imgData` The image data of frame.  
`[in] labelResults` Recognized label results of the frame.

**Code Snippet**

```java
LabelResultListener labelResultListener = new LabelResultListener() {
    @Override
    public void labelResultCallback(int frameId, ImageData imageData, DLRResult[] labelResults) {
        // Add your code
    }
};
```
