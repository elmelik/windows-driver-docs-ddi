---
UID: NC:dot11wdi.MINIPORT_WDI_RX_STOP
title: MINIPORT_WDI_RX_STOP
author: windows-driver-content
description: The MiniportWdiRxStop handler function stops RX on a given port and accepts the wildcard port ID to stop RX across the adapter.
old-location: netvista\miniportwdirxstop.htm
old-project: netvista
ms.assetid: AAFECA64-07D7-43E6-ABFB-C0C85A9C03CD
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: MINIPORT_WDI_RX_STOP, MiniportWdiRxStop, MiniportWdiRxStop callback function [Network Drivers Starting with Windows Vista], dot11wdi/MiniportWdiRxStop, netvista.miniportwdirxstop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: dot11wdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	dot11wdi.h
api_name:
-	MiniportWdiRxStop
product: Windows
targetos: Windows
req.typenames: SYNTH_STATS, *PSYNTH_STATS
---

# MINIPORT_WDI_RX_STOP callback


## -description


The 
  MiniportWdiRxStop handler function stops RX on a given port and accepts the wildcard port ID  to stop RX across the adapter. The TAL completes the RX stop operation by completing the request with a success status, or by completing it with a pending status and asynchronously indicating <a href="..\dot11wdi\nc-dot11wdi-ndis_wdi_rx_stop_confirm.md">RxStopConfirm</a>.

This is a WDI miniport handler inside <a href="..\dot11wdi\ns-dot11wdi-_ndis_miniport_wdi_data_handlers.md">NDIS_MINIPORT_WDI_DATA_HANDLERS</a>.

Prior to completing the indication, the target must be configured to stop indicating new traffic on the selected port or the entire adapter.

This request is issued to the TAL as part of a transition to low power (adapter) and dot11 reset (port).
<div class="alert"><b>Note</b>  You must declare the function by using the <b>MINIPORT_WDI_RX_STOP</b> type. For more
   information, see the following Examples section.</div><div> </div>

## -prototype


````
MINIPORT_WDI_RX_STOP MiniportWdiRxStop;

VOID MiniportWdiRxStop(
  _In_  TAL_TXRX_HANDLE MiniportTalTxRxContext,
  _In_  WDI_PORT_ID     PortId,
  _Out_ NDIS_STATUS     *pWifiStatus
)
{ ... }
````


## -parameters




### -param MiniportTalTxRxContext [in]

TAL device handle returned by the IHV miniport in <a href="..\dot11wdi\nc-dot11wdi-miniport_wdi_tal_txrx_initialize.md">MiniportWdiTalTxRxInitialize</a>.


### -param PortId [in]

The port ID.


### -param *pWifiStatus [out]

Status from the IHV miniport. A success status indicates that the operation completion synchronously.  A pending status indicates that the stop will be asynchronously confirmed.


## -returns



This callback function does not return a value.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/mt269099">WDI_PORT_ID</a>



<a href="..\dot11wdi\ns-dot11wdi-_ndis_miniport_wdi_data_handlers.md">NDIS_MINIPORT_WDI_DATA_HANDLERS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297625">TAL_TXRX_HANDLE</a>



<a href="https://msdn.microsoft.com/EEEA7181-4A24-4F40-8A44-65EC38D1A867">WDI RX path</a>



 

 


