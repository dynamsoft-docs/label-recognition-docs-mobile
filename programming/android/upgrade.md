---
layout: default-layout
title: How to upgrade - Dynamsoft Label Recognizer for Android
description: Follow the upgrade instructions to learn to upgrade Label Recognizer SDK Android edition from version 2.x to version 3.x with simple steps.
keywords: updates guide, android
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /programming/android/upgrade.html
---

# How to Upgrade

## From Version 2.x to 3.x

Dynamsoft Label Recognizer SDK has been refactored to integrate with [`DynamsoftCaptureVision (DCV)`]({{ site.dcv_introduction }}){:target="_blank"} architecture. To upgrade from version 2.x or earlier to 3.x, we recommend you to follow the [User Guide](user-guide.md) and re-write your codes.

### Update the Libraries to 3.x Version

The Dynamsoft Label Recognizer SDK has been split into multiple libraries from the previous single library, and the dependency configuration in the `app\build.gradle` file needs to be updated accordingly.

- Local Dependency
    Put the following `aar` files into `libs` directory and update `app\build.gradle` file:

  - `DynamsoftCaptureVisionRouter.aar`
  - `DynamsoftLabelRecognizer.aar`
  - `DynamsoftImageProcessing.aar`
  - `DynamsoftCore.aar`
  - `DynamsoftLicense.aar`
  - `DynamsoftCameraEnhancer.aar`(optional)
  - `DynamsoftUtility.aar`(optional)

    ```groovy
    dependencies {
        implementation fileTree(include: ['*.aar'], dir: 'libs')   
    }
    ```

