---
layout: default-layout
title: Android SDK Release Notes 2.x - Dynamsoft Label Recognizer
description: This is the release notes page of Dynamsoft Label Recognizer for Android SDK version 2.x.
keywords: release notes, android
needAutoGenerateSidebar: false
permalink: /programming/android/release-notes/android-2.html
---

# Release Notes - Android 2.x

## 2.2.20 (09/29/2022)

<div class="fold-panel-prefix"></div>

### Version Highlights <i class="fa fa-caret-down"></i>

<div class="fold-panel-start"></div>

{%- include release-notes/product-highlight-2.2.md -%}

<div class="fold-panel-end"></div>

### Changelog

#### New

- Added methods in `LabelRecognizer` class to support video streaming recognition.
  - [`setImageSource`](../api-reference/label-recognizer.md#setimagesource): Set the source of image/video.
  - [`setLabelResultListener`](../api-reference/label-recognizer.md#setlabelresultlistener): Register a listener to receive label recognizing results.
  - [`startScanning`](../api-reference/label-recognizer.md#startscanning): Start the label recognizing processes.
  - [`stopScanning`](../api-reference/label-recognizer.md#stopscanning): Stop the label recognizing processes.
- Added methods in `LabelRecognizer` class to configure settings.
  - [`initRuntimeSettings`](../api-reference/label-recognizer.md#initruntimesettings)
  - [`initRuntimeSettingsFromFile`](../api-reference/label-recognizer.md#initruntimesettingsfromfile)
  - [`outputRuntimeSettings`](../api-reference/label-recognizer.md#outputruntimesettings)
  - [`outputRuntimeSettingsFromFile`](../api-reference/label-recognizer.md#outputruntimesettingstofile)
- Added a new recognition method [`recognizeFileInMemory`](../api-reference/label-recognizer.md#recognizefileinmemory) in `LabelRecognizer` class.
- Added a protocol [`LabelResultListener`](../api-reference/label-result-listener.md) to obtain video label recognition results.
- Added a new parameter [`timeout`](../api-reference/dlr-runtime-settings.md#timeout) to `DLRRuntimeSettings` class.

#### Rename

- The following methods of `LabelRecognizer` class are renamed
  - Renamed `recognizeByFile` to [`recognizeFile`](../api-reference/label-recognizer.md#recognizefile).
  - Renamed `recognizeByBuffer` to [`recognizeBuffer`](../api-reference/label-recognizer.md#recognizebuffer).
  - Renamed `recognizeByImage` to [`recognizeImage`](../api-reference/label-recognizer.md#recognizeimage).
  - Renamed `outputSettingsToFile` to [`outputRuntimeSettingsToFile`](../api-reference/label-recognizer.md#outputruntimesettingstofile).

#### Removed

- The following methods of `LabelRecognizer` class are removed
  - `initLicense`. The method is replaced by `LicenseManager.initLicense` under `DynamsoftCore`.
  - `appendSettingsFromString`
  - `appendSettingsFromFile`
  - `clearAppendedSettings`
  - `destory`

## 2.0 (08/26/2021)

<div class="fold-panel-prefix"></div>

### Version Highlights <i class="fa fa-caret-down"></i>

<div class="fold-panel-start"></div>

{%- include release-notes/product-highlight-2.0.md -%}

<div class="fold-panel-end"></div>

### Changelog

#### New

- Added auto-deskew algorithm to improve the performance on recognizing the skewed characters.
- Added package `DynamsoftCoreAndroid.aar`. Migrated the Dynamsoft core classes/enums from package `DynamsoftLabelRecognizerAndroid.aar` to `DynamsoftCoreAndroid.aar`.
- Added class [`BarcodeResult`](../api-reference/barcode-result.md) for users to interact with Dynamsoft Barcode Reader SDK.
- Added [`DLRRuntimeSettings`](../api-reference/dlr-runtime-settings.md) property [`dictionaryPath`](../api-reference/dlr-runtime-settings.md#dictionarypath) and [`dictionaryCorrectionThreshold`](../api-reference/dlr-runtime-settings.md#dictionarycorrectionthreshold) for users to further improve the recognizing accuracy by referencing dictionary files.
- Added class [`DLRDictionaryCorrectionThreshold`](../api-reference/dlr-dictionary-correction-threshold.md).
- Added class [`DLRFurtherModes`](../api-reference/dlr-further-modes.md) and property [`DLRRuntimeSettings.furtherModes`](../api-reference/dlr-runtime-settings.md#furthermodes) for users to config more processing modes.
- Added enumeration [`TextureDetectionMode`]({{ site.enumerations }}texture-detection-mode.html) and property [`DLRFurtherModes.textureDetectionModes`](../api-reference/dlr-further-modes.md#texturedetectionmodes) for users to detect and remove the texture background. 
- Added enumeration [`ColourConversionMode`]({{ site.enumerations }}colour-conversion-mode.html) and property [`DLRFurtherModes.colourConversionModes`](../api-reference/dlr-further-modes.md#colourconversionmodes) for users to convert color images to grayscale images in differenct ways. 
- Added enumeration [`BinarizationMode`]({{ site.enumerations }}binarization-mode.html) and property [`DLRRuntimeSettings.binarizationModes`](../api-reference/dlr-runtime-settings.md#binarizationmodes) for users to convert grayscale images to binary images in different ways. 
- Added enumeration [`GrayscaleEnhancementMode`]({{ site.enumerations }}grayscale-enhancement-mode.html) and property [`DLRFurtherModes.grayscaleEnhancementModes`](../api-reference/dlr-further-modes.md#grayscaleenhancementmodes) for users to enable grayscale images preprocessing.  
- Added [`characterHConfidence`](../api-reference/dlr-character-result.md#characterhconfidence), [`characterMConfidence`](../api-reference/dlr-character-result.md#charactermconfidence) and [`characterLConfidence`](../api-reference/dlr-character-result.md#characterlconfidence) properties in [`DLRCharacterResult`](../api-reference/dlr-character-result.md) class so that more alternative results will be available for users.
- Added API [`recognizeByImage`](../api-reference/label-recognizer.md#recognizebyimage).

#### Improved

- Improved the neural network performance by replacing Caffe engine with OpenCV DNN engine. 

#### Fixed

- Fixed a bug that might cause wrong line number matching when using [`LineSpecification.LineNumber`]({{ site.parameters-reference }}line-specification/parameter-control.html#linenumber).

#### API Changes

- Modified the method initLicense(String) to static [`initLicense(String, DLRLicenseVerificationListener)`](../api-reference/label-recognizer.md#initlicense).
- Modified the parameter type of the method [`updateReferenceRegionFromBarcodeResults`](../api-reference/label-recognizer.md#updatereferenceregionfrombarcoderesults) from `TextResult[]` to `BarcodeResult[]`.
- Modified the parameters [`LabelRecognizerParameter.LetterHeightRange`]({{ site.parameters-reference }}label-recognition-parameter/parameter-control.html#letterheightrange) and [`TextArea.LetterHeightRange`]({{ site.parameters-reference }}text-area/parameter-control.html#letterheightrange). The value unit of the parameters are modified from percentage to thousandth. The available range of the value and the default value are updated as well.
- Renamed class `LabelRecognition` to [`LableRecognizer`](../api-reference/label-recognizer.md).
- Renamed interface `DLRLTSLicenseVerificationListener` to `DLRLicenseVerificationListener`.
- Renamed interface method `LTSLicenseVerificationCallback` to `DLRLicenseVerificationCallback`.
- Removed method `initLicenseFromLTS`.
- Removed method `LabelRecognizer(string license)`.
- Removed class `DMLTSConnectionParameters`.
