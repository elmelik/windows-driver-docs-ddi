---
UID: NF:portcls.IMiniportStreamAudioEngineNode.SetStreamLoopbackProtection
title: IMiniportStreamAudioEngineNode::SetStreamLoopbackProtection method
author: windows-driver-content
description: Sets the loopback protection status of the audio engine node.
old-location: audio\iminiportstreamaudioenginenode_setstreamloopbackprotection.htm
old-project: audio
ms.assetid: FAC9AC9B-9C4B-4D53-A59A-8901EC8755BC
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IMiniportStreamAudioEngineNode, IMiniportStreamAudioEngineNode interface [Audio Devices], SetStreamLoopbackProtection method, IMiniportStreamAudioEngineNode::SetStreamLoopbackProtection, SetStreamLoopbackProtection method [Audio Devices], SetStreamLoopbackProtection method [Audio Devices], IMiniportStreamAudioEngineNode interface, SetStreamLoopbackProtection,IMiniportStreamAudioEngineNode.SetStreamLoopbackProtection, audio.iminiportstreamaudioenginenode_setstreamloopbackprotection, portcls/IMiniportStreamAudioEngineNode::SetStreamLoopbackProtection
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
-	IMiniportStreamAudioEngineNode.SetStreamLoopbackProtection
product: Windows
targetos: Windows
req.typenames: PC_EXIT_LATENCY, *PPC_EXIT_LATENCY
---

# IMiniportStreamAudioEngineNode::SetStreamLoopbackProtection method


## -description


Sets the loopback protection status of the audio engine node.


## -syntax


````
NTSTATUS SetStreamLoopbackProtection(
  [in] CONSTRICTOR_OPTION ProtectionOption
);
````


## -parameters




### -param ProtectionOption [in]

A CONSTRICTOR_OPTION enumeration  value that indicates status of the loopback protection option.


## -returns



<b>SetStreamLoopbackProtection</b> returns S_OK, if the call was successful. Otherwise, the method returns an appropriate error code.




## -remarks



For more information about audio stream loopback protection, see <a href="https://msdn.microsoft.com/library/windows/hardware/hh450878">KSPROPERTY_AUDIOENGINE_LOOPBACK_PROTECTION</a>.




## -see-also

<a href="..\portcls\nn-portcls-iminiportstreamaudioenginenode.md">IMiniportStreamAudioEngineNode</a>



CONSTRICTOR_OPTION



<a href="https://msdn.microsoft.com/library/windows/hardware/hh450878">KSPROPERTY_AUDIOENGINE_LOOPBACK_PROTECTION</a>



 

 


