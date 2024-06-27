---
title: Workflows in Dynamics 365 Business Central
description: 'Verwenden Sie zum Einrichten von Genehmigungs-Workflows integrierte Workflow-Funktionen, um automatisierte Workflows basierend auf Power Automate zu ergänzen. Sie können Schritte einrichten, um Aufgaben als Teil der verschiedenen Geschäftsprozessaufgaben verschiedenen Personen zuzuweisen.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 06/13/2024
ms.custom: bap-template
---
# <a name="workflows-in-business-central"></a>Workflows in Business Central

Sie können Workflows festlegen und verwenden, die von verschiedenen Benutzern ausgeführte Geschäftsprozessaufgaben miteinander verbinden. Systemaufgaben, wie z.B. automatische Buchungen, können als Schritte in Workflows eingebunden werden. Den Systemaufgaben können Benutzeraufgaben vorausgehen oder folgen. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.

Die Standardversion von [!INCLUDE [prod_short](includes/prod_short.md)] unterstützt diese drei Typen von Workflows:
  
* Power Automate-Flows

  * Automatisierte Flows, die durch Ereignisse (z.B. Erstellung, Änderung oder Löschung von Datensätzen oder Dokumenten) in [!INCLUDE[prod_short](includes/prod_short.md)] ausgelöst werden. Dazu gehören auch in Power Automate erstellte Genehmigungs Flows, die ausgelöst werden, wenn eine Genehmigung in [!INCLUDE[prod_short](includes/prod_short.md)] beantragt wird.
  * Direktflows, die manuell durch das Aktionsmenü **Automatisieren** von Listen, Karten und Dokumentenseiten ausgelöst werden.

    Erstellen und lösen Sie Power Automate-Flows in einem [!INCLUDE[prod_short](includes/prod_short.md)] Datensatz manuell aus, wie z. B. ein Kunde, ein Artikel oder ein Verkaufsauftrag, mit Optionen zur internen und externen Bearbeitung von Informationen (unter Verwendung integrierter Tools).

* Genehmigungsworkflows basierend auf integrierten Workflow-Vorlagen

  Auf der Seite **Workflow-Vorlagen** können Sie alle verfügbaren Workflows anzeigen. Die Testversion von [!INCLUDE[prod_short](includes/prod_short.md)] umfasst viele vorkonfigurierte Workflows, für die Workflowvorlagen vorliegen. Diese können Sie kopieren, um neue zu erstellen. Wenn Sie eine Workflow-Vorlage auf der Seite **Workflow-Vorlagen** öffnen und der Name des Workflows mit *MS-* beginnt, wurde die Workflowvorlage von Microsoft hinzugefügt.

## <a name="power-automate-flows"></a>Power Automate-Flows

Mit [!INCLUDE [prod_short](includes/prod_short.md)] Online können Sie sich für Power Automate anmelden, um leistungsstarke automatisierte Workflows zu erstellen. Sie führen diese Workflows von [!INCLUDE [prod_short](includes/prod_short.md)] aus. Die Flows können interne und externe Datenquellen und Tools miteinander verbinden, ohne dass Sie Programmierkenntnisse benötigen.

|**Prozess** |**Informationen**|
|-------|-------|
|Starten Sie mit Power Automate, erstellen Sie Flows und führen Sie Direktflows aus|[Power Automate-Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)verwenden|
|Erfahren Sie mehr darüber, wie Sie Flows erstellen, bearbeiten und verwalten können|[Automatisierte Flows festlegen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) und [Instant Flows einrichten](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Festlegen von Power Automate Integration mit [!INCLUDE[prod_short](includes/prod_short.md)] für Benutzer als Admin|[Einrichten der Power Automate-Integration](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## <a name="approval-workflows"></a>Genehmigungsworkflows

Erstellen Sie einen Genehmigungs-Workflow, indem Sie festlegen, wodurch der Workflow erstellt wird und was als Nächstes geschieht, wie folgt:

* Ein Workflow-Ereignis, das durch Ereignisbedingungen moderiert wird.
* Einer Workflow-Antwort, die durch Antwortoptionen moderiert wird.

Um Workflow-Schritte zu definieren, füllen Sie Felder in Workflow-Zeilen mit den Ereignis- und Antwortwerten aus, die unterstützte Szenarien darstellen.

Beispiele für Ereignisse in Genehmigungsworkflows sind die Erstellung von Verkaufs- oder Kaufaufträgen/Angeboten/Rechnungen, Preisänderungen, Kreditoren- oder Debitorenbearbeitungen und mehr.

[!INCLUDE[workflow](includes/workflow.md)]

| **Prozess** | **Siehe** |
|--|--|
| Richten Sie Genehmigungsworkflowbenutzer ein, geben Sie an, wie Benutzer benachrichtigt werden, und erstellen Sie neue Workflows. (Um neue Workflow für nicht unterstützte Szenarien zu erstellen, implementieren Sie die erforderlichen Workflowelemente, indem Sie den Anwendungscode anpassen). | [Genehmigungsworkflows einrichten](across-set-up-workflows.md) |
| Aktivieren Sie Genehmigungsworkflows, reagieren Sie auf Workflowbenachrichtigungen, einschließlich Anfragegenehmigungen und Anforderungen, um einen Workflowschritt auszuführen. Archivieren und löschen Sie Workflows. | [Genehmigungsworkflows verwenden](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Projekte verwalten](projects-manage-projects.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Problembehandlung für automatisierte [!INCLUDE[prod_short](includes/prod_short.md)]-Workflows](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
