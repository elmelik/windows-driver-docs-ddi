---
UID: NS:rilapitypes.RILCALLINFO_V1
title: RILCALLINFO_V1
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilcallinfo_v1.htm
old-project: netvista
ms.assetid: eae7108f-94d5-4147-b554-189c1a356641
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*LPRILCALLINFO_V1, RILCALLINFO_V1, RILCALLINFO_V1 structure [Network Drivers Starting with Windows Vista], netvista.rilcallinfo_v1, ntddrilapitypes/RILCALLINFO_V1"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rilapitypes.h
req.include-header: Rilapitypes.h
req.target-type: Windows
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
-	ntddrilapitypes.h
api_name:
-	RILCALLINFO_V1
product: Windows
targetos: Windows
req.typenames: RILCALLINFO_V1, *LPRILCALLINFO_V1
req.product: Windows 10 or later.
---

# RILCALLINFO_V1 structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILCALLINFO_V1 {
  DWORD                           cbSize;
  DWORD                           dwParams;
  DWORD                           dwExecutor;
  DWORD                           dwID;
  RILCALLINFODIRECTION            dwDirection;
  RILCALLINFOSTATUS               dwStatus;
  RILCALLTYPE                     dwType;
  RILCALLINFOMULTIPARTY           dwMultiparty;
  RILADDRESS                      raAddress;
  RILSUBADDRESS                   rsaSubAddress;
  WCHAR [256]                     wszDescription;
  RILREMOTEPARTYINFOVALUE         dwNumberPresentationIndicator;
  RILREMOTEPARTYINFOVALUE         dwNamePresentationIndicator;
  BOOL                            fAlienCall;
  RILCALLINFODISCONNECTINITIATOR  dwDisconnectInitiator;
  RILCALLINFODISCONNECTREASON     dwDisconnectReason;
  RILCALLDISCONNECTDETAILS        stDisconnectDetails;
} RILCALLINFO_V1, RILCALLINFO_V1;
````


## -struct-fields




### -field cbSize


### -field dwParams


### -field dwExecutor


### -field dwID


### -field dwDirection


### -field dwStatus


### -field dwType


### -field dwMultiparty


### -field raAddress


### -field rsaSubAddress


### -field wszDescription


### -field dwNumberPresentationIndicator


### -field dwNamePresentationIndicator


### -field fAlienCall


### -field dwDisconnectInitiator


### -field dwDisconnectReason


### -field stDisconnectDetails

