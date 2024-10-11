---
layout: default-layout
title: RecognizedTextLinesUnit - Dynamsoft Label Recognizer Android Edition
description: The class RecognizedTextLinesUnit of Dynamsoft Label Recognizer Android edition represents an intermediate result unit containing recognized text lines.
keywords: Recognized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RecognizedTextLinesUnit
---

# RecognizedTextLinesUnit

The `RecognizedTextLinesUnit` class represents an intermediate result unit containing recognized text lines. It inherits from the [IntermediateResultUnit]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html) class.

## Definition

*Namespace:* com.dynamsoft.dlr.intermediate_results

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class RecognizedTextLinesUnit extends IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html) -> RecognizedTextLinesUnit

## Methods

| Method | Description |
| ------ | ----------- |
| [`getRecognizedTextLines`](#getrecognizedtextlines) | Gets a pointer to the [`RecognizedTextLineElement`](recognized-text-line-element.md) object at the specified index. |

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

### setRecognizedTextLine

Sets the recognized text line at the specified index in a [`RecognizedTextLineElement`](recognized-text-line-element.md) object.

```java
int setRecognizedTextLine(RecognizedTextLineElement element, Matrix matrixToOriginalImage);
```

**Parameters**

`element`: The [`RecognizedTextLineElement`](recognized-text-line-element.md) object to be set.

`matrixToOriginalImage`: The matrix to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
