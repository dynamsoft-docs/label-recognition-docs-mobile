---
layout: default-layout
title: BufferedCharacterItemSet - Dynamsoft Label Recognizer Android Edition
description: The class BufferedCharacterItemSet of Dynamsoft Label Recognizer Android edition represents the buffered characters and the character clusters that generated from the buffered characters.
keywords: Buffered Character Item Set
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: BufferedCharacterItemSet
---

# BufferedCharacterItemSet

The `BufferedCharacterItemSet` class represents the buffered characters and the character cluster that generated from the buffered characters.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class BufferedCharacterItemSet
```

## Methods

| Method | Description |
| ------ | ----------- |
| [`getItems`](#getitems) | Gets an array of `BufferedCharacterItem` objects that represents the buffered characters. |
| [`getCharacterClusters`](#getcharacterclusters) | Gets an array of `CharacterCluster` objects that represents the clustered characters. |

### getItems

Gets an array of `BufferedCharacterItem` objects that represents the buffered characters.

```java
BufferedCharacterItem[] getItems();
```

### getCharacterClusters

Gets an array of `CharacterCluster` objects that represents the clustered characters.

```java
CharacterCluster[] getCharacterClusters();
```
