---
layout: default-layout
title: CharacterResult - Dynamsoft Label Recognizer MAUI Edition
description: The class CharacterResult of Dynamsoft Label Recognizer MAUI edition represents the result of a character recognition process.
keywords: Character result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CharacterResult
---

# CharacterResult

The `CharacterResult` class represents the result of a character recognition process. It contains the characters recognized (high, medium, and low confidence), their respective confidences, and the location of the character in a quadrilateral shape.

## Definition

*Namespace:* Dynamsoft.LabelRecognizer.Maui

*Assembly:* Dynamsoft.LabelRecognizer.Maui

```csharp
class CharacterResult
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`CharacterH`](#characterh) | *char* | Returns the highest confidence character recognized. |
| [`CharacterM`](#characterm) | *char* | Returns the medium confidence character recognized. |
| [`CharacterL`](#characterl) | *char* | Returns the lowest confidence character recognized. |
| [`Location`](#location) | *Quadrilateral* | Returns the location of the recognized character within the image.  |
| [`CharacterHConfidence`](#characterhconfidence) | *int* | Returns the confidence score for the highest confidence character. |
| [`CharacterMConfidence`](#charactermconfidence) | *int* | Returns the confidence score for the medium confidence character. |
| [`CharacterLConfidence`](#characterlconfidence) | *int* | Returns the confidence score for the lowest confidence character. |

### CharacterH

Returns the highest confidence character recognized.

```csharp
char CharacterH { get; }
```

### CharacterM

Returns the medium confidence character recognized.

```csharp
char CharacterM { get; }
```

### CharacterL

Returns the lowest confidence character recognized.

```csharp
char CharacterL { get; }
```

### Location

Returns the location of the recognized character within the image.

```csharp
Quadrilateral Location { get; }
```

### CharacterHConfidence

Returns the confidence score for the highest confidence character.

```csharp
int CharacterHConfidence { get; }
```

### CharacterMConfidence

Returns the confidence score for the medium confidence character.

```csharp
int CharacterMConfidence { get; }
```

### CharacterLConfidence

Returns the confidence score for the lowest confidence character.

```csharp
int CharacterLConfidence { get; }
```
