---
UID: NC:dispmprt.DXGKDDI_NOTIFY_SURPRISE_REMOVAL
title: DXGKDDI_NOTIFY_SURPRISE_REMOVAL
author: windows-driver-content
description: Called by the operating system after a user disconnected an external display device without notifying the system.Can optionally be implemented by Windows Display Driver Model (WDDM) 1.2 and later display miniport drivers.
old-location: display\dxgkddinotifysurpriseremoval.htm
old-project: display
ms.assetid: 4e6403e7-7463-479a-8be9-4136287b375e
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXGKDDI_NOTIFY_SURPRISE_REMOVAL, DxgkDdiNotifySurpriseRemoval, DxgkDdiNotifySurpriseRemoval callback function [Display Devices], display.dxgkddinotifysurpriseremoval, dispmprt/DxgkDdiNotifySurpriseRemoval
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: dispmprt.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Dispmprt.h
api_name:
-	DxgkDdiNotifySurpriseRemoval
product: Windows
targetos: Windows
req.typenames: SYMBOL_INFO_EX, *PSYMBOL_INFO_EX
---

# DXGKDDI_NOTIFY_SURPRISE_REMOVAL callback


## -description


Called by the operating system after a user disconnected an external display device without notifying the system.Can optionally be implemented by Windows Display Driver Model (WDDM) 1.2 and later display miniport drivers.




## -prototype


````
DXGKDDI_NOTIFY_SURPRISE_REMOVAL DxgkDdiNotifySurpriseRemoval;

_Check_return_ NTSTATUS* DxgkDdiNotifySurpriseRemoval(
  _In_ PVOID                      MiniportDeviceContext,
  _In_ DXGK_SURPRISE_REMOVAL_TYPE RemovalType
)
{ ... }
````


## -parameters




### -param MiniportDeviceContext [in]

A handle to a context block associated with a display adapter. The display miniport driver's <a href="..\dispmprt\nc-dispmprt-dxgkddi_add_device.md">DxgkDdiAddDevice</a> function previously provided this handle to the DirectX graphics kernel subsystem.


### -param RemovalType [in]

A value of type <a href="..\dispmprt\ne-dispmprt-_dxgk_surprise_removal_type.md">DXGK_SURPRISE_REMOVAL_TYPE</a> that identifies the type of surprise removal event.


## -returns




      Returns <b>STATUS_SUCCESS</b> if software resources were cleaned up for <i>RemovalType</i> = <b>DxgkRemovalHibernation</b>. If the driver instead returns an error code, the operating system will attempt to reboot the system, as described in the following Remarks section.




## -remarks



The operating system calls <i>DxgkDdiNotifySurpriseRemoval</i> only if the display miniport driver indicates support by setting the <b>SupportSurpriseRemovalInHibernation</b> member of the <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_drivercaps.md">DXGK_DRIVERCAPS</a> structure to 1.

<div class="alert"><b>Note</b>  This function is called only if the disconnected external display device was in hibernation mode. This is indicated by <i>RemovalType</i> = <b>DxgkRemovalHibernation</b>, the only available value.</div>
<div> </div>
If the display miniport driver returns <b>STATUS_SUCCESS</b>, the DirectX graphics kernel subsystem will continue to remove the  external display adapter from the graphics stack and will call other driver-implemented <i>DxgkDdiXxx</i> kernel-mode functions to release all resources. In this case, the driver must complete its cleanup of software resources in response to calls from the operating system but must not touch or clean any hardware settings. If no other hardware is using the driver, the operating system will unload the driver.

If the driver returns an error code, does not set <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_drivercaps.md">DXGK_DRIVERCAPS</a>.<b>SupportSurpriseRemovalInHibernation</b>, or does not implement this function, the DirectX graphics kernel subsystem  will not call any more driver-implemented <i>DxgkDdiXxx</i> functions and will attempt to reboot the system. In this case, the resource that was allocated before the external display device was disconnected will not be released.




## -see-also

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_drivercaps.md">DXGK_DRIVERCAPS</a>



<a href="..\dispmprt\nc-dispmprt-dxgkddi_add_device.md">DxgkDdiAddDevice</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406678">D3DKMT_WDDM_1_2_CAPS</a>



<a href="..\dispmprt\ne-dispmprt-_dxgk_surprise_removal_type.md">DXGK_SURPRISE_REMOVAL_TYPE</a>



 

 


