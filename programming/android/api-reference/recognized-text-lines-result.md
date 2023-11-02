---
layout: default-layout
title: CRecognizedTextLinesResult - Dynamsoft Label Recognizer Android Edition
description: The class CRecognizedTextLinesResult of Dynamsoft Label Recognizer represents the result of a text recognition process.
keywords: Recognized text lines result
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: CRecognizedTextLinesResult
permalink: /programming/android/api-reference/recognized-text-lines-result.html
---

# CRecognizedTextLinesResult

The `CRecognizedTextLinesResult` class represents the result of a text recognition process. It provides access to information about the recognized text lines, the original image, and any errors that occurred during the recognition process.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class CRecognizedTextLinesResult
```

## Methods Summary

| Method               | Description |
|----------------------|-------------|
| [`GetOriginalImageHashId`](#getoriginalimagehashid) | Gets the hash ID of the original image. |
| [`GetOriginalImageTag`](#getoriginalimagetag) | Gets the tag of the original image. |
| [`GetItemsCount`](#getitemscount) | Gets the number of text line result items in the recognition result. |
| [`GetItem`](#getitem) | Gets the text line result item at the specified index. |
| [`HasItem`](#hasitem) | Check if the item is present in the array.|
| [`RemoveItem`](#removeitem) | Remove a specific item from the array in the recognition result.|
| [`GetRotationTransformMatrix`](#getrotationtransformmatrix) | Get the rotation transformation matrix of the original image relative to the rotated image.|
| [`GetErrorCode`](#geterrorcode) | Gets the error code of the recognition result, if an error occurred. |
| [`GetErrorString`](#geterrorstring) | Gets the error message of the recognition result, if an error occurred. |

### GetOriginalImageHashId

Gets the hash ID of the original image.

```java
virtual const char* GetOriginalImageHashId() const = 0;
```

**Return value**

Returns a pointer to a null-terminated string containing the hash ID of the original image.

### GetOriginalImageTag

Gets the tag of the original image.

```java
virtual const CImageTag* GetOriginalImageTag() const = 0;
```

**Return value**

Returns a pointer to a CImageTag object representing the tag of the original image.

### GetItemsCount

Gets the number of text line result items in the recognition result.

```java
virtual int GetItemsCount() const = 0;
```

**Return value**

Returns the number of text line result items in the recognition result.

### GetItem

Gets the text line result item at the specified index.

```java
virtual const CTextLineResultItem* GetItem(int index) const = 0;
```

**Parameters**

`[in] index` The zero-based index of the text line result item to retrieve.

**Return value**

Returns a pointer to the CTextLineResultItem object at the specified index.

### HasItem

Check if the item is present in the array.

```java
bool HasItem(const CTextLineResultItem* item) const
```

**Parameters**

`[in] item` The specific item to check.

**Return value**

Returns a bool value indicating whether the item is present in the array or not.

### RemoveItem

Remove a specific item from the array in the recognition result.

```java
int RemoveItem(const CTextLineResultItem* item)
```

**Parameters**

`[in] item` The specific item to remove.

**Return value**

Return value indicating whether the deletion was successful or not.

### GetRotationTransformMatrix

Get the rotation transformation matrix of the original image relative to the rotated image.

```java
void GetRotationTransformMatrix(double matrix[9]) const;
```

**Parameters**

`[out] matrix` A double array which represents the rotation transform matrix.


### GetErrorCode

Gets the error code of the recognition result, if an error occurred.

```java
virtual int GetErrorCode() const = 0;
```

**Return value**

Returns the error code of the recognition result, or 0 if no error occurred.

### GetErrorString

Gets the error message of the recognition result, if an error occurred.

```java
virtual const char* GetErrorString() const = 0;
```

**Return value**

Returns a pointer to a null-terminated string containing the error message of the recognition result, or a pointer to an empty string if no error occurred.
