---
title: IActiveScriptStats::ResetStats | Microsoft-Dokumentation
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptStats.ResetStats
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptStats::ResetStats
ms.assetid: d98276fc-ad47-4e7b-aae4-254d63aece77
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fbd18719cde85b12e9ec5de3b19dbf8e81bd8575
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "58150971"
---
# <a name="iactivescriptstatsresetstats"></a>IActiveScriptStats::ResetStats
Setzt die Statistik für dieses Skript.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT ResetStats();  
```  
  
#### <a name="parameters"></a>Parameter  
 Diese Methode akzeptiert keine Parameter.  
  
## <a name="return-value"></a>Rückgabewert  
 Die Methode gibt ein `HRESULT` zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|`S_OK`|Die Methode war erfolgreich.|  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode wird die Statistik für dieses Skript zurückgesetzt.  
  
## <a name="see-also"></a>Siehe auch  
 [IActiveScriptStats-Schnittstelle](../../winscript/reference/iactivescriptstats-interface.md)