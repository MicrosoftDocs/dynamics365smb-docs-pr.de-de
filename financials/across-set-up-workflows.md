---
title: Einrichten von Workflows | Microsoft Docs
description: "Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 75571a006ab267cfef268e0ff6b62ffd0ffb936b
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="setting-up-workflows"></a>Einrichten von Workflows
Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte. Weitere Informationen erhalten Sie unter [Workflows verwenden](across-use-workflows.md).  

 Bevor Sie beginnen, Workflows zu verwenden, müssen Sie Workflowbenutzer und Genehmigungsbenutzer einrichten und angeben, wie Benutzer Benachrichtigungen über Workflowschritte empfangen sollen. Dann müssen Sie Workflows erstellen und möglicherweise zuvor Codeanpassungen vornehmen.  

 Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.  

 Wenn ein Szenario ein Workflowereignis oder -antwort benötigt, die nicht unterstützt wird, muss ein Microsoft-Partner diese implementieren, indem er den Anwendungscode anpasst. Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Implementieren von neuen Workflowereignissen und von Kampagnenreaktionen](/dynamics_nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in der Entwickler- und IT-Pro-Hilfe.

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.  

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Einrichten von Workflowbenutzern und Benutzergruppen|[Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)|  
|Richten Sie Workflowbenutzer ein, die an den Genehmigungsworkflows teilnehmen.|[Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)|  
|Geben Sie an, wie Workflowbenutzer über Workflowschritte (einschließlich Genehmigungsanforderungen) benachrichtigt werden.|[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)|  
|Geben Sie an, wann Benutzer Benachrichtigungen empfangen und ob Benachrichtigungen innerhalb eines Zeitraums zusammengefasst werden sollen, um die Anzahl von Benachrichtigungen zu minimieren.|[Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Richten Sie das Layout und den allgemeinen Inhalt neuer Workflowbenachrichtigungs-E-Mails ein, oder exportieren, ändern und importieren Sie vorhandene Vorlagen.|[Verwalten von Benachrichtigungsvorlagen](across-how-to-manage-notification-templates.md)|  
|Richten Sie einen SMTP-Server so ein, dass die E-Mail-Kommunikation mit  aktiviert ist. [!INCLUDE[d365fin](includes/d365fin_md.md)]|[E-Mail einrichten](madeira-how-setup-email.md)|
|Geben Sie die verschiedenen Schritte eines Workflows mithilfe von Verbindungsworkflowereignissen mit Workflowantworten an.|[Erstellen eines Workflows](across-how-to-create-workflows.md)|  
|Verwenden Sie Workflowvorlagen, um neue Workflows zu erstellen.|[Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md)|  
|Teilen Sie Workflows mit anderen [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbanken.|[Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)|  
|Erfahren Sie anhand eines vollständigen Ablaufs, wie Sie einen Workflow zur Genehmigung von Verkaufsunterlagen einrichten.|[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Fügen Sie Unterstützung für ein Geschäftsszenario hinzu, das neue Workflowereignisse oder Reaktionen benötigt, indem Sie den Anwendungscode anpassen.|[Exemplarische Vorgehensweise: Implementieren neuer Workflow-Ereignisse und -Antworten](/dynamics_nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="see-also"></a>Siehe auch  
 [Verwenden von Workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
 [Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Arbeiten mit Financials](ui-work-product.md)

