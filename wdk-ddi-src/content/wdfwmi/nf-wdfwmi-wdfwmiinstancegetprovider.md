---
UID: NF:wdfwmi.WdfWmiInstanceGetProvider
title: WdfWmiInstanceGetProvider function
author: windows-driver-content
description: The WdfWmiInstanceGetProvider method returns a handle to the WMI provider object that is the parent object of a specified WMI instance object.
old-location: wdf\wdfwmiinstancegetprovider.htm
old-project: wdf
ms.assetid: e0371aeb-fcc0-4749-b70e-26b05b4f12b2
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: DFWMIRef_f5950eae-6036-4acc-91ab-d7d49ae74202.xml, WdfWmiInstanceGetProvider, WdfWmiInstanceGetProvider method, kmdf.wdfwmiinstancegetprovider, wdf.wdfwmiinstancegetprovider, wdfwmi/WdfWmiInstanceGetProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdfwmi.h
req.include-header: Wdf.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 
req.ddi-compliance: DriverCreate, KmdfIrql, KmdfIrql2
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdf01000.sys (see Framework Library Versioning.)
req.dll: 
req.irql: "<=DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Wdf01000.sys
-	Wdf01000.sys.dll
api_name:
-	WdfWmiInstanceGetProvider
product: Windows
targetos: Windows
req.typenames: WDF_WMI_PROVIDER_FLAGS
req.product: Windows 10 or later.
---

# WdfWmiInstanceGetProvider function


## -description


<p class="CCE_Message">[Applies to KMDF only]

The <b>WdfWmiInstanceGetProvider</b> method returns a handle to the WMI provider object that is the parent object of a specified WMI instance object.


## -syntax


````
WDFWMIPROVIDER WdfWmiInstanceGetProvider(
  _In_ WDFWMIINSTANCE WmiInstance
);
````


## -parameters




### -param WmiInstance [in]

A handle to a WMI instance object that the driver obtained from a previous call to <a href="..\wdfwmi\nf-wdfwmi-wdfwmiinstancecreate.md">WdfWmiInstanceCreate</a>.


## -returns



<b>WdfWmiInstanceGetProvider</b> returns a handle to a WMI provider object.

A bug check occurs if the driver supplies an invalid object handle.






## -see-also

<a href="..\wdfwmi\nf-wdfwmi-wdfwmiinstancecreate.md">WdfWmiInstanceCreate</a>



 

 


