---
title: 'Vorgehensweise: Veröffentlichen einer WPF-Anwendung mit aktivierten visuellen Stilen | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 73b22b02-fc75-42aa-82d3-51fdcaf8e5c8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ef6250e9e413d91c218634e90fe67a4f04b83bce
ms.sourcegitcommit: cea6187005f8a0cdf44e866a1534a4cf5356208c
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2019
ms.locfileid: "56953916"
---
# <a name="how-to-publish-a-wpf-application-with-visual-styles-enabled"></a>Vorgehensweise: Veröffentlichen einer WPF-Anwendung mit aktivierten visuellen Designs

Durch visuelle Stile kann die Darstellung von allgemeinen Steuerelementen auf Grundlage des vom Benutzer ausgewählten Designs geändert werden. Standardmäßig werden keine visuellen Stile für WPF-Anwendungen (Windows Presentation Foundation) aktiviert. Daher müssen Sie sie manuell aktivieren. Allerdings tritt bei der Veröffentlichung der Projektmappe ein Fehler auf, wenn visuelle Stile für eine WPF-Anwendung aktiviert sind. In diesem Thema wird beschrieben, wie dieser Fehler zu beheben ist und wie eine WPF-Anwendung mit aktivierten visuellen Stilen veröffentlicht werden kann. Weitere Informationen zu visuellen Stilen finden Sie unter [Übersicht über die visuelle Stile](/windows/desktop/Controls/visual-styles-overview). Weitere Informationen zur Fehlermeldung finden Sie unter [Beheben von spezifischen Fehlern in ClickOnce-Bereitstellungen](../deployment/troubleshooting-specific-errors-in-clickonce-deployments.md).

 Um den Fehler zu beheben und die Projektmappe zu veröffentlichen, müssen Sie die folgenden Schritte ausführen:

