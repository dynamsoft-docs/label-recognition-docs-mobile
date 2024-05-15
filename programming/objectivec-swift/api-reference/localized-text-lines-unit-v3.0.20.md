---
layout: default-layout
title: DSLocalizedTextLinesUnit - Dynamsoft Label Recognizer iOS Edition
description: The class DSLocalizedTextLinesUnit of Dynamsoft Label Recognizer iOS edition represents a unit that contains localized text lines.
keywords: Localized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSLocalizedTextLinesUnit
permalink: /programming/objectivec-swift/api-reference/localized-text-lines-unit-v3.0.20.html
---

# DSLocalizedTextLinesUnit

The `DSLocalizedTextLinesUnit` class represents a unit that contains localized text lines. It inherits from the [DSIntermediateResultUnit]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html) class.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSLocalizedTextLinesUnit: DSIntermediateResultUnit
```
2. 
```swift
class LocalizedTextLinesUnit: IntermediateResultUnit
```

*Inheritance:* [DSIntermediateResultUnit]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html) -> DSLocalizedTextLinesUnit

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`localizedTextLine`](#localizedtextlines) | *NSArray<*DSLocalizedTextLineElement*>* | All the text lines in an array of [`DSLocalizedTextLineElement`](localized-text-line-element.md), which is the basic unit of the localized text line result. |

### localizedTextLines

All the text lines in an array of [`DSLocalizedTextLineElement`](localized-text-line-element.md), which is the basic unit of the localized text line result.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, copy) NSArray<DSLocalizedTextLineElement*>* localizedTextLines;
```
2. 
```swift
var localizedTextLines: [DSLocalizedTextLineElement]? { get }
```
