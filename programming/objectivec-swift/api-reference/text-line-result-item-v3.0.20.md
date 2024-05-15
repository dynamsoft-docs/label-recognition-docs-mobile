---
layout: default-layout
title: DSTextLineResultItem - Dynamsoft Label Recognizer iOS Edition
description: The class DSTextLineResultItem of Dynamsoft Label Recognizer iOS edition represents a text line result item recognized by a document layout analysis engine.
keywords: Text line result item
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSTextLineResultItem
permalink: /programming/objectivec-swift/api-reference/text-line-result-item-v3.0.20.html
---

# DSTextLineResultItem

The `DSTextLineResultItem` class represents a single text line result item recognized by the library. It is derived from `DSCapturedResultItem` and is one of the base units of `DSRecognizedTextLinesResult`.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSTextLineResultItem: DSCapturedResultItem
```
2. 
```swift
class TextLineResultItem: CapturedResultItem
```

*Inheritance:* [DSCapturedResultItem]({{ site.dcv_ios_api }}core/basic-structures/captured-result-item.html) -> DSTextLineResultItem

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`text`](#text) | *NSString* | The text content of the text line. |
| [`location`](#location) | *DSQuadrilateral* | The location of the text line in the form of a quadrilateral. |
| [`confidence`](#confidence) | *NSInteger* | The confidence of the text line recognition result. |
| [`characterResults`](#characterresults) | *NSArray<*DSCharacterResult*>* | All the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.md) object. |

### text

Returns the text content of the individual text line.

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

### location

It is used to get the location of the text line in the form of a [DSQuadrilateral]({{ site.dcv_ios_api }}core/basic-structures/quadrilateral.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) DSQuadrilateral* location;
```
2. 
```swift
var location: Quadrilateral? { get }
```

### confidence

Returns the confidence of the individual text line recognition result.

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
var confidence: Int { get }
```

### characterResults

Returns all the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.md) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) NSArray<DSCharacterResult*>* charResult;
```
2. 
```swift
var charResult: [CharacterResult]? { get }
```
