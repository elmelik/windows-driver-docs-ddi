---
UID: NC:d3dumddi.PFND3DDDI_VIDEOPROCESSENDFRAME
title: PFND3DDDI_VIDEOPROCESSENDFRAME
author: windows-driver-content
description: The VideoProcessEndFrame function notifies the user-mode display driver that all of the data that is required to process the current frame was submitted.
old-location: display\videoprocessendframe.htm
old-project: display
ms.assetid: a5be6834-bb27-4da0-8802-25a9ca58c101
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3DDDI_VIDEOPROCESSENDFRAME, UserModeDisplayDriver_Functions_b7ef391b-90b5-49a6-880e-d0c4f287d0ad.xml, VideoProcessEndFrame, VideoProcessEndFrame callback function [Display Devices], d3dumddi/VideoProcessEndFrame, display.videoprocessendframe
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dumddi.h
req.include-header: D3dumddi.h
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
-	d3dumddi.h
api_name:
-	VideoProcessEndFrame
product: Windows
targetos: Windows
req.typenames: DXGK_PTE
---

# PFND3DDDI_VIDEOPROCESSENDFRAME callback


## -description


The <i>VideoProcessEndFrame</i> function notifies the user-mode display driver that all of the data that is required to process the current frame was submitted.


## -prototype


````
PFND3DDDI_VIDEOPROCESSENDFRAME VideoProcessEndFrame;

__checkReturn HRESULT APIENTRY VideoProcessEndFrame(
  _In_    HANDLE                         hDevice,
  _Inout_ D3DDDIARG_VIDEOPROCESSENDFRAME *pData
)
{ ... }
````


## -parameters




### -param hDevice [in]

 A handle to the display device (graphics context).


### -param *








#### - pData [in, out]

 A pointer to a <a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_videoprocessendframe.md">D3DDDIARG_VIDEOPROCESSENDFRAME</a> structure that describes the DirectX VA video processor that should stop processing a frame.


## -returns



<i>VideoProcessEndFrame</i> returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Processing of the current frame is successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
<i>VideoProcessEndFrame</i> cannot allocate memory required for it to complete.

</td>
</tr>
</table>
 




## -remarks



The <i>VideoProcessEndFrame</i> function notifies the user-mode display driver that its <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_videoprocessblt.md">VideoProcessBlt</a> function can no longer be called on the specified video processing device.




## -see-also

<a href="..\d3dumddi\ns-d3dumddi-_d3dddi_devicefuncs.md">D3DDDI_DEVICEFUNCS</a>



<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_videoprocessblt.md">VideoProcessBlt</a>



<a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_videoprocessendframe.md">D3DDDIARG_VIDEOPROCESSENDFRAME</a>



<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_createvideoprocessdevice.md">CreateVideoProcessDevice</a>



 

 


