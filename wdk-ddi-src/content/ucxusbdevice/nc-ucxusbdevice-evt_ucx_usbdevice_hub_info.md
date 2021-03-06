---
UID: NC:ucxusbdevice.EVT_UCX_USBDEVICE_HUB_INFO
title: EVT_UCX_USBDEVICE_HUB_INFO
author: windows-driver-content
description: The client driver's implementation that UCX calls to retrieve hub properties.
old-location: buses\evt_ucx_usbdevice_hub_info.htm
old-project: usbref
ms.assetid: 5bf8000d-63d8-4901-b3fc-d3c43cefe37e
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: EVT_UCX_USBDEVICE_HUB_INFO, EvtUcxUsbDeviceHubInfo, EvtUcxUsbDeviceHubInfo callback function [Buses], PEVT_UCX_USBDEVICE_HUB_INFO, PEVT_UCX_USBDEVICE_HUB_INFO callback function pointer [Buses], buses.evt_ucx_usbdevice_hub_info, ucxusbdevice/EvtUcxUsbDeviceHubInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ucxusbdevice.h
req.include-header: Ucxclass.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: DISPATCH_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ucxusbdevice.h
api_name:
-	PEVT_UCX_USBDEVICE_HUB_INFO
product: Windows
targetos: Windows
req.typenames: STREAM_INFO, *PSTREAM_INFO
req.product: Windows 10 or later.
---

# EVT_UCX_USBDEVICE_HUB_INFO callback


## -description


The client driver's implementation that UCX calls to
retrieve hub properties.


## -prototype


````
EVT_UCX_USBDEVICE_HUB_INFO EvtUcxUsbDeviceHubInfo;

VOID EvtUcxUsbDeviceHubInfo(
  _In_ UCXCONTROLLER UcxController,
  _In_ WDFREQUEST    Request
)
{ ... }

typedef EVT_UCX_USBDEVICE_HUB_INFO PEVT_UCX_USBDEVICE_HUB_INFO;
````


## -parameters




### -param UcxController [in]

 A handle to the UCX controller that the client driver received in a previous call to  the <a href="https://msdn.microsoft.com/library/windows/hardware/mt188033">UcxControllerCreate</a> method.


### -param Request [in]

Contains the <a href="..\ucxusbdevice\ns-ucxusbdevice-_usbdevice_hub_info.md">USBDEVICE_HUB_INFO</a> structure.


## -returns



This callback function does not return a value.




## -remarks



The UCX client driver registers this callback function with the USB host controller extension (UCX) by calling the <a href="..\ucxusbdevice\nf-ucxusbdevice-ucxusbdevicecreate.md">UcxUsbDeviceCreate</a> method.

If the USB device is not a hub, do not provide this callback.

The client driver returns completion status in <i>Request</i>.  The driver can complete the WDFREQUEST asynchronously.


#### Examples

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>VOID
UsbDevice_EvtUcxUsbDeviceHubInfo(
    UCXCONTROLLER      UcxController,
    WDFREQUEST         Request
)

{
    UNREFERENCED_PARAMETER(UcxController);

    DbgTrace(TL_INFO, UsbDevice, "UsbDevice_EvtUcxUsbDeviceHubInfo");

    //
    // Retrieve the USBDEVICE_HUB_INFO pointer from the
    // IOCTL_INTERNAL_USB_USBDEVICE_HUB_INFO WdfRequest.
    //
    WDF_REQUEST_PARAMETERS_INIT(&amp;wdfRequestParams);
    WdfRequestGetParameters(WdfRequest, &amp;wdfRequestParams);

    hubInfo = (PUSBDEVICE_HUB_INFO)wdfRequestParams.Parameters.Others.Arg1;

    ....


    WdfRequestComplete(Request, STATUS_SUCCESS);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also

<a href="..\ucxusbdevice\ns-ucxusbdevice-_ucx_usbdevice_event_callbacks.md">UCX_USBDEVICE_EVENT_CALLBACKS</a>



<a href="..\ucxusbdevice\ns-ucxusbdevice-_usbdevice_hub_info.md">USBDEVICE_HUB_INFO</a>



<a href="..\ucxusbdevice\nf-ucxusbdevice-ucxusbdevicecreate.md">UcxUsbDeviceCreate</a>



<a href="..\ucxusbdevice\nf-ucxusbdevice-ucx_usbdevice_event_callbacks_init.md">UCX_USBDEVICE_EVENT_CALLBACKS_INIT</a>



 

 


