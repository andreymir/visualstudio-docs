---
title: "IEnumDebugObjects | Microsoft Docs"
ms.custom: ""
ms.date: 11/15/2016
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IEnumDebugObjects"
helpviewer_keywords: 
  - "IEnumDebugObjects interface"
ms.assetid: 0950364c-6c8a-4b6c-ba37-c6aa359fa72c
caps.latest.revision: 10
ms.author: gregvanl
manager: "ghogen"
---
# IEnumDebugObjects
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

> [!IMPORTANT]
>  In Visual Studio 2015, this way of implementing expression evaluators is deprecated. For information about implementing CLR expression evaluators, please see [CLR Expression Evaluators](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) and [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 This interface represents a collection of objects implementing the [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) interface.  
  
## Syntax  
  
```  
IEnumDebugObjects : IUnknown  
```  
  
## Notes for Implementers  
 The expression evaluator implements this interface to provide sets of objects that implement the [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) interface. Note that this is not a standard COM enumeration due to the presence of the [GetCount](../../../extensibility/debugger/reference/ienumdebugobjects-getcount.md) method.  
  
## Notes for Callers  
 [GetElements](../../../extensibility/debugger/reference/idebugarrayobject-getelements.md) returns this interface.  
  
## Methods in Vtable order  
 This interface implements the following methods.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugobjects-next.md)|Retrieves the next set of [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) objects from the enumeration.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugobjects-skip.md)|Skips a specified number of entries.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugobjects-reset.md)|Resets the enumeration to the first entry.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugobjects-clone.md)|Retrieves a copy of the current enumeration.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugobjects-getcount.md)|Retrieves the number of entries in the enumeration.|  
  
## Remarks  
 This interface allows a debug engine to enumerate over a set of objects in an array.  
  
## Requirements  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)   
 [GetElements](../../../extensibility/debugger/reference/idebugarrayobject-getelements.md)

