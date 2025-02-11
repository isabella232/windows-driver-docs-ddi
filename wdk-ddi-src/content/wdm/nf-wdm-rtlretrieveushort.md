---
UID: NF:wdm.RtlRetrieveUshort
tech.root: 
title: RtlRetrieveUshort
ms.date: 07/16/2021
targetos: Windows
description: "Learn more about: RtlRetrieveUshort"
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wdm.h
req.idl: 
req.include-header: 
req.irql: Any level (see Remarks)
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - RtlRetrieveUshort
f1_keywords:
 - RtlRetrieveUshort
 - wdm/RtlRetrieveUshort
dev_langs:
 - c++
---

## -description

The **RtlRetrieveUshort** macro retrieves a USHORT value from the source address, avoiding alignment faults.

## -parameters

### -param DEST_ADDRESS

[out]
Pointer to a USHORT-aligned location in which to store the value.

### -param SRC_ADDRESS

[in]
Pointer to a location from which to retrieve the value.

## -remarks

Callers of **RtlRetrieveUshort** can be running at any IRQL if the given addresses are in nonpaged pool. Otherwise, the caller must be running at IRQL <= APC_LEVEL.
