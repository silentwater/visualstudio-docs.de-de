---
title: 'Idiasymbol:: Get_framepointerpresent | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_framePointerPresent method
ms.assetid: d036090a-1651-454d-9130-b798f58ba053
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 41120826404df4cc94bd6e65fa574509f55c302e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56622266"
---
# <a name="idiasymbolgetframepointerpresent"></a>IDiaSymbol::get_framePointerPresent
Ruft ein Flag, das angibt, ob der Frame-Pointer vorhanden ist. Verwenden, wenn die [SymTagEnum-Enumeration](../../debugger/debug-interface-access/symtagenum.md) nastaven NA hodnotu `SymTagFunction`.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_framePointerPresent( 
   BOOL* pRetVal
);
```

#### <a name="parameters"></a>Parameter
 `pRetVal`

[out]] Gibt `TRUE` gibt zurück, wenn der Frame-Pointer vorhanden, andernfalls ist, `FALSE`.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt `S_FALSE` oder ein Fehlercode.

> [!NOTE]
>  Der Rückgabewert `S_FALSE` bedeutet, dass die Eigenschaft ist nicht verfügbar für das Symbol.

## <a name="remarks"></a>Anmerkungen

## <a name="requirements"></a>Anforderungen
 Header: Dia2.h

 Bibliothek: diaguids.lib

 DLL: msdia100.dll

## <a name="see-also"></a>Siehe auch
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)