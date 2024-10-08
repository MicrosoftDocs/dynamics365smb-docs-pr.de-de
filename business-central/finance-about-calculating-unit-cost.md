---
title: Informationen zur Einstandspreisberechnung
description: 'Erfahren Sie, wie die Kalkulationsmethode und andere Faktoren das Feld Stückkosten auf der Artikelkarte beeinflussen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: article
ms.date: 07/29/2024
---

# <a name="about-unit-cost-calculation"></a>Informationen zur Einstandspreisberechnung

Jeder Artikel hat einen Einheitspreis, der basierend auf der Kostenmethode des Unternehmens und anderen Faktoren berechnet wird. Bei der Lagerabgangsmethode *Standard* basiert der Wert im Feld **Einstandspreis** grundsätzlich auf den Standardkosten für den Artikel. Bei allen anderen Lagerabgangsmethoden (*FIFO*, *LIFO*, *Spezifisch* und *Durchschnitt*) wird der Einstandspreis basierend auf dem durchschnittlichen Einstandspreis über einen bestimmten Zeitraum berechnet.  

Weitere Informationen finden Sie unter [Lagerbestandkosten verwalten](finance-manage-inventory-costs.md).  

## <a name="when-is-the-unit-cost-field-updated"></a>Wann wird das Feld „Einstandspreis“ aktualisiert

Die ausgewählte Lagerabgangsmethode beeinflusst den Zeitpunkt der Aktualisierung im Feld **Einstandspreis**.

Wenn die Lagerabgangsmethode auf *Standard* festgelegt ist, wird das Feld **Einstandspreis** aktualisiert, wenn die Standardkosten geändert werden, und Benutzer können das Feld **Einstandspreis** nicht bearbeiten. Weitere Informationen finden Sie unter [Standardkosten aktualisieren](finance-how-to-update-standard-costs.md).

Bei den Lagerabgangsmethoden *FIFO*, *LIFO*, *Spezifisch* oder *Durchschnitt* wird das Feld **Einstandspreis** in den folgenden Fällen aktualisiert:

* Wenn der Preis des Artikels automatisch oder durch die Aufgabe [Einstandspreisregulierung](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually) reguliert wurde.
* Während der Buchung von Einkaufsrechnungen, Ausgaben oder Zugängen, wenn eine der folgenden Bedingungen zutrifft:
  * Der fakturierte Bestand des Artikels ändert sich von einem negativen bzw. Nullbestand in einen positiven Bestand.
  * Der aktuelle Einstandspreis ist Null.

Wenn eine dieser Bedingungen zutrifft, wird das Feld **Einstandspreis** mit dem Wert im Feld **EK-Preis (neuester)** auf der Artikelkarte aktualisiert.

> [!NOTE]
> Das Feld **Einstandspreis** wird nicht aktualisiert, wenn der aktuelle Eilnstandspreis höher als Null und der neue Einstandspreis Null ist. Ein Einstandspreis von Null wird als Ausnahme vom regulären Geschäft betrachtet. Daher wird der aktuelle Einstandspreis beibehalten, um den letzten bekannten, relevanten Wert, bereitzustellen. Diese Ausnahme gilt auch dann, wenn der vorhandene Lagerbestand auf Null neu bewertet wurde.

Im Feld **Einstandspreis** auf der Artikelkarte können Sie einen Drilldown durchführen, um den Verlauf von Transaktionen anzuzeigen, aus denen der verfügbare durchschnittliche Einstandspreis im Fenster **Einst.-Pr. (durchschn.)-Ber., Übersicht** berechnet wird.

## <a name="unit-cost-calculation-for-purchases"></a>Einstandspreisberechnung bei Einkäufen

Wenn Sie Artikel einkaufen, wird der Wert im Feld **EK-Preis (neuester)** auf der Artikelkarte in das Feld **EK-Preis** einer Einkaufszeile oder in die Zeile **Stückpreis** einer Artikel Buch.-Blattzeile kopiert.

Ihre Auswahl im Feld **Kostenermittlungsmethode** hat Einfluss darauf, wie [!INCLUDE[prod_short](includes/prod_short.md)] den Inhalt des Feldes **Einstandspreis** in den Zeilen berechnet.

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Lagerabgangsmethode „FIFO“, „LIFO“, „Ausgewählt“ oder „Durchschnitt“

[!INCLUDE[prod_short](includes/prod_short.md)] berechnet den Inhalt des Feldes **Einstandspreis NW** in der Einkaufszeile oder den Inhalt des Feldes **Einstandspreis** in der Artikel Buch.-Blattzeile entsprechend dieser Formel:

*Einstandspreis (MW) = (EK-Preis - (Rabattbetrag / Menge)) x (1 + Indirekte Kosten % / 100) + Gemeinkostensatz*

### <a name="costing-method-standard"></a>Lagerabgangsmethode „Standard“

Die Anwendung füllt das Feld **Einstandspreis (MW)** in einer Einkaufszeile oder das Feld **Einstandspreis** in einer Artikel Buch.-Blattzeile, indem sie den Wert des Felds **Einstandspreis** von der Artikelkarte kopiert. Wenn die Lagerabgangsmethode *Standard* ist, basiert dieser Wert auf dem Einstandspreis.

Wenn Sie den Einkauf buchen, verwendet [!INCLUDE[prod_short](includes/prod_short.md)] den Einstandspreis aus der Einkaufszeile bzw. der Artikel Buch.-Blattzeile in den Rechnungsposten des eingekauften Artikels kopiert. Sie können ihn in der Postenübersicht des Artikels einsehen.

### <a name="all-costing-methods"></a>Alle Lagerabgangsmethoden

Die Anwendung verwendet immer den Einstandspreis aus der Herkunftsbelegzeile, um den Inhalt des Feldes **Einstandsbetrag (tatsächl.)** oder, falls anwendbar, des Feldes **Einstandsbetrag (erwartet)** zu berechnen, das zu diesem Artikelposten gehört, unabhängig von der Lagerabgangsmethode des Artikels.

## <a name="unit-cost-calculation-for-sales"></a>Einstandspreisberechnung für Verkäufe

Wenn Sie Artikel verkaufen, kopiert die Anwendung den Einstandspreis immer aus dem Feld **Einstandspreis** der Artikelkarte in die Verkaufszeile oder die Artikel Buch.-Blattzeile.

Beim Buchen wird später der Einstandspreis in den Artikelposten der Verkaufsrechnung übernommen; er wird darüber hinaus in den Artikelposten des jeweiligen Artikels angezeigt. [!INCLUDE[prod_short](includes/prod_short.md)] verwendet den Einstandspreis aus der Herkunftsbelegzeile, um den Inhalt des Feldes **Einstandsbetrag (tatsächl.)** oder, falls anwendbar, des Feldes **Einstandsbetrag (erwartet)** in dem Wertposten zu berechnen, der mit diesem Artikelposten verknüpft ist.

## <a name="see-also"></a>Siehe auch

[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)    
[Neue Artikel registrieren](inventory-how-register-new-items.md)    
[Informationen zur Bestandskostenrechnung](finance-learn-about-costing.md)    
[Lagerbest](inventory-manage-inventory.md)   
[Verkauf](sales-manage-sales.md)    
[Einkauf](purchasing-manage-purchasing.md)    
[Designdetails: Nicht abziehbare MwSt.](design-details-nondeductible-vat.md)  
[Best Practices für die Einrichtung: Kostenrechnungsmethode](setup-best-practices-costing-method.md)    
[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)    
[Designdetails: Kostenregulierung](design-details-cost-adjustment.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
