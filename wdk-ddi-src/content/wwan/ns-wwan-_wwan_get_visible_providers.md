---
UID: NS:wwan._WWAN_GET_VISIBLE_PROVIDERS
title: "_WWAN_GET_VISIBLE_PROVIDERS"
author: windows-driver-content
description: The WWAN_GET_VISIBLE_PROVIDERS structure provides information about the type of visible providers to return.
old-location: netvista\wwan_get_visible_providers.htm
old-project: netvista
ms.assetid: 62516178-11F9-43F3-A70D-42C8FDDAE2DB
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PWWAN_GET_VISIBLE_PROVIDERS, PWWAN_GET_VISIBLE_PROVIDERS, PWWAN_GET_VISIBLE_PROVIDERS structure pointer [Network Drivers Starting with Windows Vista], WWAN_GET_VISIBLE_PROVIDERS, WWAN_GET_VISIBLE_PROVIDERS structure [Network Drivers Starting with Windows Vista], _WWAN_GET_VISIBLE_PROVIDERS, netvista.wwan_get_visible_providers, wwan/PWWAN_GET_VISIBLE_PROVIDERS, wwan/WWAN_GET_VISIBLE_PROVIDERS"
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
-	WWAN_GET_VISIBLE_PROVIDERS
product: Windows
targetos: Windows
req.typenames: WWAN_GET_VISIBLE_PROVIDERS, *PWWAN_GET_VISIBLE_PROVIDERS
req.product: Windows 10 or later.
---

# _WWAN_GET_VISIBLE_PROVIDERS structure


## -description


The WWAN_GET_VISIBLE_PROVIDERS structure provides information about the type of visible providers to return.


## -syntax


````
typedef struct _WWAN_GET_VISIBLE_PROVIDERS {
  ULONG Action;
} WWAN_GET_VISIBLE_PROVIDERS, *PWWAN_GET_VISIBLE_PROVIDERS;
````


## -struct-fields




### -field Action

Provides information about the type of visible providers to return. The following values are defined:

<table></table>
 

<table>
<tr>
<td>
<b>Value</b>

</td>
<td>
<b>Meaning</b>

</td>
</tr>
<tr>
<td>
WWAN_GET_VISIBLE_PROVIDERS_ALL

</td>
<td>
All providers that are currently visible should be returned.

</td>
</tr>
<tr>
<td>
WWAN_GET_VISIBLE_PROVIDERS_MULTICARRIER

</td>
<td>
Only providers that are currently visible and that can be set as home provider should be returned.

</td>
</tr>
</table>
 


## -see-also

<a href="..\ndiswwan\ns-ndiswwan-_ndis_wwan_get_visible_providers.md">NDIS_WWAN_GET_VISIBLE_PROVIDERS</a>



 

 


