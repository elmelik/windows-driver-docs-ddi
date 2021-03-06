---
UID: NF:dbgeng.IDebugSymbolGroup2.GetSymbolEntryInformation
title: IDebugSymbolGroup2::GetSymbolEntryInformation method
author: windows-driver-content
description: The GetSymbolEntryInformation method returns information about a symbol in a symbol group.
old-location: debugger\getsymbolentryinformation2.htm
old-project: debugger
ms.assetid: ee8ea970-04ee-4bf5-9e81-7d5baf0eac0d
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: ComOther_b34e6d42-3da1-43bd-954d-0aaf0da5a3a8.xml, GetSymbolEntryInformation method [Windows Debugging], GetSymbolEntryInformation method [Windows Debugging], IDebugSymbolGroup2 interface, GetSymbolEntryInformation,IDebugSymbolGroup2.GetSymbolEntryInformation, IDebugSymbolGroup2, IDebugSymbolGroup2 interface [Windows Debugging], GetSymbolEntryInformation method, IDebugSymbolGroup2::GetSymbolEntryInformation, dbgeng/IDebugSymbolGroup2::GetSymbolEntryInformation, debugger.getsymbolentryinformation2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dbgeng.h
api_name:
-	IDebugSymbolGroup2.GetSymbolEntryInformation
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugSymbolGroup2::GetSymbolEntryInformation method


## -description


The <b>GetSymbolEntryInformation</b> method returns information about a symbol in a symbol group.


## -syntax


````
HRESULT GetSymbolEntryInformation(
  [in]  ULONG               Index,
  [out] PDEBUG_SYMBOL_ENTRY Entry
);
````


## -parameters




### -param Index [in]

The index of the symbol whose information iyou want.  The index of a symbol is an identification number. The index ranges from zero through the number of symbols in the symbol group minus one.


### -param Entry [out]

The information about the symbol.  For more information about this structure, see <a href="..\dbgeng\ns-dbgeng-_debug_symbol_entry.md">DEBUG_SYMBOL_ENTRY</a>.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 

This method can also return error values.  For more information, see <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a>.




## -remarks



For more information about symbol groups, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff554702">Scopes and Symbol Groups</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff547975">GetNumberSymbols</a>



<a href="..\dbgeng\ns-dbgeng-_debug_symbol_entry.md">DEBUG_SYMBOL_ENTRY</a>



<a href="https://msdn.microsoft.com/02fe418f-1793-4585-9891-1274a4ddba74">IDebugSymbols3::GetSymbolEntryInformation</a>



<a href="..\dbgeng\nn-dbgeng-idebugsymbolgroup2.md">IDebugSymbolGroup2</a>



 

 


