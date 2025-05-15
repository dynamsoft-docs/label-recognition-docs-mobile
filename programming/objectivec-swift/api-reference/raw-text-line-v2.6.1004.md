---
layout: default-layout
title: DSRawTextLine - Dynamsoft Label Recognizer iOS Edition
description: The class DSRawTextLine of Dynamsoft Label Recognizer iOS edition represents a unit which holds the raw text lines.
keywords: raw text lines unit, intermediate result unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSRawTextLine
---

# DSRawTextLine

The `DSRawTextLine` class represents a text line in an image. It can be in one of the following states:

- `TLS_LOCALIZED`: Localized but recognition not performed.
- `TLS_RECOGNITION_FAILED`: Recognition failed.
- `TLS_RECOGNIZED_SUCCESSFULLY`: Successfully recognized.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSRawTextLine: NSObject
```
2. 
```swift
class RawTextLine: NSObject
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getText`](#gettext) | Returns the recognized text. |
| [`setText`](#settext) | Sets the recognized text. |
| [`getConfidence`](#getconfidence) | Returns the confidence level of the recognized text. |
| [`getCharacterResults`](#getcharacterresults) | Returns all the characters contained by the textline. |
| [`getRowNumber`](#getrownumber) | Returns the row number of the text line within the image. |
| [`setRowNumber`](#setrownumber) | Sets the row number of the text line within the image. |
| [`getSpecificationName`](#getspecificationname) | Get the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |
| [`setSpecificationName`](#setspecificationname) | Sets the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |
| [`getLocation`](#getlocation) | Returns the location of the text line. |
| [`setLocation`](#setlocation) | Sets the location of the text line. |

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

Returns the recognized text.

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

### setRowNumber

Sets the row number of the text line within the image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setRowNumber:(NSInteger)rowNumber;
```
2. 
```swift
func setRowNumber(_ rowNumber: Int) -> Int
```

**Parameter**

`rowNumber`: The row number of the text line within the image.

**Return value**

Returns 0 if success, otherwise an error code.

### getSpecificationName

Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

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

### setSpecificationName

Sets the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setSpecificationName:(NSString *)specificationName;
```
2. 
```swift
func setSpecificationName(_ specificationName: String) -> Int
```

**Parameter**

`specificationName`: The name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

**Return value**

Returns 0 if success, otherwise an error code.

### getLocation

Returns a `Quadrilateral` object which represents the location of the text line.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(DSQuadrilateral *)getLocation;
```
2. 
```swift
func getLocation() -> Quadrilateral
```

**Return value**

A `Quadrilateral` object which represents the location of the text line.

### setLocation

Set the location of the text line.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(NSInteger)setLocation:(DSQuadrilateral *)location;
```
2. 
```swift
func setLocation(_ location: Quadrilateral) -> Int
```

**Parameter**

`location`: The location of the text line.

**Return value**

Returns 0 if success, otherwise an error code.

### getStatus

Returns the status of the text line.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
-(DSRawTextLineStatus)getStatus;
```
2. 
```swift
func getStatus() -> RawTextLineStatus
```

**Return value**

The status of the text line.
