---
layout: default-layout
title: DLRCharacterResult - Dynamsoft Label Recognition Android Class
description: This page shows the DLRCharacterResult struct of Dynamsoft Label Recognition for Android Language.
keywords: DLRCharacterResult, android
needAutoGenerateSidebar: true
permalink: /programming/android/api-reference/class/dlr-character-result.html
---


# DLRCharacterResult

> You are viewing a history document page of Dynamsoft Label Recognizer Android v1.x.

Stores the character result.
  

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`characterH`](#characterh) | *char* |
| [`characterM`](#characterm) | *char* |
| [`characterL`](#characterl) | *char* |
| [`location`](#location) | [`DLRQuadrilateral`](dlr-quadrilateral.md) |


### characterH
The recognized character with highest confidence.

```java
char com.dynamsoft.dlr.DLRCharacterResult.characterH
```

### characterM
The recognized character with middle confidence.

```java
char com.dynamsoft.dlr.DLRCharacterResult.characterM
```

### characterL
The recognized character with lowest confidence.

```java
char com.dynamsoft.dlr.DLRCharacterResult.characterL
```

### location
The location of current character.

```java
DLRQuadrilateral com.dynamsoft.dlr.DLRCharacterResult.location
```
