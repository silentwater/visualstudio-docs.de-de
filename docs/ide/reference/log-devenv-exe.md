---
title: -Log („devenv.exe“)
ms.date: 12/12/2018
ms.topic: reference
helpviewer_keywords:
- Devenv, /Log switch
- Log switch [devenv.exe]
- /Log Devenv switch
ms.assetid: ae23c4ae-2376-4fe3-b8d2-81d34e61c8ba
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4b2e11cb36176aec94528019cdd19bb5fa86c92b
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2019
ms.locfileid: "55907216"
---
# <a name="log-devenvexe"></a>/Log (devenv.exe)

Protokolliert sämtliche Aktivitäten zur Problembehandlung in der Protokolldatei. Diese Datei wird angezeigt, nachdem Sie `devenv /log` mindestens einmal aufgerufen haben. Standardmäßig befindet sich die Protokolldatei an folgendem Speicherort:

**%APPDATA%\\Microsoft\\VisualStudio\\**\<Version\>**\\ActivityLog.xml**

wobei \<Version\> für die Visual Studio-Version steht. Sie können jedoch einen anderen Pfad und Dateinamen angeben.

## <a name="syntax"></a>Syntax

```shell
devenv /Log NameOfLogFile
```

## <a name="arguments"></a>Argumente

- *NameOfLogFile*

  Erforderlich. Der vollständige Pfad und Name der Protokolldatei, in die gespeichert werden soll.

## <a name="remarks"></a>Hinweise

Dieser Schalter muss am Ende der Befehlszeile nach allen anderen Schaltern angezeigt werden.

Das Protokoll wird nur für alle Instanzen von Visual Studio geschrieben, die Sie mit dem `/Log`-Schalter geöffnet haben.

## <a name="example"></a>Beispiel

In diesem Beispiel erfolgt die Protokollierung in der Datei `MyVSLog.xml` im Basisverzeichnis des Benutzers.

```shell
devenv /log "%USERPROFILE%\MyVSLog.xml"
```

## <a name="see-also"></a>Siehe auch

- [Devenv-Befehlszeilenschalter](../../ide/reference/devenv-command-line-switches.md)