---
UID: NF:ioaccess.WRITE_REGISTER_USHORT~r2
title: WRITE_REGISTER_USHORT function (ioaccess.h)
description: The WRITE_REGISTER_USHORT function (ioaccess.h) writes a USHORT value to the specified register address in resident, mapped device memory.
old-location: kernel\write_register_ushort.htm
tech.root: kernel
ms.date: 03/01/2018
keywords: ["WRITE_REGISTER_USHORT function"]
ms.keywords: WRITE_REGISTER_USHORT, WRITE_REGISTER_USHORT routine [Kernel-Mode Driver Architecture], k103_bc20d667-b3c7-4e46-a21d-06123e73d348.xml, kernel.write_register_ushort, wdm/WRITE_REGISTER_USHORT
req.header: ioaccess.h
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
req.typenames: IDD_DRIVER_GLOBALS, *PIDD_DRIVER_GLOBALS, IDD_DRIVER_GLOBALS, *PIDD_DRIVER_GLOBALS
f1_keywords:
 - WRITE_REGISTER_USHORT
 - ioaccess/WRITE_REGISTER_USHORT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NtosKrnl.exe
api_name:
 - WRITE_REGISTER_USHORT
---

# WRITE_REGISTER_USHORT function


## -description

The <b>WRITE_REGISTER_USHORT</b> routine writes a USHORT value to the specified address.

## -parameters

### -param Register 

[in]
Pointer to the register, which must be a mapped range in memory space.

### -param Value 

[in]
Specifies a USHORT value to be written to the register.

## -syntax

```cpp
VOID WRITE_REGISTER_USHORT(
  _In_ PUSHORT Register,
  _In_ USHORT  Value
);
```

## -remarks

Callers of <b>WRITE_REGISTER_USHORT</b> can be running at any IRQL, assuming the <i>Register</i> is resident, mapped device memory.

