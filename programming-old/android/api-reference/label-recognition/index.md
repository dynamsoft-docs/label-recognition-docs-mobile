---
layout: default-layout
title: LabelRecognition Class - Dynamsoft Label Recognition Android API Reference
description: This page shows LabelRecognition methods of Dynamsoft Label Recognition for Android API Reference.
keywords: api reference, android
needAutoGenerateSidebar: false
permalink: /programming/android/api-reference/label-recognition/index.html
---


# Dynamsoft Label Recognition - CLabelRecognition Class

> You are viewing a history document page of Dynamsoft Label Recognizer Android v1.x.

## General
   
  | Method               | Description |
  |----------------------|-------------|
  | [`getVersion`](general.md#getversion) | Returns the version number string for the SDK. |
   
&nbsp; 

## Initialization
  
  | Method               | Description |
  |----------------------|-------------|
  | [`LabelRecognition`](initialization.md#labelrecognition) | Initialization of `LabelRecognition` object.|
  | [`destroy`](initialization.md#destroy) | Destroys an instance of `LabelRecognition` object.|   
  | [`initLicense`](initialization.md#initlicense) | Sets the license and activates the SDK. |
  | [`initLicenseFromLTS`](initialization.md#initlicensefromlts) | Initializes the label recognition license and connects to the specified server for online verification. |

&nbsp; 

## Setting

  | Method               | Description |
  |----------------------|-------------|
  | [`getRuntimeSettings`](settings.md#getruntimesettings) | Gets the current settings and saves it into a struct. |
  | [`updateRuntimeSettings`](settings.md#updateruntimesettings) | Updates runtime settings with a given struct. |
  | [`resetRuntimeSettings`](settings.md#resetruntimesettings) | Resets the runtime settings. |
  | [`appendSettingsFromString`](settings.md#appendsettingsfromstring) | Appends LabelRecognitionParameter settings in a string to the SDK object. |
  | [`appendSettingsFromFile`](settings.md#appendsettingsfromFile) | Appends LabelRecognitionParameter settings from a file to the SDK object. |
  | [`outputSettingsToFile`](settings.md#outputsettingstofile) | Outputs LabelRecognitionParameter settings into a file (JSON file). |
  | [`clearAppendedSettings`](settings.md#clearappendedsettings) | Clear all appended LabelRecognitionParameter settings in the SDK object. |
  | [`updateReferenceRegionFromBarcodeResults`](settings.md#updatereferenceregionfrombarcoderesults) | Updates reference region which is defined with source type DLR_LST_BARCODE. |
  | [`getModeArgument`](settings.md#getmodeargument) | Get argument value for the specified mode parameter. |
  | [`setModeArgument`](settings.md#setmodeargument) | Set argument value for the specified mode parameter. |
  | [`appendCharacterModelBuffer`](settings.md#appendcharactermodelbuffer) | Appends CharacterModel to the SDK object. |
  | [`eraseAllCharacterModels`](settings.md#appendcharactermodelbuffer) | Erases all CharacterModels the SDK object currently loaded. |
  | [`eraseCharacterModelByName`](settings.md#appendcharactermodelbuffer) | Erases a name specified CharacterModel from the SDK object. |

&nbsp; 
   
## Recognizing
   
  | Method               | Description |
  |----------------------|-------------|
  | [`recognizeByBuffer`](recognizing.md#recognizebybuffer) | Recognizes text from memory buffer containing image pixels in defined format. |
  | [`recognizeByFile`](recognizing.md#recognizebyfile) | Recognizes text from a specified image file. |
   
&nbsp; 
   