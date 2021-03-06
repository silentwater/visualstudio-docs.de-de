---
title: Enumeratorobjekt erwartet | Microsoft-Dokumentation
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5015
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: dc6e32c1-a6e6-4e12-ac99-e3f65f91c8d7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 14fcb4d990b03a8e7b896014403eb8dceac66b80
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "56841830"
---
# <a name="enumerator-object-expected"></a>Enumerator-Objekt erwartet
Sie haben versucht, rufen Sie die **Enumerator.prototype.atEnd, Enumerator.prototype.item, Enumerator.prototype.moveFirst,** oder **Enumerator.prototype.moveNext** Methode für ein Objekt eines anderen Typs als `Enumerator`. Das Objekt dieser Art von Aufruf muss vom Typ `Enumerator`. Hier ist ein Beispiel für Code, der mit dieser Regel wird ein:  
  
```JavaScript  
var o = new Object;  
o.f = Enumerator.prototype.atEnd;  
o.f();  
```  
  
### <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Rufen Sie nur die **Enumerator.prototype.atEnd**, **Enumerator.prototype.item**, **Enumerator.prototype.moveFirst**, oder  **Enumerator.prototype.moveNext** Methoden für Objekte vom Typ `Enumerator`. Um zu ermitteln, ob das Objekt ist ein `Enumerator` -Objekts:  
  
    ```js
    if(x instanceof Enumerator)  
    ```  
  
## <a name="see-also"></a>Siehe auch  
 [Enumeratorobjekt](../../javascript/reference/enumerator-object-javascript.md)