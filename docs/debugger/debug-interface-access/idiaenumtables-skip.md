---
title: 'Idiaenumtables:: Skip | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumTables::Skip method
ms.assetid: 5c9db956-0654-4f1a-8775-530aa980d8ec
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 24232878452082dd1769c9bc9f1cd22d081968f2
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596554"
---
# <a name="idiaenumtablesskip"></a>IDiaEnumTables::Skip
Überspringt eine angegebene Anzahl von Tabellen in einer Enumerationsfolge.

## <a name="syntax"></a>Syntax

```C++
HRESULT Skip ( 
   ULONG celt
);
```

#### <a name="parameters"></a>Parameter
 `celt`

[in] Die Anzahl der Tabellen in der Enumerationsfolge übersprungen werden soll.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt `S_FALSE` , wenn es keine weitere Tabellen sind zu überspringen.

## <a name="see-also"></a>Siehe auch
- [IDiaEnumTables](../../debugger/debug-interface-access/idiaenumtables.md)