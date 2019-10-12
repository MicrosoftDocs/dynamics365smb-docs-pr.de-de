---
title: 'Vorgehensweise: Konvertieren vorhandener Lagerorte in Lagerorte des Lagers | Microsoft Docs'
description: Sie können einen vorhandenen Lagerort aktivieren, um Zonen und Lagerplätze zu verwenden und als Lagerorte zu betreiben.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6319abc70c30117f7789852495501f0ef7605f49
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310446"
---
# <a name="convert-existing-locations-to-warehouse-locations"></a>Konvertieren vorhandener Lagerorte in Lagerorte des Lagers
Sie können einen vorhandenen Lagerort aktivieren, um Zonen und Lagerplätze zu verwenden und als Lagerorte zu betreiben.  

Die Stapelverarbeitung zur Aktivierung eines Lagerorts für den Lagerbetrieb erstellt für alle Artikel mit Bestand in dem Lagerort ursprüngliche Lagerplatzposten für den Ausgleichslagerplatz. Diese ursprünglichen Posten werden ausgeglichen, wenn nach Ausführung der Stapelverarbeitung Lagerinventurposten eingegeben werden.  

Zonen und Lagerplätze können vor oder nach der Umwandlung erstellt werden. Der einzige Lagerort, der vor der Umwandlung erstellt werden muss, ist der Lagerort, der als Ausgleichslagerplatz verwendet werden soll.  

> [!IMPORTANT]  
>  Vor der Änderung des Lagerorts für den Lagerdurchlauf müssen alle negativen Bestände und offenen Logistikbelege bereinigt werden, indem ein Bericht ausgeführt wird, der negative Lagerbestände und offene Logistikbelege für den Lagerort ermittelt. Weitere Informationen finden Sie unter Negativen Bestand überprüfen.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>S aktivieren Sie einen vorhandenen Lagerort für den Lagerbetrieb:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerort erstellen** ein, und wählen dann den zugehörigen Link aus.  
2.  Geben Sie im Feld **Lagerortcode** den Lagerort an, den Sie für die Lagerverarbeitung aktivieren möchten.  
3.  Geben Sie im Feld **Ausgleichslagerplatzcode** den Lagerplatz am Lagerort an, an dem nicht synchronisierte Lagerplatzposten gelagert werden. Weitere Informationen finden Sie unter [So synchronisieren Sie korrigierte Lagerplatzposten mit entsprechenden Artikelposten](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).  

    Mit Hilfe der offenen Artikelposten für den angegebenen werden Lagerort Logistik-Buch.-Blattzeilen erstellt, in denen sämtliche Kombinationen von Artikelnr., Variantencode, Einheitencode sowie ggf. Chargennr. und Seriennr. aus den Artikelposten zusammengefasst sind. Die Logistik Buch.-Blattzeilen werden dann gebucht. Bei der Buchung werden Lagerplatzposten erstellt, durch die der Bestand dem Ausgleichslagerplatz zugeordnet wird. Außerdem wird der **Ausgleichslagerplatzcode** auf der Lagerortkarte eingesetzt.  

4.  Um zu sehen, welche Artikel während der Stapelverarbeitung dem Ausgleichslagerplatz hinzugefügt wurden, können Sie den Bericht  **Ausgleichslagerplatz anpassen** ausführen.  
5.  Nachdem die Stapelverarbeitung   **Lagerort erstellen**abgeschlossen ist, muss eine Lagerinventur ausgeführt und gebucht werden. Weitere Informationen finden Sie unter [Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md)  

> [!NOTE]  
>  Es empfiehlt sich, den Batchauftrag **Lagerort erstellen** zu einem Zeitpunkt ausführen, zu dem er sich im System nicht auf die tägliche Arbeit auswirkt. Dieser Auftrag verarbeitet alle Einträge in der Tabelle **Artikelposten**. Wenn es viele Artikelposten gibt, kann der Auftrag mehrere Stunden dauern.  

 Bei den Lagerorten, für die vor der Umwandlung keine Logistikbelege verwendet wurden, müssen Herkunftsbelege, die vor der Umwandlung teilweise empfangen oder geliefert wurden, erneut geöffnet und freigegeben werden.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
