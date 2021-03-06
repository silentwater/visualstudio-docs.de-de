---
title: 'Vorgehensweise: Suchen nach einem Thread in der Ansicht "Threads" | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- threads, searching
ms.assetid: 5609a9b3-c279-4426-9e2e-dd87896a6d6f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 665633047a37a9f219306e2baaa874a37c9344ea
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689563"
---
# <a name="how-to-search-for-a-thread-in-threads-view"></a>Gewusst wie: Suchen nach einem Thread in der Threadansicht
Sie können mithilfe der Thread-ID oder eine Modul-Zeichenfolge als Suchkriterium für einen bestimmten Thread in der Ansicht "Threads" suchen. Sie können auch die anfangsrichtung für die Suche angeben. Die Felder im Dialogfeld werden die Attribute des ausgewählten Threads in der Threadstruktur angezeigt werden.

### <a name="to-search-for-a-thread-in-threads-view"></a>Suchen Sie nach einem Thread in der Ansicht "Threads"

1. Ordnen Sie die Fenster also, Spy++ und ein aktiver [Ansicht "Threads"](../debugger/threads-view.md) Fenster sichtbar sind.

2. Von der **Suche** Menü wählen **Thread suchen**.

    Die [Dialogfeld Threadsuche](../debugger/thread-search-dialog-box.md) wird geöffnet.

3. Geben Sie die Thread-ID oder eine Modulzeichenfolge als Suchkriterium an.

4. Deaktivieren Sie alle Felder, die für die Sie keine Werte angeben möchten.

   > [!TIP]
   >  Um alle Threads, die im Besitz von einem Modul zu suchen, deaktivieren Sie die **Thread** nennen Sie das Textfeld, und geben das Modul die **Modul** Feld. Verwenden Sie dann **Weitersuchen** für Threads Suche fort.

5. Wählen Sie **einrichten** oder **unten** für die anfängliche Richtung für die Suche.

6. Klicken Sie auf **OK**.

   Wenn ein entsprechender Thread gefunden wird, wird es in der Threads an hervorgehoben.