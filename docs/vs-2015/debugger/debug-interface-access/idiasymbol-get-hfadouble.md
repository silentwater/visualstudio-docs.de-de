---
title: 'Idiasymbol:: Get_hfadouble | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_hfaDouble method
ms.assetid: efc247b9-c16e-4fa3-89b0-901caf7b74c3
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 19fe7edf2d91364bbd21a8483c7c3557e36e81e3
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58957696"
---
# <a name="idiasymbolgethfadouble"></a>IDiaSymbol::get_hfaDouble
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Ruft ein Flag, das angibt, ob ein benutzerdefinierten Typ (UDT) homogene Gleitkomma (zu HFA) Aggregatdaten von Typ "double" enthält.  
  
## <a name="syntax"></a>Syntax  
  
```cpp#  
HRESULT get_hfaDouble(   
   BOOL* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pRetVal`  
 [out] Gibt `TRUE` enthält der UDT zu HFA Daten vom Typ double; andernfalls, zurückgegeben `FALSE`.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt `S_FALSE` oder ein Fehlercode.  
  
> [!NOTE]
>  Der Rückgabewert `S_FALSE` bedeutet, dass die Eigenschaft ist nicht verfügbar für das Symbol.  
  
## <a name="remarks"></a>Hinweise  
  
## <a name="requirements"></a>Anforderungen  
 Header: Dia2.h  
  
 Bibliothek: diaguids.lib  
  
 DLL: msdia100.dll  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [IDiaSymbol::get_udtKind](../../debugger/debug-interface-access/idiasymbol-get-udtkind.md)
