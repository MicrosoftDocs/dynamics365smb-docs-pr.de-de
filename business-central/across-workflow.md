---
title: Workflows in Dynamics 365 Business Central
description: Verwenden Sie Workflows, um Geschäftsprozessaufgaben zu verbinden, die von verschiedenen Benutzern ausgeführt werden. Systemaufgaben, wie z. B. automatische Buchungen, können als Workflow-Schritte eingebunden werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 1804ab571c806d9fb78d15738be7f27f21274146
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6324125"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Workflows in Dynamics 365 Business Central

Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte.  

 Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.  

 Die generische Version von [!INCLUDE[prod_short](includes/prod_short.md)] umfasst mehrere vorkonfigurierte Workflows, für die Workflowvorlagen vorliegen. Diese können Sie kopieren, um Workflows zu erstellen. Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS-“ vorangestellt. Weitere Informationen finden Sie in der Liste mit Workflowvorlagen auf der Seite Workflow-Vorlagen  

 Wenn ein Szenario ein Workflowereignis oder -antwort benötigt, die nicht unterstützt wird, können Sie Power Automate verwenden oder mit einem Microsoft-Partner zusammenarbeiten, um den Anwendungscode anzupassen. Weitere Informationen finden Sie unter [Verwenden von [!INCLUDE[prod_short](includes/prod_short.md)] in einem automatisierten Workflow](across-how-use-financials-data-source-flow.md).

Jede mit Power Automate erstellte Workflowvorlage wird der Liste der Workflowvorlagen in [!INCLUDE[prod_short](includes/prod_short.md)] hinzugefügt. Weitere Informationen finden Sie unter [Business Central in einem automatisierten Workflow nutzen](across-how-use-financials-data-source-flow.md).  

 Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..  

|**Aufgabe**|**Informationen**|  
|------------|-------------|  
|Richten Sie Workflowbenutzer ein, geben Sie an, wie Benutzer benachrichtigt werden, und erstellen Sie neue Workflows. Implementieren Sie für neue Workflow für nicht unterstützte Szenarien die erforderlichen Workflowelemente, indem Sie den Anwendungscode anpassen.|[Einrichten von Workflows](across-set-up-workflows.md)|  
|Aktivieren Sie Workflows, reagieren Sie auf Workflowbenachrichtigungen, einschließlich Anfragegenehmigungen und genehmigen Sie Anforderungen, um einen Workflowschritt auszuführen. Archivieren und löschen Sie Workflows.|[Verwenden von Workflows](across-use-workflows.md)|  

## <a name="see-also"></a>Siehe auch

[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Projekte verwalten](projects-manage-projects.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]