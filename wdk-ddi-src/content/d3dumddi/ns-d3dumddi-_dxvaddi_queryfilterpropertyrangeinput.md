---
UID: NS:d3dumddi._DXVADDI_QUERYFILTERPROPERTYRANGEINPUT
title: "_DXVADDI_QUERYFILTERPROPERTYRANGEINPUT"
author: windows-driver-content
description: The DXVADDI_QUERYFILTERPROPERTYRANGEINPUT structure describes a filter setting on a video stream that range information is requested for.
old-location: display\dxvaddi_queryfilterpropertyrangeinput.htm
old-project: display
ms.assetid: d073d326-6cc6-4216-b312-809d707aef3b
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXVA2_Structs_28a2aed9-57a1-4bd6-b8dc-c09bb9e821b0.xml, DXVADDI_QUERYFILTERPROPERTYRANGEINPUT, DXVADDI_QUERYFILTERPROPERTYRANGEINPUT structure [Display Devices], _DXVADDI_QUERYFILTERPROPERTYRANGEINPUT, d3dumddi/DXVADDI_QUERYFILTERPROPERTYRANGEINPUT, display.dxvaddi_queryfilterpropertyrangeinput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Windows
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
-	HeaderDef
api_location:
-	d3dumddi.h
api_name:
-	DXVADDI_QUERYFILTERPROPERTYRANGEINPUT
product: Windows
targetos: Windows
req.typenames: DXVADDI_QUERYFILTERPROPERTYRANGEINPUT
---

# _DXVADDI_QUERYFILTERPROPERTYRANGEINPUT structure


## -description


The DXVADDI_QUERYFILTERPROPERTYRANGEINPUT structure describes a filter setting on a video stream that range information is requested for.


## -syntax


````
typedef struct _DXVADDI_QUERYFILTERPROPERTYRANGEINPUT {
  const GUID        *pVideoProcGuid;
  DXVADDI_VIDEODESC VideoDesc;
  D3DDDIFORMAT      RenderTargetFormat;
  UINT              FilterSetting;
} DXVADDI_QUERYFILTERPROPERTYRANGEINPUT;
````


## -struct-fields




### -field pVideoProcGuid

[in] A pointer to a GUID that represents the video processing device type. 


### -field VideoDesc

[in] A <a href="..\d3dumddi\ns-d3dumddi-_dxvaddi_videodesc.md">DXVADDI_VIDEODESC</a> structure that describes the video stream.


### -field RenderTargetFormat

[in] A <a href="..\d3dukmdt\ne-d3dukmdt-_d3dddiformat.md">D3DDDIFORMAT</a>-typed value that indicates the pixel format of the render target for the video processing device.


### -field FilterSetting

[in] A filter setting that range information is requested for. This member can be one of the following settings:

<ul>
<li>
DXVADDI_NOISEFILTER_LUMALEVEL

</li>
<li>
DXVADDI_NOISEFILTER_LUMATHREASHOLD

</li>
<li>
DXVADDI_NOISEFILTER_LUMARADIUS

</li>
<li>
DXVADDI_NOISEFILTER_CHROMALEVEL

</li>
<li>
DXVADDI_NOISEFILTER_CHROMATHREASHOLD

</li>
<li>
DXVADDI_NOISEFILTER_CHROMARADIUS

</li>
<li>
DXVADDI_DETAILFILTER_LUMALEVEL

</li>
<li>
DXVADDI_DETAILFILTER_LUMATHREASHOLD

</li>
<li>
DXVADDI_DETAILFILTER_LUMARADIUS

</li>
<li>
DXVADDI_DETAILFILTER_CHROMALEVEL

</li>
<li>
DXVADDI_DETAILFILTER_CHROMATHREASHOLD

</li>
<li>
DXVADDI_DETAILFILTER_CHROMARADIUS

</li>
</ul>

## -see-also

<a href="..\d3dumddi\ns-d3dumddi-_dxvaddi_valuerange.md">DXVADDI_VALUERANGE</a>



<a href="..\d3dumddi\ne-d3dumddi-_d3dddicaps_type.md">D3DDDICAPS_TYPE</a>



<a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_getcaps.md">D3DDDIARG_GETCAPS</a>



<a href="..\d3dumddi\nc-d3dumddi-pfnd3dddi_getcaps.md">GetCaps</a>



<a href="..\d3dumddi\ns-d3dumddi-_dxvaddi_videodesc.md">DXVADDI_VIDEODESC</a>



 

 


