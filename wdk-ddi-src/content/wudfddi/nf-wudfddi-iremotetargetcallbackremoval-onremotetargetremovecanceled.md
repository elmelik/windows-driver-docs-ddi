---
UID: NF:wudfddi.IRemoteTargetCallbackRemoval.OnRemoteTargetRemoveCanceled
title: IRemoteTargetCallbackRemoval::OnRemoteTargetRemoveCanceled method
author: windows-driver-content
description: A UMDF-based driver's OnRemoteTargetRemoveCanceled event callback function performs operations that are necessary when the operating system cancels the removal of a remote I/O target's device.
old-location: wdf\iremotetargetcallbackremoval_onremotetargetremovecanceled.htm
old-project: wdf
ms.assetid: 26a6e9e7-f1bb-4174-a640-f665cecfd191
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: IRemoteTargetCallbackRemoval, IRemoteTargetCallbackRemoval interface, OnRemoteTargetRemoveCanceled method, IRemoteTargetCallbackRemoval::OnRemoteTargetRemoveCanceled, OnRemoteTargetRemoveCanceled method, OnRemoteTargetRemoveCanceled method, IRemoteTargetCallbackRemoval interface, OnRemoteTargetRemoveCanceled,IRemoteTargetCallbackRemoval.OnRemoteTargetRemoveCanceled, UMDFIoTargetObjectRef_aa4d89fd-ad91-46ea-a55d-4c89d65da13e.xml, umdf.iremotetargetcallbackremoval_onremotetargetremovecanceled, wdf.iremotetargetcallbackremoval_onremotetargetremovecanceled, wudfddi/IRemoteTargetCallbackRemoval::OnRemoteTargetRemoveCanceled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfddi.h
req.include-header: Wudfddi.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.9
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
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
-	Wudfddi.h
api_name:
-	IRemoteTargetCallbackRemoval.OnRemoteTargetRemoveCanceled
product: Windows
targetos: Windows
req.typenames: POWER_ACTION, *PPOWER_ACTION
req.product: Windows 10 or later.
---

# IRemoteTargetCallbackRemoval::OnRemoteTargetRemoveCanceled method


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

A UMDF-based driver's <b>OnRemoteTargetRemoveCanceled</b> event callback function performs operations that are necessary when the operating system cancels the removal of a remote I/O target's device.


## -syntax


````
void OnRemoteTargetRemoveCanceled(
  [in] IWDFRemoteTarget *pWdfRemoteTarget
);
````


## -parameters




### -param pWdfRemoteTarget [in]

A pointer to the <a href="..\wudfddi\nn-wudfddi-iwdfremotetarget.md">IWDFRemoteTarget</a> interface of a remote target object that represents a <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/general-i-o-targets-in-umdf">remote I/O target</a>. The driver obtains this pointer when it calls <a href="https://msdn.microsoft.com/library/windows/hardware/ff556928">IWDFDevice2::CreateRemoteTarget</a>.


## -returns



None.




## -remarks



If your driver provides an <b>OnRemoteTargetRemoveCanceled</b> event callback function, the callback function must do the following:

<ol>
<li>
Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff560278">IWDFRemoteTarget::Reopen</a>.

</li>
<li>
Do any driver-specific actions that your driver requires to restart I/O to the remote I/O target.

</li>
</ol>
If the driver does not provide this callback function, the framework calls <b>IWDFRemoteTarget::Reopen</b> for the driver.

For more information about the <b>OnRemoteTargetRemoveCanceled</b> event callback function, see <a href="https://msdn.microsoft.com/479487b2-5ce5-4522-b195-58ee50d210b6">Controlling a General I/O Target's State in UMDF</a>.




## -see-also

<a href="..\wudfddi\nn-wudfddi-iremotetargetcallbackremoval.md">IRemoteTargetCallbackRemoval</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556897">IRemoteTargetCallbackRemoval::OnRemoteTargetQueryRemove</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556900">IRemoteTargetCallbackRemoval::OnRemoteTargetRemoveComplete</a>



 

 


