---
title: Definieren und Zuweisen von Kosten
description: 'Kostenzuteilungen verschieben Kosten und Einnahmen zwischen Kostenarten, Kostenstellen und Kostenträgern. Sie können so viele Zuteilungen wie notwendig definieren.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1102, 1105, 1106, 1107, 1109, 1114'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="defining-and-allocating-costs"></a><a name="defining-and-allocating-costs"></a>Definieren und Zuweisen von Kosten

Kostenzuteilungen verschieben Kosten und Einnahmen zwischen Kostenarten, Kostenstellen und Kostenträgern. Sie können so viele Zuteilungen wie notwendig definieren. Jede Zuteilung besteht aus:  

- Eine Verteilungsquelle.  
- Mindestens einem Zuteilungsziel.  

Die Zuteilungsquelle gibt an, welche Kosten zugeordnet werden müssen, und die Zuteilungsziele bestimmen, wo die Kosten zugeordnet werden müssen. Beispielsweise können die Kosten für die Kostenart Strom und Heizung eine Verteilungsquelle sein. Sie ordnen alle Strom- und Heizkosten drei Kostenstellen zu: Werkstatt, Produktion und Verkauf. Diese Kostenstellen sind Ihre Zuteilungsziele.  

Für jede Zuteilungsquelle legen Sie eine Zuteilungsebene, eine Gültigkeitsdauer und eine Variante als Gruppen-ID fest. Sie können einen Batchauftrag verwenden, um Filter festzulegen und Zuteilungsdefinitionen auszuwählen und dann automatisch Kostenzuteilungen auszuführen.  

Für jedes Zuteilungsziel definieren Sie eine Zuteilungsgrundlage. Die Zuteilungsgrundlage kann entweder statisch oder dynamisch sein.  

- Die statische Zuteilungsgrundlagen basieren auf einem definierten Wert, zum Beispiel Quadratmeter oder ein eingerichtetes Verteilungsverhältnis, wie 5:2:4.  
- Die dynamische Zuteilung basiert auf veränderbaren Werten, wie z. B. die Anzahl der Mitarbeiter in einer Kostenstelle oder die Verkaufseinnahmen eines Kostenträgers in einem bestimmten Zeitraum.  

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..

## <a name="setting-up-allocation-source-and-targets"></a><a name="setting-up-allocation-source-and-targets"></a>Richten Sie die Zuteilungsquelle und Ziele ein

Jede Zuordnung besteht aus einer Zuordnungsquelle und einer oder mehreren Zuordnungszielen. Die Zuordnungsquelle definiert, welche Kosten zugeordnet werden. Die Zuordnungsziele bestimmen, wie die Kosten zugeordnet werden.  

### <a name="to-set-up-cost-allocations"></a><a name="to-set-up-cost-allocations"></a>So richten Sie Kostenzuordnungen ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kostenzuteilung** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Kostenzuteilung** die Aktion **Bearbeiten** aus.  
3. Geben Sie eine ID für die Zuordnungsquelle in das Feld **ID** ein.  
4. Definieren Sie eine **Ebene** als Zahl zwischen 1 und 99 im Feld . Die Verteilungsbuchung richtet sich nach der Reihenfolge der Stufen.  
5. Geben Sie eine Kostenart ein, um festzulegen, welche Kostenarten im Feld **Kostenartbereich** zugeordnet werden. Wenn alle Kosten für eine Kostenart zugeordnet werden, wird kein Bereich definiert.  
6. Geben Sie eine Kostenstelle zusammen mit den zuzuordnenden Kosten im Feld **Kostenstellencode** ein.  
7. Geben Sie eine Kostenstelle zusammen mit den zuzuordnenden Kosten im Feld **Kostenstellencode** ein. Am häufigsten bleibt das Feld leer, da Kostenobjekte selten anderen Kostenträgern zugeordnet werden.  
8. Geben Sie im Feld **Für Kostenart gutschreiben** eine Kostenart ein. Die Kosten, die zugeteilt werden, werden der ursprünglichen Kostenart gutgeschrieben. Die Kreditbuchung wird auf Kostenart gebucht, die hier angegeben ist.  
9. Definieren Sie im Inforegister **Zeilen** die Verteilungsziele. Geben Sie auf der ersten Zeile unter **Zielkostenart** eine Kostenart ein. So definieren Sie, unter welcher Kostenart die Zuordnung gebucht wird.  
10. Geben Sie in der ersten Zeile das erste Zuordnungsziel in das Feld **Zielkostenstelle** oder **Zielkostenobjekt** ein. Diese beiden Felder definieren, auf welche Kostenstelle oder welchen Kostenträger die Zuordnung gebucht wird. Sie können eines dieses Felder ausfüllen, aber nicht beide.  
11. Wiederholen Sie dieselben Schritte in der zweiten Zeile, um zusätzliche Zuordnungsziele einzurichten.  
12. Nach dem Einrichten der Zuordnungsziele und -quellen wählen Sie auf der Registerkarte Start in der Gruppe Prozess die Aktion **Verteilungsschlüssel berechnen** aus, um die gesamten Aktienwerte zu berechnen.  

