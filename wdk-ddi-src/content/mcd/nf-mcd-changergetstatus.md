---
UID: NF:mcd.ChangerGetStatus
title: ChangerGetStatus function
author: windows-driver-content
description: ChangerGetStatus handles the device-specific aspects of a device-control IRP with the IOCTL code IOCTL_CHANGER_GET_STATUS.
old-location: storage\changergetstatus.htm
old-project: storage
ms.assetid: f5719dfa-e48a-4f81-8344-31b349fadb48
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: ChangerGetStatus, ChangerGetStatus function [Storage Devices], chgrmini_8975ca0f-d42c-40d0-a16c-a2ec5d2a2f66.xml, mcd/ChangerGetStatus, storage.changergetstatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mcd.h
req.include-header: Mcd.h, Ntddchgr.h
req.target-type: Desktop
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mcd.h
api_name:
-	ChangerGetStatus
product: Windows
targetos: Windows
req.typenames: LAMP_INTENSITY_WHITE
---

# ChangerGetStatus function


## -description


<b>ChangerGetStatus</b> handles the device-specific aspects of a device-control IRP with the IOCTL code <a href="..\ntddchgr\ni-ntddchgr-ioctl_changer_get_status.md">IOCTL_CHANGER_GET_STATUS</a>. 


## -syntax


````
NTSTATUS ChangerGetStatus(
  _In_ PDEVICE_OBJECT DeviceObject,
  _In_ PIRP           Irp
);
````


## -parameters




### -param DeviceObject [in]

Pointer to the device object that represents the changer. 


### -param Irp [in]

Pointer to the IRP. 


## -returns



<b>ChangerGetStatus</b> returns the STATUS_<i>XXX</i> value returned by the system port driver. If there is not enough memory to process the request or to process the STATUS_<i>XXX</i> value returned by the system port driver <b>ChangerGetStatus</b> returns STATUS_INSUFFICIENT_RESOURCES.




## -remarks



This routine is required.

<b>ChangerGetStatus</b> indicates whether the changer is able to accept requests. 

<b>ChangerGetStatus</b> builds an SRB with a CDB to get the changer's status (using the SCSI command TEST UNIT READY or non-SCSI equivalent) and sends it to the system port driver to obtain status of the changer.




## -see-also

<a href="..\ntddchgr\ni-ntddchgr-ioctl_changer_get_status.md">IOCTL_CHANGER_GET_STATUS</a>



<a href="..\mcd\nf-mcd-changergetelementstatus.md">ChangerGetElementStatus</a>



 

 


