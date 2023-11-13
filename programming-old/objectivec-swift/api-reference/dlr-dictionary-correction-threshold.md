---
layout: default-layout
title: iDLRDictionaryCorrectionThreshold - Dynamsoft Label Recognizer iOS Class
description: This page shows the iDLRDictionaryCorrectionThreshold struct of Dynamsoft Label Recognizer for iOS SDK.
keywords: iDLRDictionaryCorrectionThreshold, objective-c, oc, swift
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
permalink: /programming/objectivec-swift/api-reference/dlr-dictionary-correction-threshold.html
---


# iDLRDictionaryCorrectionThreshold

> You are viewing a history document page of Dynamsoft Label Recognizer iOS v2.2.20.

Stores the dictionary correction threshold.

```objc
@interface iDLRDictionaryCorrectionThreshold : NSObject 
```

## Attributes
  
| Attribute | Type |
|---------- | ---- |
| [`minWordLength`](#minwordlength) | *NSInteger* |
| [`maxWordLength`](#maxwordlength) | *NSInteger* |
| [`threshold`](#threshold) | *NSInteger* |

&nbsp;

### minWordLength

The minimum value of word length.

```objc
NSInteger minWordLength
```

&nbsp;

### maxWordLength

The maximum value of word length.

```objc
NSInteger maxWordLength
```

&nbsp;

### threshold

The threshold for the number of error correction characters.

```objc
NSInteger threshold
```
