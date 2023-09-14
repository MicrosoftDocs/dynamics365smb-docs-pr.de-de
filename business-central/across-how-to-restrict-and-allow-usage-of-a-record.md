---
title: So schränken Sie die Verwendung eines Datensatzes ein und lassen sie zu
description: 'Wenn Sie die Verwendung eines Datensatzes einschränken wollen, können Sie zwei Workflow-Reaktionen in einen Workflow einbinden, der die Verwendung des Datensatzes steuert.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
---
# Zulassen und Einschränken des Verbrauchs eines Datensatzes

Wenn Sie verhindern möchten, dass ein Datensatz für bestimmte Aktivitäten verwendet wird (beispielsweise so lange, bis der Datensatz genehmigt wurde), können Sie zwei Workflowantworten in einen Workflow einbauen, der die Verwendung des Datensatzes steuert. Eine Workflowantwort schränkt die Nutzung des Datensatzes entsprechend des definierten Workflowereignis und die der Bedingungen ein. Die andere Workflowantwort läßt die Nutzung des Datensatzes entsprechend des definierten Workflowereignis und die der Bedingungen zu. In der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] sind zwei Antworten für diesen Zweck vorhanden: **Datensatzbeschränkung hinzufügen** und **Aufnahmebeschränkung entfernen**.

> [!NOTE]  
> Die Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt die Beschränkung der Buchung, des Exports als Zahlung und des Druckens als Scheck für einen Datensatz. Um andere Einschränkungen zu unterstützen muss ein Microsoft-Partner den Anwendungscode anpassen.  

> [!NOTE]  
> Die Workflowfunktionalität zur Einschränkung der Nutzung von Datensätzen ist nicht mit der Funktionalität zur Blockierung der Buchung von Artikel-, Debitor- und Kreditordatensätze verknüpft.

Nachfolgend wird beschrieben, wie das Buchen von Bestellungen bis zu deren Genehmigung eingeschränkt werden kann. Der neue Workflow basiert auf der vorhandene Workflowvorlage *Einkaufsrechnungs-Genehmigungsworkflow*.  

## Erstellen Sie einen Workflowschritt, der die Buchung von nicht genehmigten Einkaufsbestellungen einschränkt

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Workflows** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Workflows** die Aktion **Neuer Workflow aus Vorlage**. Weitere Informationen unter [Erstellen von Workflows aus Workflowvorlagen](across-how-to-create-workflows-from-workflow-templates.md).
3. Wählen Sie auf der Seite **Workflowvorlage** die Vorlage *Einkaufsrechnungs-Genehmigungsworkflow* aus.  

   Beachten Sie, dass die ersten beiden Workflowschritte zur Einschränkung und Zulassung der Nutzung von Einkaufsrechnungen dienen. Ändern Sie die Ereignisbedingung des ersten Schritts des neuen Workflows. Legen Sie fest, dass er auf Einkaufsbestellungen angewandt wird.  
4. Wählen Sie im Inforegister **Workflow-Schritte** das Feld **Bei Bedingung** für den ersten Schritt und dann für den Filter **Belegtyp** die Option **Auftrag** aus.  
5. Lösen, bearbeiten oder erstellen Sie andere Workflowschritte, um einen Geschäftsprozess abzudecken der mit der Einschränkung der Buchung von nicht genehmigten Einkaufsbestellungen beginnt.  

## Siehe auch

[Artikelgenehmigungsworkflow verwenden](across-use-workflows.md)  
[Genehmigungsworkflows erstellen](across-how-to-create-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
