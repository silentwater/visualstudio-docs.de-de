---
title: Erste Schritte mit Unittests
ms.date: 05/02/2017
ms.topic: conceptual
helpviewer_keywords:
- unit testing, create unit test plans
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 52a3d63bb7f632f1eacea603c96787dbb36d90fa
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "57984117"
---
# <a name="get-started-with-unit-testing"></a>Erste Schritte mit Unittests

Verwenden Sie Visual Studio, um Komponententests zu definieren und auszuführen, um die Integrität Ihres Codes zu gewährleisten, Code Coverage sicherzustellen und Fehler zu finden, bevor diese von Ihren Kunden erkannt werden. Führen Sie Ihre Komponententests regelmäßig durch, um sicherzustellen, dass Ihr Core ordnungsgemäß funktioniert.

## <a name="create-unit-tests"></a>Erstellen von Unittests

In diesem Abschnitt wird genauestens beschrieben, wie Sie ein Komponententestprojekt erstellen.

> [!TIP]
> Das getestete Projekt „HelloWorld“ ist ein Beispielprojekt, für das kein Code angezeigt werden soll. Wenn Sie ein HelloWorld-Projekt zum Testen erstellen möchten, finden Sie Anweisungen dazu unter [Erstellen Ihrer ersten C#-Konsolenanwendung](../ide/quickstart-csharp-console.md). Eine vollständige exemplarische Vorgehensweise finden Sie unter [Erstellen und Ausführen von Komponententests für verwalteten Code](walkthrough-creating-and-running-unit-tests-for-managed-code.md).

1. Erstellen Sie ein Unittests.

   ![Hinzufügen einer Projektmappe zu einem Unittestprojekt](media/createunittest1.png)

1. Geben Sie dem Projekt einen Namen.

   ![Vorlage für Unittestprojekte](media/createunittest2.png)

   Das Projekt wird Ihrer Projektmappe hinzugefügt.

   ![Wählen Sie das Unittestprojekt im Projektmappen-Explorer aus.](media/createunittest5.png)

1. Fügen Sie im Unittestprojekt dem zu testenden Projekt eine Referenz hinzu.

   ![Hinzufügen eines Verweises zu Ihrem Unittestprojekt.](media/createunittest6.png)

1. Wählen Sie das Projekt aus, das den Code enthält, den Sie testen möchten.

   ![Auswählen des hinzuzufügenden Verweises](media/createunittest7.png)

1. Programmieren Sie den Unittest.

   ![Hinzufügen von Code zu Ihrem Unittest](media/createunittest8.png)

Sie können Stubs für Komponententestmethoden auch mit dem **Befehl** [Komponententests erstellen](create-unit-tests-menu.md) erstellen.

![Verwenden des Befehls „Unittests erstellen“](media/createunittestcommand2.png)

## <a name="run-unit-tests"></a>Komponententests ausführen

1. Öffnen Sie den **Test-Explorer**.

   ![Öffnen des Test-Explorers im Menü „Test“](media/rununittest1.png)

1. Führen Sie Unittests aus.

   ![Ausführen von Komponententests im Test-Explorer](media/rununittest2.png)

   Es werden die Komponententests angezeigt, die im **Test-Explorer** entweder erfolgreich oder mit Fehlern ausgeführt wurden.

   ![Überprüfen der Unittestsergebnisse im Test-Explorer](media/rununittest3.png)

## <a name="view-live-unit-test-results"></a>Anzeigen der Ergebnisse von Liveunittests

Wenn Sie die Testframeworks MSTest, xUnit oder NUnit in Visual Studio 2017 oder höher verwenden, werden Live-Ergebnisse Ihrer Komponententests angezeigt.

> [!NOTE]
> Livekomponententests sind nur in der Visual Studio Enterprise-Edition verfügbar.

1. Aktivieren Sie die Liveunittests im Menü **Test**.

   ![Aktivieren der Liveunittests](media/live-test-results-start.png)

1. Schauen Sie sich die Ergebnisse der Tests im Fenster des Code-Editors an, während Sie Code schreiben und diesen bearbeiten.

   ![Überprüfen der Ergebnisse der Tests](media/live-test-results-ui.png)

1. Wählen Sie die Testergebnisindikatoren aus, um mehr Informationen anzuzeigen.

   ![Auswählen der Testergebnisindikatoren](media/live-test-results-details.png)

Weitere Informationen finden Sie unter [Live Unit Testing](../test/live-unit-testing-intro.md).

## <a name="generate-unit-tests-with-intellitest"></a>Generieren von Unittests mit IntelliTest

Wenn Sie IntelliTest ausführen, erkennen Sie ohne weiteres, welche Tests zu einem Fehler führen, und können den erforderlichen Code hinzufügen, um die Fehler zu beseitigen. Sie können wählen, welche der generierten Tests in einem Testprojekt gespeichert werden sollen, um eine Regressionsreihe zu erstellen. Wenn Sie den Code ändern, führen Sie IntelliTest erneut aus, damit die generierten Tests mit den Codeänderungen synchronisiert werden. Weitere Informationen finden Sie unter [Generieren von Komponententests für Code mit IntelliTest](../test/generate-unit-tests-for-your-code-with-intellitest.md).

![Erzeugen von Unittests mit IntelliTest](media/intellitest.png)

## <a name="run-unit-tests-with-test-explorer"></a>Ausführen von Komponententests mit dem Test-Explorer

Mithilfe des **Test-Explorers** können Sie Komponententests aus Visual Studio oder Testprojekte von Drittanbietern ausführen, Tests in Kategorien gruppieren, die Testliste filtern sowie Testwiedergabelisten erstellen, speichern und ausführen. Zudem können Sie Tests debuggen und die Leistung und Codeabdeckung von Tests analysieren. Weitere Informationen finden Sie unter [Ausführen von Unittests mit dem Test-Explorer](../test/run-unit-tests-with-test-explorer.md).

![Ausführen von Unittests mit dem Test-Explorer](media/testexplorer.png)

## <a name="use-code-coverage-to-determine-how-much-code-is-being-tested"></a>Bestimmen des Umfangs des zu testenden Codes mithilfe von Code Coverage

Wenn Sie den Anteil des Projektcodes ermitteln möchten, der in codierten Tests wie Komponententests tatsächlich getestet wird, verwenden Sie die Code Coverage-Funktion von Visual Studio. Um sich effektiv vor Fehlern zu schützen, sollten Sie die Tests für den Großteil Ihres Codes ausführen. Weitere Informationen finden Sie unter [Bestimmen des Umfangs des zu testenden Codes mithilfe von Code Coverage](../test/using-code-coverage-to-determine-how-much-code-is-being-tested.md).

## <a name="use-a-different-unit-test-framework"></a>Verwenden eines anderen Komponententest-Frameworks

Sie können Komponententests in Visual Studio auch über Testframeworks von Drittanbietern wie Boost, Google und NUnit ausführen. Verwenden Sie das Plug-In für das Framework, damit der Test Runner von Visual Studio mit dem Framework arbeiten kann.

Führen Sie die folgenden Schritte aus, um Testframeworks von Drittanbietern zu aktivieren:

::: moniker range="vs-2017"

1. Wählen Sie auf der Menüleiste **Extras** > **Erweiterungen und Updates** aus.

2. Erweitern Sie im Dialogfeld **Erweiterungen und Updates** die Kategorie **Online**, und wählen Sie dann **Visual Studio Marketplace** aus. Wählen Sie anschließend **Extras** > **Testen** aus.

   ![Visual Studio Marketplace](media/extensions-and-updates-testing.png)

::: moniker-end

::: moniker range=">=vs-2019"

1. Wählen Sie auf der Menüleiste **Erweiterungen** > **Erweiterungen verwalten** aus.

2. Erweitern Sie im Dialogfeld **Erweiterungen verwalten** die Kategorie **Online**, und wählen Sie dann **Visual Studio Marketplace** aus. Wählen Sie anschließend **Extras** > **Testen** aus.

   ![Visual Studio Marketplace](media/extensions-and-updates-testing.png)

::: moniker-end

3. Wählen Sie das Framework oder den Adapter aus, die Sie installieren möchten, und klicken Sie auf **Herunterladen**.

4. Erstellen Sie ein Klassenbibliotheksprojekt, und fügen Sie es Ihrer Projektmappe hinzu.

   ![Benennen Sie das Klassenbibliotheksprojekt und fügen Sie es hinzu](media/create3rdpartyunittest3.png)

5. Installieren Sie das Plug-In. Wählen Sie im **Projektmappen-Explorer** das Klassenbibliotheksprojekt aus, und wählen Sie anschließend im Kontextmenü die Option **NuGet-Pakete verwalten** aus.

   ![Verwalten von NuGet-Paketen zum Installieren des Plug-Ins](media/create3rdpartyunittest3a.png)

   [NuGet](https://www.nuget.org/) ist eine Erweiterung von Visual Studio, mit der Sie Bibliotheken und Tools für Ihre Projekte hinzufügen und aktualisieren können.

6. Suchen Sie im Fenster **NuGet-Paket-Manager** nach dem Plug-In, und wählen Sie es aus. Klicken Sie anschließend auf **Installieren**.

   ![Installieren des Frameworks des Drittanbieters](media/create3rdpartyunittest4.png)

   In Ihrem Projekt wird auf das Framework verwiesen.

   ![Der Verweis für das Unittestframework des Drittanbieters wird Ihrer Projektmappe hinzugefügt.](media/create3rdpartyunittest6.png)

7. Wählen Sie im Knoten **Verweise** des Klassenbibliotheksprojekts den Eintrag **Verweis hinzufügen** aus.

   ![Fügen Sie einen Verweis auf das Projekt hinzu.](media/createunittest6.png)

8. Wählen Sie im Dialogfeld **Verweis-Manager** das Projekt mit dem Code aus, den Sie testen möchten.

   ![Wählen Sie das Codeprojekt aus, das Sie testen möchten.](media/createunittest7.png)

9. Programmieren Sie den Unittest.

   ![Hinzufügen von Code zur Codedatei für Ihren Komponententest](media/create3rdpartyunittest7.png)

## <a name="see-also"></a>Siehe auch

* [Exemplarische Vorgehensweise: Erstellen und Ausführen von Komponententests für verwalteten Code](walkthrough-creating-and-running-unit-tests-for-managed-code.md)
* [Create Unit Tests command (Befehl „Komponententests erstellen“)](create-unit-tests-menu.md)
* [Generieren von Tests mit IntelliTest](generate-unit-tests-for-your-code-with-intellitest.md)
* [Ausführen von Unittests mit dem Test-Explorer](run-unit-tests-with-test-explorer.md)
* [Bestimmen von Code Coverage](using-code-coverage-to-determine-how-much-code-is-being-tested.md)
* [Verbessern der Codequalität](improve-code-quality.md)