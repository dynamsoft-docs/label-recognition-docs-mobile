---
layout: default-layout
title: DSRecognizedTextLinesUnit - Dynamsoft Label Recognizer iOS Edition
description: The class DSRecognizedTextLinesUnit of Dynamsoft Label Recognizer iOS edition represents an intermediate result unit containing recognized text lines.
keywords: Recognized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSRecognizedTextLinesUnit
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

## Methods

| Method | Description |
| ------ | ----------- |
| [`getRecognizedTextLines`](#getrecognizedtextlines) | Get all the recognized text lines in an array of [`DSRecognizedTextLineElement`](recognized-text-line-element.md). |
| [`getCount`](#getcount) | Returns the number of text lines in this unit. |
| [`getRecognizedTextLine`](#getrecognizedtextline) | Returns the text line at the specified index in a [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object. |
| [`removeAllRecognizedTextLines`](#removeallrecognizedtextlines) | Removes all the recognized text lines from this unit. |
| [`setRecognizedTextLine`](#setrecognizedtextline) | Sets the text line at the specified index. |

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

### getRecognizedTextLines

Gets all the recognized text lines in an array of [`DSRecognizedTextLineElement`](recognized-text-line-element.md).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSArray<DSRecognizedTextLineElement*>*)getRecognizedTextLines;
```
2. 
```swift
func getRecognizedTextLines() -> [RecognizedTextLineElement]?
```

**Return value**

All the recognized text lines in an array of [`DSRecognizedTextLineElement`](recognized-text-line-element.md).

### getCount

Returns the number of text lines in this unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)getCount;
```
2. 
```swift
func getCount() -> Int
```

**Return value**

The number of text lines in this unit.

### getRecognizedTextLine

Returns the text line at the specified index in a [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (nullable DSRecognizedTextLineElement*)getRecognizedTextLine:(NSInteger)index;
```
2. 
```swift
func getRecognizedTextLine(_ index: Int) -> RecognizedTextLineElement?
```

**Parameters**

`index`: The index of the text line in this unit.

**Return value**

The text line at the specified index in a [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object.

### removeAllRecognizedTextLines

Removes all the recognized text lines from this unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)removeAllRecognizedTextLines;
```
2. 
```swift
func removeAllRecognizedTextLines()
```

### setRecognizedTextLine

Sets the text line at the specified index in a [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (NSInteger)setRecognizedTextLine:(DSRecognizedTextLineElement*)element
    matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setRecognizedTextLine(_ element: RecognizedTextLineElement, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`element`: The [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object to be set.

`matrixToOriginalImage`: The matrix to transform the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
