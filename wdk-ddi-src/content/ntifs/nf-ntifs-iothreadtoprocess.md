---
UID: NF:ntifs.IoThreadToProcess
title: IoThreadToProcess function
author: windows-driver-content
description: The IoThreadToProcess routine returns a pointer to the process for the specified thread.
old-location: ifsk\iothreadtoprocess.htm
old-project: ifsk
ms.assetid: fcb51574-d966-4cd5-a946-c38dd2798b7f
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: IoThreadToProcess, IoThreadToProcess routine [Installable File System Drivers], ifsk.iothreadtoprocess, ioref_59269b9a-0a64-410d-aafa-b070b2eacfd7.xml, ntifs/IoThreadToProcess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	IoThreadToProcess
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# IoThreadToProcess function


## -description


The <b>IoThreadToProcess</b> routine returns a pointer to the process for the specified thread.


## -syntax


````
PEPROCESS IoThreadToProcess(
  _In_ PETHREAD Thread
);
````


## -parameters




### -param Thread [in]

Thread whose process is to be returned.


## -returns



<b>IoThreadToProcess</b> returns a pointer to the thread's process.

For more information about using system threads and managing synchronization within a nonarbitrary thread context, see <a href="https://msdn.microsoft.com/fbd8aadd-5a24-48c9-9865-80cc7dc97316">Driver Threads, Dispatcher Objects, and Resources</a>. 




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff559933">PsGetCurrentProcess</a>



<a href="..\wdm\nf-wdm-psgetcurrentthread.md">PsGetCurrentThread</a>



<a href="..\wdm\nf-wdm-iogetcurrentprocess.md">IoGetCurrentProcess</a>



 

 


