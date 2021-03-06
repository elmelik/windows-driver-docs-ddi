---
UID: NF:storport.StorPortFreeDeviceBase
title: StorPortFreeDeviceBase function
author: windows-driver-content
description: StorPortFreeDeviceBase frees a range of device I/O memory that was mapped by StorPortGetDeviceBase.
old-location: storage\storportfreedevicebase.htm
old-project: storage
ms.assetid: 4feb3bde-c243-493c-a6f9-4accd545955c
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: StorPortFreeDeviceBase, StorPortFreeDeviceBase function [Storage Devices], storage.storportfreedevicebase, storport/StorPortFreeDeviceBase, storprt_f8c3e4c6-8f38-4189-bdac-70c0c61e0f18.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
-	StorPortFreeDeviceBase
product: Windows
targetos: Windows
req.typenames: STOR_SPINLOCK
req.product: Windows 10 or later.
---

# StorPortFreeDeviceBase function


## -description


<b>StorPortFreeDeviceBase</b> frees a range of device I/O memory that was mapped by <a href="..\storport\nf-storport-storportgetdevicebase.md">StorPortGetDeviceBase</a>.


## -syntax


````
STORPORT_API VOID StorPortFreeDeviceBase(
  _In_ PVOID HwDeviceExtension,
  _In_ PVOID MappedAddress
);
````


## -parameters




### -param HwDeviceExtension [in]

A pointer to the hardware device extension. This is a per HBA storage area that the port driver allocates and initializes on behalf of the miniport driver. Miniport drivers usually store HBA-specific information in this extension, such as the state of the HBA and the mapped access ranges for the HBA. This area is available to the miniport driver immediately after the miniport driver calls <a href="..\storport\nf-storport-storportinitialize.md">StorPortInitialize</a>. The port driver frees this memory when it removes the device. 


### -param MappedAddress [in]

Pointer to region of memory to be freed.


## -returns



None 




## -see-also

<a href="..\srb\nf-srb-scsiportfreedevicebase.md">ScsiPortFreeDeviceBase</a>



<a href="..\storport\nf-storport-storportgetdevicebase.md">StorPortGetDeviceBase</a>



 

 


