---
title: So sperren Sie Artikel oder Artikelvarianten für den Verkauf oder Einkauf
description: Sie können Positionen und Positionsvarianten für die Eingabe in Zeilen von Verkaufs- oder Einkaufsbelegen sowie für die Buchung in einer Transaktion sperren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 08/22/2023
ms.service: dynamics-365-business-central
---
# Artikel oder Artikelvarianten für den Verkauf oder Einkauf sperren

Sie können Artikel und Artikelvarianten für die Eingabe in Zeilen von Verkaufs- oder Einkaufsbelegen und für die Buchung in Transaktionen sperren. Dies ist beispielsweise nützlich, wenn ein Artikel einen bekannten Fehler aufweist. Wenn jemand in einem Verkaufs- oder Einkaufsbeleg einen gesperrten Artikel oder eine Artikelvarianten auswählt, wird er durch eine Nachricht darüber informiert, dass der Artikel gesperrt ist.

In der folgenden Tabelle wird beschrieben, was geschieht, wenn Artikel und Artikelvarianten gesperrt sind.  

|Option|Description|  
|--------------------|------------|  
|**Verkauf gesperrt**|Sie können den Artikel oder die Variante nicht in einem Verkaufsbeleg oder einem Verkaufsartikeljournal auswählen.|  
|**Einkauf gesperrt**|Sie können den Artikel oder die Variante nicht in einem Einkaufsbeleg, einem Einkaufspositionsjournal oder in Einkaufsplanungsprozessen auswählen.|  
|**Gesperrt**|Sie können den Artikel oder die Variante nicht einbeziehen, wenn Sie Transaktionen buchen.|  

> [!NOTE]
> Blockierte Artikel können zurückgesendet werden. Das bedeutet, dass keine der obigen Einstellungen für Retouren und Gutschriften gilt.

Wenn Sie die Aktion **Aus Dokument kopieren** verwenden, um neue Belege auf der Grundlage vorhandener Belege zu erstellen, werden Sie benachrichtigt, wenn Artikel oder Varianten in den Zeilen des Quellbelegs blockiert sind. Die gesperrten Belegzeilen werden vom neuen Beleg ausgeschlossen, und eine Benachrichtigung zeigt eine Übersicht aller Belegzeilen, die im Quellbeleg gesperrt sind.

## So blockieren Sie einen Artikel  

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol einrichten möchten, geben Sie **Artikel** ein und wählen dann den entsprechenden Link.  
2. Je nachdem, was Sie tun möchten, markieren Sie das Element und wählen dann eines oder mehrere der folgenden Kontrollkästchen:
    * **Gesperrt**
    * **Verkauf gesperrt**
    * **Einkauf gesperrt**  

## So blockieren Sie eine Variante  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol einrichten möchten, geben Sie **Artikel** ein und wählen dann den entsprechenden Link.  
2. Wählen Sie den Artikel aus, dessen Variante Sie blockieren möchten, und wählen Sie **Varianten**, und wählen Sie dann eines oder mehrere der folgenden Kontrollkästchen aus:  
    * **Gesperrt**
    * **Verkauf gesperrt**
    * **Einkauf gesperrt**

## Siehe auch  

[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]