---
title: 'Idiastackframe:: Get_base | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackFrame::get_base method
ms.assetid: f27477d7-26fe-4c1c-a08a-c52cb20c8293
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f72c39e7cbfe9589d2fdf6ed8d1b8f25dee99936
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56626010"
---
# <a name="idiastackframegetbase"></a>IDiaStackFrame::get_base
Ruft die Basisadresse des Rahmens ab.

## <a name="syntax"></a>Syntax

```C++
HRESULT get_base ( 
   ULONGLONG* pRetVal
);
```

#### <a name="parameters"></a>Parameter
 `pRetVal`

[out] Gibt die Basisadresse zurück.

## <a name="return-value"></a>Rückgabewert
 Gibt bei Erfolg `S_OK` zurück. Gibt `S_FALSE` , wenn die Eigenschaft nicht unterstützt wird. Andernfalls wird ein Fehlercode zurückgegeben.

## <a name="see-also"></a>Siehe auch
- [IDiaStackFrame](../../debugger/debug-interface-access/idiastackframe.md)