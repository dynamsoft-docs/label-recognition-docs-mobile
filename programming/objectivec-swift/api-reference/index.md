---
layout: default-layout
title: Dynamsoft Label Recognizer iOS API Reference
description: This is the index of Dynamsoft Label Recognizer iOS API Reference.
keywords: label recognizer, api reference, iOS
permalink: /programming/objectivec-swift/api-reference/index.html
---

# API Reference - iOS

## Primary Class

- [`DSCaptureVisionRouter`]({{ site.dcv_ios_api }}capture-vision-router/capture-vision-router.html)

## Input

- [`DSDirectoryFetcher`]({{ site.dcv_ios_api }}utility/directory-fetcher.html)
- [`DSFileFetcher`]({{ site.dcv_ios_api }}utility/file-fetcher.html)
- [`DSImageSourceAdapter`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html)

## Final Results

- [`DSCapturedResultReceiver`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-receiver.html)
- [`DSCapturedResultItem`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-item.html)
- [`DSCapturedResult`]({{ site.dcv_ios_api }}core/basic-structures/captured-result.html)
- [`DSTextLineResultItem`]({{ site.dlr_ios_api }}text-line-result-item.html)
- [`DSCharacterResult`]({{ site.dlr_ios_api }}character-result.html)
- [`DSRecognizedTextLinesResult`]({{ site.dlr_ios_api }}recognized-text-lines-result.html)
- [`DSOriginalImageResultItem`]({{ site.dcv_ios_api }}core/basic-structures/original-image-result-item.html)

## Final Results Filters

- [`DSCapturedResultFilter`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-filter.html)
- [`DSMultiFrameResultCrossFilter`]({{ site.dcv_ios_api }}utility/multi-frame-result-cross-filter.html)

## Intermediate Results

- [`DSIntermediateResultManager`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-manager.html)
- [`DSIntermediateResultReceiver`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`DSObservationParameters`]({{ site.dcv_ios_api }}core/intermediate-results/observed-parameters.html)
- [`DSIntermediateResultExtraInfo`]({{ site.dcv_ios_api }}core/intermediate-result-extra-info.html)
- [`DSIntermediateResult`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result.html)
- [`DSIntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html)
- [`DSPredetectedRegionsUnit`]({{ site.dcv_ios_api }}core/intermediate-results/predetected-regions-unit.html)
- [`DSLocalizedTextLinesUnit`]({{ site.dlr_ios_api }}localized-text-lines-unit.html)
- [`DSRecognizedTextLinesUnit`]({{ site.dlr_ios_api }}recognized-text-lines-unit.html)
- [`DSRegionObjectElement`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html)
- [`DSPredetectedRegionElement`]({{ site.dcv_ios_api }}core/intermediate-results/predetected-region-element.html)
- [`DSLocalizedTextLineElement`]({{ site.dlr_ios_api }}localized-text-line-element.html)
- [`DSRecognizedTextLineElement`]({{ site.dlr_ios_api }}recognized-text-line-element.html)
- [`DSBinaryImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/binary-image-unit.html)
- [`DSColourImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/colour-image-unit.html)
- [`DSEnhancedGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`DSGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/grayscale-image-unit.html)
- [`DSScaledDownColourImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`DSTextZonesUnit`]({{ site.dcv_ios_api }}core/intermediate-results/text-zones-unit.html)
- [`DSTextureDetectionResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`DSTextureRemovedBinaryImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`DSTextureRemovedGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`DSTransformedGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

## Settings

- [`DSSimplifiedCaptureVisionSettings`]({{ site.dcv_ios_api }}capture-vision-router/structs/simplified-capture-vision-settings.html)
- [`DSSimplifiedLabelRecognizerSettings`]({{ site.dlr_ios_api }}simplified-label-recognizer-settings.html)

## State Listener

- [`DSCaptureStateListener`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`DSImageSourceStateListener`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## License

- [`DSLicenseManager`]({{ site.dcv_ios_api }}license/license-manager.html)

## Basic Structure

- [`DSRect`]({{ site.dcv_ios_api }}core/basic-structures/rect.html)
- [`DSQuadrilateral`]({{ site.dcv_ios_api }}core/basic-structures/quadrilateral.html)
- [`DSImageData`]({{ site.dcv_ios_api }}core/basic-structures/image-data.html)
- [`DSImageTag`]({{ site.dcv_ios_api }}core/basic-structures/image-tag.html)
- [`DSFileImageTag`]({{ site.dcv_ios_api }}core/basic-structures/file-image-tag.html)

## Modules

- [`DSCaptureVisionRouterModule`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`DSLabelRecognizerModule`]({{ site.dlr_ios_api }}label-recognizer-module.html)
- [`DSCoreModule`]({{ site.dcv_ios_api }}core/basic-structures/core-module.html)
- [`DSLicenseModule`]({{ site.dcv_ios_api }}license/license-module.html)
- [`DSUtilityModule`]({{ site.dcv_ios_api }}utility/utility-module.html)
- [`DSImageProcessingModule`]({{ site.dcv_ios_api }}image-processing/image-processing-module.html)

## Enumerations

- [`DSBufferOverflowProtectionMode`]({{ site.dcv_enumerations}}core/buffer-overflow-protection-mode.html?src=objc,swift&&lang=objc,swift)
- [`DSCapturedResultItemType`]({{ site.dcv_enumerations}}core/captured-result-item-type.html?src=objc,swift&&lang=objc,swift)
- [`DSErrorCode`]({{ site.dcv_enumerations}}core/error-code.html?src=objc,swift&&lang=objc,swift)
- [`DSGrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html?src=objc,swift&&lang=objc,swift)
- [`DSImageCaptureDistanceMode`]({{ site.dcv_enumerations}}core/image-capture-distance-mode.html?src=objc,swift&&lang=objc,swift)
- [`DSImagePixelFormat`]({{ site.dcv_enumerations}}core/image-pixel-format.html?src=objc,swift&&lang=objc,swift)
- [`DSImageSourceState`]({{ site.dcv_enumerations}}core/image-source-state.html?src=objc,swift&&lang=objc,swift)
- [`DSImageTagType`]({{ site.dcv_enumerations}}core/image-tag-type.html?src=objc,swift&&lang=objc,swift)
- [`DSIntermediateResultUnitType`]({{ site.dcv_enumerations}}core/intermediate-result-unit-type.html?src=objc,swift&&lang=objc,swift)
- [`DSDSPresetTemplate`]({{ site.dcv_enumerations }}capture-vision-router/preset-template.html?src=objc,swift&&lang=objc,swift)
- [`DSRegionObjectElementType`]({{ site.dcv_enumerations}}core/region-object-element-type.html?src=objc,swift&&lang=objc,swift)
- [`DSSectionType`]({{ site.dcv_enumerations}}core/section-type.html?src=objc,swift&&lang=objc,swift)
- [`DSVideoFrameQuality`]({{ site.dcv_enumerations }}core/video-frame-quality.html?src=objc,swift&&lang=objc,swift)
- [`DSColourChannelUsageType`]({{ site.dcv_enumerations}}core/colour-channel-usage-type.html?src=objc,swift&&lang=objc,swift)
- [`DSRasterDataSource`]({{ site.dcv_enumerations}}core/raster-data-source.html?src=objc,swift&&lang=objc,swift)
- [`DSTransformMatrixType`]({{ site.dcv_enumerations}}core/transform-matrix-type.html?src=objc,swift&&lang=objc,swift)
