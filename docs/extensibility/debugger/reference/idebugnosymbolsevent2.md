---
title: IDebugNoSymbolsEvent2 | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugNoSymbolsEvent2 interface
ms.assetid: f6fb6388-47f6-4385-9ad5-95d62f9a7592
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0850f043d763077ef9a33ad35e82ad924574b6d8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56721315"
---
# <a name="idebugnosymbolsevent2"></a>IDebugNoSymbolsEvent2
Signalisiert dem [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] debugger-Benutzeroberfläche auf den Benutzer zu warnen, dass die Symbole für die gestartete ausführbare Datei nicht gefunden.

## <a name="syntax"></a>Syntax

```
IDebugNoSymbolsEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>Hinweise für Implementierer
 Von der Debug-Engines implementiert und von der [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] debugger-Benutzeroberfläche.

## <a name="requirements"></a>Anforderungen
 Header: Msdbg.h

 Namespace: Microsoft.VisualStudio.Debugger.Interop

 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll