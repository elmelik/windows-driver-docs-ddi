---
UID: NC:d3dumddi.PFND3DDDI_UPDATEOVERLAY
title: PFND3DDDI_UPDATEOVERLAY
author: windows-driver-content
description: The UpdateOverlay function reconfigures or moves an overlay that is being displayed.
old-location: display\updateoverlay.htm
old-project: display
ms.assetid: 80d7cc5c-51d8-4b91-9581-b073f9b0e68a
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3DDDI_UPDATEOVERLAY, UpdateOverlay, UpdateOverlay callback function [Display Devices], UserModeDisplayDriver_Functions_58c588ce-de18-4aa0-bb22-0c33d053e22f.xml, d3dumddi/UpdateOverlay, display.updateoverlay
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
-	UpdateOverlay
product: Windows
targetos: Windows
req.typenames: DXGK_PTE
---

# PFND3DDDI_UPDATEOVERLAY callback


## -description


The <i>UpdateOverlay</i> function reconfigures or moves an overlay that is being displayed.


## -prototype


````
PFND3DDDI_UPDATEOVERLAY UpdateOverlay;

__checkReturn HRESULT APIENTRY UpdateOverlay(
  _In_       HANDLE                  hDevice,
  _In_ const D3DDDIARG_UPDATEOVERLAY *pData
)
{ ... }
````


## -parameters




### -param hDevice [in]

 A handle to the display device (graphics context).


### -param *








#### - pData [in]

 A pointer to a <a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_updateoverlay.md">D3DDDIARG_UPDATEOVERLAY</a> structure that describes how to reconfigure the overlay.


## -returns



<i>UpdateOverlay</i> returns one of the following values:

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
The overlay is successfully modified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
<i>UpdateOverlay</i> could not complete because of insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DDDIERR_NOTAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
<i>UpdateOverlay</i> could not complete because insufficient bandwidth was available or the requested overlay hardware was unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DDDIERR_UNSUPPORTEDOVERLAYFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The specified overlay format is not supported by the overlay hardware. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>D3DDDIERR_UNSUPPORTEDOVERLAY</b></dt>
</dl>
</td>
<td width="60%">
The overlay hardware is not supported for the specified size and display mode. 

</td>
</tr>
</table>
 




## -remarks



Overlays are independent from the resources that are displayed by using the overlays.




## -see-also

<a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_updateoverlay.md">D3DDDIARG_UPDATEOVERLAY</a>



<a href="..\d3dumddi\ns-d3dumddi-_d3dddi_devicefuncs.md">D3DDDI_DEVICEFUNCS</a>



 

 


