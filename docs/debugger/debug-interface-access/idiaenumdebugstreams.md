---
title: IDiaEnumDebugStreams | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumDebugStreams interface
ms.assetid: 611caf4f-7a5f-4aa4-b909-52feeb3cc752
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7b17e79e1bfefd5b6b23695f2f49d694c7148ae0
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 02/21/2019
ms.locfileid: "56645133"
---
# <a name="idiaenumdebugstreams"></a>IDiaEnumDebugStreams
Listet die verschiedenen Debug-Datenströme, die in der Datenquelle enthalten sind.

## <a name="syntax"></a>Syntax

```
IDiaEnumDebugStreams : IUnknown
```

## <a name="methods-in-vtable-order"></a>Methoden in Vtable-Reihenfolge
Die folgende Tabelle zeigt die Methoden der `IDiaEnumDebugStreams`.

|Methode|Beschreibung|
|------------|-----------------|
|[IDiaEnumDebugStreams::get__NewEnum](../../debugger/debug-interface-access/idiaenumdebugstreams-get-newenum.md)|Ruft die `IEnumVARIANT` Version von diesem Enumerator.|
|[IDiaEnumDebugStreams::get_Count](../../debugger/debug-interface-access/idiaenumdebugstreams-get-count.md)|Ruft die Anzahl der Debug-Streams ab.|
|[IDiaEnumDebugStreams::Item](../../debugger/debug-interface-access/idiaenumdebugstreams-item.md)|Ruft eine Debug-Stream mithilfe eines Indexes ab.|
|[IDiaEnumDebugStreams::Next](../../debugger/debug-interface-access/idiaenumdebugstreams-next.md)|Ruft eine angegebene Anzahl von Debug-Streams in der Enumerationsfolge ab.|
|[IDiaEnumDebugStreams::Skip](../../debugger/debug-interface-access/idiaenumdebugstreams-skip.md)|Überspringt eine angegebene Anzahl von Debug-Datenströme in einer Enumerationsfolge.|
|[IDiaEnumDebugStreams::Reset](../../debugger/debug-interface-access/idiaenumdebugstreams-reset.md)|Setzt eine Enumerationsfolge auf den Anfang zurück.|
|[IDiaEnumDebugStreams::Clone](../../debugger/debug-interface-access/idiaenumdebugstreams-clone.md)|Erstellt einen Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.|

## <a name="remarks"></a>Anmerkungen
Der Inhalt der Debug-Streams ist abhängig von der Implementierung und die Datenformate sind nicht dokumentiert.

## <a name="notes-for-callers"></a>Hinweise für Aufrufer
Rufen Sie die [idiasession:: Getenumdebugstreams](../../debugger/debug-interface-access/idiasession-getenumdebugstreams.md) Methode zum Abrufen einer `IDiaEnumDebugStreams` Objekt.

## <a name="example"></a>Beispiel
Dieses Beispiel zeigt, wie Sie auf die verfügbaren Datenströme von dieser Schnittstelle zugreifen. Finden Sie unter den [IDiaEnumDebugStreamData](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md) Schnittstelle für eine Implementierung der `PrintStreamData` Funktion.

```C++
void DumpAllDebugStreams( IDiaSession* pSession)
{
    IDiaEnumDebugStreams* pEnumStreams;

    wprintf(L"\n\n*** DEBUG STREAMS\n\n");
    // Retrieve an enumerated sequence of debug data streams
    if(pSession->getEnumDebugStreams(&pEnumStreams) == S_OK)
    {
        IDiaEnumDebugStreamData* pStream;
        ULONG celt = 0;

        for(; pEnumStreams->Next(1, &pStream, &celt) == S_OK; pStream = NULL)
        {
            PrintStreamData(pStream);
            pStream->Release();
        }
        pEnumStreams->Release();
    }
    else
    {
        wprintf(L"Failed to get any debug streams!\n");
    }
    wprintf(L"\n");
}
```

## <a name="requirements"></a>Anforderungen
Header: Dia2.h

Bibliothek: diaguids.lib

DLL: msdia80.dll

## <a name="see-also"></a>Siehe auch
- [Schnittstellen (Debug Interface Access SDK)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaEnumDebugStreamData](../../debugger/debug-interface-access/idiaenumdebugstreamdata.md)
- [IDiaSession::getEnumDebugStreams](../../debugger/debug-interface-access/idiasession-getenumdebugstreams.md)
