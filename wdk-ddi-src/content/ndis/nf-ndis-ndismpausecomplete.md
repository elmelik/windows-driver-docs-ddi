---
UID: NF:ndis.NdisMPauseComplete
title: NdisMPauseComplete function
author: windows-driver-content
description: A miniport driver must call the NdisMPauseComplete function to complete a pause operation if the driver returned NDIS_STATUS_PENDING from its MiniportPause function.
old-location: netvista\ndismpausecomplete.htm
old-project: netvista
ms.assetid: 08a9dccf-53bc-4b96-a794-14ead08a7b0b
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: NdisMPauseComplete, NdisMPauseComplete function [Network Drivers Starting with Windows Vista], miniport_ndis_functions_ref_1e76f7bc-a042-4a7a-8dc6-0f4cc6f7617f.xml, ndis/NdisMPauseComplete, netvista.ndismpausecomplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Universal
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: Irql_Miniport_Driver_Function
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
-	NdisMPauseComplete
product: Windows
targetos: Windows
req.typenames: NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---

# NdisMPauseComplete function


## -description


A miniport driver must call the 
  <b>NdisMPauseComplete</b> function to complete a pause operation if the driver returned NDIS_STATUS_PENDING
  from its 
  <a href="..\ndis\nc-ndis-miniport_pause.md">MiniportPause</a> function.


## -syntax


````
VOID NdisMPauseComplete(
  _In_ NDIS_HANDLE MiniportAdapterHandle
);
````


## -parameters




### -param MiniportAdapterHandle [in]

The miniport adapter handle that NDIS passed to the 
     <i>MiniportAdapterHandle</i> parameter of 
     <a href="..\ndis\nc-ndis-miniport_initialize.md">MiniportInitializeEx</a>.


## -returns



None




## -remarks



NDIS calls a miniport driver's 
    <a href="..\ndis\nc-ndis-miniport_pause.md">MiniportPause</a> function to initiate a
    pause request for a miniport adapter. The miniport adapter remains in the 
    <i>Pausing</i> state until the pause operation is complete.

After a miniport driver completes all outstanding send requests and NDIS returns all the network data
    structures in outstanding receive indications to the driver, the driver calls 
    <b>NdisMPauseComplete</b> to complete the pending pause request. After the driver calls 
    <b>NdisMPauseComplete</b>, the miniport adapter is in the 
    <i>Paused</i> state.

NDIS calls the 
    <a href="..\ndis\nc-ndis-miniport_restart.md">MiniportRestart</a> function to initiate a
    restart request for a miniport adapter that is paused.




## -see-also

<a href="..\ndis\nc-ndis-miniport_pause.md">MiniportPause</a>



<a href="..\ndis\nc-ndis-miniport_restart.md">MiniportRestart</a>



<a href="..\ndis\nc-ndis-miniport_initialize.md">MiniportInitializeEx</a>



 

 


