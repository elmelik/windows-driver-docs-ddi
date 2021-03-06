---
UID: NF:fltkernel.FltAddOpenReparseEntry
title: FltAddOpenReparseEntry function
author: windows-driver-content
description: This routine adds a caller allocated open reparse structure, OPEN_REPARSE_LIST_ENTRY, into a create operation.
old-location: ifsk\fltaddopenreparseentry.htm
old-project: ifsk
ms.assetid: D58AB46A-0D87-45B5-8C58-E99ED0F906D2
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: FltAddOpenReparseEntry, FltAddOpenReparseEntry routine [Installable File System Drivers], fltkernel/FltAddOpenReparseEntry, ifsk.fltaddopenreparseentry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fltkernel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607
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
req.irql: "_IRQL_requires_max_(APC_LEVEL)"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	fltKernel.h
api_name:
-	FltAddOpenReparseEntry
product: Windows
targetos: Windows
req.typenames: EXpsFontRestriction
---

# FltAddOpenReparseEntry function


## -description


This routine adds a caller allocated open reparse structure, <a href="..\ntifs\ns-ntifs-_open_reparse_list_entry.md">OPEN_REPARSE_LIST_ENTRY</a>,  into a create operation.


## -syntax


````
NTSTATUS FltAddOpenReparseEntry(
  _In_ PFLT_FILTER              Filter,
  _In_ PFLT_CALLBACK_DATA       Data,
  _In_ POPEN_REPARSE_LIST_ENTRY OpenReparseEntry
);
````


## -parameters




### -param Filter [in]

The filter to reference.


### -param Data [in]

The create operation to attach open reparse information to.


### -param OpenReparseEntry [in]

The open reparse information to add, of type <a href="..\ntifs\ns-ntifs-_open_reparse_list_entry.md">OPEN_REPARSE_LIST_ENTRY</a>.


## -returns



The following NT status codes are returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER_2</b></dt>
</dl>
</td>
<td width="60%">
Status code if <i>Data</i> is not a create operation. This is an error code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
</table>
 




## -remarks



This routine adds an ECP list and/or ECP as needed.  <i>Filter</i> is referenced
    for the lifetime of the open reparse entry structure, not the ECP itself,
    which is conceptually independent of any specific filter.

Use <a href="..\fltkernel\nf-fltkernel-fltremoveopenreparseentry.md">FltRemoveOpenReparseEntry</a> to remove the open reparse structure from the create operation.




## -see-also

<a href="..\fltkernel\nf-fltkernel-fltremoveopenreparseentry.md">FltRemoveOpenReparseEntry</a>



 

 


