---
UID: NE:usbfnattach._USBFN_ATTACH_ACTION
title: "_USBFN_ATTACH_ACTION"
author: windows-driver-content
description: Defines the actions that the Universal Serial Bus (USB) function stack takes when a device is attached to a USB port.
old-location: buses\usbfn_attach_action.htm
old-project: usbref
ms.assetid: 4470EBAB-6B1F-43D3-B036-F0DD07BC8321
ms.author: windowsdriverdev
ms.date: 2/24/2018
ms.keywords: "*PUSBFN_ATTACH_ACTION, USBFN_ATTACH_ACTION, USBFN_ATTACH_ACTION enumeration [Buses], UsbfnDetectProprietaryCharger, UsbfnIgnoreAttach, UsbfnPortDetected, UsbfnPortDetectedNoCad, UsbfnProceedWithAttach, _USBFN_ATTACH_ACTION, buses.usbfn_attach_action, usbfnattach/USBFN_ATTACH_ACTION, usbfnattach/UsbfnDetectProprietaryCharger, usbfnattach/UsbfnIgnoreAttach, usbfnattach/UsbfnPortDetected, usbfnattach/UsbfnPortDetectedNoCad, usbfnattach/UsbfnProceedWithAttach"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: usbfnattach.h
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	usbfnattach.h
api_name:
-	USBFN_ATTACH_ACTION
product: Windows
targetos: Windows
req.typenames: USBFN_ATTACH_ACTION, *PUSBFN_ATTACH_ACTION
req.product: Windows 10 or later.
---

# _USBFN_ATTACH_ACTION enumeration


## -description


Defines the actions that the Universal Serial Bus (USB) function stack takes when a device is attached to a USB port.


## -syntax


````
typedef enum _USBFN_ATTACH_ACTION { 
  UsbfnPortDetected              = 0,
  UsbfnPortDetectedNoCad,
  UsbfnProceedWithAttach,
  UsbfnIgnoreAttach,
  UsbfnDetectProprietaryCharger
} USBFN_ATTACH_ACTION;
````


## -enum-fields




### -field UsbfnPortDetected

The USB function stack uses the returned port type to determine charging current and notify the Charging Aggregation Driver (CAD) of the power source change.  If the detected port type is <b>UsbFnStandardDownstreamPort</b> or <b>UsbfnChargingDownstreamPort</b>, the USB function stack will attempt to connect to the host (see <a href="..\usbfnbase\ne-usbfnbase-_usbfn_port_type.md">USBFN_PORT_TYPE</a> for more information).


### -field UsbfnPortDetectedNoCad

The USB function stack does not notify the CAD of the power source change.  If the detected port type is <b>UsbFnStandardDownstreamPort</b> or <b>UsbfnChargingDownstreamPort</b>, the USB function stack attempts to connect to the host (see <a href="..\usbfnbase\ne-usbfnbase-_usbfn_port_type.md">USBFN_PORT_TYPE</a> for more information).


### -field UsbfnProceedWithAttach

The USB function stack continues with the legacy software-based detection that exists in the client drivers, and issues the CAD notifications about power source notifications.


### -field UsbfnIgnoreAttach

The USB function stack discontinues further port detection operations and does not notify CAD of a power source update.


### -field UsbfnDetectProprietaryCharger

The USB function stack calls the <a href="..\ufxproprietarycharger\nc-ufxproprietarycharger-ufx_proprietary_charger_detect.md">UFX_PROPRIETARY_CHARGER_DETECT</a> event callback function implemented by the USB lower filter driver, to perform proprietary charger detection.


### -field UsbfnHwBasedChargerDetection




## -see-also

<a href="..\usbfnattach\nc-usbfnattach-usbfn_get_attach_action.md">USBFN_GET_ATTACH_ACTION</a>



 

 


