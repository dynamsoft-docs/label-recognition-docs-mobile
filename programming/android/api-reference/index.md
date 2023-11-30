---
layout: default-layout
title: Dynamsoft Label Recognizer Android API Reference - Main Page
description: This is the main page of Dynamsoft Label Recognizer SDK API Reference for Android Language.
keywords: label recognition, api reference, Android
permalink: /programming/android/api-reference/index.html
---

# API Reference - Android

## Primary Class

- [`CaptureVisionRouter`]({{ site.dcv_android_api }}capture-vision-router/capture-vision-router.html)

## Input

- [`DirectoryFetcher`]({{ site.dcv_android_api }}utility/directory-fetcher.html)
- [`FileFetcher`]({{ site.dcv_android_api }}utility/file-fetcher.html)
- [`ImageSourceAdapter`]({{ site.dcv_android_api }}core/basic-structures/image-source-adapter.html)

## Final Results

- [`CapturedResultReceiver`]({{ site.dcv_android_api }}core/basic-structures/captured-result-receiver.html)
- [`CapturedResultItem`]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html)
- [`CapturedResult`]({{ site.dcv_android_api }}core/basic-structures/captured-result.html)
- [`TextLineResultItem`]({{ site.dlr_android_api }}text-line-result-item.html)
- [`CharacterResult`]({{ site.dlr_android_api }}character-result.html)
- [`RecognizedTextLinesResult`]({{ site.dlr_android_api }}recognized-text-lines-result.html)
- [`OriginalImageResultItem`]({{ site.dcv_android_api }}core/basic-structures/original-image-result-item.html)

## Final Results Filters

- [`CapturedResultFilter`]({{ site.dcv_android_api }}core/basic-structures/captured-result-filter.html)
- [`MultiFrameResultCrossFilter`]({{ site.dcv_android_api }}utility/multi-frame-result-cross-filter.html)

## Intermediate Results

