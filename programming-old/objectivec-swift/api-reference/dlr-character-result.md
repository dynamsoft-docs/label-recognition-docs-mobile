---
layout: default-layout
title: iDLRCharacterResult - Dynamsoft Label Recognizer iOS Class
description: This page shows the DLRCharacterResult class of Dynamsoft Label Recognizer for iOS SDK.
keywords: iDLRCharacterResult, objective-c, oc, swift
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/objectivec-swift/api-reference/dlr-character-result.html
---

# iDLRCharacterResult

> You are viewing a history document page of Dynamsoft Label Recognizer iOS v2.2.20.

Stores the character result.
  
```objc
@interface iDLRCharacterResult : NSObject 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`characterH`](#characterh) | *NSString \** |
| [`characterM`](#characterm) | *NSString \** |
| [`characterL`](#characterl) | *NSString \** |
| [`characterHConfidence`](#characterhconfidence) | *NSInteger* |
| [`characterMConfidence`](#charactermconfidence) | *NSInteger* |
| [`characterLConfidence`](#characterlconfidence) | *NSInteger* |
| [`location`](#location) | [`iQuadrilateral`](quadrilateral.md)\* |

&nbsp;

### characterH

The recognized character with highest confidence.

```objc
NSString* characterH
```

&nbsp;

### characterM

The recognized character with middle confidence.

```objc
NSString* characterM
```

&nbsp;

### characterL

The recognized character with lowest confidence.

```objc
NSString* characterL
```

&nbsp;

### characterHConfidence

The confidence of the recognized character with the highest confidence.

```objc
NSInteger characterHConfidence
```

&nbsp;

### characterMConfidence

The confidence of the recognized character with the middle confidence.

```objc
NSInteger characterMConfidence
```

&nbsp;

### characterLConfidence

The confidence of the recognized character with the lowest confidence.

```objc
NSInteger characterLConfidence
```

&nbsp;

### location

The location of current character.

```objc
iQuadrilateral* location
```
