---
title: Debuggen von 64-Bit-Anwendungen | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [Visual Studio], 64-bit
- 64-bit debugging
ms.assetid: db648e5f-6375-4e2d-aa98-eb7261958927
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 206b14a1cdab61d64354e134449149b70a030683
ms.sourcegitcommit: cea6187005f8a0cdf44e866a1534a4cf5356208c
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2019
ms.locfileid: "56954492"
---
# <a name="debug-64-bit-applications"></a>Debuggen von 64-Bit-Anwendungen
Sie können eine 64-Bit-Anwendung debuggen, die auf dem lokalen Computer oder einem Remotecomputer ausgeführt wird.

 Informationen zum Debuggen einer 64-Bit-Anwendung, die auf einem Remotecomputer ausgeführt wird, finden Sie unter [Remote Debugging](../debugger/remote-debugging.md).

 Um 64-Bit-Anwendungen lokal zu debuggen, verwendet Visual Studio einen 64-Bit-Arbeitsprozess (msvsmon.exe), um die die Low-Level-Vorgänge auszuführen, die nicht im 32-Bit-Visual Studio-Prozess ausgeführt werden können.

 Debuggen im gemischten Modus wird nicht für 64-Bit-Prozesse unterstützt, in denen .NET Framework Version 3.5 oder früher verwendet wird.

## <a name="debug-a-64-bit-application"></a>Debuggen einer 64-Bit-Anwendung
 So können Sie eine 64-Bit-Anwendung debuggen:

1.  Erstellen Sie eine Visual Studio-Projektmappe z. B. ein C#-Konsolenanwendungsprojekt.

2.  Legen Sie die Konfiguration mit dem Konfigurations-Manager auf 64-Bit fest. Weitere Informationen finden Sie unter [How to: Configure Projects to Target Platforms](../ide/how-to-configure-projects-to-target-platforms.md).

3.  Nun wird die 64-Bit-Version des Remotedebuggers (msvsmon.exe) gestartet. Diese wird ausgeführt, solange die Projektmappe mit der 64-Bit-Konfiguration geöffnet ist.

4.  Beginnen Sie mit dem Debuggen. Ihnen sollte dieselbe Funktionalität zur Verfügung stehen wie bei einer 32-Bit-Konfiguration. Informationen zur Vorgehensweise bei Fehlern finden Sie nachstehend im Abschnitt „Problembehandlung“.

## <a name="troubleshooting-64-bit-debugging"></a>Problembehandlung beim 64-Bit-Debuggen
 Möglicherweise wird folgende Fehlermeldung angezeigt: "A 64-bit debugging operation is taking longer than expected." (Ein 64-Bit-Debuggingvorgang dauert länger als erwartet.) In diesem Fall hat Visual Studio eine Anforderung an die 64-Bit-Version von „msvsmon.exe“ gesendet, und es hat sehr lange gedauert , bis das Ergebnis dieser Anforderung eingetroffen ist.

 Für diesen Fehler gibt es zwei Hauptursachen:

-   Sie haben Netzwerksicherheitssoftware auf dem Computer installiert, die dazu geführt hat, dass der Netzwerkstapel unzuverlässig wurde und über Localhost gesendete Pakete gelöscht wurden. Deaktivieren Sie jegliche Netzwerksicherheitssoftware, und ermitteln Sie, ob das Problem damit behoben ist. Wenn ja, teilen Sie dem Hersteller der Netzwerksicherheitssoftware mit, dass die Software zu einem Konflikt mit Localhost-Datenverkehr führt.

-   Sie treffen auf ein Absturz- oder Leistungsproblem mit Visual Studio. Tritt dieses Problem regelmäßig auf, können Sie Speicherabbilder von Visual Studio (devenv.exe) und vom Arbeitsprozess (msvsmon.exe) sammeln und diese an Microsoft senden. Weitere Informationen zum Berichten eines Problems finden Sie unter [How to Report a Problem with Visual Studio](../ide/how-to-report-a-problem-with-visual-studio.md).

## <a name="see-also"></a>Siehe auch

- [64-Bit-Anwendungen](https://docs.microsoft.com/dotnet/framework/64-bit-apps)
- [Configuring Programs for 64-Bit (Konfigurieren von Programmen für 64-Bit)](/cpp/build/configuring-programs-for-64-bit-visual-cpp)
- [Visual Studio-IDE-64-Bit-Unterstützung](../ide/visual-studio-ide-64-bit-support.md)
- [Speichern von Dumpdateien](../debugger/using-dump-files.md)
- [Remote Debugging](../debugger/remote-debugging.md)