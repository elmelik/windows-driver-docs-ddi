---
UID: NF:wdtfsystemaction.IWDTFSystemAction2.put_Critical
title: IWDTFSystemAction2::put_Critical method
author: windows-driver-content
description: Gets or sets a value that indicates whether the the system power state is critical.
old-location: dtf\iwdtfsystemaction2_critical.htm
old-project: dtf
ms.assetid: 173cf6f2-7c6c-41d5-bd30-e323b24a0db0
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: Critical property [Windows Device Testing Framework], Critical property [Windows Device Testing Framework], IWDTFSystemAction2 interface, IWDTFSystemAction2, IWDTFSystemAction2 interface [Windows Device Testing Framework], Critical property, IWDTFSystemAction2.Critical, IWDTFSystemAction2::get_Critical, IWDTFSystemAction2::put_Critical, Microsoft.WDTF.IWDTFSystemAction2.Critical, Microsoft::WDTF::IWDTFSystemAction2::Critical, dtf.iwdtfsystemaction2_critical, put_Critical,IWDTFSystemAction2.put_Critical, wdtfsystemaction/IWDTFSystemAction2::Critical, wdtfsystemaction/IWDTFSystemAction2::get_Critical, wdtfsystemaction/IWDTFSystemAction2::put_Critical
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtfsystemaction.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFSystemAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFSystemAction.Interop.dll
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
-	WDTFSystemAction.Interop.dll
api_name:
-	IWDTFSystemAction2.Critical
-	IWDTFSystemAction2.get_Critical
-	IWDTFSystemAction2.put_Critical
product: Windows
targetos: Windows
req.typenames: TTraceLevel
req.product: Windows 10 or later.
---

# IWDTFSystemAction2::put_Critical method


## -description


Gets or sets a value that indicates whether the the system power state is critical.

This property is read/write.


## -syntax


````
HRESULT put_Critical(
  [in]          VARIANT_BOOL bCritical
);

HRESULT get_Critical(
  [out, retval] VARIANT_BOOL *pbCritical
);
````


## -parameters


## -see-also

<a href="..\wdtfsystemaction\nn-wdtfsystemaction-iwdtfsystemaction2.md">IWDTFSystemAction2</a>



 

 


