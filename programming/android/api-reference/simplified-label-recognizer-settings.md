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

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *EnumGrayscaleTransformationMode[]* | Set the grayscale transformation modes with an array of enumeration [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html). |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *EnumGrayscaleEnhancementMode[]* | Set the grayscale enhancement modes with an array of enumeration [`GrayscaleEnhancementMode`]({{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html). |
| [`characterModelName`](#charactermodelname) | *LocalizationMode[]* | Specify a character model by its name. |
| [`lineStringRegExPattern`](#linestringregexpattern) | *DeblurMode[]* | Set the RegEx pattern of the text line string to filter out the unqualified results. |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* | Set the maximum available threads count in one label recognition task. |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* | Set the threshold for image shrinking when dealing with large images. |

### grayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html).

```java
int[] grayscaleTransformationModes;
```

**Remarks**

View the parameter reference page of [`GrayscaleTransformationMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-transformation-modes.html){:target="_blank"} for more detail about how to set grayscale transformation modes.

### grayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration [`GrayscaleEnhancementMode`]({{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html).

```java
int[] grayscaleEnhancementModes;
```

**Remarks**

View the reference page of [`GrayscaleEnhancementMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-enhancement-modes.html){:target="_blank"} for more detail about how to set grayscale enhancement modes.

### characterModelName

Specify a character model by its name.

```java
String characterModelName;
```

**Remarks**

View the parameter reference of [CharacterModelName]({{ site.dcv_parameter_reference }}text-line-specification/character-model-name.html) for more details about how to use the parameter.

### lineStringRegExPattern

Set the RegEx pattern of the text line string to filter out the unqualified results.

```java
String lineStringRegExPattern;
```

**Remarks**

### maxThreadsInOneTask

Set the maximum available threads count in one label recognition task.

```java
int maxThreadsInOneTask;
```

**Remarks**

### scaleDownThreshold

Set the threshold for image shrinking when dealing with large images.

```java
int scaleDownThreshold;
```

**Remarks**
