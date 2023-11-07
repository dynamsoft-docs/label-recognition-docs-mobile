---
layout: default-layout
title: Dynamsoft Label Recognizer C++ API Reference - Main Page
description: This is the main page of Dynamsoft Label Recognizer SDK API Reference for C++ Language.
keywords: label recognition, api reference, C++
permalink: /programming/objectivec-swift/api-reference/index.html
---

# API Reference - C++

## Primary Class

- [`CCaptureVisionRouter`]({{ site.dcv_ios_api }}capture-vision-router/capture-vision-router.html)

## Input

- [`CDirectoryFetcher`]({{ site.dcv_ios_api }}utility/directory-fetcher.html)
- [`CFileFetcher`]({{ site.dcv_ios_api }}utility/file-fetcher.html)
- [`CImageSourceAdapter`]({{ site.dcv_ios_api }}core/basic-structures/image-source-adapter.html)
- [`CProactiveImageSourceAdapter`]({{ site.dcv_ios_api }}utility/proactive-image-source-adapter.html)

## Final Results

- [`CCapturedResultReceiver`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-receiver.html)
- [`CCapturedResultItem`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-item.html)
- [`CCapturedResult`]({{ site.dcv_ios_api }}core/basic-structures/captured-result.html)
- [`CTextLineResultItem`]({{ site.cpp_api }}text-line-result-item.html)
- [`CCharacterResult`]({{ site.cpp_api }}character-result.html)
- [`CRecognizedTextLinesResult`]({{ site.cpp_api }}recognized-text-lines-result.html)
- [`COriginalImageResultItem`]({{ site.dcv_ios_api }}core/basic-structures/original-image-result-item.html)

## Final Results Filters

- [`CCapturedResultFilter`]({{ site.dcv_ios_api }}core/basic-structures/captured-result-filter.html)
- [`CMultiFrameResultCrossFilter`]({{ site.dcv_ios_api }}utility/multi-frame-result-cross-filter.html)

## Intermediate Results

- [`CIntermediateResultManager`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-manager.html)
- [`CIntermediateResultReceiver`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-receiver.html)
- [`CObservationParameters`]({{ site.dcv_ios_api }}core/intermediate-results/observed-parameters.html)
- [`IntermediateResultExtraInfo`]({{ site.dcv_ios_api }}core/structs/intermediate-result-extra-info.html)
- [`CIntermediateResult`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result.html)
- [`CIntermediateResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/intermediate-result-unit.html)
- [`CPredetectedRegionsUnit`]({{ site.dcv_ios_api }}core/intermediate-results/predetected-regions-unit.html)
- [`CLocalizedTextLinesUnit`]({{ site.cpp_api }}localized-text-lines-unit.html)
- [`CRecognizedTextLinesUnit`]({{ site.cpp_api }}recognized-text-lines-unit.html)
- [`CRegionObjectElement`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html)
- [`CPredetectedRegionElement`]({{ site.dcv_ios_api }}core/intermediate-results/predetected-region-element.html)
- [`CLocalizedTextLineElement`]({{ site.cpp_api }}localized-text-line-element.html)
- [`CRecognizedTextLineElement`]({{ site.cpp_api }}recognized-text-line-element.html)
- [`CBinaryImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/binary-image-unit.html)
- [`CColourImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/colour-image-unit.html)
- [`CEnhancedGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/enhanced-grayscale-image-unit.html)
- [`CGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/grayscale-image-unit.html)
- [`CScaledDownColourImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/scaled-down-colour-image-unit.html)
- [`CTextZonesUnit`]({{ site.dcv_ios_api }}core/intermediate-results/text-zones-unit.html)
- [`CTextureDetectionResultUnit`]({{ site.dcv_ios_api }}core/intermediate-results/texture-detection-result-unit.html)
- [`CTextureRemovedBinaryImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/texture-removed-binary-image-unit.html)
- [`CTextureRemovedGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/texture-removed-grayscale-image-unit.html)
- [`CTransformedGrayscaleImageUnit`]({{ site.dcv_ios_api }}core/intermediate-results/transformed-grayscale-image-unit.html)

## Settings

