---
layout: default-layout
title: RecognizedTextLinesUnit - Dynamsoft Label Recognizer Android Edition
description: The class RecognizedTextLinesUnit of Dynamsoft Label Recognizer Android edition represents an intermediate result unit containing recognized text lines.
keywords: Recognized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RecognizedTextLinesUnit
permalink: /programming/android/api-reference/recognized-text-lines-unit.html
---

# RecognizedTextLinesUnit

The `RecognizedTextLinesUnit` class represents an intermediate result unit containing recognized text lines. It inherits from the [IntermediateResultUnit]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html) class.

## Definition

*Namespace:* com.dynamsoft.dlr.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class RecognizedTextLinesUnit extends IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html) -> RecognizedTextLinesUnit

## Methods

| Method | Description |
| ------ | ----------- |
| [`addRecognizedTextLine`](#addrecognizedtextline) | Adds a recognized text line. |
| [`getRecognizedTextLines`](#getrecognizedtextlines) | Get all the recognized text lines in an array of [`DSRecognizedTextLineElement`](recognized-text-line-element.md). |
| [`getCount`](#getcount) | Returns the number of text lines in this unit. |
| [`getRecognizedTextLine`](#getrecognizedtextline) | Returns the text line at the specified index in a [`DSRecognizedTextLineElement`](recognized-text-line-element.md) object. |
| [`removeAllRecognizedTextLines`](#removeallrecognizedtextlines) | Removes all the recognized text lines from this unit. |
| [`removeRecognizedTextLine`](#removerecognizedtextline) | Removes the recognized text line at the specified index. |
| [`setRecognizedTextLine(index, element, matrixToOriginalImage)`](#setrecognizedtextlineindex-element-matrixtooriginalimage) | Sets the recognized text line at the specified index. |
| [`setRecognizedTextLine(element, matrixToOriginalImage)`](#setrecognizedtextlineelement-matrixtooriginalimage) | Sets the recognized text line at the specified index. |

### AddRecognizedTextLine

Adds a recognized text line.

```java
int addRecognizedTextLine(RecognizedTextLineElement element, Matrix matrixToOriginalImage);
```

**Parameters**

`element`: The [`RecognizedTextLineElement`](recognized-text-line-element.md) object to be added.

`matrixToOriginalImage`: The matrix to transform the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getRecognizedTextLines

Gets all the recognized text lines of this unit in an array of [`RecognizedTextLineElement`](recognized-text-line-element.md).

```java
RecognizedTextLineElement[] getRecognizedTextLines();
```

**Return value**

An array of [`RecognizedTextLineElement`](recognized-text-line-element.md) that contains all recognized text line of this unit.

### getCount

Gets the number of recognized text lines in this unit.

```java
int getCount();
```

**Return value**

The number of recognized text lines in this unit.

### getRecognizedTextLine

Gets the recognized text line at the specified index in a [`RecognizedTextLineElement`](recognized-text-line-element.md) object.

```java
RecognizedTextLineElement getRecognizedTextLine(int index);
```

**Parameters**

`index`: The index of the recognized text line in this unit.

**Return value**

The recognized text line at the specified index in a [`RecognizedTextLineElement`](recognized-text-line-element.md) object.

### removeAllRecognizedTextLines

Removes all the recognized text lines from the unit.

```java
void removeAllRecognizedTextLines();
```

### removeRecognizedTextLine

Removes the [`RecognizedTextLineElement`](recognized-text-line-element.md) at the specified index.

```java
int removeRecognizedTextLine(int index);
```

**Parameters**

`index`: The index of the recognized text line to remove.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setRecognizedTextLine(index, element, matrixToOriginalImage)

Sets the recognized text line at the specified index in a [`RecognizedTextLineElement`](recognized-text-line-element.md) object.

```java
int setRecognizedTextLine(int index, RecognizedTextLineElement element, Matrix matrixToOriginalImage);
```

**Parameters**

`index`: The index of the recognized text line to set.

`element`: The [`RecognizedTextLineElement`](recognized-text-line-element.md) object to be set.

`matrixToOriginalImage`: The matrix to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setRecognizedTextLine(element, matrixToOriginalImage)

> This method is deprecated.

Sets the recognized text line at the specified index in a [`RecognizedTextLineElement`](recognized-text-line-element.md) object.

```java
int setRecognizedTextLine(RecognizedTextLineElement element, Matrix matrixToOriginalImage);
```

**Parameters**

`element`: The [`RecognizedTextLineElement`](recognized-text-line-element.md) object to be set.

`matrixToOriginalImage`: The matrix to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
