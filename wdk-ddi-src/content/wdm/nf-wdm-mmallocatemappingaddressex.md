---
UID: NF:wdm.MmAllocateMappingAddressEx
title: MmAllocateMappingAddressEx function
description: The MmAllocateMappingAddressEx function allocates a system PTE mapping of the requested length that can be used later to map arbitrary addresses.
tech.root: kernel
ms.date: 03/01/2020
ms.keywords: MmAllocateMappingAddressEx
req.header: wdm.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: <=APC_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wdm.h
api_name:
 - MmAllocateMappingAddressEx
product:
 - Windows
f1_keywords:
 - MmAllocateMappingAddressEx
 - wdm/MmAllocateMappingAddressEx
---

# MmAllocateMappingAddressEx function

## -description

The **MmAllocateMappingAddressEx** function allocates a system PTE mapping of the requested length that can be used later to map arbitrary addresses.

## -parameters

### -param NumberOfBytes

Supplies the maximum number of bytes the mapping can span.

### -param PoolTag

Supplies a pool tag to associate this mapping to the caller.

### -param Flags

## -returns

Returns a virtual address where to use for later mappings.

## -remarks

## -see-also
