---
UID: NN:prcomoem.IPrintOemUni2
title: IPrintOemUni2
author: windows-driver-content
description: This section describes the methods defined for the IPrintOemUni2 COM interface.
old-location: print\iprintoemuni2_interface.htm
old-project: print
ms.assetid: 789ca699-89b3-41d3-9167-812f1a9eb3bc
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: IPrintOemUni2, IPrintOemUni2 interface [Print Devices], IPrintOemUni2 interface [Print Devices], described, prcomoem/IPrintOemUni2, print.iprintoemuni2_interface, print_unidrv-pscript_rendering_4a9b9325-06ac-4945-b4c6-8af045650439.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: prcomoem.h
req.include-header: 
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
-	COM
api_location:
-	prcomoem.h
api_name:
-	IPrintOemUni2
product: Windows
targetos: Windows
req.typenames: OEMPTOPTS, *POEMPTOPTS
req.product: Windows 10 or later.
---

# IPrintOemUni2 interface


## -description


This section describes the methods defined for the IPrintOemUni2 COM interface.

In addition to the methods that belong to the IPrintOemUni2 COM interface, this interface includes all of the methods that belong to the <a href="..\prcomoem\nn-prcomoem-iprintoemuni.md">IPrintOemUni</a> COM interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintOemUni2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPrintOemUni2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintOemUni2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a26f7094-8530-4525-b94a-c94dc9ba9629">GetImplementedMethod</a>
</td>
<td align="left" width="63%">
The <code>IPrintOemUni2::GetImplementedMethod</code> method is used by Unidrv to determine which <b>IPrintOemUni2</b> interface methods a rendering plug-in has implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61901d4d-7821-40b4-aaef-fd679985abb3">WritePrinter</a>
</td>
<td align="left" width="63%">
The <code>IPrintOemUni2::WritePrinter</code> method, if supported, enables a rendering plug-in to capture all output data generated by a Unidrv driver. If this method is not supported, the output data would otherwise be sent to the spooler in a call to the spooler's WritePrinter API (described in the Microsoft Windows SDK documentation).

</td>
</tr>
</table> 

