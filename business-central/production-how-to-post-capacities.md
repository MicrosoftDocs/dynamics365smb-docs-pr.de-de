---
title: Kapazität buchen
description: 'Buchen Sie verbrauchte Kapazitäten, die nicht dem Produktionsauftrag zugeordnet sind, im Kapazitätsjournal und zeigen Sie gebuchte Kapazitäten auf der Seite Kapazitätsbucheinträge an.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5832, 99000802, 99000820'
ms.date: 03/08/2023
ms.author: bholtorf
---
# <a name="post-capacities"></a>Kapazität buchen

Im Kapazitäts Buch.-Blatt buchen Sie verbrauchte Kapazität, die keinem Fertigungsauftrag zugeordnet ist. Zum Beispiel: Wartungsarbeit muss einem Arbeitsplatz oder einer Arbeitsplatzgruppe zugeordnet werden, aber nicht einem Fertigungsauftrag.  

## <a name="to-post-capacities"></a>Kapazitäten buchen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kapazitäts Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder **Buchungsdatum** und **Belegnr.** aus.  
3. Geben Sie in das Feld **Art** die Art der Kapazität entweder **Arbeitsplatz** oder **Arbeitsplatzgruppe** ein, die Sie buchen möchten.  
4. Geben Sie im Feld **Nr.** Geben Sie die Nummer des Arbeitsplatzes oder der Arbeitsplatzgruppe ein.  
5. Geben Sie in den anderen Feldern die entsprechenden Daten, wie zum Beispiel **Startzeit**, **Endzeit**, **Menge** und **Ausschuss** ein.  
6. Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-work-center-ledger-entries"></a>Um sich die Arbeitsplatzgruppeneinträge anzeigen zu lassen:

Auf den Seiten **Arbeitsplatzgruppenkarte** und **Arbeitsplatzkarte** können Sie gebuchte Kapazität aufgrund der Informationen zu beendeten Fertigungsaufträgen anzeigen.    
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Arbeitsplatzgruppen** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die relevante Karte **Arbeitsplatzgruppe** aus der Liste, und wählen Sie die **Kapazitätsposten** Aktion aus.  

    Auf der Seite **Kapazitätsposten** werden die gebuchten Posten der Arbeitsplatzgruppe in der Reihenfolge der Buchungen angezeigt.   

## <a name="see-also"></a>Siehe auch

[Produktion](production-manage-manufacturing.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)  
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
