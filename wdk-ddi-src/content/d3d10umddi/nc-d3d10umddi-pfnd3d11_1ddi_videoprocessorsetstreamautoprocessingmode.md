---
UID: NC:d3d10umddi.PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMAUTOPROCESSINGMODE
title: PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMAUTOPROCESSINGMODE
author: windows-driver-content
description: Enables or disables automatic processing features for an input stream on the video processor.
old-location: display\videoprocessorsetstreamautoprocessingmode.htm
old-project: display
ms.assetid: 85c504e3-46b4-434a-8ab9-5c866eafe05a
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMAUTOPROCESSINGMODE, d3d10umddi/pfnVideoProcessorSetStreamAutoProcessingMode, display.videoprocessorsetstreamautoprocessingmode, pfnVideoProcessorSetStreamAutoProcessingMode, pfnVideoProcessorSetStreamAutoProcessingMode callback function [Display Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
-	D3d10umddi.h
api_name:
-	pfnVideoProcessorSetStreamAutoProcessingMode
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMAUTOPROCESSINGMODE callback


## -description


Enables or disables automatic processing features for an input stream on the video processor.




## -prototype


````
PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMAUTOPROCESSINGMODE pfnVideoProcessorSetStreamAutoProcessingMode;

VOID APIENTRY* pfnVideoProcessorSetStreamAutoProcessingMode(
  _In_ D3D10DDI_HDEVICE           hDevice,
  _In_ D3D11_1DDI_HVIDEOPROCESSOR hVideoProcessor,
  _In_ UINT                       StreamIndex,
  _In_ BOOL                       Enable
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE


### -param D3D11_1DDI_HVIDEOPROCESSOR


### -param UINT


### -param BOOL








#### - Enable [in]

If <b>TRUE</b>, automatic processing features are enabled. If <b>FALSE</b>, the driver disables any additional video processing that it might be performing.




#### - StreamIndex [in]

The zero-based index of the input stream.


#### - hDevice [in]

A handle to the display device (graphics context).




#### - hVideoProcessor [in]

A handle to the video processor object that was created through a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createvideoprocessor.md">CreateVideoProcessor</a> function. 




## -returns



This callback function does not return a value.




## -remarks



By default, the driver might perform certain processing tasks automatically during the video processor bit-block transfer (bitblt). The <b>VideoProcessorSetStreamAutoProcessingMode</b> function enables the application to disable these additional video processing features that the driver may expose. 

For example, if the independent software vendor (ISV) provides its own pixel shader for the video processor, it might want to disable the driver's automatic processing.






## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createvideoprocessor.md">CreateVideoProcessor</a>



 

 


