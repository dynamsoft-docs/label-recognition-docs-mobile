---
layout: default-layout
title: TextLineResultItem - Dynamsoft Label Recognizer Android Edition
description: The class TextLineResultItem of Dynamsoft Label Recognizer represents a text line result item recognized by a document layout analysis engine.
keywords: Text line result item
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TextLineResultItem
permalink: /programming/android/api-reference/text-line-result-item.html
---

# TextLineResultItem

The `TextLineResultItem` class represents a text line result item recognized by the library. It is derived from `CapturedResultItem` and is one of the base units of `RecognizedTextLinesResult`.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class TextLineResultItem extends CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html) -> TextLineResultItem

## Methods Summary

| Method | Description |
| ------ | ----------- |
| [`getText`](#gettext) | Gets the text content of the text line. |
| [`getLocation`](#getlocation) | Gets the location of the text line in the form of a quadrilateral. |
| [`getConfidence`](#getconfidence) | Gets the confidence of the text line recognition result. |
| [`getCharacterResults`](#getcharacterresults) | Get all the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.md) object. |

### getText

Gets the text content of the individual text line.

```java
String getText();
```

**Return value**

Returns the text content of the text line.

### getLocation

It is used to get the location of the text line in the form of a quadrilateral.

```java
Quadrilateral getLocation();
```

**Return value**

Returns the location of the text line in the form of a quadrilateral.

### getConfidence

It is used to get the confidence of the text line recognition result.

```java
int getConfidence();
```

**Return value**

Returns the confidence of the text line recognition result.

### getCharacterResults

Get all the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.md) object.

```java
CharacterResult[] getCharacterResults();
```

**Return value**

An array of [`CharacterResult`](character-result.md) contains all the characters.
