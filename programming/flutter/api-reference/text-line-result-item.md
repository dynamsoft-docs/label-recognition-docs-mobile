---
layout: default-layout
title: TextLineResultItem - Dynamsoft Capture Vision Flutter Edition
description: The class TextLineResultItem of Dynamsoft Capture Vision Flutter edition represents a text line result item recognized by a document layout analysis engine.
keywords: Text line result item
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextLineResultItem

The `TextLineResultItem` class represents a single text line result item recognized by the library. It is derived from `CapturedResultItem` and is one of the base items of `RecognizedTextLinesResult`.

## Definition

*Assembly:* dynamsoft_capture_vision_flutter

```dart
class TextLineResultItem extends CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcv_flutter_api }}core/captured-result-item.html) -> TextLineResultItem

## Properties

| Property | Types | Description |
| -------- | ----- | ----------- |
| [`text`](#text) | *String* | Returns the text content of the text line. |
| [`location`](#location) | *Quadrilateral* | Returns the location of the text line in the form of a quadrilateral. |
| [`confidence`](#confidence) | *int* | Returns the confidence of the text line recognition result. |
| [`characterResults`](#characterresults) | *List<CharacterResult>* | Get all the characters in the text line. Each character is represented by a [`CharacterResult`]({{ site.dcv_flutter_api }}core/character-result.html) object. |
| [`specificationName`](#specificationname) | *String* | Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |
| [`rawText`](#rawtext) | *String* | Returns the recognized raw text, excluding any concatenation separators. |

### text

Returns the text content of the individual text line.

```dart
String text;
```

### location

It is used to get the location of the text line in the form of a [Quadrilateral]({{ site.dcv_flutter_api }}core/quadrilateral.html).

```dart
Quadrilateral location;
```

### confidence

Returns the confidence of the individual text line recognition result.

```dart
int confidence;
```

### characterResults

Returns all the characters in the text line. Each character is represented by a [`CharacterResult`]({{ site.dcv_flutter_api }}core/character-result.html) object.

```dart
List<CharacterResult>? characterResults;
```

### specificationName

Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

```dart
String specificationName;
```

### rawText

Returns the recognized raw text, excluding any concatenation separators.

```dart
String rawText;
```
