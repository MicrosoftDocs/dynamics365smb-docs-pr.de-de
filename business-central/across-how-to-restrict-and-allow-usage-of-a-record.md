---
title: So schränken Sie die Verwendung eines Datensatzes ein und lassen sie zu
description: Wenn Sie die Verwendung eines Datensatzes einschränken wollen, können Sie zwei Workflow-Reaktionen in einen Workflow einbinden, der die Verwendung des Datensatzes steuert.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7873091d64e55460986437cf255d98cd0d00b6d3
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130145"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Zulassen und Einschränken des Verbrauchs eines Datensatzes

Wenn Sie verhindern möchten, dass ein Datensatz für bestimmte Aktivitäten verwendet wird (beispielsweise so lange, bis der Datensatz genehmigt wurde), können Sie zwei Workflowantworten in einen Workflow einbauen, der die Verwendung des Datensatzes steuert. Eine Workflowantwort schränkt die Nutzung des Datensatzes entsprechend des definierten Workflowereignis und die der Bedingungen ein. Eine weitere Workflowantwort läßt die Nutzung des Datensatzes entsprechend des definierten Workflowereignis und die der Bedingungen zu. In der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] sind zwei Antworten für diesen Zweck vorhanden: **Datensatzbeschränkung hinzufügen** und **Aufnahmebeschränkung entfernen**.

> [!NOTE]  
> Die Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt die Beschränkung der Buchung, des Exports als Zahlung und des Druckens als Scheck für einen Datensatz. Um andere Einschränkungen zu unterstützen muss ein Microsoft-Partner den Anwendungscode anpassen.  

> [!NOTE]  
> Die Workflowfunktionalität zur Einschränkung der Nutzung von Datensätzen ist nicht mit der Funktionalität zur Blockierung der Buchung von Artikel-, Debitor- und Kreditordatensätze verknüpft.

Nachfolgend wird beschrieben, wie das Buchen von Bestellungen bis zu deren Genehmigung eingeschränkt werden kann. Der neue Workflow basiert auf der vorhandene Workflowvorlage „Einkaufsrechnungs-Genehmigungsworkflow“.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>So erstellen Sie einen Workflowschritt, der die Buchung von nicht genehmigten Einkaufsbestellungen einschränkt

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Workflows** die Aktion **Neuer Workflow aus Vorlage**. Weitere Informationen finden Sie unter [Workflows von Workflow-Vorlagen erstellen](across-how-to-create-workflows-from-workflow-templates.md).
3. Wählen Sie auf der Seite **Workflowvorlage** die Vorlage *Einkaufsrechnungs-Genehmigungsworkflow* aus.  

   Beachten Sie, dass die ersten beiden Workflowschritte zur Einschränkung und Zulassung der Nutzung von Einkaufsrechnungen dienen. Bearbeiten Sie die Ereignisbedingung des ersten Schritts des neuen Workflows. Legen Sie fest, dass er auf Einkaufsbestellungen angewandt wird.  
4. Wählen Sie im Inforegister **Workflow-Schritte** das Feld **Bei Bedingung** für den ersten Schritt und dann für den Filter **Belegtyp** die Option **Auftrag** aus.  
5. Lösen, bearbeiten oder erstellen Sie andere Workflowschritte, um einen Geschäftsprozess abzudecken der mit der Einschränkung der Buchung von nicht genehmigten Einkaufsbestellungen beginnt.  

## <a name="see-also"></a>Siehe auch

[Erstellen eines Workflows](across-how-to-create-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]