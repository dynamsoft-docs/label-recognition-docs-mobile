---
layout: default-layout
title: DSRecognizedTextLineElement - Dynamsoft Label Recognizer iOS Edition
description: The class DSRecognizedTextLineElement of Dynamsoft Label Recognizer iOS edition represents a line of recognized text in an image.
keywords: Recognized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSRecognizedTextLineElement
---

# DSRecognizedTextLineElement

The `DSRecognizedTextLineElement` class represents a line of recognized text in an image. It inherits from the [DSRegionObjectElement]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html) class.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getText`](#gettext) | Returns the recognized text. |
| [`setText`](#settext) | Sets the recognized text. |
| [`getRawText`](#getrawtext) | Returns the recognized raw text, excluding any concatenation separators. |
| [`getConfidence`](#getconfidence) | Returns the confidence level of the recognized text. |
| [`getCharacterResults`](#getcharacterresults) | Returns all the characters contained by the textline. |
| [`getRowNumber`](#getrownumber) | Returns the row number of the text line within the image. |
| [`getSpecificationName`](#getspecificationname) | Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |

### getText

Returns the recognized text.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSString*)getText;
```
2. 
```swift
func getText() -> String
```

**Return value**

Returns the text of the text line.

### setText

Sets the recognized text.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setText:(NSString *)text;
```
2. 
```swift
func setText(_ text: String) -> Int
```

**Parameter**

`text`: The text.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getRawText

Returns the recognized raw text, excluding any concatenation separators.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSString*)getRawText;
```
2. 
```swift
func getRawText() -> String
```

**Return value**

The recognized raw text, excluding any concatenation separators.

### getConfidence

Returns the confidence level of the recognized text.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)getConfidence;
```
2. 
```swift
func getConfidence() -> Int
```

**Return value**

Returns the confidence level of the text line.

### getCharacterResults

Returns all the characters contained by the textline in an array of [`DSCharacterResult`](character-result.md).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(nullable NSArray<DSCharacterResult *>*)getCharacterResults;
```
2. 
```swift
func getCharacterResults() -> [CharacterResult]
```

**Return value**

Returns all the characters contained by the textline in an array of [`DSCharacterResult`](character-result.md).

### getRowNumber

Returns the row number of the text line within the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)getRowNumber;
```
2. 
```swift
func getRowNumber() -> Int
```

**Return value**

Returns the row number of the text line within the image.

### getSpecificationName

Get the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSString *)getSpecificationName;
```
2. 
```swift
func getSpecificationName() -> String
```

**Return value**

The name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.
