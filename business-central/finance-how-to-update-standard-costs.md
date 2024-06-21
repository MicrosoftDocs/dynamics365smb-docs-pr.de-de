---
title: Standardkosten aktualisieren
description: Sie müssen die festen Einstandspreise von Komponenten in regelmäßigen Abständen aktualisieren und die neuen Einstandspreise auf den übergeordneten Artikel übertragen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Standardkosten aktualisieren
Sie müssen die festen Einstandspreise von Komponenten in regelmäßigen Abständen aktualisieren und die neuen Einstandspreise auf den übergeordneten Artikel übertragen. Der Prozess besteht in der Regel aus den folgenden vier Schritten:  

1.  Aktualisieren von Kosten auf der Komponenten- und Kapazitätsebene. Weitere Informationen finden Sie unter dem Stapelverarbeitungsauftrag **Artikel Einst.-Preis (fest) vorschlagen**.  
2.  Konsolidieren Sie und rollen Sie Komponenten- und Kapazitätskosten auf, um die Gesamtkosten für Herstellung oder Montage der Artikel zu berechnen.  
3.  Implementieren der festen Einstandspreise, die bei der Ausführung der obigen Batchaufträge eingegeben werden. Die festen Einstandspreise treten erst in Kraft, wenn Sie implementiert werden. Verwenden Sie den Stapelverarbeitungsauftrag **Einst.-Preis (fest) Vorschlag übernehmen**, der die Änderungen der Standardkosten für Artikel mit denen aus der Tabelle „Einst.-Preis (fest) Arbeitsblatt“ aktualisiert.  
4.  Implementieren der Änderungen, um das Feld **Einstandspreis** auf der Artikelkarte zu aktualisieren und eine Lagerneubewertung durchzuführen. Weitere Informationen finden Sie unter [Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md).  

Weitere Informationen finden Sie unter [Über das Berechnen von festen Einstandspreisen](finance-about-calculating-standard-cost.md).
  
## Einstandspreise aktualisieren

1.  Führen Sie die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** aus. Um die Stapelverarbeitung zu starten, wählen Sie die ![Glühbirne, die das „Wie möchten Sie weiter verfahren“-Feature öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerreg. fakt. Einst. Preise anpassen** ein, und wählen Sie dann den entsprechenden Link. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.  
2.  Aufruf der Stapelverarbeitung **Lagerregulierung buchen**. Um die Stapelverarbeitung zu starten, wählen Sie die ![Glühbirne, die das „Wie möchten Sie weiter verfahren“-Feature öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagerkosten ins Hauptbuch buchen** ein, und wählen Sie dann den zugehörigen Link. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.  
3.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Einst.-Preis (fest) Arbeitsblatt** ein und verwenden Sie dann eine oder mehrere der folgenden Aktionen:

    1.  Führen Sie die Stapelverarbeitung **Art. Einst.-Pr. (fest) vorschlagen** aus.  
    2.  Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.  
    3.  Führen Sie die Stapelverarbeitung **Einstandspreis (fest) für Kapazität vorschlagen** aus.  
    4.  Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.
    5. Führen Sie die Stapelverarbeitung **Mehrstufigen Einstandspreis berechnen** aus.
    6.  Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.
    7.  Führen Sie die Stapelverarbeitung **Einst.-Preis (fest) Vorschlag übernehmen** aus.  
4.  Sehen Sie sich das **Neubewertungs Buch.-Blatt** an, das mit Posten aus vorherigen Schritten in diesem Verfahren gefüllt wurde, und buchen Sie es.  

## Siehe auch

 [Informationen zur Berechnung von festen Einstandspreisen](finance-about-calculating-standard-cost.md)   
 [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)   
 [Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)   
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]