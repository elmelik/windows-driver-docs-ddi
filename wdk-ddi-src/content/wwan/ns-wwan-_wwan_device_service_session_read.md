---
UID: NS:wwan._WWAN_DEVICE_SERVICE_SESSION_READ
title: "_WWAN_DEVICE_SERVICE_SESSION_READ"
author: windows-driver-content
description: The WWAN_DEVICE_SERVICE_SESSION_READ structure represents data associated with a device service session read notification.
old-location: netvista\wwan_device_service_session_read.htm
old-project: netvista
ms.assetid: 248C5386-B835-4806-8DD8-39327EDADA0C
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PWWAN_DEVICE_SERVICE_SESSION_READ, PWWAN_DEVICE_SERVICE_SESSION_READ, PWWAN_DEVICE_SERVICE_SESSION_READ structure pointer [Network Drivers Starting with Windows Vista], WWAN_DEVICE_SERVICE_SESSION_READ, WWAN_DEVICE_SERVICE_SESSION_READ structure [Network Drivers Starting with Windows Vista], _WWAN_DEVICE_SERVICE_SESSION_READ, netvista.wwan_device_service_session_read, wwan/PWWAN_DEVICE_SERVICE_SESSION_READ, wwan/WWAN_DEVICE_SERVICE_SESSION_READ"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wwan.h
req.include-header: Wwan.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with  Windows 8.
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
-	wwan.h
api_name:
-	WWAN_DEVICE_SERVICE_SESSION_READ
product: Windows
targetos: Windows
req.typenames: WWAN_DEVICE_SERVICE_SESSION_READ, *PWWAN_DEVICE_SERVICE_SESSION_READ
req.product: Windows 10 or later.
---

# _WWAN_DEVICE_SERVICE_SESSION_READ structure


## -description


The WWAN_DEVICE_SERVICE_SESSION_READ structure represents data associated with a device service session read notification.


## -syntax


````
typedef struct _WWAN_DEVICE_SERVICE_SESSION_READ {
  ULONG uSessionID;
  ULONG uDataSize;
} WWAN_DEVICE_SERVICE_SESSION_READ, *PWWAN_DEVICE_SERVICE_SESSION_READ;
````


## -struct-fields




### -field uSessionID

The session ID of the device service.


### -field uDataSize

The size, in bytes, of the device service data that follows the structure instance in memory. This value should not exceed the value of the <b>uMaxSessionDataSize</b> member of the <a href="..\wwan\ns-wwan-_wwan_supported_device_services.md">WWAN_SUPPORTED_DEVICE_SERVICES</a> structure.


## -see-also

<a href="..\ndiswwan\ns-ndiswwan-_ndis_wwan_device_service_session_read.md">NDIS_WWAN_DEVICE_SERVICE_SESSION_READ</a>



<a href="..\wwan\ns-wwan-_wwan_supported_device_services.md">WWAN_SUPPORTED_DEVICE_SERVICES</a>



 

 


