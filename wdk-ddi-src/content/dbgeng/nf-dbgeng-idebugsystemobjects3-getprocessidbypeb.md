---
UID: NF:dbgeng.IDebugSystemObjects3.GetProcessIdByPeb
title: IDebugSystemObjects3::GetProcessIdByPeb (dbgeng.h)
description: "The IDebugSystemObjects3::GetProcessIdByPeb method returns the engine process ID for the specified process."
old-location: debugger\getprocessidbypeb.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugSystemObjects3::GetProcessIdByPeb"]
ms.keywords: GetProcessIdByPeb, GetProcessIdByPeb method [Windows Debugging], GetProcessIdByPeb method [Windows Debugging],IDebugSystemObjects interface, GetProcessIdByPeb method [Windows Debugging],IDebugSystemObjects2 interface, GetProcessIdByPeb method [Windows Debugging],IDebugSystemObjects3 interface, GetProcessIdByPeb method [Windows Debugging],IDebugSystemObjects4 interface, IDebugSystemObjects interface [Windows Debugging],GetProcessIdByPeb method, IDebugSystemObjects2 interface [Windows Debugging],GetProcessIdByPeb method, IDebugSystemObjects2::GetProcessIdByPeb, IDebugSystemObjects3 interface [Windows Debugging],GetProcessIdByPeb method, IDebugSystemObjects3.GetProcessIdByPeb, IDebugSystemObjects3::GetProcessIdByPeb, IDebugSystemObjects4 interface [Windows Debugging],GetProcessIdByPeb method, IDebugSystemObjects4::GetProcessIdByPeb, IDebugSystemObjects::GetProcessIdByPeb, IDebugSystemObjects_f5f2396d-d537-40a0-987d-314a9dfb01ff.xml, dbgeng/IDebugSystemObjects2::GetProcessIdByPeb, dbgeng/IDebugSystemObjects3::GetProcessIdByPeb, dbgeng/IDebugSystemObjects4::GetProcessIdByPeb, dbgeng/IDebugSystemObjects::GetProcessIdByPeb, debugger.getprocessidbypeb
req.header: dbgeng.h
req.include-header: Dbgeng.h
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
req.irql: 
targetos: Windows
req.typenames: 
f1_keywords:
 - IDebugSystemObjects3::GetProcessIdByPeb
 - dbgeng/IDebugSystemObjects3::GetProcessIdByPeb
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugSystemObjects3::GetProcessIdByPeb
---

# IDebugSystemObjects3::GetProcessIdByPeb


## -description

The <b>GetProcessIdByPeb</b> method returns the engine process ID for the specified process.  The process is specified by its process environment block (PEB).

## -parameters

### -param Offset 

[in]
Specifies the location in the target's virtual address space of the PEB of the process whose process ID is requested.

### -param Id 

[out]
Receives the engine process ID.

## -returns

This method may also return other error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The target is a kernel-mode target.  This method is currently not available in kernel-mode debugging.

</td>
</tr>
</table>

## -remarks

This method is not available in kernel-mode debugging.

For more information about processes, see <a href="/windows-hardware/drivers/debugger/threads-and-processes">Threads and Processes</a>.

