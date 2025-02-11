---
UID: NS:ucmucsispec._UCSI_SET_NOTIFICATION_ENABLE_COMMAND
title: _UCSI_SET_NOTIFICATION_ENABLE_COMMAND (ucmucsispec.h)
description: Learn how UCSI_SET_NOTIFICATION_ENABLE_COMMAND is used in the SET_NOTIFICATION_ENABLE command. See Table 4-9.
tech.root: usbref
ms.date: 09/30/2018
keywords: ["UCSI_SET_NOTIFICATION_ENABLE_COMMAND structure"]
ms.keywords: _UCSI_SET_NOTIFICATION_ENABLE_COMMAND, UCSI_SET_NOTIFICATION_ENABLE_COMMAND, *PUCSI_SET_NOTIFICATION_ENABLE_COMMAND,
req.header: ucmucsispec.h
req.include-header: UcmUcsiCx.h
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.27
req.umdf-ver: N/A
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: UCSI_SET_NOTIFICATION_ENABLE_COMMAND, *PUCSI_SET_NOTIFICATION_ENABLE_COMMAND
targetos: Windows
ms.custom: RS5
f1_keywords:
 - _UCSI_SET_NOTIFICATION_ENABLE_COMMAND
 - ucmucsispec/_UCSI_SET_NOTIFICATION_ENABLE_COMMAND
 - PUCSI_SET_NOTIFICATION_ENABLE_COMMAND
 - ucmucsispec/PUCSI_SET_NOTIFICATION_ENABLE_COMMAND
 - UCSI_SET_NOTIFICATION_ENABLE_COMMAND
 - ucmucsispec/UCSI_SET_NOTIFICATION_ENABLE_COMMAND
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ucmucsispec.h
api_name:
 - _UCSI_SET_NOTIFICATION_ENABLE_COMMAND
 - PUCSI_SET_NOTIFICATION_ENABLE_COMMAND
 - UCSI_SET_NOTIFICATION_ENABLE_COMMAND
---

# _UCSI_SET_NOTIFICATION_ENABLE_COMMAND structure


## -description

Used in the SET_NOTIFICATION_ENABLE command. See Table 4-9 in [UCSI spec version 1.1](https://www.intel.com/content/dam/www/public/us/en/documents/technical-specifications/usb-type-c-ucsi-spec.pdf).

## -struct-fields

### -field AsUInt64

### -field Command

### -field DataLength

### -field NotificationEnable

### -field CommandCompleteNotificationEnable

### -field ExternalSupplyChangeNotificationEnable

### -field PowerOperationModeChangeNotificationEnable

### -field SupportedProviderCapabilitiesChangeNotificationEnable

### -field NegotiatedPowerLevelChangeNotificationEnable

### -field PdResetNotificationEnable

### -field SupportedCamChangeNotificationEnable

### -field BatteryChargingStatusChangeNotificationEnable

### -field DataRoleSwapCompletedNotificationEnable

### -field PowerRoleSwapCompletedNotificationEnable

### -field ConnectChangeNotificationEnable

### -field ErrorNotificationEnable

## -remarks

## -see-also

