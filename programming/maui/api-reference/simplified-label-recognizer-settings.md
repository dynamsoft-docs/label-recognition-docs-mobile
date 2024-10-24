---
layout: default-layout
title: SimplifiedLabelRecognizerSettings - Dynamsoft Capture Vision MAUI Edition API Reference
description: The SimplifiedLabelRecognizerSettings contains label recognition setting of Dynamsoft Capture Vision MAUI edition
keywords: MAUI, SimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: SimplifiedLabelRecognizerSettings
---

# SimplifiedLabelRecognizerSettings

The `SimplifiedLabelRecognizerSettings` class contains settings for label recognition. It is a sub-parameter of `SimplifiedCaptureVisionSettings`

## Definition

*Namespace:* Dynamsoft.LabelRecognizer.Maui

*Assembly:* Dynamsoft.LabelRecognizer.Maui

```csharp
class SimplifiedLabelRecognizerSettings
```

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`GrayscaleTransformationModes`](#grayscaletransformationmodes) | *EnumGrayscaleTransformationMode[]* | Set the grayscale transformation modes with an array of enumeration [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html). |
| [`GrayscaleEnhancementModes`](#grayscaleenhancementmodes) | *EnumGrayscaleEnhancementMode[]* | Set the grayscale enhancement modes with an array of enumeration [`GrayscaleEnhancementMode`]({{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html). |
| [`CharacterModelName`](#charactermodelname) | *String* | Specify a character model by its name. |
| [`LineStringRegExPattern`](#linestringregexpattern) | *String* | Set the RegEx pattern of the text line string to filter out the unqualified results. |
| [`MaxThreadsInOneTask`](#maxthreadsinonetask) | *int* | Set the maximum available threads count in one label recognition task. |
| [`ScaleDownThreshold`](#scaledownthreshold) | *int* | Set the threshold for image shrinking when dealing with large images. |

### GrayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html).

```csharp
EnumGrayscaleTransformationMode[] GrayscaleTransformationModes { get; set ; }
```

**Remarks**

View the parameter reference page of [`GrayscaleTransformationMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-transformation-modes.html){:target="_blank"} for more detail about how to set grayscale transformation modes.

### GrayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration [`GrayscaleEnhancementMode`]({{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html).

```csharp
EnumGrayscaleEnhancementMode[] GrayscaleEnhancementModes { get; set; }
```

**Remarks**

View the reference page of [`GrayscaleEnhancementMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-enhancement-modes.html){:target="_blank"} for more detail about how to set grayscale enhancement modes.

### CharacterModelName

Specify a character model by its name.

```csharp
String CharacterModelName { get; set ; }
```

**Remarks**

View the parameter reference of [CharacterModelName]({{ site.dcv_parameter_reference }}text-line-specification/character-model-name.html) for more details about how to use the parameter.

### LineStringRegExPattern

Set the RegEx pattern of the text line string to filter out the unqualified results.

```csharp
String LineStringRegExPattern { get; set ; }
```

### MaxThreadsInOneTask

Set the maximum available threads count in one label recognition task.

```csharp
int MaxThreadsInOneTask { get; set ; }
```

**Remarks**

### ScaleDownThreshold

Set the threshold for image shrinking when dealing with large images.

```csharp
int ScaleDownThreshold { get; set ; }
```
