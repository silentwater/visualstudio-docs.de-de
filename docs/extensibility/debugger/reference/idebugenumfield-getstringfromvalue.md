---
title: IDebugEnumField::GetStringFromValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEnumField::GetStringFromValue
helpviewer_keywords:
- IDebugEnumField::GetStringFromValue method
ms.assetid: 5f95fd0c-fdce-497f-9f54-2ad8749494e9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 98d7e976e0cd37ad1397666471c89da3d47d45d3
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56710369"
---
# <a name="idebugenumfieldgetstringfromvalue"></a>IDebugEnumField::GetStringFromValue
Diese Methode ruft den Namen der Enumerationskonstante erhält den Wert ab.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetStringFromValue(
   ULONGLONG value,
   BSTR*     pbstrValue
);
```

```csharp
int GetStringFromValue(
   ulong      value,
   out string pbstrValue
);
```

#### <a name="parameters"></a>Parameter
 `value`

 [in] Der Wert für das der Name der Enumeration Konstanten abgerufen werden soll.

 `pbstrValue`

 [out] Der Name der Enumerationskonstante zurückgegeben.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt `S_FALSE` , wenn der Wert keinen zugeordneten Namen hat, oder gibt einen Fehlercode zurück.

## <a name="remarks"></a>Hinweise
 Ist mehr als einen Namen, die den gleichen Wert zugeordnet, wird der Vorname in der Enumeration definierte zurückgegeben.

## <a name="see-also"></a>Siehe auch
- [IDebugEnumField](../../../extensibility/debugger/reference/idebugenumfield.md)