---
title: CallTarget-Aufgabe | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- CallTarget task [MSBuild]
- MSBuild, CallTarget task
ms.assetid: bb1fe2c4-4383-436f-8326-c24cc4a46150
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6594620051675f2c0ce6e06ca098d26e443f624b
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56617235"
---
# <a name="calltarget-task"></a>CallTarget-Aufgabe
Ruft die angegebenen Ziele in der Projektdatei ab.

## <a name="task-parameters"></a>Aufgabenparameter
 In der folgenden Tabelle werden die Parameter der `CallTarget` -Aufgabe beschrieben.


| Parameter | Beschreibung |
|---------------------------| - |
| `RunEachTargetSeparately` | Optionaler `Boolean`-Eingabeparameter.<br /><br /> Wenn `true`, wird die [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]-Engine einmal pro Ziel aufgerufen. Wenn `false`, wird die [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]-Engine einmal aufgerufen, um alle Ziele zu erstellen. Der Standardwert ist `false`sein. |
| `TargetOutputs` | Optionaler <xref:Microsoft.Build.Framework.ITaskItem>`[]` -Ausgabeparameter.<br /><br /> Enthält die Ausgaben aller erstellten Ziele. |
| `Targets` | Optionaler `String[]` -Parameter.<br /><br /> Gibt das Ziel oder die Ziele an, die erstellt werden sollen. |
| `UseResultsCache` | Optionaler `Boolean` -Parameter.<br /><br /> Wenn `true`, wird das zwischengespeicherte Ergebnis zurückgegeben, sofern es vorhanden ist.<br /><br /> **Hinweis** Wenn eine MSBuild-Aufgabe ausgeführt wird, wird deren Ausgabe in einem Gültigkeitsbereich als eine Liste von Buildelementen zwischengespeichert (ProjectFileName, GlobalProperties)[TargetNames]. |

## <a name="remarks"></a>Anmerkungen
 Wenn ein in `Targets` angegebenes Ziel fehlschlägt und `RunEachTargetSeparately` `true` ist, fährt die Aufgabe mit dem Erstellen der verbleibenden Ziele fort.

 Wenn Sie die Standardziele erstellen möchten, verwenden Sie die [MSBuild-Aufgabe](../msbuild/msbuild-task.md), und legen Sie den `Projects`-Parameter auf `$(MSBuildProjectFile)` fest.

 Zusätzlich zu den oben aufgeführten Parametern erbt diese Aufgabe Parameter von der <xref:Microsoft.Build.Tasks.TaskExtension>-Klasse, die selbst von der <xref:Microsoft.Build.Utilities.Task>-Klasse erbt. Eine Liste mit diesen zusätzlichen Parametern und ihren Beschreibungen finden Sie unter [TaskExtension-Basisklasse](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Beispiel
 Über das folgende Beispiel wird `TargetA` in `CallOtherTargets` aufgerufen.

```xml
<Project DefaultTargets="CallOtherTargets"
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">

    <Target Name="CallOtherTargets">
        <CallTarget Targets="TargetA"/>
    </Target>

    <Target Name="TargetA">
        <Message Text="Building TargetA..." />
    </Target>

</Project>
```

## <a name="see-also"></a>Siehe auch
- [Referenz zu MSBuild-Tasks](../msbuild/msbuild-task-reference.md)
- [Ziele](../msbuild/msbuild-targets.md)