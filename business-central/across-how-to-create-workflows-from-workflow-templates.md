---
title: 'Vorgehensweise: Workflows von Workflowvorlagen erstellen | Microsoft Docs'
description: Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 407bf7cd60416a178e9ec8a5d0b154a7583e87e1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754842"
---
# <a name="create-workflows-from-workflow-templates"></a>Erstellen von Workflows aus Workflowvorlagen
Um Zeit zu sparen, wenn Sie neue Workflows erstellen, können Sie Workflows aus Workflowvorlagen erstellen.  

 Workflowvorlagen sind nicht-bearbeitbare Workflows, die Sie in der generischen Version von [!INCLUDE[prod_short](includes/prod_short.md)] finden. Dem Code für von Microsoft hinzugefügte Workflowvorlagen ist „MS-“ vorangestellt.  

 Eine andere Art, einen Workflow schnell zu erstellen ist es, einen vorhandenen Workflow zu importieren, den Sie in einer Datei außerhalb von [!INCLUDE[prod_short](includes/prod_short.md)] haben. Weitere Informationen finden Sie in [Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)  

Auf der Seite **Workflow** können Sie einen Workflow erstellen, indem Sie die entsprechenden Schritte in den Zeilen auflisten. Jeder Schritt besteht aus einem durch Ereignisbedingungen moderiertem Workflowereignis und einer durch Antwortoptionen moderierten Workflowantwort. Sie definieren Workflowschritte, indem Sie die Felder in Workflowzeilen mit Ereignis- und Antwortwerten aus festen Listen ausfüllen, die die Workflowszenarien darstellen, die durch den Anwendungscode unterstützt werden. Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Vorgehensweise: Workflows von Workflowvorlagen erstellen  
1.  Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Workflows** ein und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Workflow von Vorlage erstellen** aus. Die Seite **Workflowvorlagen** wird geöffnet.  
3.  Wählen Sie eine Workflowvorlage aus, und wählen Sie dann die Schaltfläche **OK**.  

     Die Seite **Workflow** wird für einen neuen Workflow geöffnet, der alle Informationen der ausgewählten Vorlage enthält. Der Wert im Feld **Code** wird beispielweise mit "-01 " erweitert. Dies zeigt an, dass dies der erste Workflow ist, der von der Workflowvorlage erstellt wurde.  
4.  Fahren Sie fort mit dem Erstellen des Workflows, indem Sie die Workflowschritte bearbeiten oder neue Schritte hinzufügen. Weitere Informationen finden Sie unter [Workflows erstellen](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Siehe auch  
 [Erstellen eines Workflows](across-how-to-create-workflows.md)   
 [Exportieren und Importieren von Workflows](across-how-to-export-and-import-workflows.md)   
 [Anzeigen von archivierten Workflowschritt-Instanzen](across-how-to-view-archived-workflow-step-instances.md)   
 [Löschen eines Workflows](across-how-to-delete-workflows.md)   
 [Exemplarische Vorgehensweise: Einrichten und Nutzen eines Einkaufsgenehmigungsworkflows](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Einrichten von Workflows](across-set-up-workflows.md)   
 [Verwenden von Workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   
