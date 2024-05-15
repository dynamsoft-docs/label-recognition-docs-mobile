---
layout: default-layout
title: RecognizedTextLineElement - Dynamsoft Label Recognizer Android Edition
description: The class RecognizedTextLineElement of Dynamsoft Label Recognizer Android edition represents a line of recognized text in an image.
keywords: Recognized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RecognizedTextLineElement
permalink: /programming/android/api-reference/recognized-text-line-element-v3.0.20.html
---

# RecognizedTextLineElement

The `RecognizedTextLineElement` class represents a line of recognized text in an image. It inherits from the [RegionObjectElement]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html) class.

## Definition

*Namespace:* com.dynamsoft.dlr.intermediate_results

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class RecognizedTextLineElement extends RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html) -> RecognizedTextLineElement

## Methods

| Method | Description |
| ------ | ----------- |
| [`getText`](#gettext) | Gets the recognized text. |
| [`getConfidence`](#getconfidence) | Gets the confidence level of the recognized text. |
| [`getCharacterResults`](#getcharacterresults) | Gets all the characters contained by the textline. |
| [`getRowNumber`](#getrownumber) | Gets the row number of the text line within the image. |

### getText

Gets the recognized text.

```java
String getText()
```

**Return value**

Returns the text of the text line.

### getConfidence

Gets the confidence level of the recognized text.

```java
int getConfidence()
```

**Return value**

Returns an integer value representing the confidence level of the recognized text.

### getCharacterResults

Gets all the characters contained by the textline in an array of [`CharacterResult`](character-result.md).

```java
CharacterResult[] getCharacterResults();
```

**Return value**

Returns an integer value representing the success of the operation. Zero indicates success, while any other value indicates failure.

### getRowNumber

Gets the row number of the text line within the image.

```java
int getRowNumber();
```

**Return value**

Returns an integer value representing the row number of the text line within the image.
