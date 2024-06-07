---
title: 'Designdetails: – Konten in der Finanzbuchhaltung | Microsoft Docs'
description: 'Um Lagerbestände und Kapazitätsposten mit der Finanzbuchhaltung abzustimmen, werden die zugehörigen Wertposten auf verschiedene Konten in der Finanzbuchhaltung gebucht.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: null
ms.date: 02/20/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="design-details-accounts-in-the-general-ledger"></a>Designdetails: Konten in der Finanzbuchhaltung

Um Lagerbestände und Kapazitätsposten mit der Finanzbuchhaltung abzustimmen, werden die zugehörigen Wertposten auf verschiedene Konten in der Finanzbuchhaltung gebucht. Weitere Informationen finden Sie unter [Designdetails: Abstimmung mit der Finanzbuchhaltung](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger"></a>Vom Bestandsposten

Die folgende Tabelle zeigt die Beziehung zwischen den verschiedenen Arten von Bestandswertposten und die Konten und Gegenkonten im Sachkonto an.  

|**Artikelpostenart**|**Wertpostenart**|**Abweichungsart**|**Soll-Kosten**|**Konto**|**Gegenkonto**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Einkauf|Direkte Kosten||Ja|Lager (Interim)|Lagerzugangskonto (Interim)|  
|Einkauf|Direkte Kosten||Nein|Lagerbest|Direkte Kosten verrechnet|  
|Einkauf|Indirekte Kosten||Nein|Lagerbest|Gemeinkosten verrechnet|  
|Einkauf|Abweichung|Einkauf|Nein|Lagerbest|Einkaufsabweichung|  
|Einkauf|Neubewertung||Nein|Lagerbest|Lagerkorrektur|  
|Einkauf|Runden||Nein|Lagerbest|Lagerkorrektur|  
|Verkauf|Direkte Kosten||Ja|Lager (Interim)|LAGERVERBR (Interim)|  
|Verkauf|Direkte Kosten||Nein|Lagerbest|LAGERVERBR|  
|Verkauf|Neubewertung||Nein|Lagerbest|Lagerkorrektur|  
|Verkauf|Runden||Nein|Lagerbest|Lagerkorrektur|  
|Zugang,Abgang,Lagerplatzumlagerung|Direkte Kosten||Nein|Lagerbest|Lagerkorrektur|  
|Zugang,Abgang,Lagerplatzumlagerung|Neubewertung||Nein|Lagerbest|Lagerkorrektur|  
|Zugang,Abgang,Lagerplatzumlagerung|Runden||Nein|Lagerbest|Lagerkorrektur|  
|(Produktions-) Verbrauch|Direkte Kosten||Nein|Lagerbest|WIP|  
|(Produktions-) Verbrauch|Neubewertung||Nein|Lagerbest|Lagerkorrektur|  
|(Produktions-) Verbrauch|Runden||Nein|Lagerbest|Lagerkorrektur|  
|Verbrauch für Montage|Direkte Kosten||Nein|Lagerbest|Lagerkorrektur|  
|Verbrauch für Montage|Direkte Kosten||Nein|Direkte Kosten verrechnet|Lagerkorrektur|  
|Verbrauch für Montage|Indirekte Kosten||Nein|Gemeinkosten verrechnet|Lagerkorrektur|  
|(Fertig produzierte Artikel; Istmeldungen)|Direkte Kosten||Ja|Lager (Interim)|WIP|  
|(Fertig produzierte Artikel; Istmeldungen)|Direkte Kosten||Nein|Lagerbest|WIP|  
|(Fertig produzierte Artikel; Istmeldungen)|Indirekte Kosten||Nein|Lagerbest|Gemeinkosten verrechnet|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Material|Nein|Lagerbest|Materialabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Kapazität|Nein|Lagerbest|Kapazitätsabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Fremdarbeit|Nein|Lagerbest|Fremdarbeitskostenabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Kapazitätsgemeinkosten|Nein|Lagerbest|Kap.-Gemeinkostenabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Produktionsgemeinkosten|Nein|Lagerbest|Prod.-Gemeinkostenabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Neubewertung||Nein|Lagerbest|Lagerkorrektur|  
|(Fertig produzierte Artikel; Istmeldungen)|Runden||Nein|Lagerbest|Lagerkorrektur|  
|Montageausstoß|Direkte Kosten||Nein|Lagerbest|Lagerkorrektur|  
|Montageausstoß|Neubewertung||Nein|Lagerbest|Lagerkorrektur|  
|Montageausstoß|Indirekte Kosten||Nein|Lagerbest|Gemeinkosten verrechnet|  
|Montageausstoß|Abweichung|Material|Nein|Lagerbest|Materialabweichung|  
|Montageausstoß|Abweichung|Kapazität|Nein|Lagerbest|Kapazitätsabweichung|  
|Montageausstoß|Abweichung|Kapazitätsgemeinkosten|Nein|Lagerbest|Kap.-Gemeinkostenabweichung|  
|Montageausstoß|Abweichung|Produktionsgemeinkosten|Nein|Lagerbest|Prod.-Gemeinkostenabweichung|  
|Montageausstoß|Runden||Nein|Lagerbest|Lagerkorrektur|  

## <a name="from-the-capacity-ledger"></a>Vom Kapazitätsposten

 Die folgende Tabelle zeigt die Beziehung zwischen den verschiedenen Arten von Kapazitätswertposten und die Konten und Gegenkonten im Sachkonto an. Kapazitätsposten stellen die Arbeitszeit dar, die bei Montage- oder Produktionsarbeiten verbraucht wird.  

|**Arbeitstyp**|**Kapazitätsposten Lfd. Nr.**|**Wertpostenart**|**Konto**|**Gegenkonto**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Montage|Ressource|Direkte Kosten|Direkte Kosten verrechnet|Lagerkorrektur|  
|Montage|Ressource|Kosten|Gemeinkosten verrechnet|Lagerkorrektur|  
|Produktion|Arbeitsplatz/Arbeitsplatzgrupe|EK-Preis|Unf.-Arbeit-Konto|Direkte Kosten verrechnet|  
|Produktion|Arbeitsplatz/Arbeitsplatzgrupe|Indirekte Kosten|Unf.-Arbeit-Konto|Gemeinkosten verrechnet|  

## <a name="assembly-costs-are-always-actual"></a>Montagekosten sind immer Ist-Kosten

 Wie in der obigen Tabelle gezeigt, werden Montagebuchungen in Interimskonten nicht repräsentiert. Dies liegt daran, dass der Begriff Umlaufbestand (WIP) in der Montageausstoßbuchung nicht gilt, anders als in der Istmeldungsbuchung. Montagekosten werden nur als Ist-Kosten gebucht, nie als erwartete Kosten.  

 Weitere Informationen finden Sie unter [Designdetails: Montageauftragsbuchung](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger"></a>Berechnung des in die Finanzbuchhaltung zu buchenden Betrags

 Die folgenden Felder in der **Werteintrag**-Tabelle werden verwendet, um den erwarteten-Kostenbetrag zu berechnen, der in die Finanzbuchhaltung gebucht wird:  

- Einstandsbetrag (tatsächl.)  
- Gebuchte Lagerregulierung  
- Einstandsbetrag (erwartet)  
- Auf Sachkonto geb. Soll-Kosten  

Die nachstehende Tabelle zeigt, wie die in die Finanzbuchhaltung zu buchenden Beträge für die beiden verschiedenen Kostenarten berechnet werden.  

|Kostenart|Berechnung|  
|---------------|-----------------|  
|Ist-Kosten|Einstandsbetrag (tatsächl.) – Gebuchte Lagerregulierung|  
|Soll-Kosten|Kostenbetrag (erwartet) – Auf Sachkonto geb. Soll-Kosten|  

## <a name="see-also"></a>Siehe auch

[Designdetails: Lagerbewertung](design-details-inventory-costing.md)  
[Designdetails: Lagerbuchung](design-details-inventory-posting.md)  
[Designdetails: Soll-Kosten-Buchen](design-details-expected-cost-posting.md)  
[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
