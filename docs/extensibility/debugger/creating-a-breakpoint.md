---
title: Erstellen eines Haltepunkts | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- breakpoints, creating
- debugging [Debugging SDK], creating breakpoints
ms.assetid: 6f9f87bb-192e-45e0-9a7a-ffe729e87f7d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8a5c2769b4d2b194923ce0ba5ca5d6e644a8c5f0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56704760"
---
# <a name="create-a-breakpoint"></a>Erstellen eines Haltepunkts
Im folgenden wird beschrieben, den Prozess zum Erstellen eines Haltepunkts.

## <a name="methods-in-breakpoint-creation"></a>Methoden in Haltepunkt erstellen
 Wenn das Modul, das erforderlich ist, um einen Haltepunkt zu binden geladen wird, ruft die Sitzungs-Debug-Manager (SDM) die folgenden Methoden:

1.  [IDebugPendingBreakpoint2::Enable](../../extensibility/debugger/reference/idebugpendingbreakpoint2-enable.md)

2.  [IDebugPendingBreakpoint2::Virtualize](../../extensibility/debugger/reference/idebugpendingbreakpoint2-virtualize.md)

3.  [IDebugPendingBreakpoint2::CanBind](../../extensibility/debugger/reference/idebugpendingbreakpoint2-canbind.md)

    > [!NOTE]
    >  **CanBind** wird nur aufgerufen, wenn ein Benutzer einen Haltepunkt aus hergestellt hat die **Haltepunkte** Fenster.

4.  [IDebugPendingBreakpoint2::Bind](../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)

5.  [IDebugPendingBreakpoint2::EnumBoundBreakpoints](../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md)

## <a name="see-also"></a>Siehe auch
- [Aufrufen von debuggerereignissen](../../extensibility/debugger/calling-debugger-events.md)