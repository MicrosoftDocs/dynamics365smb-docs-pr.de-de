---
title: Einrichten von Genehmigungs-Workflowbenachrichtigungen
description: 'In diesem Artikel erfahren Sie, wie Sie Workflow-Benachrichtigungen festlegen, um einen Benutzer zu warnen, dass ein Ereignis eingetreten ist, auf das er reagieren muss; eine Workflow-Reaktion ist erforderlich.'
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: edupont
---
# <a name="approval-workflow-notifications" />Genehmigungsworkflow-Benachrichtigungen

Richten Sie Ihre Workflows so ein, dass Benutzer automatisch benachrichtigt werden, wenn ihre Aufmerksamkeit für einen Schritt in einem Workflow erforderlich ist. Mit vielen Workflowantworten werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen.

Sie können beispielsweise festlegen, dass Benutzer 2, die genehmigende Person, eine Benachrichtigung erhält, wenn Benutzer 1 die Genehmigung für einen neuen Datensatz anfordert. Im nächsten Workflowschritt wird Benutzer 3 benachrichtigt, nachdem Benutzer 2 den Datensatz genehmigt hat, um eine entsprechende Verarbeitung des Datensatzes zu starten. Mit Genehmigungsworkflowschritten wird jede Benachrichtigung an einen Genehmigungsposten gebunden. Erfahren Sie mehr unter [Workflow](across-workflow.md).  

> [!NOTE]  
> Die Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt Benachrichtigungen in E-Mails oder in internen Notizen.  

> [!IMPORTANT]  
> Alle Workflowbenachrichtigungen werden über eine Projektwarteschlange gesendet. Stellen Sie sicher, dass die Auftragswarteschlange in Ihrer Installation so eingerichtet ist, dass Workfolw-Benachrichtigungen behandelt werden können und dass Sie **Automatisch vom Server starten** ausgewählt haben ist. Weitere Informationen finden Sie unter [Aufgabenwarteschlangen zum Planen von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications" />Benachrichtigungen einrichten

In den folgenden Bereichen können Sie verschiedene Aspekte von Workflowbenachrichtigungen einrichten:  

* Benachrichtigung des Genehmigenden

  Für Genehmigungsworkflows richten Sie die Empfänger von Workflowbenachrichtigungen ein, indem Sie auf der Seite **Benutzereinrichtungs-Genehmigung** eine Zeile für jeden Benutzer ausfüllen, der in den Workflow einbezogen wird.  

  Wenn beispielsweise Benutzer 2 im Feld **Benutzer-ID** in der Zeile für Benutzer 1 angegeben ist, dann wird die Benachrichtigung für eine Genehmigungsanforderung an Benutzer 2 gesendet. Weitere Informationen finden Sie unter . Erfahren Sie mehr unter [Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md). 
  
* Benachrichtigungspläne

  Legen Sie fest, wann und wie Benutzer Workflowbenachrichtigungen erhalten, indem Sie auf der Seite **Benachrichtigungsplan** für jeden Workflowbenutzer ausfüllen. Weitere Informationen erhalten Sie unter [Festlegen, wann und wie Sie Workflow-Benachrichtigungen erhalten möchten](across-how-to-specify-when-and-how-to-receive-notifications.md). 
  
* Passen Sie die E-Mail-Benachrichtigungen an

  Wenn Sie möchten, können Sie den Inhalt der E-Mail-Benachrichtigung anpassen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail ändern. Weitere Informationen erhalten Sie unter [Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md).  

  > [!NOTE]
  > Wenn Sie E-Mail als Benachrichtigungsmethode verwenden möchten, müssen Sie E-Mail sowohl für den Absender als auch für den Empfänger in [!INCLUDE [prod_short](includes/prod_short.md)] einrichten. Erfahren Sie mehr unter [E-Mail einrichten](admin-how-setup-email.md).
  
* Antwortoptionen

  Legen Sie bestimmte Inhalte und Regeln für eine Workflowbenachrichtigung ein, wenn Sie den betreffenden Workflow erstellen. Wählen Sie die Anpassungsoptionen auf der Seite **Workflowreaktionen** für die Workflowreaktion aus, die die Benachrichtigung darstellt. Erfahren Sie mehr ab Schritt 9 unter [ Workflows erstellen](across-how-to-create-workflows.md#to-create-a-workflow). 
  
* Den Absender benachrichtigen

  Fügen Sie für Genehmigungsworkflows einen Workflow-Antwortschritt hinzu, um den Absender zu benachrichtigen, wenn die Anforderung genehmigt oder abgelehnt wurde. Erfahren Sie mehr ab Schritt 9 unter [ Workflows erstellen](across-how-to-create-workflows.md#to-create-a-workflow).   

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## <a name="see-also" />Siehe auch

[Einrichten von Genehmigten Benutzern](across-how-to-set-up-approval-users.md)  
[Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)  
[Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Genehmigungsworkflows erstellen](across-how-to-create-workflows.md)  
[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)  
[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)  
[E-Mail einrichten](admin-how-setup-email.md)  
[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
