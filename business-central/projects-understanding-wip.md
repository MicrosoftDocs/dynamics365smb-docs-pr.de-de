---
title: WIP-Methoden zur Berechnung und Aufzeichnung des Projektfortschritts
description: 'Beschreibt die unterschiedlichen Umlaufbestand(WIP)-Methoden, die verwendet werden können, um Finanzdaten für Projekte zu senden und zu überwachen, die im Umlaufbestand sind.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: '1010,'
ms.date: 08/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="understanding-wip-methods-in-project-management"></a>WIP-Methoden im Projektmanagement verstehen

Im Laufe eines Projekts werden Material sowie Ressourcen und andere Aufwendungen verbraucht und müssen auf das Projekt gebucht werden. Umlaufbestand (WIP) ist eine Funktion, mit der Sie den finanziellen Wert von Projekten in der Finanzbuchhaltung schätzen können, solange die Projekte noch nicht abgeschlossen sind. In vielen Fällen werden die Aufwendungen für ein Projekt vor der Fakturierung eines Projekts gebucht. Wenn nur Ausgaben gebucht werden, ist Ihre Bilanz ungenau.

Zum Überwachen des Werts in der Finanzbuchhaltung können Sie die WIP berechnen und den Wert in der Finanzbuchhaltung buchen. Weitere Informationen finden Sie unter [Überwachen des Projektfortschritts und der -leistung](projects-how-monitor-progress-performance.md).

Standardmäßig werden die folgenden Methoden zur Berechnung und Aufzeichnung des Werts unfertiger Erzeugnisse unterstützt. [!INCLUDE[prod_short](includes/prod_short.md)] 

| WIP-Methode | Description | Deklarierte Kosten | Deklarierte Verkäufe |
| --- | ------- |--- | --- |
| Einstandswert |Erkennt Kosten, wenn dem Kunden eine Rechnung ausgestellt wird. Erkennt Umsätze auf Basis der fakturierten Umsätze. |Einstandswert|Vertrag (Rechnungspreis)|
| Vertriebskosten |Erkennt Kosten, wenn dem Kunden eine Rechnung ausgestellt wird. Erkennt Umsätze auf Basis der fakturierten Umsätze.|Vertriebskosten|Vertrag (fakturierter Preis)|
| Verkaufswert |Erkennt Kosten, sobald sie gemeldet werden. Erfasst Umsätze proportional zu den ausgewiesenen Kosten.|Verbrauch (Einstandsbetrag)|Verkaufswert|
| Prozentsatz der Fertigung |Erkennt Kosten, sobald sie gemeldet werden. Erfasst Umsätze proportional zu den ausgewiesenen Kosten.|Verbrauch (Einstandsbetrag)|Prozentsatz der Fertigung|
| Abgeschl. Vertrag |In die WIP-Berechnung fließen weder Umsätze noch Kosten ein. Bei einem abgeschlossenen Vertrag werden Umsatz und Kosten erst dann erfasst, wenn das Projekt abgeschlossen ist. Diese Option ist beispielsweise dann nützlich, wenn bei den Kosten- und Ertragsschätzungen für das Projekt große Unsicherheit besteht.|Nach Abschluss|Nach Abschluss|

