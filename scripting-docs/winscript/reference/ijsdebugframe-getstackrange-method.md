---
title: 'Ijsdebugframe:: GetStackRange-Methode | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugFrame.GetStackRange
apilocation:
- jscript9diag.dll
ms.assetid: a6d1d8be-efc0-442d-9756-1959c8f102bd
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 52dd6114d3ec462f91f8bce5e76f73c5487746ed
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "58147435"
---
# <a name="ijsdebugframegetstackrange-method"></a>IJsDebugFrame::GetStackRange-Methode
Gibt den Bereich der absoluten Adresse des logischen JavaScript-Stapelrahmens zurück.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT GetStackRange(  
   UINT64 *pStart,  
   UINT64 *pEnd  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pStart`  
 [out] Unterster Stapelzeiger des Frames.  
  
 `pEnd`  
 [out] Oberster Stapelzeiger des Frames.  
  
## <a name="return-value"></a>Rückgabewert  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode ist für die Zusammenführung überlappender Stapelüberwachungen nützlich, die aus mehreren Laufzeiten erfasst wird. Anfang können End Stapelzeiger mehrere Stapelrahmen für physische Computer (für interpretierte JavaScript-Laufzeitrahmen) umfassen. Start > end wie der Stapel von hohen zu niedrigen Adressen zunimmt.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** "jscript9diag.h"  
  
## <a name="see-also"></a>Siehe auch  
 [IJsDebugFrame-Schnittstelle](../../winscript/reference/ijsdebugframe-interface.md)