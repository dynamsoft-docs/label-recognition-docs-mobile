---
layout: default-layout
title: CharacterResult - Dynamsoft Label Recognizer Android Edition
description: The class CharacterResult of Dynamsoft Label Recognizer represents the result of a character recognition process.
keywords: Character result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CharacterResult
permalink: /programming/android/api-reference/character-result.html
---

# CharacterResult

The `CharacterResult` class represents the result of a character recognition process. It contains the characters recognized (high, medium, and low confidence), their respective confidences, and the location of each character in a quadrilateral shape.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class CharacterResult
```

## Methods Summary

| Method | Description |
| ------ | ----------- |
| [`getCharacterH`](#getcharacterh) | Get the character with high confidence. |
| [`getCharacterM`](#getcharacterm) | Get the character with medium confidence. |
| [`getCharacterL`](#getcharacterl) | Get the character with low confidence. |
| [`getLocation`](#getlocation) | Get the location of the character in a quadrilateral shape. |
| [`getCharacterHConfidence`](#getcharacterhconfidence) | Get the confidence of the character with high confidence. |
| [`getCharacterMConfidence`](#getcharactermconfidence) | Get the confidence of the character with medium confidence. |
| [`getCharacterLConfidence`](#getcharacterlconfidence) | Get the confidence of the character with low confidence. |

### getCharacterH

Get the character with high confidence.

```java
char getCharacterH();
```

### getCharacterM

Get the character with medium confidence.

```java
char getCharacterM();
```

### getCharacterL

Get the character with low confidence.

```java
char getCharacterL();
```

### getLocation

Get the location of the character in a quadrilateral shape.

```java
Quadrilateral getLocation();
```

### getCharacterHConfidence

Get the confidence of the character with high confidence.

```java
int getCharacterHConfidence();
```

### getCharacterMConfidence

Get the confidence of the character with medium confidence.

```java
int characterMConfidence();
```

### getCharacterLConfidence

Get the confidence of the character with low confidence.

```java
int characterLConfidence();
```
