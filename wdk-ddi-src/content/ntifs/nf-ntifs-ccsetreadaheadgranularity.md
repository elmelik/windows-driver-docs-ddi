---
UID: NF:ntifs.CcSetReadAheadGranularity
title: CcSetReadAheadGranularity function
author: windows-driver-content
description: The CcSetReadAheadGranularity routine sets the read-ahead granularity for a cached file.
old-location: ifsk\ccsetreadaheadgranularity.htm
old-project: ifsk
ms.assetid: 3ab0c8b8-1f41-48b7-9c42-ea843ebcd82e
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: CcSetReadAheadGranularity, CcSetReadAheadGranularity routine [Installable File System Drivers], ccref_9b995224-0e59-43c6-b827-c15d9ae6e86c.xml, ifsk.ccsetreadaheadgranularity, ntifs/CcSetReadAheadGranularity
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	CcSetReadAheadGranularity
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# CcSetReadAheadGranularity function


## -description


The <b>CcSetReadAheadGranularity</b> routine sets the read-ahead granularity for a cached file.


## -syntax


````
VOID CcSetReadAheadGranularity(
  _In_ PFILE_OBJECT FileObject,
  _In_ ULONG        Granularity
);
````


## -parameters




### -param FileObject [in]

Pointer to a file object for the cached file whose read-ahead granularity is to be set.


### -param Granularity [in]

Specifies the desired read-ahead granularity, which must be an even power of two and must be greater than or equal to PAGE_SIZE.


## -returns



None




## -remarks



After <a href="..\ntifs\nf-ntifs-ccinitializecachemap.md">CcInitializeCacheMap</a> is called to cache a file, but before <b>CcSetReadAheadGranularity</b> is called for the cached file, the default read-ahead granularity for the cached file is equal to PAGE_SIZE.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff539191">CcReadAhead</a>



<a href="..\ntifs\nf-ntifs-ccinitializecachemap.md">CcInitializeCacheMap</a>



<a href="..\ntifs\nf-ntifs-ccsetadditionalcacheattributes.md">CcSetAdditionalCacheAttributes</a>



<a href="..\ntifs\nf-ntifs-ccschedulereadahead.md">CcScheduleReadAhead</a>



 

 


