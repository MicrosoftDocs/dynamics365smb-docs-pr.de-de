---
title: Genehmigungsworkflows einrichten (enthält Video)
description: 'Legen Sie Workflows, Workflow-Benutzer und Genehmiger fest, um Aufgaben des Geschäftsprozesssystems zu verbinden, die von diesen verschiedenen Benutzern ausgeführt werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: bholtorf
---
# Genehmigungsworkflows einrichten

Sie können Workflows festlegen und verwenden, die von verschiedenen Benutzern ausgeführte Geschäftsprozessaufgaben miteinander verbinden. Systemaufgaben, wie automatische Buchung, können als Schritte in Workflows berücksichtigt werden, vor oder nach Benutzeraufgaben. Die Anforderung oder Bewilligung von Genehmigungen zum Erstellen neuer Datensätze sind typische Workflowschritte. Erfahren Sie mehr unter [Genehmigungsworkflows verwenden](across-use-workflows.md).

Bevor Sie beginnen, Genehmigungsworkflows zu verwenden, müssen Sie Workflowbenutzer und Genehmigungsbenutzer einrichten und angeben, wie Benutzer Benachrichtigungen über Workflowschritte empfangen sollen, und anschließend erstellen Sie Workflows.

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden.

[!INCLUDE[workflow](includes/workflow.md)]

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.

|**Prozess**|**Siehe**|  
|------------|-------------|  
|Einrichten von Workflowbenutzern und Benutzergruppen|[Einrichten von Workflowbenutzern](across-how-to-set-up-workflow-users.md)|  
|Richten Sie Workflowbenutzer ein, die an den Genehmigungsworkflows teilnehmen.|[Genehmigungsbenutzer einrichten](across-how-to-set-up-approval-users.md)|  
|Geben Sie an, wie Workflowbenutzer über Workflowschritte (einschließlich Genehmigungsanforderungen) benachrichtigt werden.|[Einrichten von Workflowbenachrichtigungen](across-setting-up-workflow-notifications.md)|  
|Geben Sie an, ob Benutzer per E-Mail oder Notiz benachrichtigt werden sollen und wie häufig Benachrichtigungen gebucht werden sollen.|[Angeben des Zeitpunkts und der Art des Empfangs von Benachrichtigungen](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Wenn Sie möchten, können Sie den Inhalt der E-Mail-Benachrichtigung anpassen, indem Sie Bericht 1320, Benachrichtigungs-E-Mail ändern.|[Erstellen und Ändern benutzerdefinierter Berichtslayouts](ui-how-create-custom-report-layout.md)|  
|Richten Sie einen SMTP-Server so ein, dass die E-Mail-Kommunikation mit [!INCLUDE[prod_short](includes/prod_short.md)] aktiviert ist.|[E-Mail einrichten](admin-how-setup-email.md)|
|Geben Sie die verschiedenen Schritte eines Workflows mithilfe von Verbindungsworkflowereignissen mit Workflowantworten an.|[Genehmigungsworkflows erstellen](across-how-to-create-workflows.md)|  
|Verwenden Sie Workflowvorlagen, um neue Workflows zu erstellen.|[Erstellen von Genehmigungsworkflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md)|  
|Teilen Sie Workflows mit anderen [!INCLUDE[prod_short](includes/prod_short.md)]-Datenbanken.|[Exportieren und Importieren von Genehmigungsworkflows](across-how-to-export-and-import-workflows.md)|  
|Erfahren Sie anhand eines vollständigen Ablaufs, wie Sie einen Workflow zur Genehmigung von Verkaufsunterlagen einrichten.|[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## Beispiel für einen Genehmigungsworkflow

In diesem Video wird gezeigt, wie ein Workflow eingerichtet wird, bei dem ein Benutzer die Genehmigung eines anderen Benutzers anfordern muss, bevor sie Informationen zu einem vorhandenen Kunden ändern oder einen neuen Kunden erstellen kann.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## Siehe auch

[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Workflow](across-workflow.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Arbeiten mit Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
