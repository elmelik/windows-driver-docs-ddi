---
UID: NF:ndis.NdisMDeregisterMiniportDriver
title: NdisMDeregisterMiniportDriver function
author: windows-driver-content
description: A miniport driver calls the NdisMDeregisterMiniportDriver function to release resources that it allocated with a previous call to the NdisMRegisterMiniportDriver function.
old-location: netvista\ndismderegisterminiportdriver.htm
old-project: netvista
ms.assetid: c428e30d-ce86-4ca0-bc65-45d84a7c910e
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: NdisMDeregisterMiniportDriver, NdisMDeregisterMiniportDriver function [Network Drivers Starting with Windows Vista], miniport_ndis_functions_ref_bd8d7bcd-098a-4367-82d2-6a35753a4a3b.xml, ndis/NdisMDeregisterMiniportDriver, netvista.ndismderegisterminiportdriver
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	ndis.lib
-	ndis.dll
api_name:
-	NdisMDeregisterMiniportDriver
product: Windows
targetos: Windows
req.typenames: NDIS_SHARED_MEMORY_USAGE, *PNDIS_SHARED_MEMORY_USAGE
---

# NdisMDeregisterMiniportDriver function


## -description


A miniport driver calls the 
  <b>NdisMDeregisterMiniportDriver</b> function to release resources that it allocated with a previous call to
  the 
  <a href="..\ndis\nf-ndis-ndismregisterminiportdriver.md">NdisMRegisterMiniportDriver</a> function.


## -syntax


````
VOID NdisMDeregisterMiniportDriver(
  _In_ NDIS_HANDLE NdisMiniportDriverHandle
);
````


## -parameters




### -param NdisMiniportDriverHandle [in]

The handle that the miniport driver obtained in a previous call to 
     <a href="..\ndis\nf-ndis-ndismregisterminiportdriver.md">NdisMRegisterMiniportDriver</a>.


## -returns



None




## -remarks



If an error occurs in the miniport driver's 
    <a href="..\wudfwdm\nc-wudfwdm-driver_initialize.md">DriverEntry</a> routine after the 
    <a href="..\ndis\nf-ndis-ndismregisterminiportdriver.md">
    NdisMRegisterMiniportDriver</a> function returns successfully, the driver must call 
    <b>NdisMDeregisterMiniportDriver</b> before 
    <b>DriverEntry</b> returns. If 
    <b>DriverEntry</b> succeeds, the driver must call 
    <b>NdisMDeregisterMiniportDriver</b> from its 
    <a href="..\ndis\nc-ndis-miniport_unload.md">MiniportDriverUnload</a> function.




## -see-also

<a href="..\wudfwdm\nc-wudfwdm-driver_initialize.md">DriverEntry</a>



<a href="..\ndis\nc-ndis-miniport_unload.md">MiniportDriverUnload</a>



<a href="..\ndis\nf-ndis-ndismregisterminiportdriver.md">NdisMRegisterMiniportDriver</a>



 

 


