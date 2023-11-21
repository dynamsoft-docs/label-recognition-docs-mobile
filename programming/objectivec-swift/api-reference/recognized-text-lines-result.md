---
layout: default-layout
title: DSRecognizedTextLinesResult - Dynamsoft Label Recognizer iOS Edition
description: The class DSRecognizedTextLinesResult of Dynamsoft Label Recognizer represents the result of a text recognition process.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSRecognizedTextLinesResult
permalink: /programming/objectivec-swift/api-reference/recognized-text-lines-result.html
---

# DSRecognizedTextLinesResult

The `DSRecognizedTextLinesResult` class represents the overall result(s) of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSRecognizedTextLinesResult : NSObject
```
2. 
```swift
class RecognizedTextLinesResult: NSObject
```

## Property Summary

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`originalImageHashId`](#originalimagehashid) | *NSString* | The hash ID of the original image. |
| [`originalImageTag`](#originalimagetag) | *DSImageTag* | The tag of the original image stores in a [`DSImageTag`]({{ site.dcv_ios_api }}core/basic-structure/image-tag.html) object. |
| [`items`](#items) | *NSArray<*DSTextLineResultItem*>* | All the text line result(s) that are recognized from the image in an array of [`DSTextLineResultItem`](text-line-result-item.md). |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image.|
| [`errorCode`](#errorcode) | *NSInteger* | The error code of the recognition result, if an error occurred. |
| [`errorMessage`](#errormessage) | *NSString* | The error message of the recognition result, if an error occurred. |

### originalImageHashId

The hash id of the source image. You can use this ID to get the source image via [`DSIntermediateResultManager`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-manager.html) class.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) NSString* originalImageHashId;
```
2. 
```swift
var originalImageHashId: String? { get }
```

### originalImageTag

Returns the [`ImageTag`]({{ site.dcv_ios_api }}core/basic-structures/image-tag.html) of the source image. The image tag contains info about the image such as the image ID and the image capture distance mode.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) DSImageTag* originalImageTag;
```
2. 
```swift
var originalImageTag: ImageTag? { get }
```

**Return value**

that contain the image extra info.

### items

All the text line result(s) recognized from the image/frame in an array of [`DSTextLineResultItem`](text-line-result-item.md).

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) NSArray<DSTextLineResultItem*>* items;
```
2. 
```swift
var items: [TextLineResultItem]? { get }
```

### rotationTransformMatrix

Get the rotation transformation matrix of the original image relative to the rotated image.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, assign, readonly) CGAffineTransform rotationTransformMatrix;
```
2. 
```swift
var rotationTransformMatrix: CGAffineTransform { get }
```

### errorCode

Returns the error code of this result should something go wrong.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) NSInteger errorCode;
```
2. 
```swift
var errorCode: Int { get }
```

### errorMessage

Returns the error message of this result should something go wrong.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) NSString * errorMessage;
```
2. 
```swift
var errorMessage: String { get }
```
