---
UID: NF:dbgeng.IDebugControl3.GetDisassembleEffectiveOffset
title: IDebugControl3::GetDisassembleEffectiveOffset (dbgeng.h)
description: The GetDisassembleEffectiveOffset method returns the address of the last instruction disassembled using Disassemble. This method belongs to IDebugControl3.
old-location: debugger\getdisassembleeffectiveoffset.htm
tech.root: debugger
ms.date: 05/03/2018
keywords: ["IDebugControl3::GetDisassembleEffectiveOffset"]
ms.keywords: GetDisassembleEffectiveOffset, GetDisassembleEffectiveOffset method [Windows Debugging], GetDisassembleEffectiveOffset method [Windows Debugging],IDebugControl interface, GetDisassembleEffectiveOffset method [Windows Debugging],IDebugControl2 interface, GetDisassembleEffectiveOffset method [Windows Debugging],IDebugControl3 interface, IDebugControl interface [Windows Debugging],GetDisassembleEffectiveOffset method, IDebugControl2 interface [Windows Debugging],GetDisassembleEffectiveOffset method, IDebugControl2::GetDisassembleEffectiveOffset, IDebugControl3 interface [Windows Debugging],GetDisassembleEffectiveOffset method, IDebugControl3.GetDisassembleEffectiveOffset, IDebugControl3::GetDisassembleEffectiveOffset, IDebugControl::GetDisassembleEffectiveOffset, IDebugControl_5593ec3a-31f4-4775-9356-49f1757323c0.xml, dbgeng/IDebugControl2::GetDisassembleEffectiveOffset, dbgeng/IDebugControl3::GetDisassembleEffectiveOffset, dbgeng/IDebugControl::GetDisassembleEffectiveOffset, debugger.getdisassembleeffectiveoffset
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
 - IDebugControl3::GetDisassembleEffectiveOffset
 - dbgeng/IDebugControl3::GetDisassembleEffectiveOffset
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dbgeng.h
api_name:
 - IDebugControl3::GetDisassembleEffectiveOffset
---

# IDebugControl3::GetDisassembleEffectiveOffset


## -description

The <b>GetDisassembleEffectiveOffset</b> method returns the address of the last instruction disassembled using <a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol3-disassemble">Disassemble</a>.

## -parameters

### -param Offset 

[out]
Receives the address in the target's memory of the effective offset from the last instruction disassembled.

## -returns

This method can also return error values.  See <a href="/windows-hardware/drivers/debugger/hresult-values">Return Values</a> for more details.

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

## -remarks

The effective offset is the memory location used by an instruction.  For example, if the last instruction to be disassembled is <code>move ax, [ebp+4]</code>, the effective address is the value of <code>ebp+4</code>.  This corresponds to the <b>$ea</b> pseudo-register.

For more information about using assembly with the debugger engine API, see <a href="/windows-hardware/drivers/debugger/assembling-and-disassembling-instructions">Assembling and Disassembling Instructions</a>.

## -see-also

<a href="/windows-hardware/drivers/ddi/dbgeng/nf-dbgeng-idebugcontrol3-disassemble">Disassemble</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugcontrol">IDebugControl</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugcontrol2">IDebugControl2</a>



<a href="/windows-hardware/drivers/ddi/dbgeng/nn-dbgeng-idebugcontrol3">IDebugControl3</a>

