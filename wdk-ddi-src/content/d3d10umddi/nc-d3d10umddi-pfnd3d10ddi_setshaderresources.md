---
UID: NC:d3d10umddi.PFND3D10DDI_SETSHADERRESOURCES
title: PFND3D10DDI_SETSHADERRESOURCES
author: windows-driver-content
description: The CsSetShaderResources function sets resources for a compute shader.
old-location: display\cssetshaderresources.htm
old-project: display
ms.assetid: 29570c3b-eb3b-4d8f-b471-8f3ea6226e23
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CsSetShaderResources, CsSetShaderResources callback function [Display Devices], PFND3D10DDI_SETSHADERRESOURCES, UserModeDisplayDriverDx11_Functions_0fe556e4-8c6f-4848-b502-d35744c60713.xml, d3d10umddi/CsSetShaderResources, display.cssetshaderresources
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: CsSetShaderResources is supported beginning with the Windows 7 operating system.
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
-	CsSetShaderResources
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D10DDI_SETSHADERRESOURCES callback


## -description


The <b>CsSetShaderResources</b> function sets resources for a compute shader.


## -prototype


````
PFND3D10DDI_SETSHADERRESOURCES CsSetShaderResources;

VOID APIENTRY CsSetShaderResources(
  _In_       D3D10DDI_HDEVICE             hDevice,
  _In_       UINT                         Offset,
  _In_       UINT                         NumViews,
  _In_ const D3D10DDI_HSHADERRESOURCEVIEW *phShaderResourceViews
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param StartSlot


### -param NumViews [in]

 The total number of views to set. 


### -param *








#### - Offset [in]

 The offset to the first view to set. 


#### - hDevice [in]

 A handle to the display device (graphics context).


#### - phShaderResourceViews [in]

 An array of handles to the shader resource views, beginning at the offset that <i>Offset</i> specifies.


## -returns



None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set an error code. For more information about setting error codes, see the following Remarks section.




## -remarks



The driver should not encounter any error, except for D3DDDIERR_DEVICEREMOVED. Therefore, if the driver passes any error, except for D3DDDIERR_DEVICEREMOVED, in a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> function, the Direct3D runtime determines that the error is critical. Even if the device is removed, the driver is not required to return D3DDDIERR_DEVICEREMOVED; however, if device removal interferes with the operation of <b>CsSetShaderResources</b> (which typically should not happen), the driver can return D3DDDIERR_DEVICEREMOVED.




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_devicefuncs.md">D3D11DDI_DEVICEFUNCS</a>



 

 


