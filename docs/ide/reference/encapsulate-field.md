---
title: Refactoring eines Felds in eine Eigenschaft
ms.date: 01/26/2018
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- vs.csharp.refactoring.encapsulatefield
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 9030fd2ae85d12760d6f6a12be54492f3c14e12b
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2019
ms.locfileid: "55911273"
---
# <a name="encapsulate-a-field-refactoring"></a>Refactoring des Kapselns eines Felds

Dieses Refactoring gilt für:

- C#

- Visual Basic

**Beschreibung:** Sie können ein Feld in eine Eigenschaft umwandeln und alle Verwendungen dieses Felds auf die neu erstellte Eigenschaft aktualisieren.

**Hintergrund:** Sie möchten ein Feld in eine Eigenschaft verschieben und alle Verweise auf dieses Feld aktualisieren.

**Vorteile**: Sie möchten anderen Klassen Zugriff auf ein Feld gewähren, die Klassen sollen aber nicht direkt zugreifen können.  Indem Sie das Feld mit einer Eigenschaft umschließen, können Sie z.B. Code schreiben, um den Wert zu überprüfen, der zugewiesen wird.

## <a name="how-to"></a>Vorgehensweise

1. Markieren Sie den Namen des zu kapselnden Felds, oder platzieren Sie den Textcursor in den Namen:

   - C#:

       ![Hervorgehobener Code – C#](media/encapsulate-highlight-cs.png)

   - Visual Basic:

       ![Hervorgehobener Code – Visual Basic](media/encapsulate-highlight-vb.png)

2. Führen Sie dann eine der folgenden Aktionen aus:

   - **Tastatur**
      - Drücken Sie **STRG+R** und dann **STRG+E**.  (Beachten Sie, dass Ihre Tastenkombination je nach dem gewählten Profil möglicherweise abweicht.)
      - Drücken Sie an einer beliebigen Stelle in einer Zeile **STRG**+**.**, um das Menü **Schnellaktionen und Refactorings** aufzurufen, und wählen Sie im Popupvorschaufenster einen der Einträge für **Feld kapseln** aus.
   - **Maus**
      - Wählen Sie **Bearbeiten > Umgestalten > Feld kapseln** aus.
      - Klicken Sie mit der rechten Maustaste auf den Code, wählen Sie das Menü **Schnellaktionen und Refactorings** aus, und wählen Sie im Popupvorschaufenster einen der Einträge für **Feld kapseln** aus.

   Auswahl | Beschreibung
   --------- | -----------
   **Feld kapseln (und Eigenschaft verwenden)** | Kapselt das Feld mit einer Eigenschaft und aktualisiert alle Verwendungen des Felds so, dass die generierte Eigenschaft verwendet wird.
   **Feld kapseln (Feld jedoch weiterhin verwenden)** | Kapselt das Feld mit einer Eigenschaft, lässt aber alle Verwendungen des Felds unverändert.

   Die Eigenschaft wird erstellt, und sofern ausgewählt, werden Verweise auf das Feld aktualisiert.

   > [!TIP]
   > Verwenden Sie den Link **Vorschau der Änderungen** im Popupfenster, um [vor einer endgültigen Änderung das Ergebnis zu sehen](../../ide/preview-changes.md).

   - C#:

      ![Ergebnis vom Kapseln der Eigenschaft – C#](media/encapsulate-result-cs.png)

   - Visual Basic:

      ![Ergebnis vom Kapseln der Eigenschaft – Visual Basic](media/encapsulate-result-vb.png)

## <a name="see-also"></a>Siehe auch

- [Refactoring](../refactoring-in-visual-studio.md)
- [Vorschau der Änderungen](../../ide/preview-changes.md)