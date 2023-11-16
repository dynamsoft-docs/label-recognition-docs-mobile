---
layout: default-layout
title: iDLRRuntimeSettings - Dynamsoft Label Recognition iOS Class
description: This page shows the iDLRRuntimeSettings class of Dynamsoft Label Recognition for iOS SDK.
keywords: iDLRRuntimeSettings, class, objective-c, oc, swift
needAutoGenerateSidebar: true
permalink: /programming/objectivec-swift/api-reference/class/dlr-runtime-settings.html
---


# iDLRRuntimeSettings

> You are viewing a history document page of Dynamsoft Label Recognizer iOS v1.x.

Defines a struct to configure the text recognizer runtime settings. These settings control the text recognition process.
  

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`maxThreadCount`](#maxthreadcount) | *NSInteger* |
| [`characterModelName`](#charactermodelname) | *NSString\** |
| [`linesCount`](#linescount) | *NSInteger* |
| [`regionPredetectionModes`](#regionpredetectionmodes) | *NSArray \** |
| [`referenceRegion`](#referenceregion) | [`iDLRReferenceRegion`](dlr-reference-region.md)\* |
| [`textArea`](#textarea) | [`iDLRQuadrilateral`](dlr-quadrilateral.md)\* |
| [`grayscaleTransformationModes`](#grayscaletransformationmodes) | *NSArray \** |


### maxThreadCount
Sets the number of threads the algorithm will use to recognize label.
```objc
NSInteger maxThreadCount
```

**Value Range**

[1, 4]

**Default value**

4

**Remarks**

To keep a balance between speed and quality, the library concurrently runs four different threads by default.

### characterModelName
The name of the CharacterModel.
```objc
NSString* characterModelName
```

### linesCount
Sets the text lines count of the text area.
```objc
NSInteger linesCount
```

**Value Range**

[0, 200]

**Default value**

0

**Remarks**

0: line count is not certain.


### regionPredetectionModes
Sets the region pre-detection mode.
```objc
NSArray * regionPredetectionModes
```

**Value Range**

Each array item can be any one of the [`EnumDLRRegionPredetectionMode`]({{ site.enumerations }}parameter-mode-enums.html#dlrregionpredetectionmode) Enumeration items.

**Default value**

`[EnumDLRRegionPredetectionModeSkip,EnumDLRRegionPredetectionModeSkip,EnumDLRRegionPredetectionModeSkip,EnumDLRRegionPredetectionModeSkip,EnumDLRRegionPredetectionModeSkip,EnumDLRRegionPredetectionModeSkip,EnumDLRRegionPredetectionModeSkip,EnumDLRRegionPredetectionModeSkip]`

**Remarks**

The array index represents the priority of the item. The smaller index is, the higher priority is.


### referenceRegion
Sets the reference region to search for text.
```objc
iDLRReferenceRegion* referenceRegion
```

### textArea
Sets the text area relative to the reference region.
```objc
iDLRQuadrilateral* textArea
```

### grayscaleTransformationModes
Sets the grayscale transformation mode.
```objc
NSArray * grayscaleTransformationModes
```

**Value Range**

Each array item can be any one of the [`EnumDLRGrayscaleTransformationMode`]({{ site.enumerations }}parameter-mode-enums.html#dlrgrayscaletransformationmode) Enumeration items.

**Default value**

`[EnumDLRGrayscaleTransformationModeOriginal,EnumDLRGrayscaleTransformationModeSkip,EnumDLRGrayscaleTransformationModeSkip,EnumDLRGrayscaleTransformationModeSkip,EnumDLRGrayscaleTransformationModeSkip,EnumDLRGrayscaleTransformationModeSkip,EnumDLRGrayscaleTransformationModeSkip,EnumDLRGrayscaleTransformationModeSkip]`

**Remarks**

The array index represents the priority of the item. The smaller index is, the higher priority is.
  

