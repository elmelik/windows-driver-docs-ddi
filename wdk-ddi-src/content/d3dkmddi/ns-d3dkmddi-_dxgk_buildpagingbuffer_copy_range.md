---
UID: NS:d3dkmddi._DXGK_BUILDPAGINGBUFFER_COPY_RANGE
title: "_DXGK_BUILDPAGINGBUFFER_COPY_RANGE"
author: windows-driver-content
description: DXGK_BUILDPAGINGBUFFER_COPY_RANGE is used as part of a page table entry copy operation.
old-location: display\dxgk_buildpagingbuffer_copy_range.htm
old-project: display
ms.assetid: BA35F50C-7399-41DC-A10B-2F5E4BB24B49
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DXGK_BUILDPAGINGBUFFER_COPY_RANGE, DXGK_BUILDPAGINGBUFFER_COPY_RANGE structure [Display Devices], _DXGK_BUILDPAGINGBUFFER_COPY_RANGE, d3dkmddi/DXGK_BUILDPAGINGBUFFER_COPY_RANGE, display.dxgk_buildpagingbuffer_copy_range
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
-	DXGK_BUILDPAGINGBUFFER_COPY_RANGE
product: Windows
targetos: Windows
req.typenames: DXGK_BUILDPAGINGBUFFER_COPY_RANGE
---

# _DXGK_BUILDPAGINGBUFFER_COPY_RANGE structure


## -description


<b>DXGK_BUILDPAGINGBUFFER_COPY_RANGE</b> is used as part of a page table entry copy operation.


## -syntax


````
typedef struct _DXGK_BUILDPAGINGBUFFER_COPY_RANGE {
  UINT                   NumPageTableEntries;
  D3DGPU_VIRTUAL_ADDRESS SrcPageTableAddress;
  D3DGPU_VIRTUAL_ADDRESS DstPageTableAddress;
  UINT                   SrcStartPteIndex;
  UINT                   DstStartPteIndex;
} DXGK_BUILDPAGINGBUFFER_COPY_RANGE;
````


## -struct-fields




### -field NumPageTableEntries

The number of page table entries to copy.


### -field SrcPageTableAddress

The virtual address of the source page table for the range. The address is aligned to 64KB boundary.


### -field DstPageTableAddress

The virtual address of the destination page table for the range. The address is aligned to 64KB boundary.


### -field SrcStartPteIndex

The index of the first page table entry in the source page table for the range.


### -field DstStartPteIndex

The index of the first page table entry in the destination page table for the range.


## -see-also

<a href="..\d3dkmddi\ns-d3dkmddi-_dxgkarg_buildpagingbuffer.md">DXGKARG_BUILDPAGINGBUFFER</a>



<a href="..\d3dkmddi\ns-d3dkmddi-_dxgk_buildpagingbuffer_copypagetableentries.md">DXGK_BUILDPAGINGBUFFER_COPYPAGETABLEENTRIES</a>



 

 


