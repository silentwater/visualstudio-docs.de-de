---
title: IDebugProperty3::CreateObjectID | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProperty3::CreateObjectID
helpviewer_keywords:
- IDebugProperty3::CreateObjectID
ms.assetid: f2fa81e7-822f-456e-8729-a96a18eea771
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ef7aa1ba25887fb306c72aa11751cd4bb97d65e7
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58957497"
---
# <a name="idebugproperty3createobjectid"></a>IDebugProperty3::CreateObjectID
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Erstellt eine eindeutige ID für diese Eigenschaft, um sicherzustellen, dass es für alle anderen Eigenschaften eindeutig ist.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HRESULT CreateObjectID(  
   void  
);  
```  
  
```csharp  
int CreateObjectID();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.  
  
## <a name="remarks"></a>Hinweise  
 Diese Methode wird aufgerufen, wenn die sitzungsbasierter Debug-Manager möchte, um sicherzustellen, dass diese Eigenschaft für alle anderen Eigenschaften eindeutig identifiziert wird. Die Debug-Engine (DE) unterstützt diese Methode auf, es sei denn, die Eigenschaften, die mit befasst sich bereits eindeutig identifiziert werden. Die DE diese Methode nicht unterstützt, gibt `E_NOTIMPL`.  
  
 Alle eindeutigen ID erstellt, mit `CreateObjectID` wird zerstört, wenn die [DestroyObjectID](../../../extensibility/debugger/reference/idebugproperty3-destroyobjectid.md) aufgerufen; dies auch signalisiert das Ende der die Notwendigkeit, die diese Eigenschaft eindeutig identifiziert.  
  
> [!NOTE]
>  Es gibt keine Methode diese eindeutige ID abrufen, damit die DE durchführen kann, was sie für die eindeutigen IDs möchte bei der `CreateObjectID` Methode wird aufgerufen.  
  
## <a name="see-also"></a>Siehe auch  
 [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)   
 [DestroyObjectID](../../../extensibility/debugger/reference/idebugproperty3-destroyobjectid.md)
