---
UID: NS:d3dkmddi._DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES
title: "_DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES"
author: windows-driver-content
description: DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES describes the operation used copy page table entries from one location to another.
old-location: display\dxgk_buildpagingbuffer_copypagetableentries.htm
old-project: display
ms.assetid: 627FB3E6-3C5D-4104-B129-08D3EC0B963E
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES, DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES structure [Display Devices], _DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES, d3dkmddi/DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES, display.dxgk_buildpagingbuffer_copypagetableentries
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dkmddi.h
req.include-header: D3dkmddi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
-	HeaderDef
api_location:
-	d3dkmddi.h
api_name:
-	DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES
product: Windows
targetos: Windows
req.typenames: DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES
---

# _DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES structure


## -description


<b>DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES</b> describes the operation used copy page table entries from one location to another. 


## -syntax


````
typedef struct _DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES {
  UINT                              NumRanges;
  DXGK_BUILDPAGINGBUFFER_COPY_RANGE *pRanges;
} DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES;
````


## -struct-fields




### -field NumRanges

The number of elements in the <b>pRanges</b> array.


### -field pRanges

A pointer to a <a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_buildpagingbuffer_copy_range.md">DXGK_BUILDPAGINGBUFFER_COPY_RANGE</a> structure describing each range of page table entries to copy.


## -see-also

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_buildpagingbuffer.md">DXGKARG_BUILDPAGINGBUFFER</a>



<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_buildpagingbuffer_copy_range.md">DXGK_BUILDPAGINGBUFFER_COPY_RANGE</a>



 

 


