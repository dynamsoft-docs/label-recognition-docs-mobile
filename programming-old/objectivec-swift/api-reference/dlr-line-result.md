---
layout: default-layout
title: iDLRLineResult - Dynamsoft Label Recognizer iOS Class
description: This page shows the iDLRLineResult class of Dynamsoft Label Recognizer for iOS SDK.
keywords: iDLRLineResult, class, objective-c, oc, swift
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/objectivec-swift/api-reference/dlr-line-result.html
---


# iDLRLineResult

> You are viewing a history document page of Dynamsoft Label Recognizer iOS v2.2.20.

Stores the line result.
  
```objc
@interface iDLRLineResult : NSObject 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`lineSpecificationName`](#linespecificationname) | *NSString\** |
| [`text`](#text) | *NSString\** |
| [`characterModelName`](#charactermodelname) | *NSString\** |
| [`location`](#location) | [`Quadrilateral`](quadrilateral.md)\* |
| [`confidence`](#confidence) | *NSInteger* |
| [`characterResults`](#characterresults) | NSArray<[`iDLRCharacterResult`](dlr-character-result.md)\*>\*|

&nbsp;

### lineSpecificationName

The name of the line specification used to recognize current line result.

```objc
NSString* lineSpecificationName
```

&nbsp;

### text

The recognized text, ends by '\0'.

```objc
NSString* text
```

&nbsp;

### characterModelName

The character model used to recognize the text.

```objc
NSString* characterModelName
```

&nbsp;

### location

The location of current line.

```objc
iQuadrilateral* location
```

&nbsp;

### confidence

The confidence of the result. It ranges from 0 to 100.

```objc
NSInteger confidence
```

&nbsp;

### characterResults

The character results array.

```objc
NSArray<iDLRCharacterResult*>* characterResults
```
