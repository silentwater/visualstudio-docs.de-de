---
title: PROGRAM_DESTROY_FLAGS | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- PROGRAM_DESTROY_FLAGS enumeration
ms.assetid: be00d4a3-d5b8-4159-b632-64577f534883
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e232570edd4fcca95089324e30f3cbd725bdb9f8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685611"
---
# <a name="programdestroyflags"></a>PROGRAM_DESTROY_FLAGS
Listet die gültigen Werte des Programms zerstört Flags.

## <a name="syntax"></a>Syntax

```cpp
enum enum_PPROGRAM_DESTROY_FLAGS
{
   PROGRAM_DESTROY_CONTINUE_DEBUGGING = 0x1
};
typedef DWORD PROGRAM_DESTROY_FLAGS;
```

```csharp
public enum enum_PPROGRAM_DESTROY_FLAGS
{
   PROGRAM_DESTROY_CONTINUE_DEBUGGING = 0x1
};
```

## <a name="terms"></a>Begriffe
 Zerstören von PROGRAM_DESTROY_CONTINUE_DEBUGGING programmieren, aber mit dem Debuggen fortfahren.

## <a name="remarks"></a>Hinweise
 Die Enumeration zurückgegeben wird, durch die [GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md) Methode.

## <a name="requirements"></a>Anforderungen
 Header: Msdbg.h

 Namespace: Microsoft.VisualStudio.Debugger.Interop

 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Siehe auch
- [Enumerationen](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md)