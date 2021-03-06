---
UID: NF:wdm.ClfsFlushBuffers
title: ClfsFlushBuffers function
author: windows-driver-content
description: The ClfsFlushBuffers routine forces all log I/O blocks in a specified marshalling area to stable storage.
old-location: kernel\clfsflushbuffers.htm
old-project: kernel
ms.assetid: 70e93c8f-a23c-4399-9299-c2743d097ded
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: ClfsFlushBuffers, ClfsFlushBuffers routine [Kernel-Mode Driver Architecture], Clfs_3c04240c-0914-472f-9b4b-97a00221e092.xml, kernel.clfsflushbuffers, wdm/ClfsFlushBuffers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Server 2003 R2, Windows Vista, and later versions of Windows.
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
req.lib: Clfs.lib
req.dll: Clfs.sys
req.irql: "<= APC_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfs.sys
-	Ext-MS-Win-fs-clfs-l1-1-0.dll
api_name:
-	ClfsFlushBuffers
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# ClfsFlushBuffers function


## -description


The <b>ClfsFlushBuffers</b> routine forces all log I/O blocks in a specified marshalling area to stable storage.


## -syntax


````
NTSTATUS ClfsFlushBuffers(
  _In_ PVOID pvMarshalContext
);
````


## -parameters




### -param pvMarshalContext [in]

A pointer to an opaque context that represents a marshalling area. The caller previously obtained this pointer by calling <a href="..\wdm\nf-wdm-clfscreatemarshallingarea.md">ClfsCreateMarshallingArea</a>.


## -returns



<b>ClfsFlushBuffers</b> returns STATUS_SUCCESS if it succeeds; otherwise, it returns one of the error codes defined in Ntstatus.h.




## -remarks



Calling <b>ClfsFlushBuffers</b> is equivalent to calling <a href="..\wdm\nf-wdm-clfsflushtolsn.md">ClfsFlushToLsn</a> with the <i>plsnFlush</i> parameter set to CLFS_LSN_NULL.

For an explanation of CLFS concepts and terminology, see <a href="https://msdn.microsoft.com/a9685648-b08c-48ca-b020-e683068f2ea2">Common Log File System</a>. 




## -see-also

<a href="..\wdm\nf-wdm-clfsflushtolsn.md">ClfsFlushToLsn</a>



 

 


