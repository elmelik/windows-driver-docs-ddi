---
UID: NS:rilapitypes.RILACCESSTECHNOLOGY
title: RILACCESSTECHNOLOGY
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilaccesstechnology.htm
old-project: netvista
ms.assetid: 28363041-4adc-4348-a1a5-2b9c11750286
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*LPRILACCESSTECHNOLOGY, RILACCESSTECHNOLOGY, RILACCESSTECHNOLOGY structure [Network Drivers Starting with Windows Vista], netvista.rilaccesstechnology, ntddrilapitypes/RILACCESSTECHNOLOGY"
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
-	RILACCESSTECHNOLOGY
product: Windows
targetos: Windows
req.typenames: RILACCESSTECHNOLOGY, *LPRILACCESSTECHNOLOGY
req.product: Windows 10 or later.
---

# RILACCESSTECHNOLOGY structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILACCESSTECHNOLOGY {
  DWORD                         cbSize;
  DWORD                         dwParams;
  DWORD                         dwSystemType;
  NULL                          RILACCESSTECHNOLOGYKINDUNION;
  RILACCESSTECHNOLOGYKINDUNION  kindUnion;
  RILEVDOKIND                   dwEvdoKind;
  RILGSMKIND                    dwGsmKind;
  RILUMTSKIND                   dwUmtsKind;
  RILTDSCDMAKIND                dwTdscdmaKind;
  RILLTEKIND                    dwLteKind;
} RILACCESSTECHNOLOGY, RILACCESSTECHNOLOGY;
````


## -struct-fields




### -field cbSize


### -field dwParams


### -field dwSystemType


### -field kindUnion


### -field RILACCESSTECHNOLOGYKINDUNION


#### - dwEvdoKind


#### - dwGsmKind


#### - dwLteKind


#### - dwTdscdmaKind


#### - dwUmtsKind

