---
UID: NC:d3dumddi.PFND3DDDI_SETMARKER
title: PFND3DDDI_SETMARKER
author: windows-driver-content
description: Notifies the user-mode display driver that it must generate a new time stamp if any GPU work has completed since the last call to pfnSetMarker.
old-location: display\pfnsetmarker.htm
old-project: display
ms.assetid: 6D4DB988-D339-4B2F-A9B8-41B4FD21FE66
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3DDDI_SETMARKER, d3dumddi/pfnSetMarker, display.pfnsetmarker, pfnSetMarker, pfnSetMarker callback function [Display Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dumddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8.1,WDDM 1.3 and later
req.target-min-winversvr: Windows Server 2012 R2
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
-	D3dumddi.h
api_name:
-	pfnSetMarker
product: Windows
targetos: Windows
req.typenames: DXGK_PTE
---

# PFND3DDDI_SETMARKER callback


## -description


Notifies the user-mode display driver that it must generate a new time stamp if any GPU work has completed since the last call to <i>pfnSetMarker</i>. Optionally implemented by Windows Display Driver Model (WDDM) 1.3 and later drivers running on Microsoft Direct3D Level 9 hardware. (See requirements in  <a href="https://msdn.microsoft.com/F9AAE489-EC45-4EE6-875E-E084BB3054EE">Direct3D rendering performance improvements</a>.)  For more advanced hardware, drivers should implement the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3dwddm1_3ddi_setmarker.md">SetMarker</a> function.


## -prototype


````
PFND3DDDI_SETMARKER pfnSetMarker;

_Check_return_ HRESULT APIENTRY* pfnSetMarker(
  _In_ HANDLE hDevice
)
{ ... }
````


## -parameters




### -param hDevice [in]

A handle to the display device (graphics context).


## -returns




      Returns <b>S_OK</b> or an appropriate error result if the function does not complete successfully.




## -remarks



If the marker event type from the  <i>Type</i> parameter of the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_setmarkermode.md">pfnSetMarkerMode</a> function is not <b>D3DDDIMT_NONE</b>, the user-mode display driver must perform this procedure with each call to <i>pfnSetMarker</i>:

<ol>
<li>Increment the value of the <b>APISequenceNumber</b> member of the <a href="..\d3dumddi\ns-d3dumddi-d3dddicb_logumdmarker.md">D3DDDICB_LOGUMDMARKER</a> structure.</li>
<li>Determine which contexts associated with single-threaded device driver interface (DDI) render calls submitted work with the last call to <i>pfnSetMarker</i>. For each such context:<ol>
<li>If the command buffer for the context is empty, do nothing.</li>
<li>Otherwise:<ul>
<li>Ensure that more memory is available in the context's history buffer. Flush the buffer if necessary.</li>
<li>Add another entry to the context's API sequence number buffer that contains the low 32 bits of the current <b>APISequenceNumber</b> value.</li>
<li>Sample and write out time stamps that are appropriate for the current marker event type.</li>
</ul>
</li>
<li>Update tracking data that will be used the next time that <i>pfnSetMarker</i> is called.</li>
</ol>
</li>
</ol>



## -see-also

<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_setmarkermode.md">pfnSetMarkerMode</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3dwddm1_3ddi_setmarker.md">SetMarker</a>



 

 


