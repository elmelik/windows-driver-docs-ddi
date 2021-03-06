---
UID: NF:portcls.IMiniportStreamAudioEngineNode.SetLfxState
title: IMiniportStreamAudioEngineNode::SetLfxState method
author: windows-driver-content
description: Sets the state of the local effects (LFX) node that is in the path of the audio stream.
old-location: audio\iminiportstreamaudioenginenode_setlfxstate.htm
old-project: audio
ms.assetid: 90EED6A9-F25D-4EF9-8523-CFFC90185588
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IMiniportStreamAudioEngineNode, IMiniportStreamAudioEngineNode interface [Audio Devices], SetLfxState method, IMiniportStreamAudioEngineNode::SetLfxState, SetLfxState method [Audio Devices], SetLfxState method [Audio Devices], IMiniportStreamAudioEngineNode interface, SetLfxState,IMiniportStreamAudioEngineNode.SetLfxState, audio.iminiportstreamaudioenginenode_setlfxstate, portcls/IMiniportStreamAudioEngineNode::SetLfxState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portcls.h
req.include-header: 
req.target-type: Universal
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
-	COM
api_location:
-	Portcls.h
api_name:
-	IMiniportStreamAudioEngineNode.SetLfxState
product: Windows
targetos: Windows
req.typenames: PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# IMiniportStreamAudioEngineNode::SetLfxState method


## -description


Sets the state of the local effects (LFX) node that is in the path of the audio stream.


## -syntax


````
NTSTATUS SetLfxState(
  [in] BOOL bEnable
);
````


## -parameters




### -param bEnable [in]

The state to which the LFX node will be set.


## -returns



<b>SetLfxState</b> returns S_OK, if the call was successful. Otherwise, the method returns an appropriate error 

code.




## -see-also

<a href="..\portcls\nn-portcls-iminiportstreamaudioenginenode.md">IMiniportStreamAudioEngineNode</a>



 

 


