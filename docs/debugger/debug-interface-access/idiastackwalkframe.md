---
title: IDiaStackWalkFrame | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkFrame interface
ms.assetid: 42d82845-d6f6-4846-9ecd-9dd169216077
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 343c56e3d3175c26900b0cfb4cdc3d816a324404
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56630586"
---
# <a name="idiastackwalkframe"></a>IDiaStackWalkFrame
Stack Kontext zwischen den Aufrufen der verwaltet die [idiaframedata:: Execute](../../debugger/debug-interface-access/idiaframedata-execute.md) Methode.

## <a name="syntax"></a>Syntax

```
IDiaStackWalkFrame : IUnknown
```

## <a name="methods-in-vtable-order"></a>Methoden in Vtable-Reihenfolge
 Die folgende Tabelle zeigt die Methoden der `IDiaStackWalkFrame`.

|Methode|Beschreibung|
|------------|-----------------|
|[IDiaStackWalkFrame::get_registerValue](../../debugger/debug-interface-access/idiastackwalkframe-get-registervalue.md)|Ruft den Wert eines Registers.|
|[IDiaStackWalkFrame::put_registerValue](../../debugger/debug-interface-access/idiastackwalkframe-put-registervalue.md)|Legt den Wert eines Registers.|
|[IDiaStackWalkFrame::readMemory](../../debugger/debug-interface-access/idiastackwalkframe-readmemory.md)|Liest Arbeitsspeicher aus Image an.|
|[IDiaStackWalkFrame::searchForReturnAddress](../../debugger/debug-interface-access/idiastackwalkframe-searchforreturnaddress.md)|Sucht den angegebenen Stapelrahmen für die nächste Funktion Absenderadresse an.|
|[IDiaStackWalkFrame::searchForReturnAddressStart](../../debugger/debug-interface-access/idiastackwalkframe-searchforreturnaddressstart.md)|Sucht den angegebenen Stapelrahmen für eine Absenderadresse an oder in der Nähe der angegebenen Adresse an.|

## <a name="remarks"></a>Anmerkungen
 Diese Schnittstelle wird verwendet, während der Ausführung des Programms zum Lesen und Schreiben von Register als auch auf Speicher zugreifen und Absenderadressen finden.

## <a name="notes-for-callers"></a>Hinweise für Aufrufer
 Die Client-Anwendung implementiert diese Schnittstelle und übergibt eine Instanz der Schnittstelle, die [idiaframedata:: Execute](../../debugger/debug-interface-access/idiaframedata-execute.md) Methode. Die gleiche Instanz dieser Schnittstelle wird wieder verwendet, um den Status der Register bei jedem Aufruf des verwalten die `execute` Methode. Die `execute` Methode verwendet auch diese Schnittstelle, um zu bestimmen, die Rückgabeadresse.

## <a name="requirements"></a>Anforderungen
 Header: Dia2.h

 Bibliothek: diaguids.lib

 DLL: msdia80.dll

## <a name="see-also"></a>Siehe auch
- [Schnittstellen (Debug Interface Access SDK)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaFrameData::execute](../../debugger/debug-interface-access/idiaframedata-execute.md)