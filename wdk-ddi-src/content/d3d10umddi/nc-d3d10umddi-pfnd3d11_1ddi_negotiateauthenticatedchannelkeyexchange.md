---
UID: NC:d3d10umddi.PFND3D11_1DDI_NEGOTIATEAUTHENTICATEDCHANNELKEYEXCHANGE
title: PFND3D11_1DDI_NEGOTIATEAUTHENTICATEDCHANNELKEYEXCHANGE
author: windows-driver-content
description: Establishes a session key for an authenticated channel.
old-location: display\negotiateauthenticatedchannelkeyexchange.htm
old-project: display
ms.assetid: a54a26d2-d38c-4e82-a3e9-7a17c0afff27
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: PFND3D11_1DDI_NEGOTIATEAUTHENTICATEDCHANNELKEYEXCHANGE, d3d10umddi/pfnNegotiateAuthenticatedChannelKeyExchange, display.negotiateauthenticatedchannelkeyexchange, pfnNegotiateAuthenticatedChannelKeyExchange, pfnNegotiateAuthenticatedChannelKeyExchange callback function [Display Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
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
-	UserDefined
api_location:
-	D3d10umddi.h
api_name:
-	pfnNegotiateAuthenticatedChannelKeyExchange
product: Windows
targetos: Windows
req.typenames: SETRESULT_INFO, *PSETRESULT_INFO
---

# PFND3D11_1DDI_NEGOTIATEAUTHENTICATEDCHANNELKEYEXCHANGE callback


## -description


Establishes a session key for an authenticated channel.




## -prototype


````
PFND3D11_1DDI_NEGOTIATEAUTHENTICATEDCHANNELKEYEXCHANGE pfnNegotiateAuthenticatedChannelKeyExchange;

HRESULT APIENTRY* pfnNegotiateAuthenticatedChannelKeyExchange(
  _In_ D3D10DDI_HDEVICE        hDevice,
  _In_ D3D11_1DDI_HAUTHCHANNEL hCAuthChannel,
  _In_ UINT                    DataSize,
  _In_ VOID                    *pData
)
{ ... }
````


## -parameters




### -param hDevice [in]

A handle to the display device (graphics context).




### -param hCAuthChannel [in]

A handle to an authenticated channel object that was created through a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createauthenticatedchannel.md">CreateAuthenticatedChannel(D3D11_1)</a> function.




### -param DataSize [in]

The size, in bytes, of the data in the <i>pData</i> array.




### -param *pData [in]

A pointer to a byte array that contains the encrypted session key.


## -returns



<b>NegotiateAuthenticatedChannelKeyExchange</b> returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The session key for the authenticated channel was negotiated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameters were validated and determined to be incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">

        Memory was not available to complete the operation.

</td>
</tr>
</table>
 




## -remarks



The <i>pData</i> parameter references a buffer that contains a session key for the authenticated channel. This key buffer must contain 256 bytes of data and must be encrypted by using the RSA Encryption Scheme - Optimal Asymmetric Encryption Padding (RSAES-OAEP) algorithm with the public key from the authenticated channel certificate.

The key exchange for an authenticated channel is identical to the key exchange for the Output Protection Manager (OPM) interface. However,  the OPM key buffer contains additional data besides the session key.  

<div class="alert"><b>Note</b>  The same certificate can be used for the authenticated channel and OPM session key.</div>
<div> </div>



## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createauthenticatedchannel.md">CreateAuthenticatedChannel(D3D11_1)</a>



 

 


