---
title: 'Idiasourcefile:: Get_checksumtype | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSourceFile::get_checksumType method
ms.assetid: 4c363e61-a6a9-409a-9cc0-d06eb2bee645
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: f859bce63e2976b23ab613e249dad41b2bc63486
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58959531"
---
# <a name="idiasourcefilegetchecksumtype"></a>IDiaSourceFile::get_checksumType
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Ruft den Typ von Prüfsumme ab.  
  
## <a name="syntax"></a>Syntax  
  
```cpp#  
HRESULT get_checksumType (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pRetVal`  
 [out] Gibt die Prüfsumme-Typ zurück.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Der Checksum-Typ ist ein Wert, der eine Prüfsumme der Prüfsummenalgorithmus zugeordnet werden kann. Beispielsweise kann das Standardformat der PDB-Datei in der Regel einen der folgenden Werte aufweisen:  
  
|Typ von Prüfsumme an|CryptoAPI-Bezeichnung|Beschreibung|  
|-------------------|---------------------|-----------------|  
|0|\<none>|Keine Prüfsumme vorhanden ist.|  
|1|`CALG_MD5`|Prüfsumme, die mit dem MD5-Hash-Algorithmus generiert.|  
|2|`CALG_SHA1`|Prüfsumme, die mit dem SHA1-Hashalgorithmus generiert werden.|  
  
 Die `CryptoAPI` Bezeichnungen sind von der `ALG_ID` Enumeration. Weitere Informationen zu Hashalgorithmen, finden Sie in der `CryptoAPI` der Microsoft [!INCLUDE[winsdkshort](../../includes/winsdkshort-md.md)].  
  
 Rufen Sie zum Abrufen der tatsächlichen Prüfsumme Bytes für die Quelldatei der [idiasourcefile:: Get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md) Methode.  
  
## <a name="see-also"></a>Siehe auch  
 [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)   
 [IDiaSourceFile::get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md)
