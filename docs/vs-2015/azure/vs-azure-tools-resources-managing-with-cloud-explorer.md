---
title: Verwalten von Azure-Ressourcen mit dem Cloud-Explorer | Microsoft Docs
description: Informationen dazu, wie Sie Azure-Ressourcen mit dem Cloud-Explorer innerhalb von Visual Studio durchsuchen und verwalten.
author: ghogen
manager: jillfra
assetId: 6347dc53-f497-49d5-b29b-e8b9f0e939d7
ms.prod: visual-studio-dev14
ms.technology: vs-azure
ms.custom: vs-azure
ms.workload: azure-vs
ms.topic: conceptual
ms.date: 03/25/2017
ms.author: ghogen
ms.openlocfilehash: 25995eacc961474fcb6486668c918d2e5be5ba76
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/23/2019
ms.locfileid: "58958826"
---
# <a name="manage-the-resources-associated-with-your-azure-accounts-in-visual-studio-cloud-explorer"></a>Verwalten der Ihren Azure-Konten zugeordneten Ressourcen im Visual Studio Cloud-Explorer

Mit dem Cloud-Explorer können Sie Ihre Azure-Ressourcen und -Ressourcengruppen anzeigen, deren Eigenschaften überprüfen und wichtige Entwickleraktionen für die Diagnose in Visual Studio ausführen.

