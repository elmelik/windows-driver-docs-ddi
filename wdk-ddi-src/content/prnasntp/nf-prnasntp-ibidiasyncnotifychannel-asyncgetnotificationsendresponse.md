---
UID: NF:prnasntp.IBidiAsyncNotifyChannel.AsyncGetNotificationSendResponse
title: IBidiAsyncNotifyChannel::AsyncGetNotificationSendResponse method
author: windows-driver-content
description: "."
old-location: print\ibidiasyncnotifychannel_asyncgetnotificationsendresponse.htm
old-project: print
ms.assetid: F30A1DEA-2B54-417A-AFE7-289655C815E2
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: AsyncGetNotificationSendResponse method [Print Devices], AsyncGetNotificationSendResponse method [Print Devices], IBidiAsyncNotifyChannel interface, AsyncGetNotificationSendResponse,IBidiAsyncNotifyChannel.AsyncGetNotificationSendResponse, IBidiAsyncNotifyChannel, IBidiAsyncNotifyChannel interface [Print Devices], AsyncGetNotificationSendResponse method, IBidiAsyncNotifyChannel::AsyncGetNotificationSendResponse, print.ibidiasyncnotifychannel_asyncgetnotificationsendresponse, prnasntp/IBidiAsyncNotifyChannel::AsyncGetNotificationSendResponse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: prnasntp.h
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Prnasntp.h
api_name:
-	IBidiAsyncNotifyChannel.AsyncGetNotificationSendResponse
product: Windows
targetos: Windows
req.typenames: USERDATA, *PUSERDATA
req.product: Windows 10 or later.
---

# IBidiAsyncNotifyChannel::AsyncGetNotificationSendResponse method


## -description





## -syntax


````
HRESULT AsyncGetNotificationSendResponse(
  [in] IPrintAsyncNotifyDataObject     *pObject,
  [in] IAsyncGetSendNotificationCookie *pCookie
);
````


## -parameters




### -param param




### -param EQUALNULL






#### - pCookie [in]


#### - pObject [in]


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also

<a href="..\prnasntp\nn-prnasntp-ibidiasyncnotifychannel.md">IBidiAsyncNotifyChannel</a>



 

 


