---
title: IDebugArrayObject2 | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugArrayObject2 interface
ms.assetid: be6e504d-4ab3-4141-a61b-0953ee0e038e
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7de86c1560f511f684daa7f6029a54865460c62e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58956627"
---
# <a name="idebugarrayobject2"></a>IDebugArrayObject2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

> [!IMPORTANT]
>  In Visual Studio 2015 ist diese Art der Implementierung von ausdrucksauswertungen veraltet. Informationen zu CLR-ausdrucksauswertungen implementieren, finden Sie unter [CLR Ausdrucksauswertungen](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) und [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Stellt ein verwaltetes Array-Objekt dar und ermöglicht eine ausdrucksauswertung (EE), um zu bestimmen, den Basisindex (untere Grenzen) für das Array.  
  
## <a name="syntax"></a>Syntax  
  
```  
IDebugArrayObject2 : IDebugArrayObject  
```  
  
## <a name="notes-for-implementers"></a>Hinweise für Implementierer  
 Dies wird von der verwalteten Debug-Engine (DE) implementiert.  
  
## <a name="methods"></a>Methoden  
 Zusätzlich zu den Methoden für die [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md) Schnittstelle, die diese Schnittstelle implementiert die folgenden Methoden:  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[GetBaseIndices](../../../extensibility/debugger/reference/idebugarrayobject2-getbaseindices.md)|Ruft den Basis-Indizes (untere Grenzen) für jeden Index in Anbetracht der Anzahl der Dimensionen im Array ab.|  
|[HasBaseIndices](../../../extensibility/debugger/reference/idebugarrayobject2-hasbaseindices.md)|Bestimmt, ob das Array Basis Indizes (untere Grenzen) definiert hat.|  
  
## <a name="remarks"></a>Hinweise  
 Eine ausdrucksauswertung verwendet diese Schnittstelle zum Darstellen von verwalteten Arrays in eine Analysestruktur.  
  
## <a name="requirements"></a>Anforderungen  
 Header: EE.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll
