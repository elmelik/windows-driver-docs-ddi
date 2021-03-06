---
UID: NF:storport.StorPortWritePortUchar
title: StorPortWritePortUchar macro
author: windows-driver-content
description: The StorPortWritePortUchar routine writes a value to a specified register address.
old-location: storage\storportwriteportuchar.htm
old-project: storage
ms.assetid: 421bd075-e919-4389-af38-e0dd686f7c05
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: StorPortWritePortUchar, StorPortWritePortUchar routine [Storage Devices], storage.storportwriteportuchar, storport/StorPortWritePortUchar, storprt_602c6d78-179c-4eaa-8131-ec2be13b2050.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: storport.h
req.include-header: Storport.h
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
req.lib: Storport.lib
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Storport.lib
-	Storport.dll
api_name:
-	StorPortWritePortUchar
product: Windows
targetos: Windows
req.typenames: STOR_SPINLOCK
req.product: Windows 10 or later.
---

# StorPortWritePortUchar macro


## -description


The <b>StorPortWritePortUchar</b> routine writes a value to a specified register address. 


## -syntax


````
STORPORT_API VOID StorPortWritePortUchar(
  _In_ PVOID  HwDeviceExtension,
  _In_ PUCHAR Port,
  _In_ UCHAR  Value
);
````


## -parameters




### -param h

TBD


### -param p

TBD


### -param v

TBD






#### - HwDeviceExtension [in]

Pointer to the hardware device extension.


#### - Port [in]

Contains the address of the port to be written to. 


#### - Value [in]

Contains the value to be written. 


## -remarks



For more information, see <a href="..\storport\nf-storport-scsiportwriteportuchar.md">ScsiPortWritePortUchar</a>. For a buffered equivalent of this routine, see <a href="..\storport\nf-storport-storportwriteportbufferuchar.md">StorPortWritePortBufferUchar</a>. 




## -see-also

<a href="..\storport\nf-storport-scsiportwriteportuchar.md">ScsiPortWritePortUchar</a>



<a href="..\storport\nf-storport-storportwriteportbufferuchar.md">StorPortWritePortBufferUchar</a>



 

 


