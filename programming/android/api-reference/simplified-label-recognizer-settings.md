---
layout: default-layout
title: struct SimplifiedLabelRecognizerSettings - Dynamsoft Capture Vision C++ Edition API Reference
description: This page shows the SimplifiedLabelRecognizerSettings struct of the CCaptureVisionRouter class of the Dynamsoft Capture Vision C++ Edition.
keywords: struct, c++, SimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: CVR C++ SimplifiedLabelRecognizerSettings Struct
permalink: /programming/android/api-reference/simplified-label-recognizer-settings.html
---

# SimplifiedLabelRecognizerSettings

The `SimplifiedLabelRecognizerSettings` struct contains settings for label recognition. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

```java
class SimplifiedLabelRecognizerSettings
```

## Attributes Summary

| Attribute | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *EnumGrayscaleTransformationMode[]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *EnumGrayscaleEnhancementMode[]* |
| [`characterModelName`](#charactermodelname) | *LocalizationMode[]* |
| [`lineStringRegExPattern`](#linestringregexpattern) | *DeblurMode[]* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* |

### grayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html).

View the parameter reference page of [`GrayscaleTransformationMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-transformation-modes.html){:target="_blank"} for more detail about how to set grayscale transformation modes.

```java
int[] grayscaleTransformationModes;
```

### grayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration [`GrayscaleEnhancementMode`]({{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html).

View the reference page of [`GrayscaleEnhancementMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-enhancement-modes.html){:target="_blank"} for more detail about how to set grayscale enhancement modes.

```java
int[] grayscaleEnhancementModes;
```

### characterModelName

Specify a character model by its name.

```java
String characterModelName;
```

### lineStringRegExPattern

Set the RegEx pattern of the text line string to filter out the unqualified results.

```java
String lineStringRegExPattern;
```

### maxThreadsInOneTask

Set the maximum available threads count in one label recognition task.

```java
int maxThreadsInOneTask;
```

### scaleDownThreshold

Set the threshold for image shrinking when dealing with large images.

```java
int scaleDownThreshold;
```
