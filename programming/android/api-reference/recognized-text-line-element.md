---
layout: default-layout
title: CRecognizedTextLineElement - Dynamsoft Label Recognizer Android Edition
description: The class CRecognizedTextLineElement of Dynamsoft Label Recognizer represents a line of recognized text in an image.
keywords: Recognized text line element
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CRecognizedTextLineElement
permalink: /programming/android/api-reference/recognized-text-line-element.html
---

# CRecognizedTextLineElement

The `CRecognizedTextLineElement` class represents a line of recognized text in an image. It inherits from the `CRegionObjectElement` class.

## Definition

*Namespace:* com.dynamsoft.dlr::intermediate_results

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class CRecognizedTextLineElement : public CRegionObjectElement
```

*Inheritance:* [CRegionObjectElement]({{ site.dcv_cpp_api }}core/intermediate-results/region-object-element.html) -> CRecognizedTextLineElement

## Methods

| Method               | Description |
|----------------------|-------------|
| [`GetText`](#gettext) | Gets the recognized text. |
| [`GetConfidence`](#getconfidence) | Gets the confidence level of the recognized text. |
| [`GetCharacterResultsCount`](#getcharacterresultscount) | Gets the number of individual character recognition results in the line. |
| [`GetCharacterResult`](#getcharacterresult) | Gets the character recognition result at the specified index. |
| [`GetRowNumber`](#getrownumber) | Gets the row number of the text line within the image. |

### GetText

Gets the recognized text.

```java
virtual const char* GetText() const = 0;
```

**Return value**

Returns a pointer to the recognized text.

### GetConfidence

Gets the confidence level of the recognized text.

```java
virtual int GetConfidence() const = 0;
```

**Return value**

Returns an integer value representing the confidence level of the recognized text.

### GetCharacterResultsCount

Gets the number of individual character recognition results in the line.

```java
virtual int GetCharacterResultsCount() const = 0;
```

**Return value**

Returns an integer value representing the number of individual character recognition results.

### GetCharacterResult

Gets the character recognition result at the specified index.

```java
virtual int GetCharacterResult(int index, CCharacterResult* charResult) const = 0;
```

**Parameters**

`[in] index` The index of the character recognition result to retrieve.<br>
`[out] charResult` A pointer to a CCharacterResult object to store the result in.

**Return value**

Returns an integer value representing the success of the operation. Zero indicates success, while any other value indicates failure.

### GetRowNumber

Gets the row number of the text line within the image.

```java
virtual int GetRowNumber() const = 0;
```

**Return value**

Returns an integer value representing the row number of the text line within the image.
