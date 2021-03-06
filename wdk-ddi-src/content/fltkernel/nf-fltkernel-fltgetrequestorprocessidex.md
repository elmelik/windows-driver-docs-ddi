---
UID: NF:fltkernel.FltGetRequestorProcessIdEx
title: FltGetRequestorProcessIdEx function
author: windows-driver-content
description: The FltGetRequestorProcessIdEx routine returns the kernel-mode handle for the process that is associated with the thread that requested a given I/O operation.
old-location: ifsk\fltgetrequestorprocessidex.htm
old-project: ifsk
ms.assetid: e6a8b2ca-7e9d-410a-b44b-7e873b6e5833
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: FltApiRef_e_to_o_ec80528f-12a7-4d31-9bd8-92050a16bd85.xml, FltGetRequestorProcessIdEx, FltGetRequestorProcessIdEx routine [Installable File System Drivers], fltkernel/FltGetRequestorProcessIdEx, ifsk.fltgetrequestorprocessidex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fltkernel.h
req.include-header: Fltkernel.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Vista or later versions of the Windows operating system.
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
req.lib: FltMgr.lib
req.dll: Fltmgr.sys
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	fltmgr.sys
api_name:
-	FltGetRequestorProcessIdEx
product: Windows
targetos: Windows
req.typenames: EXpsFontRestriction
---

# FltGetRequestorProcessIdEx function


## -description


The <b>FltGetRequestorProcessIdEx</b> routine returns the kernel-mode handle for the process that is associated with the thread that requested a given I/O operation. 


## -syntax


````
HANDLE FltGetRequestorProcessIdEx(
  _In_ PFLT_CALLBACK_DATA CallbackData
);
````


## -parameters




### -param CallbackData [in]

A pointer to an <a href="..\fltkernel\ns-fltkernel-_flt_callback_data.md">FLT_CALLBACK_DATA</a> structure that identifies the thread and the I/O operation. 


## -returns



The <b>FltGetRequestorProcessIdEx</b> routine returns the kernel-mode handle for the process that is associated with the thread that originally requested the I/O operation. If the operation is not associated with any thread, FltGetRequestorProcessIdEx returns <b>NULL</b>. 




## -remarks



The <b>FltGetRequestorProcessIdEx</b> routine returns the kernel-mode handle for the process that the requesting thread is currently attached to. This process may or may not be the same process that created the thread. 




## -see-also

<a href="..\fltkernel\nf-fltkernel-fltgetrequestorprocess.md">FltGetRequestorProcess</a>



<a href="..\fltkernel\ns-fltkernel-_flt_callback_data.md">FLT_CALLBACK_DATA</a>



 

 


