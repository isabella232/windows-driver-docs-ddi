---
UID: NF:dbgeng.IDebugSymbols.ResetScope
title: IDebugSymbols::ResetScope (dbgeng.h)
description: The ResetScope method resets the current scope to the default scope of the current thread. This method belongs to the IDebugSymbols interface.
old-location: debugger\resetscope.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugSymbols::ResetScope"]
ms.keywords: IDebugSymbols interface [Windows Debugging],ResetScope method, IDebugSymbols.ResetScope, IDebugSymbols2 interface [Windows Debugging],ResetScope method, IDebugSymbols2::ResetScope, IDebugSymbols3 interface [Windows Debugging],ResetScope method, IDebugSymbols3::ResetScope, IDebugSymbols::ResetScope, IDebugSymbols_e3d0b307-57e7-4bc1-83f6-3352dd33a7aa.xml, ResetScope, ResetScope method [Windows Debugging], ResetScope method [Windows Debugging],IDebugSymbols interface, ResetScope method [Windows Debugging],IDebugSymbols2 interface, ResetScope method [Windows Debugging],IDebugSymbols3 interface, dbgeng/IDebugSymbols2::ResetScope, dbgeng/IDebugSymbols3::ResetScope, dbgeng/IDebugSymbols::ResetScope, debugger.resetscope
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
 - IDebugSymbols::ResetScope
 - dbgeng/IDebugSymbols::ResetScope
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dbgeng.h
api_name:
 - IDebugSymbols::ResetScope
---

# IDebugSymbols::ResetScope


## -description

The <b>ResetScope</b> method resets the current scope to the default scope of the current thread.

## -parameters

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

For more information about scopes, see <a href="/windows-hardware/drivers/debugger/scopes-and-symbol-groups">Scopes and Symbol Groups</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugsymbols3-getscope">GetScope</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugsymbols">IDebugSymbols</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugsymbols2">IDebugSymbols2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugsymbols3">IDebugSymbols3</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugsymbols3-setscope">SetScope</a>

