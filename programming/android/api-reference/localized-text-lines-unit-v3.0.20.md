---
layout: default-layout
title: LocalizedTextLinesUnit - Dynamsoft Label Recognizer Android Edition
description: The class LocalizedTextLinesUnit of Dynamsoft Label Recognizer Android edition represents a unit that contains localized text lines.
keywords: Localized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: LocalizedTextLinesUnit
permalink: /programming/android/api-reference/localized-text-lines-unit-v3.0.20.html
---

# LocalizedTextLinesUnit

The `LocalizedTextLinesUnit` class represents a unit that contains localized text lines. It inherits from the [IntermediateResultUnit]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html) class.

## Definition

*Namespace:* com.dynamsoft.dlr.intermediate_results

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class LocalizedTextLinesUnit extends IntermediateResultUnit
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html) -> LocalizedTextLinesUnit

## Methods

| Method | Description |
| ------ | ----------- |
| [`getLocalizedTextLine`](#getlocalizedtextlines) | Gets a pointer to a specific localized text line element. |

### getLocalizedTextLines

Gets all the text lines that are localized from the image.

```java
LocalizedTextLineElement[] getLocalizedTextLines();
```

**Return value**

Returns an array of [`LocalizedTextLineElement`](localized-text-line-element.md), which is the basic unit of the localized text line result.
