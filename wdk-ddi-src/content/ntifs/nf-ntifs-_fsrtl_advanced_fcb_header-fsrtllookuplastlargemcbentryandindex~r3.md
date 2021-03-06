---
UID: NF:ntifs._FSRTL_ADVANCED_FCB_HEADER.FsRtlLookupLastLargeMcbEntryAndIndex~r3
title: FsRtlLookupLastLargeMcbEntryAndIndex function
author: windows-driver-content
description: The FsRtlLookupLastLargeMcbEntryAndIndex routine retrieves the last mapping entry stored in a given map control block (MCB).
old-location: ifsk\fsrtllookuplastlargemcbentryandindex.htm
old-project: ifsk
ms.assetid: 53c3109d-16e4-4db4-9c62-27c6d8501707
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: FsRtlLookupLastLargeMcbEntryAndIndex, FsRtlLookupLastLargeMcbEntryAndIndex routine [Installable File System Drivers], fsrtlref_d7148458-8a3c-4633-8be3-578623ba4d01.xml, ifsk.fsrtllookuplastlargemcbentryandindex, ntifs/FsRtlLookupLastLargeMcbEntryAndIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: This routine is available on Microsoft Windows XP and later.
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
req.irql: "<= APC_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	FsRtlLookupLastLargeMcbEntryAndIndex
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# FsRtlLookupLastLargeMcbEntryAndIndex function


## -description


The <b>FsRtlLookupLastLargeMcbEntryAndIndex</b> routine retrieves the last mapping entry stored in a given map control block (MCB). 


## -syntax


````
BOOLEAN FsRtlLookupLastLargeMcbEntryAndIndex(
  _In_  PLARGE_MCB OpaqueMcb,
  _Out_ PLONGLONG  LargeVbn,
  _Out_ PLONGLONG  LargeLbn,
  _Out_ PULONG     Index
);
````


## -parameters




### -param OpaqueMcb [in]

Pointer to an initialized MCB structure to be searched. 


### -param LargeVbn [out]

Pointer to a variable that receives the last virtual block number (VBN) that was mapped. 


### -param LargeLbn [out]

Pointer to a variable that receives the logical block number (LBN) that is mapped to the VBN pointed to by <i>LargeVbn</i>, or -1 if no such LBN exists. 


### -param Index [out]

Pointer to a variable that receives the index of the last run in the MCB. 


## -returns



<b>FsRtlLookupLastLargeMcbEntryAndIndex </b>returns <b>FALSE</b> if the MCB contains no mapping entries, <b>TRUE</b> otherwise. 




## -remarks



<b>FsRtlLookupLastLargeMcbEntryAndIndex </b>searches for the last mapping of the last run in the MCB: 

<ul>
<li>
If the MCB contains no mappings, <b>FsRtlLookupLastLargeMcbEntryAndIndex </b>returns <b>FALSE</b>. 

</li>
<li>
If the last mapping is a hole, <b>FsRtlLookupLastLargeMcbEntryAndIndex </b>returns <b>TRUE</b>, but the lookup operation yields a value of -1 for the LBN. 

</li>
<li>
If the last mapping is not a hole, the lookup operation yields a positive value for the LBN, and <b>FsRtlLookupLastLargeMcbEntryAndIndex </b>returns <b>TRUE</b>. 

</li>
</ul>
<div class="alert"><b>Note</b>    The upper 32 bits of the LBN are ignored. Only the lower 32 bits are used. </div>
<div> </div>



## -see-also

<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtluninitializelargemcb.md">FsRtlUninitializeLargeMcb</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlsplitlargemcb~r2.md">FsRtlSplitLargeMcb</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtllookuplastlargemcbentry~r2.md">FsRtlLookupLastLargeMcbEntry</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtladdlargemcbentry~r3.md">FsRtlAddLargeMcbEntry</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlremovelargemcbentry~r2.md">FsRtlRemoveLargeMcbEntry</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtltruncatelargemcb~r1.md">FsRtlTruncateLargeMcb</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtllookuplargemcbentry~r6.md">FsRtlLookupLargeMcbEntry</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlinitializelargemcb~r1.md">FsRtlInitializeLargeMcb</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlnumberofrunsinlargemcb.md">FsRtlNumberOfRunsInLargeMcb</a>



<a href="..\ntifs\nf-ntifs-_fsrtl_advanced_fcb_header-fsrtlgetnextlargemcbentry~r4.md">FsRtlGetNextLargeMcbEntry</a>



 

 


