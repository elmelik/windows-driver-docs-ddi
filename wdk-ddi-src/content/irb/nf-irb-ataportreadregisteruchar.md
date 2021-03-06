---
UID: NF:irb.AtaPortReadRegisterUchar
title: AtaPortReadRegisterUchar function
author: windows-driver-content
description: The AtaPortReadRegisterUchar routine reads an unsigned byte value from the HBA.Note  The ATA port driver and ATA miniport driver models may be altered or unavailable in the future.
old-location: storage\ataportreadregisteruchar.htm
old-project: storage
ms.assetid: 1baa8d01-b889-4f2b-ad9e-f35078f7b3d8
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: AtaPortReadRegisterUchar, AtaPortReadRegisterUchar routine [Storage Devices], atartns_63ee26b2-b436-4dc6-a3aa-5a13691e85dd.xml, irb/AtaPortReadRegisterUchar, storage.ataportreadregisteruchar
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: irb.h
req.include-header: Ata.h, Irb.h
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
req.lib: Ataport.lib; Pciidex.lib
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	ataport.lib
-	ataport.dll
-	pciidex.lib
-	pciidex.dll
api_name:
-	AtaPortReadRegisterUchar
product: Windows
targetos: Windows
req.typenames: IDE_POWER_STATE
---

# AtaPortReadRegisterUchar function


## -description


The <b>AtaPortReadRegisterUchar</b> routine reads an unsigned byte value from the HBA.
<div class="alert"><b>Note</b>  The ATA port driver and ATA miniport driver models may be altered or unavailable in the future. Instead, we recommend using the <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-driver">Storport driver</a> and <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-miniport-drivers">Storport miniport</a> driver models.</div><div> </div>

## -syntax


````
UCHAR AtaPortReadRegisterUchar(
  _In_ PUCHAR Register
);
````


## -parameters




### -param Register [in]

A pointer to the register to read. The address value that is assigned to this parameter must be within the range of mapped I/O space addresses that are obtained by a call to <a href="..\irb\nf-irb-ataportgetdevicebase.md">AtaPortGetDeviceBase</a>.


## -returns



<b>AtaPortReadRegisterUchar</b> returns a UCHAR value from the HBA's register. 




## -see-also

<a href="..\irb\nf-irb-ataportgetdevicebase.md">AtaPortGetDeviceBase</a>



<a href="..\irb\nf-irb-ataportreadregisterulong.md">AtaPortReadRegisterUlong</a>



<a href="..\irb\nf-irb-ataportreadregisterushort.md">AtaPortReadRegisterUshort</a>



 

 