- [`SimplifiedCaptureVisionSettings`]({{ site.dcv_ios_api }}capture-vision-router/structs/simplified-capture-vision-settings.html)
- [`SimplifiedLabelRecognizerSettings`]({{ site.cpp_api }}simplified-label-recognizer-settings.html)
- [`CPresetTemplate`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/preset-template.html)

## State Listener

- [`CCaptureStateListener`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/capture-state-listener.html)
- [`CImageSourceStateListener`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/image-source-state-listener.html)

## License

- [`CLicenseManager`]({{ site.dcv_ios_api }}license/license-manager.html)

## Basic Structure

- [`CPoint`]({{ site.dcv_ios_api }}core/basic-structures/point.html)
- [`CRect`]({{ site.dcv_ios_api }}core/basic-structures/rect.html)
- [`CQuadrilateral`]({{ site.dcv_ios_api }}core/basic-structures/quadrilateral.html)
- [`CImageData`]({{ site.dcv_ios_api }}core/basic-structures/image-data.html)
- [`CImageTag`]({{ site.dcv_ios_api }}core/basic-structures/image-tag.html)
- [`CFileImageTag`]({{ site.dcv_ios_api }}core/basic-structures/file-image-tag.html)
- [`CPDFReadingParameter`]({{ site.dcv_ios_api }}core/basic-structures/pdf-reading-parameter.html)

## Modules

- [`CCaptureVisionRouterModule`]({{ site.dcv_ios_api }}capture-vision-router/auxiliary-classes/capture-vision-router-module.html)
- [`CLabelRecognizerModule`]({{ site.cpp_api }}label-recognizer-module.html)
- [`CCoreModule`]({{ site.dcv_ios_api }}core/basic-structures/core-module.html)
- [`CLicenseModule`]({{ site.dcv_ios_api }}license/license-module.html)
- [`CUtilityModule`]({{ site.dcv_ios_api }}utility/utility-module.html)
- [`CImageProcessingModule`]({{ site.dcv_ios_api }}image-processing/image-processing-module.html)

## Enumerations

- [`BufferOverflowProtectionMode`]({{ site.dcv_enumerations}}core/buffer-overflow-protection-mode.html?src=cpp&&lang=cpp)
- [`CapturedResultItemType`]({{ site.dcv_enumerations}}core/captured-result-item-type.html?src=cpp&&lang=cpp)
- [`ErrorCode`]({{ site.dcv_enumerations}}core/error-code.html?src=cpp&&lang=cpp)
- [`GrayscaleTransformationMode`]({{ site.dcv_enumerations}}core/grayscale-transformation-mode.html?src=cpp&&lang=cpp)
- [`ImageCaptureDistanceMode`]({{ site.dcv_enumerations}}core/image-capture-distance-mode.html?src=cpp&&lang=cpp)
- [`ImagePixelFormat`]({{ site.dcv_enumerations}}core/image-pixel-format.html?src=cpp&&lang=cpp)
- [`ImageSourceState`]({{ site.dcv_enumerations}}core/image-source-state.html?src=cpp&&lang=cpp)
- [`ImageTagType`]({{ site.dcv_enumerations}}core/image-tag-type.html?src=cpp&&lang=cpp)
- [`IntermediateResultUnitType`]({{ site.dcv_enumerations}}core/intermediate-result-unit-type.html?src=cpp&&lang=cpp)
- [`PDFReadingMode`]({{ site.dcv_enumerations}}core/pdf-reading-mode.html?src=cpp&&lang=cpp)
- [`RegionObjectElementType`]({{ site.dcv_enumerations}}core/region-object-element-type.html?src=cpp&&lang=cpp)
- [`SectionType`]({{ site.dcv_enumerations}}core/section-type.html?src=cpp&&lang=cpp)
- [`VideoFrameQuality`]({{ site.dcv_enumerations }}core/video-frame-quality.html?src=cpp&&lang=cpp)
- [`ColourChannelUsageType`]({{ site.dcv_enumerations}}core/colour-channel-usage-type.html?src=cpp&&lang=cpp)
- [`RasterDataSource`]({{ site.dcv_enumerations}}core/raster-data-source.html?src=cpp&&lang=cpp)
- [`TransformMatrixType`]({{ site.dcv_enumerations}}core/transform-matrix-type.html?src=cpp&&lang=cpp)
