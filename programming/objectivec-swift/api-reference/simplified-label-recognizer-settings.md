---
layout: default-layout
title: Class DSSimplifiedLabelRecognizerSettings - Dynamsoft Label Recognizer iOS Edition API Reference
description: The DSSimplifiedLabelRecognizerSettings class contains label recognition settings of Dynamsoft Label Recognizer iOS Edition.
keywords: iOS, DSSimplifiedLabelRecognizerSettings
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: DSSimplifiedLabelRecognizerSettings
permalink: /programming/objectivec-swift/api-reference/simplified-label-recognizer-settings.html
---

# DSSimplifiedLabelRecognizerSettings

The `DSSimplifiedLabelRecognizerSettings` class contains settings for label recognition. It is a sub-parameter of `DSSimplifiedCaptureVisionSettings`

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSSimplifiedLabelRecognizerSettings : NSObject
```
2. 
```swift
class SimplifiedLabelRecognizerSettings: NSObject
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *NSArray<DSGrayscaleTransformationMode \*> \** | Set the grayscale transformation modes with an array of enumeration [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html). |
| [`grayscaleEnhancementModes`](#grayscaleenhancementmodes) | *NSArray<DSGrayscaleEnhancementMode \*> \** | Set the grayscale enhancement modes with an array of enumeration [`GrayscaleEnhancementMode`]({{ site.dcv_enumerations}}core/grayscale-enhancement-mode.html). |
| [`characterModelName`](#charactermodelname) | *NSString \** | Specify a character model by its name. |
| [`lineStringRegExPattern`](#linestringregexpattern) | *NSString \** | Set the RegEx pattern of the text line string to filter out the unqualified results. |
| [`maxThreadsInOneTask`](#maxthreadsinonetask) | *NSInteger* | Set the maximum available threads count in one label recognition task. |
| [`scaleDownThreshold`](#scaledownthreshold) | *NSInteger* | Set the threshold for image shrinking when dealing with large images. |

### grayscaleTransformationModes

Set the grayscale transformation modes with an array of enumeration [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, copy) NSArray* grayscaleTransformationModes;
```
2. 
```swift
var grayscaleTransformationModes: [Any]? { get set }
```

**Remarks**

View the parameter reference page of [`GrayscaleTransformationMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-transformation-modes.html){:target="_blank"} for more detail about how to set grayscale transformation modes.

### grayscaleEnhancementModes

Set the grayscale enhancement modes with an array of enumeration [`GrayscaleEnhancementMode`]({{ site.dcv_enumerations }}core/grayscale-enhancement-mode.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, copy) NSArray* grayscaleEnhancementModes;
```
2. 
```swift
var grayscaleEnhancementModes: [Any]? { get set }
```

**Remarks**

View the reference page of [`GrayscaleEnhancementMode`]({{ site.dcv_parameter_reference }}image-parameter/grayscale-enhancement-modes.html){:target="_blank"} for more detail about how to set grayscale enhancement modes.

### characterModelName

Specify a character model by its name.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, copy) NSString* characterModelName;
```
2. 
```swift
var characterModelName: String? { get set }
```

**Remarks**

View the parameter reference of [CharacterModelName]({{ site.dcv_parameter_reference }}text-line-specification/character-model-name.html) for more details about how to use the parameter.

### lineStringRegExPattern

Set the RegEx pattern of the text line string to filter out the unqualified results.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, copy) NSString* lineStringRegExPattern;
```
2. 
```swift
var lineStringRegExPattern: String? { get set }
```

**Remarks**

View the parameter reference of [`StringRegExPattern`]({{ site.dcv_parameter_reference }}label-recognizer-task-settings/string-regex-pattern.html).

### maxThreadsInOneTask

Set the maximum available threads count in one label recognition task.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger maxThreadsInOneTask;
```
2. 
```swift
var maxThreadsInOneTask: Int { get set }
```

**Remarks**

View the parameter reference of [`maxThreadsInOneTask`]({{ site.dcv_parameter_reference }}label-recognizer-task-settings/max-threads-in-one-task.html).

### scaleDownThreshold

Set the threshold for image shrinking when dealing with large images.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) NSInteger scaleDownThreshold;
```
2. 
```swift
var scaleDownThreshold: Int { get set }
```

**Remarks**

View the parameter reference of [`ScaleDownThreshold`]({{ site.dcv_parameter_reference }}image-parameter/scale-down-threshold.html).
