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

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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
| [`addRecognizedTextLine`](#addrecognizedtextline) | Adds a recognized text line. |
| [`getRecognizedTextLines`](#getrecognizedtextlines) | Get all the recognized text lines in an array of [`DSRecognizedTextLineElement`](recognized-text-line-element.md). |
| [`getCount`](#getcount) | Returns the number of text lines in this unit. |
| [`getRecognizedTextLine`](#getrecognizedtextline) | Returns the text line at the specified index in a [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object. |
| [`removeAllRecognizedTextLines`](#removeallrecognizedtextlines) | Removes all the recognized text lines from this unit. |
| [`removeRecognizedTextLine`](#removerecognizedtextline) | Removes the recognized text line at the specified index. |
| [`setRecognizedTextLine(index, element, matrixToOriginalImage)`](#setrecognizedtextlineindex-element-matrixtooriginalimage) | Sets the recognized text line at the specified index. |
| [`setRecognizedTextLine(element, matrixToOriginalImage)`](#setrecognizedtextlineelement-matrixtooriginalimage) | Sets the recognized text line at the specified index. |

### AddRecognizedTextLine

Adds a recognized text line.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)addRecognizedTextLine:(DSRecognizedTextLineElement*)element
            matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func addRecognizedTextLine(_ element: RecognizedTextLineElement, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`element`: The [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object to be added.

`matrixToOriginalImage`: The matrix to transform the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

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

### removeRecognizedTextLine

Removes the [`RecognizedTextLineElement`](recognized-text-line-element.md) at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)removeRecognizedTextLine:(NSInteger)index;
```
2. 
```swift
func removeRecognizedTextLine(_ index: Int) -> Int
```

**Parameters**

`index`: The index of the recognized text line to remove.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setRecognizedTextLine(index, element, matrixToOriginalImage)

Sets the text line at the specified index in a [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setRecognizedTextLine:(NSInteger)index
                          element:(DSRecognizedTextLineElement*)element
            matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setRecognizedTextLine(_ index: Int, element: RecognizedTextLineElement, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`index`: The index of the recognized text line to set.

`element`: The [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object to be set.

`matrixToOriginalImage`: The matrix to transform the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setRecognizedTextLine(element, matrixToOriginalImage)

> This method is deprecated.

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
