---
title: Erwartet ']' im regulären Ausdruck (JavaScript) | Microsoft-Dokumentation
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5019
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 1ca2079a-44dd-479f-a1e3-e04a14d0739e
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 377bdd6b09c9f25b759d6bf1df2d93e9bd412be5
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "56839814"
---
# <a name="expected--in-regular-expression-javascript"></a>Im regulären Ausdruck wurde ']' erwartet (JavaScript)
Sie haben versucht, eine Zeichenklasse für die Übereinstimmung eines regulären Ausdrucks zu erstellen, aber Sie hat keine die schließenden Klammer. Einzelne Literalzeichen Kombinationen können zu Zeichenklassen in regulären Ausdrücken zusammengefügt werden, Ausschnitte in Klammern aufgerufen wird. Eine Zeichenklasse entspricht einem beliebigen Zeichen, die, das Sie enthält. Z. B. / [Abc] / entspricht einem beliebigen Buchstaben "a", "b" oder "c".  
  
### <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Fügen Sie der schließenden Klammer des regulären Ausdrucks ein.  
  
    > [!NOTE]
    >  Sie können eine einzelne Klammer entsprechend mit Escapezeichen versehen sie mit einem umgekehrten Schrägstrich - \\[–, damit es nicht als Sonderzeichen von interpretiert wird [!INCLUDE[javascript](../../javascript/includes/javascript-md.md)].  
  
## <a name="see-also"></a>Siehe auch  
 [Regular Expression-Objekt](../../javascript/reference/regular-expression-object-javascript.md)   
 [Syntax für reguläre Ausdrücke (JavaScript)](https://msdn.microsoft.com/library/1400241x)