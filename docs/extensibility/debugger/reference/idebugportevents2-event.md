---
title: IDebugPortEvents2::Event | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortEvents2::Event
helpviewer_keywords:
- IDebugPortEvents2::Event
ms.assetid: 5cc813f7-04a1-4462-9ea7-fbddcf0e0143
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: da493c3d818cab1cb9a7e0ad82de3ca2fa9ef3ca
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56704474"
---
# <a name="idebugportevents2event"></a>IDebugPortEvents2::Event
Diese Methode sendet die Ereignisse, die die Erstellung und Zerstörung von Prozessen und Programme auf einem Port angeben.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Event(
   IDebugCoreServer2* pServer,
   IDebugPort2*       pPort,
   IDebugProcess2*    pProcess,
   IDebugProgram2*    pProgram,
   IDebugEvent2*      pEvent,
   REFIID             riidEvent
);
```

```csharp
int Event(
   IDebugCoreServer2 pServer,
   IDebugPort2       pPort,
   IDebugProcess2    pProcess,
   IDebugProgram2    pProgram,
   IDebugEvent2      pEvent,
   ref Guid          riidEvent
);
```

#### <a name="parameters"></a>Parameter
 `pMachine`

 [in] Ein [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md) Objekt, das der debugserver darstellt (es gibt ein für jede Instanz des [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)]) in der das Ereignis aufgetreten ist.

 `pPort`

 [in] Ein [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md) Objekt, das den Port darstellt, in dem das Ereignis aufgetreten ist.

 `pProcess`

 [in] Ein [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) -Objekt, das den Prozess darstellt, in dem das Ereignis aufgetreten ist.

 `pProgram`

 [in] Ein [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md) -Objekt, das Programm darstellt, in dem das Ereignis aufgetreten ist.

 `pEvent`

 [in] Ein [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) -Objekt, das das Ereignis identifiziert. Die möglichen Ereignisse sind wie folgt aus:

- [IDebugProcessCreateEvent2](../../../extensibility/debugger/reference/idebugprocesscreateevent2.md)

- [IDebugProcessDestroyEvent2](../../../extensibility/debugger/reference/idebugprocessdestroyevent2.md)

- [IDebugProgramCreateEvent2](../../../extensibility/debugger/reference/idebugprogramcreateevent2.md)

- [IDebugProgramDestroyEvent2](../../../extensibility/debugger/reference/idebugprogramdestroyevent2.md)

  `riidEvent` [in] Die GUID des Ereignisses. Da das Ereignis umgewandelt wird [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) vor dem Aufrufen dieser Methode diese Bezeichner macht es erheblich einfacher ermitteln, welches Ereignis gesendet wird.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.

## <a name="see-also"></a>Siehe auch
- [IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md)
- [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)