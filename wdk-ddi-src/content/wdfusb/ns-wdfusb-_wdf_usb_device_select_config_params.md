---
UID: NS:wdfusb._WDF_USB_DEVICE_SELECT_CONFIG_PARAMS
title: "_WDF_USB_DEVICE_SELECT_CONFIG_PARAMS"
author: windows-driver-content
description: The WDF_USB_DEVICE_SELECT_CONFIG_PARAMS structure specifies USB device configuration parameters.
old-location: wdf\wdf_usb_device_select_config_params.htm
old-project: wdf
ms.assetid: d48484eb-a7bf-4ca7-9d18-4c4c166db90c
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: "*PWDF_USB_DEVICE_SELECT_CONFIG_PARAMS, DFUsbRef_1f6335f1-ec4c-413e-b176-46b1bdf70d46.xml, PWDF_USB_DEVICE_SELECT_CONFIG_PARAMS, PWDF_USB_DEVICE_SELECT_CONFIG_PARAMS structure pointer, WDF_USB_DEVICE_SELECT_CONFIG_PARAMS, WDF_USB_DEVICE_SELECT_CONFIG_PARAMS structure, _WDF_USB_DEVICE_SELECT_CONFIG_PARAMS, kmdf.wdf_usb_device_select_config_params, wdf.wdf_usb_device_select_config_params, wdfusb/PWDF_USB_DEVICE_SELECT_CONFIG_PARAMS, wdfusb/WDF_USB_DEVICE_SELECT_CONFIG_PARAMS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wdfusb.h
req.include-header: Wdfusb.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 1.0
req.umdf-ver: 2.0
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
-	wdfusb.h
api_name:
-	WDF_USB_DEVICE_SELECT_CONFIG_PARAMS
product: Windows
targetos: Windows
req.typenames: WDF_USB_DEVICE_SELECT_CONFIG_PARAMS, *PWDF_USB_DEVICE_SELECT_CONFIG_PARAMS
req.product: Windows 10 or later.
---

# _WDF_USB_DEVICE_SELECT_CONFIG_PARAMS structure


## -description


<p class="CCE_Message">[Applies to KMDF and UMDF]

The <b>WDF_USB_DEVICE_SELECT_CONFIG_PARAMS</b> structure specifies USB device configuration parameters.


## -syntax


````
typedef struct _WDF_USB_DEVICE_SELECT_CONFIG_PARAMS {
  ULONG                              Size;
  WdfUsbTargetDeviceSelectConfigType Type;
  union {
    struct {
      PUSB_CONFIGURATION_DESCRIPTOR ConfigurationDescriptor;
      PUSB_INTERFACE_DESCRIPTOR     *InterfaceDescriptors;
      ULONG                         NumInterfaceDescriptors;
    } Descriptor;
    struct {
      PURB Urb;
    } Urb;
    struct {
      UCHAR           NumberConfiguredPipes;
      WDFUSBINTERFACE ConfiguredUsbInterface;
    } SingleInterface;
    struct {
      UCHAR                           NumberInterfaces;
      PWDF_USB_INTERFACE_SETTING_PAIR Pairs;
      UCHAR                           NumberOfConfiguredInterfaces;
    } MultiInterface;
  } Types;
} WDF_USB_DEVICE_SELECT_CONFIG_PARAMS, *PWDF_USB_DEVICE_SELECT_CONFIG_PARAMS;
````


## -struct-fields




### -field Size

The size, in bytes, of this structure. 


### -field Type

A <a href="..\wdfusb\ne-wdfusb-_wdfusbtargetdeviceselectconfigtype.md">WdfUsbTargetDeviceSelectConfigType</a>-typed value that either specifies the type of configuration that is being selected or indicates that the current configuration is being deconfigured.


### -field Types


### -field Types.Descriptor


### -field Types.Descriptor.ConfigurationDescriptor

If the driver sets the <b>Type</b> member to <b>WdfUsbTargetDeviceSelectConfigTypeInterfacesDescriptor</b>, this member contains a driver-supplied pointer to a <a href="..\usbspec\ns-usbspec-_usb_configuration_descriptor.md">USB_CONFIGURATION_DESCRIPTOR</a> structure that specifies a configuration descriptor. If this pointer is <b>NULL</b>, the framework uses the device's first configuration. For more information about selecting a USB configuration, see the Remarks section of <a href="..\wdfusb\nf-wdfusb-wdfusbtargetdeviceselectconfig.md">WdfUsbTargetDeviceSelectConfig</a>.


