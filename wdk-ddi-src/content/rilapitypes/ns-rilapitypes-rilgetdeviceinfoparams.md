---
UID: NS:rilapitypes.RILGETDEVICEINFOPARAMS
title: RILGETDEVICEINFOPARAMS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilgetdeviceinfoparams.htm
old-project: netvista
ms.assetid: 4cb3be01-7e74-4c98-9c4b-2e1c78d96001
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*LPRILGETDEVICEINFOPARAMS, RILGETDEVICEINFOPARAMS, RILGETDEVICEINFOPARAMS structure [Network Drivers Starting with Windows Vista], netvista.rilgetdeviceinfoparams, ntddrilapitypes/RILGETDEVICEINFOPARAMS"
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
-	RILGETDEVICEINFOPARAMS
product: Windows
targetos: Windows
req.typenames: RILGETDEVICEINFOPARAMS, *LPRILGETDEVICEINFOPARAMS
req.product: Windows 10 or later.
---

# RILGETDEVICEINFOPARAMS structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILGETDEVICEINFOPARAMS {
  DWORD                 dwExecutor;
  RILDEVICEINFORMATION  dwId;
} RILGETDEVICEINFOPARAMS, RILGETDEVICEINFOPARAMS;
````


## -struct-fields




### -field dwExecutor


### -field dwId

