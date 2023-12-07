---
layout: default-layout
title: Dynamsoft Core Android Interface - ImageSource
description: This page shows the ImageSource Interface of Dynamsoft Core for Android Language.
keywords: ImageSource, android
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/android/api-reference/image-source.html
---

# ImageSource

> You are viewing a history document page of Dynamsoft Label Recognizer Android v2.2.20.

Interface for producers of images. It can be implemented by programmers to support other image sources, such as external cameras or image filesets.

```java
inteface com.dynamsoft.core.ImageSource
```  

## Methods

| Methods | Type |
| [`getImage`](#getimage) | Convert `ImageData` to `android.graphics.Bitmap`. |

### getImage

Gets an image from an instance of subclass of `ImageSource`.

```java
ImageData getImage()
```
