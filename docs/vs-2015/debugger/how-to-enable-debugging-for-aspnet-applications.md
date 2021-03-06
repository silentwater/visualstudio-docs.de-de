---
title: 'Vorgehensweise: Aktivieren Sie das Debuggen für ASP.NET-Anwendungen | Microsoft-Dokumentation'
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
- debugging ASP.NET Web applications
- Web.config configuration file, debug mode
- debugging [Visual Studio], ASP.NET
ms.assetid: 3beed819-cece-4864-8184-bd410000973a
caps.latest.revision: 40
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0dbedf6f2bc0832fa3ba54f691cbf713ccb533a9
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58947011"
---
# <a name="how-to-enable-debugging-for-aspnet-applications"></a>Vorgehensweise: Aktivieren Sie Debuggen für ASP.NET-Anwendungen
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Wenn Sie das Debuggen aktivieren möchten, müssen Sie es auf der Seite **Projekteigenschaften** und in der Datei Web.config der Anwendung aktivieren.  
  
> [!NOTE]  
> Je nach den aktiven Einstellungen oder der Version unterscheiden sich die Dialogfelder und Menübefehle auf Ihrem Bildschirm möglicherweise von den in der Hilfe beschriebenen. Klicken Sie im Menü **Extras** auf **Einstellungen importieren und exportieren** , um die Einstellungen zu ändern. Weitere Informationen finden Sie unter [Anpassen der Entwicklungseinstellungen in Visual Studio](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### <a name="to-enable-aspnet-debugging-in-the-project-properties-visual-basicc"></a>So aktivieren Sie das ASP.NET-Debuggen in den Projekteigenschaften (Visual Basic/C#)  
  
1.  Klicken Sie im **Projektmappen-Explorer**mit der rechten Maustaste auf den Namen eines Webprojekts, und wählen Sie **Eigenschaften**aus.  
  
2.  Klicken Sie in der Projekteigenschaftenseite auf die Registerkarte **Web** .  
  
3.  Aktivieren Sie unter **Debugger**das Kontrollkästchen **ASP.NET** .  
  
### <a name="to-enable-debugging-in-the-webconfig-file"></a>So aktivieren Sie Debuggen in der Datei web.config  
  
1.  Öffnen Sie die Datei web.config mit einem beliebigen Text-Editor oder XML-Parser.  
  
    > [!NOTE]  
    > Allerdings ist es nicht möglich, über einen Webbrowser remote auf die Datei zuzugreifen. Aus Sicherheitsgründen wird Microsoft IIS durch [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] so konfiguriert, dass ein direkter Browserzugriff auf die Web.config-Dateien nicht möglich ist. Wenn Sie versuchen, mit einem Browser auf eine Konfigurationsdatei zuzugreifen, wird der HTTP-Zugriffsfehler 403 (verweigert) ausgegeben.  
  
2.  Web.config ist eine XML-Datei und enthält daher mit Tags markierte, geschachtelte Abschnitte. Suchen Sie das Element `configuration/system.web/compilation` . Wenn das compilation-Element nicht den vorhanden ist, erstellen Sie es.  
  
3.  Wenn das `compilation` -Element kein `debug` -Attribut enthält, fügen Sie dem Element das Attribut hinzu.  
  
4.  Stellen Sie sicher, dass der `debug` -Attributwert auf `true`.  
  
Die Datei "Web.config" sollte wie im folgenden Beispiel aussehen. Beachten Sie, dass es Abschnitte zwischen den Konfigurations- und den system.web-Elementen geben kann.  
  
-   Elementabschnitte zwischen den Konfigurations- und system.web-Elementen  
  
-   Elementabschnitte zwischen den system.web- und compilation-Elementen  
  
-   Das compilation-Element kann andere Attribute und Elemente enthalten.  
  
## <a name="example"></a>Beispiel  
  
```  
<configuration>  
    ...  
    <system.web>  
        <compilation  
            debug="true"  
            ...  
        >  
        ...  
        </compilation>  
    </system.web>  
</configuration>  
```  
  
## <a name="robust-programming"></a>Stabile Programmierung  
An Web.config-Dateien vorgenommene Änderungen werden von [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] automatisch erkannt und die neuen Konfigurationseinstellungen angewendet. Sie müssen den Computer oder den IIS-Server nicht neu starten, damit die Änderungen wirksam werden.  
  
Eine Website kann mehrere virtuelle Verzeichnisse und Unterverzeichnisse enthalten, in denen möglicherweise Web.config-Dateien vorhanden sind. [!INCLUDE[vstecasp](../includes/vstecasp-md.md)]-Anwendungen erben Einstellungen von Web.config-Dateien auf höheren Ebenen im URL-Pfad. Mithilfe hierarchischer Konfigurationsdateien können Sie die Einstellungen für mehrere [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] -Anwendungen gleichzeitig ändern, z. B. für alle Anwendungen, die sich in der Hierarchie unterhalb der jeweiligen Konfigurationsdatei befinden. Wenn jedoch in einer Datei auf einer niedrigeren Ebene der Hierarchie `debug` festgelegt ist, wird der aus höheren Ebenen geerbte Wert überschrieben.  
  
So können Sie z. B. in www.microsoft.com/aaa/Web.config `debug="true"` angeben, und alle Anwendungen im Ordner aaa und in jedem Unterordner von aaa erben diese Einstellung. Wenn sich die [!INCLUDE[vstecasp](../includes/vstecasp-md.md)]-Anwendung also unter www.microsoft.com/aaa/bbb befindet, erbt sie diese Einstellung ebenso wie alle [!INCLUDE[vstecasp](../includes/vstecasp-md.md)]-Anwendungen unter www.microsoft.com/aaa/ccc, www.microsoft.com/aaa/ddd usw. Die einzige Ausnahme stellen Anwendungen dar, die die Einstellungen mit einer eigenen Web.config-Datei auf einer niedrigeren Ebene überschreiben.  
  
Das Aktivieren des Debugmodus wirkt sich entscheidend auf die Leistung der [!INCLUDE[vstecasp](../includes/vstecasp-md.md)] -Anwendung aus. Vergessen Sie nie, den Debugmodus zu deaktivieren, bevor Sie die Releaseversion einer Anwendung bereitstellen oder Leistungsmessungen durchführen.  
  
## <a name="see-also"></a>Siehe auch  
[Debuggen von ASP.NET- und AJAX-Anwendungen](../debugger/debugging-aspnet-and-ajax-applications.md)  
