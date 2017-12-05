---
title: "Gewusst wie: Beschränken und Zulassen der Nutzung eines Datensatzes | Microsoft Docs"
description: "Wenn Sie verhindern möchten, dass ein Datensatz für bestimmte Aktivitäten verwendet wird (beispielsweise so lange, bis der Datensatz genehmigt wurde), können Sie zwei Workflowantworten in einen Workflow einbauen, der die Verwendung des Datensatzes steuert."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 0dc8b3eeecfbf3f4a96985f4e4adaf0b3a5a21d0
ms.contentlocale: de-de
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-restrict-and-allow-usage-of-a-record"></a>Gewusst wie: Beschränken und Zulassen der Nutzung eines Datensatzes
Wenn Sie verhindern möchten, dass ein Datensatz für bestimmte Aktivitäten verwendet wird (beispielsweise so lange, bis der Datensatz genehmigt wurde), können Sie zwei Workflowantworten in einen Workflow einbauen, der die Verwendung des Datensatzes steuert. Eine Workflowantwort schränkt die Nutzung des Datensatzes entsprechend des definierten Workflowereignis und die der Bedingungen ein. Eine weitere Workflowantwort läßt die Nutzung des Datensatzes entsprechend des definierten Workflowereignis und die der Bedingungen zu. In der generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] stehen zwei Antworten zu diesem Zweck zur Verfügung: **Nutzung eines Datensatzes einschränken** und Zulassen der Nutzung eines Datensatzes. und **Zulassen Verbrauch eines Datensatzes**.

> [!NOTE]  
>  Die generische Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt die Beschränkung der Buchung, des Exports als Zahlung und des Druckens als Scheck für einen Datensatz. Um andere Einschränkungen zu unterstützen muss ein Microsoft-Partner den Anwendungscode anpassen.  

> [!NOTE]  
>  Die Workflowfunktionalität zur Einschränkung der Nutzung von Datensätzen ist nicht mit der Funktionalität zur Blockierung der Buchung von Artikel-, Debitor- und Kreditordatensätze verknüpft.

Nachfolgend wird beschrieben, wie das Buchen von Bestellungen bis zu deren Genehmigung eingeschränkt werden kann. Der neue Workflow basiert auf der vorhandene Workflowvorlage "Einkaufsrechnungs-Genehmigungsworkflow".  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>So erstellen Sie einen Workflowschritt, der die Buchung von nicht genehmigten Einkaufsbestellungen einschränkt  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Workflows** ein und wählen dann den zugehörigen Link aus.  
2. Im Fenster **Workflo** erstellen Sie einen neuen Workflow mit dem Namen "Einkaufsbestellungs-Genehmigungsworkflow". Weitere Informationen finden Sie unter [Gewusst wie: Workflows erstellen](across-how-to-create-workflows.md).  
3. Wählen Sie die Aktion **Von Workflowvorlage kopieren** aus.  
4. Wählen Sie das **Quellworkflow-Code**-Feld aus und wählen Sie dann im Fenster die **Workflowvorlage** "Einkaufsrechnungs-Genehmigungsworkflow" aus.  

     Beachten Sie, dass die ersten beiden Workflowschritte zur Einschränkung und Zulassung der Nutzung von Einkaufsrechnungen dienen. Bearbeiten Sie die Ereignisbedingung des ersten Schritts des neuen Workflows. Legen Sie fest, dass er auf Einkaufsbestellungen angewandt wird.  
5. Wählen Sie im **Workflow-Schritte**-Inforegister das Feld **Ereigniskonditionen** , und wählen Sie dann für den Filter **Dokumentart** die Option **Auftrag** aus.  
6. Lösen, bearbeiten oder erstellen Sie andere Workflowschritte, um einen Geschäftsprozess abzudecken der mit der Einschränkung der Buchung von nicht genehmigten Einkaufsbestellungen beginnt.  

## <a name="see-also"></a>Siehe auch  
[So wird's gemacht: Erstellen von Workflows](across-how-to-create-workflows.md)   
[Workflow](across-workflow.md)   

