---
layout: default-layout
title: DSLocalizedTextLinesUnit - Dynamsoft Label Recognizer iOS Edition
description: The class DSLocalizedTextLinesUnit of Dynamsoft Label Recognizer iOS edition represents a unit that contains localized text lines.
keywords: Localized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSLocalizedTextLinesUnit
---

# DSLocalizedTextLinesUnit

The `DSLocalizedTextLinesUnit` class represents a unit that contains localized text lines. It inherits from the [DSIntermediateResultUnit]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html) class.

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
| ------ | ----------- |
| [`getLocalizedTextLines`](#getlocalizedtextlines) | Get all the text lines in an array of [`DSLocalizedTextLineElement`](localized-text-line-element.md), which is the basic unit of the localized text line result. |
| [`getCount`](#getcount) | Get the number of text lines in this unit. |
| [`getLocalizedTextLine`](#getlocalizedtextline) | Get the localized text line at the specified index in a [`LocalizedTextLineElement`](localized-text-line-element.md) object. |
| [`removeAllLocalizedTextLines`](#removealllocalizedtextlines) | Remove all the text lines from this unit. |
| [`removeLocalizedTextLine`](#removelocalizedtextline) | Remove the localized text line at the specified index from this unit. |
| [`addLocalizedTextLine`](#addlocalizedtextline) | Add a localized text line to this unit. |
| [`setLocalizedTextLine`](#setlocalizedtextline) | Set the localized text line at the specified index in a [`LocalizedTextLineElement`](localized-text-line-element.md) object. |
| [`getAuxiliaryRegionElements`](#getauxiliaryregionelements) | Get all the auxiliary region elements in an array of [`AuxiliaryRegionElement`]({{ site.dcv_ios_api }}core/intermediate-results/auxiliary-region-element.html). |
| [`getAuxiliaryRegionElementsCount`](#getauxiliaryelementscount) | Get the number of auxiliary region elements in this unit. |
| [`getAuxiliaryRegionElement`](#getauxiliaryregionelement) | Get the auxiliary region element at the specified index. |
| [`setAuxiliaryRegionElement`](#setauxiliaryregionelement) | Set or replace the auxiliary region element at the specified index. |
| [`addAuxiliaryRegionElement`](#addauxiliaryregionelement) | Add a new auxiliary region element to this unit. |
| [`removeAuxiliaryRegionElement`](#removeauxiliaryregionelement) | Remove the auxiliary region element at the specified index. |
| [`removeAllAuxiliaryRegionElements`](#removeallauxiliaryregionelements) | Remove all the auxiliary region elements from this unit. |

### getLocalizedTextLines

Get all the text lines in an array of [`DSLocalizedTextLineElement`](localized-text-line-element.md), which is the basic unit of the localized text line result.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSLocalizedTextLineElement*>*)getLocalizedTextLines;
```
2. 
```swift
func getLocalizedTextLines() -> [DSLocalizedTextLineElement]?
```

**Return value**

All the text lines in an array of [`DSLocalizedTextLineElement`](localized-text-line-element.md), which is the basic unit of the localized text line result.

### getCount

Get the number of text lines in this unit.

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

The number of text lines in this unit.

### getLocalizedTextLine

Get the localized text line at the specified index in a [`LocalizedTextLineElement`](localized-text-line-element.md) object.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSLocalizedTextLineElement*)getLocalizedTextLine:(NSInteger)index;
```
2. 
```swift
func getLocalizedTextLine(_ index: Int) -> DSLocalizedTextLineElement?
```

**Parameters**

`index`: The index of the localized text line to be retrieved.

**Return value**

The localized text line at the specified index in a [`LocalizedTextLineElement`](localized-text-line-element.md) object.

### removeAllLocalizedTextLines

Remove all the localized text lines from the unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)removeAllLocalizedTextLines;
```
2. 
```swift
func removeAllLocalizedTextLines()
```

### removeLocalizedTextLine

Remove a localized text line from the unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)removeLocalizedTextLine:(NSInteger)index;
```
2. 
```swift
func removeLocalizedTextLine(_ index: Int) -> Int
```

**Parameters**

`index`: The index of the localized text line to be removed.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addLocalizedTextLine

Add a localized text line to the unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)addLocalizedTextLine:(DSLocalizedTextLineElement*)element
           matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func addLocalizedTextLine(_ element: DSLocalizedTextLineElement, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`element`: A [`LocalizedTextLineElement`](localized-text-line-element.md) object as the localized text line to be added to the unit.

`matrixToOriginalImage`: The matrix to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setLocalizedTextLine

Set a localized text line in the unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setLocalizedTextLine:(NSInteger)index
                         element:(DSLocalizedTextLineElement*)element
           matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setLocalizedTextLine(_ index: Int, element: DSLocalizedTextLineElement, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`index`: The index of the localized text line to be set.

`element`:  A [`LocalizedTextLineElement`](localized-text-line-element.md) object as the localized text line to be set.

`matrixToOriginalImage`: The matrix to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getAuxiliaryRegionElements

Get all the auxiliary region elements in an array of [`AuxiliaryRegionElement`]({{ site.dcv_ios_api }}core/intermediate-results/auxiliary-region-element.html).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSAuxiliaryRegionElement*>*)getAuxiliaryRegionElements;
```
2. 
```swift
func getAuxiliaryRegionElements() -> [DSAuxiliaryRegionElement]?
```

**Return value**

All the auxiliary region elements in an array of [`AuxiliaryRegionElement`]({{ site.dcv_ios_api }}core/intermediate-results/auxiliary-region-element.html).

### getAuxiliaryRegionElementsCount

Get the number of auxiliary region elements in this unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)getAuxiliaryRegionElementsCount;
```
2. 
```swift
func getAuxiliaryRegionElementsCount() -> Int
```

**Return value**

The number of auxiliary region elements.

### getAuxiliaryRegionElement

Get the auxiliary region element at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable DSAuxiliaryRegionElement*)getAuxiliaryRegionElement:(NSInteger)index;
```
2. 
```swift
func getAuxiliaryRegionElement(_ index: Int) -> DSAuxiliaryRegionElement?
```

**Parameters**

`index`: The zero-based index of the auxiliary region element to retrieve.

**Return value**

The auxiliary region element at the specified index, or `nil` if the index is out of range.

### setAuxiliaryRegionElement

Set or replace the auxiliary region element at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setAuxiliaryRegionElement:(NSInteger)index
                              element:(DSAuxiliaryRegionElement*)element
                matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func setAuxiliaryRegionElement(_ index: Int, element: DSAuxiliaryRegionElement, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`index`: The zero-based index where the element should be set.

`element`: The auxiliary region element to set.

`matrixToOriginalImage`: The transformation matrix from the current image to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addAuxiliaryRegionElement

Add a new auxiliary region element to this unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)addAuxiliaryRegionElement:(DSAuxiliaryRegionElement*)element
                matrixToOriginalImage:(CGAffineTransform)matrixToOriginalImage;
```
2. 
```swift
func addAuxiliaryRegionElement(_ element: DSAuxiliaryRegionElement, matrixToOriginalImage: CGAffineTransform) -> Int
```

**Parameters**

`element`: The auxiliary region element to add.

`matrixToOriginalImage`: The transformation matrix from the current image to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### removeAuxiliaryRegionElement

Remove the auxiliary region element at the specified index.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)removeAuxiliaryRegionElement:(NSInteger)index;
```
2. 
```swift
func removeAuxiliaryRegionElement(_ index: Int) -> Int
```

**Parameters**

`index`: The zero-based index of the auxiliary region element to remove.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### removeAllAuxiliaryRegionElements

Remove all the auxiliary region elements from this unit.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(void)removeAllAuxiliaryRegionElements;
```
2. 
```swift
func removeAllAuxiliaryRegionElements()
```

