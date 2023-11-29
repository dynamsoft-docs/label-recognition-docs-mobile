---
layout: default-layout
title: How to upgrade - Dynamsoft Label Recognizer for iOS
description: Follow the upgrade instructions to learn to upgrade Label Recognizer SDK iOS edition from version 2.x to version 3.x with simple steps.
keywords: updates guide, iOS
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /programming/objectivec-swift/upgrade.html
---

# How to Upgrade

## From Version 2.x to 3.x

Dynamsoft Label Recognizer SDK has been refactored to integrate with [`DynamsoftCaptureVision (DCV)`]({{ site.dcv_introduction }}) architecture. To upgrade from version 2.x or earlier to 3.x, we recommend you to follow the [User Guide](user-guide.md) and re-write your codes.

### Update the Libraries to 3.x Version

The Dynamsoft Label Recognizer SDK has been split into multiple libraries from the previous single library.

- Local Dependency
    You have to drag and drop the following xcframeworks into your Xcode project to use Dynamsoft Label Recognizer.

  - `DynamsoftCaptureVisionRouter.xcframework`
  - `DynamsoftLabelRecognizer.xcframework`
  - `DynamsoftImageProcessing.xcframework`
  - `DynamsoftCore.xcframework`
  - `DynamsoftLicense.xcframework`
  - `DynamsoftCameraEnhancer.xcframework`(optional)

- Remote Dependency(CocoaPods)
  update **Podfile**:

    ```pod
    target '{Your project name}' do
    use_frameworks!

    pod 'DynamsoftLabelRecognizer','3.0.20'
    pod 'DynamsoftCaptureVisionRouter','2.0.21'
    pod 'DynamsoftCameraEnhancer','4.0.1'

    end
    ```

    >Note: Please view [user guide](user-guide.md#add-the-xcframeworks-via-cocoapods) for the correct version number.

### Update the License Activation Code

- License activation code in 2.x:

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@interface AppDelegate ()<LicenseVerificationListener>
...
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
   ...
   [DynamsoftLicenseManager initLicense:@"Put Your License Here" verificationDelegate:self];
}
- (void)licenseVerificationCallback:(bool)isSuccess error:(NSError *)error {
   // Add code to execute when license verification is approved or failed.
}
```
2. 
```swift
class AppDelegate: UIResponder, UIApplicationDelegate, LicenseVerificationListener {
   func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
          DynamsoftLicenseManager.initLicense("Put Your License Here",verificationDelegate:self)
   }
   func licenseVerificationCallback(_ isSuccess: Bool, error: Error?) {
          // Add code to execute when license verification is approved or failed.
   }
}
```

- License activation code in 3.x:

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
   [DSLicenseManager initLicense:@"DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9" verificationDelegate:self];
   return YES;
}
- (void)onLicenseVerified:(BOOL)isSuccess error:(NSError *)error {
   if (error != nil) {
          NSString *msg = error.localizedDescription;
          NSLog(@"erver license verify failed, error:%@", msg);
   }
}
```
2. 
```swift
func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
   LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", verificationDelegate:self)
   return true
}
func onLicenseVerified(_ isSuccess: Bool, error: Error?) {
   if(error != nil)
   {
          if let msg = error?.localizedDescription {
             print("Server license verify failed, error:\(msg)")
          }
   }
}
```

### Update Single Image Recognizing APIs

The APIs for recognizing text from single image has been adjusted as follows:

| Old APIs | New APIs |
| :------- | :------- |
| `DynamsoftLabelRecognizer.recognizeFile` | `DSCaptureVisionRouter.captureFromFile` |
| `DynamsoftLabelRecognizer.recognizeFileInMemory` | `DSCaptureVisionRouter.captureFromFileBytes` |
| `DynamsoftLabelRecognizer.recognizeBuffer` | `DSCaptureVisionRouter.captureFromBuffer` |
| `DynamsoftLabelRecognizer.recognizeImage` | `DSCaptureVisionRouter.captureFromImage` |
| `class iDLRResult` | `class DSCapturedResult/class DSRecognizedTextLinesResult` |

### Update Video Streaming Recognizing APIs

The APIs for recognizing video frames has been adjusted as follows:

| Old APIs | New APIs |
| :------- | :------- |
| `DynamsoftLabelRecognizer.setImageSource` | `DSCaptureVisionRouter.setInput` |
| `DynamsoftLabelRecognizer.startScanning` | `DSCaptureVisionRouter.startCapturing` |
| `DynamsoftLabelRecognizer.stopScanning` | `DSCaptureVisionRouter.stopCapturing` |
| `DynamsoftLabelRecognizer.setLabelResultListener` | `DSCaptureVisionRouter.addResultReceiver` |
| `protocol ImageSource` | `protocol DSImageSourceAdapter` |
| `protocol LabelResultListener` | `protocol DSCapturedResultReceiver` |
| `class iDLRLineResult` | `class DSTextLineResultItem` |

### Migrate Your Templates

The template system is upgraded. The template you used for the previous version can't be directly recognized by the new version. Please <a href="mailto:support@dynamsoft.com">contact us</a> to upgrade your template.

The template-based APIs have been updated as follows:

