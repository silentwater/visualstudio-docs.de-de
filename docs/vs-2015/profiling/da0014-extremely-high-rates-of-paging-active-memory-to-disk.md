---
title: 'DA0014: Äußerst hohes Maß an Paging von aktivem Speicher auf den Datenträger | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.rules.DAMemoryBound
- vs.performance.DA0014
- vs.performance.14
- vs.performance.rules.DA0014
ms.assetid: a7fa3749-9191-437a-9331-9d917181e62f
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 124f640fd5bf049280638408b4b6101e24e8c58b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54784437"
---
# <a name="da0014-extremely-high-rates-of-paging-active-memory-to-disk"></a>DA0014: Äußerst hohes Maß an Paging von aktivem Speicher auf den Datenträger
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Regel-Id | DA0014 |  
| Kategorie | Speicher und Auslagerung |  
| Profilerstellungsmethode | Alle |  
| Nachricht | Ein sehr hohes Maß an paging von aktivem Speicher auf den Datenträger wurde festgestellt. Die Anwendung ist möglicherweise speichergebunden.|  
| Regeltyp | Warnung |  
  
 Wenn Sie Profile mithilfe der Sampling-, .NET-Arbeitsspeicher- oder Ressourcenkonfliktmethode Profile erstellen, müssen mindestens 25 Samplings erfasst werden, damit diese Regel ausgelöst wird.  
  
## <a name="cause"></a>Ursache  
 Die bei der Profilerstellung erfassten Systemleistungsdaten deuten darauf hin, dass während der Profilerstellung ein sehr hohes Maß an Auslagerungen von aktivem Speicher auf den Datenträger (und umgekehrt) aufgetreten ist. Solch hohe Auslagerungsraten wirken sich in der Regel negativ auf Leistung und Reaktionszeit der Anwendung aus. Verringern Sie ggf. die Speicherbelegungen, indem Sie die Algorithmen überarbeiten. Sie müssen möglicherweise auch die Speicheranforderungen der Anwendung berücksichtigen. Wiederholen Sie ggf. die Profilerstellung auf einem Computer mit einem größeren Arbeitsspeicher aus.  
  
## <a name="rule-description"></a>Regelbeschreibung  
 Eine übermäßige Auslagerung auf den Datenträger kann auf einen zu kleinen physischen Speicher zurückzuführen sein. Wenn der physische Datenträger, auf dem sich die Auslagerungsdatei befindet, hauptsächlich für Auslagerungsvorgänge verwendet wird, kann dies zu einer Verlangsamung anderer anwendungsorientierter Datenträgervorgänge auf diesem Datenträger führen.  
  
 Seiten werden häufig in Massenauslagerungsvorgängen vom Datenträger gelesen oder auf den Datenträger geschrieben. Die Anzahl der geänderten Seiten pro Sekunde ist häufig deutlich größer als beispielsweise die Anzahl der Seiten-Schreibvorgänge pro Sekunde. Der Grund hierfür ist, dass die geänderten Seiten pro Sekunde auch geänderte Datenseiten aus dem Systemdateicache beinhalten. ist jedoch nicht immer einfach, den direkt für die Auslagerung verantwortlichen Prozess oder den Grund für die Auslagerung zu ermitteln.  
  
> [!NOTE]
>  Diese Regel wird ausgelöst, wenn die Auslagerung des aktiven Speichers eine sehr hohe Rate erreicht. Wenn das Maß der Auslagerung erheblich, aber nicht extrem ist, wird die Informationsregel [DA0017: Hohes Maß an paging von aktivem Speicher auf den Datenträger von](../profiling/da0017-high-rates-of-paging-active-memory-to-disk.md) stattdessen ausgelöst.  
  
## <a name="how-to-fix-violations"></a>Behandeln von Verstößen  
 Doppelklicken Sie auf die Meldung im Fenster „Fehlerliste“, um zur Ansicht [Markierungen](../profiling/marks-view.md) zu navigieren. Suchen Sie die Spalte **Arbeitsspeicher\Seiten/s**. Überprüfen Sie, ob die Auslagerung von E/A-Aktivitäten in bestimmten Phasen der Programmausführung besonders häufig auftritt.  
  
 Wenn Sie in einem Auslastungstest-Szenario Profildaten für eine ASP.NET-Anwendung erfassen, führen Sie den Auslastungstest auf einem Computer mit zusätzlichem physischem Speicher (oder RAM) erneut aus.  
  
 Verringern Sie ggf. die Speicherbelegungen, indem Sie die Algorithmen überarbeiten, und vermeiden Sie speicherintensive APIs wie String.Concat und String.Substring.
