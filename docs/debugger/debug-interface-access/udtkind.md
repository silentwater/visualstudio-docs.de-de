---
title: UdtKind | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- UdtKind enumeration
ms.assetid: 400b59b9-373c-42cb-aae1-570494214328
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 511beae100529f0db555eca0a8ddb995d7a335d1
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56636579"
---
# <a name="udtkind"></a>UdtKind
Beschreibt die verschiedenen benutzerdefinierten Typ (UDT) an.

## <a name="syntax"></a>Syntax

```C++
enum UdtKind {
    UdtStruct,
    UdtClass,
    UdtUnion,
    UdtInterface
};
```

## <a name="elements"></a>Elements
UdtStruct UDT ist eine Struktur.

UdtClass UDT ist eine Klasse.

UdtUnion UDT ist eine Union.

UdtInterface UDT ist eine Schnittstelle.

## <a name="remarks"></a>Anmerkungen
Die Werte in dieser Enumeration werden zurückgegeben, durch die [idiasymbol:: Get_udtkind](../../debugger/debug-interface-access/idiasymbol-get-udtkind.md) Methode.

## <a name="requirements"></a>Anforderungen
Header: cvconst.h

## <a name="see-also"></a>Siehe auch
- [Enumerationen und Strukturen](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaSymbol::get_udtKind](../../debugger/debug-interface-access/idiasymbol-get-udtkind.md)
