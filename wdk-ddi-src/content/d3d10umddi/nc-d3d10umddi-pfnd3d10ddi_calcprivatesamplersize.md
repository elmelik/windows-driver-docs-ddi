---
UID: NC:d3d10umddi.PFND3D10DDI_CALCPRIVATESAMPLERSIZE
title: PFND3D10DDI_CALCPRIVATESAMPLERSIZE
author: windows-driver-content
description: The CalcPrivateSamplerSize function determines the size of the user-mode display driver's private region of memory (that is, the size of internal driver structures, not the size of the resource video memory) for a sampler.
old-location: display\calcprivatesamplersize.htm
old-project: display
ms.assetid: 7231ba65-f6ed-4b00-a61f-21d8fe26398f
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CalcPrivateSamplerSize, CalcPrivateSamplerSize callback function [Display Devices], PFND3D10DDI_CALCPRIVATESAMPLERSIZE, UserModeDisplayDriverDx10_Functions_66c06423-c710-4b1f-8084-d42c79066909.xml, d3d10umddi/CalcPrivateSamplerSize, display.calcprivatesamplersize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
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
-	d3d10umddi.h
api_name:
-	CalcPrivateSamplerSize
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D10DDI_CALCPRIVATESAMPLERSIZE callback


## -description


The <b>CalcPrivateSamplerSize</b> function determines the size of the user-mode display driver's private region of memory (that is, the size of internal driver structures, not the size of the resource video memory) for a sampler.


## -prototype


````
PFND3D10DDI_CALCPRIVATESAMPLERSIZE CalcPrivateSamplerSize;

SIZE_T APIENTRY CalcPrivateSamplerSize(
  _In_       D3D10DDI_HDEVICE       hDevice,
  _In_ const D3D10_DDI_SAMPLER_DESC *pSamplerDesc
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param *








#### - hDevice [in]

 A handle to the display device (graphics context).


#### - pSamplerDesc [in]

 A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d10_ddi_sampler_desc.md">D3D10_DDI_SAMPLER_DESC</a> structure that describes the parameters that the user-mode display driver uses to calculate the size of the memory region. 


## -returns



<b>CalcPrivateSamplerSize</b> returns the size of the memory region that the driver requires for creating a sampler.




## -see-also

<a href="..\d3d10umddi\ns-d3d10umddi-d3d10_ddi_sampler_desc.md">D3D10_DDI_SAMPLER_DESC</a>



<a href="..\d3d10umddi\ns-d3d10umddi-d3d10ddi_devicefuncs.md">D3D10DDI_DEVICEFUNCS</a>



 

 


