---
UID: NF:wdtfedtaction.IWDTFEnhancedDeviceTestSupportAction2.Disable
title: IWDTFEnhancedDeviceTestSupportAction2::Disable method
author: windows-driver-content
description: Disables the Enhanced Device Test (EDT) filter driver on the target device.
old-location: dtf\iwdtfenhanceddevicetestsupportaction2_disable.htm
old-project: dtf
ms.assetid: cf67d391-8c73-43d7-aab3-57837c78dbc4
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: Disable method [Windows Device Testing Framework], Disable method [Windows Device Testing Framework], IWDTFEnhancedDeviceTestSupportAction2 interface, Disable,IWDTFEnhancedDeviceTestSupportAction2.Disable, IWDTFEnhancedDeviceTestSupportAction2, IWDTFEnhancedDeviceTestSupportAction2 interface [Windows Device Testing Framework], Disable method, IWDTFEnhancedDeviceTestSupportAction2::Disable, Microsoft.WDTF.IWDTFEnhancedDeviceTestSupportAction2.Disable, Microsoft::WDTF::IWDTFEnhancedDeviceTestSupportAction2::Disable, dtf.iwdtfenhanceddevicetestsupportaction2_disable, wdtfedtaction/IWDTFEnhancedDeviceTestSupportAction2::Disable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdtfedtaction.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows XP Professional
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WDTFEDTAction.idl
req.max-support: 
req.namespace: Microsoft.WDTF
req.assembly: WDTFDriverEDTAction.Interop.dll
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
-	WDTFDriverEDTAction.Interop.dll
api_name:
-	IWDTFEnhancedDeviceTestSupportAction2.Disable
product: Windows
targetos: Windows
req.typenames: TTraceLevel
req.product: Windows 10 or later.
---

# IWDTFEnhancedDeviceTestSupportAction2::Disable method


## -description


Disables the Enhanced Device Test (EDT) filter driver on the target device.


## -syntax


````
HRESULT Disable(
  [out, retval] VARIANT_BOOL *pbRebootRequired
);
````


## -parameters




### -param pbRebootRequired [out, retval]

True if the operation requires a restart to complete; otherwise, false.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\wdtfedtaction\nn-wdtfedtaction-iwdtfenhanceddevicetestsupportaction2.md">IWDTFEnhancedDeviceTestSupportAction2</a>



 

 