- Remote Dependency(Maven)
  update `app\build.gradle` file:

    ```groovy
    dependencies {
        implementation 'com.dynamsoft:dynamsoftcapturevisionrouter:{version-number}'
        implementation 'com.dynamsoft:dynamsoftlabelrecognizer:{version-number}'
        implementation 'com.dynamsoft:dynamsoftcameraenhancer:{version-number}'
        implementation 'com.dynamsoft:dynamsoftimageprocessing:{version-number}'
        implementation 'com.dynamsoft:dynamsoftcore:{version-number}'
        implementation 'com.dynamsoft:dynamsoftlicense:{version-number}'
        implementation 'com.dynamsoft:dynamsoftutility:{version-number}'
    }
    ```

    >Note: Please view [user guide](user-guide.md#add-the-libraries-via-maven) for the correct version number.

### Update the License Activation Code

- Java code in 2.x:

```java
LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", this, new LicenseVerificationListener() {
    @Override
    public void licenseVerificationCallback(boolean isSuccess, CoreException error) {
        if (!isSuccess) {
            error.printStackTrace();
        }
    }
});
```

- Java code in 3.x:

```java
LicenseManager.initLicense("Put your license", this, new LicenseVerificationListener() {
    @Override
    public void onLicenseVerified(boolean isSuccess, Exception error) {
        if(!isSuccess){
            error.printStackTrace();
        }
    }
});
```

### Update Single Image Recognizing APIs

The APIs for recognizing text from single image has been adjusted as follows:

| Old APIs | New APIs |
| :----------- | :------- |
| `LabelRecognizer.recognizeFile` | `CaptureVisionRouter.capture(String filePath, String templateName)` |
| `LabelRecognizer.recognizeFileInMemory` | `CaptureVisionRouter.capture(byte[] fileBytes, String templateName)` |
| `LabelRecognizer.recognizeBuffer` | `CaptureVisionRouter.capture(ImageData imageData, String templateName)` |
| `LabelRecognizer.recognizeImage` | `CaptureVisionRouter.capture(Bitmap bitmap, String templateName)` |
| `class DLRResult` | `class CapturedResult/class RecognizedTextLinesResult` |

### Update Video Streaming Recognizing APIs

The APIs for recognizing video frames has been adjusted as follows:

| Old APIs | New APIs |
| :----------- | :------- |
| `LabelRecognizer.setImageSource` | `CaptureVisionRouter.setInput` |
| `LabelRecognizer.startScanning` | `CaptureVisionRouter.startCapturing` |
| `LabelRecognizer.stopScanning` | `CaptureVisionRouter.stopCapturing` |
| `LabelRecognizer.setLabelResultListener` | `CaptureVisionRouter.addResultReceiver` |
| `interface ImageSource` | `interface ImageSourceAdapter` |
| `interface LabelResultListener` | `interface CapturedResultReceiver` |
| `class DLRLineResult` | `class TextLineResultItem` |

### Migrate Your Templates

The template system is upgraded. The template you used for the previous version can't be directly recognized by the new version. Please <a href="mailto:support@dynamsoft.com">contact us</a> to upgrade your template.

The template-based APIs have been updated as follows:

| Old APIs | New APIs |
| :----------- | :------- |
| `LabelRecognizer.initRuntimeSettingsFromFile` | `CaptureVisionRouter.initSettingsFromFile` |
| `LabelRecognizer.initRuntimeSettings` | `CaptureVisionRouter.initSettings` |
| `LabelRecognizer.outputRuntimeSettingsToFile` | `CaptureVisionRouter.outputSettingsToFile` |
| `LabelRecognizer.outputRuntimeSettings` | `CaptureVisionRouter.outputSettings` |
| `LabelRecognizer.resetRuntimeSettings` | `CaptureVisionRouter.resetSettings` |

### Migrate Your DLRRuntimeSettings

The class `DLRRuntimeSettings` has been refactored. It retains commonly used properties while removing the previously complex property settings, which are now exclusively supported through templates.

The APIs for accessing and updating `DLRRuntimeSettings` has been adjusted as follows:

| Old APIs | New APIs |
| :----------- | :------- |
| `LabelRecognizer.getRuntimeSettings` | `CaptureVisionRouter.getSimplifiedSettings` |
| `LabelRecognizer.updateRuntimeSettings` | `CaptureVisionRouter.updateSettings` |

#### Migrate to SimplifiedCaptureVisionSettings

The following properties are replaced by similar properties under `SimplifiedCaptureVisionSettings`. They can also be set via a template file(String).

| PublicRuntimeSettings Property | SimplifiedCaptureVisionSettings Property | Template File Parameter |
| ------------------------------- | ----------------------------------------- | ----------------------- |
| `textArea` | [`roi`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html#roi) & [`roiMeasuredInPercentage`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html#roimeasuredinpercentage) | [`TargetROIDef.Location.Offset`]({{ site.dcv_parameters_reference }}target-roi-def/location.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `timeout` | [`timeout`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html#timeout) | [`CaptureVisionTemplates.Timeout`]({{ site.dcv_parameters_reference }}capture-vision-template/timeout.html?lproduct=dlr&repoType=core){:target="_blank"} |

#### Migrate to SimplifiedLabelRecognizerSettings

The following properties are replaced by similar properties under `SimplifiedLabelRecognizerSettings`. The majority of them can also be set via a template file(String).

| PublicRuntimeSettings Property | SimplifiedLabelRecognizerSettings Property | Template File Parameter |
| ------------------------------- | ----------------------------------------- | ----------------------- |
| `characterModelName` | [`characterModelName`]({{ site.dlr_android_api }}simplified-label-recognizer-settings.html#charactermodelname) | [`LabelRecognizerTaskSetting.CharacterModelName`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/character-model-name.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `maxThreadCount` | [`maxThreadsInOneTask`]({{ site.dlr_android_api }}simplified-label-recognizer-settings.html#maxthreadsinonetask) | [`LabelRecognizerTaskSetting.MaxThreadsInOneTask`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/max-threads-in-one-task.html?lproduct=dlr&repoType=core){:target="_blank"} |

| FurtherModes Property | SimplifiedLabelRecognizerSettings Property | Template File Parameter |
| ---------------------- | ----------------------------------------- | ----------------------- |
| `grayscaleTransformationModes` | [`grayscaleTransformationModes`]({{ site.dlr_android_api }}simplified-label-recognizer-settings.html#grayscaletransformationmodes) | [`ImageParameter.GrayscaleTransformationModes`]({{ site.dcv_parameters_reference }}image-parameter/grayscale-enhancement-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `grayscaleEnhancementModes` | [`grayscaleEnhancementModes`]({{ site.dlr_android_api }}simplified-label-recognizer-settings.html#grayscaleenhancementmodes) | [`ImageParameter.GrayscaleEnhancementModes`]({{ site.dcv_parameters_reference }}image-parameter/grayscale-transformation-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |

#### Migrate to Template File

The following properties can only be set via a template file. Please [contact us](https://www.dynamsoft.com/company/customer-service/#contact){:target="_blank"} so that we can help you to transform your current settings to a new template file.

| PublicRuntimeSettings Property | Template File Parameter |
| ------------------------------- | ----------------------- |
| `binarizationModes` | [`ImageParameter.BinarizationModes`]({{ site.dcv_parameters_reference }}image-parameter/binarization-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `dictionaryPath` | [`LabelRecognizerTaskSettings.DictionaryPath`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/dictionary-path.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `dictionaryCorrectionThreshold` | [`LabelRecognizerTaskSettings.DictionaryCorrectionThreshold`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/dictionary-correction-thresholds.html?lproduct=dlr&repoType=core){:target="_blank"} |

| PublicRuntimeSettings.furtherModes Property | Template File Parameter |
| ---------------------- | ----------------------- |
| `colourConversionModes` | [`ImageParameter.ColourConversionModes`]({{ site.dcv_parameters_reference }}image-parameter/colour-conversion-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `regionPredetectionModes` | [`ImageParameter.RegionPredetectionModes`]({{ site.dcv_parameters_reference }}image-parameter/region-predetection-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `textureDetectionModes` | [`ImageParameter.TextureDetectionModes`]({{ site.dcv_parameters_reference }}image-parameter/texture-detection-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
