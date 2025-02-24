---
UID: NS:wdm._PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
title: _PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY (wdm.h)
description: The _PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY structure (wdm.h) describes a PCI Express (PCIe) secondary uncorrectable error severity register.
old-location: pci\pci_express_sec_uncorrectable_error_severity.htm
tech.root: PCI
ms.date: 02/24/2018
keywords: ["PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY structure"]
ms.keywords: "*PPCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY, PCI.pci_express_sec_uncorrectable_error_severity, PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY, PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY union [Buses], PPCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY, PPCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY union pointer [Buses], _PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY, pci_struct_94eb07f5-9b90-414b-a331-075c61f507a4.xml, wdm/PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY, wdm/PPCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY"
req.header: wdm.h
req.include-header: Ntddk.h, Wdm.h, Miniport.h
req.target-type: Windows
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
req.irql: PASSIVE_LEVEL (see Remarks section)
targetos: Windows
req.typenames: PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY, *PPCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
req.product: Windows 10 or later.
f1_keywords:
 - _PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
 - wdm/_PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
 - PPCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
 - wdm/PPCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
 - PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
 - wdm/PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wdm.h
api_name:
 - _PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
 - PPCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
 - PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY
---

# _PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY structure (wdm.h)


## -description

The PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY structure describes a PCI Express (PCIe) secondary uncorrectable error severity register of a PCIe advanced error reporting capability structure.

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field AsULONG

A ULONG representation of the contents of the PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_STATUS structure.


#### - DelayedTransactionDiscardTimerExpired

A single bit that indicates that an expiration of the delayed transaction discard timer is a fatal error.


#### - InternalBridgeError

A single bit that indicates that a reported internal bridge error is a fatal error.


#### - MasterAbortOnSplitCompletion

A single bit that indicates that a reported master abort on split completion is a fatal error.


#### - PERRAsserted

A single bit that indicates that a reported PERR# assertion is a fatal error.


#### - ReceivedMasterAbort

A single bit that indicates that a reported master abort is a fatal error.


#### - ReceivedTargetAbort

A single bit that indicates that a reported target abort is a fatal error.


#### - Reserved

Reserved for system use.


#### - RsvdZ

Reserved for system use.


#### - SERRAsserted

A single bit that indicates that a reported SERR# assertion is a fatal error.


#### - TargetAbortOnSplitCompletion

A single bit that indicates that a reported target abort on split completion is a fatal error.


#### - UncorrectableAddressError

A single bit that indicates that a reported uncorrectable address error is a fatal error.


#### - UncorrectableAttributeError

A single bit that indicates that a reported uncorrectable attribute error is a fatal error.


#### - UncorrectableDataError

A single bit that indicates that a reported uncorrectable data error is a fatal error.


#### - UncorrectableSplitCompletion

A single bit that indicates that a reported uncorrectable split completion message data error is a fatal error.


#### - UnexpectedSplitCompletionError

A single bit that indicates that a reported unexpected split completion error is a fatal error.

## -syntax

```cpp
typedef union _PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY {
  struct {
    ULONG TargetAbortOnSplitCompletion  :1;
    ULONG MasterAbortOnSplitCompletion  :1;
    ULONG ReceivedTargetAbort  :1;
    ULONG ReceivedMasterAbort  :1;
    ULONG RsvdZ  :1;
    ULONG UnexpectedSplitCompletionError  :1;
    ULONG UncorrectableSplitCompletion  :1;
    ULONG UncorrectableDataError  :1;
    ULONG UncorrectableAttributeError  :1;
    ULONG UncorrectableAddressError  :1;
    ULONG DelayedTransactionDiscardTimerExpired  :1;
    ULONG PERRAsserted  :1;
    ULONG SERRAsserted  :1;
    ULONG InternalBridgeError  :1;
    ULONG Reserved  :18;
  };
  ULONG  AsULONG;
} PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY, *PPCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY;
```

## -remarks

The PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY structure is available in Windows Server 2008 and later versions of Windows.

A PCI_EXPRESS_SEC_UNCORRECTABLE_ERROR_SEVERITY structure is contained in the <a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_bridge_aer_capability">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a> structure.

## -see-also

<a href="/windows-hardware/drivers/ddi/wdm/ns-wdm-_pci_express_bridge_aer_capability">PCI_EXPRESS_BRIDGE_AER_CAPABILITY</a>

