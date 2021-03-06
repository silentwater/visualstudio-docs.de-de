---
title: Auswählen einer Strategie für die ClickOnce-Bereitstellung | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, strategies
- deploying applications, ClickOnce
ms.assetid: 98bcab65-ab8b-4ed1-9adc-fdacf92b8106
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 619d70b79d75cc45add0d541cd081d9ac0f258d5
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58957980"
---
# <a name="choosing-a-clickonce-deployment-strategy"></a>Auswählen einer Strategie für die ClickOnce-Bereitstellung
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Es gibt drei verschiedene Strategien zum Bereitstellen einer [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)]-Anwendung. Es hängt primär von der Art der bereitzustellenden Anwendung ab, welche Strategie Sie auswählen. Folgende Strategien sind verfügbar:  
  
-   Installation aus dem Web oder einer Netzwerkfreigabe  
  
-   Installation von einer CD  
  
-   Starten der Anwendung aus dem Web oder einer Netzwerkfreigabe  
  
    > [!NOTE]
    >  Neben einer Bereitstellungsstrategie empfiehlt es sich außerdem, eine Strategie zum Bereitstellen von Anwendungsupdates auszuwählen. Weitere Informationen finden Sie unter [Auswählen einer Strategie der ClickOnce-Aktualisierung](../deployment/choosing-a-clickonce-update-strategy.md).  
  
## <a name="install-from-the-web-or-a-network-share"></a>Installation aus dem Web oder einer Netzwerkfreigabe  
 Bei dieser Strategie wird die Anwendung auf einem Webserver oder in einer Dateifreigabe im Netzwerk bereitgestellt. Benutzer installieren die Anwendung, indem sie auf ein Symbol auf einer Webseite klicken oder auf ein Symbol in der Dateifreigabe doppelklicken. Die Anwendung wird dann auf den Computer des Endbenutzers heruntergeladen, installiert und gestartet. Dem Menü **Start** und unter **Software** in der **Systemsteuerung** werden Elemente hinzugefügt.  
  
 Da diese Strategie von einer Netzwerkverbindung abhängt, funktioniert sie am besten bei Anwendungen, die für Benutzer bereitgestellt werden, die Zugriff auf ein lokales Netzwerk haben oder eine Internetverbindung mit hoher Geschwindigkeit besitzen.  
  
 Wenn Sie die Anwendung aus dem Web bereitstellen, können Sie Argumente in die Anwendung übergeben, wenn sie mit einer URL aktiviert wird. Weitere Informationen finden Sie unter [Vorgehensweise: Abrufen von Abfragezeichenfolgen-Informationen in einer Online-ClickOnce-Anwendung](../deployment/how-to-retrieve-query-string-information-in-an-online-clickonce-application.md). Sie können keine Argumente in eine Anwendung übergeben, die mit einer der anderen in diesem Dokument beschriebenen Methoden aktiviert wird.  
  
 Um diese Bereitstellungsstrategie in [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] zu aktivieren, klicken Sie auf der Seite **Installationsart** des Webpublishing-Assistenten auf **Aus dem Web** oder **Von UNC-Pfad oder Dateifreigabe**.  
  
 Dies ist die Standardbereitstellungsstrategie.  
  
## <a name="install-from-a-cd"></a>Installation von einer CD  
 Bei dieser Strategie wird die Anwendung auf einem Wechseldatenträger bereitgestellt, z. B. auf einer CD-ROM oder einer DVD. Wenn ein Benutzer die Anwendung installiert, wird sie wie bei der vorausgegangenen Option installiert und gestartet und dem Menü **Start** sowie unter **Software** in der **Systemsteuerung** werden Elemente hinzugefügt.  
  
 Diese Strategie funktioniert am besten bei Anwendungen, die für Benutzer bereitgestellt werden, die nicht dauerhaft über eine Netzwerkverbindung oder über eine Verbindung mit niedriger Bandbreite verfügen. Da die Anwendung von einem Wechseldatenträger installiert wird, ist bei der Installation keine Netzwerkverbindung erforderlich. Sie benötigen jedoch eine Netzwerkverbindung für Anwendungsupdates.  
  
 Um diese Bereitstellungsstrategie in [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] zu aktivieren, klicken Sie auf der Seite **Installationsart** des Webpublishing-Assistenten auf **Von CD-ROM oder DVD-ROM**.  
  
 Um diese Bereitstellungsstrategie manuell zu aktivieren, ändern Sie das **deploymentProvider**-Tag im Bereitstellungsmanifest. (In Visual Studio wird diese Eigenschaft als **Installations-URL** auf der Seite **Veröffentlichen** des Projekt-Designers verfügbar gemacht. In Mage.exe lautet **Startposition**.)  
  
## <a name="start-the-application-from-the-web-or-a-network-share"></a>Starten der Anwendung aus dem Web oder einer Netzwerkfreigabe  
 Diese Strategie ähnelt der ersten Strategie. Die Anwendung verhält sich jedoch wie eine Webanwendung. Wenn der Benutzer auf einer Webseite auf einen Link klickt (oder in einer Dateifreigabe auf ein Symbol doppelklickt), wird die Anwendung gestartet. Beim Beenden der Anwendung ist diese auf dem lokalen Computer nicht mehr verfügbar. Dem Menü **Start** und unter **Software** in der **Systemsteuerung** wird nichts hinzugefügt.  
  
> [!NOTE]
>  Technisch gesehen wird die Anwendung in einen Anwendungscache auf dem lokalen Computer heruntergeladen und dort installiert, genauso wie eine Webanwendung in den Webcache heruntergeladen wird. Wie beim Webcache werden die Dateien letztendlich aus dem Anwendungscache gelöscht. Der Benutzer empfindet es jedoch so, als ob die Anwendung aus dem Web oder der Dateifreigabe ausgeführt wird.  
  
 Diese Strategie funktioniert am besten bei Anwendungen, die selten verwendet werden, z. B. ein Tool zum Berechnen von Lohnzusatzleistungen für Angestellte, das i. d. R. nur einmal im Jahr ausgeführt wird.  
  
 Um diese Bereitstellungsstrategie in [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] zu aktivieren, klicken Sie auf der Seite **Vom Web installieren oder ausführen** des Webpublishing-Assistenten auf **Anwendung nicht installieren**.  
  
 Um diese Bereitstellungsstrategie manuell zu aktivieren, ändern Sie das **install**-Tag im Bereitstellungsmanifest. (Sein Wert kann **true** oder **false** sein. Verwenden Sie in Mage.exe die **nur Online** option die **Anwendungstyp** Liste.)  
  
## <a name="web-browser-support"></a>Unterstützung für Internetbrowser  
 Anwendungen, die auf .NET Framework 3.5 ausgerichtet sind, können mit jedem Browser installiert werden.  
  
 Anwendungen, die auf .NET Framework 2.0 ausgerichtet sind, erfordern Internet Explorer.  
  
## <a name="see-also"></a>Siehe auch  
 [ClickOnce-Sicherheit und -Bereitstellung](../deployment/clickonce-security-and-deployment.md)   
 [Auswählen einer Strategie für die ClickOnce-Aktualisierung](../deployment/choosing-a-clickonce-update-strategy.md)   
 [Vorgehensweise: Veröffentlichen einer ClickOnce-Anwendung, die mit dem Webpublishing-Assistenten](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)   
 [Sichern von ClickOnce-Anwendungen](../deployment/securing-clickonce-applications.md)
