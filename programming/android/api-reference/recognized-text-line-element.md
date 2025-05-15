---
layout: default-layout
title: RecognizedTextLineElement - Dynamsoft Label Recognizer Android Edition
description: The class RecognizedTextLineElement of Dynamsoft Label Recognizer Android edition represents a line of recognized text in an image.
keywords: Recognized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RecognizedTextLineElement
permalink: /programming/android/api-reference/recognized-text-line-element.html
---

# RecognizedTextLineElement

The `RecognizedTextLineElement` class extends the [RegionObjectElement]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html) class and represents a recognized text line element.

## Definition

*Namespace:* com.dynamsoft.dlr.intermediate_results

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class RecognizedTextLineElement extends RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html) -> RecognizedTextLineElement

## Methods

| Method | Description |
| ------ | ----------- |
| [`getText`](#gettext) | Returns the recognized text of the line. |
| [`getConfidence`](#getconfidence) | Returns the confidence score for the recognized text line. |
| [`getCharacterResults`](#getcharacterresults) | Returns all the results for individual characters within the text line. |
| [`getRowNumber`](#getrownumber) | Returns the row number of the text line, starting from 1. |
| [`setText`](#settext) | Sets the recognized text of the line. |
| [`getSpecificationName`](#getspecificationname) | Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |
| [`getRawText`](#getrawtext) | Returns the recognized raw text, excluding any concatenation separators. |

### getText

Returns the recognized text of the line.

```java
String getText()
```

**Return value**

The recognized text of the line.

### getConfidence

Returns the confidence score for the recognized text line.

```java
int getConfidence()
```

**Return value**

The confidence score for the recognized text line.

### getCharacterResults

Returns all the results for individual characters within the text line, defined by [`CharacterResult`](character-result.md).

```java
CharacterResult[] getCharacterResults();
```

**Return value**

The results for individual characters within the text line, defined by [`CharacterResult`](character-result.md).

### getRowNumber

Returns the row number of the text line, starting from 1.

```java
int getRowNumber();
```

**Return value**

The row number of the text line, starting from 1.

### setText

Sets the recognized text of the line.

```java
void setText(String text);
```

**Parameters**

`text`: The text to be set.

### getSpecificationName

Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

```java
String getSpecificationName();
```

**Return value**

The name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

### getRawText

Returns the recognized raw text, excluding any concatenation separators.

```java
String getRawText();
```

**Return value**

The recognized raw text, excluding any concatenation separators.
