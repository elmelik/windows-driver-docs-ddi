---
UID: NF:ksproxy.IKsPin.KsCreateSinkPinHandle
title: IKsPin::KsCreateSinkPinHandle method
author: windows-driver-content
description: The KsCreateSinkPinHandle method creates a pin handle and stores it in the KS pin object.
old-location: stream\ikspin_kscreatesinkpinhandle.htm
old-project: stream
ms.assetid: 68faba0a-8057-4259-b93d-c19899637356
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: IKsPin, IKsPin interface [Streaming Media Devices], KsCreateSinkPinHandle method, IKsPin::KsCreateSinkPinHandle, KsCreateSinkPinHandle method [Streaming Media Devices], KsCreateSinkPinHandle method [Streaming Media Devices], IKsPin interface, KsCreateSinkPinHandle,IKsPin.KsCreateSinkPinHandle, ksproxy/IKsPin::KsCreateSinkPinHandle, ksproxy_8d4ac125-ae14-4abf-97cb-74fd33e5029c.xml, stream.ikspin_kscreatesinkpinhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ksproxy.h
req.include-header: Ksproxy.h
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
-	ksproxy.h
api_name:
-	IKsPin.KsCreateSinkPinHandle
product: Windows
targetos: Windows
req.typenames: PIPE_STATE
---

# IKsPin::KsCreateSinkPinHandle method


## -description


The <b>KsCreateSinkPinHandle</b> method creates a pin handle and stores it in the KS pin object. 


## -syntax


````
HRESULT KsCreateSinkPinHandle(
  [in] KSPIN_INTERFACE Interface,
  [in] KSPIN_MEDIUM    Medium
);
````


## -parameters




### -param Interface [in]

A type reference to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563537">KSPIN_INTERFACE</a> structure for the interface that <b>KsCreateSinkPinHandle</b> negotiated for the created pin. 


### -param Medium [in]

A type reference to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563538">KSPIN_MEDIUM</a> structure for the medium that <b>KsCreateSinkPinHandle</b> negotiated for the created pin. 


## -returns



Returns NOERROR if successful; otherwise, returns an error code.




## -remarks



Since the <b>KsCreateSinkPinHandle</b> method uses pass-by-reference variables, it is not necessary to pass pointers to KSPIN_INTERFACE and KSPIN_MEDIUM structures as arguments. 

After <b>KsCreateSinkPinHandle</b> has created a pin handle, you can retrieve the handle by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559890">IKsObject::KsGetObjectHandle</a> method.

This method is for proxy use and is not recommended for application use.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff563538">KSPIN_MEDIUM</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563537">KSPIN_INTERFACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559890">IKsObject::KsGetObjectHandle</a>



 

 


