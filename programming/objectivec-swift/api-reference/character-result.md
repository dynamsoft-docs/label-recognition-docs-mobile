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

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

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

## Properties & Methods

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`characterH`](#characterh) | *unichar* | The character with high confidence. |
| [`characterM`](#characterm) | *unichar* | The character with medium confidence. |
| [`characterL`](#characterl) | *unichar* | The character with low confidence. |
| [`location`](#location) | *DSQuadrilateral \** | The location of the character in a quadrilateral shape. |
| [`characterHConfidence`](#characterhconfidence) | *NSInteger* | The confidence of the character with high confidence. |
| [`characterMConfidence`](#charactermconfidence) | *NSInteger* | The confidence of the character with medium confidence. |
| [`characterLConfidence`](#characterlconfidence) | *NSInteger* | The confidence of the character with low confidence. |

| Methods | Description |
| ------- | ----------- |
| [`init`](#init) | Initializes a new instance of the `DSCharacterResult` class. |
| [`initWithCharacterH`](#initwithcharacterh) | Initializes a new instance of the `DSCharacterResult` class. |

### characterH

The character with high confidence.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, assign) unichar characterH;
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
@property (nonatomic, assign) unichar characterM;
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
@property (nonatomic, assign) unichar characterL;
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
@property (nonatomic, nullable) DSQuadrilateral * location;
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
@property (nonatomic, assign) NSInteger characterHConfidence;
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
@property (nonatomic, assign) NSInteger characterMConfidence;
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
@property (nonatomic, assign) NSInteger characterLConfidence;
```
2. 
```swift
var characterLConfidence: Int { get }
```

### init

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)init;
```
2. 
```swift
init()
```

### initWithCharacterH

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (instancetype)initWithCharacterH:(unichar)characterH
                        characterM:(unichar)characterM
                        characterL:(unichar)characterL
              characterHConfidence:(DSQuadrilateral *)characterHConfidence
              characterMConfidence:(NSInteger)characterMConfidence
              characterLConfidence:(NSInteger)characterLConfidence
                          location:(NSInteger)location;
```
2. 
```swift
init(characterH: unichar, characterM: unichar, characterL: unichar, characterHConfidence: Int, characterMConfidence: Int, characterLConfidence: Int, location: Int)
```
