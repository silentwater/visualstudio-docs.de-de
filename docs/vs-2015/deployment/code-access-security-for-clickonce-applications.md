---
title: Codezugriffssicherheit für ClickOnce-Anwendungen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-deployment
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vb.XBAPProjectPropertiesSecurity.HowTo
- vb.XBAProjectPropertiesSecurity.HowTo
- vb.ProjectPropertiesSecurity.HowTo
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- deploying applications [ClickOnce], security
- ClickOnce applications, caspol
- security [ClickOnce], WPF browser-hosted applications
- security [ClickOnce], ClickOnce applications
- ClickOnce applications, code access security policies
- security, ClickOnce
ms.assetid: 04b104d0-0bd3-4ccb-b164-1de92d234487
caps.latest.revision: 33
author: mikejo5000
ms.author: mikejo
manager: wpickett
ms.openlocfilehash: 71b9344e552cb03d65b0093b1d5e0707689ec6af
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2018
ms.locfileid: "47510403"
---
# <a name="code-access-security-for-clickonce-applications"></a>Codezugriffssicherheit für ClickOnce-Anwendungen
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Die neueste Version dieses Themas finden Sie unter [Codezugriffssicherheit für ClickOnce-Anwendungen](https://docs.microsoft.com/visualstudio/deployment/code-access-security-for-clickonce-applications).  
  
ClickOnce-Anwendungen basieren auf .NET Framework und unterliegen Codezugriffssicherheits-Einschränkungen. Daher ist es wichtig, dass Sie sich mit dem Thema Codezugriffssicherheit auseinandersetzen und diese Kenntnisse beim Schreiben von ClickOnce-Anwendungen anwenden.  
  
 Mithilfe der Codezugriffssicherheit in .NET Framework wird der Zugriff von Code auf geschützte Ressourcen und Operationen beschränkt. Sie sollten die Codezugriffsberechtigungen für Ihre ClickOnce-Anwendung so konfigurieren, dass die Zone verwendet wird, die für den Speicherort des Installationsprogramms der Anwendung geeignet ist. In den meisten Fällen können Sie die Zone **Internet** für einen begrenzten Satz von Berechtigungen oder die Zone **Lokales Intranet** für einen umfangreicheren Satz von Berechtigungen verwenden.  
  
## <a name="default-clickonce-code-access-security"></a>Standardmäßige ClickOnce-Codezugriffssicherheit  
 Standardmäßig erhält eine ClickOnce-Anwendung "Voll vertrauenswürdig"-Berechtigungen, wenn sie auf einem Clientcomputer installiert oder ausgeführt wird.  
  
-   Eine Anwendung, die "Voll vertrauenswürdig"-Berechtigungen hat, hat uneingeschränkten Zugriff auf Ressourcen wie das Dateisystem und die Registrierung. Dadurch kann es passieren, dass Ihre Anwendung (und das System des Endbenutzers) durch bösartigen Code ausgenutzt wird.  
  
-   Wenn eine Anwendung "Voll vertrauenswürdig"-Berechtigungen erfordert, wird ein Endbenutzer möglicherweise aufgefordert, Berechtigungen für die Anwendung zu gewähren. Dies bedeutet, dass die Anwendung keine wirkliche ClickOnce-Bedienung bereitstellt, und die Eingabeaufforderung kann für weniger erfahrene Benutzer verwirrend sein.  
  
    > [!NOTE]
    >  Wird eine Anwendung von Wechselmedien wie z. B. einer CD-ROM installiert, wird der Benutzer nicht zu einer Eingabe aufgefordert. Darüber hinaus kann ein Netzwerkadministrator Netzwerkrichtlinien so konfigurieren, dass Benutzer nicht zu einer Eingabe aufgefordert werden, wenn sie eine Anwendung aus einer vertrauenswürdigen Quelle installieren. Weitere Informationen finden Sie unter [Trusted Application Deployment Overview](../deployment/trusted-application-deployment-overview.md).  
  
 Um die Berechtigungen für eine ClickOnce-Anwendung einzuschränken, können Sie die Codezugriffsberechtigungen für Ihre Anwendung so ändern, dass sie die Zone anfordert, die am besten für die Berechtigungen geeignet ist, die Ihre Anwendung erfordert. In den meisten Fällen können Sie die Zone auswählen, aus der die Anwendung bereitgestellt wird. Ist Ihre Anwendung beispielsweise eine Unternehmensanwendung, können Sie die Zone **Lokales Intranet** verwenden. Ist Ihre Anwendung eine Internetanwendung, können Sie die Zone **Internet** verwenden.  
  
## <a name="configuring-security-permissions"></a>Konfigurieren von Sicherheitsberechtigungen  
 Sie sollten Ihre ClickOnce-Anwendung immer so konfigurieren, dass sie die entsprechende Zone anfordert, um die Codezugriffsberechtigungen zu beschränken. Sie können Sicherheitsberechtigungen im **Projekt-Designer** auf der Seite **Sicherheit**konfigurieren.  
  
 Die Seite **Sicherheit** im **Projekt-Designer** enthält das Kontrollkästchen **ClickOnce-Sicherheitseinstellungen aktivieren** . Wenn dieses Kontrollkästchen aktiviert ist, werden die Berechtigungsanforderungen für die Sicherheit dem Bereitstellungsmanifest der Anwendung hinzugefügt. Während der Installation wird der Benutzer aufgefordert, Berechtigungen zu erteilen, wenn die angeforderten Berechtigungen über die Standardberechtigungen für die Zone hinausgehen, aus der die Anwendung bereitgestellt wird. Weitere Informationen finden Sie unter [How to: Enable ClickOnce Security Settings](../deployment/how-to-enable-clickonce-security-settings.md).  
  
 Anwendungen, die aus anderen Speicherorten bereitgestellt werden, werden ohne Eingabeaufforderung andere Berechtigungsstufen erteilt. Wird eine Anwendung beispielsweise aus dem Internet bereitgestellt, erhält sie einen sehr eingeschränkten Satz von Berechtigungen. Wird die Anwendung aus einem lokalen Intranet installiert, erhält sie mehr Berechtigungen, und wenn sie von einer CD-ROM installiert wird, erhält sie Berechtigungen für volle Vertrauenswürdigkeit.  
  
 Als Ausgangspunkt für ein Konfigurieren von Berechtigungen können Sie auf der Seite **Sicherheit** eine Sicherheitszone in der Liste **Zone** auswählen. Wird Ihre Anwendung möglicherweise aus mehreren Zonen bereitgestellt, wählen Sie die Zone mit den wenigsten Berechtigungen. Weitere Informationen finden Sie unter [Gewusst wie: Festlegen einer Sicherheitszone für eine ClickOnce-Anwendung](../deployment/how-to-set-a-security-zone-for-a-clickonce-application.md).  
  
 Die Eigenschaften, die festgelegt werden können, variieren je nach Berechtigungssatz (nicht alle Berechtigungssätze haben konfigurierbare Eigenschaften). Weitere Informationen zur vollständigen Liste der Berechtigungen, die Ihre Anwendung anfordern kann, finden Sie unter <xref:System.Security.Permissions>. Weitere Informationen über das Festlegen von Berechtigungen für eine benutzerdefinierte Zone finden Sie unter [Gewusst wie: Festlegen benutzerdefinierter Berechtigungen für eine ClickOnce-Anwendung](../deployment/how-to-set-custom-permissions-for-a-clickonce-application.md).  
  
## <a name="debugging-an-application-that-has-restricted-permissions"></a>Debuggen einer Anwendung, die eingeschränkte Berechtigungen hat  
 Als Entwickler führen Sie Ihren Entwicklungscomputer höchstwahrscheinlich mit "Voll vertrauenswürdig"-Berechtigungen aus. Aus diesem Grund sehen Sie beim Debuggen der Anwendung nicht die Sicherheitsausnahmen, die Benutzern angezeigt werden können, wenn diese die Anwendung mit eingeschränkten Berechtigungen ausführen.  
  
 Um diese Ausnahmen zu erfassen, müssen Sie die Anwendung mit genau den Berechtigungen debuggen, die ein Endbenutzer hat. Debuggen mit eingeschränkten Berechtigungen kann im **Projekt-Designer** auf der Seite **Sicherheit**aktiviert werden.  
  
 Wenn Sie eine Anwendung mit eingeschränkten Berechtigungen debuggen, wird für jede Codesicherheitsanforderung, die nicht auf der Seite **Sicherheit** aktiviert ist, eine Ausnahme ausgelöst. Es wird eine Ausnahmen-Hilfe angezeigt, die Vorschläge bereitstellt, wie Sie Ihren Code ändern sollten, um die Ausnahme zu vermeiden.  
  
 Außerdem deaktiviert die IntelliSense-Funktion, wenn Sie Code schreiben, im Code-Editor alle Elemente, die nicht in den Sicherheitsberechtigungen enthalten sind, die Sie konfiguriert haben.  
  
 Weitere Informationen finden Sie unter [Gewusst wie: Debuggen eine ClickOnce-Anwendung mit eingeschränkten Berechtigungen](../deployment/how-to-debug-a-clickonce-application-with-restricted-permissions.md).  
  
## <a name="security-permissions-for-browser-hosted-applications"></a>Sicherheitsberechtigungen für im Browser gehostete Anwendungen  
 Visual Studio bietet die folgenden Projekttypen für WPF-Anwendungen (Windows Presentation Foundation):  
  
-   WPF-Windows-Anwendung  
  
-   WPF-Webbrowseranwendung  
  
-   WPF-Benutzerdefinierte Steuerelementbibliothek  
  
-   WPF-Dienstbibliothek  
  
 Da nur WPF-Webbrowseranwendungen in einem Webbrowser gehostet werden, erfordert nur dieser Projekttyp spezielle Bereitstellungs- und Sicherheitseinstellungen. Die Standardsicherheitseinstellungen für diese Anwendungen sind wie folgt:  
  
-   **ClickOnce-Sicherheitseinstellungen aktivieren**  
  
-   **Teilweise vertrauenswürdige Anwendung**  
  
-   **Internetzone** (mit ausgewähltem Standardberechtigungssatz für WPF-Webbrowseranwendungen)  
  
 Im Dialogfeld **Erweiterte Sicherheitseinstellungen** ist das Kontrollkästchen **Diese Anwendung mit dem ausgewählten Berechtigungssatz debuggen** ausgewählt und deaktiviert. Ursache hierfür ist, dass für im Browser gehostete Anwendungen Debuggen in einer Zone nicht deaktiviert werden kann.  
  
## <a name="see-also"></a>Siehe auch  
 [Sichern von ClickOnce-Anwendungen](../deployment/securing-clickonce-applications.md)   
 [How to: Enable ClickOnce Security Settings (Vorgehensweise: Aktivieren von ClickOnce-Sicherheitseinstellungen)](../deployment/how-to-enable-clickonce-security-settings.md)   
 [How to: Set a Security Zone for a ClickOnce Application (Vorgehensweise: Festlegen einer Sicherheitszone für eine ClickOnce-Anwendung)](../deployment/how-to-set-a-security-zone-for-a-clickonce-application.md)   
 [How to: Set Custom Permissions for a ClickOnce Application (Vorgehensweise: Festlegen von benutzerdefinierten Berechtigungen für eine ClickOnce-Anwendung)](../deployment/how-to-set-custom-permissions-for-a-clickonce-application.md)   
 [How to: Debug a ClickOnce Application with Restricted Permissions (Vorgehensweise: Debuggen einer ClickOnce-Anwendung mit eingeschränkten Berechtigungen)](../deployment/how-to-debug-a-clickonce-application-with-restricted-permissions.md)   
 [Überblick über die Bereitstellung vertrauenswürdiger Anwendungen](../deployment/trusted-application-deployment-overview.md)   
 [Seite „Sicherheit“, Projekt-Designer](../ide/reference/security-page-project-designer.md)


