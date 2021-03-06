---
UID: NE:wdm._KEY_INFORMATION_CLASS
title: "_KEY_INFORMATION_CLASS"
author: windows-driver-content
description: The KEY_INFORMATION_CLASS enumeration type represents the type of information to supply about a registry key.
old-location: kernel\key_information_class.htm
old-project: kernel
ms.assetid: cb531a0e-c934-4f3e-9b92-07eb3ab75673
ms.author: windowsdriverdev
ms.date: 3/1/2018
ms.keywords: KEY_INFORMATION_CLASS, KEY_INFORMATION_CLASS enumeration [Kernel-Mode Driver Architecture], KeyBasicInformation, KeyCachedInformation, KeyFlagsInformation, KeyFullInformation, KeyHandleTagsInformation, KeyNameInformation, KeyNodeInformation, KeyVirtualizationInformation, MaxKeyInfoClass, _KEY_INFORMATION_CLASS, kernel.key_information_class, sysenum_c64ec9c8-1eda-495a-8b4a-566607e29a78.xml, wdm/KEY_INFORMATION_CLASS, wdm/KeyBasicInformation, wdm/KeyCachedInformation, wdm/KeyFlagsInformation, wdm/KeyFullInformation, wdm/KeyHandleTagsInformation, wdm/KeyNameInformation, wdm/KeyNodeInformation, wdm/KeyVirtualizationInformation, wdm/MaxKeyInfoClass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
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
-	wdm.h
api_name:
-	KEY_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: KEY_INFORMATION_CLASS
req.product: Windows 10 or later.
---

# _KEY_INFORMATION_CLASS enumeration


## -description


The <b>KEY_INFORMATION_CLASS</b> enumeration type represents the type of information to supply about a registry key.


## -syntax


````
typedef enum _KEY_INFORMATION_CLASS { 
  KeyBasicInformation           = 0,
  KeyNodeInformation            = 1,
  KeyFullInformation            = 2,
  KeyNameInformation            = 3,
  KeyCachedInformation          = 4,
  KeyFlagsInformation           = 5,
  KeyVirtualizationInformation  = 6,
  KeyHandleTagsInformation      = 7,
  MaxKeyInfoClass               = 8
} KEY_INFORMATION_CLASS;
````


## -enum-fields




### -field KeyBasicInformation

A <a href="..\wdm\ns-wdm-_key_basic_information.md">KEY_BASIC_INFORMATION</a> structure is supplied.


### -field KeyNodeInformation

A <a href="..\wdm\ns-wdm-_key_node_information.md">KEY_NODE_INFORMATION</a> structure is supplied.


### -field KeyFullInformation

A <a href="..\wdm\ns-wdm-_key_full_information.md">KEY_FULL_INFORMATION</a> structure is supplied.


### -field KeyNameInformation

A <a href="..\ntddk\ns-ntddk-_key_name_information.md">KEY_NAME_INFORMATION</a> structure is supplied.


### -field KeyCachedInformation

A <a href="..\ntddk\ns-ntddk-_key_cached_information.md">KEY_CACHED_INFORMATION</a> structure is supplied.


### -field KeyFlagsInformation

Reserved for system use.


### -field KeyVirtualizationInformation

A <a href="..\ntddk\ns-ntddk-_key_virtualization_information.md">KEY_VIRTUALIZATION_INFORMATION</a> structure is supplied.


### -field KeyHandleTagsInformation

Reserved for system use.


### -field KeyTrustInformation


### -field KeyLayerInformation


### -field MaxKeyInfoClass

The maximum value in this enumeration type.


## -remarks



Use the <b>KEY_INFORMATION_CLASS</b> values to specify the type of data to be supplied by the <a href="..\wdm\nf-wdm-zwenumeratekey.md">ZwEnumerateKey</a> and <a href="..\wdm\nf-wdm-zwquerykey.md">ZwQueryKey</a> routines.




## -see-also

<a href="..\wdm\ns-wdm-_key_full_information.md">KEY_FULL_INFORMATION</a>



<a href="..\wdm\ns-wdm-_key_basic_information.md">KEY_BASIC_INFORMATION</a>



<a href="..\ntddk\ns-ntddk-_key_virtualization_information.md">KEY_VIRTUALIZATION_INFORMATION</a>



<a href="..\wdm\ns-wdm-_key_node_information.md">KEY_NODE_INFORMATION</a>



<a href="..\ntddk\ns-ntddk-_key_cached_information.md">KEY_CACHED_INFORMATION</a>



<a href="..\wdm\nf-wdm-zwenumeratekey.md">ZwEnumerateKey</a>



<a href="..\wdm\nf-wdm-zwquerykey.md">ZwQueryKey</a>



<a href="..\ntddk\ns-ntddk-_key_name_information.md">KEY_NAME_INFORMATION</a>



 

 


