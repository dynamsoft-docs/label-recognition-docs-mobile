---
layout: default-layout
title: RawTextLinesUnit - Dynamsoft Label Recognizer iOS Edition
description: The class RawTextLinesUnit of Dynamsoft Label Recognizer iOS edition represents a unit which holds the raw text lines.
keywords: raw text lines unit, intermediate result unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RawTextLinesUnit
---

# RawTextLinesUnit

The `RawTextLinesUnit` class represents a unit which holds the raw text lines.

## Definition

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftCaptureVisionBundle.aar

```java
class RawTextLine
```

*Inheritance:* [IntermediateResultUnit]({{ site.dcv_android_api }}core/intermediate-results/intermediate-result-unit.html) -> RecognizedTextLinesUnit

## Methods

| Method | Description |
| --- | --- |
| [`getCount`](#getcount) | Gets the number of raw text lines in the unit. |
| [`getRawTextLine`](#getrawtextline) | Gets a raw text line at the specified index. |
| [`getRawTextLines`](#getrawtextlines) | Gets all raw text lines of the unit. |
| [`removeAllRawTextLines`](#removeallrawtextlines) | Removes all raw text lines. |
| [`removeRawTextLine`](#removerawtextline) | Removes the raw text line at the specified index. |
| [`addRawTextLine`](#addrawtextline) | Adds a raw text line. |
| [`setRawTextLine`](#setrawtextline) | Sets the raw text line at the specified index. |

### getCount

Returns the number of raw text lines in the unit.

```java
int getCount();
```

**Return value**

Returns the number of raw text lines in the unit.

### getRawTextLine

Gets a raw text line at the specified index.

```java
RawTextLine getRawTextLine(int index);
```

**Parameters**

`index`: The index of the raw text line.

**Return value**

Returns a pointer to the [`RawTextLine`](raw-text-line.md) object at the specified index.

### getRawTextLines

Gets all raw text lines of the unit.

```java
RawTextLine[] getRawTextLines();
```

**Return value**

Returns all the [`RawTextLine`](raw-text-line.md) objects of the unit in an array.

### removeAllRawTextLines

Removes all raw text lines.

```java
void removeAllRawTextLines();
```

### removeRawTextLine

Removes the raw text line at the specified index.

```java
int removeRawTextLine(int index);
```

**Parameters**

`index`: The index of the raw text line to be removed.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addRawTextLine

Adds a raw text line to the unit.

```java
int addRawTextLine(RawTextLine textline, Matrix matrixToOriginalImage);
```

**Parameters**

`textline`: A [`RawTextLine`](raw-text-line.md) object as the raw text line to be added to the unit.

`matrixToOriginalImage`: The matrix to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setRawTextLine

Sets the raw text line at the specified index.

```java
int setRawTextLine(int index, RawTextLine textline, Matrix matrixToOriginalImage);
```

**Parameters**

`index`: The index of the raw text line to be set.

`textline`: A [`RawTextLine`](raw-text-line.md) object as the raw text line to be set.

`matrixToOriginalImage`: The matrix to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
