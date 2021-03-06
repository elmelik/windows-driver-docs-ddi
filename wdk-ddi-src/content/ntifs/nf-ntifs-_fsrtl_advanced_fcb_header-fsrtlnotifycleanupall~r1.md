---
UID: NF:ntifs._FSRTL_ADVANCED_FCB_HEADER.FsRtlNotifyCleanupAll~r1
title: FsRtlNotifyCleanupAll function
author: windows-driver-content
description: The FsRtlNotifyCleanupAll routine removes all members of the specified notification list.
old-location: ifsk\fsrtlnotifycleanupall.htm
old-project: ifsk
ms.assetid: 850728bd-6758-4c21-9bfd-10a0f3d006d6
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: FsRtlNotifyCleanupAll, FsRtlNotifyCleanupAll routine [Installable File System Drivers], fsrtlref_f0eea2f1-9bc9-41e1-843c-a69b3e63f452.xml, ifsk.fsrtlnotifycleanupall, ntifs/FsRtlNotifyCleanupAll
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: FltKernel.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows Vista and later version of the Windows operating system.
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
req.irql: "<=APC_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	FsRtlNotifyCleanupAll
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# FsRtlNotifyCleanupAll function


## -description


The <b>FsRtlNotifyCleanupAll</b> routine removes all members of the specified notification list. 


## -syntax


````
VOID FsRtlNotifyCleanupAll(
  _In_ PNOTIFY_SYNC NotifySync,
  _In_ PLIST_ENTRY  NotifyList
);
````


## -parameters




### -param NotifySync [in]

A pointer to the opaque synchronization object for <i>NotifyList</i>. 


### -param NotifyList [in]

A pointer to the head of the notify list to be cleaned up. Each element in the list is an opaque notify structure. 


## -returns



None




## -remarks



For each entry in the <i>NotifyList</i> list, <b>FsRtlNotifyCleanupAll</b> completes all pending IRPs. Then the routine removes the entry from the list and deallocates the entry.

Because a notify list is typically associated with a volume, the <b>FsRtlNotifyCleanupAll</b> routine can be used to complete all the IRP requests for the volume.




## -see-also

<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlnotifyfullreportchange~r8.md">FsRtlNotifyFullReportChange</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlnotifyfilterreportchange~r9.md">FsRtlNotifyFilterReportChange</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlnotifycleanup~r2.md">FsRtlNotifyCleanup</a>



<a href="..\rxprocs\nf-rxprocs-fsrtlnotifyfullchangedirectory.md">FsRtlNotifyFullChangeDirectory</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlnotifyfilterchangedirectory~r10.md">FsRtlNotifyFilterChangeDirectory</a>



 

 


