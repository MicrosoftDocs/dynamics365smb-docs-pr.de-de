---
title: Einrichten von Workflowbenachrichtigungen | Microsoft Docs
description: "Mit vielen Workflowantworten werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen. Bei einem Workflowschritt kann es sich beispielsweise um das Ereignis handeln, dass Benutzer 1 die Genehmigung eines neuen Datensatzes anfordert, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 2 (den Genehmiger) gesendet wird. Der nächste Workflowschritt kann das Ereignis umfassen, dass Benutzer 2 den Datensatz genehmigt, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 3 gesendet wird, damit die entsprechende Verarbeitung des genehmigten Datensatzes gestartet wird. Für Workflowschritte in Bezug auf Genehmigungen ist jede Benachrichtigung an einen Genehmigungsposten gebunden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 222056cc8b505d0ed027492d764ff4cde7f68795
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-workflow-notifications"></a>Einrichten von Workflowbenachrichtigungen
Mit vielen Workflowantworten werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen. Bei einem Workflowschritt kann es sich beispielsweise um das Ereignis handeln, dass Benutzer 1 die Genehmigung eines neuen Datensatzes anfordert, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 2 (den Genehmiger) gesendet wird. Der nächste Workflowschritt kann das Ereignis umfassen, dass Benutzer 2 den Datensatz genehmigt, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 3 gesendet wird, damit die entsprechende Verarbeitung des genehmigten Datensatzes gestartet wird. Für Workflowschritte in Bezug auf Genehmigungen ist jede Benachrichtigung an einen Genehmigungsposten gebunden. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

> [!NOTE]  
>  Die allgemeine Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt Benachrichtigungen in Form von E-Mails und internen Notizen.  

> [!IMPORTANT]  
>  Alle Workflowbenachrichtigungen werden über eine Projektwarteschlange gesendet. Stellen Sie sicher, dass die Projektwarteschlange in Ihrer Lösung eingerichtet ist. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)

In den folgenden Bereichen richten Sie verschiedene Aspekte von Workflowbenachrichtigungen ein:  

1.  Für Genehmigungsworkflows richten Sie die Empfänger von Workflowbenachrichtigungen ein, indem Sie im Fenster **Benutzereinrichtungs-Genehmigung** eine Zeile für jeden Benutzer ausfüllen, der in den Workflow einbezogen wird. Wenn beispielsweise Benutzer 2 im Feld  **Benutzer-ID**in der Zeile für Benutzer 1 angegeben ist, dann wird die Benachrichtigung für eine Genehmigungsanforderung an Benutzer 1 gesendet. Weitere Informationen finden Sie unter . [Weitere Informationen finden Sie unter Vorgehensweise: Einrichten von Genehmigungsbenutzern.](across-how-to-set-up-approval-users.md)  
2.  Sie legen fest, wann und wie Benutzer Workflowbenachrichtigungen erhalten, indem Sie das Fenster **Benachrichtigungsplan** für jeden Workflowbenutzer ausfüllen. Weitere Informationen finden Sie unter [Vorgehensweise: Definieren Sie, wann und wie Sie Benachrichtigungen möchten](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Zum Einrichten des allgemeinen Inhalts und des Layouts von Benachrichtigungen, einschließlich Benachrichtigungen über überfällige Workflowantworten, definieren Sie Benachrichtigungsvorlagen im Fenster **Benachrichtigungsvorlagen** Sie können die Standardvorlagen von [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden.  
4.  Sie richten bestimmte Inhalte und Regeln für eine Workflowbenachrichtigung ein, wenn Sie den betreffenden Workflow erstellen. Dazu wählen Sie Optionen im Fenster **Workflowreaktion-Optionen** für die Workflowantwort aus, die die Benachrichtigung darstellt. Weitere Informationen finden Sie unter Schritt 9 unter [Gewusst wie: Erstellen von Workflows](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Siehe auch  
 [Gewusst wie: Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md)   
 [So wird's gemacht: Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)   
 [Gewusst wie: Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [So wird's gemacht: Erstellen von Workflows](across-how-to-create-workflows.md)   
 [Gewusst wie: Verwalten von Benachrichtigungssorlagen](across-how-to-manage-notification-templates.md)   
 [Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)   
 [Gewusst wie: Einrichten von E-Mails](madeira-how-setup-email.md)   
 [Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Workflow](across-workflow.md)   

