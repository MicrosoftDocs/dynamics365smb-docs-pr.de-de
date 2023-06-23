---
title: Designdetails - Bestandbuchung | Microsoft Docs
description: 'Jede Bestandstransaktion, wie etwa eine Einkaufslieferung oder eine Verkaufslieferung, bucht zwei Posten unterschiedlichen Typs.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-inventory-posting" />Designdetails: Bestandsbuchung

Jede Bestandstransaktion, wie etwa eine Einkaufslieferung oder eine Verkaufslieferung, bucht zwei Posten unterschiedlichen Typs.  

|Postenart|Description|  
|----------|-----------|  
|Menge|Spiegelt die Menge im Bestand wider. Diese Informationen werden in Artikelposten gespeichert.<br /><br /> Begleitet von den Artikelausgleichsposten.|  
|Wert|Spiegelt die Änderung des Lagerwerts wider. Diese Informationen werden in Wertposten gespeichert.<br /><br /> Pro Artikelposten und pro Kapazitätsposten kann es einen oder mehrere Wertposten geben.<br /><br /> Informationen zu Kapazitätswertposten, die sich auf die Verwendung der Produktions- oder Montageressourcen beziehen, finden Sie unter [Designdetails: Produktionsauftragsbuchung](design-details-production-order-posting.md) .|  

 In Verbindung mit Mengenbuchungen gibt es Artikelausgleichsposten, um die Bestandserhöhung mit der Bestandsminderung zu verknüpfen. Dies ermöglicht dem Kalkulationsmodul, Kosten für Lagerzu- an die entsprechenden Abgänge weiterzuleiten und umgekehrt. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgung](design-details-item-application.md).  

 Artikelposten, Wertposten und Artikelausgleichsposten werden durch eine Artikel Buch.-Blattzeile erstellt, entweder indirekt durch Buchen einer Auftragszeile oder direkt auf der Seite Fenster Artikel Buch.-Blatt.  

 In regelmäßigen dynamischen Abständen werden Wertposten, die im Bestandsposten erstellt werden, ins Hauptbuch gebucht, um die beiden Bücher aus Finanzkontrollgründen abzugleichen. Weitere Informationen finden Sie unter [Designdetails: Abstimmung mit der Finanzbuchhaltung](design-details-reconciliation-with-the-general-ledger.md).  

 ![Eintrags-Flow beim Abstimmen des Bestands mit dem Hauptbuch.](media/design_details_inventory_costing_1_entry_flow.png "Eintragsfluss beim Abgleich des Lagerbestands mit dem Sachkonto")  

## <a name="example" />Beispiel

Im folgenden Beispiel wird veranschaulicht, wie Artikelposten, Wertposten und Artikelausgleichsposten zu Sachposten führen.  

 Sie buchen eine Einkaufsbestellung als erhalten und fakturiert für 10 Artikel mit einem EK-Preis von MW 7 und einem Gemeinkostensatz von MW 1. Das Buchungsdatum ist 01-01-20. Die folgenden Einträge werden folgendermaßen erzeugt:  

### <a name="item-ledger-entries-1" />Artikelposten (1)

|Buchungsdatum|Postenart |Einstandsbetrag (tatsächl.)|Menge|Eingabenr.|  
|------------|----------|--------------------|--------|---------|  
|01-01-20|Einkauf|80.00|10|1|  

### <a name="value-entries-1" />Wertposten (1)

|Buchungsdatum|Postenart |Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|------------|----------|--------------------|---------------------|---------|  
|01-01-20|EK-Preis|70.00|1|1|  
|01-01-20|Indirekte Kosten|10,00|1|2|  

### <a name="item-application-entries-1" />Artikelausgleichsposten (1)

|Eingabenr.|Artikelposten Lfd. Nr.|Eingeh. Artikelposten Lfd. Nr.|Ausgeh. Artikelposten Lfd. Nr.|Menge|  
|---------|---------------------|----------------------|-----------------------|--------|  
|1|1|1|0|10|  

 Als nächsten Schritt buchen Sie einen Verkauf mit 10 Stück des Artikels mit einem Buchungsdatum aus 01-15-20.  

### <a name="item-ledger-entries-2" />Artikelposten (2)

