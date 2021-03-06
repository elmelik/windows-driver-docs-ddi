---
UID: NC:d3dkmddi.DXGKDDI_VIDPNTARGETMODESET_ACQUIRENEXTMODEINFO
title: DXGKDDI_VIDPNTARGETMODESET_ACQUIRENEXTMODEINFO
author: windows-driver-content
description: The pfnAcquireNextModeInfo function returns a descriptor of the next mode in a specified VidPN target mode set, given the current mode.
old-location: display\dxgk_vidpntargetmodeset_interface_pfnacquirenextmodeinfo.htm
old-project: display
ms.assetid: 894d0d15-d12a-4138-9a92-8f930c12dd52
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXGKDDI_VIDPNTARGETMODESET_ACQUIRENEXTMODEINFO, VidPnFunctions_27f5e19c-6a31-4e02-b9a2-8feaa5798fc3.xml, d3dkmddi/pfnAcquireNextModeInfo, display.dxgk_vidpntargetmodeset_interface_pfnacquirenextmodeinfo, pfnAcquireNextModeInfo, pfnAcquireNextModeInfo callback function [Display Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	d3dkmddi.h
api_name:
-	pfnAcquireNextModeInfo
product: Windows
targetos: Windows
req.typenames: DD_MULTISAMPLEQUALITYLEVELSDATA
---

# DXGKDDI_VIDPNTARGETMODESET_ACQUIRENEXTMODEINFO callback


## -description


The <b>pfnAcquireNextModeInfo</b> function returns a descriptor of the next mode in a specified VidPN target mode set, given the current mode.


## -prototype


````
DXGKDDI_VIDPNTARGETMODESET_ACQUIRENEXTMODEINFO pfnAcquireNextModeInfo;

NTSTATUS APIENTRY pfnAcquireNextModeInfo(
  _In_  const D3DKMDT_HVIDPNTARGETMODESET     hVidPnTargetModeSet,
  _In_  const D3DKMDT_VIDPN_TARGET_MODE CONST *pVidPnTargetModeInfo,
  _Out_ const D3DKMDT_VIDPN_TARGET_MODE       **ppNextVidPnTargetModeInfo
)
{ ... }
````


## -parameters




### -param hVidPnTargetModeSet [in]

[in] A handle to a VidPN target mode set object. The display miniport driver previously obtained this handle by calling the <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpn_acquiretargetmodeset.md">pfnAcquireTargetModeSet</a> function of the <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_vidpn_interface.md">DXGK_VIDPN_INTERFACE</a> interface.


### -param pVidPnTargetModeInfo [in]

[in] A pointer to a <a href="..\d3dkmdt\ns-d3dkmdt-_d3dkmdt_vidpn_target_mode.md">D3DKMDT_VIDPN_TARGET_MODE</a> structure that describes the current mode. The display miniport driver previously obtained this pointer by calling <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpntargetmodeset_acquirefirstmodeinfo.md">pfnAcquireFirstModeInfo</a> or <b>pfnAcquireNextModeInfo</b>.


### -param ppNextVidPnTargetModeInfo [out]

[out] A pointer to a variable that receives a pointer to a D3DKMDT_VIDPN_TARGET_MODE structure that describes the next mode.


## -returns



The <b>pfnAcquireNextModeInfo</b> function returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_GRAPHICS_INVALID_VIDPN_TARGETMODESET</b></dt>
</dl>
</td>
<td width="60%">
The handle supplied in <i>hVidPnTargetModeSet</i> was invalid.

</td>
</tr>
</table>
 




## -remarks



When you have finished using the <a href="..\d3dkmdt\ns-d3dkmdt-_d3dkmdt_vidpn_target_mode.md">D3DKMDT_VIDPN_TARGET_MODE</a> structure, you must release the structure by calling <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpntargetmodeset_releasemodeinfo.md">pfnReleaseModeInfo</a>.

You can enumerate all the modes that belong to a particular target mode set object by calling <a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpntargetmodeset_acquirefirstmodeinfo.md">pfnAcquireFirstModeInfo</a> and then making a sequence of calls to <b>pfnAcquireNextModeInfo</b>.

The D3DKMDT_HVIDPNTARGETMODESET data type is defined in <i>D3dkmdt.h</i>. 




## -see-also

<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpntargetmodeset_acquirefirstmodeinfo.md">pfnAcquireFirstModeInfo</a>



<a href="..\d3dkmddi\nc-d3dkmddi-dxgkddi_vidpntargetmodeset_releasemodeinfo.md">pfnReleaseModeInfo</a>



<a href="..\d3dkmdt\ns-d3dkmdt-_d3dkmdt_vidpn_target_mode.md">D3DKMDT_VIDPN_TARGET_MODE</a>



 

 


