---
layout: default-layout
title: Dynamsoft Core Android Class - ImageData
description: This page shows the ImageData Class of Dynamsoft Core for Android Language.
keywords: ImageData, android
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/android/api-reference/image-data-v2.0.html
---


# ImageData

> You are viewing a history document page of Dynamsoft Label Recognizer Android v2.2.20.

Stores the image data.  

```java
class com.dynamsoft.core.ImageData
```

## Attributes

| Attribute | Type |
|---------- | ---- |
| [`bytes`](#bytes) | *byte[]* |
| [`width`](#width) | *int* |
| [`height`](#height) | *int* |
| [`stride`](#stride) | *int* |
| [`format`](#format) | [`EnumImagePixelFormat`]({{ site.enumerations }}image-pixel-format.html) |

&nbsp;

### bytes

The image data content in a byte array.

```java
byte[] bytes
```

&nbsp;

### width

The width of the image in pixels.

```java
int width
```

&nbsp;

### height

The height of the image in pixels.

```java
int height
```

&nbsp;

### stride

The stride (or scan width) of the image.

```java
int stride
```

&nbsp;

### format

The image pixel format used in the image byte array.

```java
ImagePixelFormat format
```
