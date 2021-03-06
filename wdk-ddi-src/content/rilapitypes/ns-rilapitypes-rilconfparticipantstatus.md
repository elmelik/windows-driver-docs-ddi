---
UID: NS:rilapitypes.RILCONFPARTICIPANTSTATUS
title: RILCONFPARTICIPANTSTATUS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilconfparticipantstatus.htm
old-project: netvista
ms.assetid: 7eb0e06b-85f0-4b61-9ed0-2f35156fbb8c
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*LPRILCONFPARTICIPANTSTATUS, RILCONFPARTICIPANTSTATUS, RILCONFPARTICIPANTSTATUS structure [Network Drivers Starting with Windows Vista], netvista.rilconfparticipantstatus, ntddrilapitypes/RILCONFPARTICIPANTSTATUS"
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
-	RILCONFPARTICIPANTSTATUS
product: Windows
targetos: Windows
req.typenames: RILCONFPARTICIPANTSTATUS, *LPRILCONFPARTICIPANTSTATUS
req.product: Windows 10 or later.
---

# RILCONFPARTICIPANTSTATUS structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILCONFPARTICIPANTSTATUS {
  DWORD                    cbSize;
  DWORD                    dwParams;
  DWORD                    dwExecutor;
  DWORD                    dwID;
  BOOL                     bCallTransfer;
  RILADDRESS               raAddress;
  RILPARTICIPANTOPERATION  dwParticipantOp;
  DWORD                    dwSIPStatus;
} RILCONFPARTICIPANTSTATUS, RILCONFPARTICIPANTSTATUS;
````


## -struct-fields




### -field cbSize


### -field dwParams


### -field dwExecutor


### -field dwID


### -field bCallTransfer


### -field raAddress


### -field dwParticipantOp


### -field dwSIPStatus

