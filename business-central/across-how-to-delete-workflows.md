---
title: So löschen Sie Genehmigungsworkflows
description: 'Wenn Sie sicher sind, dass ein Workflow nicht mehr verwendet wird, können Sie ihn löschen. Alle im Workflow definierten Workflow-Schrittinstanzen müssen den Status **Erledigt** haben.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '1500,'
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="delete-approval-workflows"></a>Genehmigungsworkflows löschen

Wenn Sie sicher sind, dass ein Workflow nicht mehr verwendet wird, können Sie ihn löschen. Alle im Workflow definierten Workflow-Schrittinstanzen müssen den Status **Abgeschlossen** haben.

> [!CAUTION]
> Wenn Sie einen Workflow löschen, gehen alle Informationen im Workflow verloren.

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden. Erfahren Sie mehr unter [Genehmigungsworkflows erstellen](across-how-to-create-workflows.md).

## <a name="delete-a-workflow"></a>Löschen eines Workflows

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den zu löschenden Workflow aus.
3. Wählen Sie die Aktion **Löschen** aus.
4. Öffnen Sie alternativ den Workflow, den Sie löschen möchten.
5. Wählen Sie im Fenster **Workflow** die Aktion **Löschen** aus.

> [!NOTE]
> Um einen Workflow zu löschen, muss er deaktiviert werden. Um einen Workflow zu deaktivieren, öffnen Sie ihn auf der Seite **Workflows** und schalten Sie **Aktiviert** aus.

## <a name="see-also"></a>Siehe auch

[Genehmigungsworkflows erstellen](across-how-to-create-workflows.md)  
[Genehmigungsworkflow aktivieren](across-how-to-enable-workflows.md)  
[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Archivierte Workflowschritt-Instanzen anzeigen](across-how-to-view-archived-workflow-step-instances.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
