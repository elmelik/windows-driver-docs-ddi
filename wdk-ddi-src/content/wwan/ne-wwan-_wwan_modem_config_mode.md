---
UID: NE:wwan._WWAN_MODEM_CONFIG_MODE
title: "_WWAN_MODEM_CONFIG_MODE"
author: windows-driver-content
description: The WWAN_MODEM_CONFIG_MODE enumeration lists modem configuration modes.
old-location: netvista\wwan_modem_config_mode.htm
old-project: netvista
ms.assetid: 1AA3EDCC-EB6E-4118-8081-CA1914140683
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PWWAN_MODEM_CONFIG_MODE, PWWAN_MODEM_CONFIG_MODE, PWWAN_MODEM_CONFIG_MODE enumeration pointer [Network Drivers Starting with Windows Vista], WWAN_MODEM_CONFIG_MODE, WWAN_MODEM_CONFIG_MODE enumeration [Network Drivers Starting with Windows Vista], WwanModemConfigModeHostCentric, WwanModemConfigModeMax, WwanModemConfigModeModemCentric, WwanModemConfigModeUnknown, _WWAN_MODEM_CONFIG_MODE, netvista.wwan_modem_config_mode, wwan/PWWAN_MODEM_CONFIG_MODE, wwan/WWAN_MODEM_CONFIG_MODE, wwan/WwanModemConfigModeHostCentric, wwan/WwanModemConfigModeMax, wwan/WwanModemConfigModeModemCentric, wwan/WwanModemConfigModeUnknown"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wwan.h
req.include-header: Wwan.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709
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
-	wwan.h
api_name:
-	WWAN_MODEM_CONFIG_MODE
product: Windows
targetos: Windows
req.typenames: WWAN_MODEM_CONFIG_MODE, *PWWAN_MODEM_CONFIG_MODE
req.product: Windows 10 or later.
---

# _WWAN_MODEM_CONFIG_MODE enumeration


## -description


The <b>WWAN_MODEM_CONFIG_MODE</b> enumeration lists modem configuration modes.


## -syntax


````
typedef enum _WWAN_MODEM_CONFIG_MODE { 
  WwanModemConfigModeUnknown       = 0,
  WwanModemConfigModeModemCentric,
  WwanModemConfigModeHostCentric,
  WwanModemConfigModeMax
} WWAN_MODEM_CONFIG_MODE, *PWWAN_MODEM_CONFIG_MODE;
````


## -enum-fields




### -field WwanModemConfigModeUnknown

The modem configuration mode is currently not available.


### -field WwanModemConfigModeModemCentric

The modem configuration mode is modem centric. The modem is responsible for the selection process of configuration based on UICC info or any other vendor-specified algorithm.


### -field WwanModemConfigModeHostCentric

The modem configuration mode is host centric. The host will inform the modem which configuration file the modem will use.


### -field WwanModemConfigModeMax

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.


## -remarks



The modem configuration mode shall not change during runtime. If a change is detected, it will be ignored by the OS.




## -see-also

<a href="..\wwan\ns-wwan-_wwan_modem_config_info.md">WWAN_MODEM_CONFIG_INFO</a>



 

 


