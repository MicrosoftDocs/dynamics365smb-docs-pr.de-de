---
title: Designdetails – Erwartete Kostenbuchung
description: 'Soll-Kosten repräsentieren die Schätzung der Kosten, z. B. für die Kosten eines Einkaufsartikels, die Sie registrieren, bevor Sie die Rechnung für den Artikel erhalten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/20/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Designdetails: Soll-Kosten-Buchen
Soll-Kosten repräsentieren die Schätzung der Kosten, z. B. für die Kosten eines Einkaufsartikels, die Sie registrieren, bevor Sie die Rechnung für den Artikel erhalten.  

 Sie können Soll-Kosten buchen, um sowie Fibu-Posten in den Lagerbestand zurückgeführt. Wenn Sie eine Menge buchen, die nur erhalten oder geliefert, aber nicht fakturiert wurde, kann ein Wertposten mit den Soll-Kosten erstellt werden. Diese Soll-Kosten beeinflussen den Lagerwert, werden aber nicht in der Finanzbuchhaltung gebucht, es sei denn, das System wird entsprechend eingerichtet.  

> [!NOTE]  
>  Soll-Kosten werden nur für Artikeltransaktionen verwaltet. Soll-Kosten sind nicht für immaterielle Transaktionstypen, wie etwa Kapazität und Artikel Zu-/Abschläge.  

 Wenn nur der Mengenteil eine Bestandserhöhung gebucht wurde, dann ändert sich der Lagerwert in der Finanzbuchhaltung nicht, es sei denn, Sie haben das Kontrollkästchen E**rwartete Soll-Kosten buchen** auf der Seite **Bestand einrichten** ausgewählt. In diesem Fall werden die Soll-Kosten auf Interimskonten zum Zeitpunkt des Wareneingangs gebucht. Nachdem der Wareneingang vollständig fakturiert wurde, werden die Interimskonten ausgeglichen und die Ist-Kosten werden im Lagerkonto gebucht.  

 Um Abstimmung und Verfolgbarkeit zu unterstützen, zeigt der fakturierte Wertposten den Soll-Kostenbetrag, der zum Ausgleichen der Interimskonten gebucht wurde.  

## Voraussetzungen für die Buchung der erwarteten Kosten

Um die erwarteten Kosten buchen zu können, müssen Sie Folgendes tun:
1. Aktivieren Sie auf der Seite **Lager-Einrichtung** das Kontrollkästchen **Automatische Kostenbuchung** und das Kontrollkästchen **Soll-Kosten buchen**.
2. Legen Sie fest, welche Interimskonten während des erwarteten Kostenbuchungsprozesses verwendet werden sollen.  

  Überprüfen Sie auf der Seite **Lagerbuchungseinrichtung** die Felder **Lagerkonto** und **Lagerkonto (Interim)** auf den **Lagerortcode und Lagerbuchungsgruppencode** des Artikels, den Sie kaufen möchten. Weitere Informationen zu diesen Konten finden Sie unter [Designdetails: Konten in der Finanzbuchhaltung](design-details-accounts-in-the-general-ledger.md).
3. Überprüfen Sie auf der Seite **Buchungsmatrix Einrichtung** das Feld **Lagerzugangskonto (Interim)** auf die **Geschäftsbuchungsgruppe** und die **Produktbuchungsgruppe**, die Sie verwenden.
4. Wenn Sie eine Bestellung erstellen, ist die Standardeinstellung, dass das Feld **Kred.-Rechnungsnr.** erforderlich ist. Sie müsse dies auf der Seite **Kreditoren & Einkauf Einr.** deaktivieren, indem Sie das Feld **Ext. Belegnr. erforderlich** deaktivieren.

## Beispiel  

> [!NOTE]  
> Die in diesem Beispiel verwendeten Kontonummern dienen nur als Referenz und unterscheiden sich in Ihrem System. Richten Sie sie wie in den Voraussetzungen oben beschrieben ein.

Sie buchen eine Einkaufsbestellung als erhalten. Die erwarteten Kosten sind MW 95,00.  

 **Wertposten**  

|Buchungsdatum|Postentyp|Einstandsbetrag (erwartet)|Auf Sachkonto geb. Soll-Kosten|Soll-Kosten|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|01-01-20|EK-Preis|95.00|95.00|Ja|1|1|  

 **Relationsposten im Sachkonto – Tabelle Artikelpostenrelation**  

|Sachposten Lfd. Nr.|Wertposten Lfd. Nr.|Fibujournalnr.|  
|--------------------|---------------------|-----------------------|  
|1|1|1|  
|2|1|1|  

 **Sachposten**  

|Buchungsdatum|Sachkonto|Kontonr. (En-US-Demo)|Betrag|Lfd. Nr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|Lagerzugangskonto (Interim)|5530|-95.00|2|  
|01-01-20|Lagerkonto (Interim)|2131|95.00|1|  

 Sie können die Einkaufsbestellung sofort oder zu einem späteren Zeitpunkt buchen. Die fakturierten Kosten sind MW 100,00.  

 **Wertposten**  

|Buchungsdatum|Einstandsbetrag (tatsächl.)|Einstandsbetrag (erwartet)|Gebuchte Lagerregulierung an G/L|Soll-Kosten|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|01-15-20|100.00|-95.00|100.00|Nein|1|2|  

 **Relationsposten im Sachkonto – Tabelle Artikelpostenrelation**  

|Sachposten Lfd. Nr.|Wertposten Lfd. Nr.|Fibujournalnr.|  
|--------------------|---------------------|-----------------------|  
|3|2|2|  
|4|2|2|  
|5|2|2|  
|6|2|2|  

 **Sachposten**  

|Buchungsdatum|Sachkonto|Kontonummer (nur Beispiele!)|Betrag|Eingabenr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-15-20|Lagerzugangskonto (Interim)|5530|95.00|4|  
|01-15-20|Lagerkonto (Interim)|2131|-95.00|3|  
|01-15-20|Direkte Kosten Verrech.-Konto|7291|-100|6|  
|01-15-20|Lagerkonto|2130|100|5|  

## Siehe auch
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Kostenregulierung](design-details-cost-adjustment.md)   
 [Designdetails: Abgleich mit der Finanzbuchhaltung](design-details-reconciliation-with-the-general-ledger.md)   
 [Designdetails: Bestandsbuchung](design-details-inventory-posting.md)   
 [Designdetails: Abweichung](design-details-variance.md)  
 [Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
