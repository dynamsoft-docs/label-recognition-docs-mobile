---
layout: default-layout
title: DSRecognizedTextLineElement - Dynamsoft Label Recognizer iOS Edition
description: The class DSRecognizedTextLineElement of Dynamsoft Label Recognizer iOS edition represents a line of recognized text in an image.
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

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getText`](#gettext) | Gets the recognized text. |
| [`setText`](#settext) | Sets the recognized text. |
| [`getConfidence`](#getconfidence) | Gets the confidence level of the recognized text. |
| [`getCharacterResults`](#getcharacterresults) | Gets all the characters contained by the textline. |
| [`getRowNumber`](#getrownumber) | Gets the row number of the text line within the image. |
| [`getSpecificationName`](#getspecificationname) | Get the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |

### getText

Gets the recognized text.

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

### getConfidence

Gets the confidence level of the recognized text.

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

Gets all the characters contained by the textline in an array of [`DSCharacterResult`](character-result.md).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSArray<DSCharacterResult *>*)getCharacterResults;
```
2. 
```swift
func getCharacterResults() -> [CharacterResult]
```

**Return value**

Returns all the characters contained by the textline in an array of [`DSCharacterResult`](character-result.md).

### getRowNumber

Gets the row number of the text line within the image.

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
