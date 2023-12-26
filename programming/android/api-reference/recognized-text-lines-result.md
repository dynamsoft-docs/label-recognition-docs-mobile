---
layout: default-layout
title: RecognizedTextLinesResult - Dynamsoft Label Recognizer Android Edition
description: The class RecognizedTextLinesResult of Dynamsoft Label Recognizer represents the result of a text recognition process.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RecognizedTextLinesResult
permalink: /programming/android/api-reference/recognized-text-lines-result.html
---

# RecognizedTextLinesResult

The `RecognizedTextLinesResult` class represents the result of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class RecognizedTextLinesResult
```

## Methods Summary

| Method | Description |
| ------ | ----------- |
| [`getOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`getOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image. |
| [`getItems`](#getitems) | Gets the text line result item at the specified index. |
| [`getRotationTransformMatrix`](#getrotationtransformmatrix) | Get the rotation transformation matrix of the original image relative to the rotated image.|
| [`getErrorCode`](#geterrorcode) | Gets the error code of the recognition result, if an error occurred. |
| [`getErrorMessage`](#geterrormessage) | Gets the error message of the recognition result, if an error occurred. |

### getOriginalImageHashId

Get the hash id of the original image. You can use this ID to get the original image via the [`IntermediateResultManager`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-manager.html) class.

```java
String getOriginalImageHashId();
```

**Return value**

Returns the hash ID of the original image as a string.

### getOriginalImageTag

Get the [`ImageTag`]({{ site.dcv_android_api }}core/basic-structures/image-tag.html) of the original image. The image tag contains info about the image such as the image ID and the image capture distance mode.

```java
ImageTag getOriginalImageTag();
```

**Return value**

An [`ImageTag`]({{ site.dcv_android_api }}core/basic-structures/image-tag.html) object that contain the image extra info.

### getItems

Gets all the text line result(s) recognized from the image/frame in an array of [`DSTextLineResultItem`](text-line-result-item.md).

```java
TextLineResultItem[] getItems();
```

**Return value**

Returns an array of `TextLineResultItem` that contains all text line recognition results.

### getRotationTransformMatrix

Get the rotation transformation matrix of the original image relative to the rotated image.

```java
Matrix getRotationTransformMatrix();
```

**Return Value**

A `Matrix` which represents the rotation transform matrix.

### getErrorCode

Gets the error code of the recognition result, if an error occurred.

```java
int getErrorCode();
```

**Return value**

Returns the error code of the recognition result, or 0 if no error occurred.

### getErrorMessage

Get the error message of this result should something go wrong.

```java
String getErrorMessage();
```

**Return value**

Returns a string that describes the error message.