- [Veröffentlichen der Projektmappe ohne aktivierten visuellen Designs](#publish-the-solution-without-visual-styles-enabled)

- [Erstellen einer Manifestdatei](#create-a-manifest-file)

- [Einbetten der Manifestdatei in die ausführbare Datei der veröffentlichten Projektmappe](#embed-the-manifest-file-into-the-executable-file-of-the-published-solution)

- [Signieren der Anwendungs- und Bereitstellungsmanifeste](#sign-the-application-and-deployment-manifests)

  Anschließend können Sie die veröffentlichten Dateien an den Speicherort verschieben, von dem Endbenutzer die Anwendung installieren sollen.

##  <a name="publish-the-solution-without-visual-styles-enabled"></a>So veröffentlichen Sie die Projektmappe ohne aktivierte visuelle Stile

1. Stellen Sie sicher, dass visuelle Stile für das Projekt nicht aktiviert sind. Überprüfen Sie zunächst die Manifestdatei des Projekts auf folgenden XML-Code. Wenn der XML-Code vorhanden ist, schließen Sie ihn in ein Kommentartag ein.

     Visuelle Stile sind standardmäßig nicht aktiviert.

    ```xml
    <dependency>
        <dependentAssembly>
            <assemblyIdentity type="win32" name="Microsoft.Windows.Common-Controls" version="6.0.0.0" processorArchitecture="*" publicKeyToken="6595b64144ccf1df" language="*" />
        </dependentAssembly>
    </dependency>
    ```

     Die folgenden Prozeduren zeigen, wie die Manifestdatei geöffnet wird, die Ihrem Projekt zugeordnet ist.

    **So öffnen Sie die Manifestdatei in einem Visual Basic-Projekt**

    1. Wählen Sie auf der Menüleiste **Projekt**, *ProjectName* **Eigenschaften**, wobei *ProjectName* ist der Name des WPF-Projekts.

         Die Eigenschaftenseiten für das WPF-Projekt werden angezeigt.

    2. Klicken Sie in der Registerkarte **Anwendung** auf **Windows-Einstellungen anzeigen**.

         Die Datei „app.manifest“ wird im **Code-Editor** geöffnet.

    **So öffnen Sie die Manifestdatei in einem C#-Projekt**

    1. Wählen Sie auf der Menüleiste **Projekt**, *ProjectName* **Eigenschaften**, wobei *ProjectName* ist der Name des WPF-Projekts.

         Die Eigenschaftenseiten für das WPF-Projekt werden angezeigt.

    2. Beachten Sie auf der Registerkarte **Anwendung** den Namen, der im Manifestfeld angezeigt wird. Dies ist der Name des Manifests, das dem Projekt zugeordnet ist.

        > [!NOTE]
        > Wenn **Manifest mit Standardeinstellungen einbetten** oder **Anwendung ohne Manifest erstellen** im Manifestfeld angezeigt wird, werden visuelle Designs nicht aktiviert. Wenn der Name einer Manifestdatei im Manifestfeld angezeigt wird, wechseln Sie zum nächsten Schritt in diesem Verfahren.

    3. Klicken Sie im **Projektmappen-Explorer** auf **Alle Dateien anzeigen**.

         Mit dieser Schaltfläche werden alle Projektelemente angezeigt, einschließlich der ausgeschlossen und derjenigen, die normalerweise ausgeblendet werden. Die Manifestdatei erscheint als Projektelement.

2. Erstellen und veröffentlichen Sie die Projektmappe. Weitere Informationen zum Veröffentlichen der Projektmappe finden Sie unter [Vorgehensweise: veröffentlichen eine ClickOnce-Anwendung, die mit dem Webpublishing-Assistenten](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md).

## <a name="create-a-manifest-file"></a>So erstellen Sie eine Manifestdatei

1. Fügen Sie folgendes XML in eine Editor-Datei ein.

     Dieser XML-Code beschreibt die Assembly, die Steuerelemente enthält, die visuelle Stile unterstützen.

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <asmv1:assembly manifestVersion="1.0"
        xmlns="urn:schemas-microsoft-com:asm.v1"
        xmlns:asmv1="urn:schemas-microsoft-com:asm.v1"
        xmlns:asmv2="urn:schemas-microsoft-com:asm.v2"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
        <dependency>
            <dependentAssembly>
                <assemblyIdentity type="win32" name="Microsoft.Windows.Common-Controls" version="6.0.0.0" processorArchitecture="*" publicKeyToken="6595b64144ccf1df" language="*" />
            </dependentAssembly>
        </dependency>
    </asmv1:assembly>
    ```

2. Klicken Sie im Editor auf **Datei**, und klicken Sie dann auf **Speichern unter...**

3. Klicken Sie im Dialogfeld **Speichern unter** auf die Dropdownliste **Dateityp**, und wählen Sie **Alle Dateien** aus.

4. Geben Sie im Feld **Dateiname** einen Namen für die Datei ein, und fügen Sie dem Ende des Namens *.manifest* an. Beispiel: *themes.manifest*.

5. Klicken Sie auf die Schaltfläche **Ordner durchsuchen**, wählen Sie einen beliebigen Ordner aus, und klicken Sie dann auf **Speichern**.

    > [!NOTE]
    > Im verbleibenden Verfahren wird davon ausgegangen, dass der Name dieser Datei *themes.manifest* ist und auf dem Computer im Verzeichnis *C:\temp* gespeichert wird.

## <a name="embed-the-manifest-file-into-the-executable-file-of-the-published-solution"></a>So fügen Sie die Manifestdatei in die ausführbare Datei der veröffentlichten Projektmappe ein

1. Öffnen Sie die **Visual Studio-Eingabeaufforderung**.

    Weitere Informationen zum Öffnen der **Visual Studio-Eingabeaufforderung**, finden Sie unter [eingabeaufforderungen](/dotnet/framework/tools/developer-command-prompt-for-vs).

   > [!NOTE]
   > In den verbleibenden Schritten werden die folgenden Annahmen über die Projektmappe gemacht:
   >
   > - Der Name der Projektmappe ist **MyWPFProject**.
   > - Die Projektmappe befindet sich im folgenden Verzeichnis: `%UserProfile%\Documents\Visual Studio 2010\Projects\`.
   >
   > - Die Lösung wird im folgenden Verzeichnis veröffentlicht: `%UserProfile%\Documents\Visual Studio 2010\Projects\publish`.
   > - Die neueste Version der veröffentlichten Anwendungsdateien befindet sich im folgenden Verzeichnis: `%UserProfile%\Documents\Visual Studio 2010\Projects\publish\Application Files\WPFApp_1_0_0_0`
   >
   > Sie müssen die oben genannten Namen und Verzeichnisspeicherorte nicht verwenden. Die oben genannten Namen und Speicherorte dienen nur als Beispiele bei der Veranschaulichung der Schritte, die für die Veröffentlichung der Projektmappe erforderlich sind.

2. Ändern Sie an der Eingabeaufforderung den Pfad zu dem Verzeichnis, das die neueste Version der veröffentlichten Anwendungsdateien enthält. Das folgende Beispiel veranschaulicht diesen Schritt.

   ```cmd
   cd "%UserProfile%\Documents\Visual Studio 2010\Projects\MyWPFProject\publish\Application Files\WPFApp_1_0_0_0"
   ```

3. Geben Sie an der Eingabeaufforderung den folgenden Befehl ein, um die Manifestdatei in die ausführbare Datei der Anwendung einzubetten:

   ```cmd
   mt -manifest c:\temp\themes.manifest -outputresource:MyWPFApp.exe.deploy
   ```

## <a name="sign-the-application-and-deployment-manifests"></a>So signieren Sie die Anwendungs- und Bereitstellungsmanifeste

1. Führen Sie an der Eingabeaufforderung den folgenden Befehl zum Entfernen der *".deploy"* Erweiterung aus der ausführbaren Datei im aktuellen Verzeichnis.

   ```cmd
   ren MyWPFApp.exe.deploy MyWPFApp.exe
   ```

   > [!NOTE]
   > In diesem Beispiel wird davon ausgegangen, dass nur eine Datei hat die *".deploy"* Dateierweiterung. Stellen Sie sicher, dass Sie alle Dateien in diesem Verzeichnis umbenennen, die die *".deploy"* Dateierweiterung.

2. Geben Sie an der Eingabeaufforderung den folgenden Befehl zum Signieren des Anwendungsmanifests ein:

   ```cmd
   mage -u MyWPFApp.exe.manifest -cf ..\..\..\MyWPFApp_TemporaryKey.pfx
   ```

   > [!NOTE]
   > In diesem Beispiel wird davon ausgegangen, dass Sie mit das Manifest signiert die *PFX* -Datei des Projekts. Wenn Sie das Manifest nicht signieren, können Sie weglassen der `-cf` Parameter, die in diesem Beispiel verwendet wird. Wenn Sie das Manifest mit einem Zertifikat, das ein Kennwort erforderlich ist signieren, geben Sie die `-password` Option (`For example: mage -u MyWPFApp.exe.manifest -cf ..\..\..\MyWPFApp_TemporaryKey.pfx - password Password`).

3. Führen Sie an der Eingabeaufforderung den folgenden Befehl zum Hinzufügen der *".deploy"* Erweiterung auf den Namen der Datei, die Sie in einem vorherigen Schritt dieses Verfahrens umbenannt.

   ```
   ren MyWPFApp.exe MyWPFApp.exe.deploy
   ```

   > [!NOTE]
   > In diesem Beispiel wird davon ausgegangen, dass nur eine Datei hatte eine *".deploy"* Dateierweiterung. Stellen Sie sicher, dass Sie alle Dateien in diesem Verzeichnis umbenennen, die bisher die *".deploy"* Dateinamenerweiterung.

4. Geben Sie an der Eingabeaufforderung den folgenden Befehl zum Signieren des Verteilungsmanifests ein:

   ```
   mage -u ..\..\MyWPFApp.application -appm MyWPFApp.exe.manifest -cf ..\..\..\MyWPFApp_TemporaryKey.pfx
   ```

   > [!NOTE]
   > In diesem Beispiel wird davon ausgegangen, dass Sie mit das Manifest signiert die *PFX* -Datei des Projekts. Wenn Sie das Manifest nicht signieren, können Sie weglassen der `-cf` Parameter, die in diesem Beispiel verwendet wird. Wenn Sie das Manifest mit einem Zertifikat, das ein Kennwort erforderlich ist signieren, geben Sie die `-password` auswählen, wie im folgenden Beispiel:`For example: mage -u MyWPFApp.exe.manifest -cf ..\..\..\MyWPFApp_TemporaryKey.pfx - password Password`.

   Nachdem Sie diese Schritte ausgeführt haben, können Sie die veröffentlichten Dateien an den Speicherort verschieben, von dem aus Endbenutzer die Anwendung installieren sollen. Wenn Sie beabsichtigen, die Projektmappe häufig zu aktualisieren, können Sie diese Befehle in ein Skript übernehmen und das Skript jedes Mal ausführen, wenn Sie eine neue Version veröffentlichen.

## <a name="see-also"></a>Siehe auch

-[Troubleshooting Specific Errors in ClickOnce Deployments (Beheben von spezifischen Fehlern in ClickOnce-Bereitstellungen)](../deployment/troubleshooting-specific-errors-in-clickonce-deployments.md)
- [Übersicht über die visuelle Stile](/windows/desktop/Controls/visual-styles-overview)
- [Enabling Visual Styles (Aktivieren von visuellen Designs)](/windows/desktop/Controls/cookbook-overview)
- [Eingabeaufforderungen](/dotnet/framework/tools/developer-command-prompt-for-vs)
