---
title: IDebugProcess2::CanDetach | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess2::CanDetach
helpviewer_keywords:
- IDebugProcess2::CanDetach
ms.assetid: 2830f7c3-69fb-474a-97b8-5b869e38d546
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ad1a127a390b27a08a89ac939d9dcce60e60a64e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56695777"
---
# <a name="idebugprocess2candetach"></a>IDebugProcess2::CanDetach
Bestimmt, ob die sitzungsbasierter Debug-Manager (SDM) den Prozess trennen kann.

## <a name="syntax"></a>Syntax

```cpp
HRESULT CanDetach(
   void
);
```

```csharp
int CanDetach();
```

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK.` gibt `S_FALSE` , wenn der Debugger eine Trennen vom Prozess nicht möglich. Andernfalls wird ein Fehlercode zurückgegeben.

## <a name="see-also"></a>Siehe auch
- [CanDetach](../../../extensibility/debugger/reference/idebugprogram2-candetach.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)