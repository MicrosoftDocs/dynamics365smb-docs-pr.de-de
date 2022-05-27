---
title: Workflows in Dynamic 365 Business Central
description: Verwenden Sie zum Einrichten von Genehmigungs-Workflows die integrierten Workflow-Funktionen, um automatisierte Workflows basierend auf Power Automate zu ergänzen. Sie können Schritte einrichten, um Aufgaben als Teil der verschiedenen Geschäftsprozessaufgaben verschiedenen Personen zuzuweisen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: 84d4a87a0edab18be342b9ed5732de0350a31645
ms.sourcegitcommit: bc645e7ecb1940a85b2c433aa894d3494c9b10df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743671"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflows in Dynamics 365 Business Central

Sie können Workflows festlegen und verwenden, die von verschiedenen Benutzern ausgeführte Geschäftsprozessaufgaben miteinander verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.  

Die Standardversion von [!INCLUDE [prod_short](includes/prod_short.md)] unterstützt drei Arten von Workflows:

* Automatisierte Genehmigungs-Workflows basierend auf integrierten Workflow-Vorlagen  

  Auf der Seite **Workflow-Vorlagen** können Sie alle verfügbaren Workflows anzeigen. Die Testversion von [!INCLUDE[prod_short](includes/prod_short.md)] umfasst mehrere vorkonfigurierte Workflows, für die Workflowvorlagen vorliegen. Diese können Sie kopieren, um Workflows zu erstellen. Wenn Sie eine Workflow-Vorlage auf der Seite **Workflow-Vorlagen** öffnen und der Name des Workflows mit *MS-* beginnt, wird die Workflowvorlage von Microsoft hinzugefügt.  
* Automatisierte Abläufe, die Sie selbst einrichten  

  Jede mit Power Automate erstellte Workflowvorlage wird der Liste der Workflowvorlagen in [!INCLUDE[prod_short](includes/prod_short.md)] hinzugefügt. Weitere Informationen finden Sie unter [Business Central in Power Automate-Flows verwenden](across-how-use-financials-data-source-flow.md).  
* Manuell ausgelöste Flows aus der Aktion **Automatisieren** ([!INCLUDE [prod_short](includes/prod_short.md)] nur online). Weitere Informationen finden Sie unter [Manuelle Direktflows](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Power Automate-Flows

Für [!INCLUDE [prod_short](includes/prod_short.md)] Online können Sie sich bei Power Automate anmelden und dann leistungsstarke automatisierte Flows erstellen, die Sie über [!INCLUDE [prod_short](includes/prod_short.md)] ausführen können. Weitere Informationen finden Sie unter [[!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate-Flows verwenden](across-how-use-financials-data-source-flow.md).  

## <a name="automated-approval-workflows"></a>Automatisierte Genehmigungsworkflows

Sie können einen Genehmigungsworkflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.  

Wenn ein Geschäftsszenario ein Workflowereignis oder eine Reaktion erfordert, das/die in der Standardversion nicht unterstützt wird, registrieren Sie sich bei Power Automate. Weitere Informationen finden Sie unter [[!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate-Flows verwenden](across-how-use-financials-data-source-flow.md). Holen Sie sich alternativ eine App, oder arbeiten Sie mit einem Microsoft-Partner zusammen, um den Anwendungscode anzupassen.  

Lesen Sie die folgenden Artikel, um Workflows, die nicht in Power Automate definiert sind, einzurichten und zu verwenden:  

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Richten Sie Workflowbenutzer ein, geben Sie an, wie Benutzer benachrichtigt werden, und erstellen Sie neue Workflows. Implementieren Sie für neue Workflow für nicht unterstützte Szenarien die erforderlichen Workflowelemente, indem Sie den Anwendungscode anpassen.|[Einrichten von Workflows](across-set-up-workflows.md)|  
|Aktivieren Sie Workflows, reagieren Sie auf Workflowbenachrichtigungen, einschließlich Anfragegenehmigungen und genehmigen Sie Anforderungen, um einen Workflowschritt auszuführen. Archivieren und löschen Sie Workflows.|[Verwenden von Workflows](across-use-workflows.md)|  

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Projekte verwalten](projects-manage-projects.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate-Flows verwenden](across-how-use-financials-data-source-flow.md)  
[Problembehandlung für automatisierte [!INCLUDE[prod_short](includes/prod_short.md)]-Workflows](across-flow-troubleshoot.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]