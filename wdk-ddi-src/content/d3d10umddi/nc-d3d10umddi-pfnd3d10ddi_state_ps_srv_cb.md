---
UID: NC:d3d10umddi.PFND3D10DDI_STATE_PS_SRV_CB
title: PFND3D10DDI_STATE_PS_SRV_CB
author: windows-driver-content
description: The pfnStatePsSrvCb function causes the Microsoft Direct3D 10 runtime to refresh the pixel shader stage's bound shader resource views.
old-location: display\pfnstatepssrvcb.htm
old-project: display
ms.assetid: ed49ce47-c56d-4d38-8f2c-562841b8e804
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3D10DDI_STATE_PS_SRV_CB, d3d10state_functions_39451a84-f247-4325-bcc0-b9ee23c2cfe3.xml, d3d10umddi/pfnStatePsSrvCb, display.pfnstatepssrvcb, pfnStatePsSrvCb, pfnStatePsSrvCb callback function [Display Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
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
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	d3d10umddi.h
api_name:
-	pfnStatePsSrvCb
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D10DDI_STATE_PS_SRV_CB callback


## -description


The <b>pfnStatePsSrvCb</b> function causes the Microsoft Direct3D 10 runtime to refresh the pixel shader stage's bound shader resource views.


## -prototype


````
PFND3D10DDI_STATE_PS_SRV_CB pfnStatePsSrvCb;

void APIENTRY pfnStatePsSrvCb(
  _In_ D3D10DDI_HRTCORELAYER hRuntimeDevice,
  _In_ UINT                  Base,
  _In_ UINT                  Count
)
{ ... }
````


## -parameters




### -param D3D10DDI_HRTCORELAYER


### -param UINT








#### - Base [in]

 The beginning resource view for which the runtime should refresh state. 


#### - Count [in]

 The total number of resource views. The number can be -1, which specifies that the Direct3D runtime will use its high watermarks to substitute an optimal value (which is typically less than the maximum valid value for <i>Count</i>). However, no non-NULL binding exists in a slot larger than the optimal <i>Count</i> value.


#### - hRuntimeDevice [in]

 A handle to a context for the core Direct3D 10 runtime. This handle is supplied to the driver in a call to the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createdevice.md">CreateDevice(D3D10)</a> function. 


## -returns



None




## -see-also

<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_corelayer_devicecallbacks.md">D3D10DDI_CORELAYER_DEVICECALLBACKS</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createdevice.md">CreateDevice(D3D10)</a>



 

 


