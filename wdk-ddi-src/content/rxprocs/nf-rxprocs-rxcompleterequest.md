---
UID: NF:rxprocs.RxCompleteRequest
title: RxCompleteRequest function
author: windows-driver-content
description: RxCompleteRequest completes the IRP request associated with an RX_CONTEXT structure.
old-location: ifsk\rxcompleterequest.htm
old-project: ifsk
ms.assetid: f5e9219b-0697-427e-b92e-7cd647a0e0b6
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: RxCompleteRequest, RxCompleteRequest function [Installable File System Drivers], ifsk.rxcompleterequest, rxprocs/RxCompleteRequest, rxref_12eec336-4619-430c-a36c-ddbe855b8865.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rxprocs.h
req.include-header: Rxprocs.h, Rxcontx.h
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
req.irql: "<= APC_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	rxprocs.h
api_name:
-	RxCompleteRequest
product: Windows
targetos: Windows
req.typenames: RX_CONTEXT, *PRX_CONTEXT
req.product: Windows 10 or later.
---

# RxCompleteRequest function


## -description


<b>RxCompleteRequest</b> completes the IRP request associated with an RX_CONTEXT structure.


## -syntax


````
NTSTATUS RxCompleteRequest(
   PRX_CONTEXT RxContext,
   NTSTATUS    Status
);
````


## -parameters




### -param pContext

TBD


### -param Status

The status value to return when the IRP request is complete. This is the value that will be stored in the <b>IoStatus.Status</b> member of the associated IRP on completion.


#### - RxContext

A pointer to the RX_CONTEXT. This parameter contains the IRP requesting the operation to complete. 


## -returns



<b>RxCompleteRequest</b> returns the value of the <i>Status</i> parameter.




## -remarks



The <b>RxCompleteRequest</b> routine is not normally called by network mini-redirector drivers directly. RDBSS calls this routine internally to complete an I/O request packet. 

<b>RxCompleteRequest</b> internally calls <b>RxCompleteRequest_Real</b> to complete the request. Before calling <b>RxCompleteRequest_Real</b>, the <b>RxCompleteRequest</b> routine checks the value of the <b>LoudCompletionString</b> member in the RX_CONTEXT structure pointed to by the <i>RxContext</i> parameter and prints extra debugging information if <i>Status</i> is not equal to STATUS_SUCCESS. 




## -see-also

<a href="..\rxcontx\nf-rxcontx-rxpreparecontextforreuse.md">RxPrepareContextForReuse</a>



<a href="..\rxcontx\nf-rxcontx-rxcreaterxcontext.md">RxCreateRxContext</a>



<a href="..\rxcontx\nf-rxcontx-rxdereferenceanddeleterxcontext_real.md">RxDereferenceAndDeleteRxContext_Real</a>



<a href="..\rxcontx\nf-rxcontx-__rxsynchronizeblockingoperations.md">__RxSynchronizeBlockingOperations</a>



<a href="..\rxcontx\nf-rxcontx-rxinitializecontext.md">RxInitializeContext</a>



<a href="..\rxprocs\nf-rxprocs-rxcompleterequest_real.md">RxCompleteRequest_Real</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557382">__RxSynchronizeBlockingOperationsMaybeDroppingFcbLock</a>



<a href="..\rxcontx\nf-rxcontx-rxresumeblockedoperations_serially.md">RxResumeBlockedOperations_Serially</a>



<a href="..\rxprocs\nf-rxprocs-rxdereference.md">RxDereference</a>



 

 


