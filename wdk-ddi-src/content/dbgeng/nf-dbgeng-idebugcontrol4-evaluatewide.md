---
UID: NF:dbgeng.IDebugControl4.EvaluateWide
title: IDebugControl4::EvaluateWide method
author: windows-driver-content
description: The EvaluateWide method evaluates an expression, returning the result.
old-location: debugger\evaluatewide.htm
old-project: debugger
ms.assetid: 1a40e8a7-ba7b-4aaf-975f-4095f9ef7ba7
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: EvaluateWide method [Windows Debugging], EvaluateWide method [Windows Debugging], IDebugControl4 interface, EvaluateWide,IDebugControl4.EvaluateWide, IDebugControl4, IDebugControl4 interface [Windows Debugging], EvaluateWide method, IDebugControl4::EvaluateWide, dbgeng/IDebugControl4::EvaluateWide, debugger.evaluatewide
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dbgeng.h
req.include-header: Dbgeng.h
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
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dbgeng.h
api_name:
-	IDebugControl4.EvaluateWide
product: Windows
targetos: Windows
req.typenames: DOT4_ACTIVITY, *PDOT4_ACTIVITY
---

# IDebugControl4::EvaluateWide method


## -description


The <b>EvaluateWide</b>  method evaluates an expression, returning the result.


## -syntax


````
HRESULT EvaluateWide(
  [in]            PCWSTR       Expression,
  [in]            ULONG        DesiredType,
  [out]           PDEBUG_VALUE Value,
  [out, optional] PULONG       RemainderIndex
);
````


## -parameters




### -param Expression [in]

Specifies the expression to be evaluated.


### -param DesiredType [in]

Specifies the desired return type.  Possible values are described in <a href="..\dbgeng\ns-dbgeng-_debug_value.md">DEBUG_VALUE</a>; with the addition of DEBUG_VALUE_INVALID, which indicates that the return type should be the expression's natural type.


### -param Value [out]

Receives the value of the expression.


### -param RemainderIndex [out, optional]

Receives the index of the first character of the expression not used in the evaluation.  If <i>RemainderIndex</i> is <b>NULL</b>, this information isn't returned.


## -returns



This method may also return other error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

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
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while evaluating the expression.  For example, there was a syntax error, an undefined variable, or a division by zero exception.

</td>
</tr>
</table>
 




## -remarks



Expressions are evaluated by the current <i>expression evaluator</i>.  The engine contains multiple expression evaluators; each supports a different syntax.  The current expression evaluator can be chosen by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff556696">SetExpressionSyntax</a>.

For details of the available expression evaluators and their syntaxes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552280">Numerical Expression Syntax</a>.

If an error occurs while evaluating the expression, returning E_FAIL, the <i>RemainderIndex</i> variable can be used to determine approximately where in the expression the error occurred. 




## -see-also

<a href="https://msdn.microsoft.com/library/windows/hardware/ff556697">SetExpressionSyntaxByName</a>



<a href="..\dbgeng\nn-dbgeng-idebugcontrol4.md">IDebugControl4</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556696">SetExpressionSyntax</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546701">GetExpressionSyntax</a>



 

 


