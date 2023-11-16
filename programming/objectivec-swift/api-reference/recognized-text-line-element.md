---
layout: default-layout
title: DSRecognizedTextLineElement - Dynamsoft Label Recognizer iOS Edition
description: The class DSRecognizedTextLineElement of Dynamsoft Label Recognizer represents a line of recognized text in an image.
keywords: Recognized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSRecognizedTextLineElement
permalink: /programming/objectivec-swift/api-reference/recognized-text-line-element.html
---

# DSRecognizedTextLineElement

The `DSRecognizedTextLineElement` class represents a line of recognized text in an image. It inherits from the [DSRegionObjectElement]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html) class.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSRecognizedTextLineElement: DSRegionObjectElement
```
2. 
```swift
class RecognizedTextLineElement: RegionObjectElement
```

*Inheritance:* [DSRegionObjectElement]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html) -> DSRecognizedTextLineElement

## Property Summary

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`text`](#text) | *NSString* | The recognized text. |
| [`confidence`](#confidence) | *NSInteger* | The confidence level of the recognized text. |
| [`characterResults`](#characterresults) | *NSArray<*DSCharacterResult*>* | All the characters contained by the textline. |
| [`rowNumber`](#rownumber) | *NSInteger* | The row number of the text line within the image. |

### text

The recognized text.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) NSString* text;
```
2. 
```swift
var text: String? { get }
```

### confidence

The confidence level of the recognized text.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) NSInteger confidence;
```
2. 
```swift
var confidence: String? { get }
```

### characterResults

All the characters contained by the textline in an array of [`DSCharacterResult`](character-result.md).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) NSArray<DSCharacterResult *>* characterResults;
```
2. 
```swift
var text: [CharacterResult]? { get }
```

### rowNumber

The row number of the text line within the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) NSInteger rowNumber;
```
2. 
```swift
var rowNumber: Int { get }
```
