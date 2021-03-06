---
title: Einstellungen für Webprojekte von Eigenschaftenseiten | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugging [Visual Studio], Web applications
- project settings [Visual Studio], debug configurations
- debug builds, project settings
- projects [Visual Studio], debug configurations
- debugging Web applications, project settings
- debug configurations, Web projects
ms.assetid: 8ec5160a-6408-4f47-8d41-f0e20e79a3b9
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3cb7cd3f8c3678d37feb2267f68ab5d2b3d970e0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58957836"
---
# <a name="property-pages-settings-for-web-projects"></a>Einstellungen von Eigenschaftenseiten für Webprojekte
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sie können die Eigenschafteneinstellungen für eine Website-Debugkonfiguration im Dialogfeld **Eigenschaftenseiten** ändern. Eine genaue Anweisung finden Sie unter [Debug- und Releasekonfigurationen](../debugger/how-to-set-debug-and-release-configurations.md). Anhand der folgenden Tabellen erfahren Sie, wo die debuggerspezifischen Einstellungen im Dialogfeld **Eigenschaftenseiten** zu finden sind.  
  
### <a name="configuration-properties-folder-start-options-category"></a>Ordner "Konfigurationseigenschaften" (Kategorie "Startoptionen")  
  
|**Einstellung**|**Beschreibung**|  
|-----------------|---------------------|  
|**Startaktion**|Überschrift, unter der sich Optionen für den Anwendungsstart befinden.|  
|**Aktuelle Seite verwenden**|Legt die aktuelle Seite als Ausgangspunkt für das Debuggen fest.|  
|**Bestimmte Seite:**|Gibt die Webseite an, bei der das Debuggen beginnen soll.|  
|**Externes Programm starten:**|Gibt den Startbefehl für das Programm an, das gedebuggt werden soll.|  
|**Befehlszeilenargumente:**|Gibt Argumente für den oben aufgeführten Befehl an.|  
|**Arbeitsverzeichnis:**|Gibt das Arbeitsverzeichnis des Programms an, das gerade gedebuggt wird. Das Arbeitsverzeichnis in [!INCLUDE[csprcs](../includes/csprcs-md.md)] ist das Verzeichnis, über das die Anwendung gestartet wird: standardmäßig \bin\debug.|  
|**Start-URL**|Gibt den Pfad der Webanwendung an, die gedebuggt werden soll.|  
|**Keine Seite öffnen, sondern auf eine Anforderung einer externen Anwendung warten**|Legt fest, dass auf die Anforderung einer externen Anwendung gewartet wird. Mit dieser Option wird weder Internet Explorer noch eine andere Anwendung gestartet. Sie wird lediglich zum Debuggen vorbereitet, wenn sie von einer Anwendung aufgerufen wird.|  
|**Server**|Überschrift, unter der sich Optionen zum zu verwendenden Server befinden.|  
|**Standardwebserver verwenden**|Legt fest, dass der Standardwebserver verwendet wird.|  
|**Benutzerdefinierten Server verwenden**|Ermöglicht es Ihnen, die Basis-URL einzugeben, die als Server verwendet werden soll.|  
|**Debugger**|Überschrift, unter der sich Optionen zum Debugtyp befinden.|  
|**ASP.NET-Debuggen**|Ermöglicht das Debuggen von Serverseiten, die für die [!INCLUDE[vstecasp](../includes/vstecasp-md.md)]-Entwicklungsplattform geschrieben wurden. Sie müssen unter **Start-URL** eine URL angeben.|  
|**Debuggen von nativem Code**|Bietet die Möglichkeit, Aufrufe von systemeigenem (nicht verwaltetem) Win32-Code von einer verwalteten Anwendung aus zu debuggen.|  
|**SQL Server debuggen**|Ermöglicht das Debuggen von SQL Server-Datenbankobjekten.|  
|**Silverlight-Debuggen**|Ermöglicht das Debuggen von Silverlight-Komponenten.|  
  
## <a name="see-also"></a>Siehe auch  
 [Debuggereinstellungen und -vorbereitung](../debugger/debugger-settings-and-preparation.md)
