---
title: IDebugThread2::SetNextStatement | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugThread2::SetNextStatement
helpviewer_keywords:
- IDebugThread2::SetNextStatement
ms.assetid: 9e2834dd-4ecf-45af-8e6c-f9318ebdac06
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 755044ec1d713075c1c1fd3165254ba192943288
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58960274"
---
# <a name="idebugthread2setnextstatement"></a>IDebugThread2::SetNextStatement
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Legt den aktuellen Anweisungszeiger auf den angegebenen Code-Kontext fest.  
  
## <a name="syntax"></a>Syntax  
  
```cpp#  
HRESULT SetNextStatement (   
   IDebugStackFrame2*  pStackFrame,  
   IDebugCodeContext2* pCodeContext  
);  
```  
  
```csharp  
int SetNextStatement (   
   IDebugStackFrame2  pStackFrame,  
   IDebugCodeContext2 pCodeContext  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `pStackFrame`  
 Für die zukünftige Verwendung reserviert. Legen Sie auf einen null-Wert.  
  
 `pCodeContext`  
 [in] Ein [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) -Objekt, das beschreibt, der Code-Ort ausgeführt werden und der Kontext.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben. Die folgende Tabelle zeigt weitere mögliche Werte.  
  
|Wert|Beschreibung|  
|-----------|-----------------|  
|E_CANNOT_SET_NEXT_STATEMENT_ON_NONLEAF_FRAME|Die nächste Anweisung kann nicht in einem Stapelrahmen im Stapel Frame tiefer sein.|  
|E_CANNOT_SETIP_TO_DIFFERENT_FUNCTION|Die nächste Anweisung ist nicht für alle Rahmen im Stapel zugeordnet.|  
|E_CANNOT_SET_NEXT_STATEMENT_ON_EXCEPTION|Einige Debug-Engines können nicht auf die nächste Anweisung nach einer Ausnahme festgelegt.|  
  
## <a name="remarks"></a>Hinweise  
 Der Anweisungszeiger gibt an, der nächsten Anweisung oder Anweisung ausgeführt. Diese Methode wird eine Zeile des Quellcodes zu wiederholen, oder erzwingen z. B. in einer anderen Funktion Fortsetzen der Ausführung verwendet.  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)
