---
UID: NS:wsk._WSK_DATA_INDICATION
title: "_WSK_DATA_INDICATION"
author: windows-driver-content
description: The WSK_DATA_INDICATION structure describes data that has been received on a connection-oriented socket.
old-location: netvista\wsk_data_indication.htm
old-project: netvista
ms.assetid: 10af500f-bb3b-427f-86b1-ee075ffc7ac6
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PWSK_DATA_INDICATION, PWSK_DATA_INDICATION, PWSK_DATA_INDICATION structure pointer [Network Drivers Starting with Windows Vista], WSK_DATA_INDICATION, WSK_DATA_INDICATION structure [Network Drivers Starting with Windows Vista], _WSK_DATA_INDICATION, netvista.wsk_data_indication, wsk/PWSK_DATA_INDICATION, wsk/WSK_DATA_INDICATION, wskref_89ac35f7-4945-4b2d-90d6-177d9bca7361.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsk.h
req.include-header: Wsk.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
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
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wsk.h
api_name:
-	WSK_DATA_INDICATION
product: Windows
targetos: Windows
req.typenames: WSK_DATA_INDICATION, *PWSK_DATA_INDICATION
req.product: Windows 10 or later.
---

# _WSK_DATA_INDICATION structure


## -description


The WSK_DATA_INDICATION structure describes data that has been received on a connection-oriented
  socket.


## -syntax


````
typedef struct _WSK_DATA_INDICATION {
  struct _WSK_DATA_INDICATION  *Next;
  WSK_BUF                     Buffer;
} WSK_DATA_INDICATION, *PWSK_DATA_INDICATION;
````


## -struct-fields




### -field Next

A pointer to the next WSK_DATA_INDICATION structure in a linked list of WSK_DATA_INDICATION
     structures. If this member is <b>NULL</b>, this structure is the last WSK_DATA_INDICATION structure in the
     linked list.


### -field Buffer

A WSK_BUF structure that describes the data that has been received on the socket.


## -remarks



The WSK subsystem passes a pointer to a WSK_DATA_INDICATION structure as the 
    <i>DataIndication</i> parameter when it calls a connection-oriented socket's 
    <a href="..\wsk\nc-wsk-pfn_wsk_receive_event.md">WskReceiveEvent</a> event callback
    function.




## -see-also

<a href="..\wsk\ns-wsk-_wsk_buf.md">WSK_BUF</a>



<a href="..\wsk\nc-wsk-pfn_wsk_release_data_indication_list.md">WskRelease</a>



<a href="..\wsk\nc-wsk-pfn_wsk_receive_event.md">WskReceiveEvent</a>



 

 


