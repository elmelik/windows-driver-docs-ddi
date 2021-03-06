---
UID: NS:iscsiop._DeleteInitiatorNodeName_OUT
title: "_DeleteInitiatorNodeName_OUT"
author: windows-driver-content
description: The DeleteInitiatorNodeName_OUT structure holds the output data for the DeleteInitiatorNodeName method.
old-location: storage\deleteinitiatornodename_out.htm
old-project: storage
ms.assetid: 105f6687-ea0f-45e9-be44-eafdd06156eb
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PDeleteInitiatorNodeName_OUT, DeleteInitiatorNodeName_OUT, DeleteInitiatorNodeName_OUT structure [Storage Devices], PDeleteInitiatorNodeName_OUT, PDeleteInitiatorNodeName_OUT structure pointer [Storage Devices], _DeleteInitiatorNodeName_OUT, iscsiop/DeleteInitiatorNodeName_OUT, iscsiop/PDeleteInitiatorNodeName_OUT, storage.deleteinitiatornodename_out, structs-iSCSI_2a85602a-f8f8-45c5-948d-128e3f5621a0.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iscsiop.h
req.include-header: Iscsiop.h
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
-	iscsiop.h
api_name:
-	DeleteInitiatorNodeName_OUT
product: Windows
targetos: Windows
req.typenames: DeleteInitiatorNodeName_OUT, *PDeleteInitiatorNodeName_OUT
---

# _DeleteInitiatorNodeName_OUT structure


## -description


The DeleteInitiatorNodeName_OUT structure holds the output data for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552500">DeleteInitiatorNodeName</a> method.


## -syntax


````
typedef struct _DeleteInitiatorNodeName_OUT {
  ULONG Status;
} DeleteInitiatorNodeName_OUT, *PDeleteInitiatorNodeName_OUT;
````


## -struct-fields




### -field Status

The status of the <b>DeleteInitiatorNodeName</b> operation. For a list of status qualifiers, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff561568">ISCSI_STATUS_QUALIFIERS</a>. 


## -remarks



It is optional that you implement this method.




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff561568">ISCSI_STATUS_QUALIFIERS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552500">DeleteInitiatorNodeName</a>



<a href="..\iscsiop\ns-iscsiop-_deleteinitiatornodename_in.md">DeleteInitiatorNodeName_IN</a>



 

 


