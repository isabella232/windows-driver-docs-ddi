---
UID: NF:miniport.WRITE_PORT_UCHAR
title: WRITE_PORT_UCHAR function (miniport.h)
description: The WRITE_PORT_UCHAR function (miniport.h) writes a byte to the specified port address in resident, mapped device memory.
old-location: kernel\write_port_uchar.htm
tech.root: kernel
ms.date: 04/30/2018
keywords: ["WRITE_PORT_UCHAR function"]
ms.keywords: WRITE_PORT_UCHAR, WRITE_PORT_UCHAR routine [Kernel-Mode Driver Architecture], k103_1495098b-03fb-4677-ac5a-2a1de9223f8b.xml, kernel.write_port_uchar, wdm/WRITE_PORT_UCHAR
req.header: miniport.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h, Ioaccess.h, Miniport.h
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
req.lib: Hal.lib
req.dll: 
req.irql: Any level (see Remarks section)
targetos: Windows
req.typenames: 
f1_keywords:
 - WRITE_PORT_UCHAR
 - miniport/WRITE_PORT_UCHAR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Hal.lib
 - Hal.dll
api_name:
 - WRITE_PORT_UCHAR
---

# WRITE_PORT_UCHAR function (miniport.h)


## -description

The <b>WRITE_PORT_UCHAR</b> routine writes a byte to the specified port address.

## -parameters

#### - Port [in]

Pointer to the port, which must be a mapped memory range in I/O space.


#### - Value [in]

Specifies a byte to be written to the port.

## -remarks

Callers of <b>WRITE_PORT_UCHAR</b> can be running at any IRQL, assuming the <i>Port</i> is resident, mapped device memory.

