---
layout: default-layout
title: RecognizedTextLinesResult - Dynamsoft Capture Vision React Native Edition
description: Interface RecognizedTextLinesResult of Dynamsoft Capture Vision React Native edition represents the result of a text recognition process.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# RecognizedTextLinesResult

Interface `RecognizedTextLinesResult` represents the overall result(s) of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface RecognizedTextLinesResult extends CapturedResultBase
```

## Properties

| Property | Types | Description |
| -------- | ----- | ----------- |
| [`getItems`](#getitems) | *List<TextLineResultItem>* | The text line result(s) recognized from the image/frame in an array of [`TextLineResultItem`](text-line-result-item.md). |

The following properties are inherited from [`CapturedResultBase`]({{ site.dcv_react_native_api }}core/captured-result-base.html):

| Property | Types | Description |
| -------- | ----- | ----------- |
| [`originalImageHashId`]({{ site.dcv_react_native_api }}core/captured-result-base.html#originalimagehashid) | *String* | The hash id of the original image. |
| [`rotationTransformMatrix`]({{ site.dcv_react_native_api }}core/captured-result-base.html#rotationtransformmatrix) | *Matrix4* | The rotation transformation matrix of the original image relative to the rotated image. |
| [`errorCode`]({{ site.dcv_react_native_api }}core/captured-result-base.html#errorcode) | *int* | The error code of this result. |
| [`errorMessage`]({{ site.dcv_react_native_api }}core/captured-result-base.html#errormessage) | *String* | The error message of this result. |

### getItems

The text line result(s) recognized from the image/frame in an array of [`TextLineResultItem`](text-line-result-item.md).

```js
items?: Array<TextLineResultItem>;
```
