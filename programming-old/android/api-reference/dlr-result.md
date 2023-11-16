---
layout: default-layout
title: DLRResult - Dynamsoft Label Recognizer Android Class
description: This page shows the DLRResult struct of Dynamsoft Label Recognizer for Android Language.
keywords: DLRResult, struct, android
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/android/api-reference/dlr-result.html
---


# DLRResult

> You are viewing a history document page of Dynamsoft Label Recognizer Android v2.2.20.

Stores the recognized result.

```java
class com.dynamsoft.dlr.DLRResult
```  

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`referenceRegionName`](#referenceregionname) | *String* |
| [`textAreaName`](#textareaname) | *String* |
| [`location`](#location) | [`Quadrilateral`](quadrilateral.md) |
| [`confidence`](#confidence) | *int* |
| [`lineResults`](#lineresults) | [`DLRLineResult[]`](dlr-line-result.md) |
| [`pageNumber`](#pagenumber) | *int* |

&nbsp;

### referenceRegionName

The name of the reference region which is used to recognize the current result.

```java
String referenceRegionName
```

&nbsp;

### textAreaName

The name of the text area used to recognize current result.

```java
String textAreaName
```

&nbsp;

### location

The location of current recognized text.

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

### lineResults

The line results array.

```java
DLRLineResult[] lineResults
```

&nbsp;

### pageNumber

The page number the result located in. The index is 0-based.

```java
int pageNumber
```
