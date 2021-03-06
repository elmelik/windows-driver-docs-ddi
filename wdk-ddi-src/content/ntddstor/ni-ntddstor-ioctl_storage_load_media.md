---
UID: NI:ntddstor.IOCTL_STORAGE_LOAD_MEDIA
title: IOCTL_STORAGE_LOAD_MEDIA
author: windows-driver-content
description: Causes media to be loaded in a device that the caller has opened for read or write access.
old-location: storage\ioctl_storage_load_media.htm
old-project: storage
ms.assetid: 137ebbec-53f7-4bf6-b43b-2c736d66eb97
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: IOCTL_STORAGE_LOAD_MEDIA, IOCTL_STORAGE_LOAD_MEDIA control code [Storage Devices], k307_730c4c03-9d36-406b-8965-270aa539d0ca.xml, ntddstor/IOCTL_STORAGE_LOAD_MEDIA, storage.ioctl_storage_load_media
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntddstor.h
req.include-header: Ntddstor.h
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
-	HeaderDef
api_location:
-	Ntddstor.h
api_name:
-	IOCTL_STORAGE_LOAD_MEDIA
product: Windows
targetos: Windows
req.typenames: STORAGE_ZONE_CONDITION, *PSTORAGE_ZONE_CONDITION
---

# IOCTL_STORAGE_LOAD_MEDIA IOCTL


## -description



Causes media to be loaded in a device that the caller has opened for read or write access. If read or write access to the device is not necessary, the caller can improve performance by opening the device with FILE_READ_ATTRIBUTES and issuing an <a href="..\ntddstor\ni-ntddstor-ioctl_storage_load_media2.md">IOCTL_STORAGE_LOAD_MEDIA2</a> request instead. 




## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

None.


### -output-buffer-length

None.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

The <b>Information</b> field is set to zero. The <b>Status</b> field is set to STATUS_SUCCESS, or possibly to STATUS_INVALID_DEVICE_REQUEST, STATUS_NO_MEDIA_IN_DEVICE, STATUS_BUFFER_TOO_SMALL, or STATUS_DEVICE_NOT_CONNECTED.


## -see-also

<a href="..\ntddstor\ni-ntddstor-ioctl_storage_load_media2.md">IOCTL_STORAGE_LOAD_MEDIA2</a>



 

 


