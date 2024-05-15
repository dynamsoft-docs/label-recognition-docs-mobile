---
layout: default-layout
title: LocalizedTextLinesUnit - Dynamsoft Label Recognizer Android Edition
description: The class LocalizedTextLinesUnit of Dynamsoft Label Recognizer Android edition represents a unit that contains localized text lines.
keywords: Localized text lines unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: LocalizedTextLinesUnit
permalink: /programming/android/api-reference/localized-text-lines-unit.html
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
| [`getLocalizedTextLine`](#getlocalizedtextlines) | Returns an array of `LocalizedTextLineElement` objects, each representing a localized text line. |
| [`getCount`](#getcount) | Returns the number of text lines that are localized from the image. |
| [`getLocalizedTextLine`](#getlocalizedtextline) | Returns the localized text line at the specified index in a [`LocalizedTextLineElement`](localized-text-line-element.md) object. |
| [`removeAllLocalizedTextLines`](#removealllocalizedtextlines) | Removes all the localized text lines from the unit. |
| [`removeLocalizedTextLine`](#removelocalizedtextline) | Removes a localized text line from the unit. |
| [`addLocalizedTextLine`](#addlocalizedtextline) | Adds a [`LocalizedTextLineElement`](localized-text-line-element.md) to the unit. |
| [`setLocalizedTextLine`](#setlocalizedtextline) | Sets the [`LocalizedTextLineElement`](localized-text-line-element.md) at the specified index. |

### getLocalizedTextLines

Returns an array of [`LocalizedTextLineElement`](localized-text-line-element.md) objects, each representing a localized text line.

```java
LocalizedTextLineElement[] getLocalizedTextLines();
```

**Return value**

Returns an array of [`LocalizedTextLineElement`](localized-text-line-element.md), which is the basic unit of the localized text line result.

### getCount

Returns the number of [`LocalizedTextLineElement`](localized-text-line-element.md) objects from the image.

```java
int getCount();
```

**Return value**

Returns the number of text lines that are localized from the image.

### getLocalizedTextLine

Returns the localized text line at the specified index in a [`LocalizedTextLineElement`](localized-text-line-element.md) object.

```java
LocalizedTextLineElement getLocalizedTextLine(int index);
```

**Parameters**

`index`: The index of the [`LocalizedTextLineElement`](localized-text-line-element.md) to be retrieved.

### removeAllLocalizedTextLines

Removes all the [`LocalizedTextLineElement`](localized-text-line-element.md) objects from the unit.

```java
void removeAllLocalizedTextLines();
```

### removeLocalizedTextLine

Removes a [`LocalizedTextLineElement`](localized-text-line-element.md) from the unit.

```java
int removeLocalizedTextLine(int index);
```

**Parameters**

`index`: The index of the [`LocalizedTextLineElement`](localized-text-line-element.md) to be removed.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### addLocalizedTextLine

Adds a [`LocalizedTextLineElement`](localized-text-line-element.md) to the unit.

```java
int addLocalizedTextLine(LocalizedTextLineElement element, Matrix matrixToOriginalImage); 
```

**Parameters**

`element`: A [`LocalizedTextLineElement`](localized-text-line-element.md) object as the localized text line to be added to the unit.

`matrixToOriginalImage`: The matrix to convert the coordinates of the localized text line to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### setLocalizedTextLine

Sets the [`LocalizedTextLineElement`](localized-text-line-element.md) at the specified index.

```java
int setLocalizedTextLine(int index, LocalizedTextLineElement element, Matrix matrixToOriginalImage); 
```

**Parameters**

`index`: The index of the localized text line to be set.

`element`:  A [`LocalizedTextLineElement`](localized-text-line-element.md) object as the localized text line to be set.

`matrixToOriginalImage`: The matrix to convert the coordinates of the localized text line to the original image.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.
