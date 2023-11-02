---
layout: default-layout
title: CRecognizedTextLinesUnit - Dynamsoft Label Recognizer Android Edition
description: The class CRecognizedTextLinesUnit of Dynamsoft Label Recognizer represents an intermediate result unit containing recognized text lines.
keywords: Recognized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CRecognizedTextLinesUnit
permalink: /programming/android/api-reference/recognized-text-lines-unit.html
---

# CRecognizedTextLinesUnit

The `CRecognizedTextLinesUnit` class represents an intermediate result unit containing recognized text lines. It inherits from the `CIntermediateResultUnit` class.

## Definition

*Namespace:* com.dynamsoft.dlr::intermediate_results

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class CRecognizedTextLinesUnit : public CIntermediateResultUnit
```

*Inheritance:* [CIntermediateResultUnit]({{ site.dcv_cpp_api }}core/intermediate-results/intermediate-result-unit.html) -> CRecognizedTextLinesUnit


## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetCount`](#getcount) | Gets the number of recognized text lines in the unit.|
| [`GetRecognizedTextLine`](#getrecognizedtextline) | Gets a pointer to the CRecognizedTextLineElement object at the specified index. |

### GetCount

Gets the number of recognized text lines in the unit.

```java
virtual int GetCount() const = 0;
```

**Return value**

Returns the number of recognized text lines in the unit.

### GetRecognizedTextLine

Gets a pointer to the CRecognizedTextLineElement object at the specified index.

```java
virtual const CRecognizedTextLineElement* GetRecognizedTextLine(int index) const = 0;
```

**Parameters**

`[in] index` The index of the desired CRecognizedTextLineElement object.

**Return value**

Returns a pointer to the CRecognizedTextLineElement object at the specified index.
