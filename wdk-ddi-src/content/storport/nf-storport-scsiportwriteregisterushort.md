---
UID: NF:storport.ScsiPortWriteRegisterUshort
title: ScsiPortWriteRegisterUshort macro (storport.h)
description: Learn how the ScsiPortWriteRegisterUshort routine transfers a USHORT value to the HBA.Note  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future.
old-location: storage\scsiportwriteregisterushort.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["ScsiPortWriteRegisterUshort macro"]
ms.keywords: ScsiPortWriteRegisterUshort, ScsiPortWriteRegisterUshort routine [Storage Devices], scsiprt_550ba014-1ffa-496f-8cea-009f234fa8e4.xml, srb/ScsiPortWriteRegisterUshort, storage.scsiportwriteregisterushort
req.header: storport.h
req.include-header: Miniport.h, Scsi.h, Storport.h
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
req.lib: Scsiport.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - ScsiPortWriteRegisterUshort
 - storport/ScsiPortWriteRegisterUshort
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Scsiport.lib
 - Scsiport.dll
api_name:
 - ScsiPortWriteRegisterUshort
---

# ScsiPortWriteRegisterUshort macro


## -description

The <b>ScsiPortWriteRegisterUshort</b> routine transfers a USHORT value to the HBA.
<div class="alert"><b>Note</b>  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future. Instead, we recommend using the <a href="/windows-hardware/drivers/storage/storport-driver">Storport driver</a> and <a href="/windows-hardware/drivers/storage/storport-miniport-drivers">Storport miniport</a> driver models.</div><div> </div>

## -parameters

### -param Register 

[in]
Pointer to the register. The given <i>Register</i> must be in a mapped memory-space range returned by <b>ScsiPortGetDeviceBase</b>.

### -param Value 

[in]
Specifies the value to be written to the HBA's register.

## -see-also

<a href="/windows-hardware/drivers/ddi/srb/nf-srb-scsiportgetdevicebase">ScsiPortGetDeviceBase</a>
