---
layout: default-layout
title: Android User Guide - Dynamsoft Label Recognizer
description: This is the user guide page of Dynamsoft Label Recognizer for Android Language.
keywords: a, user guide
needAutoGenerateSidebar: true
needGenerateH3Content: true
permalink: /programming/android/user-guide.html
---

# Dynamsoft Label Recognizer - Android User Guide

- [Dynamsoft Label Recognizer - Android User Guide](#dynamsoft-label-recognizer---android-user-guide)
  - [Requirements](#requirements)
  - [Add the Libraries](#add-the-libraries)
    - [Add the Libraries Manually](#add-the-libraries-manually)
    - [Add the Libraries via Maven](#add-the-libraries-via-maven)
  - [Build Your First Application](#build-your-first-application)
    - [Create a New Project](#create-a-new-project)
    - [Include the Library](#include-the-library)
    - [Initialize the License](#initialize-the-license)
    - [Initialize Camera Module](#initialize-camera-module)
    - [Initialize Capture Vision Router](#initialize-capture-vision-router)
    - [Display Recognized Textline Results](#display-recognized-textline-results)
    - [Build and Run the Project](#build-and-run-the-project)

## Requirements

- Supported OS: Android 5.0 (API Level 21) or higher.
- Supported ABI: **armeabi-v7a**, **arm64-v8a**, **x86** and **x86_64**.
- Development Environment: Android Studio 3.4+ (Android Studio 4.2+ recommended).

## Add the Libraries

The Dynamsoft Label Recognizer (DLR) Android SDK comes with seven libraries:

   | File | Description |
   |---------|-------------|
   | `DynamsoftCaptureVisionRouter.aar` | The Capture Vision Router library is used to interact with image-processing and semantic-processing products in the applications. It accepts an image source and returns processing results which may contain final results or intermediate results. |
   | `DynamsoftLabelRecognizer.aar` | The Dynamsoft Label Recognizer library, which includes label localization and text recognition algorithm and related APIs. |
   | `DynamsoftCore.aar` | The core library, which includes common basic structures and intermediate result related APIs. |
   | `DynamsoftImageProcessing.aar` | The image processing library, which incorporates a collection of basic and specialized image processing algorithms.  |
   | `DynamsoftLicense.aar` | The license library, which includes license related APIs. |
   | `DynamsoftCameraEnhancer.aar`(Optional) | The <a href="/camera-enhancer/docs/mobile/programming/android/" target="_blank">Dynamsoft Camera Enhancer (DCE) SDK</a> provides camera control, camera enhancements, and basic UI configuration features. |
   | `DynamsoftUtility.aar`(Optional) | The utility library, which includes multiple implementations of image source adapters, result filter, image exporter, and other utility APIs etc. |

There are two ways to add the libraries into your project - **Manually** and **Maven**.

### Add the Libraries Manually

1. Download the SDK package from the <a href="https://www.dynamsoft.com/survey/dlr/?utm_source=docs" target="_blank">Dynamsoft Website</a>. After unzipping, seven **aar** files can be found in the **Dynamsoft\Libs** directory:

   - **DynamsoftCaptureVisionRouter.aar**
   - **DynamsoftLabelRecognizer.aar**
   - **DynamsoftCore.aar**
   - **DynamsoftImageProcessing.aar**
   - **DynamsoftLicense.aar**
   - **DynamsoftUtility.aar**
   - **DynamsoftCameraEnhancer.aar** (Optional)

2. Copy the above seven **aar** files to the target directory such as `[App Project Root Path]\app\libs`

3. Open the file `[App Project Root Path]\app\build.gradle` and add the reference in the dependencies:

   ```groovy
   dependencies {
         implementation fileTree(dir: 'libs', include: ['*.aar'])

         def camerax_version = '1.1.0'
         implementation "androidx.camera:camera-core:$camerax_version"
         implementation "androidx.camera:camera-camera2:$camerax_version"
         implementation "androidx.camera:camera-lifecycle:$camerax_version"
         implementation "androidx.camera:camera-view:$camerax_version"
   }
   ```

   > Note:
   >
   > DCE 4.x is based on Android CameraX, so you need to add the CameraX dependency manually.

4. Click **Sync Now**. After the synchronization is complete, the SDK is added to the project.

### Add the Libraries via Maven

1. Open the file `[App Project Root Path]\app\build.gradle` and add the Maven repository:

   ```groovy
   repositories {
        maven {
           url "https://download2.dynamsoft.com/maven/aar"
        }
   }
   ```

2. Add the references in the dependencies:

   ```groovy
   dependencies {
      implementation 'com.dynamsoft:dynamsoftcapturevisionrouter:2.0.21'
      implementation 'com.dynamsoft:dynamsoftlabelrecognizer:3.0.20'
      implementation 'com.dynamsoft:dynamsoftcameraenhancer:4.0.1'
      implementation 'com.dynamsoft:dynamsoftutility:1.0.20'
   }
   ```

3. Click **Sync Now**. After the synchronization is complete, the SDK is added to the project.

## Build Your First Application

In this section, we are going to explain how to create a Hello World implementation similar to our simple `ReadTextLinesWithCameraEnhancer` app for recognizing text from camera video input.

>Note:
>
>- The following steps are completed in Android Studio 4.2.
>- You can download the complete source code of the [HelloWorld sample](https://github.com/Dynamsoft/label-recognizer-mobile-samples/tree/master/android/HelloWorld).

### Create a New Project

1. Open Android Studio and select New Project… in the File > New > New Project… menu to create a new project.

2. Choose the correct template for your project. In this sample, we'll use `Empty Activity`.

3. When prompted, choose your app name (`ReadTextLinesWithCameraEnhancer`) and set the Save location, Language, and Minimum SDK (21)
    >Note: With minSdkVersion set to 21, your app is available on more than 94.1% of devices on the Google Play Store (last update: March 2021).

### Include the Library

Add the SDK to your new project. Please read [Add the Libraries](#add-the-libraries) section for more details.

### Initialize the License

1. Initialize the license in the file `MainActivity.java`.

   <div class="sample-code-prefix"></div>
   >- Java
   >- Kotlin
   >
   >1. 
   ```java
   import com.dynamsoft.license.LicenseManager;
   public class MainActivity extends AppCompatActivity {
      @Override
      protected void onCreate(Bundle savedInstanceState) {
             super.onCreate(savedInstanceState);
             setContentView(R.layout.activity_main);
             LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9",  this, (isSuccess, error) -> {
             if (!isSuccess) {
                error.printStackTrace();
                runOnUiThread(new Runnable() {
                   @Override
                   public void run() {
                      Toast ts = Toast.makeText(getBaseContext(), "error: " + error.getMessage(), Toast.LENGTH_LONG);
                      ts.show();
                   }
                });
             }
         });
      }
   }
   ```
   2. 
   ```kotlin
   import com.dynamsoft.license.LicenseManager;
   class MainActivityKt : AppCompatActivity() {
      override fun onCreate(savedInstanceState: Bundle?) {
             super.onCreate(savedInstanceState)
             setContentView(R.layout.activity_main_kt)
             LicenseManager.initLicense("DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", this) { isSuccess, error ->
                if (!isSuccess) {
                   error.printStackTrace()
                   runOnUiThread {
                      val ts = Toast.makeText(
                            baseContext,
                            "error: " + error.message,
                            Toast.LENGTH_LONG
                      )
                      ts.show()
                   }
                }
             }
      }
   }
   ```

   >Note:  
   >  
   >- Network connection is required for the license to work.
   >- The license string here will grant you a 24 hour trial license.
   >- You can go to the <a href="https://www.dynamsoft.com/customer/license/trialLicense?utm_source=docs" target="_blank">customer portal</a> to request your own 30-day trial license or to extend an expired trial license.

### Initialize the Camera Module

1. In the Project window, open **app > res > layout > `activity_main.xml`** and create a DCE camera view section under the root node.

    ```xml
    <com.dynamsoft.dce.CameraView
        android:id="@+id/dce_camera_view"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
    ```

2. Import the dynamsoft camera module, initialize the camera view and bind to the created Camera Enhancer instance in the file `MainActivity.java`.

   <div class="sample-code-prefix"></div>
   >- Java
   >- Kotlin
   >
   >1. 
   ```java
   import com.dynamsoft.dce.CameraView;
   import com.dynamsoft.dce.CameraEnhancer;
   import com.dynamsoft.dce.utils.PermissionUtil;
   public class MainActivity extends AppCompatActivity {
      private CameraEnhancer mCamera;
      @Override
      protected void onCreate(Bundle savedInstanceState) {
             ...
             // Add camera view for previewing video.
             PermissionUtil.requestCameraPermission(this);
             CameraView cameraView = findViewById(R.id.dce_camera_view);
             mCamera = new CameraEnhancer(cameraView, this);
      }
   }
   ```
   2. 
   ```kotlin
   import com.dynamsoft.dce.CameraView
   import com.dynamsoft.dce.CameraEnhancer
   import com.dynamsoft.dce.utils.PermissionUtil
   class MainActivityKt : AppCompatActivity() {
      private lateinit var mCamera: CameraEnhancer
      override fun onCreate(savedInstanceState: Bundle?) {
             ...
             PermissionUtil.requestCameraPermission(this)
             val cameraView: CameraView = findViewById(R.id.dce_camera_view)
             mCamera = CameraEnhancer(cameraView, this)
      }
   }
   ```

3. Define a scan region for recognition.

   <div class="sample-code-prefix"></div>
   >- Java
   >- Kotlin
   >
   >1. 
   ```java
   public class MainActivity extends AppCompatActivity {
      @Override
      protected void onCreate(Bundle savedInstanceState) {
             ...
             DSRect region = new DSRect(0.1f, 0.4f, 0.9f, 0.6f, true);
             try {
                mCamera.setScanRegion(region);
             } catch (CameraEnhancerException e) {
                e.printStackTrace();
             }
      }
   }
   ```
   2. 
   ```kotlin
   class MainActivityKt : AppCompatActivity() {
      override fun onCreate(savedInstanceState: Bundle?) {
             ...
             val region = DSRect(0.1f, 0.4f, 0.9f, 0.6f, true)
             try {
                   mCamera.scanRegion = region
             } catch (e: CameraEnhancerException) {
                   e.printStackTrace()
             }
      }
   }
   ```

### Initialize Capture Vision Router

1. Import and initialize the `CaptureVisionRouter` and set the previously created `CameraEnhancer` instance as its input.

   <div class="sample-code-prefix"></div>
   >- Java
   >- Kotlin
   >
   >1. 
   ```java
   import com.dynamsoft.cvr.CaptureVisionRouter;
   import com.dynamsoft.cvr.CaptureVisionRouterException;
   public class MainActivity extends AppCompatActivity {
      ...
      private CaptureVisionRouter mRouter;
      @Override
      protected void onCreate(Bundle savedInstanceState) {
             ...
             mRouter = new CaptureVisionRouter(this);
             try {
                mRouter.setInput(mCamera);
             } catch (CaptureVisionRouterException e) {
                throw new RuntimeException(e);
             }
      }
   }
   ```
   2. 
   ```kotlin
   import com.dynamsoft.cvr.CaptureVisionRouter
   import com.dynamsoft.cvr.CaptureVisionRouterException
   class MainActivityKt : AppCompatActivity() {
      private lateinit var mRouter: CaptureVisionRouter
      override fun onCreate(savedInstanceState: Bundle?) {
             ...
             mRouter = CaptureVisionRouter(this)
             try {
                mRouter.setInput(mCamera)
             } catch (e: CaptureVisionRouterException) {
                throw RuntimeException(e)
             }
      }
   }
   ```

2. Create a `CapturedResultReceiver` and register with the `CaptureVisionRouter` instance to get recognized textline results.

   <div class="sample-code-prefix"></div>
   >- Java
   >- Kotlin
   >
   >1. 
   ```java
   import com.dynamsoft.core.basic_structures.CapturedResultReceiver;
   import com.dynamsoft.dlr.RecognizedTextLinesResult;
   public class MainActivity extends AppCompatActivity {
      @Override
      protected void onCreate(Bundle savedInstanceState) {
             ...
             mRouter.addResultReceiver(new CapturedResultReceiver() {
                @Override
                public void onRecognizedTextLinesReceived(RecognizedTextLinesResult result) {
                   runOnUiThread(() -> showResults(result.getItems()));
                }
             });
      }
   }
   ```
   2. 
   ```kotlin
   import com.dynamsoft.core.basic_structures.CapturedResultReceiver
   import com.dynamsoft.dlr.RecognizedTextLinesResult
   class MainActivityKt : AppCompatActivity() {
      override fun onCreate(savedInstanceState: Bundle?) {
             ...
             mRouter.addResultReceiver(object : CapturedResultReceiver {
                override fun onRecognizedTextLinesReceived(result: RecognizedTextLinesResult) {
                   showResults(result.items)
                }
             })
      }
   }
   ```

3. Override the `MainActivity.onResume` and `MainActivity.onPause` functions to start/stop video text recognition. After starting recognition, the sdk will automatically recognize text in video frames from the Camera Enhancer, then send the recognized textline results to the callback.

   <div class="sample-code-prefix"></div>
   >- Java
   >- Kotlin
   >
   >1. 
   ```java
   import com.dynamsoft.cvr.EnumPresetTemplate;
   import com.dynamsoft.dce.CameraEnhancerException;
   public class MainActivity extends AppCompatActivity {
      ...
      @Override
      public void onResume() {
             try {
                mCamera.open();
             } catch (CameraEnhancerException e) {
                e.printStackTrace();
             }
             mRouter.startCapturing(EnumPresetTemplate.PT_RECOGNIZE_TEXT_LINES, new CompletionListener() {
                @Override
                public void onSuccess() {
                }
                @Override
                public void onFailure(int errorCode, String errorString) {
                   runOnUiThread(() -> Toast.makeText(MainActivity.this, errorString, Toast.LENGTH_SHORT).show());
                }
             });
             super.onResume();
      }
      @Override
      public void onPause() {
             try {
                mCamera.close();
             } catch (CameraEnhancerException e) {
                e.printStackTrace();
             }
             mRouter.stopCapturing();
             super.onPause();
      }
   }
   ```
   2. 
   ```kotlin
   import com.dynamsoft.cvr.EnumPresetTemplate
   import com.dynamsoft.dce.CameraEnhancerException
   public class MainActivity extends AppCompatActivity {
      ...
      public override fun onResume() {
             try {
                mCamera.open()
             } catch (e: CameraEnhancerException) {
                e.printStackTrace()
             }
             mRouter.startCapturing(
                EnumPresetTemplate.PT_RECOGNIZE_TEXT_LINES,
                object : CompletionListener {
                    override fun onSuccess() {}
                    override fun onFailure(errorCode: Int, errorString: String) {
                        runOnUiThread {
                           Toast.makeText(
                              this@MainActivity,
                              errorString,
                              Toast.LENGTH_SHORT
                           ).show()
                        }
                    }
                })
             super.onResume()
      }
      public override fun onPause() {
             try {
                mCamera.close()
             } catch (e: CameraEnhancerException) {
                e.printStackTrace()
             }
             mRouter.stopCapturing()
             super.onPause()
      }
   }
   ```

### Display Recognized Textline Results

1. In the Project window, open **app > res > layout > `activity_main.xml`**, create a text view control under the root node.

   ```xml
   ...
   <TextView
      android:id="@+id/tv_res"
      android:layout_width="match_parent"
      android:layout_height="wrap_content"
      android:textSize="18sp"
      android:padding="15dp"
      android:lineSpacingMultiplier="1.0"
      android:gravity="center"
      android:textColor="@color/white"
      app:layout_constraintBottom_toBottomOf="parent"
      app:layout_constraintStart_toStartOf="parent" />
   ```

2. Display the text result(s) in the text view.

   <div class="sample-code-prefix"></div>
   >- Java
   >- Kotlin
   >
   >1. 
   ```java
   ...
   public class MainActivity extends AppCompatActivity {
      ...
      private TextView tvRes;
      @Override
      protected void onCreate(Bundle savedInstanceState) {
             ...
             tvRes = findViewById(R.id.tv_res);
      }
      private void showResults(TextLineResultItem[] results) {
             StringBuilder resultBuilder = new StringBuilder();
             if (results != null) {
                for (TextLineResultItem result : results) {
                   resultBuilder.append(result.getText()).append("\n\n");
                }
             }
             runOnUiThread(() -> tvRes.setText(resultBuilder.toString()));
      }
   }
   ```
   2. 
   ```kotlin
   ...
   class MainActivityKt : AppCompatActivity() {
      ...
      private lateinit var tvRes: TextView
      override fun onCreate(savedInstanceState: Bundle?) {
             ...
             tvRes = findViewById(R.id.tv_res)
      }
      private fun showResults(results: Array<TextLineResultItem>?) {
             val resultBuilder = StringBuilder()
             if (results != null) {
                for (result in results) {
                      resultBuilder.append(result.text).append("\n\n")
                }
             }
             runOnUiThread { tvRes.text = resultBuilder.toString() }
      }
   }
   ```

### Build and Run the Project

1. Select the device that you want to run your app on from the target device drop-down menu in the toolbar.

2. Click the **Run app** button, then Android Studio installs your app on the connected device and launches it.

You can also download the full source code of all the steps above:

- <a href="https://github.com/Dynamsoft/label-recognizer-mobile-samples/tree/main/android/HelloWorld/ReadTextLinesWithCameraEnhancer" target="_blank">ReadTextLinesWithCameraEnhancer Sample (Java)</a>
- <a href="https://github.com/Dynamsoft/label-recognizer-mobile-samples/tree/main/android/HelloWorld/ReadTextLinesWithCameraEnhancerkt" target="_blank">ReadTextLinesWithCameraEnhancer Sample (Kotlin)</a>
