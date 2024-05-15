---
layout: default-layout
title: BufferedCharacterItem - Dynamsoft Label Recognizer Android Edition
description: The class BufferedCharacterItem of Dynamsoft Label Recognizer Android edition represents a buffered character.
keywords: Buffered Character Item Set
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BufferedCharacterItem
---

# BufferedCharacterItem

The `BufferedCharacterItem` class represents a buffered character.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class BufferedCharacterItem
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getCharacter`](#getcharacter) | Gets the string that represents the character. |
| [`getImage`](#getimage) | Gets the image data of the buffered character. |
| [`getFeatures`](#getfeatures) | Gets a `HashMap` that contains all buffered character features. The values of the dictionary are float type. |

### getCharacter

Gets the string that represents the character.

```java
String getCharacter();
```

### getImage

Gets the image data of the buffered character.

```java
ImageData getImage();
```

### getFeatures

Gets a `HashMap` that contains all buffered character features. The values of the dictionary are float type.

```java
HashMap<Integer, Float> getFeatures();
```
