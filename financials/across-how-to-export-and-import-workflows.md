---
title: 'Vorgehensweise: Exportieren und Importieren von Workflows | Microsoft Docs'
description: "Um Workflows auf andere  [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datenbanken zu übertragen, beispielsweise um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Workflows exportiert und importiert werden."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8126d3850103819e885d9d131ca3074f1b7cfda1
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

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

