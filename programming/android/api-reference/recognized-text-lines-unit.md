---
layout: default-layout
title: RecognizedTextLinesUnit - Dynamsoft Label Recognizer Android Edition
description: The class RecognizedTextLinesUnit of Dynamsoft Label Recognizer represents an intermediate result unit containing recognized text lines.
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

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class RecognizedTextLinesUnit extends IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html) -> RecognizedTextLinesUnit

## Methods Summary

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
