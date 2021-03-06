---
UID: NC:d3d10umddi.PFND3D11DDI_CHECKDEFERREDCONTEXTHANDLESIZES
title: PFND3D11DDI_CHECKDEFERREDCONTEXTHANDLESIZES
author: windows-driver-content
description: The CheckDeferredContextHandleSizes function verifies the sizes of the driver-private memory spaces that hold the handle data of deferred context handles.
old-location: display\checkdeferredcontexthandlesizes.htm
old-project: display
ms.assetid: 0ddaec86-79e6-4d09-8403-6588b35f8b0f
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CheckDeferredContextHandleSizes, CheckDeferredContextHandleSizes callback function [Display Devices], PFND3D11DDI_CHECKDEFERREDCONTEXTHANDLESIZES, UserModeDisplayDriverDx11_Functions_f96ddf8f-1b3c-4840-b76c-2386dfb582f8.xml, d3d10umddi/CheckDeferredContextHandleSizes, display.checkdeferredcontexthandlesizes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: CheckDeferredContextHandleSizes is supported beginning with the Windows 7 operating system.
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
-	CheckDeferredContextHandleSizes
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11DDI_CHECKDEFERREDCONTEXTHANDLESIZES callback


## -description


The <b>CheckDeferredContextHandleSizes</b> function verifies the sizes of the driver-private memory spaces that hold the handle data of deferred context handles.


## -prototype


````
PFND3D11DDI_CHECKDEFERREDCONTEXTHANDLESIZES CheckDeferredContextHandleSizes;

VOID APIENTRY CheckDeferredContextHandleSizes(
  _In_      D3D10DDI_HDEVICE    hDevice,
  _Inout_   UINT                *pHSizes,
  _Out_opt_ D3D11DDI_HANDLESIZE *pHandleSize
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param *pHSizes [in, out]

The size, in bytes, of the array pointed to by <i>pHandleSize</i>.


### -param *








#### - hDevice [in]

 A handle to the display device (graphics context).


#### - pHandleSize [out, optional]

 An array of <a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_handlesize.md">D3D11DDI_HANDLESIZE</a> structures that describe the handle data of deferred context handles.


## -returns



None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set a critical error code. For more information about setting error codes, see the Remarks section.




## -remarks



The driver is only required to implement <i>CheckDeferredContextHandleSizes</i> if the driver supports the <b>D3D11DDICAPS_COMMANDLISTS_BUILD_2</b> capability that can be returned in the <a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_threading_caps.md">D3D11DDI_THREADING_CAPS</a> structure from a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10_2ddi_getcaps.md">GetCaps(D3D10_2)</a> function.

For more information about how <i>CheckDeferredContextHandleSizes</i> is used, see <a href="https://msdn.microsoft.com/1b3e5c29-9b9e-4c10-8fe0-706255c8fd91">Using Context-Local DDI Handles</a>. 

The driver's <i>CheckDeferredContextHandleSizes</i> function cannot call the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set the <b>D3DDDIERR_DEVICEREMOVED</b> error code because <i>CheckDeferredContextHandleSizes</i> is a capability-check type of function. The driver must ensure that it has enough information after device creation to respond to a call to <i>CheckDeferredContextHandleSizes</i>, even in the presence of <b>D3DDDIERR_DEVICEREMOVED</b>.

<i>CheckDeferredContextHandleSizes</i> should not encounter any errors. However, <i>CheckDeferredContextHandleSizes</i> might call <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> for critical errors.




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_devicefuncs.md">D3D11DDI_DEVICEFUNCS</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11ddi_checkdeferredcontexthandlesizes.md">CheckDeferredContextHandleSizes</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10_2ddi_getcaps.md">GetCaps(D3D10_2)</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_threading_caps.md">D3D11DDI_THREADING_CAPS</a>



 

 


