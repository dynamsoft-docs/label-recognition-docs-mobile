---
layout: default-layout
title: DSRecognizedTextLinesResult - Dynamsoft Label Recognizer iOS Edition
description: The class DSRecognizedTextLinesResult of Dynamsoft Label Recognizer iOS edition represents the result of a text recognition process.
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
@interface DSRecognizedTextLinesResult : DSCapturedResultBase
```
2. 
```swift
class RecognizedTextLinesResult: CapturedResultBase
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`items`](#items) | *NSArray<DSTextLineResultItem \*> \** | All the text line result items that recognized from the image in an array of [`DSTextLineResultItem`](text-line-result-item.md). |

The following attributes are inherited from [`DSCapturedResultBase`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html):

| Attributes | Type | Description |
| ---------- | ---- | ----------- |
| [`originalImageHashId`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#originalimagehashid) | *NSString \** | The hash id of the original image. |
| [`originalImageTag`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#originalimagetag) | *DSImageTag \** | The [DSImageTag](image-tag.md) of the original image. |
| [`rotationTransformMatrix`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#rotationtransformmatrix) | *CGAffineTransform* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#errorcode) | *NSInteger* | Get the error code of this result. |
| [`errorMessage`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-base.html#errormessage) | *NSString \** | Get the error message of this result. |

### items

All the text line result items that recognized from the image in an array of [`DSTextLineResultItem`](text-line-result-item.md).

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
