---
UID: NS:ndkpi._NDK_ADAPTER_DISPATCH
title: "_NDK_ADAPTER_DISPATCH"
author: windows-driver-content
description: The NDK_ADAPTER_DISPATCH structure specifies dispatch function entry points for the NDK adapter object.
old-location: netvista\ndk_adapter_dispatch.htm
old-project: netvista
ms.assetid: 61C425CB-4900-4EB2-8D33-FF235BC03929
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: NDK_ADAPTER_DISPATCH, NDK_ADAPTER_DISPATCH structure [Network Drivers Starting with Windows Vista], PNDK_ADAPTER_DISPATCH, PNDK_ADAPTER_DISPATCH structure pointer [Network Drivers Starting with Windows Vista], _NDK_ADAPTER_DISPATCH, ndkpi/NDK_ADAPTER_DISPATCH, ndkpi/PNDK_ADAPTER_DISPATCH, netvista.ndk_adapter_dispatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ndkpi.h
req.include-header: Ndkpi.h
req.target-type: Windows
req.target-min-winverclnt: None supported,Supported in NDIS 6.30 and later.
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
req.irql: "<=DISPATCH_LEVEL"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ndkpi.h
api_name:
-	NDK_ADAPTER_DISPATCH
product: Windows
targetos: Windows
req.typenames: NDK_ADAPTER_DISPATCH
---

# _NDK_ADAPTER_DISPATCH structure


## -description


The <b>NDK_ADAPTER_DISPATCH</b> structure specifies dispatch function entry points for the NDK adapter object.


## -syntax


````
typedef struct _NDK_ADAPTER_DISPATCH {
  NDK_FN_QUERY_EXTENSION_INTERFACE NdkQueryExtension;
  NDK_FN_QUERY_ADAPTER_INFO        NdkQueryAdapterInfo;
  NDK_FN_CREATE_CQ                 NdkCreateCq;
  NDK_FN_CREATE_PD                 NdkCreatePd;
  NDK_FN_CREATE_SHARED_ENDPOINT    NdkCreateSharedEndpoint;
  NDK_FN_CREATE_CONNECTOR          NdkCreateConnector;
  NDK_FN_CREATE_LISTENER           NdkCreateListener;
  NDK_FN_BUILD_LAM                 NdkBuildLAM;
  NDK_FN_RELEASE_LAM               NdkReleaseLAM;
} NDK_ADAPTER_DISPATCH, *PNDK_ADAPTER_DISPATCH;
````


## -struct-fields




### -field NdkQueryExtension

The entry point for the object's <a href="..\ndkpi\nc-ndkpi-ndk_fn_query_extension_interface.md">NDK_FN_QUERY_EXTENSION_INTERFACE</a> dispatch function.


### -field NdkQueryAdapterInfo

The entry point for the object's <a href="..\ndkpi\nc-ndkpi-ndk_fn_query_adapter_info.md">NDK_FN_QUERY_ADAPTER_INFO</a> dispatch function.


### -field NdkCreateCq

The entry point for the object's <a href="..\ndkpi\nc-ndkpi-ndk_fn_create_cq.md">NDK_FN_CREATE_CQ</a> dispatch function.


### -field NdkCreatePd

The entry point for the object's <a href="..\ndkpi\nc-ndkpi-ndk_fn_create_pd.md">NDK_FN_CREATE_PD</a> dispatch function.


### -field NdkCreateSharedEndpoint

The entry point for the object's <a href="..\ndkpi\nc-ndkpi-ndk_fn_create_shared_endpoint.md">NDK_FN_CREATE_SHARED_ENDPOINT</a> dispatch function.


### -field NdkCreateConnector

The entry point for the object's <a href="..\ndkpi\nc-ndkpi-ndk_fn_create_connector.md">NDK_FN_CREATE_CONNECTOR</a> dispatch function.


### -field NdkCreateListener

The entry point for the object's <a href="..\ndkpi\nc-ndkpi-ndk_fn_create_listener.md">NDK_FN_CREATE_LISTENER</a> dispatch function.


### -field NdkBuildLAM

The entry point for the object's <a href="..\ndkpi\nc-ndkpi-ndk_fn_build_lam.md">NDK_FN_BUILD_LAM</a> dispatch function.


### -field NdkReleaseLAM

The entry point for the object's <a href="..\ndkpi\nc-ndkpi-ndk_fn_release_lam.md">NDK_FN_RELEASE_LAM</a> dispatch function.


## -remarks



The <b>NDK_ADAPTER_DISPATCH</b> structure is used in the <a href="..\ndkpi\ns-ndkpi-_ndk_adapter.md">NDK_ADAPTER</a> structure.




## -see-also

<a href="..\ndkpi\nc-ndkpi-ndk_fn_build_lam.md">NDK_FN_BUILD_LAM</a>



<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_connector.md">NDK_FN_CREATE_CONNECTOR</a>



<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_shared_endpoint.md">NDK_FN_CREATE_SHARED_ENDPOINT</a>



<a href="..\ndkpi\nc-ndkpi-ndk_fn_release_lam.md">NDK_FN_RELEASE_LAM</a>



<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_cq.md">NDK_FN_CREATE_CQ</a>



<a href="..\ndkpi\nc-ndkpi-ndk_fn_query_extension_interface.md">NDK_FN_QUERY_EXTENSION_INTERFACE</a>



<a href="..\ndkpi\nc-ndkpi-ndk_fn_query_adapter_info.md">NDK_FN_QUERY_ADAPTER_INFO</a>



<a href="..\ndkpi\ns-ndkpi-_ndk_adapter.md">NDK_ADAPTER</a>



<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_pd.md">NDK_FN_CREATE_PD</a>



<a href="..\ndkpi\nc-ndkpi-ndk_fn_create_listener.md">NDK_FN_CREATE_LISTENER</a>



 

 


