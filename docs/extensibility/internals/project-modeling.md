---
title: Projekt Modellierung | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- automation [Visual Studio SDK], implementing project objects
- project models, automation
ms.assetid: c8db8fdb-88c1-4b12-86fe-f3c30a18f9ee
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3a2ae395d94d76fd2b11de33cc6d5053d8b92432
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56633433"
---
# <a name="project-modeling"></a>Projektmodellierung
Der nächste Schritt im Bereitstellen von Automatisierung für Ihr Projekt ist, um die standard-Projekt-Objekte zu implementieren: die <xref:EnvDTE.Projects> und `ProjectItems` Auflistungen; die `Project` und <xref:EnvDTE.ProjectItem> Objekte und die übrigen Objekte, die für Ihre Implementierung eindeutig. Diese standard-Objekte werden in Dteinternal.h-Datei definiert. Eine Implementierung der standardmäßigen Objekte wird im Beispiel BscPrj bereitgestellt. Sie können diese Klassen als Modelle verwenden, um Ihre eigenen Objekte für die standard-Projekt zu erstellen, die Seite-an-Seite zu stehen mit Projektobjekten aus anderen Projekttypen.

 Setzt voraus, dass ein automatisierungsbenutzer aufrufen können <xref:EnvDTE.Solution>("`<UniqueProjName>")` und <xref:EnvDTE.ProjectItems> (`n`), wobei n ist eine Indexnummer für ein bestimmtes Projekt in der Lösung abrufen. Dieses Automation-Aufruf führt dazu, dass die Umgebung Aufrufen <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.GetProperty%2A> auf den entsprechenden Projekthierarchie übergeben VSITEMID_ROOT als Element-ID-Parameter und VSHPROPID_ExtObject: VSHPROPID-Parameter. `IVsHierarchy::GetProperty` Gibt eine `IDispatch` Zeiger auf die Bereitstellung der Hauptfunktionen der Automatisierungsobjekt `Project` -Schnittstelle, die Sie implementiert haben.

 Im folgenden finden Sie die Syntax der `IVsHierarchy::GetProperty`.

 `HRESULT GetProperty (`

 `VSITEMID` `itemid`,

 `VSHPROPID` `propid`,

 `VARIANT` `*pvar`

 `);`

 Projekte Schachtelung aufzunehmen, und Verwenden von Sammlungen zum Erstellen von Gruppen von Projektelementen. Die Hierarchie sieht wie folgt aus.

```
Projects
  |- Project
      |- ProjectItems (a collection of ProjectItem)
          |- ProjectItem (single object) or ProjectItems (another collection)
```

 Schachteln bedeutet, dass eine <xref:EnvDTE.ProjectItem> Objekt kann es sich <xref:EnvDTE.ProjectItems> Auflistung gleichzeitig da eine `ProjectItems` Sammlung kann die geschachtelten Objekte enthalten. Im Beispiel Basic-Projekts wird diese Schachtelung nicht veranschaulicht. Durch die Implementierung der `Project` -Objekts können Sie teilnehmen, in der Baumstruktur, das den Entwurf des allgemeinen Automatisierungsmodells bestimmt.

 Die Projekt-Automatisierung folgt den Pfad in der folgenden Abbildung.

 ![Visual Studio-Projektobjekten](../../extensibility/internals/media/projectobjects.gif "ProjectObjects") Websiteprojektautomatisierung

 Wenn Sie nicht implementieren eine `Project` Objekt ist, wird die Umgebung weiterhin einen generischen zurück `Project` -Objekt, das nur den Namen des Projekts enthält.

## <a name="see-also"></a>Siehe auch
- <xref:EnvDTE.Projects>
- <xref:EnvDTE.ProjectItem>
- <xref:EnvDTE.ProjectItems>