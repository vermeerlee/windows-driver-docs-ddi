---
UID: NF:rxce.RxCeQueryAdapterStatus
title: RxCeQueryAdapterStatus function (rxce.h)
description: RxCeQueryAdapterStatus returns the ADAPTER_STATUS structure for a given transport in a caller-allocated buffer.
old-location: ifsk\rxcequeryadapterstatus.htm
tech.root: ifsk
ms.assetid: ebe9bec3-6c38-48d8-b9af-03aadbc09d98
ms.date: 04/16/2018
keywords: ["RxCeQueryAdapterStatus function"]
ms.keywords: RxCeQueryAdapterStatus, RxCeQueryAdapterStatus function [Installable File System Drivers], ifsk.rxcequeryadapterstatus, rxce/RxCeQueryAdapterStatus, rxref_0813f428-95ae-47df-969c-c00563f3b3c8.xml
req.header: rxce.h
req.include-header: Rxce.h
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
req.irql: <= APC_LEVEL
targetos: Windows
req.typenames: 
f1_keywords:
 - RxCeQueryAdapterStatus
 - rxce/RxCeQueryAdapterStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rxce.h
api_name:
 - RxCeQueryAdapterStatus
---

# RxCeQueryAdapterStatus function


## -description

<b>RxCeQueryAdapterStatus</b> returns the ADAPTER_STATUS structure for a given transport in a caller-allocated buffer.

## -parameters

### -param pTransport

A pointer to the RDBSS transport that is associated with an adapter.

### -param pAdapterStatus

On input, this parameter contains a pointer to caller-allocated buffer to hold the adapter status. On output when this call is successful, the buffer contains the adapter status associated with the specified RDBSS transport.

## -returns

<b>RxCeQueryAdapterStatus</b> returns STATUS_SUCCESS on success or one of the following error codes on failure: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ADDRESS_NOT_ASSOCIATED</b></dt>
</dl>
</td>
<td width="60%">
An adapter address is not associated with the RDBSS transport. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INSUFFICIENT_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The allocation of nonpaged pool memory needed by this routine failed. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTransport</i> parameter passed to this routine was invalid. 

</td>
</tr>
</table>

## -remarks

<b>RxCeQueryAdapterStatus</b> returns an ADAPTER_STATUS structure for a given transport. This routine is most commonly used to get the NetBIOS name of the adapter. 

<b>RxCeQueryAdapterStatus</b> calls <b>TdiBuildQueryInformation</b> with a TDI_QUERY_ADAPTER_STATUS query.

## -see-also

<a href="/windows/win32/api/nb30/ns-nb30-adapter_status">ADAPTER_STATUS</a>



<a href="/windows-hardware/drivers/ddi/rxce/nf-rxce-rxcequeryinformation">RxCeQueryInformation</a>



<a href="/windows-hardware/drivers/ddi/rxce/nf-rxce-rxcequerytransportinformation">RxCeQueryTransportInformation</a>