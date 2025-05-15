---
layout: default-layout
title: DSCharacterResult - Dynamsoft Label Recognizer iOS Edition
description: The class DSCharacterResult of Dynamsoft Label Recognizer iOS edition represents the result of a character recognition process.
keywords: Character result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSCharacterResult
permalink: /programming/objectivec-swift/api-reference/character-result.html
---

# DSCharacterResult

The `DSCharacterResult` class represents the result of a character recognition process. It contains the characters recognized (high, medium, and low confidence), their respective confidences, and the location of the character in a quadrilateral shape.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSCharacterResult : NSObject
```
2. 
```swift
class CharacterResult: NSObject
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`characterH`](#characterh) | *unichar* | The character with high confidence. |
| [`characterM`](#characterm) | *unichar* | The character with medium confidence. |
| [`characterL`](#characterl) | *unichar* | The character with low confidence. |
| [`location`](#location) | *DSQuadrilateral \** | The location of the character in a quadrilateral shape. |
| [`characterHConfidence`](#characterhconfidence) | *NSInteger* | The confidence of the character with high confidence. |
| [`characterMConfidence`](#charactermconfidence) | *NSInteger* | The confidence of the character with medium confidence. |
| [`characterLConfidence`](#characterlconfidence) | *NSInteger* | The confidence of the character with low confidence. |

### characterH

The character with high confidence.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) unichar characterH;
```
2. 
```swift
var characterH: unichar { get }
```

### characterM

The character with medium confidence.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) unichar characterM;
```
2. 
```swift
var characterM: unichar { get }
```

### characterL

The character with low confidence.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) unichar characterL;
```
2. 
```swift
var characterL: unichar { get }
```

### location

The location of the character in a quadrilateral shape.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, nullable, readonly) DSQuadrilateral * location;
```
2. 
```swift
var location: Quadrilateral? { get }
```

### characterHConfidence

The confidence of the character with high confidence.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) NSInteger characterHConfidence;
```
2. 
```swift
var characterHConfidence: Int { get }
```

### characterMConfidence

The confidence of the character with medium confidence.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) NSInteger characterMConfidence;
```
2. 
```swift
var characterMConfidence: Int { get }
```

### characterLConfidence

The confidence of the character with low confidence.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign, readonly) NSInteger characterLConfidence;
```
2. 
```swift
var characterLConfidence: Int { get }
```
