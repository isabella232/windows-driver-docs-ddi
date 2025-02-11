---
UID: NF:miniport.InterlockedOr
title: InterlockedOr function (miniport.h)
description: The InterlockedOr function (miniport.h) atomically computes a bitwise OR operation with the specified variable and specified value.
old-location: kernel\interlockedor.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["InterlockedOr function"]
ms.keywords: InterlockedOr, InterlockedOr routine [Kernel-Mode Driver Architecture], k102_05d8ca48-ab6f-46ae-b026-cb2aaf6f37aa.xml, kernel.interlockedor, wdm/InterlockedOr
req.header: miniport.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Miniport.h
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
req.irql: Any level
targetos: Windows
req.typenames: 
f1_keywords:
 - InterlockedOr
 - miniport/InterlockedOr
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - InterlockedOr
---

# InterlockedOr function (miniport.h)


## -description

The <b>InterlockedOr</b> routine atomically computes a bitwise OR operation.

## -parameters

### -param Destination 

[in, out]
A pointer to the variable to be ORed with <i>Value</i>. The result of the operation is stored in the variable.

### -param Value 

[in]
Specifies the value to be ORed with the variable that is pointed to by <i>Destination</i>.

## -returns

<b>InterlockedOr</b> returns the original value stored in the variable pointed to by <i>Destination</i>.

## -remarks

<b>InterlockedOr</b> atomically computes <b>*</b><i>Destination</i><b>|=</b><i>Value</i>. 

Interlocked operations cannot be used on non-cached memory.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedand">InterlockedAnd</a>



<a href="/windows-hardware/drivers/ddi/wdm/nf-wdm-interlockedxor">InterlockedXor</a>
