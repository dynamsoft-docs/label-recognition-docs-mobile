---
layout: default-layout
title: RawTextLine - Dynamsoft Label Recognizer iOS Edition
description: The class RawTextLine of Dynamsoft Label Recognizer iOS edition represents a unit which holds the raw text lines.
keywords: raw text lines unit, intermediate result unit
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RawTextLine
---

# RawTextLine

The `RawTextLine` class represents a text line in an image. It can be in one of the following states:

- `TLS_LOCALIZED`: Localized but recognition not performed.
- `TLS_RECOGNITION_FAILED`: Recognition failed.
- `TLS_RECOGNIZED_SUCCESSFULLY`: Successfully recognized.

## Definition

*Namespace:* com.dynamsoft.dlr

*Assembly:* DynamsoftLabelRecognizer.aar

```java
class RawTextLine
```

## Methods

| Methods | Description |
| ------- | ----------- |
| [`getText`](#gettext) | Returns the recognized text. |
| [`setText`](#settext) | Sets the recognized text. |
| [`getConfidence`](#getconfidence) | Returns the confidence level of the recognized text. |
| [`getCharacterResults`](#getcharacterresults) | Returns all the characters contained by the textline. |
| [`getRowNumber`](#getrownumber) | Returns the row number of the text line within the image. |
| [`setRowNumber`](#setrownumber) | Sets the row number of the text line within the image. |
| [`getSpecificationName`](#getspecificationname) | Get the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |
| [`setSpecificationName`](#setspecificationname) | Sets the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`. |
| [`getLocation`](#getlocation) | Returns the location of the text line. |
| [`setLocation`](#setlocation) | Sets the location of the text line. |

### getText

Returns the recognized text.

```java
String getText();
```

**Return value**

Returns the text of the text line.

### setText

Returns the recognized text.

```java
void setText(string text);
```

**Parameter**

`text`: The text.

**Return value**

Returns the `ErrorCode` if failed. Otherwise, returns 0.

### getConfidence

Returns the confidence level of the recognized text.

```java
int getConfidence();
```

**Return value**

Returns the confidence level of the text line.

### getCharacterResults

Returns all the characters contained by the textline in an array of [`CharacterResult`](character-result.md).

```java
CharacterResult[] getCharacterResults();
```

**Return value**

Returns all the characters contained by the textline in an array of [`CharacterResult`](character-result.md).

### getRowNumber

Returns the row number of the text line within the image.

```java
int getRowNumber();
```

**Return value**

Returns the row number of the text line within the image.

### setRowNumber

Sets the row number of the text line within the image.

```java
int setRowNumber(int rowNumber);
```

**Parameter**

`rowNumber`: The row number of the text line within the image.

**Return value**

Returns 0 if success, otherwise an error code.

### getSpecificationName

Returns the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

```java
String getSpecificationName();
```

**Return value**

The name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

### setSpecificationName

Sets the name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

```java
int setSpecificationName(String specificationName);
```

**Parameter**

`specificationName`: The name of the [`TextLineSpecification`]({{site.dcv_parameter_reference}}text-line-specification/) object that generated this `TextLineResultItem`.

**Return value**

Returns 0 if success, otherwise an error code.

### getLocation

Returns a `Quadrilateral` object which represents the location of the text line.

```java
Quadrilateral getLocation();
```

**Return value**

A `Quadrilateral` object which represents the location of the text line.

### setLocation

Set the location of the text line.

```java
int setLocation(Quadrilateral location);
```

**Parameter**

`location`: The location of the text line.

**Return value**

Returns 0 if success, otherwise an error code.

### getStatus

Returns the status of the text line.

```java
RawTextLineStatus getStatus();
```

**Return value**

The status of the text line.
