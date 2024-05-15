---
layout: default-layout
title: DSLocalizedTextLineElement - Dynamsoft Label Recognizer iOS Edition
description: The class DSLocalizedTextLineElement of Dynamsoft Label Recognizer iOS edition represents a localized text line element.
keywords: Localized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSLocalizedTextLineElement
permalink: /programming/objectivec-swift/api-reference/localized-text-line-element.html
---

# DSLocalizedTextLineElement

The `DSLocalizedTextLineElement` class represents a localized text line element. It inherits from the `DSRegionObjectElement` class.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSLocalizedTextLineElement: DSRegionObjectElement
```
2. 
```swift
class LocalizedTextLineElement: RegionObjectElement
```

*Inheritance:* [DSRegionObjectElement]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html) -> DSLocalizedTextLineElement

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`characterQuads`](#characterquads) | *NSArray<DSQuadrilateral \*> \** | The quadrilaterals of all characters in the text line. |
| [`rowNumber`](#rownumber) | *NSInteger* | The row number of the text line. |

### characterQuads

The quadrilaterals of all characters in the text line.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) NSArray<DSQuadrilateral *>* characterQuads;
```
2. 
```swift
var characterQuads: [Quadrilateral]? { get }
```

### rowNumber

The row number of the text line.

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
