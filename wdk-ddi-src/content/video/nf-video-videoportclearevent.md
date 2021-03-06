---
UID: NF:video.VideoPortClearEvent
title: VideoPortClearEvent function
author: windows-driver-content
description: The VideoPortClearEvent function sets a given event object to the nonsignaled state.
old-location: display\videoportclearevent.htm
old-project: display
ms.assetid: 70b9b8b4-8adc-4628-a37b-b513ecaca9ca
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: VideoPortClearEvent, VideoPortClearEvent function [Display Devices], VideoPort_Functions_4b6d9a3c-ee76-4c45-888f-4ef37f802e6b.xml, display.videoportclearevent, video/VideoPortClearEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: video.h
req.include-header: Video.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later versions of the Windows operating systems.
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
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Videoprt.sys
api_name:
-	VideoPortClearEvent
product: Windows
targetos: Windows
req.typenames: VIDEO_PORT_SERVICES
req.product: Windows 10 or later.
---

# VideoPortClearEvent function


## -description


The <b>VideoPortClearEvent</b> function sets a given event object to the nonsignaled state.


## -syntax


````
VOID VideoPortClearEvent(
  _In_ PVOID  HwDeviceExtension,
  _In_ PEVENT pEvent
);
````


## -parameters




### -param HwDeviceExtension [in]

Pointer to the miniport driver's device extension.


### -param pEvent [in]

Pointer to the event object.


## -returns



None




## -remarks



To set the state of an event object to the signaled state, use <a href="..\video\nf-video-videoportsetevent.md">VideoPortSetEvent</a>. 




## -see-also

<a href="..\video\nf-video-videoportsetevent.md">VideoPortSetEvent</a>



 

 


