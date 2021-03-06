---
UID: NF:ks.KsQueryObjectCreateItem
title: KsQueryObjectCreateItem function
author: windows-driver-content
description: The KsQueryObjectCreateItem function returns the create item assigned to the object when created.
old-location: stream\ksqueryobjectcreateitem.htm
old-project: stream
ms.assetid: dd6d436c-6166-4baf-b180-67f7aa7238e3
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: KsQueryObjectCreateItem, KsQueryObjectCreateItem function [Streaming Media Devices], ks/KsQueryObjectCreateItem, ksfunc_57cde673-cd08-4018-b01e-45214058b435.xml, stream.ksqueryobjectcreateitem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ks.h
req.include-header: Ks.h
req.target-type: Universal
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
req.lib: Ks.lib
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Ks.lib
-	Ks.dll
api_name:
-	KsQueryObjectCreateItem
product: Windows
targetos: Windows
req.typenames: 
---

# KsQueryObjectCreateItem function


## -description


The <b>KsQueryObjectCreateItem</b> function returns the create item assigned to the object when created.


## -syntax


````
PKSOBJECT_CREATE_ITEM KsQueryObjectCreateItem(
  _In_ KSOBJECT_HEADER Header
);
````


## -parameters




### -param Header [in]

Indicates the header previously allocated.


## -returns



The <b>KsQueryObjectCreateItem</b> function returns a pointer to a create item.