Genaue Formeln und Hauptbuchtransaktionen werden durch die Auswahl in den Feldern  [**Anerkannte Kosten**](#recognized-cost)  und  [**Anerkannte Verkäufe**](#recognized-sales)  definiert.

## <a name="create-a-project-wip-method"></a>WIP-Methode für ein Projekt erstellen

Erstellen Sie eine Projekt-WIP-Methode, die den Bedarf Ihrer Organisation wiedergibt und legen Sie sie als Standard fest.  

> [!NOTE]
> Nachdem Sie eine Methode zum Erstellen von WIP-Einträgen verwendet haben, können Sie die Methode nicht mehr ändern oder löschen.  

1. Wählen Sie das ![Glühbirne, die das „Sie wünschen ...“-Feature öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie  **Projekt-WIP-Methoden** ein und wählen Sie dann das zugehörige verknüpfen aus.  
2. Wählen Sie die Aktion  **Neu**, geben Sie die entsprechenden Werte für die Felder  **Anerkannte Kosten**  und  **Anerkannte Umsätze**  ein und füllen Sie dann die anderen Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Schließen Sie die Seite.
4. Um diese Methode als Standard festzulegen, wählen Sie die ![Glühbirne, die die Funktion „Wie möchten Sie weiter vorgehen“ öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie  **Projekt-Setup** ein und wählen Sie dann das zugehörige verknüpfen aus.  
5. Wählen Sie im Feld **WIP-Standardmethode** die Methode aus der Liste aus.

### <a name="recognized-cost"></a>Anerkannte Kosten

| Anerkannte Kosten | Anerkannte Kostenberechnungsformel | Finanzbuchhaltungsposten |
| --- | --- | ---------- |
|Nach Abschluss|0 (Null)|Dt **Konto für anerkannte Kosten** Cr **Konto für WIP-Kosten** </br>Betrag: AnerkannteKosten </br></br>Dt **Konto für WIP-Kosten** Cr **Konto für angewandte Projektkosten** </br>Betrag: MAX[ErkannteKosten; Tatsächlich (Gesamtkosten)]|
|Vertriebskosten|Tatsächlich (Gesamtkosten) – Budget (Gesamtkosten) * Rechnungsbetrag %, wobei:</br></br> In Rechnung gestellt % = In Rechnung gestellt (Gesamtpreis) / In Rechnung zu stellen (Gesamtpreis)</br></br>**Hinweis:** Diese Berechnung erfordert, dass der abrechenbare Betrag (Gesamtpreis) und das Budget (Gesamtkosten) für das gesamte Projekt korrekt eingegeben werden.|Dt **Konto für anerkannte Kosten** Cr **Konto für WIP-Kosten** </br>Betrag: AnerkannteKosten </br></br>Dt **Konto für WIP-Kosten** Cr **Konto für angewandte Projektkosten** </br>Betrag: MAX[ErkannteKosten; Tatsächlich (Gesamtkosten)] </br></br>Dt **Projektkosten-Anpassungskonto** Cr **WIP-Konto für aufgelaufene Kosten** </br>Betrag: AnerkannteKosten – Tatsächliche (Gesamtkosten), wenn AnerkannteKosten > Tatsächliche (Gesamtkosten)|
|Einstandswert|Tatsächlich (Gesamtkosten) – [Fertigstellung % – Rechnungsbetrag %] * Abrechenbarer (Gesamtpreis) * Budget-Kosten-Preis-Verhältnis, wobei: </br></br> BudgetCostPriceRatio = Budget (Gesamtkosten) / Budget (Gesamtpreis)</br>In Rechnung gestellt % = In Rechnung gestellt (Gesamtpreis) / In Rechnung zu stellen (Gesamtpreis)</br>Fertigstellungsgrad = Tatsächlich (Gesamtkosten)/Budget (Gesamtkosten)</br></br>**Hinweis:** Für diese Berechnung müssen die abrechenbaren Beträge (Gesamtpreis), das Budget (Gesamtpreis) und das Budget (Gesamtkosten) für das gesamte Projekt korrekt eingegeben werden.|Dt **Konto für anerkannte Kosten** Cr **Konto für WIP-Kosten** </br>Betrag: AnerkannteKosten</br></br>Dt **Konto für WIP-Kosten** Cr **Konto für angewandte Projektkosten** </br>Betrag: MAX[ErkannteKosten; Tatsächlich (Gesamtkosten)] </br></br>Dt **Projektkosten-Anpassungskonto** Cr **WIP-Konto für aufgelaufene Kosten** </br>Betrag: AnerkannteKosten – Tatsächliche (Gesamtkosten), wenn AnerkannteKosten > Tatsächliche (Gesamtkosten)|
|Vertrag (fakturierte Kosten)|Fakturiert (Einstandsbetrag) |Dt **Konto für anerkannte Kosten** Cr **Konto für WIP-Kosten** </br>Betrag: AnerkannteKosten </br></br> Dt **Konto für WIP-Kosten** Cr **Konto für angewandte Projektkosten** </br>Betrag: MAX[ErkannteKosten; Tatsächlich (Gesamtkosten)] </br></br>Dt **Projektkosten-Anpassungskonto** Cr **WIP-Konto für aufgelaufene Kosten** </br>Betrag: AnerkannteKosten – Tatsächliche (Gesamtkosten), wenn AnerkannteKosten > Tatsächliche (Gesamtkosten)|
|Verbrauch (Einstandsbetrag)|Ist-Einstandsbetrag |Dt **Konto für anerkannte Kosten** Cr **Konto für WIP-Kosten** </br>Betrag: AnerkannteKosten </br></br>Dt **Konto für WIP-Kosten** Cr **Konto für angewandte Projektkosten** </br>Betrag: MAX[ErkannteKosten; Tatsächlich (Gesamtkosten)]|

Wenn der Projektstatus auf „Abgeschlossen“ geändert wird, wird durch die  **WIP berechnen** Aufgabe die WIP-Transaktion rückgängig gemacht und stattdessen gebucht.

Dt **Konto für anerkannte Kosten** Cr **Konto für angewandte Projektkosten**, Betrag: **Tatsächlich (Gesamtkosten)**

> [!NOTE]
> Abhängig von der Auswahl im Feld  **Verwendete WIP-Buchungsmethode**  kann anstelle des  **Kontos für Projektkosten** das  **Konto für angewendete Artikelkosten**, das  **Konto für angewendete Ressourcenkosten**  oder das  **Konto für angewendete Sachkosten** verwendet werden. Weitere Informationen finden Sie unter  [Projektbuchungsgruppen](projects-how-setup-jobs.md#to-set-general-information-for-projects).

### <a name="recognized-sales"></a>Anerkannte Verkäufe

| Deklarierte Verkäufe | Anerkannte Formel zur Umsatzberechnung | Finanzbuchhaltungsposten |
| --- | --- | ---------- |
|Nach Abschluss|0 (Null)|Dt **WIP-Rechnungsverkaufskonto** Cr **Anerkanntes Verkaufskonto** </br>Betrag: AnerkannterUmsatz</br></br>Dt **Konto für angewandte Projektverkäufe** Cr **Konto für fakturierte WIP-Verkäufe** </br>Betrag: Rechnungsbetrag (Gesamtpreis)|
|Vertrag (fakturierter Preis)|Fakturiert (Verkaufsbetrag)|Dt **WIP-Rechnungsverkaufskonto** Cr **Anerkanntes Verkaufskonto** </br>Betrag: AnerkannterUmsatz</br></br>Dt **Konto für angewandte Projektverkäufe** Cr **Konto für fakturierte WIP-Verkäufe** </br>Betrag: Rechnungsbetrag (Gesamtpreis)|
|Verbrauch (Einstandsbetrag)|Ist-Einstandsbetrag|Dt **WIP-Rechnungsverkaufskonto** Cr **Anerkanntes Verkaufskonto** </br>Betrag: AnerkannterUmsatz</br></br>Dt **Konto für angewandte Projektverkäufe** Cr **Konto für fakturierte WIP-Verkäufe** </br>Betrag: Rechnungsbetrag (Gesamtpreis)
|Prozentsatz der Fertigung|MIN[Abrechnungsfähig (Gesamtpreis) * Fertigstellung %; Abrechnungsfähig (Gesamtpreis)], wobei:</br></br>Fertigstellungsgrad = Tatsächlich (Gesamtkosten)/Budget (Gesamtkosten)</br></br>**Hinweis:** Diese Berechnung erfordert, dass der abrechenbare Betrag (Gesamtpreis) und das Budget (Gesamtkosten) für das gesamte Projekt korrekt eingegeben werden.|Dt **Konto für aufgelaufene WIP-Verkäufe** Cr **Konto für anerkannte Verkäufe** </br>Betrag: AnerkannterUmsatz</br></br>Dt **Konto für angewandte Projektverkäufe** Cr **Konto für fakturierte WIP-Verkäufe** </br>Betrag: Rechnungsbetrag (Gesamtpreis)|
|Verbrauch (Verkaufsbetrag)|Ist-Verkaufsbetrag|Dt **WIP-Rechnungsverkaufskonto** Cr **Anerkanntes Verkaufskonto** </br>Betrag: AnerkannterUmsatz </br></br>Dt **Konto für angewandte Projektverkäufe** Cr **Konto für fakturierte WIP-Verkäufe** </br>Betrag: MAX[Anerkannte Verkäufe; In Rechnung gestellt (Gesamtpreis)]</br></br>Dt **Konto für aufgelaufene WIP-Verkäufe** Cr **Konto für Projektverkaufsanpassungen** </br>Betrag: MAX[ErkannteVerkäufe; In Rechnung gestellt (Gesamtpreis)] – In Rechnung gestellt (Gesamtpreis)|
|Verkaufswert| Tatsächlich (Gesamtpreis) * Abrechenbarer (Gesamtpreis)/Budget (Gesamtpreis)</br></br>**Hinweis:** Diese Berechnung erfordert, dass der abrechenbare Betrag (Gesamtpreis) und das Budget (Gesamtpreis) für das gesamte Projekt korrekt eingegeben werden.|Dt **WIP-Rechnungsverkaufskonto** Cr **Anerkanntes Verkaufskonto** </br>Betrag: AnerkannterUmsatz</br></br>Dt **Konto für angewandte Projektverkäufe** Cr **Konto für fakturierte WIP-Verkäufe** </br>Betrag: MAX[Anerkannte Verkäufe; In Rechnung gestellt (Gesamtpreis)]</br></br>Dt **Konto für aufgelaufene WIP-Verkäufe** Cr **Konto für Projektverkaufsanpassungen** </br>Betrag: MAX[ErkannteVerkäufe; In Rechnung gestellt (Gesamtpreis)] – In Rechnung gestellt (Gesamtpreis)|

Wenn der Projektstatus auf „Abgeschlossen“ geändert wird, wird die WIP-Transaktion durch die  **WIP berechnen** Aufgabe rückgängig gemacht und stattdessen gebucht.

Dt **Konto für angewandte Projektverkäufe** Cr **Konto für anerkannte Verkäufe**, Betrag: **Rechnungsbetrag (Gesamtpreis)**

## <a name="see-also"></a>Siehe auch

[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
