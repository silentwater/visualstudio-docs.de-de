---
title: FIELD_KIND | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- FIELD_KIND
helpviewer_keywords:
- FIELD_KIND enumeration
ms.assetid: fd522b9c-52e2-42fa-939d-343347d5c3b1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 46b965def820771b0bab883c1bdd9bf90d18414e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56680373"
---
# <a name="fieldkind"></a>FIELD_KIND
Gibt die Art des Feld in einer [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) Objekt.

## <a name="syntax"></a>Syntax

```cpp
enum enum_FIELD_KIND {
    FIELD_KIND_NONE       = 0x00000000,

    // Type of field
    FIELD_KIND_TYPE       = 0x00000001,
    FIELD_KIND_SYMBOL     = 0x00000002,

    // Storage type of the field
    FIELD_TYPE_PRIMITIVE  = 0x00000010,
    FIELD_TYPE_STRUCT     = 0x00000020,
    FIELD_TYPE_CLASS      = 0x00000040,
    FIELD_TYPE_INTERFACE  = 0x00000080,
    FIELD_TYPE_UNION      = 0x00000100,
    FIELD_TYPE_ARRAY      = 0x00000200,
    FIELD_TYPE_METHOD     = 0x00000400,
    FIELD_TYPE_BLOCK      = 0x00000800,
    FIELD_TYPE_POINTER    = 0x00001000,
    FIELD_TYPE_ENUM       = 0x00002000,
    FIELD_TYPE_LABEL      = 0x00004000,
    FIELD_TYPE_TYPEDEF    = 0x00008000,
    FIELD_TYPE_BITFIELD   = 0x00010000,
    FIELD_TYPE_NAMESPACE  = 0x00020000,
    FIELD_TYPE_MODULE     = 0x00040000,
    FIELD_TYPE_DYNAMIC    = 0x00080000,
    FIELD_TYPE_PROP       = 0x00100000,
    FIELD_TYPE_INNERCLASS = 0x00200000,
    FIELD_TYPE_REFERENCE  = 0x00400000,
    FIELD_TYPE_EXTENDED   = 0x00800000,

    // Specific information about symbols
    FIELD_SYM_MEMBER      = 0x01000000,
    FIELD_SYM_LOCAL       = 0x02000000,
    FIELD_SYM_PARAM       = 0x04000000,
    FIELD_SYM_THIS        = 0x08000000,
    FIELD_SYM_GLOBAL      = 0x10000000,
    FIELD_SYM_PROP_GETTER = 0x20000000,
    FIELD_SYM_PROP_SETTER = 0x40000000,
    FIELD_SYM_EXTENDED    = 0x80000000,

    FIELD_KIND_MASK       = 0x0000000f,
    FIELD_TYPE_MASK       = 0x00fffff0,
    FIELD_SYM_MASK        = 0xff000000,

    FIELD_KIND_ALL        = 0xffffffff
};
typedef DWORD FIELD_KIND;
```

```csharp
public enum enum_FIELD_KIND {
    FIELD_KIND_NONE       = 0x00000000,

    // Type of field
    FIELD_KIND_TYPE       = 0x00000001,
    FIELD_KIND_SYMBOL     = 0x00000002,

    // Storage type of the field
    FIELD_TYPE_PRIMITIVE  = 0x00000010,
    FIELD_TYPE_STRUCT     = 0x00000020,
    FIELD_TYPE_CLASS      = 0x00000040,
    FIELD_TYPE_INTERFACE  = 0x00000080,
    FIELD_TYPE_UNION      = 0x00000100,
    FIELD_TYPE_ARRAY      = 0x00000200,
    FIELD_TYPE_METHOD     = 0x00000400,
    FIELD_TYPE_BLOCK      = 0x00000800,
    FIELD_TYPE_POINTER    = 0x00001000,
    FIELD_TYPE_ENUM       = 0x00002000,
    FIELD_TYPE_LABEL      = 0x00004000,
    FIELD_TYPE_TYPEDEF    = 0x00008000,
    FIELD_TYPE_BITFIELD   = 0x00010000,
    FIELD_TYPE_NAMESPACE  = 0x00020000,
    FIELD_TYPE_MODULE     = 0x00040000,
    FIELD_TYPE_DYNAMIC    = 0x00080000,
    FIELD_TYPE_PROP       = 0x00100000,
    FIELD_TYPE_INNERCLASS = 0x00200000,
    FIELD_TYPE_REFERENCE  = 0x00400000,
    FIELD_TYPE_EXTENDED   = 0x00800000,

    // Specific information about symbols
    FIELD_SYM_MEMBER      = 0x01000000,
    FIELD_SYM_LOCAL       = 0x02000000,
    FIELD_SYM_PARAM       = 0x04000000,
    FIELD_SYM_THIS        = 0x08000000,
    FIELD_SYM_GLOBAL      = 0x10000000,
    FIELD_SYM_PROP_GETTER = 0x20000000,
    FIELD_SYM_PROP_SETTER = 0x40000000,
    FIELD_SYM_EXTENDED    = 0x80000000,

    FIELD_KIND_MASK       = 0x0000000f,
    FIELD_TYPE_MASK       = 0x00fffff0,
    FIELD_SYM_MASK        = 0xff000000,

    FIELD_KIND_ALL        = 0xffffffff
};
```

