---
title: 'Vorgehensweise: Erstellen von bestimmten Zielen in Projektmappen mit MSBuild.exe | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
helpviewer_keywords:
- MSBuild, building specific targets in a solution
- msbuild.exe, building specific targets in a solution
- MSBuild, msbuild.exe
ms.assetid: f46feb9b-4c16-4fec-b6e1-36a959692ba3
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 85c8f3dcb9364c2837cd4d10f163de3795821ce7
ms.sourcegitcommit: 4d9c54f689416bf1dc4ace058919592482d02e36
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "58194229"
---
# <a name="how-to-build-specific-targets-in-solutions-by-using-msbuildexe"></a>Gewusst wie: Erstellen von bestimmten Zielen in Projektmappen mit MSBuild.exe
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Sie können MSBuild.exe verwenden, um bestimmte Ziele von bestimmten Projekten in einer Projektmappe zu erstellen.  
  
### <a name="to-build-a-specific-target-of-a-specific-project-in-a-solution"></a>So erstellen Sie ein bestimmtes Ziel von einem bestimmten Projekt in einer Projektmappe.  
  
1.  Geben Sie in der Befehlszeile `MSBuild.exe <SolutionName>.sln` ein, bei der `<SolutionName>` dem Dateinamen der Projektmappe entspricht, die das Ziel enthält, das Sie ausführen möchten.  
  
2.  Geben Sie das Ziel nach dem **/t**-Schalter im Format *ProjektName*:*ZielName* an.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel führt das Ziel `Rebuild` des Projekts `NotInSlnFolder` aus und führt anschließend das Ziel `Clean` des Projekts `InSolutionFolder` aus, das im Projektmappenordner `NewFolder` ist .  
  
```  
msbuild SlnFolders.sln /t:NotInSlnfolder:Rebuild;NewFolder\InSolutionFolder:Clean  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Befehlszeilenreferenz](../msbuild/msbuild-command-line-reference.md)   
 [MSBuild Reference](../msbuild/msbuild-reference.md)  (MSBuild-Referenz)  
 [MSBuild](msbuild.md)  
 [MSBuild-Grundlagen](../msbuild/msbuild-concepts.md)
