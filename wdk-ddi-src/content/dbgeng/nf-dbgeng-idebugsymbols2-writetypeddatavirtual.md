---
UID: NF:dbgeng.IDebugSymbols2.WriteTypedDataVirtual
title: IDebugSymbols2::WriteTypedDataVirtual method
author: windows-driver-content
description: The WriteTypedDataVirtual method writes data to the target's virtual address space. The number of bytes written is the size of the specified type.
old-location: debugger\writetypeddatavirtual.htm
old-project: debugger
ms.assetid: c7a3854b-2405-4e20-8c6c-4e0c0d43987e
ms.author: windowsdriverdev
ms.date: 1/19/2018
ms.keywords: IDebugSymbols::WriteTypedDataVirtual, WriteTypedDataVirtual, IDebugSymbols3::WriteTypedDataVirtual, WriteTypedDataVirtual method [Windows Debugging], IDebugSymbols2 interface, WriteTypedDataVirtual method [Windows Debugging], IDebugSymbols3 interface, IDebugSymbols2, WriteTypedDataVirtual method [Windows Debugging], IDebugSymbols interface, IDebugSymbols2 interface [Windows Debugging], WriteTypedDataVirtual method, dbgeng/IDebugSymbols::WriteTypedDataVirtual, dbgeng/IDebugSymbols2::WriteTypedDataVirtual, WriteTypedDataVirtual method [Windows Debugging], IDebugSymbols interface [Windows Debugging], WriteTypedDataVirtual method, IDebugSymbols3 interface [Windows Debugging], WriteTypedDataVirtual method, IDebugSymbols, dbgeng/IDebugSymbols3::WriteTypedDataVirtual, IDebugSymbols2::WriteTypedDataVirtual, debugger.writetypeddatavirtual, IDebugSymbols_51186c12-dc2b-4906-a8fa-9e0f4a960135.xml
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
req.lib: dbgeng.h
req.dll: 
req.irql: 
topictype:
-	APIRef
-	kbSyntax
apitype:
-	COM
apilocation:
-	dbgeng.h
apiname:
-	IDebugSymbols.WriteTypedDataVirtual
-	IDebugSymbols2.WriteTypedDataVirtual
-	IDebugSymbols3.WriteTypedDataVirtual
product: Windows
targetos: Windows
req.typenames: "*PDOT4_ACTIVITY, DOT4_ACTIVITY"
---

# IDebugSymbols2::WriteTypedDataVirtual method


## -description


The <b>WriteTypedDataVirtual</b> method writes data to the target's virtual address space.  The number of bytes written is the size of the specified type.


## -syntax


````
HRESULT WriteTypedDataVirtual(
  [in]            ULONG64 Offset,
  [in]            ULONG64 Module,
  [in]            ULONG   TypeId,
  [in]            PVOID   Buffer,
  [in]            ULONG   BufferSize,
  [out, optional] PULONG  BytesWritten
);
````


## -parameters




### -param Offset [in]

Specifies the location in the target's virtual address space where the data will be written.


### -param Module [in]

Specifies the base address of the module containing the type.


### -param TypeId [in]

Specifies the type ID of the type.


### -param Buffer [in]

Specifies the buffer containing the data to be written.


### -param BufferSize [in]

Specifies the size in bytes of the buffer <i>Buffer</i>.  This is the maximum number of bytes to be written.


### -param BytesWritten [out, optional]

Receives the number of bytes that were written.  If <i>BytesWritten</i> is <b>NULL</b>, this information is not returned.


## -returns



This method may also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.  All the bytes in the buffer <i>Buffer</i> were written.  However, the buffer was smaller than the size of the type specified. 

</td>
</tr>
</table>
 




## -remarks



This is a convenience method.  The same result can be obtained by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff549457">GetTypeSize</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff561468">WriteVirtual</a>.

For more information about types, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff558931">Types</a>.