### -field Types.Descriptor.InterfaceDescriptors

If the driver sets <b>Type</b> to <b>WdfUsbTargetDeviceSelectConfigTypeInterfacesDescriptor</b>, this member contains a driver-supplied pointer to an array of <a href="..\usbspec\ns-usbspec-_usb_interface_descriptor.md">USB_INTERFACE_DESCRIPTOR</a> structures that represent the interfaces to select for the configuration.


### -field Types.Descriptor.NumInterfaceDescriptors

If the driver sets <b>Type</b> to <b>WdfUsbTargetDeviceSelectConfigTypeInterfacesDescriptor</b>, this member contains the number of elements that are in the interface array that <b>Types.Descriptor.InterfaceDescriptors</b> points to.


### -field Types.Urb


### -field Types.Urb.Urb

If the driver sets <b>Type</b> to <b>WdfUsbTargetDeviceSelectConfigTypeUrb</b>, this member specifies a driver-initialized <a href="..\usb\ns-usb-_urb.md">URB</a> structure that the framework uses to configure the device. 


### -field Types.SingleInterface


### -field Types.SingleInterface.NumberConfiguredPipes

If the driver sets <b>Type</b> to <b>WdfUsbTargetDeviceSelectConfigTypeSingleInterface</b>, the framework provides the number of pipes that are configured for the interface. 


### -field Types.SingleInterface.ConfiguredUsbInterface

If the driver sets <b>Type</b> to <b>WdfUsbTargetDeviceSelectConfigTypeSingleInterface</b>, the framework provides a handle to a USB interface object that represents the configured interface. 


### -field Types.MultiInterface


### -field Types.MultiInterface.NumberInterfaces

If the driver sets <b>Type</b> to <b>WdfUsbTargetDeviceSelectConfigTypeInterfacesPairs</b>, this member specifies the number of elements that are in the <b>Types.MultiInterface.Pairs</b> array.


### -field Types.MultiInterface.Pairs

If the driver sets <b>Type</b> to <b>WdfUsbTargetDeviceSelectConfigTypeInterfacesPairs</b>, this member specifies a pointer to an array of <a href="..\wdfusb\ns-wdfusb-_wdf_usb_interface_setting_pair.md">WDF_USB_INTERFACE_SETTING_PAIR</a> structures that identify the interfaces to select. 


### -field Types.MultiInterface.NumberOfConfiguredInterfaces

If the driver sets <b>Type</b> to <b>WdfUsbTargetDeviceSelectConfigTypeInterfacesPairs</b> or <b>WdfUsbTargetDeviceSelectConfigTypeMultiInterface</b>, the framework provides the number if interfaces that are configured for the device.


## -remarks



The <b>WDF_USB_DEVICE_SELECT_CONFIG_PARAMS</b> structure is used as input to <a href="..\wdfusb\nf-wdfusb-wdfusbtargetdeviceselectconfig.md">WdfUsbTargetDeviceSelectConfig</a>.

To initialize a <b>WDF_USB_DEVICE_SELECT_CONFIG_PARAMS</b> structure, use one of the following functions:


<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_deconfig.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_DECONFIG</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_single_interface.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_SINGLE_INTERFACE</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_multiple_interfaces.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_MULTIPLE_INTERFACES</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_interfaces_descriptors.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_INTERFACES_DESCRIPTORS</a>



<a href="..\wdfusb\nf-wdfusb-wdf_usb_device_select_config_params_init_urb.md">WDF_USB_DEVICE_SELECT_CONFIG_PARAMS_INIT_URB</a>


If the driver sets the <b>Type</b> member to <b>WdfUsbTargetDeviceSelectConfigTypeInterfacesDescriptor</b>, it can change the USB device configuration. All other values use the current USB device configuration.




## -see-also

<a href="..\wdfusb\ne-wdfusb-_wdfusbtargetdeviceselectconfigtype.md">WdfUsbTargetDeviceSelectConfigType</a>



<a href="..\usbspec\ns-usbspec-_usb_interface_descriptor.md">USB_INTERFACE_DESCRIPTOR</a>



<a href="..\usbspec\ns-usbspec-_usb_configuration_descriptor.md">USB_CONFIGURATION_DESCRIPTOR</a>



<a href="..\wdfusb\ns-wdfusb-_wdf_usb_interface_setting_pair.md">WDF_USB_INTERFACE_SETTING_PAIR</a>



 

 


