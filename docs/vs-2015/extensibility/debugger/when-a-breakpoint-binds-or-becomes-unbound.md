---
title: Wenn ein Haltepunkt gebunden bzw. Aufheben der Bindung | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], breakpoint unbound events
- breakpoint bound events
ms.assetid: 61bf00b2-8293-49d3-b919-1efb0dec9151
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 2f5c14ba620cee34d83e4be09b23a7e9fb28a0a5
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58959091"
---
# <a name="when-a-breakpoint-binds-or-becomes-unbound"></a>Binden bzw. Aufheben der Bindung eines Haltepunkts
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Wenn Sie ein Haltepunkt zur Zeit nicht gebunden werden kann, ein Aufruf, um ausgelöst wird, die [IDebugPendingBreakpoint2::CanBind](../../extensibility/debugger/reference/idebugpendingbreakpoint2-canbind.md) -Methode, die Bindung Zeit und die Erstellungszeit des Haltepunkts unterscheiden.  
  
## <a name="methods-called"></a>Methoden aufgerufen werden  
 Sitzungsbasierter Debug-Manager (SDM) Ruft die folgenden Methoden:  
  
1.  [IDebugEngine2::CreatePendingBreakpoint](../../extensibility/debugger/reference/idebugengine2-creatependingbreakpoint.md). Die DE-gibt ein [IDebugPendingBreakpoint2](../../extensibility/debugger/reference/idebugpendingbreakpoint2.md).  
  
2.  [IDebugPendingBreakpoint2::Enable](../../extensibility/debugger/reference/idebugpendingbreakpoint2-enable.md).  
  
3.  [IDebugPendingBreakpoint2::Virtualize](../../extensibility/debugger/reference/idebugpendingbreakpoint2-virtualize.md).  
  
4.  Die [IDebugPendingBreakpoint2::Bind](../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md) -Methode und gibt S_OK zurück. Der DE sendet eine [IDebugBreakpointBoundEvent2](../../extensibility/debugger/reference/idebugbreakpointboundevent2.md) oder [IDebugBreakpointErrorEvent2](../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md).  
  
5.  [IDebugBreakpointBoundEvent2::GetPendingBreakpoint](../../extensibility/debugger/reference/idebugbreakpointboundevent2-getpendingbreakpoint.md) und [IDebugBreakpointBoundEvent2::EnumBoundBreakpoints](../../extensibility/debugger/reference/idebugbreakpointboundevent2-enumboundbreakpoints.md) Methoden, um zu überprüfen und um die gebundene Haltepunkte abzurufen.  
  
## <a name="see-also"></a>Siehe auch  
 [Aufrufen von Debuggerereignissen](../../extensibility/debugger/calling-debugger-events.md)
