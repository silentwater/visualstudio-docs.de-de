---
title: IDiaSymbol::get_subType | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
ms.assetid: 0b3cbf77-8f11-434a-ad60-ea9829fec6fa
caps.latest.revision: 6
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 705bbb952436c9e87e16fe0a5901472b0bbb71be
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58958131"
---
# <a name="idiasymbolgetsubtype"></a>IDiaSymbol::get_subType
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Ruft den Untertyp ab.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT get_subType(   
   IDiaSymbol** pRetVal);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pRetVal`  
 [out] Ein Zeiger auf den untergeordneten Typ.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls gibt `S_FALSE` oder ein Fehlercode.  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
