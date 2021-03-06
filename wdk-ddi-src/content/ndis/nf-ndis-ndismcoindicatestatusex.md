---
UID: NF:ndis.NdisMCoIndicateStatusEx
title: NdisMCoIndicateStatusEx function
author: windows-driver-content
description: The NdisMCoIndicateStatusEx function reports a change in the status of a CoNDIS miniport adapter.
old-location: netvista\ndismcoindicatestatusex.htm
tech.root: netvista
ms.assetid: e6d5bd94-d9cb-462f-84e4-bf9d70961e95
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: NdisMCoIndicateStatusEx, NdisMCoIndicateStatusEx function [Network Drivers Starting with Windows Vista], condis_status_ref_1a0c27e2-e728-4b1d-8e45-9305869d3bfc.xml, ndis/NdisMCoIndicateStatusEx, netvista.ndismcoindicatestatusex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Desktop
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: Irql_MCO_Function
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ndis.lib
req.dll: 
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	ndis.lib
-	ndis.dll
api_name:
-	NdisMCoIndicateStatusEx
product:
- Windows
targetos: Windows
req.typenames: 
---

# NdisMCoIndicateStatusEx function


## -description


The 
  <b>NdisMCoIndicateStatusEx</b> function reports a change in the status of a CoNDIS miniport adapter.


## -parameters




### -param MiniportAdapterHandle [in]

The miniport adapter handle that NDIS passed at the 
     <i>MiniportAdapterHandle</i> parameter of the 
     <a href="https://msdn.microsoft.com/b146fa81-005b-4a6c-962d-4cb023ea790e">
     MiniportInitializeEx</a> function.


### -param NdisVcHandle [in, optional]

A handle that identifies the virtual connection (VC). The miniport driver obtained this handle as
     an input parameter to its 
     <a href="https://msdn.microsoft.com/99eaba29-ce17-4e79-878e-5fdf7411e56c">MiniportCoCreateVc</a> function, either
     when a client set up an outgoing call or when the call manager created a VC for a client-registered
     service access point (SAP). The call manager created the VC to indicate an incoming-call notification.
     To send the status indication to all protocol bindings, set this parameter to <b>NULL</b>.


### -param StatusIndication [in]

A pointer to an 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff567373">NDIS_STATUS_INDICATION</a> structure
     that contains the status information.


## -returns



None




## -remarks



When a miniport driver calls 
    <b>NdisMCoIndicateStatusEx</b> with a <b>NULL</b> VC handle for the 
    <i>NdisVcHandle</i> parameter, NDIS forwards the status-change notification to all of the bound protocol
    drivers by calling each bound protocol driver's 
    <a href="https://msdn.microsoft.com/1416ad56-548c-4f12-9922-9ab9a7e4fd3a">ProtocolCoStatusEx</a> function. A call
    to 
    <b>NdisMCoIndicateStatusEx</b> with a non-<b>NULL</b> VC handle restricts the status notification to clients or
    call managers that the miniport driver shares this VC handle with.

A miniport driver can call 
    <b>NdisMCoIndicateStatusEx</b> after setting its registration attributes, by calling the 
    <a href="https://msdn.microsoft.com/861626af-23ea-40dc-a91a-7da42d4b0a1c">
    NdisMSetMiniportAttributes</a> function from its 
    <a href="https://msdn.microsoft.com/b146fa81-005b-4a6c-962d-4cb023ea790e">MiniportInitializeEx</a> function,
    even if the driver is still in the context of the 
    <i>MiniportInitializeEx</i> function. The driver must not call 
    <b>NdisMCoIndicateStatusEx</b> after it returns from the 
    <a href="https://msdn.microsoft.com/b8d452b4-bef3-4991-87cf-fac15bedfde4">MiniportHaltEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/99eaba29-ce17-4e79-878e-5fdf7411e56c">MiniportCoCreateVc</a>



<a href="https://msdn.microsoft.com/b8d452b4-bef3-4991-87cf-fac15bedfde4">MiniportHaltEx</a>



<a href="https://msdn.microsoft.com/b146fa81-005b-4a6c-962d-4cb023ea790e">MiniportInitializeEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567373">NDIS_STATUS_INDICATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563672">NdisMSetMiniportAttributes</a>



<a href="https://msdn.microsoft.com/1416ad56-548c-4f12-9922-9ab9a7e4fd3a">ProtocolCoStatusEx</a>
 

 

