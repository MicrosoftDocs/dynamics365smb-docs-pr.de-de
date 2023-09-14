---
title: So erstellen Sie Workflows aus Workflow-Vorlagen
description: 'Um beim Erstellen neuer Genehmigungsworkflows Zeit zu sparen, können Sie nicht editierbare Workflows aus Workflow-Vorlagen erstellen, denen das Kürzel „MS“ vorangestellt ist.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
---
# Erstellen von Workflows aus Workflowvorlagen

Um Zeit zu sparen, wenn Sie neue Genehmigungsworkflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.  

Workflowvorlagen sind nicht-bearbeitbare Workflows, die Sie in der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] finden. Den von Microsoft erstellten Codes für Workflowvorlagen ist „MS-“ vorangestellt.  

Eine andere Art, einen Workflow schnell zu erstellen ist es, einen vorhandenen Workflow zu importieren, den Sie in einer Datei außerhalb von [!INCLUDE[prod_short](includes/prod_short.md)] haben. Erfahren Sie mehr unter [Workflows exportieren und importieren](across-how-to-export-and-import-workflows.md).  

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden. Erfahren Sie mehr unter [Workflows erstellen](across-how-to-create-workflows.md).  

## So erstellen Sie einen Workflow über eine Workflowvorlage

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neuen Workflow aus Vorlage** aus. Die Seite **Workflowvorlagen** wird geöffnet.  
3. Wählen Sie eine Workflowvorlage aus, und dann **OK**.  

   Die Seite **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält. Der Wert im Feld **Code** wird beispielweise mit „-01“ erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Workflowvorlage erstellt wurde.  
4. Fahren Sie fort mit dem Erstellen des Workflows, indem Sie die Workflowschritte bearbeiten oder neue Schritte hinzufügen. Erfahren Sie mehr unter [Workflows erstellen](across-how-to-create-workflows.md).  

## Siehe verwandte [Microsoft Schulungen](/training/modules/create-workflows/)

## Siehe auch

[Genehmigungsworkflows erstellen](across-how-to-create-workflows.md)  
[Exportieren und Importieren von Genehmigungsworkflows](across-how-to-export-and-import-workflows.md)  
[Archivierte Workflowschritt-Instanzen anzeigen](across-how-to-view-archived-workflow-step-instances.md)  
[Artikelgenehmigungsworkflow löschen](across-how-to-delete-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
