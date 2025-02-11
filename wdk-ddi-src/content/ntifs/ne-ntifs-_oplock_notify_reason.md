---
UID: NE:ntifs.__unnamed_enum_3
title: _OPLOCK_NOTIFY_REASON (ntifs.h)
description: OPLOCK_NOTIFY_REASON specifies the reason for calling the notification callback provided to FsRtlCheckOplockEx2.
tech.root: ifsk
ms.date: 03/24/2020
ms.keywords: _OPLOCK_NOTIFY_REASON, OPLOCK_NOTIFY_REASON,
req.header: ntifs.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: OPLOCK_NOTIFY_REASON, *POPLOCK_NOTIFY_REASON
targetos: Windows
ms.custom: 
f1_keywords:
 - OPLOCK_NOTIFY_REASON
 - ntifs/OPLOCK_NOTIFY_REASON
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ntifs.h
api_name:
 - OPLOCK_NOTIFY_REASON
dev_langs:
 - c++
---

# _OPLOCK_NOTIFY_REASON enumeration


## -description

OPLOCK_NOTIFY_REASON specifies the reason for calling the notification callback provided to [**FsRtlCheckOplockEx2**](nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlcheckoplockex2.md).

## -enum-fields

### -field OPLOCK_NOTIFY_BREAK_WAIT_INTERIM_TIMEOUT

The first blocking wait for an opportunistic lock (oplock) break timed out.

### -field OPLOCK_NOTIFY_BREAK_WAIT_TERMINATED

The wait for an oplock break is completed, successfully or otherwise. If successful, the *Status* field of [OPLOCK_NOTIFY_PARAMS](ns-ntifs-_oplock_notify_params.md) is STATUS_SUCCESS; otherwise, *Status* is set to indicate the reason for the termination.

## -remarks

The OPLOCK_NOTIFY_REASON is specified in the *NotifyReason* member of the OPLOCK_NOTIFY_PARAMS structure.

## -see-also

[**FsRtlCheckOplockEx2**](nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlcheckoplockex2.md)

[OPLOCK_NOTIFY_PARAMS](ns-ntifs-_oplock_notify_params.md)

