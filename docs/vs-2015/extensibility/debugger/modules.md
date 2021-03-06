---
title: Module | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- modules
- debugging [Debugging SDK], modules
ms.assetid: c4cf2809-dbdb-4e75-9273-b3d3d77b67d0
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 802a40c248df243adf1319c522278ad94d69eeed
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58956618"
---
# <a name="modules"></a>Module
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Im Hinblick auf die Debugger-Architektur eine **Modul**:  
  
-   Ist ein physischer Container von Code, z.B. eine ausführbare Datei oder eine DLL-Datei.  
  
-   Laden die Symbole und selbst beschreiben können. Modulbeschreibungen werden im Fenster "Module" von der IDE angezeigt.  
  
-   Wird durch dargestellt eine [IDebugModule2](../../extensibility/debugger/reference/idebugmodule2.md) Schnittstelle, die von einer Debug-Engine, um das Modul beschreiben erstellt.  
  
## <a name="see-also"></a>Siehe auch  
 [Debuggerkonzepte](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugModule2](../../extensibility/debugger/reference/idebugmodule2.md)
