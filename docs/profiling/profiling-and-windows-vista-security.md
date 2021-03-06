---
title: Profilerstellung und Sicherheit in Windows Vista | Microsoft-Dokumentation
ms.date: 11/02/2018
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools,security
- performance tools, security
ms.assetid: 842112fc-b886-4801-8cd7-a25b314b0393
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 091961f3425714c0dc5ddabfac847c76339ab064
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55025565"
---
# <a name="profiling-and-windows-vista-security"></a>Profilerstellung und Sicherheit in Windows Vista

Je nach [!INCLUDE[wiprlhext](../debugger/includes/wiprlhext_md.md)]-Einstellungen für die Benutzerzugriffsberechtigung, die ein Administrator zur Verfügung gestellt hat, kann ein einzelner Benutzer über die Sicherheitsberechtigung zur Profilerstellung eines Prozesses auf dem Computer verfügen. Die folgenden Beispiele veranschaulichen mögliche Unterschiede zwischen Benutzern:

- Einige Benutzer können auf erweiterte Profilerstellungsfeatures zugreifen, wenn der Administrator Treiber und Dienst gestartet hat.

- Domänenbenutzer können nur auf Beispiel-Profilerstellung zugreifen.

- Einige Benutzer können den Zugriff auf die Profilerstellung für alle anderen Benutzer verweigern.

  Weitere Informationen finden Sie unter den ADMIN-Optionen in [VSPerfCmd](../profiling/vsperfcmd.md).

## <a name="cross-session-profiling"></a>Sitzungsübergreifende Profilerstellung

*Sitzungsübergreifende Profilerstellung* ist die Möglichkeit, ein Profil für einen Prozess zu erstellen, der in einer anderen Benutzersitzung ausgeführt wird. Die meisten Dienste werden z.B. in Sitzung 0 ausgeführt, und Benutzer können nicht direkt in Sitzung 0 ausgeführt werden. Mithilfe der Schaltfläche **An den Prozess anhängen** auf der Leistungs-Explorer-Symbolleiste oder mithilfe der `/attach`-Option vom Befehlszeilentool VSPerfCmd können Sie Profile für die meisten Prozesse in unterschiedlichen Benutzersitzungen erstellen.

Sie können eine Liste der Prozesse ansehen, die durch Festlegen der Sichtbarkeitsoptionen der prozessübergreifenden Profilerstellung verfügbar sind. Diese Optionen stehen im Fenster **An den Prozess anhängen** zur Verfügung. Dieses Fenster wird angezeigt, wenn Sie **An den Prozess anhängen** auswählen:

- **Prozesse aller Benutzer anzeigen**

  Wenn diese Option nicht ausgewählt ist, zeigt die Liste nur die Prozesse an, die dem aktuellen Benutzer gehören. Andernfalls zeigt die Liste Prozesse aller Benutzer an.

- **Prozesse in allen Sitzungen anzeigen**

  Wenn diese Option nicht ausgewählt ist, zeigt die Liste Prozesse in der aktuellen Sitzung an. Andernfalls zeigt die Liste Prozesse in allen Sitzungen an.

## <a name="see-also"></a>Siehe auch

- [Übersichten](../profiling/overviews-performance-tools.md)
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Vorgehensweise: Anfügen an einen laufenden Prozess](/previous-versions/visualstudio/visual-studio-2010/c6wf8e4z\(v\=vs.100\))
