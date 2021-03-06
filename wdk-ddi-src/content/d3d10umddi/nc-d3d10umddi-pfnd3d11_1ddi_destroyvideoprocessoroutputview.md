---
UID: NC:d3d10umddi.PFND3D11_1DDI_DESTROYVIDEOPROCESSOROUTPUTVIEW
title: PFND3D11_1DDI_DESTROYVIDEOPROCESSOROUTPUTVIEW
author: windows-driver-content
description: Releases resources for the video processor output view that were created through a call to the CreateVideoProcessorOutputView function.
old-location: display\destroyvideoprocessoroutputview.htm
old-project: display
ms.assetid: 7efc032e-0ee4-4eca-b6b0-dda4bfab2756
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3D11_1DDI_DESTROYVIDEOPROCESSOROUTPUTVIEW, d3d10umddi/pfnDestroyVideoProcessorOutputView, display.destroyvideoprocessoroutputview, pfnDestroyVideoProcessorOutputView, pfnDestroyVideoProcessorOutputView callback function [Display Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	D3d10umddi.h
api_name:
-	pfnDestroyVideoProcessorOutputView
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11_1DDI_DESTROYVIDEOPROCESSOROUTPUTVIEW callback


## -description


Releases resources for the video processor output view that were created through a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createvideoprocessoroutputview.md">CreateVideoProcessorOutputView</a> function.



## -prototype


````
PFND3D11_1DDI_DESTROYVIDEOPROCESSOROUTPUTVIEW pfnDestroyVideoProcessorOutputView;

VOID APIENTRY* pfnDestroyVideoProcessorOutputView(
  _In_ D3D10DDI_HDEVICE                     hDevice,
  _In_ D3D11_1DDI_HVIDEOPROCESSOROUTPUTVIEW hView
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param D3D11_1DDI_HVIDEOPROCESSOROUTPUTVIEW








#### - hDevice [in]

A handle to the display device (graphics context).




#### - hView [in]

A handle to the driver's private data for the video processor output view. This handle was created by the Direct3D runtime and passed to the driver in the call to <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createvideoprocessoroutputview.md">CreateVideoProcessorOutputView</a>.


## -returns



This callback function does not return a value.




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createvideoprocessoroutputview.md">CreateVideoProcessorOutputView</a>



 

 


