---
title: 'Vorgehensweise: Deaktivieren von Kompatibilitätswarnungen für Quellcodeverwaltungs-Plug-ins | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, turning off compatibility warnings
- compatibility warnings, turning off
ms.assetid: ba318e12-921b-4b7a-a8c2-12c712be1dbf
caps.latest.revision: 22
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 9efe961774ef1939cfc95c2efe9146a59e46bc17
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58959372"
---
# <a name="how-to-turn-off-compatibility-warnings-for-source-control-plug-ins"></a>Vorgehensweise: Deaktivieren von Kompatibilitätswarnungen für Quellcodeverwaltungs-Plug-ins
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Ein Benutzer möglicherweise mehrere kompatibilitätswarnungen angezeigt, wenn es sich bei Verwendung der quellcodeverwaltung in [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Die Warnungen dargestellt richten sich nach den Funktionen von das Quellcodeverwaltungs-Plug-in und können wie folgt deaktiviert werden.  
  
### <a name="to-disable-the-warning-to-ensure-optimal-source-control-integration-with-visual-studio"></a>Um die Warnung zu deaktivieren: "So stellen Sie sicher eine optimale Integration der quellcodeverwaltung mit Visual Studio..."  
  
-   Legen Sie den folgenden Registrierungseintrag (den Wert hinzufügen, falls erforderlich):  
  
     HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\DontDisplayCheckDotNETCompatible = dword:00000001  
  
     Diese Warnung wird angezeigt, für alle nicht-[!INCLUDE[vsvss](../includes/vsvss-md.md)] -Plug-ins.  
  
### <a name="to-disable-the-warning-the-installed-source-control-provider-does-not-support-all-the-capabilities"></a>Um die Warnung zu deaktivieren: "Die installierte quellcodeverwaltung unterstützt nicht alle Funktionen, die..."  
  
-   Legen Sie die folgenden zwei Werte (die Werte hinzufügen, falls erforderlich):  
  
     HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\WarnedOldMSSCCIProvider = dword:00000000  
  
     HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\UseOldSCC = dword:00000001  
  
     Diese Warnung wird angezeigt, wenn das Quellcodeverwaltungs-Plug-in explizit Eintrittsinvarianz für mehrere Projekte nicht unterstützt (d. h., wenn sie in nur ein Datei- und Projektinformationen zu einem Zeitpunkt überprüfen kann).  
  
     Es wird empfohlen, die Unterstützung von Eintrittsinvarianz (`SCC_CAP_REENTRANT` Funktion); Dies wird daher diese Warnung entfernen. Allerdings ist diese Unterstützung nicht möglich, können diese Registrierungseinträge festgelegt werden.  
  
## <a name="see-also"></a>Siehe auch  
 [Funktionsflags](../extensibility/capability-flags.md)
