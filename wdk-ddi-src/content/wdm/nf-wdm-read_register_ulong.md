---
UID: NF:wdm.READ_REGISTER_ULONG
title: READ_REGISTER_ULONG function (wdm.h)
description: The READ_REGISTER_ULONG function (wdm.h) returns a ULONG value read from the specified register address in resident, mapped device memory.
old-location: kernel\read_register_ulong.htm
tech.root: kernel
ms.date: 09/07/2021
keywords: ["READ_REGISTER_ULONG function"]
ms.keywords: READ_REGISTER_ULONG, READ_REGISTER_ULONG routine [Kernel-Mode Driver Architecture], k103_c2da9866-18ac-438b-aa32-991d1bda139f.xml, kernel.read_register_ulong, wdm/READ_REGISTER_ULONG
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Ioaccess.h, Miniport.h, Wudfwdm.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: Any level (see Remarks section)
targetos: Windows
req.typenames: 
f1_keywords:
 - READ_REGISTER_ULONG
 - wdm/READ_REGISTER_ULONG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - READ_REGISTER_ULONG
---

# READ_REGISTER_ULONG function (wdm.h)


## -description

The **READ_REGISTER_ULONG** routine dereferences the supplied pointer, inserts a memory barrier, and reads a ULONG value from the specified register address.

## -parameters

#### - Register [in]

Pointer to the register address, which must be a mapped range in memory space.

## -returns

<b>READ_REGISTER_ULONG</b> returns the ULONG value read from the specified register address.

## -remarks

This routine inserts a memory barrier into your code. This barrier guarantees that every operation that appears in the source code before the call to this routine will complete before any operation that appears after the call.

For more info about memory barriers, see [**KeMemoryBarrier**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kememorybarrier).

Callers of <b>READ_REGISTER_ULONG</b> can be running at any IRQL, assuming the <i>Register</i> is resident, mapped device memory.

