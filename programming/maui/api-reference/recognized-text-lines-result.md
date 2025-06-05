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
class RecognizedTextLinesResult : CapturedResultBase
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`Items`](#items) | *TextLineResultItem[]* | Gets the text line result item at the specified index. |

The following properties are inherited from [`CapturedResultBase`]({{ site.dcv_maui_api }}core/captured-result-base.html):

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`OriginalImageHashId`]({{ site.dcv_maui_api }}core/captured-result-base.html#originalimagehashid) | *string* | Represents the hash id of the original image. |
| [`RotationTransformMatrix`]({{ site.dcv_maui_api }}core/captured-result-base.html#rotationtransformmatrix) | *Matrix* | Represents the rotation transformation matrix of the original image relative to the rotated image. |
| [`ErrorCode`]({{ site.dcv_maui_api }}core/captured-result-base.html#errorcode) | *int* | Represents the error code of this result. |
| [`ErrorMessage`]({{ site.dcv_maui_api }}core/captured-result-base.html#errormessage) | *string* | Represents the error message of this result. |

### Items

Gets all the text line result(s) recognized from the image/frame in an array of [`DSTextLineResultItem`](text-line-result-item.md).

```csharp
TextLineResultItem[]? Items { get; }
```
