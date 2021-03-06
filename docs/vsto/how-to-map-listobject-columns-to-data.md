---
title: 'Vorgehensweise: Zuordnung von ListObject-Spalten zu Daten'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data [Office development in Visual Studio], mapping to ListObject column
- ListObject control, mapping data
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: cf6e693bf216cedf2734d78ca13662739981f235
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56639894"
---
# <a name="how-to-map-listobject-columns-to-data"></a>Vorgehensweise: Zuordnung von ListObject-Spalten zu Daten
  Beim Binden eines <xref:Microsoft.Office.Tools.Excel.ListObject> -Steuerelements an <xref:System.Data.DataTable>sollen möglicherweise nicht alle Spalten in einer Liste angezeigt werden, oder Sie verfügen u. U. über bestimmte Spalten, die nicht an Daten gebunden sind. Durch den Aufruf der <xref:Microsoft.Office.Tools.Excel.ListObject> -Methode können Sie die Spalten zuordnen, die in <xref:Microsoft.Office.Tools.Excel.ListObject.SetDataBinding%2A> angezeigt werden sollen.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 ![Link zum Video](../vsto/media/playvideo.gif "Link zum Video") eine entsprechende Videodemo finden Sie unter [Gewusst wie: Erstellen Sie eine Liste in Excel, die mit einer SharePoint-Liste verbunden ist? ](http://go.microsoft.com/fwlink/?LinkID=130263).

## <a name="map-columns"></a>Zuordnen von Spalten

### <a name="to-map-a-data-table-to-columns-in-a-list"></a>So ordnen Sie eine Datentabelle Spalten in einer Liste zu

1.  Erstellen Sie <xref:System.Data.DataTable> auf Klassenebene.

     [!code-csharp[Trin_VstcoreHostControlsExcel#16](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet3.cs#16)]
     [!code-vb[Trin_VstcoreHostControlsExcel#16](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet3.vb#16)]

2.  Fügen Sie Beispielspalten und Daten in die `Startup` -Ereignishandler von dem `Sheet1` -Klasse (in einem Projekt auf Dokumentebene) oder `ThisAddIn` Klasse (in einem VSTO-Add-in-Projekt).

     [!code-csharp[Trin_VstcoreHostControlsExcel#17](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet3.cs#17)]
     [!code-vb[Trin_VstcoreHostControlsExcel#17](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet3.vb#17)]

3.  Rufen Sie die <xref:Microsoft.Office.Tools.Excel.ListObject.SetDataBinding%2A> -Methode auf, und übergeben Sie die Spaltennamen in der Reihenfolge, in der sie angezeigt werden sollen. Das Listenobjekt gebunden werden wird auf das neu erstellte <xref:System.Data.DataTable>, aber die Reihenfolge der Spalten in der Liste variieren je nach der Reihenfolge der <xref:System.Data.DataTable>.

     [!code-csharp[Trin_VstcoreHostControlsExcel#18](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet3.cs#18)]
     [!code-vb[Trin_VstcoreHostControlsExcel#18](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet3.vb#18)]

## <a name="specify-unmapped-columns"></a>Geben Sie nicht zugeordnete Spalten
 Beim Zuordnen von Spalten zu <xref:System.Data.DataTable>können Sie auch angeben, dass bestimmte Spalten nicht an Daten gebunden werden sollen, indem Sie eine leere Zeichenfolge übergeben. In diesem Fall wird dem <xref:Microsoft.Office.Tools.Excel.ListObject> -Steuerelement eine neue Spalte hinzugefügt, die nicht an Daten gebunden ist.

### <a name="to-specify-an-unmapped-column-when-mapping-listobject-columns"></a>So geben Sie beim Zuordnen von ListObject-Spalten eine nicht zugeordnete Spalte an

1.  Rufen Sie die <xref:Microsoft.Office.Tools.Excel.ListObject.SetDataBinding%2A> -Methode auf, und übergeben Sie die Spaltennamen in der Reihenfolge, in der sie angezeigt werden sollen. Verwenden Sie eine leere Zeichenfolge, um anzugeben, wo eine nicht zugeordnete Spalte hinzugefügt wird: in diesem Fall zwischen der Spalte für den Titel und der Spalte für den Nachnamen.

     [!code-csharp[Trin_VstcoreHostControlsExcel#19](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet3.cs#19)]
     [!code-vb[Trin_VstcoreHostControlsExcel#19](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet3.vb#19)]

## <a name="compile-the-code"></a>Kompilieren des Codes
 In diesem Codebeispiel wird davon ausgegangen, dass Sie in dem Arbeitsblatt, in dem dieser Code angezeigt wird, über ein <xref:Microsoft.Office.Tools.Excel.ListObject> namens `list1` verfügen.

## <a name="see-also"></a>Siehe auch
- [Erweitern von Word-Dokumenten und Excel-Arbeitsmappen in VSTO-Add-ins zur Laufzeit](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Steuerelemente für Office-Dokumente](../vsto/controls-on-office-documents.md)
- [Hinzufügen von Steuerelementen zu Office-Dokumenten zur Laufzeit](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Vorgehensweise: Füllen Sie ListObject-Steuerelementen mit Daten.](../vsto/how-to-fill-listobject-controls-with-data.md)
- [Automatisieren von Excel mithilfe von erweiterten Objekten](../vsto/automating-excel-by-using-extended-objects.md)
- [ListObject-Steuerelement](../vsto/listobject-control.md)
