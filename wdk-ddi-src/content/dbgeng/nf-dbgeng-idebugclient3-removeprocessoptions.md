---
UID: NF:dbgeng.IDebugClient3.RemoveProcessOptions
title: IDebugClient3::RemoveProcessOptions (dbgeng.h)
description: The RemoveProcessOptions method removes process options from those options that affect the current process. This method belongs to the IDebugClient3 interface.
old-location: debugger\removeprocessoptions.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugClient3::RemoveProcessOptions"]
ms.keywords: IDebugClient interface [Windows Debugging],RemoveProcessOptions method, IDebugClient2 interface [Windows Debugging],RemoveProcessOptions method, IDebugClient2::RemoveProcessOptions, IDebugClient3 interface [Windows Debugging],RemoveProcessOptions method, IDebugClient3.RemoveProcessOptions, IDebugClient3::RemoveProcessOptions, IDebugClient4 interface [Windows Debugging],RemoveProcessOptions method, IDebugClient4::RemoveProcessOptions, IDebugClient5 interface [Windows Debugging],RemoveProcessOptions method, IDebugClient5::RemoveProcessOptions, IDebugClient::RemoveProcessOptions, IDebugClient_eafb8a9c-18a4-4737-8ece-955596338fe5.xml, RemoveProcessOptions, RemoveProcessOptions method [Windows Debugging], RemoveProcessOptions method [Windows Debugging],IDebugClient interface, RemoveProcessOptions method [Windows Debugging],IDebugClient2 interface, RemoveProcessOptions method [Windows Debugging],IDebugClient3 interface, RemoveProcessOptions method [Windows Debugging],IDebugClient4 interface, RemoveProcessOptions method [Windows Debugging],IDebugClient5 interface, dbgeng/IDebugClient2::RemoveProcessOptions, dbgeng/IDebugClient3::RemoveProcessOptions, dbgeng/IDebugClient4::RemoveProcessOptions, dbgeng/IDebugClient5::RemoveProcessOptions, dbgeng/IDebugClient::RemoveProcessOptions, debugger.removeprocessoptions
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
 - IDebugClient3::RemoveProcessOptions
 - dbgeng/IDebugClient3::RemoveProcessOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugClient3::RemoveProcessOptions
---

# IDebugClient3::RemoveProcessOptions


## -description

The <b>RemoveProcessOptions</b> method removes process options from those options that affect the current process.

## -parameters

### -param Options 

[in]
Specifies the process options to remove from those affecting the current process.  For details on these options, see <a href="/windows-hardware/drivers/debugger/debug-process-xxx">DEBUG_PROCESS_XXX</a>.

## -returns

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
</table>
 

This method may also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

## -remarks

This method is available only in live user-mode debugging.

Some of the process options are global options, others are specific to the current process.

If any process options are modified, the engine will notify the event callbacks by calling their <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugeventcallbacks-changeenginestate">IDebugEventCallbacks::ChangeEngineState</a> method with the DEBUG_CES_PROCESS_OPTIONS flag set.

For more information about creating and attaching to live user-mode targets, see <a href="/windows-hardware/drivers/debugger/live-user-mode-targets">Live User-Mode Targets</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugclient5-addprocessoptions">AddProcessOptions</a>



<a href="/windows-hardware/drivers/debugger/debug-process-xxx">DEBUG_PROCESS_XXX</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugclient5-getprocessoptions">GetProcessOptions</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient">IDebugClient</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient2">IDebugClient2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient3">IDebugClient3</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient4">IDebugClient4</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugclient5">IDebugClient5</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugclient5-setprocessoptions">SetProcessOptions</a>

