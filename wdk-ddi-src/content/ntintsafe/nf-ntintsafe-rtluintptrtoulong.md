---
UID: NF:ntintsafe.RtlUIntPtrToULong
title: RtlUIntPtrToULong function (ntintsafe.h)
description: Learn how this function converts a value of type UINT_PTR to a value of type LONG.
old-location: kernel\rtluintptrtoulong.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["RtlUIntPtrToULong function"]
ms.keywords: RtlUIntPtrToULong, RtlUIntPtrToULong function [Kernel-Mode Driver Architecture], kernel.rtluintptrtoulong, ntintsafe/RtlUIntPtrToULong
req.header: ntintsafe.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - RtlUIntPtrToULong
 - ntintsafe/RtlUIntPtrToULong
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntintsafe.h
api_name:
 - RtlUIntPtrToULong
---

# RtlUIntPtrToULong function


## -description

Converts a value of type <b>UINT_PTR</b> to a value of type <b>LONG</b>.

## -parameters

### -param uOperand 

[in]
The value to be converted.

### -param pulResult 

[out]
A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns STATUS_INTEGER_OVERFLOW and this parameter is not valid.

## -returns

Returns STATUS_SUCCESS if the operation is successful. 

See the implementation of this helper function in `ntintsafe.h` in the WDK for possible error return values. 

## -remarks

This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.

This function uses the following alternate name:

<ul>
<li>RtlUIntPtrToDWord
</li>
<li>RtlSizeTToULong
</li>
<li>RtlSizeTToDWord
</li>
</ul>

