---
title: Attach | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 79614283-6733-4592-a53a-d428052271ad
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7c5c734d4d0b12bea1e13ac216700be5f85ed088
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56627336"
---
# <a name="attach"></a>Anfügen
Die *VSPerfCmd.exe*-Option **Attach** beginnt mit der Samplingprofilerstellung für den ausgeführten Prozesses, der durch die Prozess-ID (PID) angegeben wird.

 Um **Attach** zu verwenden, müssen Sie die Methode **Sample** in der Option „Start“ angeben.

> [!NOTE]
>  Wenn die Option **CrossSession** für die Option **Start** angegeben wurde, müssen alle Aufrufe von **VSPerfCmd /Attach** oder **VSPerfCmd /Detach** auch **CrossSession** angeben.

## <a name="syntax"></a>Syntax

```cmd
VSPerfCmd.exe /Attach:ProcessID [Options]
```

#### <a name="parameters"></a>Parameter
 `ProcessID`: die Prozess-ID (PID) des laufenden Prozesses. Die PID eines laufenden Prozesses wird auf der Registerkarte „Prozesse“ des Windows Task-Managers aufgeführt.

## <a name="valid-options"></a>Gültige Optionen
 Die folgenden **VSPerfCmd**-Optionen können mit der Option **Attach** in derselben Befehlszeile kombiniert werden.

 **CrossSession:** aktiviert die Profilerstellung für Anwendungen in Sitzungen, die keine Anmeldesitzungen sind. Diese Option ist erforderlich, wenn die Option **Start** mit der Option **CrossSession** angegeben wurde.

 **Start:** `Method` initialisiert die Befehlszeilen-Profilerstellungssitzung und legt die angegebene Profilerstellungsmethode fest.

 **TargetCLR:** Gibt die Version der .NET Framework-CLR (Common Language Runtime) für die Profilerstellung an, wenn mehr als eine Version in einer Profilerstellungssitzung geladen wird. Standardmäßig wird für die zuerst geladene Version ein Profil erstellt.

 **GlobalOn und GlobalOff**: Setzen die Profilerstellung fort (**GlobalOn**) oder unterbrechen sie (**GlobalOff**), aber nicht die Profilerstellungssitzung.

 **ProcessOn:** `PID` **ProcessOff:** `PID` setzt die Profilerstellung für den angegebenen Prozess fort (**ProcessOn**) oder unterbricht sie (**ProcessOff**).

## <a name="interval-options"></a>Intervalloptionen
 Eine der folgenden Optionen für Samplingintervalle kann in der Attach-Befehlszeile angegeben werden. Das Standardsamplingintervall sind 10.000.000 Prozessortaktzyklen.

 **Timer**[**:**`Cycles`]**PF**[**:**`Events`]**Sys**[<strong>:</strong>Events]**Counter**[**:**`Name`,`Reload`,`FriendlyName`]: gibt die Anzahl und den Typ des Samplingintervalls an.

-   **Timer**: Sampelt alle `Cycles`-Prozessortaktzyklen. Wenn `Cycles` nicht angegeben ist, wird ein Intervall von 10.000.000 verwendet.

-   **PF**: Sampelt alle `Events`-Seitenfehler. Wenn `Events` nicht angegeben ist, geschieht dies bei jedem 10. Seitenfehler.

-   **Sys**: Sampelt `Events`-Aufrufe des Betriebssystems. Wenn `Events` nicht angegeben ist, wird jeder 10. Systemaufruf untersucht.

-   **Counter**: Sampelt alle `Reload`-Zahlen der von `Name` angegebenen CPU-Leistungsindikatoren. `FriendlyName` kann optional eine Zeichenfolge angeben, die als Spaltenüberschrift in Profilerberichten verwendet wird.

## <a name="example"></a>Beispiel
 In diesem Beispiel wird veranschaulicht, wie eine ausgeführte Instanz einer Anwendung mit der Prozess-ID 12345 angefügt wird.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Attach:12345
```

## <a name="see-also"></a>Siehe auch
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Profilerstellung für eigenständige Anwendungen](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profilerstellung für ASP.NET-Webanwendungen](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profilerstellung für Dienste](../profiling/command-line-profiling-of-services.md)