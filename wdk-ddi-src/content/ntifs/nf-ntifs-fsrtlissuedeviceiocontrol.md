---
UID: NF:ntifs.FsRtlIssueDeviceIoControl
title: FsRtlIssueDeviceIoControl function
author: windows-driver-content
description: The FsRtlIssueDeviceIoControl routine sends a synchronous device I/O control request to a target device object.
old-location: ifsk\fsrtlissuedeviceiocontrol.htm
old-project: ifsk
ms.assetid: 3BB31389-EB1B-4443-9FCF-70B420D71126
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: FsRtlIssueDeviceIoControl, FsRtlIssueDeviceIoControl routine [Installable File System Drivers], ifsk.fsrtlissuedeviceiocontrol, ntifs/FsRtlIssueDeviceIoControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 8.
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
req.lib: Ntoskrnl.lib
req.dll: 
req.irql: "<= APC_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	ntoskrnl.lib
-	ntoskrnl.dll
api_name:
-	FsRtlIssueDeviceIoControl
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# FsRtlIssueDeviceIoControl function


## -description


The <b>FsRtlIssueDeviceIoControl</b> routine sends a synchronous device I/O control request to a target device object.


## -syntax


````
NTSTATUS FsRtlIssueDeviceIoControl(
  _In_      PDEVICE_OBJECT DeviceObject,
  _In_      ULONG          IoCtl,
  _In_      ULONG          IrpFlags,
  _In_opt_  ULONG          InputBuffer,
  _In_      ULONG          InputBufferLength,
  _Out_opt_ ULONG          OutputBuffer,
  _In_      ULONG          OutputBufferLength,
  _In_      PULONG_PTR     IosbInformation
);
````


## -parameters




### -param DeviceObject [in]

The target device object.


### -param IoCtl [in]

The IOCTL control code to issue.


### -param Flags

TBD


### -param InputBuffer [in, optional]

An optional buffer containing the input data for the request.


### -param InputBufferLength [in]

The length, in bytes, of the input data in <i>InputBuffer</i>.


### -param OutputBuffer [out, optional]

An optional caller-supplied output buffer for returned data.


### -param OutputBufferLength [in]

The length, in bytes, of the output data buffer at <i>OutputBuffer</i>.


### -param IosbInformation [in]

A pointer to a <b>ULONG</b> status value to receive the information field value set in the I/O status block at completion of the request.


#### - IrpFlags [in]

The desired IRP flags to set for IOCTL request.


## -returns



<b>FsRtlIssueDeviceIoControl</b> returns <b>STATUS_SUCCESS</b> or an another <b>NTSTATUS</b> value returned in the status block from the I/O operation.




## -see-also

<a href="..\fltkernel\nf-fltkernel-fltdeviceiocontrolfile.md">FltDeviceIoControlFile</a>



 

 