|Buchungsdatum|Postenart |Einstandsbetrag (tatsächl.)|Menge|Eingabenr.|  
|------------|----------|--------------------|--------|---------|  
|01-15-20|Verkauf|-80.00|-10|2|  

### <a name="value-entries-2" />Wertposten (2)

|Buchungsdatum|Postenart |Einstandsbetrag (tatsächl.)|Artikelposten Lfd. Nr.|Eingabenr.|  
|------------|----------|--------------------|---------------------|---------|  
|01-15-20|Direkte Kosten|-80.00|2|3|  

### <a name="item-application-entries-2" />Artikelausgleichsposten (2)

|Eingabenr.|Artikelposten Lfd. Nr.|Eingeh. Artikelposten Lfd. Nr.|Ausgeh. Artikelposten Lfd. Nr.|Menge|  
|---------|---------------------|----------------------|-----------------------|--------|  
|2|2|1|2|-10|  

Am Ende der Buchhaltungsperiode führen Sie die Stapelverarbeitung **Bestandkosten in Sachbuch buchen** aus, um diese Lagertransaktionen mit der Finanzbuchhaltung abzustimmen.  

 Weitere Informationen finden Sie unter [Designdetails: Konten in der Finanzbuchhaltung](design-details-accounts-in-the-general-ledger.md).  

 Die folgenden Tabellen zeigen das Ergebnis der Abstimmung der Lagertransaktionen in diesem Beispiel mit der Finanzbuchhaltung.  

### <a name="value-entries-3" />Wertposten (3)

|Buchungsdatum|Postenart |Einstandsbetrag (tatsächl.)|Gebuchte Lagerregulierung an G/L|Artikelposten Lfd. Nr.|Lfd. Nr.|  
|------------|----------|--------------------|------------------|---------------------|---------|  
|01-01-20|EK-Preis|70.00|70.00|1|1|  
|01-01-20|Kosten|10,00|10,00|1|2|  
|01-15-20|Direkte Kosten|-80.00|-80.00|2|3|  

### <a name="general-ledger-entries-3" />Sachposten (3)

|Buchungsdatum|Sachkonto|Kontonr. (En-US-Demo)|Betrag|Eingabenr.|  
|------------|-----------|------------------------|------|---------|  
|01-01-20|[Lagerkonto]|2130|70.00|1|  
|01-01-20|[Direkte Kosten Verrech.-Konto]|7291|-70.00|2|  
|01-01-20|[Lagerkonto]|2130|10,00|3|  
|01.01.07|[Gemeinkostenverrechnungskonto]|7292|-10.00|4|  
|01-15-20|[Lagerkonto]|2130|-80.00|5|  
|01-15-20|[COGS-Konto]|7290|80.00|6|  

> [!NOTE]  
> Das Buchungsdatum der Sachposten ist das gleiche wie für die zugehörigen Wertposten.  
> 
> Das Feld Im **Sachbuch gebuchte Kosten** in der Tabelle **Wertposten** wird ausgefüllt.  

 Die Beziehung zwischen Wertposten und Sachkontoposten wird in der Tabelle **Sachposten-Artikelbeziehung** gespeichert.  

### <a name="relation-entries-in-the-gl--item-ledger-relation-table-3" />Relationsposten im Sachkonto – Tabelle Artikelpostenrelation (3)

|Sachposten Lfd. Nr.|Wertposten Lfd. Nr.|Fibujournalnr.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  
|5|3|1|  
|6|3|1|  

## <a name="assembly-and-production-posting" />Montage- und Produktions-Buchung

Kapazitäts- und Ressourcenposten repräsentieren die Zeit, die als bei Produktion oder Montage verbraucht gebucht wird. Diese Prozesskosten werden als Wertposten in der Finanzbuchhaltung zusammen mit den entsprechenden Materialkosten in einer ähnlichen Struktur gebucht, wie für Artikelposten in diesem Thema beschrieben.  

Weitere Informationen finden Sie unter [Designdetails: Montageauftragsbuchung](design-details-assembly-order-posting.md).  

## <a name="see-also" />Siehe auch

 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  
 [Designdetails: Konten in der Finanzbuchhaltung](design-details-accounts-in-the-general-ledger.md)  
 [Designdetails: Kostenkomponenten](design-details-cost-components.md) [Verwalten der Lagerkosten](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
