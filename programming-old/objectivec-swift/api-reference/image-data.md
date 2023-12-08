---
layout: default-layout
title: Dynamsoft Core iOS Class - iImageData
description: This page shows the iImageData class of Dynamsoft Label Recognizer iOS Edition.
keywords: iImageData, objective-c, oc, swift
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/objectivec-swift/api-reference/image-data.html
ignore: true
---

# iImageData

> You are viewing a history document page of Dynamsoft Label Recognizer iOS v2.2.20.

Stores the image data.  

```objc
@interface iImageData : NSObject 
```

## Attributes

| Attribute | Type |
|---------- | ---- |
| [`bytes`](#bytes) | *NSData\** |
| [`width`](#width) | *NSInteger* |
| [`height`](#height) | *NSInteger* |
| [`stride`](#stride) | *NSInteger* |
| [`format`](#format) | [`EnumImagePixelFormat`]({{ site.enumerations }}image-pixel-format.html) |

&nbsp;

### bytes

The image data content in a byte array.

```objc
NSData* bytes
```

&nbsp;

### width

The width of the image in pixels.  

```objc
NSInteger width
```

&nbsp;

### height

The height of the image in pixels.  

```objc
NSInteger height
```

&nbsp;

### stride

The stride (or scan width) of the image.

```objc
NSInteger stride
```

&nbsp;

### format

The image pixel format used in the image byte array.

```objc
EnumImagePixelFormat format
```
