---
title: IDebugCanStopEvent2::CanStop | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCanStopEvent2::CanStop
helpviewer_keywords:
- IDebugCanStopEvent2::CanStop
ms.assetid: 7d61adbe-6b3d-41f3-86a1-45d9cc01a7f8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 307b6d25f2e45276ead7c4b360ae191a01059104
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56716557"
---
# <a name="idebugcanstopevent2canstop"></a>IDebugCanStopEvent2::CanStop
Benachrichtigt der Debug-Engine (DE), ob an der aktuellen Codeposition zu beenden oder Fortsetzen der Ausführung.

## <a name="syntax"></a>Syntax

```cpp
HRESULT CanStop ( 
   BOOL fCanStop
);
```

```csharp
int CanStop ( 
   int fCanStop
);
```

#### <a name="parameters"></a>Parameter
 `fCanStop`

 [in] Ungleich 0 (`TRUE`), wenn die DE werden, an der aktuellen Position des Codes beendet soll; andernfalls NULL (`FALSE`).

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise
 Ruft der Empfänger der dieses Ereignis in der Regel die [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md) Methode, um die Ursache zu ermitteln, die DE beenden möchte, und ruft dann die `IDebugCanStopEvent2::CanStop` Methode mit der entsprechenden Antwort.

 Wenn die DE beendet wird, sendet er ein Ereignis, das den Grund für Beenden beschreibt. In der Regel werden zwei Ereignisse, die einen Benutzer oder ein Signal Umbruch, der durch dargestellt wird gesendet, werden die [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md) -Schnittstelle, und ein Haltepunktereignis, dargestellt durch die [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md) Schnittstelle.

## <a name="see-also"></a>Siehe auch
- [IDebugCanStopEvent2](../../../extensibility/debugger/reference/idebugcanstopevent2.md)
- [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md)
- [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md)
- [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)