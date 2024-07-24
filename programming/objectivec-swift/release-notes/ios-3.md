---
layout: default-layout
title: iOS SDK Release Notes 3.x - Dynamsoft Label Recognizer
description: This is the release notes page of Dynamsoft Label Recognizer for iOS SDK version 3.x.
keywords: release notes, ios
needAutoGenerateSidebar: false
permalink: /programming/objectivec-swift/release-notes/ios-3.html
---

# DLR Release Notes - iOS 3.x

<!-- ## 3.2.3001 (07/24/2024)

- Updated signature of license module to prevent rejection of Apple store. -->

## 3.2.30 (05/15/2024)

### Highlights

- Added confusable character distinguishing: this feature enhances the library’s ability to distinguish between common confusable character sets including {0, o, O}, {1, I, l}, and {5, s, S}, across popular fonts like Arial, Times New Roman, and Verdana, etc.
- Supported confusable character set customization: leveraging the new caching mechanism in the `CaptureVisionRouter (CVR)` module, the library now enables users to customize confusable character sets to meet the needs of specific scenarios.
- Introduced the capability for users to influence the image processing process by altering intermediate results. Users can now clone, edit, and substitute intermediate result units within the callback function of each type. Subsequent operations will then proceed based on the updated unit.
- Introduced a feature for multi-condition filtering across products. Users can now specify filtering criteria for the task results of a [`TargetROIDef`]({{ site.dcv_parameter }}reference/target-roi-def/){:target="_blank"} by implementing an OutputTaskSetting based on the task results of varying products from descendant `TargetROIDef` objects.
- Enhanced the [`Offset`]({{ site.dcv_parameter }}reference/target-roi-def/location.html#offset){:target="_blank"} parameter in `TargetROIDef`. Users now have the capability to meticulously customize components of the coordinate system, including the origin, X-axis, and Y-axis, for precise offset calculation.
- Introduced a feature for grouping text lines. A text line group consists of spatially adjacent lines of text. Through the [`TextLineSpecification`]({{ site.dcv_parameter }}reference/text-line-specification/){:target="_blank"} parameters, users can now do two things:
  - Put text lines in groups and also define the spatial relationship between different groups;
  - Specify whether to concatenate text line results within a group, how to do the concatenation and whether to output the concatenated result.

### Changelogs

#### Improved

- Improved the speed of `TextLineGroup` detection by optimizing internal logic.
- Security update for `DynamsoftLabelRecognizer` library and other corresponding libraries.
- Supported multiple instances of the class `CaptureVisionRouter`.
- Supported the filter configuration of the characters that are not recognized by the Deep Neural Network via the Filter.txt file.
- Improved the usage count logic of the concurrent license mode.
- Improved the experience of local cache usage when failing to connect the license server. The renewal of the local cache is optimized as well.
- Improved the `CharacterModel` loading mechanism. If a model file is available under the `DynamsoftResources.bundle` file, the `CharacterModel` will be loaded autometically. Otherwise, it will be downloaded from the server.

### New

- Added new APIs for users to obtain the cached character items and the character clusters:
- A new class [`DSBufferedCharacterItemSet`]({{ site.dlr_ios_api }}buffered-character-item-set.html) to represent a collection of buffered character items and cluster information.
- A new class [`DSBufferedCharacterItem`]({{ site.dlr_ios_api }}buffered-character-item.html) to represent a basic item of the buffered characters with its image and features information.
- A new class [`DSCharacterCluster`]({{ site.dlr_ios_api }}character-cluster.html) to represent a character cluster generated from the collected buffered character items.
- Added a new class [`DSBufferedItemsManager`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/buffered-items-manager.html) to manage the buffered character items.
- Added a new method [`getBufferedItemsManger`]({{ site.dcv_ios_api }}capture-vision-router/buffered-items.html#getbuffereditemsmanager) to the `CaptureVisionRouter` class to get an object of `DSBufferedItemsManager`.
- Added a new property [`specificationName`]({{ site.dlr_ios_api }}text-line-result-item.html#specificationname) to the `TextLineResultItem` class to get the name of the [`TextLineSpecificationObject`]({{ site.dcv_parameter }}file/auxiliary/textline-specification.html){:target="_blank"} that generated this `TextLineResultItem`.
- Added a new method [`getSpecificationName`]({{ site.dlr_ios_api }}recognized-text-line-element.html#getspecificationname) to the `DSRecognizedTextLineElement` class to get the name of the [`TextLineSpecificationObject`]({{ site.dcv_parameter }}file/auxiliary/textline-specification.html){:target="_blank"} that generated this `DSRecognizedTextLineElement`.
- Added new [error codes]({{ site.dcv_enumerations }}core/error-code.html?lang=objc,swift):
  - `DSErrorResultTypeMismatchIrreplaceable`
  - `DSErrorLicenseCacheUsed`
  - `DSErrorImageSizeNotMatch`
  - `DSErrorImagePixelFormatNotMatch`
  - `DSErrorSectionLevelResultIrreplaceable`
  - `DSErrorAxisDefinitionIncorrect`
  - `DSErrorTextLineGroupLayoutConflict`
  - `DSErrorTextLineGroupRegexConflict`
- Added a new method [`getRecognizedTextLinesResult`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result.html#getrecognizedtextlinesresult) to the `DSCapturedResult` class to get all the result items with the type `CRIT_TEXT_LINE`.
- Added new virtual destructors to the following interfaces to prevent memory leaks.
  - [`DSCaptureStateListener`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
  - [`DSImageSourceStateListener`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)
- The following classes are migrated from `DynamsoftCore.framework` into `DynamsoftCaptureVision.framework`:
  - [`DSCapturedResult`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result.html)
  - [`DSIntermediateResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html)
  - [`DSCapturedResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html)
  - [`DSCapturedResultFilter`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-filter.html)
  - [`DSIntermediateResultManager`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/intermediate-result-manager.html)
- Added a new call back method [`onShortLinesUnitReceived`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html#onshortlinesunitreceived) to the [`DSIntermediateResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/intermediate-result-receiver.html) class.
- Added methods [`pauseCapturing`]({{ site.dcv_ios_api }}capture-vision-router/multiple-file-processing.html#pausecapturing) and [`resumeCapturing`]({{ site.dcv_ios_api }}capture-vision-router/multiple-file-processing.html#resumecapturing). Two new enumeration members, `CapturedStatePaused` and `CapturedStateResumed`, are added to [`DSCapturedState`]({{ site.dcv_enumerations }}capture-vision-router/capture-state.html?lang=objc,swift) as well.
- Added a new property [`resultUnitTypesOnlyForInput`]({{ site.dcv_ios_api }}core/intermediate-results/observation-parameters.html#resultunittypesonlyforinput) to the `ObservationParameters` class to specify the `input only` result unit.
- Added the following methods to the [`RegionObjectElement`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html) class to support the intermediate result modification.
  - `setLocation`
  - `clone`
  - `retain`
  - `release`
- Added a new method `replace` to the [`DSIntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html) class to support the replacement of intermediate result units.
- Added `setImageData` methods to the following classes:
  - [`DSColourImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/colour-image-unit.html)
  - [`DSScaledDownColourImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
  - [`DSGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/grayscale-image-unit.html)
  - [`DSTransformedGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/transformed-grayscale-image-unit.html)
  - [`DSEnhancedGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
  - [`DSBinaryImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/binary-image-unit.html)
  - [`DSTextureRemovedGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
  - [`DSTextureRemovedBinaryImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
  - [`DSTextRemovedBinaryImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/text-removed-binary-image-unit.html)
- Added new methods to the [`DSPredetectedRegionsUnit`]({{ site.dcv_ios_api }}core/intermediate-results/predetected-regions-unit.html) class to add, remove or set the predetected regions.
- Added new methods to the [`DSLineSegmentsUnit`]({{ site.dcv_ios_api }}core/intermediate-results/line-segments-unit.html) class to add, remove or set the line segments.
- Added new methods to the [`DSTextZonesUnit`]({{ site.dcv_ios_api }}core/intermediate-results/text-zones-unit.html) class to add, remove or set the text zones. Added a new class CTextZone to store the information of a single text zone.
- Added a new method `setContours` to the [`DSContourUnit`]({{ site.dcv_ios_api }}core/intermediate-results/contours-unit.html) class.
- Added new methods to the [`DSTextureDetectionResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/texture-detection-result-unit.html) class to set the X & Y spacing.
- Added a new intermediate result unit, [`DSShortLinesUnit`]({{ site.dcv_ios_api }}core/intermediate-results/short-lines-unit.html), to output the detected short lines. The corresponding enumeration member `DSIntermediateResultUnitTypeShortLines` is added to the [`DSIntermediateResultUnitType`]({{ site.dcv_enumerations }}core/intermediate-result-unit-type.html?lang=objc,swift).
- Added the following methods to the [`DSCapturedResultItem`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-item.html) class
  - `getTargetROIDefName`
  - `getTaskName`
  - `retain`
  - `release`
- Added the following methods to the [`DSCapturedResult`]({{ site.dcv_ios_api }}core/basic-structures/captured-result.html) class.
  - `retain`
  - `release`
- Added a new supported image pixel format, binary 8 inverted. The corresponding enumeration member is added to the [`DSImagePixelFormat`]({{ site.dcv_enumerations }}core/image-pixel-format.html?lang=objc,swift).
- Added return value for the `retain` method of the [`DSIntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html) class. The method will return the pointer of the current `DSIntermediateResultUnit`.
- Added new methods to the [`DSLocalizedTextLinesUnit`]({{ site.dlr_ios_api }}localized-text-lines-unit.html) class to add, set or remove the localized text line elements.
- Added new methods to the [`DSRecognizedTextLinesUnit`]({{ site.dlr_ios_api }}recognized-text-lines-unit.html) class to add, set or remove the recognized text line elements.
- Added a new method `setText` to the [`DSRecognizedTextLineElement`]({{ site.dlr_ios_api }}recognized-text-line-element.html) class.
- Added the following methods to the [`DSRecognizedTextLinesResult`]({{ site.dlr_ios_api }}recognized-text-lines-result.html) class.
  - `retain`
  - `release`
- Added new constructors to the following classes.
  - [`DSRecognizedTextLineElement`]({{ site.dlr_ios_api }}recognized-text-line-element.html)
  - [`DSLocalizedTextLineElement`]({{ site.dlr_ios_api }}localized-text-line-element.html)
- Updated the template system
  - Added new [`LabelRecognizerTaskSettings`]({{ site.dcv_parameter }}reference/label-recognizer-task-settings/){:target="_blank"} parameters.
    - Added `ConfusableCharactersPath` to define the path of the resource files that store the confusable characters' information.
    - Added `ClusterSamplesCountThreshold` to specify the lowest required sample count for clustering.
  - Added new [`TextLineSpecification`]({{ site.dcv_parameter }}reference/text-line-specification/){:target="_blank"} parameters.
    - Added `ConfusableCharactersCorrection` to define which confusable characters you are going to distinguish. You can also specify the font type of the characters.
    - Added `ExpectedGroupCount` to define the count of `TextLineGroups` that might exist on the image.
  - Added `StringLengthRange` for [`TextDetectionMode`]({{ site.dcv_parameter }}reference/image-parameter/text-detection-mode.html){:target="_blank"}.
  - Added `ReferenceTaskNameArray` under [`Location.ReferenceObjectFilter`]({{ site.dcv_parameter }}reference/target-roi-def/location.html){:target="_blank"} to filter the reference objects generated by the task name.
  - Added the support of the [`OutputTaskSetting`]({{ site.dcv_parameter }}reference/output-task-setting/index.html){:target="_blank"} definition. The following subparameters are available in `OutputTaskSetting` object:
    - [`OutputCondition`]({{ site.dcv_parameter }}reference/output-task-setting/output-condition.html){:target="_blank"}
      - [`TaskResultArray`]({{ site.dcv_parameter }}reference/output-task-setting/output-condition.html#taskresultarray){:target="_blank"}
      - [`TargetROIDefName`]({{ site.dcv_parameter }}reference/target-roi-def/index.html#targetroidefname){:target="_blank"}
      - [`TaskSettingNameArray`]({{ site.dcv_parameter }}reference/output-task-setting/output-condition.html#tasksettingnamearray){:target="_blank"}
      - [`BackwardReferenceOutput`]({{ site.dcv_parameter }}reference/output-task-setting/output-condition.html#backwardreferenceoutput){:target="_blank"}
        - `ReferenceTaskNameArray`
        - `ReferenceResultTypeArray`
      - [`Operator`]({{ site.dcv_parameter }}reference/output-task-setting/output-condition.html){:target="_blank"}
    - [`Name`]({{ site.dcv_parameter }}reference/output-task-setting/name.html){:target="_blank"}
  - [`Offset`]({{ site.dcv_parameter }}reference/target-roi-def/location.html#offset){:target="_blank"} parameter is optimized.
    - Added `ReferenceObjectType` to specify whether the reference object is an atomic object or the whole image.
    - Added `ReferenceXAxis` & `ReferenceYAxis` to define the X & Y axis.
    - Modified `FirstPoint`, `SecondPoint`, `ThirdPoint` & `FourthPoint`. You can specify whether the X or Y coordinate of the point is measured by percentage.
    - Deprecated `ReferenceObjectSize` Type.

### Changes

- Changed the logic of the [`stopCapturing`]({{ site.dcv_ios_api }}capture-vision-router/multiple-file-processing.html#stopCapturing) method.
  - [`DSCaptureResultReceiver`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/captured-result-receiver.html) will not receive results after `stopCapturing` is triggered with `waitForRemainingTasks` false.
  - Support stop capturing after the [`pauseCapturing`]({{ site.dcv_ios_api }}capture-vision-router/multiple-file-processing.html#pauseCapturing) method is triggered.
- Changed the logic of the [`capturedResultItemTypes`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/simplified-capture-vision-settings.html#capturedresultitemtypes) setting of `DSSimplifiedCaptureVisionSettings`:
  - If the result item types don't match the specified template, the method [`updateSettings`]({{ site.dcv_ios_api }}capture-vision-router/settings.html#updatesettings) will return the error code `DSErrorParameterValueInvalid` with the message "The captured result item types do not match the task configurations in the template".
  - Based on the `capturedResultItemTypes` setting, the irrelevant tasks will be removed from the template.
  - The `capturedResultItemTypes` should include at least one of the `DSCapturedResultItemTypeBarcode`, `DSCapturedResultItemTypeTextLine`, `DSCapturedResultItemTypeDetectedQuad`, `DSCapturedResultItemTypeNormalizedImage`. Otherwise, the method `updateSettings` will return the error code `DSErrorParameterValueInvalid` with the message "The captured result item types should contain at least one task result type".
- Refactored the [`DSContour`]({{ site.dcv_ios_api }}core/basic-structures/contour.html) class. Please view API reference - [`DSContour`]({{ site.dcv_ios_api }}core/basic-structures/contour.html) class for more information.
- Changed the internal logic of the property [`resultUnitTypesOnlyForInput`]({{ site.dcv_ios_api }}core/intermediate-results/observation-parameters.html#resultunittypesonlyforinput) of `DSObservationParameters`. The method only takes effect when the callback of the specified result unit is implemented.

### Fixed

- Fixed a crash bug that might happen when triggering the [`setNextImageToReturn`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html#setnextimagetoreturn) method of the `DSImageSourceAdapter` class.
- Fixed a crash bug of the Replace method of the `IntermediateResultUnit` class. The method will return the error code `EC_RESULT_TYPE_MISMATCH_IRREPLACEABLE` when the result type is mismatched.
- Fixed a bug where error messages are not output when parsing the parameter templates.
- Fixed a bug where multiple results were output from the same text area.
- Fixed a bug where the capture might be blocked due to the network latency.
- Fixed the bugs of usage count. The usage count of text line recognition might be double counted when the intermediate results are output.

## 3.0.20 (12/07/2023)

{%- include release-notes/product-highlight-3.0.0.md -%}

The APIs of Dynamsoft Label Recognizer are comprehensively updated. Please follow the view [upgrade instructions]{{ site.dlr_ios }}upgrade.html to update your code.
