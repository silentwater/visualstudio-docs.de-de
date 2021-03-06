---
title: FormatUrl-Aufgabe | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, FormatUrl task
- FormatUrl task [MSBuild]
ms.assetid: 81114b67-520f-43b5-8891-224f68a78516
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e6c8bc23a843112a234dad0dfc718937bebfe5aa
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56629884"
---
# <a name="formaturl-task"></a>FormatUrl-Aufgabe
Konvertiert eine URL in ein gültiges URL-Format

## <a name="parameters"></a>Parameter
 In der folgenden Tabelle werden die Parameter der `FormatUrl` -Aufgabe beschrieben.

|Parameter|Beschreibung|
|---------------|-----------------|
|`InputUrl`|Optionaler `String` -Parameter.<br /><br /> Gibt die zu formatierende URL an|
|`OutputUrl`|Optionaler `String`-Ausgabeparameter.<br /><br /> Gibt die formatierte URL an|

## <a name="remarks"></a>Anmerkungen
 Zusätzlich zu den in der Tabelle aufgeführten Parametern erbt dieser Task Parameter von der <xref:Microsoft.Build.Tasks.TaskExtension>-Klasse, die selbst von der <xref:Microsoft.Build.Utilities.Task>-Klasse erbt. Eine Liste mit diesen zusätzlichen Parametern und ihren Beschreibungen finden Sie unter [TaskExtension-Basisklasse](../msbuild/taskextension-base-class.md).

## <a name="see-also"></a>Siehe auch
- [Aufgaben](../msbuild/msbuild-tasks.md)
- [Referenz zu MSBuild-Tasks](../msbuild/msbuild-task-reference.md)