---
title: MODULE_INFO_FIELDS | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MODULE_INFO_FIELDS
helpviewer_keywords:
- MODULE_INFO_FIELDS enumeration
ms.assetid: 8bed85f4-235f-4192-b58f-5fad7a4d7a78
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f4302a911e58a23bdcd58bb054c1fc90c389fed6
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56708382"
---
# <a name="moduleinfofields"></a>MODULE_INFO_FIELDS
Gibt die Flags für die Debuginformationen für das Modul an.

## <a name="syntax"></a>Syntax

```cpp
enum enum_MODULE_INFO_FIELDS { 
   MIF_NONE              = 0x0000,
   MIF_NAME              = 0x0001,
   MIF_URL               = 0x0002,
   MIF_VERSION           = 0x0004,
   MIF_DEBUGMESSAGE      = 0x0008,
   MIF_LOADADDRESS       = 0x0010,
   MIF_PREFFEREDADDRESS  = 0x0020,
   MIF_SIZE              = 0x0040,
   MIF_LOADORDER         = 0x0080,
   MIF_TIMESTAMP         = 0x0100,
   MIF_URLSYMBOLLOCATION = 0x0200,
   MIF_FLAGS             = 0x0400,
   MIF_ALLFIELDS         = 0x07ff
};
typedef DWORD MODULE_INFO_FIELDS;
```

```csharp
public enum enum_MODULE_INFO_FIELDS { 
   MIF_NONE              = 0x0000,
   MIF_NAME              = 0x0001,
   MIF_URL               = 0x0002,
   MIF_VERSION           = 0x0004,
   MIF_DEBUGMESSAGE      = 0x0008,
   MIF_LOADADDRESS       = 0x0010,
   MIF_PREFFEREDADDRESS  = 0x0020,
   MIF_SIZE              = 0x0040,
   MIF_LOADORDER         = 0x0080,
   MIF_TIMESTAMP         = 0x0100,
   MIF_URLSYMBOLLOCATION = 0x0200,
   MIF_FLAGS             = 0x0400,
   MIF_ALLFIELDS         = 0x07ff
};
```

## <a name="members"></a>Member
 MIF_NONE initialisieren/verwenden keines der Felder in der Struktur.

 MIF_NAME initialisieren und Verwenden der `m_bstrName` -Feld in der [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) Struktur.

 MIF_URL initialisieren und Verwenden der `m_bstrUrl` -Feld in der `MODULE_INFO` Struktur.

 MIF_VERSION initialisieren und Verwenden der `m_bstrVersion` -Feld in der `MODULE_INFO` Struktur.

 MIF_DEBUGMESSAGE initialisieren und Verwenden der `m_bstrDebugMessage` -Feld in der `MODULE_INFO` Struktur.

 MIF_LOADADDRESS initialisieren und Verwenden der `m_addrLoadAddress` -Feld in der `MODULE_INFO` Struktur.

 MIF_PREFFEREDADDRESS initialisieren und Verwenden der `m_addrPreferredLoadAddress` -Feld in der `MODULE_INFO` Struktur.

 MIF_SIZE initialisieren und Verwenden der `m_dwSize` -Feld in der `MODULE_INFO` Struktur.

 MIF_LOADORDER initialisieren und Verwenden der `m_dwLoadOrder` -Feld in der `MODULE_INFO` Struktur.

 MIF_TIMESTAMP initialisieren und Verwenden der `m_TimeStamp` -Feld in der `MODULE_INFO` Struktur.

 MIF_URLSYMBOLLOCATION initialisieren und Verwenden der `m_bstrUrlSymbolLocation` -Feld in der `MODULE_INFO` Struktur.

 MIF_FLAGS initialisieren und Verwenden der `m_dwModuleFlags` -Feld in der `MODULE_INFO` Struktur.

 MIF_ALLFIELDS initialisieren/verwenden alle Felder in der `MODULE_INFO` Struktur.

## <a name="remarks"></a>Hinweise
 Diese Werte werden übergeben, als Argument an die [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md) Methode, um die Felder anzugeben der [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) sind, dass die Struktur initialisiert werden.

 Diese Werte werden auch verwendet, der `MODULE_INFO` Struktur, um anzugeben, welche Felder verwendet und gültig sind.

 Diese Flags können kombiniert werden, mit einer bitweisen `OR`.

## <a name="requirements"></a>Anforderungen
 Header: msdbg.h

 Namespace: Microsoft.VisualStudio.Debugger.Interop

 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Siehe auch
- [Enumerationen](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugmodule2-getinfo.md)