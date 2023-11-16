---
layout: default-layout
title: DSRecognizedTextLinesUnit - Dynamsoft Label Recognizer iOS Edition
description: The class DSRecognizedTextLinesUnit of Dynamsoft Label Recognizer represents an intermediate result unit containing recognized text lines.
keywords: Recognized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSRecognizedTextLinesUnit
permalink: /programming/objectivec-swift/api-reference/recognized-text-lines-unit.html
---

# DSRecognizedTextLinesUnit

The `DSRecognizedTextLinesUnit` class represents an intermediate result unit containing recognized text lines. It inherits from the [DSIntermediateResultUnit]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html) class.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSRecognizedTextLinesUnit: DSIntermediateResultUnit
```
2. 
```swift
class RecognizedTextLinesUnit: IntermediateResultUnit
```

*Inheritance:* [DSIntermediateResultUnit]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html) -> DSRecognizedTextLinesUnit

## Property Summary

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`recognizedTextLines`](#recognizedtextlines) | *NSArray<*DSRecognizedTextLineElement*>* | A pointer to the [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object at the specified index. |

### recognizedTextLines

All the recognized text lines of this unit in an array of [`DSRecognizedTextLineElement`](recognized-text-line-element.md).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, copy) NSArray<DSRecognizedTextLineElement*>* recognizedTextLines;
```
2. 
```swift
var recognizedTextLines: [RecognizedTextLineElement]? { get }
```
