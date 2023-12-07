---
layout: default-layout
title: Recognizing - Dynamsoft Label Recognition iOS API Reference
description: This is the recognizing functions of Dynamsoft Label Recognition for iOS API Reference.
keywords: api reference, objective-c, oc, swift
needAutoGenerateSidebar: true
permalink: /programming/objectivec-swift/api-reference/methods/recognizing.html
---

# iOS API Reference - Recognizing

> You are viewing a history document page of Dynamsoft Label Recognizer iOS v1.x.

| Method               | Description |
|----------------------|-------------|
  | [`recognizeByBuffer`](#recognizebybuffer) | Recognizes text from memory buffer containing image pixels in defined format. |
  | [`recognizeByFile`](#recognizebyfile) | Recognizes text from a specified image file. |

---

## recognizeByBuffer
Recognizes text from the memory buffer containing image pixels in defined format.

```objc
- (NSArray<iDLRResult*>*)recognizeByBuffer:(iDLRImageData*)imageData templateName:(NSString*)templateName error:(NSError**)error
```   
   
**Parameters**
`[in]	imageData` An object of iDLRImageData that represents an image.  
`[in]	templateName` The template name. A template name is the value of key LabelRecognitionParameter.Name defined in JSON formatted settings. If no template name is specified, current runtime settings will be used.
`[in,out] error` Input a pointer to an error object. If an error occurs, this pointer is set to an actual error object containing the error information. You may specify nil for this parameter if you do not want the error information.

**Return Value**
All results recognized successfully.

**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
DynamsoftLabelRecognition *recognizer;
iDMLTSConnectionParameters* lts = [[iDMLTSConnectionParameters alloc] init];
lts.organizationID = @"200001";
lts.sessionPassword = @"******";
recognizer = [[DynamsoftLabelRecognition alloc] initLicenseFromLTS:lts verificationDelegate:self];
- (void)LTSLicenseVerificationCallback:(bool)isSuccess error:(NSError * )error
{
    //TODO add your code for license verification
}
iDLRResult *result;
iDLRImageData *imageData = [[iDLRImageData alloc] init];
//construct imageData
NSError __autoreleasing *  error;
result = [recognizer recognizeByBuffer:imageData templateName:@"" error:&error];
```
2. 
```swift
let lts = iDMLTSConnectionParameters()
lts.organizationID = "200001"
lts.sessionPassword = "******"
let recognizer = DynamsoftLabelRecognition(licenseFromLTS: lts, verificationDelegate: self)
let imageData = iDLRImageData.init()
let error: NSError? = NSError()
//construct imageData
let result = recognizer.recognizeByBuffer(imageData:imageData, templateName:"", error:&error)
```

&nbsp;


## recognizeByFile
Recognizes text from a specified image file.

```objc
- (NSArray<iDLRResult*>*)recognizeByFile:(NSString*)name templateName:(NSString*)templateName error:(NSError**)error
```   
   
**Parameters**
`name` A string defining the file name.  
`templateName` The template name. A template name is the value of key LabelRecognitionParameter.Name defined in JSON formatted settings. If no template name is specified, current runtime settings will be used.
`[in,out] error` Input a pointer to an error object. If an error occurs, this pointer is set to an actual error object containing the error information. You may specify nil for this parameter if you do not want the error information.

**Return Value**
All results recognized successfully.


**Code Snippet**

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
DynamsoftLabelRecognition *recognizer;
iDMLTSConnectionParameters* lts = [[iDMLTSConnectionParameters alloc] init];
lts.organizationID = @"200001";
lts.sessionPassword = @"******";
recognizer = [[DynamsoftLabelRecognition alloc] initLicenseFromLTS:lts verificationDelegate:self];
- (void)LTSLicenseVerificationCallback:(bool)isSuccess error:(NSError * )error
{
    //TODO add your code for license verification
}
iDLRResult *result;
NSError __autoreleasing *  error;
result = [recognizer recognizeByFile:@"your file path" templateName:@"" error:&error];
```
2. 
```swift
let lts = iDMLTSConnectionParameters()
lts.organizationID = "200001"
lts.sessionPassword = "******"
let recognizer = DynamsoftLabelRecognition(licenseFromLTS: lts, verificationDelegate: self)
let error: NSError? = NSError()
//construct imageData
let result = recognizer.recognizeByFile("your file path", templateName:"", error:&error)
```

&nbsp;


