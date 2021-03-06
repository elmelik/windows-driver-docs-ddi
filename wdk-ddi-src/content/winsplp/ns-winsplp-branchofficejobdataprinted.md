---
UID: NS:winsplp.BranchOfficeJobDataPrinted
title: BranchOfficeJobDataPrinted
author: windows-driver-content
description: Contains the necessary data for logging a branch office job completed event on a remote server. This is based on standard job-related data available to the spooler.
old-location: print\branchofficejobdataprinted.htm
old-project: print
ms.assetid: 77737A33-9592-43A3-B12A-5BFDCA0209BE
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PBranchOfficeJobDataPrinted, BranchOfficeJobDataPrinted, BranchOfficeJobDataPrinted structure [Print Devices], PBranchOfficeJobDataPrinted, PBranchOfficeJobDataPrinted structure pointer [Print Devices], print.branchofficejobdataprinted, winsplp/BranchOfficeJobDataPrinted, winsplp/PBranchOfficeJobDataPrinted"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winsplp.h
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
-	HeaderDef
api_location:
-	Winsplp.h
api_name:
-	BranchOfficeJobDataPrinted
product: Windows
targetos: Windows
req.typenames: BranchOfficeJobDataPrinted, *PBranchOfficeJobDataPrinted
req.product: Windows 10 or later.
---

# BranchOfficeJobDataPrinted structure


## -description


Contains the necessary data for logging a branch office job completed event on a remote server. This is based on standard job-related data available to the spooler.


## -syntax


````
typedef struct {
  DWORD    Status;
  LPWSTR   pDocumentName;
  LPWSTR   pUserName;
  LPWSTR   pMachineName;
  LPWSTR   pPrinterName;
  LPWSTR   pPortName;
  LONGLONG Size;
  DWORD    TotalPages;
} BranchOfficeJobDataPrinted, *PBranchOfficeJobDataPrinted;
````


## -struct-fields




### -field Status

Specifies the current status, or the failure code for a JOB_ERROR event.


### -field pDocumentName

Specifies the name of the printed document.


### -field pUserName

Specifies the user who submitted the job.


### -field pMachineName

Specifies the name of the client machine printing the job


### -field pPrinterName

Specifies the name of the print connection.


### -field pPortName

Specifies the name of the port the job printed on.


### -field Size

Specifies the 64-bit size of the job.


### -field TotalPages

Specifies the total number of pages in the job.

