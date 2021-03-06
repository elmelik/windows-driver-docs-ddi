---
UID: NF:rxtimer.RxPostOneShotTimerRequest
title: RxPostOneShotTimerRequest function
author: windows-driver-content
description: RxPostOneShotTimerRequest initializes a one-shot timer entry. The passed-in pointer to a worker thread routine is called once when the timer expires.
old-location: ifsk\rxpostoneshottimerrequest.htm
old-project: ifsk
ms.assetid: d3ae6401-6d1b-428f-ae74-e262682bcb10
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: RxPostOneShotTimerRequest, RxPostOneShotTimerRequest routine [Installable File System Drivers], ifsk.rxpostoneshottimerrequest, rxref_9fb32d67-ac0a-4f85-b999-5f5beaf6b26f.xml, rxtimer/RxPostOneShotTimerRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rxtimer.h
req.include-header: Rxtimer.h, Rxworkq.h
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
req.lib: 
req.dll: 
req.irql: "<= APC_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	rxtimer.h
api_name:
-	RxPostOneShotTimerRequest
product: Windows
targetos: Windows
req.typenames: RX_CONTEXT, *PRX_CONTEXT
req.product: Windows 10 or later.
---

# RxPostOneShotTimerRequest function


## -description


<b>RxPostOneShotTimerRequest</b> initializes a one-shot timer entry. The passed-in pointer to a worker thread routine is called once when the timer expires. 


## -syntax


````
NTSTATUS RxPostOneShotTimerRequest(
  _In_ PRDBSS_DEVICE_OBJECT     pDeviceObject,
  _In_ PRX_WORK_ITEM            pWorkItem,
  _In_ PRX_WORKERTHREAD_ROUTINE Routine,
  _In_ PVOID                    pContext,
  _In_ LARGE_INTEGER            TimeInterval
);
````


## -parameters




### -param pDeviceObject [in]

A pointer to the device object to be associated with this timer. 


### -param pWorkItem [in]

A pointer to the worker item.


### -param Routine [in]

A pointer to the worker thread routine to call when this timer expires. 


### -param pContext [in]

A pointer to the context parameter associated with this timer.


### -param TimeInterval [in]

The time interval, in 100-nanosecond ticks.


## -returns



<b>RxPostOneShotTimerRequest</b>
      returns STATUS_SUCCESS on success. 

If a <b>NULL</b> pointer is passed as the <i>pWorkItem</i> parameter, this routine causes the system to ASSERT on checked builds.




## -see-also

<a href="..\rxtimer\nf-rxtimer-rxcanceltimerrequest.md">RxCancelTimerRequest</a>



<a href="..\rxtimer\nf-rxtimer-rxpostrecurrenttimerrequest.md">RxPostRecurrentTimerRequest</a>



 

 


