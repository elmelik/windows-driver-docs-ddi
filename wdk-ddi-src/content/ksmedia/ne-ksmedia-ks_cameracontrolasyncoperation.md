---
UID: NE:ksmedia.KS_CameraControlAsyncOperation
title: KS_CameraControlAsyncOperation
author: windows-driver-content
description: Defines notifications that the driver uses to start and stop an asynchronous camera operation, including setting the flash, the image pin control properties, the region of interest in the image, or video stabilization.
old-location: stream\ks_cameracontrolasyncoperation.htm
old-project: stream
ms.assetid: 0ca676d9-5047-451a-abbb-2692cc2d69f6
ms.author: windowsdriverdev
ms.date: 2/23/2018
ms.keywords: KS_CAMERACONTROL_ASYNC_RESET, KS_CAMERACONTROL_ASYNC_START, KS_CAMERACONTROL_ASYNC_STOP, KS_CameraControlAsyncOperation, KS_CameraControlAsyncOperation enumeration [Streaming Media Devices], ksmedia/KS_CAMERACONTROL_ASYNC_RESET, ksmedia/KS_CAMERACONTROL_ASYNC_START, ksmedia/KS_CAMERACONTROL_ASYNC_STOP, ksmedia/KS_CameraControlAsyncOperation, stream.ks_cameracontrolasyncoperation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ksmedia.h
req.include-header: Ksmedia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
-	Ksmedia.h
api_name:
-	KS_CameraControlAsyncOperation
product: Windows
targetos: Windows
req.typenames: KS_CameraControlAsyncOperation
---

# KS_CameraControlAsyncOperation enumeration


## -description


Defines notifications that the driver uses to start and stop an asynchronous camera operation, including setting the flash, the image pin control properties, the region of interest in the image, or video stabilization.


## -syntax


````
typedef enum  { 
  KS_CAMERACONTROL_ASYNC_START  = 0x0001,
  KS_CAMERACONTROL_ASYNC_STOP   = 0x0002,
  KS_CAMERACONTROL_ASYNC_RESET  = 0x0003
} KS_CameraControlAsyncOperation;
````


## -enum-fields




### -field KS_CAMERACONTROL_ASYNC_START

Initiate an asynchronous camera control operation.


### -field KS_CAMERACONTROL_ASYNC_STOP

Stop the requested asynchronous camera control operation and maintain current camera control settings, including the lens focus.


### -field KS_CAMERACONTROL_ASYNC_RESET

Stop the requested asynchronous camera control operation and reset the lens focus to infinity.


## -remarks



For more information, see <a href="..\ksmedia\ns-ksmedia-ksproperty_cameracontrol_s_ex.md">KSPROPERTY_CAMERACONTROL_S_EX</a>.




## -see-also

<a href="..\ksmedia\ns-ksmedia-ksproperty_cameracontrol_s_ex.md">KSPROPERTY_CAMERACONTROL_S_EX</a>



 

 


