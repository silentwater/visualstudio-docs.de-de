---
title: 'Vorgehensweise: Erstellen von Zuordnungen zwischen Typen (Klassen-Designer) | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- vs.classdesigner.associationline
helpviewer_keywords:
- types [Visual Studio], associations
- association lines, defining (Class Designer)
- defining association lines (Class Designer)
- associations, types
- association lines
ms.assetid: adccb9c8-2f8a-4086-9fa9-f70f99fb6e00
caps.latest.revision: 24
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 8a1126427a1454ec09f0460cb9da1eb65fb72b31
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "54764797"
---
# <a name="how-to-create-associations-between-types-class-designer"></a>Gewusst wie: Erstellen von Zuordnungen zwischen Typen (Klassen-Designer)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Anhand von Assoziationslinien im Klassen-Designer ist zu erkennen, in welcher Beziehung Klassen in einem Diagramm stehen. Eine Assoziationslinie stellt eine Klasse dar, die der Typ einer Eigenschaft oder eines Felds einer anderen Klasse im Projekt ist. In der Regel dienen Assoziationslinien zur Darstellung der wichtigsten Beziehungen zwischen Klassen im Projekt.  
  
 Sie können alle Felder und Eigenschaften als Assoziationen anzuzeigen. Je nachdem, welche Elemente im Diagramm hervorgehoben werden sollen, ist jedoch sinnvoller, nur wichtige Member als Assoziationen anzeigen. (Sie können weniger wichtige Member als reguläre Member anzeigen oder alle ausblenden.)  
  
> [!NOTE]
>  Der Klassen-Designer unterstützt nur Assoziationen in eine Richtung.  
  
### <a name="to-define-an-association-line-in-the-class-diagram"></a>So definieren Sie im Klassendiagramm eine Assoziationslinie  
  
1.  Wählen Sie in der Toolbox unter „Klassen-Designer“ die Option **Zuordnung** aus.  
  
2.  Zeichnen Sie eine Linie zwischen den beiden Formen, die Sie mithilfe einer Assoziation miteinander verbinden möchten.  
  
     In der ersten Klasse wird eine neue Eigenschaft erstellt. Diese Eigenschaft wird als Assoziationslinie (nicht als Eigenschaft in einem Depot in der Form) mit einem Standardnamen angezeigt. Der zugehörige Typ ist die Form, auf die die Assoziationslinie weist.  
  
### <a name="to-change-the-name-of-an-association"></a>So ändern Sie den Namen einer Assoziation  
  
- Klicken Sie auf der Diagrammoberfläche auf die Bezeichnung der Assoziationslinie, und geben Sie eine neue Bezeichnung ein.  
  
  \- oder –  
  
1.  Klicken Sie auf die Form, in der die als Assoziation angezeigte Eigenschaft enthalten ist.  
  
     Die Form erhält den Fokus, und die zugehörigen Member werden im Klassendetailsfenster und im Eigenschaftenfenster angezeigt.  
  
2.  Bearbeiten Sie nun entweder im Klassendetailsfenster oder im Eigenschaftenfenster das Namensfeld der Eigenschaft, und drücken Sie die EINGABETASTE.  
  
     Der Name wird im Fenster **Klassendetails**, auf der Assoziationslinie, im Eigenschaftenfenster und im Code aktualisiert.  
  
## <a name="see-also"></a>Siehe auch  
 [Gewusst wie: Wechseln zwischen Member- und Zuordnungsnotation (Klassen-Designer)](../ide/how-to-change-between-member-notation-and-association-notation-class-designer.md)
