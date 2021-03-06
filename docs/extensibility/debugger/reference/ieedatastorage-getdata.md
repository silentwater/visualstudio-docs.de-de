---
title: IEEDataStorage::GetData | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEEDataStorage::GetData
helpviewer_keywords:
- IEEDataStorage::GetData
ms.assetid: 4d384039-73d4-40b4-ace6-a2474c546397
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0b6dbf712fc21338f8f5c4699ca2e11d5344dbad
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56693749"
---
# <a name="ieedatastoragegetdata"></a>IEEDataStorage::GetData
Ruft die angegebene Anzahl von Bytes aus dem Objekt ab.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetData(
   ULONG  dataSize,
   ULONG* sizeGotten,
   BYTE*  data
);
```

```csharp
int GetData(
   uint     dataSize,
   out uint sizeGotten,
   byte[]   data
);
```

#### <a name="parameters"></a>Parameter
 `dataSize`

 [in] Die Anzahl der abzurufenden Bytes (der `data` Array muss mindestens diese Anzahl von Bytes enthalten).

 `sizeGotten`

 [out] Gibt die Anzahl der Bytes, die tatsächlich abgerufen.

 `data`

 [in, out] Ein Array mit den angeforderten Daten gefüllt werden soll.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird `S_OK`ist, andernfalls ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise
 Die empfohlene Verwendung dieser Methode ist die Datenbytes in ein lokales Array, abrufen, da es keine Möglichkeit, zu der Bytes während des Abfrageprozesses überspringen. In diesem Fall ist der Parameter `dataSize` zurückgegeben werden soll der Wert durch die [GetSize](../../../extensibility/debugger/reference/ieedatastorage-getsize.md) Methode.

## <a name="see-also"></a>Siehe auch
- [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)
- [GetSize](../../../extensibility/debugger/reference/ieedatastorage-getsize.md)