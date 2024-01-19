---
layout: default-layout
title: iOS User Guide - Dynamsoft Label Recognizer
description: This is the user guide page of Dynamsoft Label Recognizer for iOS SDK.
keywords: iOS, swift, objective-c, user guide
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /programming/objectivec-swift/user-guide.html
---

# Dynamsoft Label Recognizer - iOS User Guide

- [Requirements](#requirements)
- [Add the xcframeworks](#add-the-xcframeworks)
   - [Add the xcframeworks Manually](#add-the-xcframeworks-manually)
   - [Add the xcframeworks via CocoaPods](#add-the-xcframeworks-via-cocoapods)
- [Build Your First Application](#build-your-first-application)
   - [Create a New Project](#create-a-new-project)
   - [Include the Library](#include-the-library)
   - [Initialize the License](#initialize-the-license)
   - [Initialize the Camera Module](#initialize-the-camera-module)
   - [Initialize the Capture Vision Router](#initialize-the-capture-vision-router)
   - [Receive the Text Line Recognition Results](#receive-the-text-line-recognition-results)
   - [Display the Recognized Textline Results](#display-the-recognized-textline-results)
   - [Configure viewWillAppear, viewDidLoad](#configure-viewwillappear-viewdidload)
   - [Build and Run the Project](#build-and-run-the-project)

## Requirements

- Supported OS: iOS 11+ (iOS 13+ recommended).
- Supported ABI: arm64 and x86_64.
- Development Environment: Xcode 13+ (Xcode 14.1+ recommended).

## Add the xcframeworks

The Dynamsoft Label Recognizer (DLR) iOS SDK comes with seven libraries:

| File | Description |
|---------|-------------|
| *DynamsoftCaptureVisionRouter.xcframework* | The Capture Vision Router library is used to interact with image-processing and semantic-processing products in the applications. It accepts an image source and returns processing results which may contain final results or intermediate results. |
| *DynamsoftLabelRecognizer.xcframework* | The Dynamsoft Label Recognizer library, which includes label localization and text recognition algorithm and related APIs. |
| *DynamsoftCore.xcframework* | The core library, which includes common basic structures and intermediate result related APIs. |
| *DynamsoftImageProcessing.xcframework* | The image processing library, which incorporates a collection of basic and specialized image processing algorithms.  |
| *DynamsoftLicense.xcframework* | The license library, which includes license related APIs. |
| *DynamsoftCameraEnhancer.xcframework* (Optional) | The <a href="/camera-enhancer/docs/mobile/programming/ios/" target="_blank">Dynamsoft Camera Enhancer (DCE) SDK</a> provides camera control, camera enhancements, and basic UI configuration features. |
| *DynamsoftUtility.xcframework* (Optional) | The utility library, which includes multiple implementations of image source adapters, result filter, image exporter, and other utility APIs etc. |

There are two ways to add the libraries into your project - **Manually** or via **CocaPods**.

### Add the xcframeworks Manually

1. Download the SDK package from the <a href="https://www.dynamsoft.com/survey/dlr/?utm_source=docs" target="_blank">Dynamsoft website</a>. After unzipping, seven **xcframework** files can be found in the **Dynamsoft/Frameworks** directory:

   - **DynamsoftCaptureVisionRouter.xcframework**
   - **DynamsoftLabelRecognizer.xcframework**
   - **DynamsoftCore.xcframework**
   - **DynamsoftImageProcessing.xcframework**
   - **DynamsoftLicense.xcframework**
   - **DynamsoftUtility.xcframework**
   - **DynamsoftCameraEnhancer.xcframework**

2. Drag and drop the above **xcframeworks** into your Xcode project. Make sure to check Copy items if needed and create groups to copy the **xcframeworks** into your project's folder.
3. Click on the project settings then go to **General –> Frameworks, Libraries, and Embedded Content**. Set the **Embed** field to **Embed & Sign** for all the **xcframeworks**.

### Add the xcframeworks via CocoaPods

1. Add the frameworks in your **Podfile**, replace *TargetName* with your real target name.

   ```pod
   target '{Your project name}' do
     use_frameworks!

     pod 'DynamsoftLabelRecognizer','3.0.20'
     pod 'DynamsoftCaptureVisionRouter','2.0.21'
     pod 'DynamsoftCore','3.0.20'
     pod 'DynamsoftImageProcessing','2.0.21'
     pod 'DynamsoftLicense','3.0.30'
     pod 'DynamsoftCameraEnhancer','4.0.2'
     pod 'DynamsoftUtility','1.0.21'

   end
   ```

2. Execute the pod command to install the frameworks and generate workspace(**{Your project name}.xcworkspace**):

   ```bash
   pod install
   ```

## Build Your First Application

The following sample will demonstrate how to create a HelloWorld app for recognizing text from camera video input.

>Note:
>
>- The following steps are completed in XCode 14.2
>- View the entire Objective-C source code from [ReadTextLinesWithCameraEnhancerObjc sample](https://github.com/Dynamsoft/label-recognizer-mobile-samples/blob/master/ios/HelloWorld/ReadTextLinesWithCameraEnhancerObjc/)
>- View the entire Swift source code from [ReadTextLinesWithCameraEnhancer sample](https://github.com/Dynamsoft/label-recognizer-mobile-samples/blob/master/ios/HelloWorld/ReadTextLinesWithCameraEnhancer/)

### Create a New Project

1. Open XCode and select *Create a new Xcode Project* or in the *File > New > Project* menu to create a new project.

2. Select **iOS -> App** for your application.

3. Input your product name (Helloworld), interface (StoryBoard) and language (Objective-C/Swift)

4. Click on **Next** and select the location to save the project.

5. Click on **Create** to finish  creating the new project.

### Include the Library

To add the SDK to your new project, please read [add the xcframeworks](#add-the-xcframeworks) section for more details.

### Initialize the License

1. Use the `LicenseManager` class and initialize the license in **AppDelegate**.

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

   >Note:  
   >  
   >- Network connection is required for the license to work.
   >- The license string here will grant you a time-limited trial license.
   >- If the license has expired, you can go to the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=docs&product=dlr&package=mobile" target="_blank">customer portal</a> to request for an extension.

### Initialize the Camera Module

1. Create the instances of `CameraEnhancer` and `CameraView` in **ViewController**.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong) DSCameraEnhancer *dce;
@property (nonatomic, strong) DSCameraView *dceView;
- (void)configureDCE {
   _dceView = [[DSCameraView alloc] initWithFrame:self.view.bounds];
   _dceView.scanLaserVisible = YES;
   [self.view addSubview:_dceView];
   DSDrawingLayer *dlrDrawingLayer = [_dceView getDrawingLayer:DSDrawingLayerIdDLR];
   dlrDrawingLayer.visible = YES;
   _dce = [[DSCameraEnhancer alloc] initWithView:_dceView];
   [_dce open];
   // Set a scan region to restrict the scan area.
   DSRect *region = [[DSRect alloc] init];
   region.top = 0.4;
   region.bottom = 0.6;
   region.left = 0.1;
   region.right = 0.9;
   region.measuredInPercentage = YES;
   [_dce setScanRegion:region error:nil];
}
```
2. 
```swift
class ViewController: BaseViewController{
   private var dce: CameraEnhancer!
   private var dceView: CameraView!
   private func configureDCE() -> Void {
          dceView = CameraView(frame: self.view.bounds)
          dceView.scanLaserVisible = true
          self.view.addSubview(dceView)
          let dlrDrawingLayer = dceView.getDrawingLayer(DrawingLayerId.DLR.rawValue)
          dlrDrawingLayer?.visible = true
          dce = CameraEnhancer(view: dceView)
          dce.open()
          // Set a scan region to restrict the scan area.
          let region = Rect()
          region.top = 0.4
          region.bottom = 0.6
          region.left = 0.1
          region.right = 0.9
          region.measuredInPercentage = true
          try? dce.setScanRegion(region)
   }
}
```

### Initialize the Capture Vision Router

Create an instance of `CaptureVisionRouter` and bind it with the already created instance of `DynamsoftCameraEnhancer`.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong) DSCaptureVisionRouter *cvr;
...
- (void)configureCVR {
   _cvr = [[DSCaptureVisionRouter alloc] init];
   // Set DCE as the input.
   [_cvr setInput:_dce error:nil];
}
```
2. 
```swift
class ViewController: BaseViewController{
   private var cvr: CaptureVisionRouter!
   ...
   private func configureCVR() -> Void {
          cvr = CaptureVisionRouter()
          // Set DCE as the input.
          try? cvr.setInput(dce)
   }
}
```

### Receive the Text Line Recognition Results

Set up result callback in order to receive the text line recognition results after the camera is opened and the scanning starts.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
// Add DSCapturedResultReceiver to the class.
@interface ViewController ()<DSCapturedResultReceiver>
- (void)configureCVR {
   ...
   [_cvr addResultReceiver:self];
}
- (void)onRecognizedTextLinesReceived:(DSRecognizedTextLinesResult *)result {
   if (result.items != nil) {
          // Parse results.
          int index = 0;
          NSMutableString *resultText = [NSMutableString string];
          for (DSTextLineResultItem *dlrLineResults in result.items) {
             index++;
             [resultText appendString:[NSString stringWithFormat:@"Result %d:%@\n", index, dlrLineResults.text != nil ? dlrLineResults.text : @""]];
          }
          dispatch_async(dispatch_get_main_queue(), ^{
             self.resultView.text = [NSString stringWithFormat:@"Results(%d)\n%@", (int)result.items.count, resultText];
          });
   }
}
```
2. 
```swift
// Add CapturedResultReceiver to the class.
class ViewController: UIViewController, CapturedResultReceiver {
   ...
   private func configureCVR() -> Void {
          ...
          // Add a CaptureResultReceiver to receive results.
          cvr.addResultReceiver(self)
   }
   func onRecognizedTextLinesReceived(_ result: RecognizedTextLinesResult) {
          guard let items = result.items else { return }
          // Parse Results.
          var resultText = ""
          var index = 0
          for dlrLineResults in items {
             index+=1
             resultText += String(format: "Result %d:%@\n", index, dlrLineResults.text ?? "")
          }
          DispatchQueue.main.async {
             self.resultView.text = String(format: "Results(%d)\n", items.count) + resultText
          }
   }
}
```

### Display the Recognized Textline Results

Now that we created the result receiver, let's now create a text view to display the text line recognition results that's referenced in the result callback.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
@property (nonatomic, strong) UITextView *resultView;
...
- (UITextView *)resultView {
   if (!_resultView) {
          CGFloat left = 0.0;
          CGFloat width = self.view.bounds.size.width;
          CGFloat height = self.view.bounds.size.height / 2.5;
          CGFloat top = self.view.bounds.size.height - height;
          _resultView = [[UITextView alloc] initWithFrame:CGRectMake(left, top, width, height)];
          _resultView.layer.backgroundColor = [UIColor clearColor].CGColor;
          _resultView.layoutManager.allowsNonContiguousLayout = NO;
          _resultView.font = [UIFont systemFontOfSize:14.0 weight:UIFontWeightMedium];
          _resultView.textColor = [UIColor whiteColor];
          _resultView.textAlignment = NSTextAlignmentCenter;
   }
   return _resultView;
}
- (void)setupUI {
   [self.view addSubview:self.resultView];
}
```
2. 
```swift
class ViewController: UIViewController, CapturedResultReceiver {
   ...
   lazy var resultView: UITextView = {
          let left = 0.0
          let width = self.view.bounds.size.width
          let height = self.view.bounds.size.height / 2.5
          let top = self.view.bounds.size.height - height
          resultView = UITextView(frame: CGRect(x: left, y: top , width: width, height: height))
          resultView.layer.backgroundColor = UIColor.clear.cgColor
          resultView.layoutManager.allowsNonContiguousLayout = false
          resultView.isEditable = false
          resultView.isSelectable = false
          resultView.font = UIFont.systemFont(ofSize: 14.0, weight: .medium)
          resultView.textColor = UIColor.white
          resultView.textAlignment = .center
          return resultView
   }()
   private func setupUI() -> Void {
          self.view.addSubview(resultView)
   }
}
```

### Configure viewWillAppear, viewDidLoad

Time to configure these core functions that will connect everything together. All of the configuration code such as the *configureCVR* and *configureDCE* goes in *viewDidLoad*. While *viewWillAppear* contains the method that will open the camera and start scanning.

<div class="sample-code-prefix"></div>
>- Objective-C
>- Swift
>
>1. 
```objc
- (void)viewWillAppear:(BOOL)animated {
   [super viewWillAppear:animated];
   weakSelfs(self)
   // Start capturing when the view appear.
   [self.cvr startCapturing:DSPresetTemplateRecognizeTextLines completionHandler:^(BOOL isSuccess, NSError * _Nullable error) {
          if (error != nil) {
             [weakSelf displayError:error.localizedDescription completion:nil];
          }
   }];
}
- (void)viewDidLoad {
   [super viewDidLoad];
   self.view.backgroundColor = [UIColor whiteColor];
   // Initialize CaptureVisionRouter, CameraEnhancer and the text view you created.
   [self configureCVR];
   [self configureDCE];
   [self setupUI];
}
- (void)displayError:(NSString *)msg completion:(nullable ConfirmCompletion)completion {
   dispatch_async(dispatch_get_main_queue(), ^{
          UIAlertController *alert = [UIAlertController alertControllerWithTitle:@"" message:msg preferredStyle: UIAlertControllerStyleAlert];
          UIAlertAction *action = [UIAlertAction actionWithTitle:@"OK" style:UIAlertActionStyleDefault handler:^(UIAlertAction * _Nonnull action) {
             if (completion) completion();
          }];
          [alert addAction:action];
          [self presentViewController:alert animated:YES completion:nil];
   });
}
```
2. 
```swift
class ViewController: UIViewController, CapturedResultReceiver {
   override func viewWillAppear(_ animated: Bool) {
          super.viewWillAppear(animated)
          cvr.startCapturing(PresetTemplate.recognizeTextLines.rawValue) {
             [unowned self] isSuccess, error in
             if let error = error {
                self.displayError(msg: error.localizedDescription)
             }
          }
   }
   override func viewDidLoad() {
          super.viewDidLoad()
          self.view.backgroundColor = .white
          // Initialize CaptureVisionRouter, CameraEnhancer and the text view you created.
          configureCVR()
          configureDCE()
          setupUI()
   }
   private func displayError(_ title: String = "", msg: String, _ acTitle: String = "OK", completion: ConfirmCompletion? = nil) {
          DispatchQueue.main.async {
             let alert = UIAlertController(title: title, message: msg, preferredStyle: .alert)
             alert.addAction(UIAlertAction(title: acTitle, style: .default, handler: { _ in completion?() }))
             self.present(alert, animated: true, completion: nil)
          }
   }
}
```

### Build and Run the Project

1. Before deploying the project, select the device that you want to run your app on.
2. Run the project, then your app will be installed on your device.

>Note:
>
>- You can get the source code of the HelloWord app from the following link
>- View the entire Objective-C source code from [ReadTextLinesWithCameraEnhancerObjc sample](https://github.com/Dynamsoft/label-recognizer-mobile-samples/blob/master/ios/HelloWorld/ReadTextLinesWithCameraEnhancerObjc/)
>- View the entire Swift source code from [ReadTextLinesWithCameraEnhancer sample](https://github.com/Dynamsoft/label-recognizer-mobile-samples/blob/master/ios/HelloWorld/ReadTextLinesWithCameraEnhancer/)
