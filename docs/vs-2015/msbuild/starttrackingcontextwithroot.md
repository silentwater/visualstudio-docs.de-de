---
title: StartTrackingContextWithRoot | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
api_name:
- StartTrackingContextWithRoot
api_location:
- filetracker.dll
api_type:
- COM
helpviewer_keywords:
- StartTrackingContextWithRoot
ms.assetid: f6ef2b76-8035-4a14-8195-aa221c46ef48
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: e35384af02ad2fb5f3c15d1851cdc716bc29445b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54787171"
---
# <a name="starttrackingcontextwithroot"></a>StartTrackingContextWithRoot
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Startet einen Nachverfolgungskontext mithilfe einer Antwortdatei, die einen Stammmarker angibt.  
  
## <a name="syntax"></a>Syntax  
  
```  
HRESULT WINAPI StartTrackingContextWithRoot(LPCTSTR intermediateDirectory, LPCTSTR taskName, LPCTSTR rootMarkerResponseFile);  
```  
  
#### <a name="parameters"></a>Parameter  
 [in] `intermediateDirectory`  
 Das Verzeichnis, in dem das Nachverfolgungsprotokoll gespeichert werden soll  
  
 [in] `taskName`  
 Identifiziert den Nachverfolgungskontext. Dieser Name wird verwendet, um den Protokolldateinamen zu erstellen.  
  
 [in] `rootMarkerResponseFile`  
 Der Pfadname einer Antwortdatei mit einem Stammmarker. Der Stammname wird verwendet, um alle Nachverfolgungen für einen Kontext zusammen zu gruppieren.  
  
## <a name="return-value"></a>Rückgabewert  
 Ein [HRESULT](<!-- TODO: review code entity reference <xref:assetId:///HRESULT?qualifyHint=False&amp;autoUpgrade=True>  -->), bei dem [SUCCEEDED](<!-- TODO: review code entity reference <xref:assetId:///SUCCEEDED?qualifyHint=False&amp;autoUpgrade=True>  -->) festgelegt ist, wenn der Nachverfolgungskontext erstellt wurde.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** FileTracker.h  
  
## <a name="see-also"></a>Siehe auch  
 [StartTrackingContext](../msbuild/starttrackingcontext.md)