- [`IntermediateResultManager`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-manager.html)
- [`IntermediateResultReceiver`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`ObservationParameters`]({{ site.dcv_android_api }}core/intermediate-results/observed-parameters.html)
- [`IntermediateResultExtraInfo`]({{ site.dcv_android_api }}core/intermediate-result-extra-info.html)
- [`IntermediateResult`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result.html)
- [`IntermediateResultUnit`]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html)
- [`PredetectedRegionsUnit`]({{ site.dcv_android_api }}core/intermediate-results/predetected-regions-unit.html)
- [`LocalizedTextLinesUnit`]({{ site.dlr_android_api }}localized-text-lines-unit.html)
- [`RecognizedTextLinesUnit`]({{ site.dlr_android_api }}recognized-text-lines-unit.html)
- [`RegionObjectElement`]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html)
- [`PredetectedRegionElement`]({{ site.dcv_android_api }}core/intermediate-results/predetected-region-element.html)
- [`LocalizedTextLineElement`]({{ site.dlr_android_api }}localized-text-line-element.html)
- [`RecognizedTextLineElement`]({{ site.dlr_android_api }}recognized-text-line-element.html)
- [`BinaryImageUnit`]({{ site.dcv_android_api }}core/intermediate-results/binary-image-unit.html)
- [`ColourImageUnit`]({{ site.dcv_android_api }}core/intermediate-results/colour-image-unit.html)
- [`EnhancedGrayscaleImageUnit`]({{ site.dcv_android_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`GrayscaleImageUnit`]({{ site.dcv_android_api }}core/intermediate-results/grayscale-image-unit.html)
- [`ScaledDownColourImageUnit`]({{ site.dcv_android_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`TextZonesUnit`]({{ site.dcv_android_api }}core/intermediate-results/text-zones-unit.html)
- [`TextureDetectionResultUnit`]({{ site.dcv_android_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`TextureRemovedBinaryImageUnit`]({{ site.dcv_android_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`TextureRemovedGrayscaleImageUnit`]({{ site.dcv_android_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`TransformedGrayscaleImageUnit`]({{ site.dcv_android_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

## Settings

- [`SimplifiedCaptureVisionSettings`]({{ site.dcv_android_api }}capture-vision-router/structs/simplified-capture-vision-settings.html)
- [`SimplifiedLabelRecognizerSettings`]({{ site.dlr_android_api }}simplified-label-recognizer-settings.html)

## State Listener

- [`CaptureStateListener`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`ImageSourceStateListener`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## License

- [`LicenseManager`]({{ site.dcv_android_api }}license/license-manager.html)

## Basic Structure

- [`Rect`]({{ site.dcv_android_api }}core/basic-structures/rect.html)
- [`Quadrilateral`]({{ site.dcv_android_api }}core/basic-structures/quadrilateral.html)
- [`ImageData`]({{ site.dcv_android_api }}core/basic-structures/image-data.html)
- [`ImageTag`]({{ site.dcv_android_api }}core/basic-structures/image-tag.html)
- [`FileImageTag`]({{ site.dcv_android_api }}core/basic-structures/file-image-tag.html)
- [`PDFReadingParameter`]({{ site.dcv_android_api }}core/basic-structures/pdf-reading-parameter.html)

## Modules

- [`CaptureVisionRouterModule`]({{ site.dcv_android_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`LabelRecognizerModule`]({{ site.dlr_android_api }}label-recognizer-module.html)
- [`CoreModule`]({{ site.dcv_android_api }}core/basic-structures/core-module.html)
- [`LicenseModule`]({{ site.dcv_android_api }}license/license-module.html)
- [`UtilityModule`]({{ site.dcv_android_api }}utility/utility-module.html)
- [`ImageProcessingModule`]({{ site.dcv_android_api }}image-processing/image-processing-module.html)

## Enumerations

- [`BufferOverflowProtectionMode`]({{ site.dcv_enumerations}}core/buffer-overflow-protection-mode.html?src=android&&lang=android)
- [`CapturedResultItemType`]({{ site.dcv_enumerations}}core/captured-result-item-type.html?src=android&&lang=android)
- [`ErrorCode`]({{ site.dcv_enumerations}}core/error-code.html?src=android&&lang=android)
- [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html?src=android&&lang=android)
- [`ImageCaptureDistanceMode`]({{ site.dcv_enumerations}}core/image-capture-distance-mode.html?src=android&&lang=android)
- [`ImagePixelFormat`]({{ site.dcv_enumerations}}core/image-pixel-format.html?src=android&&lang=android)
- [`ImageSourceState`]({{ site.dcv_enumerations}}core/image-source-state.html?src=android&&lang=android)
- [`ImageTagType`]({{ site.dcv_enumerations}}core/image-tag-type.html?src=android&&lang=android)
- [`IntermediateResultUnitType`]({{ site.dcv_enumerations}}core/intermediate-result-unit-type.html?src=android&&lang=android)
- [`PDFReadingMode`]({{ site.dcv_enumerations}}core/pdf-reading-mode.html?src=android&&lang=android)
- [`PresetTemplate`]({{ site.dcv_enumerations }}capture-vision-router/preset-template.html?src=android&&lang=android)
- [`RegionObjectElementType`]({{ site.dcv_enumerations}}core/region-object-element-type.html?src=android&&lang=android)
- [`SectionType`]({{ site.dcv_enumerations}}core/section-type.html?src=android&&lang=android)
- [`VideoFrameQuality`]({{ site.dcv_enumerations }}core/video-frame-quality.html?src=android&&lang=android)
- [`ColourChannelUsageType`]({{ site.dcv_enumerations}}core/colour-channel-usage-type.html?src=android&&lang=android)
- [`RasterDataSource`]({{ site.dcv_enumerations}}core/raster-data-source.html?src=android&&lang=android)
- [`TransformMatrixType`]({{ site.dcv_enumerations}}core/transform-matrix-type.html?src=android&&lang=android)
