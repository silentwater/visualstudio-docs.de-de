---
title: Grundlagen zu Samplingdatenwerten | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- sampling profiling method
- Profiling Tools, sampling
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f2668d5b60fba429613975cc24e751dbe07f87b7
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56641077"
---
# <a name="understand-sampling-data-values"></a>Grundlagen zu Samplingdatenwerten

Die *Samplingmethode* zur Profilerstellung der Visual Studio-Profilerstellungstools unterbricht den Computerprozessor in festgelegten Intervallen und erfasst die Funktionsaufrufliste. Eine *Aufrufliste* ist eine dynamische Struktur, die Informationen über die Funktionen speichert, die auf dem Prozessor ausgeführt werden.

Die Profileranalyse ermittelt, ob der Prozessor Code im Zielprozess ausführt. Wenn der Prozessor keinen Code im Zielprozess ausführt, wird das Sampling verworfen.

Wenn der Prozessor den Zielcode ausführt, erhöht der Profiler die Samplinganzahl für jede Funktion in der Aufrufliste. Während der Erfassung des Samplings führt nur eine Funktion in der Aufrufliste Code aus. Die anderen Funktionen in der Liste sind übergeordnete Elemente in der Hierarchie von Funktionsaufrufen, die auf den Abschluss ihrer untergeordneten Elemente warten.

Für das Samplingereignis erhöht der Profiler die *exklusive* Samplinganzahl der Funktion, die gerade die Anweisungen ausführt. Da ein exklusives Sampling auch Teil der gesamten (*inklusiven*) Samplings der Funktion ist, wird die inklusive Samplinganzahl der aktuell aktiven Funktion auch erhöht.

 Der Profiler erhöht die inklusive Samplinganzahl aller anderen Funktionen in der Aufrufliste.

## <a name="inclusive-samples"></a>Inklusive Samplinganzahl

Die Gesamtanzahl der Samplings, die während der Ausführung der Zielfunktion erfasst werden.

Dies umfasst Samplings, die während der direkten Ausführung des Funktionscodes erfasst werden, und Samples, die während der Ausführung von untergeordneten Funktionen erfasst werden, die von der Zielfunktion aufgerufen werden.

## <a name="exclusive-samples"></a>Exklusive Samplinganzahl

Die Anzahl der Samplings, die während der direkten Ausführung der Anweisungen der Zielfunktion erfasst werden.

Exklusive Samplings beinhalten keine Samplings, die während der Ausführung von Funktionen erfasst werden, die von der Zielfunktion aufgerufen werden.

## <a name="inclusive-percent"></a>Inklusive Samplings in Prozent

Der prozentuale Anteil der Gesamtanzahl inklusiver Samplings in der Profilerstellungsausführung, die inklusive Samplings der Funktion oder des Datenbereichs sind.

## <a name="exclusive-percent"></a>Exklusive Samplings in Prozent

Der prozentuale Anteil der Gesamtanzahl exklusiver Samplings in der Profilerstellungsausführung, die exklusive Samplings der Funktion oder des Datenbereichs sind.

## <a name="see-also"></a>Siehe auch

[Vorgehensweise: Auswählen von Sammlungsmethoden](../profiling/how-to-choose-collection-methods.md)
[Analysieren der durch Leistungstools erstellten Daten](../profiling/analyzing-performance-tools-data.md)