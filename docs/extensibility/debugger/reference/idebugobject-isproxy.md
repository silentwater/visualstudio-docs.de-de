---
title: IDebugObject::IsProxy | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugObject::IsProxy
- IsProxy
ms.assetid: 06c66b87-db95-4400-ab26-5d33e743a439
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 037245524446ded2ec250f1d4a04e21bf5924a61
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678422"
---
# <a name="idebugobjectisproxy"></a>IDebugObject::IsProxy
Bestimmt, ob das Objekt über einen transparenten Proxy ist.

## <a name="syntax"></a>Syntax

```cpp
HRESULT IsProxy (
   BOOL* pfIsProxy
);
```

```csharp
int IsProxy (
   out bool pfIsProxy
);
```

#### <a name="parameters"></a>Parameter
 `pfIsProxy`

 [out] `TRUE` ist das Objekt einen transparenten Proxy ist; andernfalls `FALSE`.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise
 Diese Methode wird von der standardmäßigen C++-Debug-Engine implementiert.

## <a name="see-also"></a>Siehe auch
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)