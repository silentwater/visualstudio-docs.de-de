---
title: Protokollierung in MSBuild | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- msbuild, logging
ms.assetid: 9aea2e76-8f60-4234-913d-598e7bbad808
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 99bbb6ba880ace8b21ae6b6009ee84cffee79485
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56618730"
---
# <a name="logging-in-msbuild"></a>Protokollierung in MSBuild
Durch die Protokollierung können Sie den Status eines Builds nachverfolgen. Die Protokollierung erfasst Buildereignisse, Benachrichtigungen, Warnungen und Fehler in einer Protokolldatei.

## <a name="in-this-section"></a>In diesem Abschnitt
- [Erhalten von Buildprotokollen](../msbuild/obtaining-build-logs-with-msbuild.md)

 Beschreibt die verschiedenen Aspekte der Protokollierung in [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)].

- [Buildprotokollierungen](../msbuild/build-loggers.md)

 Erläutert die erforderlichen Schritte zum Erstellen einer Protokollierung mit einem Prozessor.

- [Protokollierung in einer Multiprozessorumgebung](../msbuild/logging-in-a-multi-processor-environment.md)

 Beschreibt, wie die Protokollierung in einer Umgebung mit mehreren Prozessoren und zwei Multiprozessor-Protokollierungsmodellen funktioniert.

- [Schreiben von multiprozessorfähigen Protokollierungen](../msbuild/writing-multi-processor-aware-loggers.md)

 Beschreibt, wie Sie multiprozessorfähige Protokollierungen erstellen und wie ConfigurableForwardingLogger verwendet wird.

- [Erstellen von Weiterleitungsprotokollierungen](../msbuild/creating-forwarding-loggers.md)

 Erläutert, wie Sie benutzerdefinierte Weiterleitungsprotokollierungen erstellen.

## <a name="see-also"></a>Siehe auch
- Unter [Paralleles Erstellen von mehreren Projekten mit MSBuild](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md) wird beschrieben, wie mehrere Projekte schneller erstellt werden können, indem Sie sie parallel ausführen.