> [!NOTE]  
> Aktivieren Sie das Kontrollkästchen **Gesperrt**, um die Verteilungseinrichtung zu deaktivieren.

## <a name="setting-filters-for-dynamic-allocation-bases"></a><a name="setting-filters-for-dynamic-allocation-bases"></a>Setzen von Filtern für dynamische Zuteilungsgrundlagen

Die Methode der dynamischen Zuteilung basiert auf veränderbaren Werten. Zum Beispiel die Anzahl der Mitarbeiter in einer Kostenstelle oder die Artikel eines Kostenträgers, die in einem bestimmten Zeitraum verkauft wurden. Es gibt neun vordefinierte Zuteilungsgrundlagen und zwölf dynamische Datumsbereiche. Die verschiedenen Filter werden basierend auf der Zuteilungsgrundlage eingestellt.  

### <a name="setting-filters"></a><a name="setting-filters"></a>Festlegen von Filtern

Die nachstehende Tabelle zeigt, welche Filter für verschiedene Zuteilungsgrundlagen möglich sind und welche Werte in den Feldern **Filter-Nr.** und **Gruppenfilter** gültig sind. Wählen Sie <kbd>F1</kbd> im Feld **Datenfiltercode**, um detaillierte Beschreibungen zu lesen.  

|**Bemessungsgrundlage**|**Nr. Filter**|**Datumsfiltercode**|**Kostenstellenfilter**|**Kostenträgerfilter**|**Gruppenfilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Sachposten|Sachkonto|Ja|Ja|Ja|N/Z|  
|Finanzbudgetposten|Sachkonto|Ja|Ja|Ja|Finanzbudgetname|  
|Kostenartposten|Einstandspreisberechnung|Ja|Ja|Ja|N/Z|  
|Kostenbudgetposten|Einstandspreisberechnung|Ja|Ja|Ja|Budgetname|  
|Anzahl Mitarbeiter|N/Z|Ja|Ja|Ja|N/Z|  
|Verkaufte Artikel (Menge)|Artikelnr.|Ja|Ja|Ja|Lagerbuchungsgruppe|  
|Erworbene Artikel (Menge)|Artikelnr.|Ja|Ja|Ja|Lagerbuchungsgruppe|  
|Verkaufte Artikel (Betrag)|Artikelnr.|Ja|Ja|Ja|Lagerbuchungsgruppe|  
|Erworbene Artikel (Betrag)|Artikelnummer|Ja|Ja|Ja|Lagerbuchungsgruppe|

## <a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a><a name="scenario-1-defining-static-allocations-based-on-allocation-ratio"></a>Szenario 1: Definieren von statischen Verteilungen basierend auf dem Verteilungsverhältnis

Die statische Verteilungsmethode basiert auf einem definierten Wert, zum Beispiel die verwendeten Quadratmeter oder ein eingerichtetes Verteilungsverhältnis, wie 5:2:4.  

In diesem Thema wird beschrieben, wie drei neue Verteilungsziel-Kostenträger für die Kostenstelle der Verteilungsquelle PROD mithilfe des eingerichteten Verteilungsverhältnisses 5:2:4 definiert wird. Die drei Zielkostenträger sind ZUBEHÖR, FARBE und EINRICHTUNG.  

> [!NOTE]  
> Das Beispiel verwendet die Demodaten in [!INCLUDE[prod_short](includes/prod_short.md)]  

### <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>So definieren die die Kostenstelle der Verteilungsquelle PROD auf dem Inforegister "Allgemein"

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kostenzuteilung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Kostenzuteilung** die Aktion **Neu** aus.  
3. Wählen Sie im Feld **ID** die <kbd>EINGABETASTE</kbd>, oder geben Sie eine ID ein.  
4. Geben Sie in dem Feld **Menge** **1** ein.  
5. In den Feldern **Gültigkeit ab** und **Gültig bis** geben Sie passende Datumsangaben ein.  
6. Geben Sie im Feld **Kostenstellencode** **PROD** ein.  
7. Geben Sie im Feld **Für Kostenart gutschreiben** die Kostenart **9903** ein.  

### <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>So definieren Sie die Verteilungsziel-Kostenträger auf dem Inforegister "Zeilen"

