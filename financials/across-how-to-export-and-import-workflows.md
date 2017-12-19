---
title: 'Vorgehensweise: Exportieren und Importieren von Workflows | Microsoft Docs'
description: "Um Workflows auf andere Dynamics 365-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden."
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
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 520c81b9c550b4ef29b077685541a2e7ea30d4d7
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-export-and-import-workflows"></a>Vorgehensweise: Exportieren und Importieren von Workflows
Um Workflows auf andere [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden.  

 Eine andere Art, Workflows schnell zu erstellen, besteht darin, Workflows aus Workflow-Vorlagen zu erstellen. Weitere Informationen finden Sie unter [Gewusst wie: Workflows von Workflow-Vorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md).  

 Im Fenster **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden. Weitere Informationen finden Sie unter [Gewusst wie: Workflows erstellen](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>So exportieren Sie ein Workflow  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflows** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie einen Workflow, und wählen die **In Datei exportieren** Aktion aus.  
3.  Klicken Sie im Fenster **Datei exportieren** auf die Schaltfläche **Speichern**.  
4.  Wählen Sie im Fenster **Exportieren** einen Dateistandort aus, und wählen Sie dann die Schaltfläche **Speichern** aus.  

## <a name="to-import-a-workflow"></a>So importieren Sie einen Workflow  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflows** ein und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Importieren aus Datei** aus.  
3.  Wählen Sie im Fenster **Importieren** die XML-Datei aus, die den Workflow enthält, und wählen Sie dann die Schaltfläche **Öffnen**.  

> [!CAUTION]  
>  Wenn der Workflowcode bereits in der Datenbank vorhanden ist, werden die Workflowschritte mit den Schritten im importierten Workflow überschrieben.  

## <a name="see-also"></a>Siehe auch  
 [So wird's gemacht: Erstellen von Workflows](across-how-to-create-workflows.md)   
 [Vorgehensweise: Workflows von Workflowvorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md)   
 [Gewusst wie: Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md)   
 [So wird's gemacht: Löschen von Workflows](across-how-to-delete-workflows.md)   
 [Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsanfrage-Genehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Einrichten von Workflows](across-set-up-workflows.md)   
 [Verwenden von Workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   

