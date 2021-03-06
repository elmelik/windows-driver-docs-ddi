---
UID: NC:d3d10umddi.PFND3D10DDI_STATE_IA_PRIMITIVE_TOPOLOGY_CB
title: PFND3D10DDI_STATE_IA_PRIMITIVE_TOPOLOGY_CB
author: windows-driver-content
description: The pfnStateIaPrimitiveTopologyCb function causes the Microsoft Direct3D 10 runtime to refresh the primitive topology state.
old-location: display\pfnstateiaprimitivetopologycb.htm
old-project: display
ms.assetid: 5a394a5b-afbc-41f5-8013-ab228e6284f9
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3D10DDI_STATE_IA_PRIMITIVE_TOPOLOGY_CB, d3d10state_functions_5866253f-2d14-41e3-b60d-d633b272848c.xml, d3d10umddi/pfnStateIaPrimitiveTopologyCb, display.pfnstateiaprimitivetopologycb, pfnStateIaPrimitiveTopologyCb, pfnStateIaPrimitiveTopologyCb callback function [Display Devices]
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
-	pfnStateIaPrimitiveTopologyCb
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D10DDI_STATE_IA_PRIMITIVE_TOPOLOGY_CB callback


## -description


The <b>pfnStateIaPrimitiveTopologyCb</b> function causes the Microsoft Direct3D 10 runtime to refresh the primitive topology state.


## -prototype


````
PFND3D10DDI_STATE_IA_PRIMITIVE_TOPOLOGY_CB pfnStateIaPrimitiveTopologyCb;

void APIENTRY pfnStateIaPrimitiveTopologyCb(
  _In_ D3D10DDI_HRTCORELAYER hRuntimeDevice
)
{ ... }
````


## -parameters




### -param D3D10DDI_HRTCORELAYER








#### - hRuntimeDevice [in]

 A handle to a context for the core Direct3D 10 runtime. This handle is supplied to the driver in a call to the driver's <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createdevice.md">CreateDevice(D3D10)</a> function. 


## -returns



None




## -see-also

<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_corelayer_devicecallbacks.md">D3D10DDI_CORELAYER_DEVICECALLBACKS</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_createdevice.md">CreateDevice(D3D10)</a>



 

 


