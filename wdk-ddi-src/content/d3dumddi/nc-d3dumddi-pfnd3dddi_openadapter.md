---
UID: NC:d3dumddi.PFND3DDDI_OPENADAPTER
title: PFND3DDDI_OPENADAPTER
author: windows-driver-content
description: The OpenAdapter function creates a graphics adapter object that is referenced in subsequent calls.
old-location: display\openadapter.htm
old-project: display
ms.assetid: 41dc9ee4-e9bc-4ebd-9b90-6446ded6ea16
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: OpenAdapter, OpenAdapter callback function [Display Devices], PFND3DDDI_OPENADAPTER, UserModeDisplayDriver_Functions_1b93a0e5-3f89-47aa-9e63-3ae50f1acd1e.xml, d3dumddi/OpenAdapter, display.openadapter
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
-	OpenAdapter
product: Windows
targetos: Windows
req.typenames: DXGK_PTE
---

# PFND3DDDI_OPENADAPTER callback


## -description


The <i>OpenAdapter</i> function creates a graphics adapter object that is referenced in subsequent calls. 


## -prototype


````
PFND3DDDI_OPENADAPTER OpenAdapter;

__checkReturn HRESULT APIENTRY OpenAdapter(
  _Inout_ D3DDDIARG_OPENADAPTER *pOpenData
)
{ ... }
````


## -parameters




### -param *








#### - pOpenData [in, out]

 A pointer to a <a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_openadapter.md">D3DDDIARG_OPENADAPTER</a> structure. On input, this structure contains information that the driver can use. On output, the driver specifies information that the Microsoft Direct3D runtime can use.


## -returns



<i>OpenAdapter</i> returns one of the following values:

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
The graphics adapter object is successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
<i>OpenAdapter</i> could not allocate the required memory for it to complete.

</td>
</tr>
</table>
 




## -remarks



The graphics adapter object that is created by <i>OpenAdapter</i> represents the underlying graphics hardware. Before the Microsoft Direct3D runtime can create a display device by calling <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_createdevice.md">CreateDevice</a>, the user-mode display driver should call the <a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_queryadapterinfocb.md">pfnQueryAdapterInfoCb</a> function to query for the graphics hardware capabilities from the display miniport driver. 

The Direct3D runtime can open multiple graphics adapter objects from a single graphics adapter.




## -see-also

<a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_openadapter.md">D3DDDIARG_OPENADAPTER</a>



<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_createdevice.md">CreateDevice</a>



<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_queryadapterinfocb.md">pfnQueryAdapterInfoCb</a>



 

 


