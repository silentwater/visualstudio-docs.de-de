---
title: 'DA0502: Maximale CPU-Auslastung durch den Prozess, für den die Profilerstellung ausgeführt wird | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.rules.DA0502
- vs.performance.DA0502
- vs.performance.502
ms.assetid: 1ee53df5-b0dc-4265-9d4f-527830d08725
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a47a9c5964ccf15d2c609233eb600f39bc3ad2d1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54787354"
---
# <a name="da0502-maximum-cpu-consumption-by-the-process-being-profiled"></a>DA0502: Maximale CPU-Auslastung durch den Prozess, für den die Profilerstellung ausgeführt wird
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Regel-Id | DA0502 |  
| Kategorie | Ressourcenüberwachung |  
| Profilerstellungsmethode | Alle |  
| Nachricht | Diese Regel dient nur zu Informationszwecken. Der Leistungsindikator für die Process()\\%-Prozessorzeit dient zum Messen der CPU-Auslastung des Prozesses, für den die Profilerstellung ausgeführt wird. Bei dem gemeldeten Wert handelt es sich um den Maximalwert aus allen Messintervallen.|  
| Regeltyp | Nur zu Informationszwecken |  
  
 Wenn Sie Profile mithilfe der Sampling-, .NET-Arbeitsspeicher- oder Ressourcenkonfliktmethode Profile erstellen, müssen mindestens 10 Samplings erfasst werden, damit diese Regel ausgelöst wird.  
  
## <a name="rule-description"></a>Regelbeschreibung  
 In dieser Meldung wird der maximale Prozentsatz der Zeit angegeben, die ein Prozessor mit dem Ausführen von Anweisungen aus der Anwendung beschäftigt war. Bei dem gemeldeten Wert handelt es sich um den Maximalwert aller Messintervalle, in denen der Prozess, dessen Profil erstellt wird, aktiv war. Bei einem Computer mit mehreren Prozessoren kann der Prozentsatz 100 Prozent übersteigen.  
  
## <a name="how-to-use-the-rule-data"></a>Verwenden der Regeldaten  
 Mithilfe des Regelwerts können Sie die Leistung anderer Versionen oder Builds des Programms vergleichen oder die Leistung der Anwendung in unterschiedlichen Profilerstellungsszenarios nachvollziehen.
