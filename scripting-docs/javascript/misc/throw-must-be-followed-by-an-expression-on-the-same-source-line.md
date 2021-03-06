---
title: Throw muss durch einen Ausdruck in derselben Quellzeile folgen | Microsoft-Dokumentation
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT1035
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: b03b7747-01a1-40c6-af80-a1dd70bc5781
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5d2989b2ebb5cf0095736d5667f85a807558c495
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "56841142"
---
# <a name="throw-must-be-followed-by-an-expression-on-the-same-source-line"></a>Auf 'throw' muss ein Ausdruck in derselben Quellzeile folgen
Sie verwendet die `throw` -Schlüsselwort, aber nicht es mit einem Ausdruck in derselben Quellzeile folgen. Ein `throw` Anweisung besteht aus zwei Teilen: dem `throw` -Schlüsselwort, gefolgt von dem Ausdruck, der ausgelöst wird. Zum Beispiel:  
  
```JavaScript  
if (denominator == 0) {  
 throw new DivideByZeroException();  
}  
```  
  
 Sie können nicht diese beiden Komponenten aufgeteilt.  
  
### <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Stellen Sie sicher, dass die `throw` -Schlüsselwort und der Ausdruck, der ausgelöst werden, die in der gleichen Zeile angezeigt wird.  
  
## <a name="see-also"></a>Siehe auch  
 [Error-Objekt](../../javascript/reference/error-object-javascript.md)   
 [Throw-Anweisung](../../javascript/reference/throw-statement-javascript.md)   
 [try...catch...finally-Anweisung](../../javascript/reference/try-dot-dot-dot-catch-dot-dot-dot-finally-statement-javascript.md)