Der Cloud-Explorer setzt wie das [Azure-Portal](http://go.microsoft.com/fwlink/p/?LinkID=525040) auf dem Azure Resource Manager-Stapel auf. Daher kann der Cloud-Explorer mit Ressourcen wie Azure-Ressourcengruppen und Azure-Diensten wie Logic Apps und API-Apps arbeiten und unterstützt die [rollenbasierte Zugriffssteuerung](/azure/role-based-access-control/role-assignments-portal) (Role-Based Access Control, RBAC).

## <a name="prerequisites"></a>Vorraussetzungen

* Visual Studio 2015 mit dem [Microsoft Azure SDK für .NET 2.9](https://www.microsoft.com/download/details.aspx?id=51657).
* Microsoft Azure-Konto: Wenn Sie noch nicht über ein Konto verfügen, können Sie sich [für eine kostenlose Testversion registrieren](http://go.microsoft.com/fwlink/?LinkId=623901) oder Ihre [Visual Studio-Abonnentenvorteile aktivieren](http://go.microsoft.com/fwlink/?LinkId=623901).

> [!NOTE]
> Um den Cloud-Explorer anzuzeigen, wählen Sie auf der Menüleiste die Option **Ansicht** > **Cloud-Explorer**.

## <a name="add-an-azure-account-to-cloud-explorer"></a>Hinzufügen eines Azure-Kontos zum Cloud-Explorer

Um die Ressourcen anzuzeigen, die einem Azure-Konto zugeordnet sind, müssen Sie das Konto zuerst zum Cloud-Explorer hinzufügen.

1. Wählen Sie im **Cloud-Explorer** die Option **Azure-Kontoeinstellungen**.

   ![Symbol für die Azure-Kontoeinstellungen im Cloud-Explorer](./media/vs-azure-tools-resources-managing-with-cloud-explorer/azure-account-settings.png)

1. Wählen Sie **Konten verwalten** aus.

   ![Cloud-Explorer-Link zum Hinzufügen eines Kontos](./media/vs-azure-tools-resources-managing-with-cloud-explorer/manage-accounts-link.png)

1. Melden Sie sich bei dem Azure-Konto an, dessen Ressourcen Sie durchsuchen möchten.

1. Wenn Sie bei einem Azure-Konto angemeldet sind, werden die Abonnements angezeigt, die diesem Konto zugeordnet sind. Aktivieren Sie die Kontrollkästchen für die Kontoabonnements, die Sie durchsuchen möchten, und wählen dann **Übernehmen**.

   ![Cloud-Explorer: anzuzeigende Azure-Abonnements auswählen](./media/vs-azure-tools-resources-managing-with-cloud-explorer/select-subscriptions.png)

1. Nach der Auswahl der Abonnements, deren Ressourcen Sie durchsuchen möchten, werden diese Abonnements und Ressourcen im Cloud-Explorer angezeigt.

   ![Ressourcenliste für ein Azure-Konto im Cloud-Explorer](./media/vs-azure-tools-resources-managing-with-cloud-explorer/resources-listed.png)

## <a name="remove-an-azure-account-from-cloud-explorer"></a>Entfernen eines Azure-Kontos aus dem Cloud-Explorer

1. Wählen Sie im **Cloud-Explorer** die Option **Kontenverwaltung** aus.

   ![Symbol für die Azure-Kontoeinstellungen im Cloud-Explorer](./media/vs-azure-tools-resources-managing-with-cloud-explorer/azure-account-settings.png)

1. Wählen Sie neben dem Konto, das Sie entfernen möchten, **Konten verwalten** aus.

   ![Symbol für die Azure-Kontoeinstellungen im Cloud-Explorer](./media/vs-azure-tools-resources-managing-with-cloud-explorer/remove-account.png)

1. Wählen Sie **Entfernen** aus, um ein Konto zu entfernen.

    ![Cloud-Explorer-Dialogfeld „Konten verwalten“](./media/vs-azure-tools-resources-managing-with-cloud-explorer/accountmanage.PNG)

## <a name="view-resource-types-or-resource-groups"></a>Anzeigen von Ressourcentypen oder Ressourcengruppen

Um Ihre Azure-Ressourcen anzuzeigen, wählen Sie entweder die Ansicht **Ressourcentypen** oder **Ressourcengruppen** aus.

1. Wählen Sie im **Cloud-Explorer** die Dropdownliste für die Ressourcenansicht.

   ![Cloud-Explorer-Dropdownliste zum Auswählen der gewünschten Ressourcenansicht](./media/vs-azure-tools-resources-managing-with-cloud-explorer/resources-view-dropdown.png)

1. Wählen Sie im Kontextmenü die gewünschte Ansicht aus:

   * Ansicht **Ressourcentypen**: Die übliche Ansicht im [Azure-Portal](http://go.microsoft.com/fwlink/p/?LinkID=525040), zeigt Ihre Azure-Ressourcen in Typkategorien wie Web-Apps, Speicherkonten und virtuellen Computern.
   * In Ansicht **Ressourcengruppen**: Zeigt Azure-Ressourcen gemäß der Kategorie der Azure-Ressourcengruppe, der sie zugeordnet sind. Eine Ressourcengruppe ist ein Bündel von Azure-Ressourcen, die in der Regel von einer bestimmten Anwendung verwendet werden. Weitere Informationen zu Azure-Ressourcengruppen finden Sie unter [Azure Resource Manager – Übersicht](/azure/azure-resource-manager/resource-group-overview).

   Die folgende Abbildung zeigt einen Vergleich der beiden Ressourcenansichten:

   ![Vergleich der Cloud-Explorer-Ressourcenansichten](./media/vs-azure-tools-resources-managing-with-cloud-explorer/resource-views-comparison.png)

## <a name="view-and-navigate-resources-in-cloud-explorer"></a>Anzeigen von und Navigieren in Ressourcen im Cloud-Explorer

Um zu einer Azure-Ressource zu navigieren und zugehörige Informationen im Cloud-Explorer anzuzeigen, erweitern Sie den Typ oder die zugeordnete Ressourcengruppe des Elements und wählen dann die Ressource aus. Wenn Sie eine Ressource auswählen, werden Informationen auf den beiden Registerkarten **Aktionen** und **Eigenschaften** unten im Cloud-Explorer angezeigt.

* Registerkarte **Aktionen**: Führt die Aktionen auf, die Sie im Cloud-Explorer für die ausgewählte Ressource ausführen können. Sie können diese Optionen auch anzeigen, indem Sie mit der rechten Maustaste auf die Ressource klicken, um das Kontextmenü zu öffnen.

* Registerkarte **Eigenschaften**: Zeigt die Eigenschaften der Ressource an, z.B. Typ, Gebietsschema und die Ressourcengruppe, der die Ressource zugeordnet ist.

Die folgende Abbildung zeigt einen Vergleich der Informationen, die auf beiden Registerkarten beispielsweise für eine App Service-Instanz angezeigt werden:

  ![Screenshot des Cloud-Explorers](./media/vs-azure-tools-resources-managing-with-cloud-explorer/actions-and-properties.png)

Für jede Ressource gibt es die Aktion **Im Portal öffnen**. Wenn Sie diese Aktion auswählen, zeigt der Cloud-Explorer die ausgewählte Ressource im [Azure-Portal](http://go.microsoft.com/fwlink/p/?LinkID=525040)an. Das Feature **Im Portal öffnen** ist besonders nützlich für die Navigation in sehr tief geschachtelten Ressourcen.

Zusätzliche Aktionen und Eigenschaftswerte können auch basierend auf der Azure-Ressource angezeigt werden. Für Web- und Logik-Apps gibt es zusätzlich zu **Im Portal öffnen** die Aktionen **Im Browser öffnen** und **Debugger anfügen**. Aktionen zum Öffnen von Editoren werden angezeigt, wenn Sie ein Blob, eine Warteschlange oder Tabelle eines Speicherkontos auswählen. Für Azure-Apps stehen die Eigenschaften **URL** und **Status** zur Verfügung, während Speicherressourcen Schlüssel und Verbindungszeichenfolgen-Eigenschaften aufweisen.

## <a name="find-resources-in-cloud-explorer"></a>Suchen von Ressourcen im Cloud-Explorer

Um in Ihren Azure-Kontoabonnements Ressourcen mit einem bestimmten Namen zu suchen, geben Sie den Namen in das Feld **Suchen** im Cloud-Explorer ein.

  ![Suchen von Ressourcen im Cloud-Explorer](./media/vs-azure-tools-resources-managing-with-cloud-explorer/search-for-resources.png)

Bei der Eingabe von Zeichen in das Feld **Suchen** werden in der Ressourcenstruktur nur die Ressourcen angezeigt, die mit diesen Zeichen übereinstimmen.
