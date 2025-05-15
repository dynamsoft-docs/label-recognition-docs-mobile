---
layout: default-layout
title: LocalizedTextLineElement - Dynamsoft Label Recognizer Android Edition
description: The class LocalizedTextLineElement of Dynamsoft Label Recognizer Android edition represents a localized text line element.
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

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class LocalizedTextLineElement extends RegionObjectElement
```

*Inheritance:* [RegionObjectElement]({{ site.dcv_android_api }}core/intermediate-results/region-object-element.html) -> LocalizedTextLineElement

## Methods

| Method | Description |
| ------ | ----------- |
| [`getCharacterQuads`](#getcharacterquads) | Returns the `Quadrilaterals` for each character in the text line. |
| [`getRowNumber`](#getrownumber) | Returns the row number of the text line, starting from 1. |

The following methods are inherited from the `RegionObjectElement` class:

| Method | Description |
|------- |-------------|
| [`getLocation`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html#getlocation) | Returns the location of the region object, represented as a quadrilateral. |
| [`setLocation`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html#setlocation) | Sets the location of the region object. |
| [`getReferencedElement`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html#getreferencedelement) | Returns the referenced element that supports the capturing of this element. |
| [`getRegionObjectElementType`]({{ site.dcv_ios_api }}core/intermediate-results/region-object-element.html#getregionobjectelementtype) | Returns the type of the region object element, defined by the enumeration [`DSRegionObjectElementType`]({{ site.dcv_enumerations }}core/region-object-element-type.html?lang=objc,swift). |



### getCharacterQuads

Returns the `Quadrilaterals` for each character in the text line.

```java
Quadrilateral[] getCharacterQuads()
```

**Return value**

The `Quadrilaterals` for each character in the text line.

### getRowNumber

Returns the row number of the text line, starting from 1.

```java
int getRowNumber()
```

**Return value**

The row number of the text line.
