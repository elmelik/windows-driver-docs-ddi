---
UID: NC:ndis.PROTOCOL_UNINSTALL
title: PROTOCOL_UNINSTALL
author: windows-driver-content
description: NDIS calls a protocol driver's ProtocolUninstall function to perform cleanup operations before a protocol driver is uninstalled.Note  You must declare the function by using the PROTOCOL_UNINSTALL type.
old-location: netvista\protocoluninstall.htm
old-project: netvista
ms.assetid: 959baf54-849c-4bb1-b4c5-4d5537e1d688
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: PROTOCOL_UNINSTALL, ProtocolUninstall, ProtocolUninstall callback function [Network Drivers Starting with Windows Vista], ndis/ProtocolUninstall, netvista.protocoluninstall, protocol_functions_ref_5c889ae3-39d9-43ff-84b5-8ecbb0b48be5.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ndis.h
req.include-header: Ndis.h
req.target-type: Windows
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
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
-	UserDefined
api_location:
-	Ndis.h
api_name:
-	ProtocolUninstall
product: Windows
targetos: Windows
req.typenames: VIDEO_STREAM_INIT_PARMS, *LPVIDEO_STREAM_INIT_PARMS
---

# PROTOCOL_UNINSTALL callback


## -description


NDIS calls a protocol driver's 
  <i>ProtocolUninstall</i> function to perform cleanup operations before a protocol driver is
  uninstalled.
<div class="alert"><b>Note</b>  You must declare the function by using the <b>PROTOCOL_UNINSTALL</b> type. For more
   information, see the following Examples section.</div><div> </div>

## -prototype


````
PROTOCOL_UNINSTALL ProtocolUninstall;

VOID ProtocolUninstall(void)
{ ... }
````


## -parameters










## -returns



None




## -remarks



The 
    <i>ProtocolUninstall</i> function is optional. The protocol driver registered an entry point, if any, for
    this function in the 
    <a href="..\ndis\ns-ndis-_ndis_protocol_driver_characteristics.md">
    NDIS_PROTOCOL_DRIVER_CHARACTERISTICS</a> structure that it passed to the 
    <a href="..\ndis\nf-ndis-ndisregisterprotocoldriver.md">
    NdisRegisterProtocolDriver</a> function.

In response to a user request to uninstall a protocol driver, NDIS calls a protocol driver's 
    <i>ProtocolUninstall</i> function. NDIS calls 
    <i>ProtocolUninstall</i> after calling the protocol driver's 
    <a href="..\ndis\nc-ndis-protocol_unbind_adapter_ex.md">
    ProtocolUnbindAdapterEx</a> function once for each bound adapter.

<i>ProtocolUninstall</i> performs driver-determined cleanup operations. For example, 
    <i>ProtocolUninstall</i> could request clients to close open handles to device objects that the protocol
    driver exported. Until all such handles are closed, the I/O manager will not call the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff564886">Unload</a> routine that the protocol driver registered in
    the driver object passed to its 
    <a href="..\wudfwdm\nc-wudfwdm-driver_initialize.md">DriverEntry</a> routine. After all the handles are
    closed, 
    <i>ProtocolUninstall</i> can call 
    <a href="..\ndis\nf-ndis-ndisderegisterdeviceex.md">NdisDeregisterDeviceEx</a> to delete
    any device objects created by the protocol driver.

The protocol lower edge of an intermediate driver might require a 
    <i>ProtocolUninstall</i> function. The intermediate driver can release its protocol edge resources in 
    <i>ProtocolUninstall</i> before NDIS calls its 
    <a href="..\ndis\nc-ndis-miniport_unload.md">MiniportDriverUnload</a> function.

NDIS calls
    <i>ProtocolUninstall</i> at IRQL = PASSIVE_LEVEL.

<h3><a id="Examples"></a><a id="examples"></a><a id="EXAMPLES"></a>Examples</h3>
To define a <i>ProtocolUninstall</i> function, you must first provide a function declaration that identifies the type of function you're defining. Windows provides a set of function types for drivers. Declaring a function using the function types helps <a href="https://msdn.microsoft.com/2F3549EF-B50F-455A-BDC7-1F67782B8DCA">Code Analysis for Drivers</a>, <a href="https://msdn.microsoft.com/74feeb16-387c-4796-987a-aff3fb79b556">Static Driver Verifier</a> (SDV), and other verification tools find errors, and it's a requirement for writing drivers for the Windows operating system.

For example, to define a <i>ProtocolUninstall</i> function that is named "MyUninstall", use the <b>PROTOCOL_UNINSTALL</b> type as shown in this code example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>PROTOCOL_UNINSTALL MyUninstall;</pre>
</td>
</tr>
</table></span></div>
Then, implement your function as follows:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>_Use_decl_annotations_
VOID
 MyUninstall(void)
  {...}</pre>
</td>
</tr>
</table></span></div>
The <b>PROTOCOL_UNINSTALL</b> function type is defined in the Ndis.h header file. To more accurately identify errors when you run the code analysis tools, be sure to add the _Use_decl_annotations_ annotation to your function definition.  The _Use_decl_annotations_ annotation ensures that the annotations that are applied to the <b>PROTOCOL_UNINSTALL</b> function type in the header file are used.  For more information about the requirements for function declarations, see <a href="https://msdn.microsoft.com/232c4272-0bf0-4a4e-9560-3bceeca8a3e3">Declaring Functions by Using Function Role Types for NDIS Drivers</a>.

For information about  _Use_decl_annotations_, see <a href="http://go.microsoft.com/fwlink/p/?linkid=286697">Annotating Function Behavior</a>. 




## -see-also

<a href="..\ndis\nf-ndis-ndisderegisterdeviceex.md">NdisDeregisterDeviceEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564886">Unload</a>



<a href="..\ndis\nc-ndis-protocol_unbind_adapter_ex.md">ProtocolUnbindAdapterEx</a>



<a href="..\wudfwdm\nc-wudfwdm-driver_initialize.md">DriverEntry</a>



<a href="..\ndis\nc-ndis-miniport_unload.md">MiniportDriverUnload</a>



<a href="..\ndis\ns-ndis-_ndis_protocol_driver_characteristics.md">
   NDIS_PROTOCOL_DRIVER_CHARACTERISTICS</a>



<a href="..\ndis\nf-ndis-ndisregisterprotocoldriver.md">NdisRegisterProtocolDriver</a>



 

 


