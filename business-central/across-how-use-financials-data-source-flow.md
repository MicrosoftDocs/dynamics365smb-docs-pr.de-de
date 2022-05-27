---
title: Business Central in Power Automate-Flows verwenden
description: Richten Sie Power Automate-Flows zum Erstellen ode Ändern von Business Central-Daten ein, und verwenden Sie sie.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: 93eb177ff9ba102277a50f9686ea941df33d5563
ms.sourcegitcommit: 13ac10624bee47c73989b2b20942a01c849b4a6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2022
ms.locfileid: "8744110"
---
# <a name="use-prod_short-in-power-automate-flows"></a>[!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate-Flows verwenden

Sie können Ihre [!INCLUDE[prod_short](includes/prod_short.md)]-Daten als Teil eines Workflows in Microsoft Power Automate verwenden. Erstellen Sie Ihre eigenen Flows, und stellen Sie eine Verbindung mit Ihren Daten mit dem [!INCLUDE [prod_short](includes/prod_short.md)]-Konnektor her.  

> [!NOTE]  
> Sie müssen ein gültiges Konto bei [!INCLUDE[prod_short](includes/prod_short.md)] und Power Automate haben.  

> [!TIP]
> Zusätzlich zu Power Automate können Sie die Vorlagen für Genehmigungsworkflow in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden. Obwohl es zwei verschiedene Workflowsysteme sind, wird jede Vorlage für Genehmigungsworkflows, die Sie mit Power Automate erstellen, der Liste von Workflows in [!INCLUDE[prod_short](includes/prod_short.md)] hinzugefügt. Weitere Informationen finden Sie unter [Workflows](across-workflow.md).  

## <a name="automated-workflows"></a>Automatisierte Workflows

Mit Power Automate können Sie Geschäftsabläufe direkt intern erstellen und sich auf Citizen Developer verlassen. Weitere Informationen finden Sie unter [Automatisierte Workflows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) im Verwaltungsinhalt.  

## <a name="manual-instant-flows"></a>Manuelle Direktflows

Ab Mai 2022 kann ein Administrator von [!INCLUDE [prod_short](includes/prod_short.md)] Online kann [eine Funktion einschalten](admin-feature-management.md), um die Ausführung eines Power Automate-Flows von den meisten Seiten aus zu ermöglichen. Weitere Informationen finden Sie unter [Automatisierte Workflows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) im Verwaltungsinhalt.  

Sobald der Administrator [!INCLUDE [prod_short](includes/prod_short.md)] mit Power Automate verbunden hat, werden alle von Ihrer Organisation hinzugefügten Flows angezeigt, wenn Sie die Aktion **Automatisieren** auf den entsprechenden Seiten auswählen. Sie führen die Flows aus, ohne [!INCLUDE [prod_short](includes/prod_short.md)] zu verlassen.  

Diese automatisierten Workflows werden in einem Bereich in [!INCLUDE [prod_short](includes/prod_short.md)] Online geöffnet, damit Sie im Kontext des Geschäftsprozesses bleiben, in dem Sie sich gerade befanden. Auf einigen Seiten ist die Aktion **Automatisieren** unter dem Menü **Weitere Optionen** verborgen. Suchen Sie sie, wählen Sie den Menüpunkt **Power Automate** und dann den entsprechenden Link aus, um den Workflow auszulösen. Die Verknüpfung zu Power Automate ist bereits eingerichtet.  

Bei den meisten Flows müssen Sie ein oder zwei Felder ausfüllen, bevor Sie die Aktion **Flow ausführen** ausführen.  

> [!TIP]
> Wenn die Aktion **Automatisieren** nicht angezeigt wird, wurde [!INCLUDE [prod_short](includes/prod_short.md)] wahrscheinlich noch nicht für die Verwendung von Power Automate eingerichtet. Weitere Informationen erhalten Sie von Ihrem Administrator.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Weitere automatisierte Flows und manuelle Instant-Flows hinzufügen

Sie können Flows auf der Website [powerautomate.microsoft.com](https://powerautomate.microsoft.com) erstellen. Wenn Ihr Administrator jedoch die Funktion zum Ausführen von Power Automate-Flows in [!INCLUDE [prod_short](includes/prod_short.md)] Online deaktiviert hat, können Sie mit dem Erstellen eines Flows über die Aktion **Automatisieren** auf den entsprechenden Seiten beginnen. Auf einigen Seiten ist die Aktion **Automatisieren** unter dem Menü **Weitere Optionen** verborgen. Suchen Sie sie, wählen Sie den Menüpunkt **Power Automate** und dann die Aktion **Flow erstellen** aus. Power Automate wird dann in einer neuen Browserregisterkarte geöffnet, und Sie werden automatisch angemeldet.

## <a name="manage-workflows"></a>Workflows verwalten

Sie erhalten eine Übersicht aller Workflows, auf die Sie Zugriff haben, indem Sie auf die Aktion **Workflows verwalten** im Menü **Power Automate** klicken. Die Liste wird in einer neuen Browserregisterkarte geöffnet, und Sie werden automatisch bei Power Automate angemeldet. Dort können Sie sehen, wann jeder Flow zuletzt ausgeführt wurde.  

## <a name="see-also"></a>Siehe auch

[Problembehandlung für automatisierte [!INCLUDE[prod_short](includes/prod_short.md)]-Workflows](across-flow-troubleshoot.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Workflows](across-workflow.md)  
[Importieren von Geschäftsdaten aus anderen Finanzsystemen](across-import-data-configuration-packages.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] einrichten](setup.md)  
[Finanzen](finance.md)  
[Automatisierte Workflows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]