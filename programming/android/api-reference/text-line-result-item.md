---
layout: default-layout
title: TextLineResultItem - Dynamsoft Label Recognizer Android Edition
description: The class TextLineResultItem of Dynamsoft Label Recognizer Android edition represents a text line result item recognized by a document layout analysis engine.
keywords: Text line result item
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TextLineResultItem
---

# TextLineResultItem

The `TextLineResultItem` class represents a single text line result item recognized by the library. It is derived from `CapturedResultItem` and is one of the base items of `RecognizedTextLinesResult`.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class TextLineResultItem extends CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html) -> TextLineResultItem

## Methods

| Method | Description |
| ------ | ----------- |
| [`getText`](#gettext) | Returns the text content of the text line. |
| [`getLocation`](#getlocation) | Returns the location of the text line in the form of a quadrilateral. |
| [`getConfidence`](#getconfidence) | Returns the confidence of the text line recognition result. |
| [`getCharacterResults`](#getcharacterresults) | Get all the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.md) object. |
| [`getSpecificationName`](#getspecificationname) | Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |
| [`getRawText`](#getrawtext) | Returns the recognized raw text, excluding any concatenation separators. |

### getText

Returns the text content of the individual text line.

```java
String getText();
```

**Return value**

Returns the text content of the text line.

### getLocation

It is used to get the location of the text line in the form of a [Quadrilateral]({{ site.dcv_android_api }}core/basic-structures/quadrilateral.html).

```java
Quadrilateral getLocation();
```

**Return value**

Returns the location of the text line in the form of a quadrilateral.

### getConfidence

Returns the confidence of the individual text line recognition result.

```java
int getConfidence();
```

**Return value**

Returns the confidence of the text line recognition result.

### getCharacterResults

Returns all the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.md) object.

```java
CharacterResult[] getCharacterResults();
```

**Return value**

An array of [`CharacterResult`](character-result.md) contains all the characters.

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
