---
UID: NS:ucmtcpciportcontrollerrequests._UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS
title: "_UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS"
author: windows-driver-content
description: Stores information about the alternate mode that was exited. This structure is used in the IOCTL_UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED request.
old-location: buses\ucmtcpci_port_controller_alternate_mode_exited_in_params.htm
old-project: usbref
ms.assetid: FB324CA7-94B0-4BA2-A004-D333A20FCB51
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PUCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS, PUCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS, PUCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS structure pointer [Buses], UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS, UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS structure [Buses], _UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS, buses.ucmtcpci_port_controller_alternate_mode_exited_in_params, ucmtcpciportcontrollerrequests/PUCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS, ucmtcpciportcontrollerrequests/UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ucmtcpciportcontrollerrequests.h
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
-	Ucmtcpciportcontrollerrequests.h
api_name:
-	UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS
product: Windows
targetos: Windows
req.typenames: UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS, *PUCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS
req.product: Windows 10 or later.
---

# _UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS structure


## -description


Stores information about the  alternate mode that was exited. This structure is used in the 
             <a href="..\ucmtcpciportcontrollerrequests\ni-ucmtcpciportcontrollerrequests-ioctl_ucmtcpci_port_controller_alternate_mode_exited.md">IOCTL_UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED</a>  request. 


## -syntax


````
typedef struct _UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS {
  UCMTCPCIPORTCONTROLLER PortControllerObject;
  UINT16                 SVID;
  UINT32                 Mode;
} UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS, *PUCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED_IN_PARAMS;
````


## -struct-fields




### -field PortControllerObject

Handle to the port controller object that the client driver received in the previous call to <a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrollercreate.md">UcmTcpciPortControllerCreate</a>.


### -field SVID

The Standard or Vendor ID (SVID) for the alternate mode that was exited. In Windows 10, version 1703, the supported  value is DISPLAYPORT_SVID, indicating that the partner device has exited DisplayPort mode. 


### -field Mode

The Standard or Vendor defined Mode value for the alternate mode that was exited. 


## -see-also

<a href="..\ucmtcpciportcontrollerrequests\ni-ucmtcpciportcontrollerrequests-ioctl_ucmtcpci_port_controller_alternate_mode_exited.md">IOCTL_UCMTCPCI_PORT_CONTROLLER_ALTERNATE_MODE_EXITED</a>



 

 


