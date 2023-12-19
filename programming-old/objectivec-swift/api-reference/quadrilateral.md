---
layout: default-layout
title: Dynamsoft Core iOS Class - iQuadrilateral
description: This page shows the iQuadrilateral class of Dynamsoft Label Recognizer iOS Edition v1.x.
keywords: iQuadrilateral, class, objective-c, oc, swift
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/objectivec-swift/api-reference/quadrilateral.html
---

# iQuadrilateral

> You are viewing a history document page of Dynamsoft Label Recognizer iOS v2.2.20.

Stores the quadrilateral.  

```objc
@interface iQuadrilateral : NSObject 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`points`](#points) | *NSArray\** |

&nbsp;

### points

Four vertexes (CGPoint) in a clockwise direction of a quadrilateral. Index 0 represents the left-most vertex.

```objc
NSArray* points
```
