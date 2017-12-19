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
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 6beb70ad41fa32043e9b8afea67d390929533007
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="setting-up-workflows"></a>Einrichten von Workflows
Sie können Workflows einrichten und verwenden, die Geschäftsprozessaufgaben von verschiedenen Benutzern verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte. Weitere Informationen erhalten Sie unter [Workflows verwenden](across-use-workflows.md).  

 Bevor Sie beginnen, Workflows zu verwenden, müssen Sie Workflowbenutzer und Genehmigungsbenutzer einrichten und angeben, wie Benutzer Benachrichtigungen über Workflowschritte empfangen sollen. Dann müssen Sie Workflows erstellen und möglicherweise zuvor Codeanpassungen vornehmen.  

 Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.  

 Wenn ein Szenario ein Workflowereignis oder -antwort benötigt, die nicht unterstützt wird, muss ein Microsoft-Partner diese implementieren, indem er den Anwendungscode anpasst. Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Implementieren von neuen Workflowereignissen und von Kampagnenreaktionen](/dynamics_nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in der Entwickler- und IT-Pro-Hilfe.

 Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.  

|**An**|**Siehe**|  
|------------|-------------|  
|Einrichten von Workflowbenutzern und Benutzergruppen|[So wird's gemacht: Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)|  
|Richten Sie Workflowbenutzer ein, die an den Genehmigungsworkflows teilnehmen.|[Gewusst wie: Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md)|  
|Geben Sie an, wie Workflowbenutzer über Workflowschritte (einschließlich Genehmigungsanforderungen) benachrichtigt werden.|[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)|  
|Geben Sie an, wann Benutzer Benachrichtigungen empfangen und ob Benachrichtigungen innerhalb eines Zeitraums zusammengefasst werden sollen, um die Anzahl von Benachrichtigungen zu minimieren.|[Gewusst wie: Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Richten Sie das Layout und den allgemeinen Inhalt neuer Workflowbenachrichtigungs-E-Mails ein, oder exportieren, ändern und importieren Sie vorhandene Vorlagen.|[Gewusst wie: Verwalten von Benachrichtigungssorlagen](across-how-to-manage-notification-templates.md)|  
|Richten Sie einen SMTP-Server so ein, dass die E-Mail-Kommunikation mit [!INCLUDE[d365fin](includes/d365fin_md.md)] aktiviert ist.|[Gewusst wie: Einrichten von E-Mails](madeira-how-setup-email.md)|
|Geben Sie die verschiedenen Schritte eines Workflows mithilfe von Verbindungsworkflowereignissen mit Workflowantworten an.|[So wird's gemacht: Erstellen von Workflows](across-how-to-create-workflows.md)|  
|Verwenden Sie Workflowvorlagen, um neue Workflows zu erstellen.|[Vorgehensweise: Workflows von Workflowvorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md)|  
|Teilen Sie Workflows mit anderen [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbanken.|[Vorgehensweise: Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)|  
|Erfahren Sie anhand eines vollständigen Ablaufs, wie Sie einen Workflow zur Genehmigung von Verkaufsunterlagen einrichten.|[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Fügen Sie Unterstützung für ein Geschäftsszenario hinzu, das neue Workflowereignisse oder Reaktionen benötigt, indem Sie den Anwendungscode anpassen.|[Exemplarische Vorgehensweise: Implementieren neuer Workflow-Ereignisse und -Antworten](/dynamics_nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="see-also"></a>Siehe auch  
 [Verwenden von Workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
 [Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Arbeiten mit Financials](ui-work-product.md)

