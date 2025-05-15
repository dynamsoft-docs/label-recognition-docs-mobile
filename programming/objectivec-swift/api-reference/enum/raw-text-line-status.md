---
layout: default-layout
title: RawTextLineStatus - Dynamsoft LabelRecognizer Enumerations
description: The enumeration RawTextLineStatus of Dynamsoft LabelRecognizer describes the final status of a raw text line.
keywords: Raw Text Line Status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RawTextLineStatus
codeAutoHeight: true
---

# Enumeration RawTextLineStatus

`RawTextLineStatus` enumerates the final status of a raw text line.

<div class="sample-code-prefix template2"></div>
   >- Objective-C
   >- Swift
   >
>
```objc
typedef NS_ENUM(NSInteger, DSRawTextLineStatus)
{
    /** Localized but recognition not performed. */
    DSRawTextLineStatusLocalized,
    /** Recognition failed. */
    DSRawTextLineStatusRecognitionFailed, 
    /** Successfully recognized. */
    DSRawTextLineStatusRecognitionSucceeded
}NS_SWIFT_NAME(RawTextLineStatus);
```
>
```swift
enum RawTextLineStatus: Int {
    /** Localized but recognition not performed. */
    case localized
    /** Recognition failed. */
    case recognitionFailed
    /** Successfully recognized. */
    case recognitionSucceeded
}
```
