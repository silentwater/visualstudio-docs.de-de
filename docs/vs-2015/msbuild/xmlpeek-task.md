---
title: XmlPeek-Aufgabe | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- XmlPeek task [MSBuild]
- MSBuild, XmlPeek task
ms.assetid: 19196031-a3bc-41b5-9c4a-f2572630e179
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: fc39cde1a332e925f998a67ed261346320f18a3c
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2019
ms.locfileid: "54787794"
---
# <a name="xmlpeek-task"></a>XmlPeek-Aufgabe
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Gibt die Werte wie von der XPath-Abfrage angegeben aus einer XML-Datei zurück  
  
## <a name="parameters"></a>Parameter  
 In der folgenden Tabelle werden die Parameter der `XmlPeek` -Aufgabe beschrieben.  
  
|Parameter|Beschreibung|  
|---------------|-----------------|  
|`Namespaces`|Optionaler `String` -Parameter.<br /><br /> Gibt die Namespaces für die Präfixe der XPath-Abfrage an|  
|`Query`|Optionaler `String` -Parameter.<br /><br /> Gibt die XPath-Abfrage an|  
|`Result`|Optionaler <xref:Microsoft.Build.Framework.ITaskItem>`[]` -Ausgabeparameter.<br /><br /> Enthält die Ergebnisse, die von dieser Aufgabe zurückgegeben werden|  
|`XmlContent`|Optionaler `String` -Parameter.<br /><br /> Gibt die XML-Eingabe als Zeichenfolge an|  
|`XmlInputPath`|Optionaler <xref:Microsoft.Build.Framework.ITaskItem> -Parameter.<br /><br /> Gibt die XML-Eingabe als Dateipfad an|  
  
## <a name="remarks"></a>Anmerkungen  
 Zusätzlich zu den in der Tabelle aufgeführten Parametern erbt dieser Task Parameter von der <xref:Microsoft.Build.Tasks.TaskExtension>-Klasse, die selbst von der <xref:Microsoft.Build.Utilities.Task>-Klasse erbt. Eine Liste mit diesen zusätzlichen Parametern und ihren Beschreibungen finden Sie unter [TaskExtension Base Class](../msbuild/taskextension-base-class.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Tasks (Aufgaben)](../msbuild/msbuild-tasks.md)   
 [Aufgabenreferenz](../msbuild/msbuild-task-reference.md)
