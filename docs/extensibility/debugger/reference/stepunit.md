---
title: STEPUNIT | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- STEPUNIT
helpviewer_keywords:
- STEPUNIT enumeration
ms.assetid: cb8441f2-f744-4e73-acfe-ae8542df9649
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0f1d6742b28badf39a5c9273d2891c2da9a9d5f0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56712124"
---
# <a name="stepunit"></a>STEPUNIT
Gibt die Schrittweite für die schrittweise Ausführung.

## <a name="syntax"></a>Syntax

```cpp
enum enum_STEPUNIT { 
   STEP_STATEMENT   = 0,
   STEP_LINE        = 1,
   STEP_INSTRUCTION = 2
};
typedef DWORD STEPUNIT;
```

```csharp
enum enum_STEPUNIT { 
   STEP_STATEMENT   = 0,
   STEP_LINE        = 1,
   STEP_INSTRUCTION = 2
};
```

## <a name="members"></a>Member
 STEP_STATEMENT Schritte von-Anweisung.

 STEP_LINE-Schritte nach Zeile.

 STEP_INSTRUCTION Schritte nach Anweisung.

## <a name="remarks"></a>Hinweise
 Übergeben als Argument an die [Schritt](../../../extensibility/debugger/reference/idebugprocess3-step.md) Methode.

## <a name="requirements"></a>Anforderungen
 Header: msdbg.h

 Namespace: Microsoft.VisualStudio.Debugger.Interop

 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Siehe auch
- [Enumerationen](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [Step](../../../extensibility/debugger/reference/idebugprocess3-step.md)