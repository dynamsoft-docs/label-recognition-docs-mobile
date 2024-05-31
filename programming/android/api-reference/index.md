---
layout: default-layout
title: Dynamsoft Label Recognizer Android API Reference - Main Page
description: This is the main page of Dynamsoft Label Recognizer SDK API Reference for Android Language.
keywords: Label Recognizer, api reference, Android
---

# SDK Overview: Modules and Main APIs

This page provides an overview of the various modules and highlights the most essential APIs that form the backbone of Dynamsoft Label Recognizer SDK.

## Modules Summary

The Dynamsoft Label Recognizer (DLR) SDK is built on the Dynamsoft Capture Vision (DCV) framework, which includes multiple modules working together to achieve text line recognition. The hierarchical structure diagram below illustrates the various modules of the DLR SDK (with modules at the top depending on those below).

<div align="center">
    <p><img src="../../assets/dcv-dlr-dependency.png" width="70%" alt="region-def"></p>
    <p>Modules hierarchical of the DLR SDK</p>
</div>

The table below describes details the functionalities of these modules:

| Module | Description | Mandatory/Optional |
|:-----|:------------|:-------------------|
| `DynamsoftLabelRecognizer.aar`(DLR) | The Dynamsoft Label Recognizer module identifies and recognizes text labels such as passport MRZs, ID cards, and VIN numbers. | Mandatory |
| `DynamsoftCore.aar`(Core)  | The Dynamsoft Core module lays the foundation for Dynamsoft SDKs based on the DCV (Dynamsoft Capture Vision) architecture. It encapsulates the basic classes, interfaces, and enumerations shared by these SDKs. | Mandatory |
| `DynamsoftCaptureVisionRouter.aar`(CVR) | The Dynamsoft Capture Vision Router module is the cornerstone of the Dynamsoft Capture Vision (DCV) architecture. It focuses on coordinating batch image processing and provides APIs for setting up image sources and result receivers, configuring workflows with parameters, and controlling processes. | Mandatory |
| `DynamsoftImageProcessing.aar`(DIP) | The Dynamsoft Image Processing module facilitates digital image processing and supports operations for other modules, including the Barcode Reader, Label Recognizer, and Document Normalizer. | Mandatory |
| `DynamsoftNeuralNetwork.aar`(DNN) | The Dynamsoft Neural Network module allows SDKs compliant with the DCV (Dynamsoft Capture Vision) architecture to leverage the power of deep learning when processing digital images. | Mandatory |
| `DynamsoftLicense.aar`(License) | The Dynamsoft License module manages the licensing aspects of Dynamsoft SDKs based on the DCV (Dynamsoft Capture Vision) architecture. | Mandatory |
| `DynamsoftCameraEnhancer.aar`(DCE) | The [Dynamsoft Camera Enhancer]({{ site.dce_android }}){:target="_blank"} module controls the camera, transforming it into an image source for the DCV (Dynamsoft Capture Vision) architecture through ISA implementation. It also enhances image quality during acquisition and provides basic viewers for user interaction. | Optional |
| `DynamsoftUtility.aar`(Utility) | The Dynamsoft Utility module defines auxiliary classes, including the ImageManager, and implementations of the CRF (Captured Result Filter) and ISA (Image Source Adapter) . These are shared by all Dynamsoft SDKs based on the DCV (Dynamsoft Capture Vision) architecture. | Optional |

## Main APIs

### Capture Vision Router

The main class [`CaptureVisionRouter`]({{ site.dcv_android_api }}capture-vision-router/capture-vision-router.html) acts as the SDK entry point and provides the following essential APIs:

- [Set input]({{ site.dcv_android_api }}capture-vision-router/multiple-file-processing.html#setinput)
- [Config Label Recognizer settings]({{ site.dcv_android_api }}capture-vision-router/settings.html)
- [Add result receiver]({{ site.dcv_android_api }}capture-vision-router/multiple-file-processing.html#addresultreceiver)
- [Start video stream text recognizing]({{ site.dcv_android_api }}capture-vision-router/multiple-file-processing.html#startcapturing)

### Image Source Adapter

The [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html) class is an abstract class representing an adapter for image sources, providing a framework for fetching, buffering, and managing images from various sources. It serves as the input for the [`CaptureVisionRouter`]({{ site.dcv_android_api }}capture-vision-router/capture-vision-router.html). You can either use the typical implementations of [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html) or implement your own.

Class [`CameraEnhancer`]({{ site.dce_android }}primary-api/camera-enhancer.html) is one of the typical implementations of [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html). It is a class that not only implements the video frame obtaining APIs but also enable you to improve the video quality by adjusting the camera settings.

### Captured Result Receiver

To receive the results of video streaming text recognizing, you need to implement the [`CapturedResultReceiver`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) with the callback method [`onRecognizedTextlinesReceived`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html#onrecognizedtextlinesreceived). The result you received in the callback method is a [`RecognizedTextlinesResult`](recognized-text-lines-result.md) object, which contains all the recognized text lines from the processed video frame.

- [`onRecognizedTextlinesReceived`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html#onrecognizedtextlinesreceived): The callback method for you to receive the text recognizing results with a [`RecognizedTextlinesResult`](recognized-text-lines-result.md) object.
- [`RecognizedTextlinesResult`](recognized-text-lines-result.md): An object that contains all the [`TextLineResultItem`](text-line-result-item.md) that obtained from a video frame.
- [`TextLineResultItem`](text-line-result-item.md): The basic item that represents a single text line with the decoded text and other information.

### Camera View

[`CameraView`]({{ site.dce_android }}auxiliary-api/dcecameraview.html) is a view class that design for visualizing the real time video streaming and the text recognizing result. If the [`CameraEnhancer`]({{ site.dce_android }}primary-api/camera-enhancer.html) is set as the input of your CVR, the recognized text lines will be highlighted automatically on the [`CameraView`]({{ site.dce_android }}auxiliary-api/dcecameraview.html).
