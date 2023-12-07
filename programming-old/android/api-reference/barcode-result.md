---
layout: default-layout
title: Dynamsoft Core Android Class - BarcodeResult
description: This page shows the BarcodeResult Class of Dynamsoft Core for Android Language.
keywords: BarcodeResult, Android
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/android/api-reference/barcode-result.html
---


# BarcodeResult

> You are viewing a history document page of Dynamsoft Label Recognizer Android v2.2.20.

Stores the barcode result.

```java
class com.dynamsoft.core.BarcodeResult
```
  
## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`barcodeFormat`](#barcodeformat) | *int* |
| [`barcodeFormat_2`](#barcodeformat_2) | *int* |
| [`text`](#text) | *String* |
| [`bytes`](#bytes) | *byte[]* |
| [`location`](#location) | [`Quadrilateral`](quadrilateral.md) |
| [`moduleSize`](#modulesize) | *int* |
| [`pageNumber`](#pagenumber) | *int* |

&nbsp;

### barcodeFormat

Barcode type in BarcodeFormat group 1.

```java
int barcodeFormat
```

**See also**

[`EnumBarcodeFormat`]({{ site.enumerations }}barcode-format.html)

&nbsp;

### barcodeFormat_2

Barcode type in BarcodeFormat group 2.

```java
int barcodeFormat_2
```

**See also**

[`EnumBarcodeFormat_2`]({{ site.enumerations }}barcode-format-2.html)

&nbsp;

### text

The barcode text.

```java
String text
```

&nbsp;

### bytes

The barcode content in a byte array.

```java
byte[] bytes
```

&nbsp;

### location

The location of current recognized text.

```java
Quadrilateral location
```

&nbsp;

### moduleSize

The barcode module size (the minimum bar width in pixel).

```java
int moduleSize
```

&nbsp;

### pageNumber

The page number the barcode located in. The index is 0-based.

```java
int pageNumber
```
