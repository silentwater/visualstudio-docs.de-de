---
title: IDebugPropertyEnumType_All::GetName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugPropertyEnumType_All.GetName
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugPropertyEnumType_All::GetName
ms.assetid: 24bbe4d5-4263-48d0-8e8d-bff957ffcad2
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 1c4f416e7cf525d28ad544c361168f55b964f353
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "58146642"
---
# <a name="idebugpropertyenumtypeallgetname"></a>IDebugPropertyEnumType_All::GetName
Gibt einen BSTR, das mit dem Namen des der `EnumType`.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
HRESULT GetName(  
   BSTR*  pname  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pname`  
 [out] Einem BSTR mit dem Namen des der `EnumType`.  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt einen gültigen `HRESULT`, in der Regel `S_OK`.  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugPropertyEnumType_All-Schnittstelle](../../winscript/reference/idebugpropertyenumtype-all-interface.md)