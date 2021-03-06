---
title: Remotedebugger – Portzuweisungen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 05/18/2018
ms.topic: reference
ms.assetid: 238bb4ec-bb00-4c2b-986e-18ac278f3959
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 672d54b29e6de9302e88b1b95b4117783b8a0113
ms.sourcegitcommit: 1024f336dcd8e8a4c50b9a9ad8ec85b6e70073a8
ms.translationtype: MTE95
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2019
ms.locfileid: "57699615"
---
# <a name="remote-debugger-port-assignments"></a>Remotedebugger - Portzuweisungen
Der Visual Studio-Remotedebugger kann als Anwendung oder als Hintergrunddienst ausgeführt werden. Bei der Ausführung als Anwendung wird standardmäßig der folgende Port zugewiesen:
::: moniker range=">=vs-2019"
- Visual Studio 2019: 4024
::: moniker-end
- Visual Studio 2017: 4022

- Visual Studio 2015: 4020

- Visual Studio 2013: 4018

- Visual Studio 2012: 4016

  Die Nummer des Ports, der dem Remotedebugger zugewiesen ist, wird also für jede Version um 2 erhöht. Sie können bei Bedarf eine andere Portnummer festlegen. Das Festlegen von Portnummern wird in einem späteren Abschnitt erläutert.

## <a name="the-remote-debugger-port-on-32-bit-operating-systems"></a>Remotedebugger-Port bei 32-Bit-Betriebssystemen

::: moniker range=">=vs-2019"
 TCP 4024 (Visual Studio 2019) ist der Hauptport und für alle Szenarien erforderlich. Sie können ihn über die Befehlszeile oder das Fenster "Remotedebugger" konfigurieren.
::: moniker-end
::: moniker range="vs-2017"
 TCP 4022 (Visual Studio 2017) ist der Hauptport und für alle Szenarien erforderlich. Sie können ihn über die Befehlszeile oder das Fenster "Remotedebugger" konfigurieren.
::: moniker-end

 Klicken Sie im Fenster „Remotedebugger“ auf **Extras > Optionen**, und legen Sie die Nummer für den TCP/IP-Port fest.

 Starten Sie von der Befehlszeile aus den Remotedebugger über die Option **/port**: **msvsmon /port \<Portnummer>**.

 Alle Remotedebugger-Befehlszeilenoptionen finden Sie in der Hilfe zum Remotedebugging (drücken Sie F1, oder klicken Sie im Fenster „Remotedebugger“ auf **Hilfe** > **Verwendung**).

## <a name="the-remote-debugger-port-on-64-bit-operating-systems"></a>Remotedebugger-Port bei 64-Bit-Betriebssystemen
::: moniker range=">=vs-2019"
 Wenn die 64-Bit-Version des Remotedebuggers gestartet wird, verwendet er die Main (4024) standardmäßig port.  Wenn Sie einen 32-Bit-Prozess debuggen, startet die 64-Bit-Version des Remotedebuggers eine 32-Bit-Version des Remotedebuggers über Port 4025 (wichtigsten Port Anzahl um 1 erhöht). Wenn Sie den 32-Bit-Remotedebugger ausführen, wird Port 4024 und nicht Port 4025 verwendet.
::: moniker-end
::: moniker range="vs-2017"
 Wenn die 64-Bit-Version des Remotedebuggers gestartet wird, verwendet er die Main Standardport (4022) standardmäßig.  Wenn Sie einen 32-Bit-Prozess debuggen, startet die 64-Bit-Version des Remotedebuggers eine 32-Bit-Version des Remotedebuggers über Port 4023 (wichtigsten Port Anzahl um 1 erhöht). Wenn Sie den 32-Bit-Remotedebugger ausführen, wird Port 4022 und nicht Port 4023 verwendet.
:::moniker-end

 Dieser Port ist über die Befehlszeile konfigurierbar: **Msvsmon /wow64port \<Portnummer>**.

## <a name="the-discovery-port"></a>Port für die Ermittlung
 UDP 3702 wird für die Suche nach ausgeführten Instanzen des Remotedebuggers im Netzwerk verwendet (z. B. bei **Suchen** im Dialogfeld **An den Prozess anhängen** ). Er wird nur für die Ermittlung von Computern verwendet, auf denen der Remotedebugger ausgeführt wird, und ist daher optional, wenn Sie den Computernamen oder die IP-Adresse des Zielcomputers auf andere Weise ermitteln können. Da dies der Standardport für die Ermittlung ist, kann die Portnummer nicht konfiguriert werden.

 Wenn Sie die Ermittlung nicht aktivieren möchten, können Sie msvsmon von der Befehlszeile aus mit deaktivierter Ermittlung starten:  **msvsmon /nodiscovery**.

## <a name="remote-debugger-ports-on-azure"></a>Remotedebugger-Ports in Azure
 Die folgenden Ports werden vom Remotedebugger in Azure verwendet. Die Ports im Clouddienst werden den Ports auf den einzelnen virtuellen Computern zugeordnet. Bei allen Ports handelt es sich um TCP-Ports.

|Verbindung|Port im Clouddienst|Port auf virtuellem Computer|
|-|-|-|
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.Connector|30400|30398|
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.Forwarder|31400|31398|
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.Forwarderx86|31401|31399|
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.FileUpload|32400|32398|

## <a name="see-also"></a>Siehe auch
- [Remote Debugging](../debugger/remote-debugging.md)