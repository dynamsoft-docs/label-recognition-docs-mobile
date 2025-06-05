---
layout: default-layout
title: TextLineResultItem - Dynamsoft Capture Vision MAUI Edition
description: The class TextLineResultItem of Dynamsoft Capture Vision MAUI edition represents a text line result item recognized by a document layout analysis engine.
keywords: Text line result item
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: TextLineResultItem
---

# TextLineResultItem

The `TextLineResultItem` class represents a single text line result item recognized by the library. It is derived from `CapturedResultItem` and is one of the base items of `RecognizedTextLinesResult`.

## Definition

*Namespace:* Dynamsoft.LabelRecognizer.Maui

*Assembly:* Dynamsoft.LabelRecognizer.Maui

```csharp
public class TextLineResultItem : CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcv_maui_api }}core/captured-result-item.html) -> TextLineResultItem

## Properties

| Property | Type | Description |
| --------- | ---- | ----------- |
| [`Text`](#text) | *String* | Returns the text content of the text line. |
| [`Location`](#location) | *Quadrilateral* | Returns the location of the text line in the form of a quadrilateral. |
| [`Confidence`](#confidence) | *int* | Returns the confidence of the text line recognition result. |
| [`CharacterResults`](#characterresults) | *CharacterResult[]* | Get all the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.html) object. |
| [`SpecificationName`](#specificationname) | *String* | Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |

### Text

Returns the text content of the individual text line.

```csharp
string Text { get; }
```

### Location

It is used to get the location of the text line in the form of a [Quadrilateral]({{ site.dcv_maui_api }}core/quadrilateral.html).

```csharp
Quadrilateral Location { get; }
```

### Confidence

Returns the confidence of the individual text line recognition result.

```csharp
int Confidence { get; }
```

### CharacterResults

Returns all the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.md) object.

```csharp
CharacterResult[] CharacterResults { get; }
```

### SpecificationName

Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

```csharp
String SpecificationName { get; }
```
