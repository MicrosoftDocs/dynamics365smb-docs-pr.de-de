---
title: Vorgehensweise beim Exportieren und Importieren von Genehmigungsworkflows
description: 'Um Workflows auf andere Business Central-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="export-and-import-approval-workflows"></a>Exportieren und Importieren von Genehmigungsworkflows

Um Workflows auf andere [!INCLUDE[prod_short](includes/prod_short.md)]-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden.  

Eine andere Art, Workflows schnell zu erstellen, besteht darin, Workflow-Vorlagen zu verwenden. Weitere Informationen unter [Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md).  

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden. Erfahren Sie mehr unter [Workflows erstellen](across-how-to-create-workflows.md).  

## <a name="export-a-workflow"></a>Workflow exportieren

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie einen Workflow, und wählen die **In Datei exportieren** Aktion aus.  

## <a name="import-a-workflow"></a>Workflow importieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Importieren aus Datei** aus.  
3. Wählen Sie auf der Seite **Importieren** die Option **Wählen** aus und wählen Sie die XML-Datei aus, die den Workflow enthält, und wählen Sie dann **Öffnen**.  

> [!CAUTION]  
> Wenn der Workflowcode bereits in der Datenbank vorhanden ist, werden die Workflowschritte mit den Schritten im importierten Workflow überschrieben.  

## <a name="see-also"></a>Siehe auch

[Genehmigungsworkflows erstellen](across-how-to-create-workflows.md)  
[Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md)  
[Archivierte Workflowschritt-Instanzen anzeigen](across-how-to-view-archived-workflow-step-instances.md)  
[Artikelgenehmigungsworkflow löschen](across-how-to-delete-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
