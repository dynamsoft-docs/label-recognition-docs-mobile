---
layout: default-layout
title: Recognize Text Lines from Camera Enhancer - Dynamsoft Label Recognizer Android edition
description: This is page introduce RecognizeTextLinesWithCameraEnhancer sample of Dynamsoft Label Recognizer Android edition.
keywords: HelloWorld, Android
needAutoGenerateSidebar: true
---

# RecognizeTextLinesWithCameraEnhancer

This sample illustrates how to recognize text lines from the video streaming. In this sample, you can read how to use [`DynamsoftCameraEnhancer`]({{ site.dce_ios }}) to capture the video streaming.

**View the sample code**

* <a href="https://github.com/Dynamsoft/label-recognizer-mobile-samples/tree/main/android/HelloWorld/ReadTextLinesWithCameraEnhancer/" target="_blank">RecognizeTextLineWithCameraEnahcner Sample (Java)</a>
* <a href="https://github.com/Dynamsoft/label-recognizer-mobile-samples/tree/main/android/HelloWorld/ReadTextLinesWithCameraEnhancerKt/" target="_blank">RecognizeTextLineWithCameraEnahcner Sample (Kotlin)</a>

There are some basic concepts that are helpful on understanding the SDK.

## CaptureVisionRouter

[`CaptureVisionRouter`]({{ site.dcv_android_api }}capture-vision-router/capture-vision-router.html) is a router that responsible for retrieving images from the source, coordinating the image processing tasks and dispatching the processing results. To implement a text line recognizing task, what you have to do are:

* Set a standard input for your `CaptureVisionRouter` instance.
* Set a result receiver via your `CaptureVisionRouter` instance.
* Tell your `CaptureVisionRouter` instance to start working and specify a text line recognizing template with its name.
* (Additional) Configure the image processing Parameters to optimize the text line recognizing performance.

## Standard Input

Use the [`setInput`]({{ site.dcv_android_api }}capture-vision-router/multiple-file-processing.html#setinput) method of the `CaptureVisionRouter` to bind an `ImageSourceAdapter` (ISA) instance is the simplest way to access to the standard input. `CameraEnhancer` is one of the official implementation of the ISA for you to quickly set up the mobile camera as the image source.

## Output

To get the output result, you have to implement the `CapturedResultReceiver` and bind it with your `CaptureVisionRouter` instance. You will receive the text line recognizing results in the [`onDecodedBarcodesReceived`]({{ site.dcv_android_api }}core/basic-structures/captured-result-receiver.html#onrecognizedtextlinesreceived) method each time when a image (video frame) is processed.

## Control the Start & Stop of the Capturing

If only one text line recognizing result is required in one scan, you can stop the text line recognizing thread via [`stopCapturing`]({{ site.dcv_android_api }}capture-vision-router/multiple-file-processing.html#stopcapturing) method. You can call the [`startCapturing`]({{ site.dcv_android_api }}capture-vision-router/multiple-file-processing.html#startcapturing) at any time when you want to restart the text line recognizing.

<div class="sample-code-prefix"></div>
>- Java
>- Kotlin
>
>1. 
```java
@Override
public void onRecognizedTextLinesReceived(RecognizedTextLinesResult result) {
    if (result != null && result.getItems() != null && result.getItems().length > 0){
        runOnUiThread(() -> mRouter.stopCapturing());
    }
}
```
2. 
```kotlin
override fun onRecognizedTextLinesReceived(result: RecognizedTextLinesResult) {
    if (result?.items != null && result.items.isNotEmpty()) {
        runOnUiThread { mRouter.stopCapturing() }
    }
}
```
