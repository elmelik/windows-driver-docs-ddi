---
UID: NF:dbgeng.IDebugClient3.AddProcessOptions
title: IDebugClient3::AddProcessOptions method
author: windows-driver-content
description: The AddProcessOptions method adds the process options to those options that affect the current process.
old-location: debugger\addprocessoptions.htm
old-project: debugger
ms.assetid: eb5f1d91-cfad-48e6-b578-64b64034222f
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: AddProcessOptions method [Windows Debugging], AddProcessOptions method [Windows Debugging], IDebugClient interface, AddProcessOptions method [Windows Debugging], IDebugClient2 interface, AddProcessOptions method [Windows Debugging], IDebugClient3 interface, AddProcessOptions method [Windows Debugging], IDebugClient4 interface, AddProcessOptions method [Windows Debugging], IDebugClient5 interface, AddProcessOptions,IDebugClient3.AddProcessOptions, IDebugClient interface [Windows Debugging], AddProcessOptions method, IDebugClient2 interface [Windows Debugging], AddProcessOptions method, IDebugClient2::AddProcessOptions, IDebugClient3, IDebugClient3 interface [Windows Debugging], AddProcessOptions method, IDebugClient3::AddProcessOptions, IDebugClient4 interface [Windows Debugging], AddProcessOptions method, IDebugClient4::AddProcessOptions, IDebugClient5 interface [Windows Debugging], AddProcessOptions method, IDebugClient5::AddProcessOptions, IDebugClient::AddProcessOptions, IDebugClient_995041c9-9380-4a66-b9f8-d74d68398a44.xml, dbgeng/IDebugClient2::AddProcessOptions, dbgeng/IDebugClient3::AddProcessOptions, dbgeng/IDebugClient4::AddProcessOptions, dbgeng/IDebugClient5::AddProcessOptions, dbgeng/IDebugClient::AddProcessOptions, debugger.addprocessoptions
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
-	IDebugClient.AddProcessOptions
-	IDebugClient2.AddProcessOptions
-	IDebugClient3.AddProcessOptions
-	IDebugClient4.AddProcessOptions
-	IDebugClient5.AddProcessOptions
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugClient3::AddProcessOptions method


## -description


The <b>AddProcessOptions</b> method adds the process options to those options that affect the <a href="https://msdn.microsoft.com/295b05a3-e27f-4761-a562-7e87e25bfd3b">current process</a>.


## -syntax


````
HRESULT AddProcessOptions(
  [in] ULONG Options
);
````


## -parameters




### -param Options [in]

Specifies the process options to add to those affecting the current process.  For details on these process options, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff541534">DEBUG_PROCESS_XXX</a>.


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
</table>
 




## -remarks



This method is available only in <a href="https://msdn.microsoft.com/d290c203-4cb3-423c-a41f-baabb3c9a3c1">live user-mode debugging</a>.

Some of the process options are global options, others are specific to the current process.

If any process options are modified, the engine will notify the <a href="https://msdn.microsoft.com/1e32bd40-8c77-4c6b-913c-6ec26707ed36">event callbacks</a> by calling their <a href="https://msdn.microsoft.com/library/windows/hardware/ff550683">IDebugEventCallbacks::ChangeEngineState</a> method with the DEBUG_CES_PROCESS_OPTIONS flag set.

For more information about creating and attaching to live user-mode targets, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552020">Live User-Mode Targets</a>.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff556765">SetProcessOptions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548163">GetProcessOptions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541534">DEBUG_PROCESS_XXX</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient5.md">IDebugClient5</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient4.md">IDebugClient4</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient3.md">IDebugClient3</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient.md">IDebugClient</a>



<a href="..\dbgeng\nn-dbgeng-idebugclient2.md">IDebugClient2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554505">RemoveProcessOptions</a>



 

 


