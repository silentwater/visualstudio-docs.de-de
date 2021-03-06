---
title: T4-Assemblydirektive | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
ms.assetid: 44949749-ce3c-4fb5-8690-a17f1564ac2f
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f81bdcad4f255585c2c554add59ed04dea5872d3
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58960763"
---
# <a name="t4-assembly-directive"></a>T4-Assemblydirektive
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

In einer [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]-Entwurfszeittextvorlage wird mit der `assembly`-Anweisung eine Assembly geladen, damit im Vorlagencode die Typen der Vorlage verwendet werden können. Der Effekt ist mit dem Hinzufügen eines Assemblyverweises in einem [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]-Projekt vergleichbar.  
  
 Eine allgemeine Übersicht über das Schreiben von Textvorlagen finden Sie unter [Schreiben einer T4-Textvorlage](../modeling/writing-a-t4-text-template.md).  
  
> [!NOTE]
>  Die `assembly`-Anweisung ist in einer Laufzeitvorlage (vorverarbeiteten Vorlage) nicht erforderlich. Fügen Sie stattdessen die notwendigen Assemblys hinzu. die **Verweise** von Ihrem [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Projekt.  
  
## <a name="using-the-assembly-directive"></a>Verwenden der Assemblyanweisung  
 Die Syntax der Anweisung lautet wie folgt:  
  
```  
<#@ assembly name="[assembly strong name|assembly file name]" #>  
```  
  
 Folgende Optionen stehen zum Angeben des Assemblynamens zur Verfügung:  
  
- Der starke Name einer Assembly im GAC, z. B. `System.Xml.dll`. Sie können auch das lange Formular verwenden, z. B. `name="System.Xml, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"`. Weitere Informationen finden Sie unter <xref:System.Reflection.AssemblyName>.  
  
- Absoluter Pfad der Assembly  
  
  Sie können mit der `$(variableName)`-Syntax auf [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]-Variablen wie `$(SolutionDir)` und mit `%VariableName%` auf Umgebungsvariablen verweisen. Zum Beispiel:  
  
```  
<#@ assembly name="$(SolutionDir)\MyProject\bin\Debug\SomeLibrary.Dll" #>  
```  
  
 Die assembly-Anweisung hat in einer vorverarbeiteten Textvorlage keinerlei Auswirkungen. Fügen Sie stattdessen die notwendigen Verweise in die **Verweise** Teil Ihrer [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] Projekt. Weitere Informationen finden Sie unter [Run-Time-Textgenerierung mithilfe von T4-Textvorlagen](../modeling/run-time-text-generation-with-t4-text-templates.md).  
  
## <a name="standard-assemblies"></a>Standardassemblys  
 Die folgenden Assemblys werden automatisch geladen, damit Sie keine Assemblyanweisungen dafür schreiben müssen:  
  
- `Microsoft.VisualStudio.TextTemplating.1*.dll`  
  
- `System.dll`  
  
- `WindowsBase.dll`  
  
  Wenn Sie eine benutzerdefinierte Direktive verwenden, lädt der Direktivenprozessor möglicherweise zusätzliche Assemblys. Wenn Sie z. B. Vorlagen für eine domänenspezifische Sprache (DSL) schreiben, müssen Sie keine Assemblyanweisungen für die folgenden Assemblys schreiben:  
  
- `Microsoft.VisualStudio.Modeling.Sdk.1*.dll`  
  
- `Microsoft.VisualStudio.Modeling.Sdk.Diagrams.1*.dsl`  
  
- `Microsoft.VisualStudio.TextTemplating.Modeling.1*.dll`  
  
- Die Assembly mit der DSL.  
  
##  <a name="msbuild"></a> Verwenden von Projekteigenschaften in MSBuild und Visual Studio  
 Visual Studio-Makros wie $ (SolutionDir) funktionieren nicht in MSBuild. Wenn Sie Vorlagen im Buildcomputer transformieren möchten, müssen Sie dies mithilfe von Projekteigenschaften tun.  
  
 Bearbeiten Sie die CSPROJ- oder VBPROJ-Datei, und definieren Sie eine Projekteigenschaft. In folgendem Beispiel wird eine Eigenschaft mit dem Namen `myLibFolder` definiert:  
  
```xml  
<!-- Define a project property, myLibFolder: -->  
<PropertyGroup>  
    <myLibFolder>$(MSBuildProjectDirectory)\..\libs</myLibFolder>  
</PropertyGroup>  
  
<!-- Tell the MSBuild T4 task to make the property available: -->  
<ItemGroup>  
    <T4ParameterValues Include="myLibFolder">  
      <Value>$(myLibFolder)</Value>  
    </T4ParameterValues>  
  </ItemGroup>  
  
```  
  
 Nun können Sie die Projekteigenschaft in Textvorlagen verwenden, die sowohl in Visual Studio als auch in MSBuild ordnungsgemäß transformiert werden:  
  
```  
<#@ assembly name="$(myLibFolder)\MyLib.dll" #>  
```  
  
## <a name="see-also"></a>Siehe auch  
 [T4-Include-Direktive](../modeling/t4-include-directive.md)