## <a name="members"></a>Member
FIELD_KIND_TYPE gibt an, dass das Feld nur einen Typ.

FIELD_KIND_SYMBOL gibt an, dass das Feld ein Symbol, mit dem Typ, Name und andere Informationen.

FIELD_TYPE_PRIMITIVE gibt an, dass das Feld ein primitiver Datentyp.

FIELD_TYPE_STRUCT gibt an, dass das Feld eine Struktur ist.

FIELD_TYPE_CLASS gibt an, dass das Feld einer Klasse.

FIELD_TYPE_INTERFACE gibt an, dass das Feld eine Schnittstelle.

FIELD_TYPE_UNION gibt an, dass das Feld eine Union ist.

FIELD_TYPE_ARRAY gibt an, dass das Feld ein Array.

FIELD_TYPE_METHOD gibt an, dass das Feld eine Methode.

FIELD_TYPE_BLOCK gibt an, dass das Feld ein Block ist.

FIELD_TYPE_POINTER gibt an, dass das Feld ein Zeiger ist.

FIELD_TYPE_ENUM gibt an, dass das Feld enumerierten Datentyps.

FIELD_TYPE_LABEL gibt an, dass das Feld eine Bezeichnung.

FIELD_TYPE_TYPEDEF gibt an, dass das Feld eine Typdefinition ist.

FIELD_TYPE_BITFIELD gibt an, dass das Feld ein Bitfeld ist.

FIELD_TYPE_NAMESPACE gibt an, dass das Feld ein Namespace ist.

FIELD_TYPE_MODULE gibt an, dass das Feld ein Modul.

FIELD_TYPE_DYNAMIC gibt an, dass das Feld dynamisch ist.

FIELD_TYPE_PROP gibt an, dass das Feld eine Eigenschaft ist.

FIELD_TYPE_INNERCLASS gibt an, dass das Feld einer inneren Klasse.

FIELD_TYPE_REFERENCE gibt an, dass das Feld ein Verweis ist.

FIELD_TYPE_EXTENDED für zukünftige Verwendung reserviert.

FIELD_SYM_MEMBER gibt an, dass das Feld gehört.

FIELD_SYM_LOCAL gibt an, dass das Feld lokal ist.

FIELD_SYM_PARAMETER gibt an, dass das Feld ein Parameter ist.

FIELD_SYM_THIS gibt an, dass das Feld, das "this"-Zeigers ist.

FIELD_SYM_GLOBAL gibt an, dass das Feld auf global festgelegt ist.

FIELD_SYM_PROP_GETTER gibt an, dass das Feld Eigenschaften abruft.

FIELD_SYM_PROP_SETTER gibt an, dass das Feld Eigenschaften festlegt.

FIELD_SYM_EXTENDED für zukünftige Verwendung reserviert.

FIELD_KIND_MASK gibt eine Maske für Feld Arten an.

FIELD_TYPE_MASK gibt eine Maske für die Feldtypen an.

FIELD_SYM_MASK gibt eine Maske für Symbolinformationen an.

## <a name="remarks"></a>Hinweise
Zurückgegeben von einem Aufruf der [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) Methode.

Je nach Art des Felds [QueryInterface](/cpp/atl/queryinterface) aufgerufen werden kann, auf die [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) Schnittstelle für eine genauere Form der Schnittstelle. Z. B. wenn [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) gibt `FIELD_TYPE_METHOD`, rufen Sie anschließend `QueryInterface` auf ich`DebugField` zum Abrufen der [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md) Schnittstelle.

## <a name="requirements"></a>Anforderungen
Header: sh.h

Namespace: Microsoft.VisualStudio.Debugger.Interop

Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Siehe auch
- [Enumerationen](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md)
- [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
