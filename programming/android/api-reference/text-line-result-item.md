---
layout: default-layout
title: CTextLineResultItem - Dynamsoft Label Recognizer Android Edition
description: The class CTextLineResultItem of Dynamsoft Label Recognizer represents a text line result item recognized by a document layout analysis engine.
keywords: Text line result item
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CTextLineResultItem
permalink: /programming/android/api-reference/text-line-result-item.html
---

# CTextLineResultItem

The `CTextLineResultItem` class represents a text line result item recognized by the library. It is derived from `CCapturedResultItem`.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class CTextLineResultItem : public CCapturedResultItem
```

*Inheritance:* [CCapturedResultItem]({{ site.dcv_android_api }}core/basic-structures/captured-result-item.html) -> CTextLineResultItem

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`getText`](#gettext) | Gets the text content of the text line. |
| [`getLocation`](#getlocation) | Gets the location of the text line in the form of a quadrilateral. |
| [`getConfidence`](#getconfidence) | Gets the confidence of the text line recognition result. |
| [`GetCharacterResultsCount`](#getcharacterresultscount) | Gets the count of character results in the text line. |
| [`GetCharacterResult`](#getcharacterresult) | Gets the character result at the specified index. |
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Gets the rotation transform matrix of the text line. |

### GetText

It is used to get the text content of the text line.

```java
virtual const char* GetText() const = 0;
```

**Return value**

Returns the text content of the text line.

### GetLocation

It is used to get the location of the text line in the form of a quadrilateral.

```java
virtual CQuadrilateral GetLocation() const = 0;
```

**Return value**

Returns the location of the text line in the form of a quadrilateral.

### GetConfidence

It is used to get the confidence of the text line recognition result.

```java
virtual int GetConfidence() const = 0;
```

**Return value**

Returns the confidence of the text line recognition result.

### GetCharacterResultsCount

It is used to get the count of character results in the text line.

```java
virtual int GetCharacterResultsCount() const = 0;
```

**Return value**

Returns the count of character results in the text line.

### GetCharacterResult

It is used to get the character result at the specified index.

```java
virtual int GetCharacterResult(int index, CCharacterResult* charResult) const = 0;
```

**Parameters**

`[in] index` The index of the character result to get.

`[out] charResult` The character result at the specified index.

**Return value**

Returns 0 if successful, otherwise returns a non-zero error code.

### GetRotationTransformMatrix

It is used to get the rotation transform matrix of the text line.

```java
virtual void GetRotationTransformMatrix(double matrix[9]) const = 0;
```

**Parameters**

`[out] matrix` The rotation transform matrix of the text line.

**Return value**

None.
