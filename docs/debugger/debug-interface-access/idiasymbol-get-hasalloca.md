---
title: 'Idiasymbol:: Get_hasalloca | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_hasAlloca method
ms.assetid: 3b9fb747-670b-4da7-bb70-612f7b911786
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f86eb2c4e0d95d3fbb9c24ee8596193b31223b11
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56698390"
---
# <a name="idiasymbolgethasalloca"></a>IDiaSymbol::get_hasAlloca
Ruft ein Flag, das angibt, ob die Funktion einen Aufruf von enthält `alloca` (dient zum Zuordnen von Speicher auf dem Stapel).

## <a name="syntax"></a>Syntax

```cpp
HRESULT get_hasAlloca(   BOOL *pFlag);
```

#### <a name="parameters"></a>Parameter
 `pFlag`

[out] Gibt `TRUE` , wenn die Funktion einen Aufruf enthält `alloca`ist, andernfalls gibt `FALSE`.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt `S_FALSE` oder ein Fehlercode.

> [!NOTE]
>  Der Rückgabewert `S_FALSE` bedeutet, dass die Eigenschaft nicht für das Symbol verfügbar ist.

## <a name="requirements"></a>Anforderungen

|Anforderung|Beschreibung|
|-----------------|-----------------|
|Header:|dia2.h|
|Version:|DIA-SDK 8.0|

## <a name="see-also"></a>Siehe auch
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)