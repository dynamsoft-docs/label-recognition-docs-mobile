---
layout: default-layout
title: Recognize Text Lines from Camera Enhancer - Dynamsoft Label Recognizer iOS edition
description: This is page introduce RecognizeTextLinesWithCameraEnhancer sample of Dynamsoft Label Recognizer iOS edition.
keywords: HelloWorld, iOS
needAutoGenerateSidebar: true
---

# RecognizeTextLinesWithCameraEnhancer

This sample illustrates how to recognize text lines from the video streaming. In this sample, you can read how to use [`DynamsoftCameraEnhancer`]({{ site.dce_ios }}){:target="_blank"} to capture the video streaming.

**View the sample code**

* <a href="https://github.com/Dynamsoft/label-recognizer-mobile-samples/tree/main/ios/HelloWorld/ReadTextLinesWithCameraEnhancer/" target="_blank">RecognizeTextLineWithCameraEnahcner Sample (Swift)</a>
* <a href="https://github.com/Dynamsoft/label-recognizer-mobile-samples/tree/main/ios/HelloWorld/ReadTextLinesWithCameraEnhancerObjc/" target="_blank">RecognizeTextLineWithCameraEnahcner Sample (Objective-C)</a>

There are some basic concepts that are helpful on understanding the SDK.

## CaptureVisionRouter

[`CaptureVisionRouter`]({{ site.dcv_ios_api }}capture-vision-router/capture-vision-router.html) is a router that responsible for retrieving images from the source, coordinating the image processing tasks and dispatching the processing results. To implement a text line recognizing task, what you have to do are:

* Set a standard input for your `CaptureVisionRouter` instance.
* Set a result receiver via your `CaptureVisionRouter` instance.
* Tell your `CaptureVisionRouter` instance to start working and specify a text line recognizing template with its name.
* (Additional) Configure the image processing Parameters to optimize the text line recognizing performance.

## Standard Input

Use the [`setInput`]({{ site.dcv_ios_api }}capture-vision-router/multiple-file-processing.html#setinput) method of the `CaptureVisionRouter` to bind an `ImageSourceAdapter` (ISA) instance is the simplest way to access to the standard input. `CameraEnhancer` is one of the official implementation of the ISA for you to quickly set up the mobile camera as the image source.

## Output

To get the output result, you have to implement the `CapturedResultReceiver` and bind it with your `CaptureVisionRouter` instance. You will receive the text line recognizing results in the [`onDecodedBarcodesReceived`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-receiver.html#onrecognizedtextlinesreceived) method each time when a image (video frame) is processed.

## Control the Start & Stop of the Capturing

If only one text line recognizing result is required in one scan, you can stop the text line recognizing thread via [`stopCapturing`]({{ site.dcv_ios_api }}capture-vision-router/multiple-file-processing.html#stopcapturing) method. You can call the [`startCapturing`]({{ site.dcv_ios_api }}capture-vision-router/multiple-file-processing.html#startcapturing) at any time when you want to restart the text line recognizing.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)onRecognizedTextLinesReceived:(DSRecognizedTextLinesResult *)result {
   if (result.items.count > 0) {
          // Stop capturing if barcode result is no empty.
          dispatch_async(dispatch_get_main_queue(), ^{
             [self.cvr stopCapturing];
          });
          for (DSBarcodeResultItem *item in result.items) {
             // Deal with the result you get.
          }
   }
}
```
2. 
```swift
func onRecognizedTextLinesReceived(_ result: RecognizedTextLinesResult) {
   if let items = result.items, items.count > 0 {
          DispatchQueue.main.async {
             self.cvr.stopCapturing()
          }
          for item in items {
             // Deal with the result you get.
          }
   }
}
```
