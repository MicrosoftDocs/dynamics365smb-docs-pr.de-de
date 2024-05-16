---
title: So erstellen Sie Workflows aus Workflow-Vorlagen
description: 'Um Zeit zu sparen, wenn Sie neue Genehmigungsworkflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dajoo
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Workflows aus Workflowvorlagen erstellen

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie in den Zeilen eine Reihe von Workflowschritten erstellen. Jeder Schritt besteht aus einem durch Workflowereignis (Wenn-Ereignis), moderierten Ereignisbedingungen (Bei-Bedingung) und einer durch Antwortoptionen moderierten Workflowreaktion (Dann-Antwort). Die Felder in den Workflowzeilen bieten eine feste Liste an Ereignis- und Antwortwerten, welche die von [!INCLUDE [prod_short](includes/prod_short.md)] unterstützten Szenarien darstellen. Erfahren Sie mehr unter [Workflows erstellen](across-how-to-create-workflows.md).

Um Zeit zu sparen, wenn Sie Genehmigungsworkflows erstellen, stellt [!INCLUDE [prod_short](includes/prod_short.md)] Workflowvorlagen bereit. Die Vorlagen sind auf der Seite **Workflowvorlagen** verfügbar. Sie können die Vorlagen unverändert verwenden oder an Ihre Anforderungen anpassen. Den von Microsoft für die Workflowvorlagen erstellten Codes ist **MS-** vorangestellt.

[!INCLUDE [workflow-next-step](includes/workflow-next-step.md)]

Wenn Sie eine Workflowvorlage ändern, die Änderung aber später bereuen, verwenden Sie die Aktion **Microsoft-Vorlagen zurücksetzen**, um die ursprüngliche Einstellung für den Workflow wiederherzustellen.

> [!CAUTION]
> Die Aktion **Microsoft-Vorlagen zurücksetzen** setzt alle Microsoft-Workflow-Vorlagen zurück. Sie können keine einzelne Vorlage zurücksetzen.  

Eine andere Möglichkeit, einen Workflow schnell zu erstellen, besteht darin, ihn zu importieren, beispielsweise wenn Sie ihn aus einer anderen Instanz von [!INCLUDE[prod_short](includes/prod_short.md)] exportiert haben. Erfahren Sie mehr unter [Workflows exportieren und importieren](across-how-to-export-and-import-workflows.md).  

## So erstellen Sie einen Workflow über eine Workflowvorlage

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neuen Workflow aus Vorlage** aus. Die Seite **Workflowvorlagen** wird geöffnet.  
3. Wählen Sie eine Workflowvorlage aus, und dann **OK**.  

   Die Seite **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält. Der Wert im Feld **Code** wird beispielweise mit „-01“ erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Workflowvorlage erstellt wurde.  
4. Um den Workflow anzupassen, bearbeiten Sie die Workflowschritte oder fügen Sie neue Schritte hinzu. Erfahren Sie mehr unter [Workflows erstellen](across-how-to-create-workflows.md).  

## Siehe auch

[Genehmigungsworkflows erstellen](across-how-to-create-workflows.md)  
[Genehmigungsworkflows exportieren und importieren](across-how-to-export-and-import-workflows.md)  
[Archivierte Workflowschritt-Instanzen anzeigen](across-how-to-view-archived-workflow-step-instances.md)  
[Artikelgenehmigungsworkflow löschen](across-how-to-delete-workflows.md)  
[Beispielhafte Vorgehensweise: Einrichten und Verwenden eines Workflows zur Genehmigung von Käufen](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Genehmigungsworkflows einrichten](across-set-up-workflows.md)  
[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
