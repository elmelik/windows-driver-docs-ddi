---
UID: NC:d3d10umddi.PFND3D11DDI_COMMANDLISTEXECUTE
title: PFND3D11DDI_COMMANDLISTEXECUTE
author: windows-driver-content
description: The CommandListExecute function runs a command list.
old-location: display\commandlistexecute.htm
old-project: display
ms.assetid: 49f44f29-52f6-40d9-8617-a24aa3d30736
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CommandListExecute, CommandListExecute callback function [Display Devices], PFND3D11DDI_COMMANDLISTEXECUTE, UserModeDisplayDriverDx11_Functions_14a50e02-5483-4d83-83d7-79064981f4c8.xml, d3d10umddi/CommandListExecute, display.commandlistexecute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: CommandListExecute is supported beginning with the Windows 7 operating system.
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
-	CommandListExecute
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11DDI_COMMANDLISTEXECUTE callback


## -description


The <b>CommandListExecute</b> function runs a command list.


## -prototype


````
PFND3D11DDI_COMMANDLISTEXECUTE CommandListExecute;

VOID APIENTRY CommandListExecute(
  _In_ D3D10DDI_HDEVICE      hDevice,
  _In_ D3D11DDI_HCOMMANDLIST hCommandList
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param D3D11DDI_HCOMMANDLIST








#### - hCommandList [in]

 A handle to the driver's private data for the command list to run. 


#### - hDevice [in]

 A handle to the display device (graphics context).


## -returns



None

The driver can use the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> callback function to set an error code. For more information about setting error codes, see the Remarks section.




## -remarks



The driver is only required to implement <b>CommandListExecute</b> if the driver supports the D3D11DDICAPS_COMMANDLISTS_BUILD_2 capability that can be returned in the <a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_threading_caps.md">D3D11DDI_THREADING_CAPS</a> structure from a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10_2ddi_getcaps.md">GetCaps(D3D10_2)</a> function.

The driver can pass E_OUTOFMEMORY (if the driver runs out of memory) or D3DDDIERR_DEVICEREMOVED (if the device is removed) in a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a> function. The Direct3D runtime determines that any other errors are critical.




## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10ddi_seterror_cb.md">pfnSetErrorCb</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_devicefuncs.md">D3D11DDI_DEVICEFUNCS</a>



<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d10_2ddi_getcaps.md">GetCaps(D3D10_2)</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d11ddi_threading_caps.md">D3D11DDI_THREADING_CAPS</a>



 

 


