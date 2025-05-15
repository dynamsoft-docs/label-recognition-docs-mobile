---
layout: default-layout
title: RawTextLineStatus - Dynamsoft LabelRecognizer Enumerations
description: The enumeration RawTextLineStatus of Dynamsoft LabelRecognizer describes the final status of a raw text line.
keywords: Raw Text Line Status
needGenerateH3Content: true
needAutoGenerateSidebar: true
noTitleIndex: true
breadcrumbText: RawTextLineStatus
codeAutoHeight: true
---

# Enumeration RawTextLineStatus

`RawTextLineStatus` enumerates the final status of a raw text line.

```java
@IntDef({})
@Retention(RetentionPolicy.CLASS)
public @interface EnumRawTextLineStatus {
    /** Localized but recognition not performed. */
    public static final int RTLS_LOCALIZED = 0;
    /** Recognition failed. */
    public static final int RTLS_RECOGNITION_FAILED = 1;
    /** Successfully recognized. */
    public static final int RTLS_RECOGNITION_SUCCEEDED = 2;
} EnumRawTextLineStatus;
```
