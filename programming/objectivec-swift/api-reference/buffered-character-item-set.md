---
layout: default-layout
title: DSBufferedCharacterItemSet - Dynamsoft Label Recognizer iOS Edition
description: The class DSBufferedCharacterItemSet of Dynamsoft Label Recognizer iOS edition represents the buffered characters and the character clusters that generated from the buffered characters.
keywords: Buffered Character Item Set
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSBufferedCharacterItemSet
---

# DSBufferedCharacterItemSet

The `DSBufferedCharacterItemSet` class represents the buffered characters and the character cluster that generated from the buffered characters.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSBufferedCharacterItemSet : NSObject
```
2. 
```swift
class BufferedCharacterItemSet: NSObject
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`items`](#items) | *NSArray<DSBufferedCharacterItem \*> \** | An array of `BufferedCharacterItem` objects that represents the buffered characters. |
| [`characterClusters`](#characterclusters) | *NSArray<DSCharacterCluster \*> \** | An array of `CharacterCluster` objects that represents the clustered characters. |

### items

An array of `BufferedCharacterItem` objects that represents the buffered characters.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) NSArray<DSBufferedCharacterItem *> * items;
```
2. 
```swift
var items: [BufferedCharacterItem] { get }
```

### characterClusters

An array of `CharacterCluster` objects that represents the clustered characters.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) NSArray<DSCharacterCluster *> * characterClusters;
```
2. 
```swift
var characterClusters: [CharacterCluster] { get }
```
