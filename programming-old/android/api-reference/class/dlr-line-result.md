---
layout: default-layout
title: DLRLineResult - Dynamsoft Label Recognition Android Class
description: This page shows the DLRLineResult struct of Dynamsoft Label Recognition for Android Language.
keywords: DLRLineResult, struct, android
needAutoGenerateSidebar: true
permalink: /programming/android/api-reference/class/dlr-line-result.html
---


# DLRLineResult

> You are viewing a history document page of Dynamsoft Label Recognizer Android v1.x.

Stores the line result.
  

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`lineSpecificationName`](#linespecificationname) | *String* |
| [`text`](#text) | *String* |
| [`characterModelName`](#charactermodelname) | *String* |
| [`location`](#location) | [`DLRQuadrilateral`](dlr-quadrilateral.md) |
| [`confidence`](#confidence) | *int* |
| [`characterResults`](#characterresults) | [`DLRCharacterResult[]`](dlr-character-result.md) |


### lineSpecificationName
The name of the line specification used to recognize current line result.

```java
String com.dynamsoft.dlr.DLRLineResult.lineSpecificationName
```

### text
The recognized text, ends by '\0'.

```java
String com.dynamsoft.dlr.DLRLineResult.text
```

### characterModelName
The character model used to recognize the text.

```java
String com.dynamsoft.dlr.DLRLineResult.characterModelName
```

### location
The location of current line.

```java
DLRQuadrilateral com.dynamsoft.dlr.DLRLineResult.location
```


### confidence
The confidence of the result. It ranges from 0 to 100.

```java
int com.dynamsoft.dlr.DLRLineResult.confidence
```

### characterResults
The character results array.

```java
DLRCharacterResult[] com.dynamsoft.dlr.DLRLineResult.characterResults
```

