---
layout: default-layout
title: CharacterCluster - Dynamsoft Label Recognizer Android Edition
description: The class CharacterCluster of Dynamsoft Label Recognizer Android edition represents the clustered characters.
keywords: Character cluster
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CharacterCluster
---

# CharacterCluster

The `CharacterCluster` class represents the character clustering result. Each `CharacterCluster` object records the character info with its mean value.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class CharacterCluster
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getCharacter`](#getcharacter) | Gets the string that represents the character. |
| [`getMean`](#getmean) | Gets the mean value of the character cluster, of type `BufferedCharacterItem`. |

### getCharacter

Gets the string that represents the character.

```java
String getCharacter();
```

### getMean

Gets the mean value of the character cluster, of type `BufferedCharacterItem`.

```java
BufferedCharacterItem getMean();
```
