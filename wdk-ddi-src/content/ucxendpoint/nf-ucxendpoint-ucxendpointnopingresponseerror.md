---
UID: NF:ucxendpoint.UcxEndpointNoPingResponseError
title: UcxEndpointNoPingResponseError function
author: windows-driver-content
description: Notifies UCX about a &#0034;No Ping Response&#0034; error for a transfer on the specified endpoint object.
old-location: buses\_ucxendpointnopingresponseerror.htm
old-project: usbref
ms.assetid: 0EDC524E-12BB-49AD-AA12-A7D9CF7D2F9C
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: UcxEndpointNoPingResponseError, UcxEndpointNoPingResponseError method [Buses], buses._ucxendpointnopingresponseerror, ucxendpoint/UcxEndpointNoPingResponseError
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ucxendpoint.h
req.include-header: Ucxclass.h, Ucxendpoint.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: "<=DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ucxendpoint.h
api_name:
-	UcxEndpointNoPingResponseError
product: Windows
targetos: Windows
req.typenames: UCX_ENDPOINT_CHARACTERISTIC_TYPE
req.product: Windows 10 or later.
---

# UcxEndpointNoPingResponseError function


## -description


Notifies UCX about a "No Ping Response" error for a transfer on
    the specified endpoint object


## -syntax


````
void UcxEndpointNoPingResponseError(
  [in] UCXENDPOINT Endpoint
);
````


## -parameters




### -param Endpoint [in]

A handle to the endpoint object. The client driver retrieved the handle in a previous call to <a href="..\ucxendpoint\nf-ucxendpoint-ucxendpointcreate.md">UcxEndpointCreate</a>.


## -returns



This method does not return a value.




## -see-also

<a href="..\ucxendpoint\nf-ucxendpoint-ucxendpointcreate.md">UcxEndpointCreate</a>



 

 


