---
title: IDiaSymbol::findSymbolsByRVAForAcceleratorPointerTag | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 024ccd78-5867-4ca7-bc26-548758e9ac53
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 673ca8137244fed933df0be3fa0221115951a9c1
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56618106"
---
# <a name="idiasymbolfindsymbolsbyrvaforacceleratorpointertag"></a>IDiaSymbol::findSymbolsByRVAForAcceleratorPointerTag
Wenn einen entsprechenden Tagwert, gibt diese Methode eine Enumeration von Symbolen, die enthalten sind, in dieser Stub-Funktion an eine angegebene relative virtuelle Adresse.

## <a name="syntax"></a>Syntax

```C++
HRESULT findSymbolsByRVAForAcceleratorPointerTag (
   DWORD             tagValue,
   DWORD             rva,
   IDiaEnumSymbols** ppResult);
```

#### <a name="parameters"></a>Parameter
 `tagValue`

[in] Der Wert des Zeigers-Tag, für den die symboldatensätze Pointee gefunden werden.

 `rva`

[in] Die Rva, die verwendet wird, um die Symbole zu filtern, die die Pointee-Variable mit dem angegebenen Tagwert entsprechen.

 `ppResult`

[out] Ein Zeiger auf ein `IDiaEnumSymbols` Schnittstellenzeiger, der mit dem Ergebnis initialisiert wurde.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt `S_FALSE` oder ein Fehlercode.

## <a name="remarks"></a>Anmerkungen
 Rufen Sie diese Methode nur auf eine `IDiaSymbol` Schnittstelle, die eine Accelerator-Stub-Funktion entspricht.

## <a name="see-also"></a>Siehe auch
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [IDiaEnumSymbols](../../debugger/debug-interface-access/idiaenumsymbols.md)