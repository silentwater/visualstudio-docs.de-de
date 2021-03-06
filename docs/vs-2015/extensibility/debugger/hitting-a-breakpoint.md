---
title: Erreichen eines Haltepunkts | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], hitting breakpoints
- breakpoints, hitting
ms.assetid: a77816e3-b15b-46a0-90cd-be7242e4d6c9
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 5ae077b8ccb4ce41f94fbc5e11bfff1f16c826c0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58957689"
---
# <a name="hitting-a-breakpoint"></a>Erreichen eines Haltepunkts
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Im folgenden wird den Prozess, wenn die Debug-Engine (DE) einen Haltepunkt erreicht, bei der Ausführung oder schrittweise beschrieben:  
  
## <a name="troubleshooting-a-hit-breakpoint"></a>Problembehandlung für einen Haltepunkt drücken  
  
1.  Der DE sendet eine [IDebugBreakpointEvent2](../../extensibility/debugger/reference/idebugbreakpointevent2.md) Schnittstelle als eine **EVENT_SYNC_STOP**.  
  
2.  Ruft die Sitzungs-Debug-Manager (SDM) [IDebugBreakpointEvent2:::EnumBreakpoints](../../extensibility/debugger/reference/idebugbreakpointevent2-enumbreakpoints.md) um den Haltepunkt zu erhalten, das ermittelt wurde.  
  
## <a name="see-also"></a>Siehe auch  
 [Aufrufen von Debuggerereignissen](../../extensibility/debugger/calling-debugger-events.md)
