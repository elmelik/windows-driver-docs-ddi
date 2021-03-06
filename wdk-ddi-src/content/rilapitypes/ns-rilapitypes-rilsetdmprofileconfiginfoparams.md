---
UID: NS:rilapitypes.RILSETDMPROFILECONFIGINFOPARAMS
title: RILSETDMPROFILECONFIGINFOPARAMS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilsetdmprofileconfiginfoparams.htm
old-project: netvista
ms.assetid: d485f00e-5fa6-4a01-83fe-78e59a8d8fcb
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*LPRILSETDMPROFILECONFIGINFOPARAMS, RILSETDMPROFILECONFIGINFOPARAMS, RILSETDMPROFILECONFIGINFOPARAMS structure [Network Drivers Starting with Windows Vista], netvista.rilsetdmprofileconfiginfoparams, ntddrilapitypes/RILSETDMPROFILECONFIGINFOPARAMS"
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
-	RILSETDMPROFILECONFIGINFOPARAMS
product: Windows
targetos: Windows
req.typenames: RILSETDMPROFILECONFIGINFOPARAMS, *LPRILSETDMPROFILECONFIGINFOPARAMS
req.product: Windows 10 or later.
---

# RILSETDMPROFILECONFIGINFOPARAMS structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILSETDMPROFILECONFIGINFOPARAMS {
  DWORD                 dwExecutor;
  RILDMCONFIGINFOITEM   dwConfigItem;
  RILDMCONFIGINFOVALUE  rciValue;
} RILSETDMPROFILECONFIGINFOPARAMS, RILSETDMPROFILECONFIGINFOPARAMS;
````


## -struct-fields




### -field dwExecutor


### -field dwConfigItem


### -field rciValue

