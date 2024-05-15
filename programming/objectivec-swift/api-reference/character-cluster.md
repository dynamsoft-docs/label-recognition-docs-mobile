---
layout: default-layout
title: DSCharacterCluster - Dynamsoft Label Recognizer iOS Edition
description: The class DSCharacterCluster of Dynamsoft Label Recognizer iOS edition represents the clustered characters.
keywords: Character cluster
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSCharacterCluster
---

# CharacterCluster

The `DSCharacterCluster` class represents the character clustering result. Each `DSCharacterCluster` object records the character info with its mean value.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCharacterCluster : NSObject
```
2. 
```swift
class CharacterCluster: NSObject
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`character`](#character) | *NSString \** | The string that represents the character. |
| [`mean`](#mean) | *DSBufferedCharacterItem \** | The mean value of the character cluster, of type `BufferedCharacterItem`. |

### character

The string that represents the character.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) NSString * character;
```
2. 
```swift
var character: String { get }
```

### mean

The mean value of the character cluster, of type `BufferedCharacterItem`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) DSBufferedCharacterItem * mean;
```
2. 
```swift
var mean: BufferedCharacterItem { get }
```
