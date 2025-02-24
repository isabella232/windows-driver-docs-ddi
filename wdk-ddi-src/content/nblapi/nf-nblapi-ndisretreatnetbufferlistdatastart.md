---
UID: NF:nblapi.NdisRetreatNetBufferListDataStart
title: NdisRetreatNetBufferListDataStart
ms.date: 11/30/2020
targetos: Windows
description: Call the NdisRetreatNetBufferListDataStart function to increase the used data space in all the NET_BUFFER structures in a NET_BUFFER_LIST structure.
tech.root: netvista
req.assembly: 
req.construct-type: function
req.ddi-compliance: Irql_NetBuffer_Function
req.dll: 
req.header: ndis/nblapi.h
req.idl: 
req.include-header: ndis.h
req.irql: <= DISPATCH_LEVEL
req.kmdf-ver: 
req.lib: Ndis.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
req.target-min-winversvr: 
req.target-type: Universal
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - nblapi.h
api_name:
 - NdisRetreatNetBufferListDataStart
f1_keywords:
 - NdisRetreatNetBufferListDataStart
 - nblapi/NdisRetreatNetBufferListDataStart
dev_langs:
 - c++
---


# NdisRetreatNetBufferListDataStart function


## -description

Call the 
  <b>NdisRetreatNetBufferListDataStart</b> function to increase the 
  <i>used data space</i> in all the 
  <a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer">NET_BUFFER</a> structures in a 
  <a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer_list">NET_BUFFER_LIST</a> structure.

## -parameters

### -param NetBufferList 

[in]
A pointer to a previously allocated NET_BUFFER_LIST structure.

### -param DataOffsetDelta 

[in]
The amount of additional 
     <i>used data space</i> in each NET_BUFFER structure. If there is not enough 
     <i>unused data space</i> to satisfy the request, NDIS allocates more memory.

### -param DataBackFill 

[in]
If NDIS must allocate memory, this parameter specifies the amount of data space in addition to the
     value of the 
     <i>DataOffsetDelta</i> parameter to allocate.

### -param AllocateMdlHandler 

[in, optional]
An optional entry point for an 
     <a href="/windows-hardware/drivers/ddi/nblapi/nc-nblapi-net_buffer_allocate_mdl">NetAllocateMdl</a> function. If the caller
     specifies an entry point for the 
     <i>NetAllocateMdl</i> function, NDIS calls 
     <i>NetAllocateMdl</i> to allocate an MDL and memory.

### -param FreeMdlHandler 

[in, optional]
An optional entry point for an 
     <a href="/windows-hardware/drivers/ddi/nblapi/nc-nblapi-net_buffer_free_mdl">NetFreeMdl</a> function. If the caller
     specifies an entry point for the 
     <i>NetFreeMdl</i> function, NDIS calls 
     <i>NetFreeMdl</i> to free an MDL and memory.

## -returns

<b>NdisRetreatNetBufferListDataStart</b> returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDIS_STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
<b>NdisRetreatNetBufferListDataStart</b> successfully allocated the data space on all the NET_BUFFER
       structures either by reducing the value of the 
       <b>DataOffset</b> member or by allocating new storage.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDIS_STATUS_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
<b>NdisRetreatNetBufferListDataStart</b> failed due to insufficient resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDIS_STATUS_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
<b>NdisRetreatNetBufferListDataStart</b> failed for reasons other than insufficient resources.

</td>
</tr>
</table>

## -remarks

Calling 
    <b>NdisRetreatNetBufferListDataStart</b> is the equivalent of calling the 
    <a href="/windows-hardware/drivers/ddi/ndis/nf-ndis-ndisretreatnetbufferdatastart">
    NdisRetreatNetBufferDataStart</a> function for every 
    <a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer">NET_BUFFER</a> structure on the 
    <a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer_list">NET_BUFFER_LIST</a> structure. 
    <b>NdisRetreatNetBufferListDataStart</b> attempts to satisfy the request by reducing the value of the 
    <b>DataOffset</b> member in every NET_BUFFER structure. If there is not enough 
    <i>unused data space</i> available, this function allocates a new buffer and MDL, and then chains the new
    MDL to the beginning of the MDL chain on the NET_BUFFER structure.

Call the 
    <a href="/windows-hardware/drivers/ddi/ndis/nf-ndis-ndisadvancenetbufferlistdatastart">
    NdisAdvanceNetBufferListDataStart</a> function to release data space that was claimed in a previous 
    <b>NdisRetreatNetBufferListDataStart</b> call. Alternatively, the driver can call the 
    <a href="/windows-hardware/drivers/ddi/ndis/nf-ndis-ndisadvancenetbufferdatastart">
    NdisAdvanceNetBufferDataStart</a> function for each NET_BUFFER structure on the NET_BUFFER_LIST
    structure. Calling 
    <b>NdisAdvanceNetBufferListDataStart</b> is more efficient.

## -see-also

<a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer">NET_BUFFER</a>



<a href="/windows-hardware/drivers/ddi/nbl/ns-nbl-net_buffer_list">NET_BUFFER_LIST</a>



<a href="/windows-hardware/drivers/ddi/ndis/nf-ndis-ndisadvancenetbufferdatastart">
   NdisAdvanceNetBufferDataStart</a>



<a href="/windows-hardware/drivers/ddi/ndis/nf-ndis-ndisadvancenetbufferlistdatastart">
   NdisAdvanceNetBufferListDataStart</a>



<a href="/windows-hardware/drivers/ddi/ndis/nf-ndis-ndisretreatnetbufferdatastart">
   NdisRetreatNetBufferDataStart</a>



<a href="/windows-hardware/drivers/ddi/nblapi/nc-nblapi-net_buffer_allocate_mdl">NetAllocateMdl</a>



<a href="/windows-hardware/drivers/ddi/nblapi/nc-nblapi-net_buffer_free_mdl">NetFreeMdl</a>
