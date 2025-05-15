---
layout: default-layout
title: RecognizedTextLinesResult - Dynamsoft Label Recognizer Android Edition
description: The class RecognizedTextLinesResult of Dynamsoft Label Recognizer Android edition represents the result of a text recognition process.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RecognizedTextLinesResult
permalink: /programming/android/api-reference/recognized-text-lines-result.html
---

# RecognizedTextLinesResult

The `RecognizedTextLinesResult` class represents the overall result(s) of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class RecognizedTextLinesResult extends CapturedResultBase
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getItems`](#getitems) | Gets the text line result item at the specified index. |

The following methods are inherited from [`CapturedResultBase`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html):

| Method | Description |
| ------ | ----------- |
| [`getOriginalImageHashId`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#getoriginalimagehashid) | Gets the hash id of the original image. |
| [`getOriginalImageTag`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#getoriginalimagetag) | Gets the [ImageTag](image-tag.md) of the original image. |
| [`getRotationTransformMatrix`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#getrotationtransformmatrix) | Gets the rotation transformation matrix of the original image relative to the rotated image. |
| [`getErrorCode`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#geterrorcode) | Gets the error code of this result. |
| [`getErrorMessage`]({{ site.dcv_android_api }}core/basic-structures/captured-result-base.html#geterrormessage) | Gets the error message of this result. |

### getItems

Gets all the text line result(s) recognized from the image/frame in an array of [`DSTextLineResultItem`](text-line-result-item.md).

```java
TextLineResultItem[] getItems();
```

**Return value**

Returns an array of `TextLineResultItem` that contains all text line recognition results.
