---
UID: NF:wdm.RtlStringFromGUID
title: RtlStringFromGUID function
author: windows-driver-content
description: The RtlStringFromGUID routine converts a given GUID from binary format into a Unicode string.
old-location: kernel\rtlstringfromguid.htm
old-project: kernel
ms.assetid: 89a3ca92-7c8a-40e3-a818-0127af6f2e91
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: RtlStringFromGUID, RtlStringFromGUID routine [Kernel-Mode Driver Architecture], k109_8a3ac592-7ade-48fc-9536-d8a6c84fb033.xml, kernel.rtlstringfromguid, wdm/RtlStringFromGUID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
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
req.dll: NtosKrnl.exe (kernel mode); Ntdll.dll (user mode)
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
-	Ntdll.dll
api_name:
-	RtlStringFromGUID
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# RtlStringFromGUID function


## -description


The <b>RtlStringFromGUID</b> routine converts a given GUID from binary format into a Unicode string. 


## -syntax


````
NTSTATUS RtlStringFromGUID(
  _In_  REFGUID         Guid,
  _Out_ PUNICODE_STRING GuidString
);
````


## -parameters




### -param Guid [in]

Specifies the binary-format GUID to convert. 


### -param GuidString [out]

Pointer to a caller-supplied variable in which a pointer to the converted GUID string is returned. <b>RtlStringFromGUID</b> allocates the buffer space for the string, which the caller must free by calling <b>RtlFreeUnicodeString</b>. 


## -returns



If the conversion succeeds, <b>RtlStringFromGUID</b> returns STATUS_SUCCESS. Otherwise, no storage was allocated, nor was the conversion performed.




## -see-also

<a href="..\wdm\nf-wdm-rtlguidfromstring.md">RtlGUIDFromString</a>



 

 


