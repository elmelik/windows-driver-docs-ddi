---
UID: NF:ucmtcpciportcontroller.UCMTCPCI_PORT_CONTROLLER_CAPABILITIES_INIT
title: UCMTCPCI_PORT_CONTROLLER_CAPABILITIES_INIT function
author: windows-driver-content
description: Initializes the UCMTCPCI_PORT_CONTROLLER_CAPABILITIES structure.
old-location: buses\ucmtcpci_port_controller_capabilities_init.htm
old-project: usbref
ms.assetid: d6a30351-4d0f-462a-bbf7-672f4da75bf5
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: UCMTCPCI_PORT_CONTROLLER_CAPABILITIES_INIT, UCMTCPCI_PORT_CONTROLLER_CAPABILITIES_INIT method [Buses], buses.ucmtcpci_port_controller_capabilities_init, ucmtcpciportcontroller/UCMTCPCI_PORT_CONTROLLER_CAPABILITIES_INIT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ucmtcpciportcontroller.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
-	ucmtcpciportcontroller.h
api_name:
-	UCMTCPCI_PORT_CONTROLLER_CAPABILITIES_INIT
product: Windows
targetos: Windows
req.typenames: UCMTCPCI_PORT_CONTROLLER_ALERT_TYPE
req.product: Windows 10 or later.
---

# UCMTCPCI_PORT_CONTROLLER_CAPABILITIES_INIT function


## -description



                        Initializes the <a href="..\ucmtcpciportcontroller\ns-ucmtcpciportcontroller-_ucmtcpci_port_controller_capabilities.md">UCMTCPCI_PORT_CONTROLLER_CAPABILITIES</a> structure.
                


## -syntax


````
VOID UCMTCPCI_PORT_CONTROLLER_CAPABILITIES_INIT(
  _Out_ PUCMTCPCI_PORT_CONTROLLER_CAPABILITIES Capabilities
);
````


## -parameters




### -param Capabilities [out]

A pointer to the driver-allocated <a href="..\ucmtcpciportcontroller\ns-ucmtcpciportcontroller-_ucmtcpci_port_controller_capabilities.md">UCMTCPCI_PORT_CONTROLLER_CAPABILITIE</a>S structure.


## -returns



This method does not return a value.




## -see-also

<a href="..\ucmtcpciportcontroller\nf-ucmtcpciportcontroller-ucmtcpciportcontrollercreate.md">UcmTcpciPortControllerCreate</a>



 

 


