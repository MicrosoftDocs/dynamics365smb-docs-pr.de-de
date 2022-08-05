---
title: So erstellen Sie Workflows aus Workflow-Vorlagen
description: Um beim Erstellen neuer Workflows Zeit zu sparen, können Sie nicht editierbare Workflows aus Workflow-Vorlagen erstellen, denen das Kürzel „MS“ vorangestellt ist.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 18a9d4ba7e2865e41d660261a598b1b755c68023
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129703"
---
# <a name="create-workflows-from-workflow-templates"></a>Erstellen von Workflows aus Workflowvorlagen

Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.  

Workflowvorlagen sind nicht-bearbeitbare Workflows, die Sie in der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] finden. Den von Microsoft erstellten Codes für Workflowvorlagen ist „MS-“ vorangestellt.  

Eine andere Art, einen Workflow schnell zu erstellen ist es, einen vorhandenen Workflow zu importieren, den Sie in einer Datei außerhalb von [!INCLUDE[prod_short](includes/prod_short.md)] haben. Weitere Informationen finden Sie in [Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)  

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden. Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>So erstellen Sie einen Workflow über eine Workflowvorlage

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neuen Workflow aus Vorlage** aus. Die Seite **Workflowvorlagen** wird geöffnet.  
3. Wählen Sie eine Workflowvorlage aus, und wählen Sie dann die Schaltfläche **OK**.  

   Die Seite **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält. Der Wert im Feld **Code** wird beispielweise mit „-01“ erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Workflowvorlage erstellt wurde.  
4. Fahren Sie fort mit dem Erstellen des Workflows, indem Sie die Workflowschritte bearbeiten oder neue Schritte hinzufügen. Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Siehe auch

[Erstellen eines Workflows](across-how-to-create-workflows.md)  
[Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)  
[Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md)  
[Löschen eines Workflows](across-how-to-delete-workflows.md)  
[Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Einrichten von Workflows](across-set-up-workflows.md)  
[Verwenden von Workflows](across-use-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]