---
title: 'Vorgehensweise: Workflows von Workflowvorlagen erstellen | Microsoft Docs'
description: "Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: be25518b225b479d5db21b7014817743f28837bd
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="create-workflows-from-workflow-templates"></a>Erstellen von Workflows aus Workflowvorlagen
Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.  

 Workflowvorlagen sind nicht-bearbeitbare Workflows, die Sie in der generischen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] finden. Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS-“ vorangestellt.  

 Eine andere Art, einen Workflow schnell zu erstellen ist es, einen vorhandenen Workflow zu importieren, den Sie in einer Datei außerhalb von [!INCLUDE[d365fin](includes/d365fin_md.md)] haben. Weitere Informationen finden Sie in [Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)  

Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden. Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Vorgehensweise: Workflows von Workflowvorlagen erstellen  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflows** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Workflow von Vorlage erstellen** aus. Das Fenster **Workflowvorlagen** wird geöffnet.  
3.  Wählen Sie eine Workflowvorlage aus, und wählen Sie dann die Schaltfläche **OK**.  

     Das Fenster **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält. Der Wert im Feld **Code** wird beispielweise mit "-01 " erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Workflowvorlage erstellt wurde.  
4.  Fahren Sie fort mit dem Erstellen des Workflows, indem Sie die Workflowschritte bearbeiten oder neue Schritte hinzufügen. Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Siehe auch  
 [Erstellen eines Workflows](across-how-to-create-workflows.md)   
 [Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)   
 [Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md)   
 [Löschen eines Workflows](across-how-to-delete-workflows.md)   
 [Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Einrichten von Workflows](across-set-up-workflows.md)   
 [Verwenden von Workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   

