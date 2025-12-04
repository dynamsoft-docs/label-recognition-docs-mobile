---
layout: default-layout
title: CharacterResult - Dynamsoft Capture Vision React Native Edition
description: Interface CharacterResult of Dynamsoft Capture Vision React Native edition represents the result of a character recognition process.
keywords: Character result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CharacterResult
---

# CharacterResult

Interface `CharacterResult` represents the result of a character recognition process. It contains the characters recognized (high, medium, and low confidence), their respective confidences, and the location of the character in a quadrilateral shape.

## Definition

*Assembly:* dynamsoft-capture-vision-react-native

```js
interface CharacterResult
```

## Properties

| Property | Types | Description |
| -------- | ----- | ----------- |
| [`characterH`](#characterh) | *string* | The character with the highest confidence. |
| [`characterM`](#characterm) | *string* | The character with medium confidence. |
| [`characterL`](#characterl) | *string* | The character with the lowest confidence. |
| [`characterHConfidence`](#characterhconfidence) | *number* | The confidence score for the highest confidence character. |
| [`characterMConfidence`](#charactermconfidence) | *number* | The confidence score for the medium confidence character. |
| [`characterLConfidence`](#characterlconfidence) | *number* | The confidence score for the lowest confidence character. |

### CharacterH

The character with the highest confidence.

```js
characterH: string;
```

### CharacterM

The character with medium confidence.

```js
characterM: string;
```

### CharacterL

The character with the lowest confidence.

```js
characterL: string;
```

### CharacterHConfidence

The confidence score for the highest confidence character.

```js
characterHConfidence: number;
```

### CharacterMConfidence

The confidence score for the medium confidence character.

```js
characterMConfidence: number;
```

### CharacterLConfidence

The confidence score for the lowest confidence character.

```js
characterLConfidence: number;
```
