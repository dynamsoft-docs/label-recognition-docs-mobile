---
layout: default-layout
title: CharacterResult - Dynamsoft Label Recognizer Android Edition
description: The class CharacterResult of Dynamsoft Label Recognizer Android edition represents the result of a character recognition process.
keywords: Character result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CharacterResult
permalink: /programming/android/api-reference/character-result.html
---

# CharacterResult

The `CharacterResult` class represents the result of a character recognition process. It contains the characters recognized (high, medium, and low confidence), their respective confidences, and the location of the character in a quadrilateral shape.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class CharacterResult
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getCharacterH`](#getcharacterh) | Returns the highest confidence character recognized. |
| [`getCharacterM`](#getcharacterm) | Returns the medium confidence character recognized. |
| [`getCharacterL`](#getcharacterl) | Returns the lowest confidence character recognized. |
| [`getLocation`](#getlocation) | Returns the location of the recognized character within the image.  |
| [`getCharacterHConfidence`](#getcharacterhconfidence) | Returns the confidence score for the highest confidence character. |
| [`getCharacterMConfidence`](#getcharactermconfidence) | Returns the confidence score for the medium confidence character. |
| [`getCharacterLConfidence`](#getcharacterlconfidence) | Returns the confidence score for the lowest confidence character. |

### getCharacterH

Returns the highest confidence character recognized.

```java
char getCharacterH();
```

### getCharacterM

Returns the medium confidence character recognized.

```java
char getCharacterM();
```

### getCharacterL

Returns the lowest confidence character recognized.

```java
char getCharacterL();
```

### getLocation

Returns the location of the recognized character within the image.

```java
Quadrilateral getLocation();
```

### getCharacterHConfidence

Returns the confidence score for the highest confidence character.

```java
int getCharacterHConfidence();
```

### getCharacterMConfidence

Returns the confidence score for the medium confidence character.

```java
int characterMConfidence();
```

### getCharacterLConfidence

Returns the confidence score for the lowest confidence character.

```java
int characterLConfidence();
```
