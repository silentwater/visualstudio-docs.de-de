---
title: 'CA1900: Werttypfelder sollten portabel sein | Microsoft-Dokumentation'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1900
- ValueTypeFieldsShouldBePortable
helpviewer_keywords:
- ValueTypeFieldsShouldBePortable
- CA1900
ms.assetid: 1787d371-389f-4d39-b305-12b53bc0dfb9
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 35bdef10d63f79c3d1ff649a486a708c34b28078
ms.sourcegitcommit: 3201da3499051768ab59f492699a9049cbc5c3c6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2019
ms.locfileid: "59001839"
---
# <a name="ca1900-value-type-fields-should-be-portable"></a>CA1900: Werttypfelder sollten portabel sein.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Die neueste Dokumentation zu Visual Studio finden Sie unter [CA1900: Werttypfelder sollten portabel sein](https://docs.microsoft.com/visualstudio/code-quality/ca1900-value-type-fields-should-be-portable) auf docs.microsoft.com.  
  
|||  
|-|-|  
|TypeName|ValueTypeFieldsShouldBePortable|  
|CheckId|CA1900|  
|Kategorie|Microsoft.Portability|  
|Unterbrechende Änderung|Unterbrechend – Wenn das Feld außerhalb der Assembly angezeigt werden.<br /><br /> Nicht unterbrechend – Wenn das Feld nicht außerhalb der Assembly sichtbar ist.|  
  
## <a name="cause"></a>Ursache  
 Diese Regel überprüft, dass mit explizitem Layout deklarierten Strukturen korrekt, beim Marshallen an nicht verwalteten Code auf 64-Bit-Betriebssystemen ausgerichtet werden. IA-64 lässt nicht korrekt ausgerichteten Speicher zugreift und der Prozess stürzt ab, wenn diese Verletzung nicht behoben wurde.  
  
## <a name="rule-description"></a>Regelbeschreibung  
 Strukturen mit explizitem Layout, das falsch ausgerichtete Felder verursachen auf 64-Bit-Betriebssystemen Systemabstürze enthält.  
  
## <a name="how-to-fix-violations"></a>Behandeln von Verstößen  
 Müssen alle Felder, die kleiner als 8 Bytes, Offsets, die ein Vielfaches von ihrer Größe und Felder, die 8 Bytes sind, oder benötigen mehr Offsets, die ein Vielfaches von 8 sind. Eine andere Lösung ist die Verwendung `LayoutKind.Sequential` anstelle von `LayoutKind.Explicit`, bei Bedarf.  
  
## <a name="when-to-suppress-warnings"></a>Wann sollten Warnungen unterdrückt werden?  
 Nur, wenn Fehler auftreten, sollte diese Warnung unterdrückt werden.
