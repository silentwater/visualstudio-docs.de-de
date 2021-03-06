---
title: 'Vorgehensweise: Programmgesteuertes Anwenden von Formaten auf Bereiche in Arbeitsmappen'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ranges, styles
- styles, workbook ranges
- workbooks, styles
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 178d5c22c74386cb70ced170b8643baeedfab55e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56607966"
---
# <a name="how-to-programmatically-apply-styles-to-ranges-in-workbooks"></a>Vorgehensweise: Programmgesteuertes Anwenden von Formaten auf Bereiche in Arbeitsmappen
  Sie können benannte Formatvorlagen auf Bereiche in Arbeitsmappen anwenden. Excel stellt eine Reihe von vordefinierten Formaten bereit.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Das Dialogfeld **Zellen formatieren** zeigt alle Optionen an, die Sie zum Formatieren von Zellen verwenden können, und jede dieser Optionen ist aus Ihrem Code verfügbar. Klicken Sie zum Anzeigen dieses Dialogfelds in Excel im Menü **Format** auf **Zellen** .

## <a name="to-apply-a-style-to-a-named-range-in-a-document-level-customization"></a>So wenden Sie eine Formatvorlage auf einen benannten Bereich in einer Anpassung auf Dokumentebene an

1.  Erstellen eine neue Formatvorlage, und legen Sie ihre Attribute fest.

     [!code-csharp[Trin_VstcoreExcelAutomation#53](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#53)]
     [!code-vb[Trin_VstcoreExcelAutomation#53](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#53)]

2.  Erstellen Sie eine <xref:Microsoft.Office.Tools.Excel.NamedRange>-Steuerelement, weisen Sie diesem Text zu, und wenden Sie dann die neue Formatvorlage an. Dieser Code muss in einer Sheet-Klasse platziert werden und nicht in der `ThisWorkbook` -Klasse.

     [!code-csharp[Trin_VstcoreExcelAutomation#54](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#54)]
     [!code-vb[Trin_VstcoreExcelAutomation#54](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#54)]

## <a name="to-clear-a-style-from-a-named-range-in-a-document-level-customization"></a>So löschen Sie eine Formatvorlage aus einem benannten Bereich in einer Anpassung auf Dokumentebene

1.  Wenden Sie die Formatvorlage "NORMAL.DOT" auf den Bereich an. Dieser Code muss in einer Sheet-Klasse platziert werden und nicht in der `ThisWorkbook` -Klasse.

     [!code-csharp[Trin_VstcoreExcelAutomation#55](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#55)]
     [!code-vb[Trin_VstcoreExcelAutomation#55](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#55)]

## <a name="to-apply-a-style-to-a-named-range-in-a-vsto-add-in"></a>So wenden Sie eine Formatvorlage auf einen benannten Bereich in einem VSTO-Add-In an

1.  Erstellen eine neue Formatvorlage, und legen Sie ihre Attribute fest.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#28](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#28)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#28](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#28)]

2.  Erstellen Sie einen <xref:Microsoft.Office.Interop.Excel.Range>, weisen Sie diesem Text zu, und wenden Sie dann die neue Formatvorlage an.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#29](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#29)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#29](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#29)]

## <a name="to-clear-a-style-from-a-named-range-in-a-vsto-add-in"></a>So löschen Sie eine Formatvorlage aus einem benannten Bereich in einem VSTO-Add-in

1.  Wenden Sie die Formatvorlage "NORMAL.DOT" auf den Bereich an.

     [!code-csharp[Trin_VstcoreExcelAutomation#56](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#56)]
     [!code-vb[Trin_VstcoreExcelAutomation#56](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#56)]

## <a name="see-also"></a>Siehe auch
- [Arbeiten mit Bereichen](../vsto/working-with-ranges.md)
- [NamedRange-Steuerelement](../vsto/namedrange-control.md)
- [Globaler Zugriff auf Objekte in Office-Projekten](../vsto/global-access-to-objects-in-office-projects.md)
- [Optionaler Parameter in Office-Projektmappen](../vsto/optional-parameters-in-office-solutions.md)
