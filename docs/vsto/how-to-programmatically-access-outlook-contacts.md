---
title: 'Vorgehensweise: Programmgesteuertes Zugreifen auf Outlook-Kontakte'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- contacts [Office development in Visual Studio], searching
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: c46df4218a12c0f9a155567aeee0c007d0a19c53
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56598205"
---
# <a name="how-to-programmatically-access-outlook-contacts"></a>Vorgehensweise: Programmgesteuertes Zugreifen auf Outlook-Kontakte
  Dieses Beispiel ermittelt alle Kontakte, deren Nachname eine angegebene Suchzeichenfolge enthalten.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>Beispiel
 [!code-csharp[Trin_OL_AccessContacts#1](../vsto/codesnippet/CSharp/Trin_OL_AccessContacts.trin_ol_accesscontacts/thisaddin.cs#1)]
 [!code-csharp[Trin_OL_AccessContacts#1](../vsto/codesnippet/CSharp/Trin_OL_AccessContacts.trin_ol_accesscontacts/thisaddin.cs#1)]
 [!code-vb[Trin_OL_AccessContacts#1](../vsto/codesnippet/VisualBasic/Trin_OL_AccessContacts/thisaddin.vb#1)]

## <a name="compile-the-code"></a>Kompilieren des Codes
 Für dieses Beispiel benötigen Sie Folgendes:

-   Kontakte, deren Nachname die Zeichenfolge enthalten "**Na"** (z. B. Tzipi Butnaru) in der **Kontakte** Ordner.

## <a name="see-also"></a>Siehe auch
- [Arbeiten mit Kontaktelementen](../vsto/working-with-contact-items.md)
- [Vorgehensweise: Programmgesteuertes Hinzufügen eines Eintrags zu Outlook-Kontakten](../vsto/how-to-programmatically-add-an-entry-to-outlook-contacts.md)
- [Vorgehensweise: Programmgesteuertes Suchen eines bestimmten Kontakts](../vsto/how-to-programmatically-search-for-a-specific-contact.md)
- [Vorgehensweise: Suchen Sie programmgesteuert eine e-Mail-Adresse in den Kontakten](../vsto/how-to-programmatically-search-for-an-e-mail-address-in-contacts.md)
- [Vorgehensweise: Programmgesteuertes Löschen von Outlook-Kontakten](../vsto/how-to-programmatically-delete-outlook-contacts.md)
