---
title: 'Fehler: Eine Sicherheitsprüfung ist fehlgeschlagen, weil der IIS-Verwaltungsdienst nicht reagiert hat | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.iis_not_responding
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
ms.assetid: 6060e94e-71dc-49f2-bb59-2584216eadbf
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 9434ad3d67b8cf724323bdb9614d3bfdbd569882
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58955934"
---
# <a name="error-a-security-check-failed-because-the-iis-admin-service-did-not-respond"></a>Fehler: Fehler bei einer Sicherheitsüberprüfung, weil der IIS-Verwaltungsdienst nicht reagiert hat
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Dieser Fehler tritt auf, wenn der IIS-Verwaltungsdienst nicht reagiert. Normalerweise weist dies auf ein Problem mit der IIS-Installation hin. Stellen Sie zunächst in der **Verwaltung** unter **Dienste** sicher, dass der Dienst ausgeführt wird.  
  
### <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Installieren Sie IIS mithilfe der Option **Software** in der Systemsteuerung neu.  
  
-   - oder -   
  
-   IIS in der Systemsteuerung mithilfe der Einstellungen „Software“ vom Computer entfernen. Wenn Sie IIS entfernt haben und die Probleme weiterhin auftreten, vergewissern Sie sich in der Registrierung, dass der folgende Schlüssel nicht mehr existiert:  
  
    ```  
    HKEY_CLASSES_ROOT\CLSID\{A9E69610-B80D-11D0-B9B9-00A0C922E750}  
    ```  
  
     - oder -   
  
-   Deaktivieren Sie den IIS-Verwaltungsdienst in der Systemsteuerung über die Option Verwaltung. Dadurch wird IIS auf dem Computer deaktiviert.  
  
     Sie müssen den Computer nach jedem dieser drei Schritte neu starten.  
  
     Weitere Informationen finden Sie in der IIS-Dokumentation.  
  
## <a name="see-also"></a>Siehe auch  
 [Debuggen von Webanwendungen: Fehler und Problembehandlung](../debugger/debugging-web-applications-errors-and-troubleshooting.md)
