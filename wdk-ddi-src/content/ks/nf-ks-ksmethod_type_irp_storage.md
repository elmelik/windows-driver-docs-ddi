---
UID: NF:ks.KSMETHOD_TYPE_IRP_STORAGE
title: KSMETHOD_TYPE_IRP_STORAGE macro
author: windows-driver-content
description: This macro accesses the type of method as described in the KSMETHOD_ITEM. If the method will be processed asynchronously using KsDispatchSpecificMethod, this storage must be maintained intact.
old-location: stream\ksmethod_type_irp_storage.htm
old-project: stream
ms.assetid: f5327cbf-e71b-4c1c-94c0-0e27afb4d7cf
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: KSMETHOD_TYPE_IRP_STORAGE, KSMETHOD_TYPE_IRP_STORAGE macro [Streaming Media Devices], ks/KSMETHOD_TYPE_IRP_STORAGE, ksfunc_de99d882-5298-4972-9d16-fa4478d6229c.xml, stream.ksmethod_type_irp_storage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: ks.h
req.include-header: Ks.h
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
-	HeaderDef
api_location:
-	ks.h
api_name:
-	KSMETHOD_TYPE_IRP_STORAGE
product: Windows
targetos: Windows
req.typenames: 
---

# KSMETHOD_TYPE_IRP_STORAGE macro


## -description


This macro accesses the type of method as described in the <a href="..\ks\ns-ks-ksmethod_item.md">KSMETHOD_ITEM</a>. If the method will be processed asynchronously using <a href="..\ks\nf-ks-ksdispatchspecificmethod.md">KsDispatchSpecificMethod</a>, this storage must be maintained intact.


## -syntax


````
VOID KSMETHOD_TYPE_IRP_STORAGE(
  [in] IRP Irp
);
````


## -parameters




### -param Irp [in]

Specifies the IRP passed to the handler routine.


## -remarks



The relevant KSMETHOD_ITEM structure is extracted from <b>Irp-&gt;Tail.Overlay.DriverContext</b>. Parameters in <b>DriverContext</b> are initialized by <a href="..\ks\nf-ks-ksmethodhandler.md">KsMethodHandler</a> and <a href="..\ks\nf-ks-ksmethodhandlerwithallocator.md">KsMethodHandlerWithAllocator</a>.

The macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define KSMETHOD_TYPE_IRP_STORAGE(Irp)      (*(ULONG_PTR*)(&amp;(Irp)-&gt;Tail.Overlay.DriverContext[2]))</code></pre>



## -see-also

<a href="..\ks\ns-ks-ksmethod_set.md">KSMETHOD_SET</a>



<a href="..\ks\nf-ks-ksfastmethodhandler.md">KsFastMethodHandler</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563398">KSMETHOD</a>



<a href="..\ks\nf-ks-ksmethodhandlerwithallocator.md">KsMethodHandlerWithAllocator</a>



<a href="..\ks\nf-ks-ksmethodhandler.md">KsMethodHandler</a>



<a href="..\ks\ns-ks-ksmethod_item.md">KSMETHOD_ITEM</a>



 

 


