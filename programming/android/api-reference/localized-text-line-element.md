---
layout: default-layout
title: LocalizedTextLineElement - Dynamsoft Label Recognizer Android Edition
description: The class LocalizedTextLineElement of Dynamsoft Label Recognizer represents a localized text line element.
keywords: Localized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: LocalizedTextLineElement
permalink: /programming/android/api-reference/localized-text-line-element.html
---

# LocalizedTextLineElement

The `LocalizedTextLineElement` class represents a localized text line element. It inherits from the `RegionObjectElement` class.

## Definition

*Namespace:* com.dynamsoft.dlr.intermediate_results

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class LocalizedTextLineElement extends RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html) -> LocalizedTextLineElement

## Methods Summary

| Method | Description |
| ------ | ----------- |
| [`getCharacterQuads`](#getcharacterquads) | Gets the quadrilaterals of all characters in the text line. |
| [`getRowNumber`](#getrownumber) | Gets the row number of the text line. |

### getCharacterQuads

Gets the quadrilaterals of all characters in the text line.

```java
Quadrilateral[] getCharacterQuads()
```

**Return value**

Returns an array of quadrilaterals.

### getRowNumber

Gets the row number of the text line.

```java
int getRowNumber()
```

**Return value**

Returns the row number of the text line.
