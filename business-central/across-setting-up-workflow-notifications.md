---
title: Einrichten von Workflow-Benachrichtigungen
description: In diesem Artikel erfahren Sie, wie Sie Workflow-Benachrichtigungen festlegen, um einen Benutzer zu warnen, dass ein Ereignis eingetreten ist, auf das er reagieren muss; eine Workflow-Reaktion ist erforderlich.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 99c08769429eef51a1d52e142d455ccd227781c7
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130010"
---
# <a name="workflow-notifications"></a>Workflow-Benachrichtigungen

Richten Sie Ihre Workflows so ein, dass Benutzer automatisch benachrichtigt werden, wenn ihre Aufmerksamkeit für einen Schritt in diesem Workflow erforderlich ist. Mit vielen Workflowantworten werden Benutzer darüber benachrichtigt, dass ein Ereignis stattgefunden hat, auf das sie reagieren müssen.

Sie können beispielsweise festlegen, dass Benutzer 2, die genehmigende Person, eine Benachrichtigung erhält, wenn Benutzer 1 die Genehmigung für einen neuen Datensatz anfordert. Im nächsten Workflowschritt wird Benutzer 3 benachrichtigt, nachdem Benutzer 2 den Datensatz genehmigt hat, um eine entsprechende Verarbeitung des Datensatzes zu starten. Mit Genehmigungsworkflowschritten wird jede Benachrichtigung an einen Genehmigungsposten gebunden. Weitere Informationen finden Sie unter [Workflow](across-workflow.md).  

> [!NOTE]  
> Die Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt Benachrichtigungen in Form von E-Mails und internen Notizen.  

> [!IMPORTANT]  
> Alle Workflowbenachrichtigungen werden über eine Projektwarteschlange gesendet. Stellen Sie sicher, dass die Auftragswarteschlange in Ihrer Installation so eingerichtet ist, dass Workfolw-Benachrichtigungen behandelt werden können und dass das Kontrollkästchen **Automatisch vom Server starten** aktiviert ist. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).

## <a name="set-up-notifications"></a>Benachrichtigungen einrichten

In den folgenden Bereichen können Sie verschiedene Aspekte von Workflowbenachrichtigungen einrichten:  

* Benachrichtigung des Genehmigenden

    Für Genehmigungsworkflows richten Sie die Empfänger von Workflowbenachrichtigungen ein, indem Sie auf der Seite **Benutzereinrichtungs-Genehmigung** eine Zeile für jeden Benutzer ausfüllen, der in den Workflow einbezogen wird.  

    Wenn beispielsweise Benutzer 2 im Feld **Benutzer-ID** in der Zeile für Benutzer 1 angegeben ist, dann wird die Benachrichtigung für eine Genehmigungsanforderung an Benutzer 2 gesendet. Weitere Informationen finden Sie unter . Weitere Informationen finden Sie unter [Einrichten von Genehmigungsbenutzern](across-how-to-set-up-approval-users.md).  
* Benachrichtigungspläne

    Sie legen fest, wann und wie Benutzer Workflowbenachrichtigungen erhalten, indem Sie auf der Seite **Benachrichtigungsplan** für jeden Workflowbenutzer ausfüllen. Weitere Informationen finden Sie unter [Definieren Sie, wann und wie Sie Benachrichtigungen möchten](across-how-to-specify-when-and-how-to-receive-notifications.md).  
* Passen Sie die E-Mail-Benachrichtigungen an

    Wenn Sie möchten, können Sie den Inhalt der E-Mail-Benachrichtigung anpassen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail ändern. Weitere Informationen finden Sie unter [Benutzerdefinierte Berichtslayouts erstellen und ändern](ui-how-create-custom-report-layout.md).  

    > [!NOTE]
    > Wenn Sie E-Mail als Benachrichtigungsmethode verwenden möchten, müssen Sie E-Mail sowohl für den Absender als auch für den Empfänger in [!INCLUDE [prod_short](includes/prod_short.md)] einrichten. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

* Antwortoptionen

    Sie richten bestimmte Inhalte und Regeln für eine Workflowbenachrichtigung ein, wenn Sie den betreffenden Workflow erstellen. Wählen Sie die Anpassungsoptionen auf der Seite **Workflowreaktionen** für die Workflowreaktion aus, die die Benachrichtigung darstellt. Weitere Informationen finden Sie unter Schritt 9 im Abschnitt [Workflows erstellen](across-how-to-create-workflows.md#to-create-a-workflow).  

* Den Absender benachrichtigen

    Fügen Sie für Genehmigungsworkflows einen Workflow-Antwortschritt hinzu, um den Absender zu benachrichtigen, wenn die Anforderung genehmigt oder abgelehnt wurde. Weitere Informationen finden Sie unter Schritt 9 im Abschnitt [Workflows erstellen](across-how-to-create-workflows.md#to-create-a-workflow).  

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Siehe auch

[Einrichten von Genehmigten Benutzern](across-how-to-set-up-approval-users.md)  
[Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)  
[Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Erstellen eines Workflows](across-how-to-create-workflows.md)  
[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)  
[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)  
[E-Mail einrichten](admin-how-setup-email.md)  
[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]