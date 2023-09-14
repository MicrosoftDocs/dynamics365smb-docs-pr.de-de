---
title: So teilen Sie die Zeilen für Lager-Aktivitäten
description: 'Erfahren Sie, wie Sie Lageraktivitäten-Zeilen aufteilen können, wenn die verfügbare Kapazität auf einem vorgeschlagenen Lagerplatz nicht ausreicht.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 9314, 9313, 9315, 9330'
---
# Lageraktivitätszeilen aufzuteilen

In Einlagerungen, Lagerplatzumlagerungen oder Kommissionierungen und in Lagereinlagerungen und Lagerkommissionierungen werden Lagerplätze für das Kommissionieren oder Einlagern von Artikeln vorgeschlagen. Die Menge, die tatsächlich im vorgeschlagenen Lagerplatz vorhanden ist, ist möglicherweise nicht ausreichend, oder in dem Lagerplatz ist nicht genügend Platz, um die erforderliche Menge einzulagern. In diesen Fällen können Sie die Zeile aufteilen, so dass die Artikel für eine Zeile entweder aus mehr als einem Lagerplatz entnommen oder in mehr als einen Lagerplatz eingelagert werden.  

Das folgende Verfahren gilt für die folgenden Lagerbelege:

* Lagereinlagerungen
* Lagerplatzumlagerungen
* Lagerkommissionierungen
* Lagereinlagerungen
* Lagerbestandsumlagerungen
* Lagerkommissionierungen  

## Um Lageraktivitätszeilen aufzuteilen  

1. Öffnen Sie eine Lageraktivitätszeile, in der Sie versuchen, eine nicht ausreichende Menge zu bearbeiten.  
2. Geben Sie im Feld **Bewegungsmenge** die reduzierte Menge ein, die Sie bearbeiten können.  
3. Wählen Sie im Inforegister **Zeilen** die Aktion **Aktionen**, dann die Aktion **Funktionen** und die Aktion **Zeile aufteilen** aus. Eine neue Zeile erscheint. Die Zeile ist eine Kopie der Originalzeile. Einziger Unterschied: Das Feld **Bewegungsmenge** enthält die Menge, die aus der ursprünglichen Zeile entfernt wurde.  
4. Ordnen Sie dieser neuen Zeile einen Lagerplatz zu, und eine Zone, wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden, oder setzen Sie das Aufteilen der Zeile so lange fort, wie es erforderlich ist, um geeignete Lagerplätze für die gesamte Menge zu finden.  

> [!NOTE]  
> Wenn der Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet und Sie die Zeilen aufteilen, müssen Sie sich mit dem Lager auskennen und in der Lage sein, einen Lagerplatz auszuwählen, der den Lageranforderungen des Artikels und den allgemeinen Anforderungen des Logistikbelegs entspricht. Sie würden z. B. nicht eine Zeile eines Kommissionierbelegs aufteilen und einige der Artikel in den Palettenlagerplätzen einlagern.  

## Weitere Informationen  

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]