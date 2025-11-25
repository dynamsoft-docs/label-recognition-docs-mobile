---
layout: default-layout
title: SimplifiedLabelRecognizerSettings - Dynamsoft Capture Vision Flutter Edition API Reference
description: The SimplifiedLabelRecognizerSettings contains label recognition setting of Dynamsoft Capture Vision Flutter edition
keywords: Flutter, SimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
---

# SimplifiedLabelRecognizerSettings

The `SimplifiedLabelRecognizerSettings` class contains settings for label recognition. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class SimplifiedLabelRecognizerSettings
```

## Properties

| Property | Types | Description |
| -------- | ----- | ----------- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *EnumGrayscaleTransformationMode[]* | The grayscale transformation modes in an array of [`EnumGrayscaleTransformationMode`]({{ site.dcv_flutter_api}}core/enum/grayscale-transformation-mode.html). |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *EnumGrayscaleEnhancementMode[]* | The grayscale enhancement modes in an array of [`EnumGrayscaleEnhancementMode`]({{ site.dcv_flutter_api}}core/enum/grayscale-enhancement-mode.html). |
| [`characterModelName`](#charactermodelname) | *String* | Specify a character model by its name. |
| [`lineStringRegExPattern`](#linestringregexpattern) | *String* | The RegEx pattern of the text line string to filter out the unqualified results. |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* | The maximum available threads count in one label recognition task. |
| [`scaleDownThreshold`](#scaledownthreshold) | *int* | The threshold for image shrinking when dealing with large images. |

### grayscaleTransformationModes

The grayscale transformation modes in an array of [`EnumGrayscaleTransformationMode`]({{ site.dcv_flutter_api }}core/enum/grayscale-transformation-mode.html).

```dart
List<EnumGrayscaleTransformationMode> grayscaleTransformationModes;
```

**Remarks**

View the parameter reference page of [`GrayscaleTransformationMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-transformation-modes.html) for more detail about how to set grayscale transformation modes.

### grayscaleEnhancementModes

The grayscale enhancement modes in an array of [`EnumGrayscaleEnhancementMode`]({{ site.dcv_flutter_api }}core/enum/grayscale-enhancement-mode.html).

```dart
List<EnumGrayscaleEnhancementMode> grayscaleEnhancementModes;
```

**Remarks**

View the reference page of [`GrayscaleEnhancementMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-enhancement-modes.html) for more detail about how to set grayscale enhancement modes.

### characterModelName

Specify a character model by its name.

```dart
String? characterModelName;
```

**Remarks**

View the parameter reference of [`CharacterModelName`]({{ site.dcv_parameter_reference }}text-line-specification/character-model-name.html) for more details about how to use the parameter.

### lineStringRegExPattern

The RegEx pattern of the text line string to filter out the unqualified results.

```dart
String? lineStringRegExPattern;
```

**Remarks**

### maxThreadsInOneTask

The maximum available threads count in one label recognition task.

```dart
int maxThreadsInOneTask;
```

**Remarks**

### scaleDownThreshold

The threshold for image shrinking when dealing with large images.

```dart
int scaleDownThreshold;
```
