---
layout: default-layout
title: DLRResult - Dynamsoft Label Recognition Android Class
description: This page shows the DLRResult struct of Dynamsoft Label Recognition for Android Language.
keywords: DLRResult, struct, android
needAutoGenerateSidebar: true
permalink: /programming/android/api-reference/class/dlr-result-v1.0.html
---


# DLRResult
Stores the recognized result.

  

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`referenceRegionName`](#referenceregionname) | *String* |
| [`textAreaName`](#textareaname) | *String* |
| [`location`](#location) | [`DLRQuadrilateral`](dlr-quadrilateral.md) |
| [`confidence`](#confidence) | *int* |
| [`lineResults`](#lineresults) | [`DLRLineResult[]`](dlr-line-result.md) |


### referenceRegionName
The name of the reference region which is used to recognize the current result.

```java
String com.dynamsoft.dlr.DLRResult.referenceRegionName
```

### textAreaName
The name of the text area used to recognize current result.

```java
String com.dynamsoft.dlr.DLRResult.textAreaName
```

### location
The location of current recognized text.

```java
DLRQuadrilateral com.dynamsoft.dlr.DLRResult.location
```


### confidence
The confidence of the result. It ranges from 0 to 100.

```java
int com.dynamsoft.dlr.DLRResult.confidence
```


### lineResults
The line results array.

```java
DLRLineResult[] com.dynamsoft.dlr.DLRResult.lineResults
```

