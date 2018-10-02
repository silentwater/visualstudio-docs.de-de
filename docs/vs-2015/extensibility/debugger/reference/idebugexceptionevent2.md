---
title: IDebugExceptionEvent2 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugExceptionEvent2
helpviewer_keywords:
- IDebugExceptionEvent2 interface
ms.assetid: 53d32e59-a84b-4710-833e-c5ab08100516
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8f873f76eeac3af93d8ce031d2b4315e2dcacc72
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2018
ms.locfileid: "47522384"
---
# <a name="idebugexceptionevent2"></a>IDebugExceptionEvent2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Die neueste Version dieses Themas finden Sie unter [IDebugExceptionEvent2](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugexceptionevent2).  
  
Die Debug-Engine (DE) sendet diese Schnittstelle für die Sitzung Debug-Manager (SDM), wenn eine Ausnahme ausgelöst wird, in der Anwendung, die gerade ausgeführt wird.  
  
## <a name="syntax"></a>Syntax  
  
```  
IDebugExceptionEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Hinweise für Implementierer  
 Die DE implementiert diese Schnittstelle für den Bericht, in der zu debuggende Programm wird eine Ausnahme aufgetreten ist. Die [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) Schnittstelle muss auf dasselbe Objekt wie diese Schnittstelle implementiert werden. Wird verwendet, das SDM [QueryInterface](http://msdn.microsoft.com/library/62fce95e-aafa-4187-b50b-e6611b74c3b3) für den Zugriff auf die `IDebugEvent2` Schnittstelle.  
  
## <a name="notes-for-callers"></a>Hinweise für Aufrufer  
 Die DE erstellt und sendet dieses Ereignisobjekt, um eine Ausnahme zu melden. Das Ereignis gesendet wird, mit der [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) Callback-Funktion, die durch die SDM bereitgestellt wird, wenn diese an die zu debuggende Programm wird angefügt.  
  
## <a name="methods-in-vtable-order"></a>Methoden in Vtable-Reihenfolge  
 Die folgende Tabelle zeigt die Methoden der `IDebugExceptionEvent2`.  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[GetException](../../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md)|Ruft detaillierte Informationen über die Ausnahme, die dieses Ereignis ausgelöst hat.|  
|[GetExceptionDescription](../../../extensibility/debugger/reference/idebugexceptionevent2-getexceptiondescription.md)|Ruft eine lesbare Beschreibung für die ausgelöste Ausnahme, die dieses Ereignis ausgelöst hat.|  
|[CanPassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md)|Bestimmt, ob die Debug-Engine (DE) die Möglichkeit unterstützt, übergeben diese Ausnahme an die Anwendung gedebuggt wird, wenn die Ausführung fortsetzt.|  
|[PassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-passtodebuggee.md)|Gibt an, ob die Ausnahme übergeben werden soll, die zu debuggende Programm wird bei der Ausführung fortgesetzt wird, oder die Ausnahme verworfen werden sollen.|  
  
## <a name="requirements"></a>Anforderungen  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="remarks"></a>Hinweise  
 Vor dem Senden des Ereignisses, das DE überprüft, um festzustellen, ob dieses Ausnahmeereignis eine erste Chance "oder" zweite Chance Ausnahme durch einen vorherigen Aufruf festgelegt wurde [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md). Wenn es festgelegt wurde, eine Ausnahme der ersten Chance, werden die `IDebugExceptionEvent2` Ereignis, das SDM gesendet wird. Wenn dies nicht der Fall ist, wird die DE der Anwendung bietet die Möglichkeit zur Behandlung von Ausnahmen. Wenn kein Ausnahmehandler bereitgestellt wird und die Ausnahme als eine zweite Chance-Ausnahme festgelegt wurde die `IDebugExceptionEvent2` Ereignis, das SDM gesendet wird. Andernfalls die DE setzt die Ausführung des Programms und des Betriebssystems oder der Common Language Runtime Ausnahmen behandelt.  
  
## <a name="see-also"></a>Siehe auch  
 [Wichtige Schnittstellen](../../../extensibility/debugger/reference/core-interfaces.md)   
 [SetException](../../../extensibility/debugger/reference/idebugengine2-setexception.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
