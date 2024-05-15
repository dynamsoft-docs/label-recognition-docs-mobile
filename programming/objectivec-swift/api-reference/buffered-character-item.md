---
layout: default-layout
title: DSBufferedCharacterItem - Dynamsoft Label Recognizer iOS Edition
description: The class DSBufferedCharacterItem of Dynamsoft Label Recognizer iOS edition represents a buffered character.
keywords: Buffered Character Item Set
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: DSBufferedCharacterItem
---

# BufferedCharacterItem

The `DSBufferedCharacterItem` class represents a buffered character.

## Definition

*Assembly:* DynamsoftLabelRecognizer.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSBufferedCharacterItem : NSObject
```
2. 
```swift
class BufferedCharacterItem: NSObject
```

## Properties

| Property | Type | Description |
| -------- | ---- | ----------- |
| [`character`](#character) | *NSString \** | The string that represents the character. |
| [`image`](#image) | *DSImageData \** | The image data of the buffered character. |
| [`features`](#features) | *NSDictionary<NSNumber \*, NSNumber \*> \** | A `NSDictionary` that represents all buffered character features. The values of the dictionary are float type. |

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

### image

The image data of the buffered character.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) DSImageData * image;
```
2. 
```swift
var image: ImageData { get }
```

### features

A `NSDictionary` that represents all buffered character features. The values of the dictionary are float type.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, readonly) NSDictionary<NSNumber *, NSNumber *> * features;
```
2. 
```swift
var features: [NSNumber: NSNumber] { get }
```
