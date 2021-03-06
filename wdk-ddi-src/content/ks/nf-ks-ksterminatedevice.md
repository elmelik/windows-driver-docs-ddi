---
UID: NF:ks.KsTerminateDevice
title: KsTerminateDevice function
author: windows-driver-content
description: The KsTerminateDevice function removes an AVStream device.
old-location: stream\ksterminatedevice.htm
old-project: stream
ms.assetid: 3d6ad381-0bd9-47d8-a4dd-e434b62bf5a1
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: KsTerminateDevice, KsTerminateDevice function [Streaming Media Devices], avfunc_42f55ca4-ed73-4ea2-9f33-462d9d13e3e3.xml, ks/KsTerminateDevice, stream.ksterminatedevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ks.h
req.include-header: Ks.h
req.target-type: Universal
req.target-min-winverclnt: Available in Microsoft Windows XP and later operating systems and DirectX 8.0 and later DirectX versions.
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Ks.lib
-	Ks.dll
api_name:
-	KsTerminateDevice
product: Windows
targetos: Windows
req.typenames: 
---

# KsTerminateDevice function


## -description


The<b> KsTerminateDevice </b>function removes an AVStream device.


## -syntax


````
void KsTerminateDevice(
  _In_ PDEVICE_OBJECT DeviceObject
);
````


## -parameters




### -param DeviceObject [in]

A pointer to a <a href="..\wdm\ns-wdm-_device_object.md">DEVICE_OBJECT</a> structure corresponding to the device for which to remove AVStream support.


## -returns



None




## -remarks



Normally, AVStream calls <b>KsTerminateDevice</b> upon receipt of a PnP remove device IRP (IRP_MN_REMOVE_DEVICE). Most minidrivers do not call this function directly; however, it can be used to remove AVStream support for the device given in <i>DeviceObject</i>. 




## -see-also

<a href="..\wdm\ns-wdm-_device_object.md">DEVICE_OBJECT</a>



<a href="..\ks\nf-ks-ksadddevice.md">KsAddDevice</a>



<a href="..\ks\nf-ks-ksinitializedevice.md">KsInitializeDevice</a>



<a href="..\wdm\ns-wdm-_driver_object.md">DRIVER_OBJECT</a>



<a href="..\ks\nf-ks-ksinitializedriver.md">KsInitializeDriver</a>



<a href="..\ks\nf-ks-kscreatedevice.md">KsCreateDevice</a>



<a href="..\ks\ns-ks-_ksdevice.md">KSDEVICE</a>



 

 


