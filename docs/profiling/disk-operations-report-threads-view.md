---
title: Bericht über Datenträgervorgänge (Threadansicht) | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.cv.threads.report.diskoperations
helpviewer_keywords:
- Concurrency Visualizer, File Operations Report (Threads View)
ms.assetid: e352f4f3-f654-45eb-96ed-417863487ddc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c890ac9dbd3b542a400fc2a5b6db7ee2eb8f5db2
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56613855"
---
# <a name="disk-operations-report-threads-view"></a>Bericht über Datenträgervorgänge (Threadansicht)
Im Bericht über Datenträgervorgänge werden Datenträger-E/A-Vorgänge in den Datenträgerkanälen angezeigt.

 Für jeden Datenträgerzugriff, der für den Prozess durchgeführt wird, für den im derzeit angezeigten Zeitfenster ein Profil erstellt wird, werden folgende Informationen angezeigt:

-   Name und PID des Prozesses, von dem der Datenträgerzugriff durchgeführt wurde

-   ID des Threads, von dem auf den Datenträger zugegriffen wurde

-   Name der Datei, auf die zugegriffen wurde

-   Anzahl der Lesevorgänge pro Datei

-   Anzahl der gelesenen Bytes

-   Latenz beim Lesen in Millisekunden

-   Anzahl von Schreibvorgängen

-   Anzahl der geschriebenen Bytes

-   Latenz beim Schreiben in Millisekunden

## <a name="see-also"></a>Siehe auch
- [Threads View (Threadansicht)](../profiling/threads-view-parallel-performance.md)