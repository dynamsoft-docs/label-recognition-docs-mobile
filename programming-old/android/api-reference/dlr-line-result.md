---
layout: default-layout
title: DLRLineResult - Dynamsoft Label Recognizer Android Class
description: This page shows the DLRLineResult struct of Dynamsoft Label Recognizer for Android Language.
keywords: DLRLineResult, struct, android
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/android/api-reference/dlr-line-result.html
---


# DLRLineResult

> You are viewing a history document page of Dynamsoft Label Recognizer Android v2.2.20.

Stores the line result.
  
```java
class com.dynamsoft.dlr.DLRLineResult
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`lineSpecificationName`](#linespecificationname) | *String* |
| [`text`](#text) | *String* |
| [`characterModelName`](#charactermodelname) | *String* |
| [`location`](#location) | [`Quadrilateral`](quadrilateral.md) |
| [`confidence`](#confidence) | *int* |
| [`characterResults`](#characterresults) | [`DLRCharacterResult[]`](dlr-character-result.md) |

&nbsp;

### lineSpecificationName

The name of the line specification used to recognize current line result.

```java
String lineSpecificationName
```

&nbsp;

### text

The recognized text, ends by '\0'.

```java
String text
```

&nbsp;

### characterModelName

The character model used to recognize the text.

```java
String characterModelName
```

&nbsp;

### location

The location of current line.

```java
com.dynamsoft.core.Quadrilateral location
```

&nbsp;

### confidence

The confidence of the result. It ranges from 0 to 100.

```java
int confidence
```

&nbsp;

### characterResults

The character results array.

```java
DLRCharacterResult[] characterResults
```