| Old APIs | New APIs |
| :------- | :------- |
| `DynamsoftLabelRecognizer.initRuntimeSettingsFromFile` | `DSCaptureVisionRouter.initSettingsFromFile` |
| `DynamsoftLabelRecognizer.initRuntimeSettings` | `DSCaptureVisionRouter.initSettings` |
| `DynamsoftLabelRecognizer.outputRuntimeSettingsToFile` | `DSCaptureVisionRouter.outputSettingsToFile` |
| `DynamsoftLabelRecognizer.outputRuntimeSettings` | `DSCaptureVisionRouter.outputSettings` |
| `DynamsoftLabelRecognizer.resetRuntimeSettings` | `DSCaptureVisionRouter.resetSettings` |

### Migrate Your DLRRuntimeSettings

The class `DLRRuntimeSettings` has been refactored. It retains commonly used properties while removing the previously complex property settings, which are now exclusively supported through templates.

The APIs for accessing and updating `DLRRuntimeSettings` has been adjusted as follows:

| Old APIs | New APIs |
| :----------- | :------- |
| `DynamsoftLabelRecognizer.getRuntimeSettings` | `DSCaptureVisionRouter.getSimplifiedSettings` |
| `DynamsoftLabelRecognizer.updateRuntimeSettings` | `DSCaptureVisionRouter.updateSettings` |

#### Migrate to DSSimplifiedCaptureVisionSettings

The following properties are replaced by similar properties under `DSSimplifiedCaptureVisionSettings`. They can also be set via a template file(String).

| PublicRuntimeSettings Property | DSSimplifiedCaptureVisionSettings Property | Template File Parameter |
| ------------------------------- | ----------------------------------------- | ----------------------- |
| `textArea` | [`roi`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html#roi) & [`roiMeasuredInPercentage`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html#roimeasuredinpercentage) | [`TargetROIDef.Location.Offset`]({{ site.dcv_parameters_reference }}target-roi-def/location.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `timeout` | [`timeout`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html#timeout) | [`CaptureVisionTemplates.Timeout`]({{ site.dcv_parameters_reference }}capture-vision-template/timeout.html?lproduct=dlr&repoType=core){:target="_blank"} |

#### Migrate to DSSimplifiedLabelRecognizerSettings

The following properties are replaced by similar properties under `DSSimplifiedLabelRecognizerSettings`. The majority of them can also be set via a template file(String).

| PublicRuntimeSettings Property | DSSimplifiedLabelRecognizerSettings Property | Template File Parameter |
| ------------------------------- | ----------------------------------------- | ----------------------- |
| `characterModelName` | [`characterModelName`]({{ site.dlr_ios_api }}simplified-label-recognizer-settings.html#charactermodelname) | [`DynamsoftLabelRecognizerTaskSetting.CharacterModelName`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/character-model-name.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `maxThreadCount` | [`maxThreadsInOneTask`]({{ site.dlr_ios_api }}simplified-label-recognizer-settings.html#maxthreadsinonetask) | [`DynamsoftLabelRecognizerTaskSetting.MaxThreadsInOneTask`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/max-threads-in-one-task.html?lproduct=dlr&repoType=core){:target="_blank"} |

| FurtherModes Property | DSSimplifiedLabelRecognizerSettings Property | Template File Parameter |
| ---------------------- | ----------------------------------------- | ----------------------- |
| `grayscaleTransformationModes` | [`grayscaleTransformationModes`]({{ site.dlr_ios_api }}simplified-label-recognizer-settings.html#grayscaletransformationmodes) | [`ImageParameter.GrayscaleTransformationModes`]({{ site.dcv_parameters_reference }}image-parameter/grayscale-enhancement-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `grayscaleEnhancementModes` | [`grayscaleEnhancementModes`]({{ site.dlr_ios_api }}simplified-label-recognizer-settings.html#grayscaleenhancementmodes) | [`ImageParameter.GrayscaleEnhancementModes`]({{ site.dcv_parameters_reference }}image-parameter/grayscale-transformation-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |

#### Migrate to Template File

The following properties can only be set via a template file. Please [contact us](https://www.dynamsoft.com/company/customer-service/#contact){:target="_blank"} so that we can help you to transform your current settings to a new template file.

| PublicRuntimeSettings Property | Template File Parameter |
| ------------------------------- | ----------------------- |
| `binarizationModes` | [`ImageParameter.BinarizationModes`]({{ site.dcv_parameters_reference }}image-parameter/binarization-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `dictionaryPath` | [`DynamsoftLabelRecognizerTaskSettings.DictionaryPath`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/dictionary-path.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `dictionaryCorrectionThreshold` | [`DynamsoftLabelRecognizerTaskSettings.DictionaryCorrectionThreshold`]({{ site.dcv_parameters_reference }}label-recognizer-task-settings/dictionary-correction-thresholds.html?lproduct=dlr&repoType=core){:target="_blank"} |

| PublicRuntimeSettings.furtherModes Property | Template File Parameter |
| ---------------------- | ----------------------- |
| `colourConversionModes` | [`ImageParameter.ColourConversionModes`]({{ site.dcv_parameters_reference }}image-parameter/colour-conversion-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `regionPredetectionModes` | [`ImageParameter.RegionPredetectionModes`]({{ site.dcv_parameters_reference }}image-parameter/region-predetection-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
| `textureDetectionModes` | [`ImageParameter.TextureDetectionModes`]({{ site.dcv_parameters_reference }}image-parameter/texture-detection-modes.html?lproduct=dlr&repoType=core){:target="_blank"} |
