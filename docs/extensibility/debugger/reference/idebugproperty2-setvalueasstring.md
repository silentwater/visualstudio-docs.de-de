---
title: IDebugProperty2::SetValueAsString | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProperty2::SetValueAsString
helpviewer_keywords:
- IDebugProperty2::SetValueAsString
ms.assetid: 9e6a5054-41b7-4223-b509-b93689d366a5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6acc3c0c0ec271793832783b2fb7eb9f2ff2309a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56686482"
---
# <a name="idebugproperty2setvalueasstring"></a>IDebugProperty2::SetValueAsString
Legt den Wert einer Eigenschaft aus einer angegebenen Zeichenfolge fest.

## <a name="syntax"></a>Syntax

```cpp
HRESULT SetValueAsString ( 
   LPCOLESTR pszValue,
   UINT      nRadix,
   DWORD     dwTimeout
);
```

```csharp
int SetValueAsString ( 
   string pszValue,
   uint   nRadix,
   uint   dwTimeout
);
```

#### <a name="parameters"></a>Parameter
 `pszValue`

 [in] Eine Zeichenfolge, die mit dem Wert, der festgelegt werden.

 `nRadix`

 [in] Eine Basis zur Interpretation numerische Informationen verwendet werden soll. Dies kann 0, um zu versuchen, die die Basis wird er automatisch bestimmt sein.

 `dwTimeout`

 [in] Gibt die maximale Zeit in Millisekunden, warten Sie vor der Rückgabe dieser Methode an. Verwendung `INFINITE` für Warten ohne Timeout.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`; gibt andernfalls den Fehlercode zurück. Die folgende Tabelle zeigt weitere mögliche Werte.

|Wert|Beschreibung|
|-----------|-----------------|
|`E_SETVALUE_VALUE_CANNOT_BE_SET`|Die Zeichenfolge konnte nicht in einem Eigenschaftswert konvertiert werden, oder den Wert der Eigenschaft konnte nicht festgelegt werden.|
|`E_SETVALUE_VALUE_IS_READONLY`|Die Eigenschaft ist schreibgeschützt.|

## <a name="see-also"></a>Siehe auch
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)