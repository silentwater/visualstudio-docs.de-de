---
title: 'Idiasymbol:: Get_isaggregated | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_isAggregated method
ms.assetid: 24d280ef-6ea3-4958-9418-4ad3ca7c67c1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0ac588314b69c6be8b31cc5719a4be8add3cad33
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56611034"
---
# <a name="idiasymbolgetisaggregated"></a>IDiaSymbol::get_isAggregated
Ruft ein Flag, das angibt, ob das Datensymbol Teil ein Aggregat oder eine Auflistung von Symbolen ist; vom Compiler aggregierte Symbole als separate Entitäten behandelt, aber sie gehören eigentlich ein einmaliges umfangreicheren Symbol.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_isAggregated(
   BOOL *pFlag
);
```

#### <a name="parameters"></a>Parameter
 `pFlag`

[out] Gibt `TRUE` , wenn die Daten eine Kombination aus Symbolen, die aus einer übergeordneten Symbol; Teilen gehört, andernfalls `FALSE`.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt `S_FALSE` oder ein Fehlercode.

> [!NOTE]
>  Der Rückgabewert `S_FALSE` bedeutet, dass die Eigenschaft ist nicht verfügbar für das Symbol.

## <a name="remarks"></a>Anmerkungen
 Die [idiasymbol:: Get_issplitted](../../debugger/debug-interface-access/idiasymbol-get-issplitted.md) Methode `TRUE` für das Symbol, das das übergeordnete Element der aggregierten Symbole ist.

## <a name="requirements"></a>Anforderungen

|Anforderung|Beschreibung|
|-----------------|-----------------|
|Header:|dia2.h|
|Version:|DIA-SDK 8.0|

## <a name="see-also"></a>Siehe auch
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [IDiaSymbol::get_isSplitted](../../debugger/debug-interface-access/idiasymbol-get-issplitted.md)