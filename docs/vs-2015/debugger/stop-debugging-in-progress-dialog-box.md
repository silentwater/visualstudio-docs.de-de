---
title: Beenden Sie das Debuggen im Dialogfeld Status | Microsoft-Dokumentation
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.stopnow
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- SQL
- VB
- CSharp
- C++
helpviewer_keywords:
- Stop Debugging in Progress dialog box
ms.assetid: ed7ef49d-e25f-4a4d-9396-9bc7b4143117
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c29754937d3b1ff7f4c44fc87929d84844743387
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58960060"
---
# <a name="stop-debugging-in-progress-dialog-box"></a>Debuggen wird beendet (Dialogfeld)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Dieses Dialogfeld wird angezeigt, wenn vom Debugger versucht wird, eine Debugsitzung zu beenden, der Beendigungsvorgang jedoch einige Zeit dauert. Das Beenden einer Debugsitzung erfolgt normalerweise sehr schnell, sodass dieses Dialogfeld nicht angezeigt wird. Manchmal dauert es jedoch eine Weile, bis alle derzeit debuggten Prozesse getrennt sind. Wenn das Beenden der Sitzung mehrere Sekunden dauert (bzw. ein Fehler beim Trennen auftritt), wird dieses Dialogfeld angezeigt. Bei wiederholtem Auftreten kann dies auf ein internes Problem hindeuten. Nehmen Sie ggf. Kontakt zum Produktsupport auf.  
  
 Sie können entweder warten, bis alle Prozesse getrennt sind und dieses Dialogfeld ausgeblendet wird, oder Sie erzwingen über die Schaltfläche **Jetzt beenden** die sofortige Beendigung.  
  
 **Jetzt beenden**  
 Klicken Sie auf diese Schaltfläche, um die Debugsitzung sofort zu beenden. Mithilfe von **jetzt beenden**wird beendet, anstatt die debuggten Prozesse getrennt. Wenn Sie Systemprozesse debuggen und die Prozesse mit **Jetzt beenden** stoppen, kann es zu unerwarteten und unerwünschten Folgen kommen.  
  
## <a name="see-also"></a>Siehe auch  
 [Debugger Security (Debuggersicherheit)](../debugger/debugger-security.md)   
 [Trennen von Programmen](http://msdn.microsoft.com/f2c756c2-8079-474b-94c2-01c19a141a01)
