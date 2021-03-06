---
title: Generieren einer Dekonstruktorschnellaktion
ms.date: 02/19/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 8887f4cd6b4dcd7f08e808f1271f5d546d6a224c
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "58159178"
---
# <a name="generate-a-deconstructor-in-visual-studio"></a>Generieren eines Dekonstruktors in Visual Studio

Diese Codegenerierung gilt für:

- C#

**Beschreibung:** Hiermit können Sie sofort den Methodenstub für einen neuen Dekonstruktor generieren.

**Hintergrund:** Wenn Sie Ihren Typ automatisch ordnungsgemäß dekonstruieren möchten.

**Vorteile**: Sie können einen Dekonstruktor manuell schreiben, mit diesem Feature wird der Stub jedoch mit den richtigen Out-Parametern für Sie generiert.

## <a name="generate-deconstructor"></a>Generieren eines Dekonstruktors

1. Deklarieren Sie einen neuen Typ mit den gewünschten Out-Parametern. Diese Deklaration löst einen Fehler aus, wenn keine Dekonstruktionsinstanz gefunden wird, die mit Ihrer Deklaration übereinstimmt.

   ![Fehler: fehlender Dekonstruktor](media/deconstruct.png)

2. Gehen Sie als Nächstes wie folgt vor:

   - **Tastatur**
      - Drücken Sie mit dem Cursor in der Deklaration **STRG**+**.**, um das Menü **Schnellaktionen und Refactorings** aufzurufen.
   - **Maus**
      - Führen Sie einen Rechtsklick durch, und klicken Sie auf das Menü **Schnellaktionen und Refactorings**.
      - Klicken Sie auf die Schaltfläche ![Schraubendrehersymbol](media/screwdriver.png) das am linken Rand angezeigt wird, sofern der Textcursor bereits in der leeren Zeile in der Klasse platziert wurde.

      ![Codefix zum Generieren eines Dekonstruktors](media/deconstruct-codefix.png)

3. Klicken Sie auf **Generate method 'MyInternalClass.Deconstruct'** (Methode „MyInternalClass.Deconstruct“ generieren), um den Dekonstruktor zu generieren.

   ![Resultierender Dekonstruktorcode](media/deconstruct-result.png)


## <a name="see-also"></a>Siehe auch

- [Codegenerierung](../code-generation-in-visual-studio.md)
- [Vorschau der Änderungen](../../ide/preview-changes.md)
- [Tipps für .NET-Entwickler](../../ide/visual-studio-2017-for-dotnet-developers.md)