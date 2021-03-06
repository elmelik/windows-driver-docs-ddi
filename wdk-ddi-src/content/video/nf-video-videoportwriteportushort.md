---
UID: NF:video.VideoPortWritePortUshort
title: VideoPortWritePortUshort function
author: windows-driver-content
description: The VideoPortWritePortUshort function writes a USHORT value to a mapped I/O port.
old-location: display\videoportwriteportushort.htm
old-project: display
ms.assetid: c0431b2a-c075-48e4-9476-42c42a86f8ed
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: VideoPortWritePortUshort, VideoPortWritePortUshort function [Display Devices], VideoPort_Functions_919dd8ab-f319-4071-b375-b269823adb31.xml, display.videoportwriteportushort, video/VideoPortWritePortUshort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: video.h
req.include-header: Video.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Videoprt.lib
req.dll: Videoprt.sys
req.irql: Any level (see Remarks section)
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Videoprt.sys
api_name:
-	VideoPortWritePortUshort
product: Windows
targetos: Windows
req.typenames: VIDEO_PORT_SERVICES
req.product: Windows 10 or later.
---

# VideoPortWritePortUshort function


## -description


The <b>VideoPortWritePortUshort</b> function writes a USHORT value to a mapped I/O port.


## -syntax


````
VOID VideoPortWritePortUshort(
   PUSHORT Port,
   USHORT  Value
);
````


## -parameters




### -param Port

Pointer to the port. The given <i>Port</i> must be in a mapped I/O-space range returned by <a href="..\video\nf-video-videoportgetdevicebase.md">VideoPortGetDeviceBase</a>.


### -param Value

Specifies a USHORT value to be transferred to the adapter.


## -returns



None




## -remarks



A miniport driver's <a href="..\video\nc-video-pvideo_hw_interrupt.md">HwVidInterrupt</a> or <a href="..\video\nc-video-pminiport_synchronize_routine.md">HwVidSynchronizeExecutionCallback</a> function can call <b>VideoPortWritePortUshort</b>.

Callers of <b>VideoPortWritePortUshort</b> can be running at any IRQL, provided that the memory pointed to by the <i>Port</i> parameter is resident, mapped device memory.




## -see-also

<a href="..\video\nf-video-videoportgetdevicebase.md">VideoPortGetDeviceBase</a>



 

 


