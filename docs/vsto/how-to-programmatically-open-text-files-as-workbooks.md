---
title: 'Vorgehensweise: Programmgesteuertes Öffnen von Textdateien als Arbeitsmappen'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks, opening text files as
- text [Office development in Visual Studio], text files
- text files, opening as workbooks
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 8d53c21247e18f198fdac1c22a3b38c0bc5348b6
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56633914"
---
# <a name="how-to-programmatically-open-text-files-as-workbooks"></a>Vorgehensweise: Programmgesteuertes Öffnen von Textdateien als Arbeitsmappen
  Sie können eine Textdatei als eine Arbeitsmappe öffnen. Sie müssen den Namen der Textdatei übergeben, die Sie öffnen möchten. Sie können verschiedene optionale Parameter, wie z. B. die Zeilennummer, zu starten, die Analyse und die Spaltenformat der Daten in der Datei angeben.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="example"></a>Beispiel
 [!code-csharp[Trin_VstcoreExcelAutomation#80](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#80)]
 [!code-vb[Trin_VstcoreExcelAutomation#80](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#80)]

## <a name="compile-the-code"></a>Kompilieren des Codes
 In diesem Beispiel muss die folgenden Komponenten:

-   Eine durch Trennzeichen getrennte Textdatei mit dem Namen `Test.txt` , die in den letzten drei Zeilen Text enthält.

-   Die Textdatei `Test.txt` auf Laufwerk c gespeichert werden

## <a name="see-also"></a>Siehe auch
- [Arbeiten mit Arbeitsmappen](../vsto/working-with-workbooks.md)
- [Vorgehensweise: Programmgesteuertes Öffnen von Arbeitsmappen](../vsto/how-to-programmatically-open-workbooks.md)
- [Vorgehensweise: Programmgesteuertes Erstellen neuer Arbeitsmappen](../vsto/how-to-programmatically-create-new-workbooks.md)
- [Vorgehensweise: Programmgesteuertes Speichern von Arbeitsmappen](../vsto/how-to-programmatically-save-workbooks.md)
- [Vorgehensweise: Programmgesteuertes Schließen von Arbeitsmappen](../vsto/how-to-programmatically-close-workbooks.md)
- [Optionaler Parameter in Office-Projektmappen](../vsto/optional-parameters-in-office-solutions.md)
