---
UID: NF:wdm.KeInitializeDeviceQueue
title: KeInitializeDeviceQueue function
author: windows-driver-content
description: The KeInitializeDeviceQueue routine initializes a device queue object to a not-busy state.
old-location: kernel\keinitializedevicequeue.htm
old-project: kernel
ms.assetid: 0df0fcba-9ae8-4c69-957a-5685ea40c378
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: KeInitializeDeviceQueue, KeInitializeDeviceQueue routine [Kernel-Mode Driver Architecture], k105_5d7ea571-8c88-45f7-917c-e42e6caac514.xml, kernel.keinitializedevicequeue, wdm/KeInitializeDeviceQueue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: IrqlKeDispatchLte, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: "<= DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	KeInitializeDeviceQueue
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# KeInitializeDeviceQueue function


## -description


The <b>KeInitializeDeviceQueue</b> routine initializes a device queue object to a not-busy state.


## -syntax


````
VOID KeInitializeDeviceQueue(
  _Out_ PKDEVICE_QUEUE DeviceQueue
);
````


## -parameters




### -param DeviceQueue [out]

Pointer to a device queue object for which the caller provides the storage. 


## -returns



None




## -remarks



<b>KeInitializeDeviceQueue</b> initializes the specified device queue and sets its state to not-busy.

A driver should call <b>KeInitializeDeviceQueue</b> from its <i>AddDevice</i> routine after creating the device object for the associated device. Storage for the device queue object must be resident: in the device extension of a driver-created device object, in the controller extension of a driver-created controller object, or in nonpaged pool allocated by the caller. 




## -see-also

<a href="..\wdm\nf-wdm-keinsertbykeydevicequeue.md">KeInsertByKeyDeviceQueue</a>



<a href="..\wdm\nf-wdm-keremovedevicequeue.md">KeRemoveDeviceQueue</a>



<a href="..\wdm\nf-wdm-keinsertdevicequeue.md">KeInsertDeviceQueue</a>



<a href="..\wdm\nf-wdm-keremoveentrydevicequeue.md">KeRemoveEntryDeviceQueue</a>



 

 


