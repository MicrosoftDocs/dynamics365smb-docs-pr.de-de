---
title: Einrichten von Workflowbenachrichtigungen | Microsoft Docs
description: Mit vielen Workflowantworten werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen. Bei einem Workflowschritt kann es sich beispielsweise um das Ereignis handeln, dass Benutzer 1 die Genehmigung eines neuen Datensatzes anfordert, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 2 (den Genehmiger) gesendet wird. Der nächste Workflowschritt kann das Ereignis umfassen, dass Benutzer 2 den Datensatz genehmigt, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 3 gesendet wird, damit die entsprechende Verarbeitung des genehmigten Datensatzes gestartet wird. Für Workflowschritte in Bezug auf Genehmigungen ist jede Benachrichtigung an einen Genehmigungsposten gebunden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2dc95629a923bea30d1c23bbbf0f016e5ef2dcc4
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187628"
---
# <a name="setting-up-workflow-notifications"></a>Einrichten von Workflowbenachrichtigungen
Mit vielen Workflowantworten werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen. Bei einem Workflowschritt kann es sich beispielsweise um das Ereignis handeln, dass Benutzer 1 die Genehmigung eines neuen Datensatzes anfordert, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 2 (den Genehmiger) gesendet wird. Der nächste Workflowschritt kann das Ereignis umfassen, dass Benutzer 2 den Datensatz genehmigt, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 3 gesendet wird, damit die entsprechende Verarbeitung des genehmigten Datensatzes gestartet wird. Für Workflowschritte in Bezug auf Genehmigungen ist jede Benachrichtigung an einen Genehmigungsposten gebunden. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

> [!NOTE]  
>  Die allgemeine Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt Benachrichtigungen in Form von E-Mails und internen Notizen.  

> [!IMPORTANT]  
>  Alle Workflowbenachrichtigungen werden über eine Projektwarteschlange gesendet. Stellen Sie sicher, dass die Auftragswarteschlange in Ihrer Installation so eingerichtet ist, dass Workfolw-Benachrichtigungen behandelt werden können und dass das Kontrollkästchen **Automatisch vom Server starten** aktiviert ist. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)

In den folgenden Bereichen richten Sie verschiedene Aspekte von Workflowbenachrichtigungen ein:  

1.  Für Genehmigungsworkflows richten Sie die Empfänger von Workflowbenachrichtigungen ein, indem Sie auf der Seite **Benutzereinrichtungs-Genehmigung** eine Zeile für jeden Benutzer ausfüllen, der in den Workflow einbezogen wird. Wenn beispielsweise Benutzer 2 im Feld **Benutzer-ID** in der Zeile für Benutzer 1 angegeben ist, dann wird die Benachrichtigung für eine Genehmigungsanforderung an Benutzer 1 gesendet. Weitere Informationen finden Sie unter . Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern.](across-how-to-set-up-approval-users.md)  
2.  Sie legen fest, wann und wie Benutzer Workflowbenachrichtigungen erhalten, indem Sie auf der Seite **Benachrichtigungsplan** für jeden Workflowbenutzer ausfüllen. Weitere Informationen finden Sie unter [Definieren Sie, wann und wie Sie Benachrichtigungen möchten](across-how-to-specify-when-and-how-to-receive-notifications.md).  
3.  Wenn Sie möchten, können Sie den Inhalt der E-Mail-Benachrichtigung anpassen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail ändern. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).  
4.  Sie richten bestimmte Inhalte und Regeln für eine Workflowbenachrichtigung ein, wenn Sie den betreffenden Workflow erstellen. Dazu wählen Sie Optionen auf der Seite **Workflowreaktion-Optionen** für die Workflowantwort aus, die die Benachrichtigung darstellt. Weitere Informationen finden Sie unter Schritt 9 unter [Erstellen von Workflows](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Siehe auch  
 [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)   
 [Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)   
 [Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen](across-how-to-specify-when-and-how-to-receive-notifications.md)   
 [Erstellen eines Workflows](across-how-to-create-workflows.md)   
 [Erstellen und bearbeiten von benutzerdefinierten Berichtslayouts](ui-how-create-custom-report-layout.md)   
 [Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)   
 [E-Mail einrichten](admin-how-setup-email.md)   
 [Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsgenehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Workflow](across-workflow.md)   
