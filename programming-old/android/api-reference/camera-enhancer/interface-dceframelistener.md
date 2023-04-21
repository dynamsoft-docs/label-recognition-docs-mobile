---
layout: default-layout
title: Android DCEFrameListener - Dynamsoft Label Recognizer Documents
description: This is the documentation - DCEFrameListener page of Dynamsoft Camera Enhancer.
keywords:  Camera Enhancer, DCEFrameListener
needAutoGenerateSidebar: true
noTitleIndex: true
needGenerateH3Content: true
breadcrumbText: DCEFrameListener
permalink: /programming/android/api-reference/camera-enhancer/interface-dceframelistener.html
---

# DCEFrameListener

The interface to handle callback when previewed frame callback is returned.

```java
interface com.dynamsoft.dce.DCEFrameListener
```

| Functions | Description |
| --------- | ----------- |
| [`frameOutputCallback`](#frameoutputcallback) | The callback method for user to implement when frame is output. |

## frameOutputCallback

The callback method can be triggered when `frame` is output.

```java
void frameOutputCallback(DCEFrame frame, long timeStamp);
```

**Parameters**

`frame`: The `DCEFrame` object that contains the image data and further information.  
`timeStamp`: The `timeStamp` that records when the `frame` is output.

**Code Snippet**

```java
cameraEnhancer.addListener(new DCEFrameListener() {
    @Override
    public void frameOutputCallback(DCEFrame frame, long timeStamp) {
        // Add your code
    }
});
```

**See also**

- [`class DCEFrame`](dceframe.md)
