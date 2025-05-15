---
layout: default-layout
title: DSLabelRecognizerModule - Dynamsoft Label Recognizer iOS Edition
description: The DSLabelRecognizerModule class of Dynamsoft Label Recognizer iOS edition defines general functions in the label recognizer module.
keywords: label recognizer module, iOS
needAutoGenerateSidebar: true
needGenerateH3Content: true
breadcrumbText: DSLabelRecognizerModule
permalink: /programming/objectivec-swift/api-reference/label-recognizer-module.html
---

# DSLabelRecognizerModule

The `DSLabelRecognizerModule` class defines general functions in the label recognizer module.

## Definition

*Assembly:* DynamsoftCaptureVisionBundle.xcframework

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface DSLabelRecognizerModule : NSObject
```
2. 
```swift
class LabelRecognizerModule: NSObject
```

## Methods

| Method | Description |
| ------ | ----------- |
| [getVersion](#getversion) | Get the version of the label recognizer module. |

### getVersion

Get the version of the label recognizer module.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
+ (NSString *)getVersion;
```
2. 
```swift
class func getVersion() -> String
```

**Return Value**

Returns a string representing the version of the label recognizer module.
