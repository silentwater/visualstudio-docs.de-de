---
title: IDebugProcess2::Terminate | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess2::Terminate
helpviewer_keywords:
- IDebugProcess2::Terminate
ms.assetid: 5e6bf373-0fe9-4321-b04a-473a65f664d9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 704f2b59852a47b02dcf5d6bdaa60e05ca722ca0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56703564"
---
# <a name="idebugprocess2terminate"></a>IDebugProcess2::Terminate
Beendet den Prozess.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Terminate( 
   void 
);
```

```csharp
int Terminate();
```

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise
 Wenn ein Prozess beendet wird, werden alle Programme, die während des Prozesses beendet. keine dürfen weiteren Code ausgeführt.

## <a name="see-also"></a>Siehe auch
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)