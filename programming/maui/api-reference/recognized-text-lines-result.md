---
layout: default-layout
title: RecognizedTextLinesResult - Dynamsoft Capture Vision MAUI Edition
description: The class RecognizedTextLinesResult of Dynamsoft Capture Vision MAUI edition represents the result of a text recognition process.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RecognizedTextLinesResult
---

# RecognizedTextLinesResult

The `RecognizedTextLinesResult` class represents the overall result(s) of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Namespace:* Dynamsoft.LabelRecognizer.Maui

*Assembly:* Dynamsoft.LabelRecognizer.Maui

```csharp
class RecognizedTextLinesResult
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`OriginalImageHashId`](#originalimagehashid) | *String* | Gets the hash ID of the original image. |
| [`Items`](#items) | *IList<TextLineResultItem>* | Gets the text line result item at the specified index. |
| [`RotationTransformMatrix`](#rotationtransformmatrix) | *Matrix* | Get the rotation transformation matrix of the original image relative to the rotated image.|
| [`ErrorCode`](#errorcode) | *int* | Gets the error code of the recognition result, if an error occurred. |
| [`ErrorMessage`](#errormessage) | *String* | Gets the error message of the recognition result, if an error occurred. |

### OriginalImageHashId

Get the hash id of the original image. You can use this ID to get the original image via the [`IntermediateResultManager`]({{ site.dcv_maui_api }}core/intermediate-results/intermediate-result-manager.html) class.

```csharp
String OriginalImageHashId { get; }
```

**Return value**

Returns the hash ID of the original image as a string.

### Items

Gets all the text line result(s) recognized from the image/frame in an array of [`DSTextLineResultItem`](text-line-result-item.md).

```csharp
IList<TextLineResultItem> Items { get; }
```

**Return value**

Returns an array of `TextLineResultItem` that contains all text line recognition results.

### RotationTransformMatrix

Get the rotation transformation matrix of the original image relative to the rotated image.

```csharp
Matrix RotationTransformMatrix { get; }
```

**Return Value**

A `Matrix` which represents the rotation transform matrix.

### ErrorCode

Gets the error code of the recognition result, if an error occurred.

```csharp
int ErrorCode { get; }
```

**Return value**

Returns the error code of the recognition result, or 0 if no error occurred.

### ErrorMessage

Gets the error message of the recognition result, if an error occurred.

```csharp
String ErrorMessage { get; }
```

**Return value**

Returns a string that describes the error message.
