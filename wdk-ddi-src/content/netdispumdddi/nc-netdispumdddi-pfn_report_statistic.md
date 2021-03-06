---
UID: NC:netdispumdddi.PFN_REPORT_STATISTIC
title: PFN_REPORT_STATISTIC
author: windows-driver-content
description: Called by the user-mode display driver to report the statistics of the Miracast link to the operating system.The data type of this function is PFN_REPORT_STATISTIC.
old-location: display\reportstatistic.htm
old-project: display
ms.assetid: 13e1afa2-5552-468f-ac6b-3458dedd9b76
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFN_REPORT_STATISTIC, ReportStatistic, ReportStatistic callback function [Display Devices], display.reportstatistic, netdispumdddi/ReportStatistic
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: netdispumdddi.h
req.include-header: Netdispumdddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8.1
req.target-min-winversvr: Windows Server 2012 R2
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
-	UserDefined
api_location:
-	Netdispumdddi.h
api_name:
-	ReportStatistic
product: Windows
targetos: Windows
req.typenames: NDK_SRQ_DISPATCH
---

# PFN_REPORT_STATISTIC callback


## -description


Called by the user-mode display driver to report the statistics of the Miracast link to the operating system.The data type of this function is <b>PFN_REPORT_STATISTIC</b>.




## -prototype


````
PFN_REPORT_STATISTIC ReportStatistic;

VOID ReportStatistic(
  _In_ HANDLE                  hMiracastDeviceHandle,
  _In_ MIRACAST_STATISTIC_DATA *pStatistics
)
{ ... }
````


## -parameters




### -param hMiracastDeviceHandle [in]

A handle that represents a Miracast device. The Miracast user-mode driver previously obtained this handle as the <i>hMiracastDeviceHandle</i> parameter in a call to the <a href="..\netdispumdddi\nc-netdispumdddi-pfn_create_miracast_context.md">CreateMiracastContext</a> function.


### -param *pStatistics [in]

A pointer to a <a href="..\netdispumdddi\ns-netdispumdddi-miracast_statistic_data.md">MIRACAST_STATISTIC_DATA</a> structure that contains the statistics data.


## -returns



Does not return a value.




## -remarks



When the operating system calls this function, it logs the data from the <i>pStatistics</i> parameter but takes no other action.

For more info on how to use this function, see these topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/FF5D7760-2407-487A-8363-7AC3B6385F6C">Miracast user-mode driver tasks to support Miracast wireless displays</a>
</li>
<li>
<a href="https://msdn.microsoft.com/E1CE637F-42ED-4BEB-A2FF-04B4B88469DC">Reporting Miracast encode chunks and statistics</a>
</li>
</ul>



## -see-also

<a href="..\netdispumdddi\ns-netdispumdddi-miracast_statistic_data.md">MIRACAST_STATISTIC_DATA</a>



<a href="..\netdispumdddi\nc-netdispumdddi-pfn_create_miracast_context.md">CreateMiracastContext</a>



 

 


