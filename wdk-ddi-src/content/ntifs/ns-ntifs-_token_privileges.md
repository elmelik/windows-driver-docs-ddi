---
UID: NS:ntifs._TOKEN_PRIVILEGES
title: "_TOKEN_PRIVILEGES"
author: windows-driver-content
description: TOKEN_PRIVILEGES contains information about a set of privileges for an access token.
old-location: ifsk\token_privileges.htm
old-project: ifsk
ms.assetid: f2f4b2b7-bec0-42c3-904b-cbc74ca76bb3
ms.author: windowsdriverdev
ms.date: 2/16/2018
ms.keywords: "*PTOKEN_PRIVILEGES, PTOKEN_PRIVILEGES, PTOKEN_PRIVILEGES structure pointer [Installable File System Drivers], TOKEN_PRIVILEGES, TOKEN_PRIVILEGES structure [Installable File System Drivers], _TOKEN_PRIVILEGES, ifsk.token_privileges, ntifs/PTOKEN_PRIVILEGES, ntifs/TOKEN_PRIVILEGES, securitystructures_3da1d9ba-6fa7-4b16-bdd7-416890b57f7e.xml"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntifs.h
req.include-header: Ntifs.h
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
-	HeaderDef
api_location:
-	ntifs.h
api_name:
-	TOKEN_PRIVILEGES
product: Windows
targetos: Windows
req.typenames: TOKEN_PRIVILEGES, *PTOKEN_PRIVILEGES
---

# _TOKEN_PRIVILEGES structure


## -description


TOKEN_PRIVILEGES contains information about a set of privileges for an access token. 


## -syntax


````
typedef struct _TOKEN_PRIVILEGES {
  ULONG               PrivilegeCount;
  LUID_AND_ATTRIBUTES Privileges[ANYSIZE_ARRAY];
} TOKEN_PRIVILEGES, *PTOKEN_PRIVILEGES;
````


## -struct-fields




### -field PrivilegeCount

Specifies the number of entries in the <b>Privileges</b> array. 


### -field Privileges

Specifies an array of LUID_AND_ATTRIBUTES structures. Each structure contains the LUID and attributes of a privilege. 


## -see-also

<a href="..\ntifs\ne-ntifs-_token_information_class.md">TOKEN_INFORMATION_CLASS</a>



<a href="..\ntifs\nf-ntifs-sefiltertoken.md">SeFilterToken</a>



<a href="..\ntifs\nf-ntifs-zwsetinformationtoken.md">ZwSetInformationToken</a>



<a href="..\igpupvdev\ns-igpupvdev-_luid.md">LUID</a>



<a href="..\ntifs\nf-ntifs-sequeryinformationtoken.md">SeQueryInformationToken</a>



<a href="..\ntifs\ns-ntifs-_sid.md">SID</a>



<a href="..\wdm\ns-wdm-_luid_and_attributes.md">LUID_AND_ATTRIBUTES</a>



<a href="..\ntifs\nf-ntifs-zwqueryinformationtoken.md">ZwQueryInformationToken</a>



 

 


