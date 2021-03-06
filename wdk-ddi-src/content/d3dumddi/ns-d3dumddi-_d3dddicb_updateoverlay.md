---
UID: NS:d3dumddi._D3DDDICB_UPDATEOVERLAY
title: "_D3DDDICB_UPDATEOVERLAY"
author: windows-driver-content
description: The D3DDDICB_UPDATEOVERLAY structure describes parameters for modifying an overlay.
old-location: display\d3dddicb_updateoverlay.htm
old-project: display
ms.assetid: efa54d23-99bc-49ea-b8a3-7ea5b00e36d8
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: D3DDDICB_UPDATEOVERLAY, D3DDDICB_UPDATEOVERLAY structure [Display Devices], D3D_param_Structs_b9e39db9-44ba-45d5-9500-dd9d5d8cc4bb.xml, _D3DDDICB_UPDATEOVERLAY, d3dumddi/D3DDDICB_UPDATEOVERLAY, display.d3dddicb_updateoverlay
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Windows
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
-	HeaderDef
api_location:
-	d3dumddi.h
api_name:
-	D3DDDICB_UPDATEOVERLAY
product: Windows
targetos: Windows
req.typenames: D3DDDICB_UPDATEOVERLAY
---

# _D3DDDICB_UPDATEOVERLAY structure


## -description


The D3DDDICB_UPDATEOVERLAY structure describes parameters for modifying an overlay.


## -syntax


````
typedef struct _D3DDDICB_UPDATEOVERLAY {
  D3DKMT_HANDLE            hKernelOverlay;
  D3DDDI_KERNELOVERLAYINFO OverlayInfo;
} D3DDDICB_UPDATEOVERLAY;
````


## -struct-fields




### -field hKernelOverlay

[in] A D3DKMT_HANDLE data type that represents the kernel-mode handle that is returned by the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_createoverlaycb.md">pfnCreateOverlayCb</a> function and that identifies the kernel-mode overlay object to modify. 


### -field OverlayInfo

[in] A <a href="..\d3dukmdt\ns-d3dukmdt-_d3dddi_kerneloverlayinfo.md">D3DDDI_KERNELOVERLAYINFO</a> structure that describes modification information for the kernel-mode overlay object. 


## -see-also

<a href="..\d3dukmdt\ns-d3dukmdt-_d3dddi_kerneloverlayinfo.md">D3DDDI_KERNELOVERLAYINFO</a>



<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_updateoverlaycb.md">pfnUpdateOverlayCb</a>



<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_createoverlaycb.md">pfnCreateOverlayCb</a>



 

 


