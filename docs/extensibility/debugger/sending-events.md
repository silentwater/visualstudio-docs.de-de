---
title: Senden von Ereignissen | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], sending events
ms.assetid: 064231e7-59b5-4437-8240-a23c0a7ec2a9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cd282dd38d322a5b7d9821406d30a303fabb02bb
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685065"
---
# <a name="send-events"></a>Senden von Ereignissen
Der Mechanismus für die Kommunikation zwischen dem Debugger und die Debug-Engine (DE) ist eine auf DCOM basierende Ereignismodell. Ereignisse werden als COM-Objekte gesendet, und jedes Ereignis verfügt über Parameter, die angeben:

- Die DE, die das Ereignis aufgerufen.

- Eine Beschreibung des was passiert ist.

- Der Prozess, Anwendung und Threadinformationen, identifiziert der Kontext, in dem das Ereignis aufgetreten ist. Der Prozess wird nicht für Ereignisse, die von einer bereitgestellten Kompatibilitätsrichtlinie gesendeten gesendet.

- Der Ereignistyp, der angibt, ob das Ereignis synchron oder asynchron ist.

  Alle Debug-Ereignisse gesendet werden, mithilfe der Methode [IDebugEventCallback2::Event](../../extensibility/debugger/reference/idebugeventcallback2-event.md).

## <a name="in-this-section"></a>In diesem Abschnitt
 [Ereignisquellen](../../extensibility/debugger/event-sources-visual-studio-sdk.md) wird erläutert, die zwei Quellen von Ereignissen: die Debug-Engine (DE) und die Sitzung debug-Manager (SDM).

 [Unterstützte Ereignistypen](../../extensibility/debugger/supported-event-types.md) wird erläutert, die derzeit unterstützten Ereignistypen: asynchrone und synchrone.

 [Ereignisbeschreibungen](../../extensibility/debugger/event-descriptions.md) definiert, Ereignisse und die Gründe für deren Verwendung.

## <a name="related-sections"></a>Verwandte Abschnitte
 [Erstellen einer benutzerdefinierten Debug-Engine](../../extensibility/debugger/creating-a-custom-debug-engine.md) beschreibt die Funktionsweise einer bereitgestellten Kompatibilitätsrichtlinie mit den Interpreter Betriebssystem oder Debugdienste bereit.