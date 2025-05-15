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
| [`CharacterResult`](#characterresult) | The constructor. |
| [`getCharacterH`](#getcharacterh) | Returns the highest confidence character recognized. |
| [`setCharacterH`](#setcharacterh) | Sets the highest confidence character recognized. |
| [`getCharacterM`](#getcharacterm) | Returns the medium confidence character recognized. |
| [`setCharacterM`](#setcharacterm) | Sets the medium confidence character recognized. |
| [`getCharacterL`](#getcharacterl) | Returns the lowest confidence character recognized. |
| [`setCharacterL`](#setcharacterl) | Sets the lowest confidence character recognized. |
| [`getLocation`](#getlocation) | Returns the location of the recognized character within the image. |
| [`setLocation`](#setlocation) | Sets the location of the recognized character within the image. |
| [`getCharacterHConfidence`](#getcharacterhconfidence) | Returns the confidence score for the highest confidence character. |
| [`setCharacterHConfidence`](#setcharacterhconfidence) | Sets the confidence score for the highest confidence character. |
| [`getCharacterMConfidence`](#getcharactermconfidence) | Returns the confidence score for the medium confidence character. |
| [`setCharacterMConfidence`](#setcharactermconfidence) | Sets the confidence score for the medium confidence character. |
| [`getCharacterLConfidence`](#getcharacterlconfidence) | Returns the confidence score for the lowest confidence character. |
| [`setCharacterLConfidence`](#setcharacterlconfidence) | Sets the confidence score for the lowest confidence character. |

### CharacterResult

The constructor.


```java
CharacterResult(char characterH, char characterM, char characterL, int characterHConfidence, int characterMConfidence, int characterLConfidence, Quadrilateral location);
```

### getCharacterH

Returns the highest confidence character recognized.

```java
char getCharacterH();
```

### setCharacterH

Sets the highest confidence character recognized.

```java
setCharacterH(char characterH);
```

### getCharacterM

Returns the medium confidence character recognized.

```java
char getCharacterM();
```

### setCharacterM

Sets the medium confidence character recognized.

```java
setCharacterM(char characterM);
```

### getCharacterL

Returns the lowest confidence character recognized.

```java
char getCharacterL();
```

### setCharacterL

Sets the lowest confidence character recognized.

```java
setCharacterL(char characterL);
```

### getLocation

Returns the location of the recognized character within the image.

```java
Quadrilateral getLocation();
```

### setLocation

Sets the location of the recognized character within the image.

```java
setLocation(Quadrilateral location);
```

### getCharacterHConfidence

Returns the confidence score for the highest confidence character.

```java
int getCharacterHConfidence();
```

### setCharacterHConfidence

Sets the confidence score for the highest confidence character.

```java
setCharacterHConfidence(int characterHConfidence);
```

### getCharacterMConfidence

Returns the confidence score for the medium confidence character.

```java
int characterMConfidence();
```

### setCharacterMConfidence

Sets the confidence score for the medium confidence character.

```java
setCharacterMConfidence(int characterMConfidence);
```

### getCharacterLConfidence

Returns the confidence score for the lowest confidence character.

```java
int characterLConfidence();
```

### setCharacterLConfidence

Sets the confidence score for the lowest confidence character.

```java
setCharacterLConfidence(int characterLConfidence);
```
