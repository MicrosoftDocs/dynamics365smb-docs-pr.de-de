---
title: Einrichten von Workflow-Benachrichtigungen
description: In diesem Thema erfahren Sie, wie Sie Workflow-Benachrichtigungen festlegen, um einen Benutzer zu warnen, dass ein Ereignis eingetreten ist, auf das er reagieren muss; eine Workflow-Reaktion ist erforderlich.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: f0db9d63257d37fe6be5d31fc58541caf968907a
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482432"
---
# <a name="workflow-notifications"></a>Workflow-Benachrichtigungen

Richten Sie Ihre Workflows so ein, dass Benutzer automatisch benachrichtigt werden, wenn ihre Aufmerksamkeit für einen Schritt in diesem Workflow erforderlich ist. Mit vielen Workflowantworten werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen. Bei einem Workflowschritt kann es sich beispielsweise um das Ereignis handeln, dass Benutzer 1 die Genehmigung eines neuen Datensatzes anfordert, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 2 (den Genehmiger) gesendet wird. Der nächste Workflowschritt kann das Ereignis umfassen, dass Benutzer 2 den Datensatz genehmigt, und die Antwort besteht darin, dass eine Benachrichtigung an Benutzer 3 gesendet wird, damit die entsprechende Verarbeitung des genehmigten Datensatzes gestartet wird. Für Workflowschritte in Bezug auf Genehmigungen ist jede Benachrichtigung an einen Genehmigungsposten gebunden. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

> [!NOTE]  
> Die allgemeine Version von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt Benachrichtigungen in Form von E-Mails und internen Notizen.  

> [!IMPORTANT]  
> Alle Workflowbenachrichtigungen werden über eine Projektwarteschlange gesendet. Stellen Sie sicher, dass die Auftragswarteschlange in Ihrer Installation so eingerichtet ist, dass Workfolw-Benachrichtigungen behandelt werden können und dass das Kontrollkästchen **Automatisch vom Server starten** aktiviert ist. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Benachrichtigungen einrichten

In den folgenden Bereichen richten Sie verschiedene Aspekte von Workflowbenachrichtigungen ein:  

* Benachrichtigung des Genehmigenden

    Für Genehmigungsworkflows richten Sie die Empfänger von Workflowbenachrichtigungen ein, indem Sie auf der Seite **Benutzereinrichtungs-Genehmigung** eine Zeile für jeden Benutzer ausfüllen, der in den Workflow einbezogen wird.  

    Wenn beispielsweise Benutzer 2 im Feld **Benutzer-ID** in der Zeile für Benutzer 1 angegeben ist, dann wird die Benachrichtigung für eine Genehmigungsanforderung an Benutzer 1 gesendet. Weitere Informationen finden Sie unter . Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md).  
* Benachrichtigungspläne

    Sie legen fest, wann und wie Benutzer Workflowbenachrichtigungen erhalten, indem Sie auf der Seite **Benachrichtigungsplan** für jeden Workflowbenutzer ausfüllen. Weitere Informationen finden Sie unter [Definieren Sie, wann und wie Sie Benachrichtigungen möchten](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Passen Sie die E-Mail-Benachrichtigungen an

    Wenn Sie möchten, können Sie den Inhalt der E-Mail-Benachrichtigung anpassen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail ändern. Weitere Informationen finden Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Wenn Sie E-Mail als Benachrichtigungsmethode verwenden möchten, müssen Sie E-Mail sowohl für den Absender als auch für den Empfänger in [!INCLUDE [prod_short](includes/prod_short.md)] einrichten. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

* Antwortoptionen

    Sie richten bestimmte Inhalte und Regeln für eine Workflowbenachrichtigung ein, wenn Sie den betreffenden Workflow erstellen. Dazu wählen Sie Optionen auf der Seite **Workflowreaktion-Optionen** für die Workflowantwort aus, die die Benachrichtigung darstellt. Weitere Informationen finden Sie unter Schritt 9 unter [Erstellen von Workflows](across-how-to-create-workflows.md).  

* Den Absender benachrichtigen

    Fügen Sie für Genehmigungsworkflows einen Workflow-Antwortschritt hinzu, um den Absender zu benachrichtigen, wenn die Anforderung genehmigt oder abgelehnt wurde. Weitere Informationen finden Sie unter Schritt 9 unter [Erstellen von Workflows](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Siehe auch

[Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)  
[Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)  
[Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Erstellen eines Workflows](across-how-to-create-workflows.md)  
[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)  
[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)  
[E-Mail einrichten](admin-how-setup-email.md)  
[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]