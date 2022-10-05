---
title: Workflows in Dynamics 365 Business Central
description: Verwenden Sie zum Einrichten von Genehmigungs-Workflows integrierte Workflow-Funktionen, um automatisierte Workflows basierend auf Power Automate zu ergänzen. Sie können Schritte einrichten, um Aufgaben als Teil der verschiedenen Geschäftsprozessaufgaben verschiedenen Personen zuzuweisen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585621"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflows in Dynamics 365 Business Central

Sie können Workflows festlegen und verwenden, die von verschiedenen Benutzern ausgeführte Geschäftsprozessaufgaben miteinander verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.

Die Standardversion von [!INCLUDE [prod_short](includes/prod_short.md)] unterstützt drei Arten von Workflows:

* Genehmigungsworkflows basierend auf integrierten Workflow-Vorlagen

  Auf der Seite **Workflow-Vorlagen** können Sie alle verfügbaren Workflows anzeigen. Die Testversion von [!INCLUDE[prod_short](includes/prod_short.md)] umfasst viele vorkonfigurierte Workflows, für die Workflowvorlagen vorliegen. Diese können Sie kopieren, um neue zu erstellen. Wenn Sie eine Workflow-Vorlage auf der Seite **Workflow-Vorlagen** öffnen und der Name des Workflows mit *MS-* beginnt, wurde die Workflowvorlage von Microsoft hinzugefügt.
  
* Power Automate-Flows, die Sie selbst einrichten

  Jede mit Microsoft Power Automate erstellte Workflowvorlage wird der Liste der Workflowvorlagen in [!INCLUDE[prod_short](includes/prod_short.md)] hinzugefügt. Erfahren Sie mehr unter [[!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate-Flows verwenden](across-how-use-financials-data-source-flow.md). 
  
* Manuell ausgelöste Direktflows aus der Aktion **Automatisieren** ([!INCLUDE [prod_short](includes/prod_short.md)] nur online).

  Erstellen und lösen Sie Power Automate-Flows in einem [!INCLUDE[prod_short](includes/prod_short.md)] Datensatz manuell aus, wie z. B. ein Kunde, ein Artikel oder ein Verkaufsauftrag, mit Optionen zur internen und externen Bearbeitung von Informationen (unter Verwendung integrierter Tools). Erfahren Sie mehr im Abschnitt [Direktflows](across-how-use-financials-data-source-flow.md#instant-flows).

## <a name="power-automate-flows"></a>Power Automate-Flows

Mit [!INCLUDE [prod_short](includes/prod_short.md)] Online können Sie sich für Power Automate anmelden, um leistungsstarke automatisierte Workflows erstellen. Sie können diese Workflows aus [!INCLUDE [prod_short](includes/prod_short.md)] heraus ausführen, interne und externe Datenquellen und Tools ohne Programmierkenntnisse ohne Codekenntnisse verbinden.

Power Automate-Flows können durch Ereignisse ausgelöst werden (z. B. Erstellen, Ändern oder Löschen von Datensätzen oder Dokumenten) und nach einem benutzerdefinierten Zeitplan oder bei Bedarf (**Direktflow**).

## <a name="approval-workflows"></a>Genehmigungsworkflows

Sie können einen Genehmigungsworkflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.<!--What are the "values"? Can we give an example?-->

Beispiele für Genehmigungs-Workflow-Ereignisse sind unter anderem die Erstellung von Verkaufs- oder Kaufaufträgen/Angeboten/Rechnungen, Preisänderungen und Lieferanten- oder Kundenbearbeitungen.

[!INCLUDE[workflow](includes/workflow.md)]

| **Prozess** | **Siehe** |
|--|--|
| Richten Sie Genehmigungsworkflowbenutzer ein, geben Sie an, wie Benutzer benachrichtigt werden, und erstellen Sie neue Workflows. (Um neue Workflow für nicht unterstützte Szenarien zu erstellen, implementieren Sie die erforderlichen Workflowelemente, indem Sie den Anwendungscode anpassen). | [Genehmigungsworkflows einrichten](across-set-up-workflows.md) |
| Aktivieren Sie Genehmigungsworkflows, reagieren Sie auf Workflowbenachrichtigungen, einschließlich Anfragegenehmigungen und Anforderungen, um einen Workflowschritt auszuführen. Archivieren und löschen Sie Workflows. | [Artikelgenehmigungsworkflow verwenden](across-use-workflows.md) |
| Integrieren Sie Unternehmensdaten mit Power Automate Workflows, wobei sowohl interne als auch externe Quellen und Ereignisse verwendet werden, um Aufgaben oder Workflows zu erstellen und zu automatisieren. | [Power Automate-Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)verwenden |

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Projekte verwalten](projects-manage-projects.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Problembehandlung für automatisierte [!INCLUDE[prod_short](includes/prod_short.md)]-Workflows](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
