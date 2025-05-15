---
layout: default-layout
title: DSRawTextLinesUnit - Dynamsoft Label Recognizer iOS Edition
description: The class DSRawTextLinesUnit of Dynamsoft Label Recognizer iOS edition represents a unit which holds the raw text lines.
keywords: raw text lines unit, intermediate result unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSRawTextLinesUnit
---

# DSRawTextLinesUnit

The `DSRawTextLinesUnit` class represents a unit which holds the raw text lines.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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

## Methods

| Method | Description |
| --- | --- |
| [`getCount`](#getcount) | Gets the number of raw text lines in the unit. |
| [`getRawTextLine`](#getrawtextline) | Gets a raw text line at the specified index. |
| [`getRawTextLines`](#getrawtextlines) | Gets all raw text lines of the unit. |
| [`removeAllRawTextLines`](#removeallrawtextlines) | Removes all raw text lines. |
| [`removeRawTextLine`](#removerawtextline) | Removes the raw text line at the specified index. |
| [`addRawTextLine`](#addrawtextline) | Adds a raw text line. |
| [`setRawTextLine`](#setrawtextline) | Sets the raw text line at the specified index. |

### getCount

Returns the number of raw text lines in the unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)getCount;
```
2. 
```swift
func getCount() -> Int
```

**Return value**

Returns the number of raw text lines in the unit.

### getRawTextLine

Gets a raw text line at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSRawTextLine)getRawTextLine:(NSInteger)index;
```
2. 
```swift
func getRawTextLine(_ index: Int) -> DSRawTextLine?
```

**Parameters**

`index`: The index of the raw text line.

**Return value**

Returns a pointer to the [`RawTextLine`](raw-text-line.md) object at the specified index.

### getRawTextLines

Gets all raw text lines of the unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSRawTextLine *> *)getRawTextLines;
```
2. 
```swift
func getRawTextLines() -> [DSRawTextLine]?
```

**Return value**

Returns all the [`RawTextLine`](raw-text-line.md) objects of the unit in an array.

### removeAllRawTextLines

Removes all raw text lines.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)removeAllRawTextLines;
```
2. 
```swift
func removeAllRawTextLines()
```

### removeRawTextLine

Removes the raw text line at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)removeRawTextLine:(NSInteger)index;
```
2. 
```swift
func removeRawTextLine(_ index: Int) -> Int
```

**Parameters**

`index`: The index of the raw text line to be removed.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addRawTextLine

Adds a raw text line to the unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)addRawTextLine:(DSRawTextLine *)textline
     matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func addRawTextLine(_ textline: DSRawTextLine, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`textline`: A [`RawTextLine`](raw-text-line.md) object as the raw text line to be added to the unit.

`matrixToOriginalImage`: The matrix to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setRawTextLine

Sets the raw text line at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setRawTextLine:(NSInteger)index
                   element:(DSRawTextLine *)textline
     matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setRawTextLine(_ index: Int, textline: DSRawTextLine, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`index`: The index of the raw text line to be set.

`textline`: A [`RawTextLine`](raw-text-line.md) object as the raw text line to be set.

`matrixToOriginalImage`: The matrix to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
