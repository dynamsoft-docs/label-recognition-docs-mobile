---
layout: default-layout
title: RecognizedTextLinesResult - Dynamsoft Capture Vision Flutter Edition
description: The class RecognizedTextLinesResult of Dynamsoft Capture Vision Flutter edition represents the result of a text recognition process.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RecognizedTextLinesResult

The `RecognizedTextLinesResult` class represents the overall result(s) of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class RecognizedTextLinesResult extends CapturedResultBase
```

## Properties

| Property | Types | Description |
| -------- | ----- | ----------- |
| [`getItems`](#getitems) | *List<TextLineResultItem>* | The text line result(s) recognized from the image/frame in an array of [`TextLineResultItem`](text-line-result-item.md). |

The following properties are inherited from [`CapturedResultBase`]({{ site.dcv_flutter_api }}core/captured-result-base.html):

| Property | Types | Description |
| -------- | ----- | ----------- |
| [`originalImageHashId`](#originalimagehashid) | *String* | The hash id of the original image. |
| [`rotationTransformMatrix`](#rotationtransformmatrix) | *Matrix4* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`](#errorcode) | *int* | The error code of this result. |
| [`errorMessage`](#errormessage) | *String* | The error message of this result. |

### getItems

The text line result(s) recognized from the image/frame in an array of [`TextLineResultItem`](text-line-result-item.md).

```dart
List<TextLineResultItem>? items;
```