1. Geben Sie in der ersten Rechnungszeile in dem Feld **Zielkostenart** die Zahl **9903** ein.  
2. Wählen Sie in der ersten Rechnungszeile in dem Feld **Zielkosteobjekt** **ACCESSO**.  
3. Wählen Sie in der ersten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.  
4. Wählen Sie in der ersten Zeile im Feld **Basis** die Option **Statisch** aus, um die Methode der statischen Verteilung zu verwenden.  
5. Geben Sie in der ersten Zeile im Feld **Aktie** das Verteilungsverhältnis **5**ein.  
6. Wählen Sie in der zweiten Rechnungszeile in dem Feld **Zielkostenart** **9903**.  
7. Wählen Sie in der zweiten Rechnungszeile in dem Feld **Zielkosteobjekt** **PAINT.**  
8. Wählen Sie in der zweiten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.  
9. Wählen Sie in der zweiten Zeile im Feld **Basis** die Option **Statisch** aus, um die Methode der statischen Verteilung zu verwenden.  
10. Geben Sie in der zweiten Zeile im Feld **Aktie** das Verteilungsverhältnis **2**ein.  
11. Wählen Sie in der dritten Rechnungszeile in dem Feld **Zielkostenart** **9903** ein.  
12. Wählen Sie in der dritten Rechnungszeile in dem Feld **Zielkosteobjekt** **ACCESSO**.  
13. Wählen Sie in der dritten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.  
14. Wählen Sie in der dritten Zeile im Feld **Basis** die Option **Statisch** aus, um die Methode der statischen Verteilung zu verwenden.  
15. Geben Sie in der dritten Zeile im Feld **Aktie** das Verteilungsverhältnis **4**ein.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] berechnet automatisch das Feld unter Verwendung eines **Prozentsatzes**, der von allen drei Zuteilungsverhältnissen abhängt, die im Feld **Aktie** für alle drei Zeilen eingegeben werden.

## <a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a><a name="scenario-2-defining-dynamic-allocations-based-on-items-sold"></a>Szenario 2: Definieren von dynamischen Zuteilungen auf der Basis der verkauften Artikel

Dieses Thema zeigt ein Beispiel für das Definieren von Zuordnungen mithilfe der Methode der dynamischen Verteilung. In dem Beispiel ändern Sie die dynamische Verteilung der Kosten für die VERKAUF-Kostenstelle, sodass der neue Kostenträger COMPUTERAUSSTATTUNG unterstützt wird. COMPUTERAUSSTATTUNG-Pakete haben Artikelnummern im Bereich von 8904-W bis 8924-W. Sie verwenden die Verkaufszahlen des Vorjahres, um den Anteil zu berechnen. Die Verteilung wird auf die helfende Kostenart 9903 gebucht.  

> [!NOTE]  
> Das Beispiel verwendet die Demodaten in [!INCLUDE[prod_short](includes/prod_short.md)]  

### <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>So definieren Sie dynamische Zuteilungen auf der Basis der im Vorjahr verkauften Artikel

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kostenzuteilungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Kostenzuteilung** die Aktion **Neu** aus.  
3. Wählen Sie im Feld **ID** die <kbd>EINGABETASTE</kbd>, oder geben Sie eine ID ein.  
4. Geben Sie in dem Feld **Menge** **1** ein.  
5. In den Feldern **Gültigkeit ab** und **Gültig bis** geben Sie passende Datumsangaben ein.  
6. Geben Sie im Feld **Kostenstellencode** **VERKAUF** ein.  
7. Geben Sie im Feld **Für Kostenart gutschreiben** die Kostenart **9903** ein.  
8. Geben Sie im Feld **Für Kostenart gutschreiben** die Kostenart **9903** ein.  
9. Wählen Sie im Feld **Zielkostenobjekt** die Option **Neu** aus, um einen neuen Kostenträger COMPUTERAUSSTATTUNG zu erstellen, und füllen Sie ggf. Felder aus. Wählen Sie **COMPUTERAUSSTATTUNG** aus. Lassen Sie das Feld **Zielkostenstelle** leer.  
10. Wählen Sie in der dritten Zeile im Feld **Zielart zuweisen** die Option **Alle Kosten** aus, um festzulegen, wie alle anfallenden Kosten zugeordnet werden.  
11. Wählen Sie im Feld **Basis** die Verteilungsgrundlage **Verkaufte Artikel (Betrag)** aus.  
12. Geben Sie im Feld **Nummernfilter** den Wert **8904-W..8924-W** ein.  
13. In dem Feld **Datumsfiltercode** geben Sie **Vorjahr** ein.  
14. Damit der Vorschlag berechnet wird, klicken Sie auf Aktionen **Fremdarbeit berechnen**.  

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] verwendet die Verkaufszahlen der Vorjahre, um einen Anteil von 1596,50 MW mit 100 Prozent für die COMPUTERAUSSTATTUNG-Pakete zu berechnen. Das bedeutet, dass alle Artikel, die letztes Jahr verkauft wurden, dem Kostenträger COMPUTERAUSSTATTUNG zugeordnet werden.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/allocate-costs-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

 [Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md)  
 [Übertragen und Buchen von Kalkulationen](finance-transfer-and-post-cost-entries.md)  
 [Kostenrechnung](finance-manage-cost-accounting.md)  
 [Terminologie in der Kostenrechnung](finance-terminology-in-cost-accounting.md)  
 [Informationen zur Kostenrechnung](finance-about-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
