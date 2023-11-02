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
typedef struct tagSimplifiedLabelRecognizerSettings
{
    GrayscaleTransformationMode grayscaleTransformationModes[8];
    GrayscaleEnhancementMode grayscaleEnhancementModes[8];
    char characterModelName[64];
    char lineStringRegExPattern[1024];
    int maxThreadsInOneTask;
    char reserved[512];
} SimplifiedLabelRecognizerSettings;
```

## Attributes Summary

| Attribute | Type |
| --------- | ---- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *GrayscaleTransformationMode[8]* |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *GrayscaleEnhancementMode[8]* |
| [`characterModelName`](#charactermodelname) | *LocalizationMode[8]* |
| [`lineStringRegExPattern`](#linestringregexpattern) | *DeblurMode[10]* |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *int* |
| [`reserved`](#reserved) | *char[512]* |

### grayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration `GrayscaleTransformationMode`. View the reference page of <a href="{{ site.dcv_enumerations}}core/grayscale-transformation-mode.html?src=cpp&&lang=cpp" target="_blank">`GrayscaleTransformationMode`</a> for more detail about grayscale transformation modes.

```java
GrayscaleTransformationMode grayscaleTransformationModes[8];
```

### grayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration `GrayscaleEnhancementMode`. View the reference page of <a href="{{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html?src=cpp&&lang=cpp" target="_blank">`GrayscaleEnhancementMode`</a> for more detail about grayscale enhancement modes.

```java
GrayscaleEnhancementMode grayscaleEnhancementModes[8];
```

### characterModelName

Specify a character model by its name.

```java
char characterModelName[64];
```

### lineStringRegExPattern

Set the RegEx pattern of the text line string to filter out the unqualified results.

```java
char lineStringRegExPattern[1024];
```

### maxThreadsInOneTask

Set the maximum available threads count in one label recognition task.

```java
int maxThreadsInOneTask;
```

### reserved

Reserved for future use.

```java
char reserved[512];
```
