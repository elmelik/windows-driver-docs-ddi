---
UID: NS:ksmedia.tagKS_DATARANGE_VIDEO_PALETTE
title: tagKS_DATARANGE_VIDEO_PALETTE
author: windows-driver-content
description: The KS_DATARANGE_VIDEO_PALETTE structure describes a stream and its color capabilities.
old-location: stream\ks_datarange_video_palette.htm
old-project: stream
ms.assetid: 45488748-fc7e-47a6-8427-479c63d74a27
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: "*PKS_DATARANGE_VIDEO_PALETTE, KS_DATARANGE_VIDEO_PALETTE, KS_DATARANGE_VIDEO_PALETTE structure [Streaming Media Devices], PKS_DATARANGE_VIDEO_PALETTE, PKS_DATARANGE_VIDEO_PALETTE structure pointer [Streaming Media Devices], ksmedia/KS_DATARANGE_VIDEO_PALETTE, ksmedia/PKS_DATARANGE_VIDEO_PALETTE, stream.ks_datarange_video_palette, tagKS_DATARANGE_VIDEO_PALETTE, vidcapstruct_8bba39d4-8ffb-41df-b314-f63fe26d66fa.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.target-type: Windows
req.target-min-winverclnt: 
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
-	ksmedia.h
api_name:
-	KS_DATARANGE_VIDEO_PALETTE
product: Windows
targetos: Windows
req.typenames: KS_DATARANGE_VIDEO_PALETTE, *PKS_DATARANGE_VIDEO_PALETTE
---

# tagKS_DATARANGE_VIDEO_PALETTE structure


## -description


The KS_DATARANGE_VIDEO_PALETTE structure describes a stream and its color capabilities.


## -syntax


````
typedef struct tagKS_DATARANGE_VIDEO_PALETTE {
  KSDATARANGE                 DataRange;
  BOOL                        bFixedSizeSamples;
  BOOL                        bTemporalCompression;
  DWORD                       StreamDescriptionFlags;
  DWORD                       MemoryAllocationFlags;
  KS_VIDEO_STREAM_CONFIG_CAPS ConfigCaps;
  KS_VIDEOINFO                VideoInfo;
} KS_DATARANGE_VIDEO_PALETTE, *PKS_DATARANGE_VIDEO_PALETTE;
````


## -struct-fields




### -field DataRange

Specifies the major identifier for the format.


### -field bFixedSizeSamples

Specifies that all the samples are the same size if set to <b>TRUE</b>.


### -field bTemporalCompression

Specifies whether each sample can stand independently on its own, without relying on previous or future samples.


### -field StreamDescriptionFlags

Unused and should be set to zero.


### -field MemoryAllocationFlags

Unused and should be set to zero.


### -field ConfigCaps

Specifies the configuration of the stream, including scaling, cropping, and frame and data rates.


### -field VideoInfo

Specifies the details of the video stream.


## -see-also

<a href="..\ksmedia\ns-ksmedia-_ks_video_stream_config_caps.md">KS_VIDEO_STREAM_CONFIG_CAPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff561658">KSDATARANGE</a>



<a href="..\ksmedia\ns-ksmedia-tagks_videoinfo.md">KS_VIDEOINFO</a>



 

 


