---
title: IDebugArrayObject2::GetBaseIndices | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- GetBaseIndices
- IDebugArrayObject2::GetBaseIndices
ms.assetid: 882951a2-3da0-49bf-8d1e-7daedd13ffe6
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 3c10fb65ec698bf9c5c9b7623b29e2f47851afe8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58957564"
---
# <a name="idebugarrayobject2getbaseindices"></a>IDebugArrayObject2::GetBaseIndices
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ruft den Basis-Indizes (untere Grenzen) für jeden Index in Anbetracht der Anzahl der Dimensionen im Array ab.  
  
## <a name="syntax"></a>Syntax  
  
```cpp#  
HRESULT GetBaseIndices (  
   DWORD  dwRank,  
   DWORD* dwIndices  
);  
```  
  
```csharp  
int GetBaseIndices (  
   uint       dwRank,  
   out uint[] dwIndices  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `dwRank`  
 [in] Die Anzahl der Dimensionen (Rang) des Arrays.  
  
 `dwIndices`  
 [out] Die Basis Indizes (untere Grenzen) für das Array.  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Beispielsweise würde diese Funktion '5' für das Array erstellt, mit dem folgenden C#-Code zurückgeben:  
  
```  
int[] lengths = { 12 };  
int[] lowerbounds = { 5 };  
Array.CreateInstance(typeof(int), lengths, lowerbounds);  
```  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugArrayObject2](../../../extensibility/debugger/reference/idebugarrayobject2.md)
