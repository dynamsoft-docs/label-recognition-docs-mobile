---
layout: default-layout
title: TextLineResultItem - Dynamsoft Capture Vision React Native Edition
description: Interface TextLineResultItem of Dynamsoft Capture Vision React Native edition represents a text line result item recognized by a document layout analysis engine.
keywords: Text line result item
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
---

# TextLineResultItem

Interface `TextLineResultItem` represents a single text line result item recognized by the library. It is derived from `CapturedResultItem` and is one of the base items of `RecognizedTextLinesResult`.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface TextLineResultItem extends CapturedResultItem
```

*Inheritance:* [CapturedResultItem]({{ site.dcv_react_native_api }}core/captured-result-item.html) -> TextLineResultItem

## Properties

| Property | Types | Description |
| -------- | ----- | ----------- |
| [`text`](#text) | *String* | Returns the text content of the text line. |
| [`location`](#location) | *Quadrilateral* | Returns the location of the text line in the form of a quadrilateral. |
| [`confidence`](#confidence) | *int* | Returns the confidence of the text line recognition result. |
| [`characterResults`](#characterresults) | *List<CharacterResult>* | Get all the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.md) object. |
| [`specificationName`](#specificationname) | *String* | Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |
| [`rawText`](#rawtext) | *String* | Returns the recognized raw text, excluding any concatenation separators. |

### text

Returns the text content of the individual text line.

```js
text: string;
```

### location

It is used to get the location of the text line in the form of a [Quadrilateral]({{ site.dcv_react_native_api }}core/quadrilateral.html).

```js
location: Quadrilateral;
```

### confidence

Returns the confidence of the individual text line recognition result.

```js
confidence: number;
```

### characterResults

Returns all the characters in the text line. Each character is represented by a [`CharacterResult`](character-result.md) object.

```js
characterResults: CharacterResult[];
```

### specificationName

Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

```js
specificationName:string;
```

### rawText

Returns the recognized raw text, excluding any concatenation separators.

```js
rawText: string;
```
