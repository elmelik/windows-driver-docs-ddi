---
UID: NI:ntdddisk.IOCTL_DISK_GET_DRIVE_LAYOUT
title: IOCTL_DISK_GET_DRIVE_LAYOUT
author: windows-driver-content
description: Returns information about the number of partitions, disk signature, and features of each partition on a disk. (Floppy drivers need not handle this request.).
old-location: storage\ioctl_disk_get_drive_layout.htm
old-project: storage
ms.assetid: f3f78e70-1111-41a1-af12-1f57055d0ca1
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_LAYOUT, IOCTL_DISK_GET_DRIVE_LAYOUT control code [Storage Devices], k307_85ebcb24-3ad1-4961-bc03-d32faf9fa0fd.xml, ntdddisk/IOCTL_DISK_GET_DRIVE_LAYOUT, storage.ioctl_disk_get_drive_layout
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: ntdddisk.h
req.include-header: Ntdddisk.h
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
-	Ntdddisk.h
api_name:
-	IOCTL_DISK_GET_DRIVE_LAYOUT
product: Windows
targetos: Windows
req.typenames: DETECTION_TYPE
---

# IOCTL_DISK_GET_DRIVE_LAYOUT IOCTL


## -description



Returns information about the number of partitions, disk signature, and features of each partition on a disk. (Floppy drivers need not handle this request.)




## -ioctlparameters




### -input-buffer

None.


### -input-buffer-length

None.


### -output-buffer

The driver returns the <a href="..\ntdddisk\ns-ntdddisk-_drive_layout_information.md">DRIVE_LAYOUT_INFORMATION</a> data in the buffer at <b>Irp-&gt;AssociatedIrp.SystemBuffer</b>.


### -output-buffer-length

<b>Parameters.DeviceIoControl.OutputBufferLength</b> in the I/O stack location of the IRP indicates the size, in bytes, of the buffer, which must be &gt;= <b>sizeof</b>(DRIVE_LAYOUT_INFORMATION). Note that this structure contains a variable-sized array of <a href="..\ntdddisk\ns-ntdddisk-_partition_information.md">PARTITION_INFORMATION</a> elements.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

The <b>Information</b> field is set to the size, in bytes, of the returned data. The <b>Status</b> field can be set to STATUS_SUCCESS, or possibly to STATUS_DEVICE_OFF_LINE, STATUS_INFO_LENGTH_MISMATCH, STATUS_INSUFFICIENT_RESOURCES, or STATUS_BUFFER_TOO_SMALL.


## -see-also

<a href="..\ntdddisk\ns-ntdddisk-_partition_information.md">PARTITION_INFORMATION</a>



<a href="..\ntdddisk\ns-ntdddisk-_drive_layout_information.md">DRIVE_LAYOUT_INFORMATION</a>



 

 


