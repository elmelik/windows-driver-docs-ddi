---
UID: NC:d3d10umddi.PFND3D11_1DDI_GETVIDEODECODERBUFFERINFO
title: PFND3D11_1DDI_GETVIDEODECODERBUFFERINFO
author: windows-driver-content
description: Queries the description of a video decoder buffer for a specified video operation.
old-location: display\getvideodecoderbufferinfo.htm
old-project: display
ms.assetid: f129ae04-da7f-4681-a266-ac13317a895d
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3D11_1DDI_GETVIDEODECODERBUFFERINFO, d3d10umddi/pfnGetVideoDecoderBufferInfo, display.getvideodecoderbufferinfo, pfnGetVideoDecoderBufferInfo, pfnGetVideoDecoderBufferInfo callback function [Display Devices]
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
-	pfnGetVideoDecoderBufferInfo
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11_1DDI_GETVIDEODECODERBUFFERINFO callback


## -description


Queries the description of a video decoder buffer for a specified video operation.


## -prototype


````
PFND3D11_1DDI_GETVIDEODECODERBUFFERINFO pfnGetVideoDecoderBufferInfo;

VOID APIENTRY* pfnGetVideoDecoderBufferInfo(
  _In_        D3D10DDI_HDEVICE                     hDevice,
  _In_  const D3D11_1DDI_VIDEO_DECODER_DESC        *pDecodeDesc,
  _In_        UINT                                 Index,
  _Out_       D3D11_1DDI_VIDEO_DECODER_BUFFER_INFO *pInfo
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param *








### -param UINT


#### - Index [in]

The zero-based index of the video decoder buffer type that is used for the specified operation. The display miniport driver returns the maximum number of video decoder buffer types that are required for the operation through a call to its <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_getvideodecoderbuffertypecount.md">GetVideoDecoderBufferTypeCount</a> function.


#### - hDevice [in]

A handle to the display device (graphics context).




#### - pDecodeDesc [in]

A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_decoder_desc.md">D3D11_1DDI_VIDEO_DECODER_DESC</a> structure that specifies the video decoder operation.


#### - pInfo [out]

A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_decoder_buffer_info.md">D3D11_1DDI_VIDEO_DECODER_BUFFER_INFO</a> structure that describes the video decoder buffer.


## -returns



This callback function does not return a value.




## -remarks



The Microsoft Direct3D runtime verifies that the <i>pDecodeDesc</i>  and <i>Index</i> parameter data is valid before it calls the <b>GetVideoDecoderBufferInfo</b> function.




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_getvideodecoderbuffertypecount.md">GetVideoDecoderBufferTypeCount</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_decoder_desc.md">D3D11_1DDI_VIDEO_DECODER_DESC</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_decoder_buffer_info.md">D3D11_1DDI_VIDEO_DECODER_BUFFER_INFO</a>



 

 


