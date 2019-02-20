---
title: 'Exemplarische Vorgehensweise: Verfolgung von Serien-/Chargennummern | Microsoft Docs'
description: "Wenn Produktfehler auftreten, müssen die Fehler identifiziert werden, und es muss verhindert werden, dass die betroffenen Artikel das Unternehmen verlassen. Falls bereits defekte Artikel geliefert wurden, müssen Sie verfolgen, wer diese Artikel erhalten hat, und ggf. muss ein Rückruf eingeleitet werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/31/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a94c4f2f8d622a91b74ba0de6f0f18e7eb84a5ef
ms.openlocfilehash: a37561ebf8b9572f69e0ce3c3b83613b98a1098f
ms.contentlocale: de-de
ms.lasthandoff: 01/31/2019

---
# <a name="walkthrough-tracing-serial-lot-numbers"></a>Exemplarische Vorgehensweise: Verfolgung von Serien-/Chargennummern

**Hinweis**: In dieser exemplarischen Vorgehensweise muss in einem Demomandanten mit der Option **Volle Auswertung - vollständige Beispieldaten** ausgeführt werden, die in der Sandboxumgebung verfügbar ist. Weitere Informationen finden Sie unter [Erstellen einer Sandbox-Umgebung](across-how-create-sandbox-environment.md).

Wenn Produktfehler auftreten, müssen die Fehler identifiziert werden, und es muss verhindert werden, dass die betroffenen Artikel das Unternehmen verlassen. Falls bereits defekte Artikel geliefert wurden, müssen Sie verfolgen, wer diese Artikel erhalten hat, und ggf. muss ein Rückruf eingeleitet werden.  

Als erste Aufgabe bei der Defektverwaltung ermitteln Sie, woher die defekten Artikel stammen und wo Sie verwendet wurden. Diese Untersuchung basiert auf historischen Daten und wird durch Durchsuchen von Artikelverfolgungsposten auf der Seite **Artikelablaufverfolgung** vorgenommen.  

Als zweite Aufgabe bei der Defektverwaltung stellen Sie fest, ob die verfolgten Artikel in offenen Belegen eingeplant sind, z. B. in nicht gebuchten Verkaufsaufträgen oder Verbrauchsprotokollen. Dieser Vorgang wird auf der Seite **Navigation** ausgeführt. Sie können die Funktion "Navigieren" verwenden, um alle Arten Datenbankdatensätze zu suchen.  

## <a name="about-this-walkthrough"></a>Informationen zu dieser exemplarischen Vorgehensweise  
In dieser exemplarischen Vorgehensweise wird gezeigt, wie Sie feststellen, welche Artikel defekt sind, von welchem Kreditor sie stammen und wo sie verwendet werden, sodass diese Aufträge gestoppt oder storniert werden können.  

In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

-   Verfolgung vom Verbrauch zum Ursprung.  
-   Verfolgung vom Ursprung zum Verbrauch.  
-   Durchsuchen aller aktuellen Datensätze, die die verfolgte Serien-/Chargennummer enthalten  

## <a name="roles"></a>Rollen  
Die Aufgaben in dieser Demonstration werden von den folgenden Benutzerrollen ausgeführt:  

-   Qualitätskontrolleur  
-   Lagerortleiter  
-   Auftragsverarbeitung  
-   Einkäufer  

## <a name="prerequisites"></a>Voraussetzungen  
Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

-   Das [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmen .  
-   Erstellen Sie später in dies Demonstration anhand der Schritte im Abschnitt "Vorbereiten der Beispieldaten" neue Artikel und verschiedene Geschäftstransaktionen.  

## <a name="story"></a>Hintergrund  
Andreas, der Qualitätskontrolleur, bearbeitet eine Verkaufsreklamation für Artikel 1002, Rennrad. Der Debitor, Blütenhaus GmbH, hat sich über gerissene Schweißnähte im Rennradrahmen beschwert. Die Ingenieure der Qualitätskontrolle haben bestätigt, dass der Rahmen des zurückgesendeten Rennrads defekt ist. Der Qualitätskontrolleur muss nun Folgendes feststellen:  

-   Welche Rahmencharge war fehlerhaft?  
-   In welche Bestellung ist die fehlerhafte Charge eingegangen?  

Von der Verkaufsabteilung weiß der Qualitätskontrolleur, dass das reklamierte Rennrad, Artikel 1002, die Seriennummer SN1 besitzt. Wenn er diese grundlegenden Informationen verwendet, muss er festlegen, wo das fertige Rennrad zuletzt verwendet wurde, und dann muss er es bis zum Ursprung zurückverfolgen, um festzustellen, aus welcher Chargennummer die fehlerhafte Komponente, der Rahmen, stammte.  

Diese erste Aufgabe der Artikelverfolgung ergibt, welche Rennradrahmen defekt waren und von welchem Kreditor sie stammen. Danach muss der Qualitätskontrolleur im Rahmen desselben Verfolgungsprozesses alle verkauften Rennräder ermitteln, die Rennradrahmen aus der fehlerhaften Charge enthalten, sodass diese Aufträge gestoppt oder zurückgerufen werden können. Zum Schluss muss er alle offenen Belege finden, in denen die fehlerhafte Charge verwendet wurde, um zusätzliche Transaktionen zu verhindern.  

Für die ersten beiden Aufgaben der Defektverwaltung wird die Seite **Artikelablaufverfolgung** verwendet. Die letzte Aufgabe wird auf der Seite **Navigate** durchgeführt, wobei die Ergebnisse aus der Seite **Artikelablaufverfolgung** integriert werden.  

## <a name="prepare-sample-data"></a>Vorbereiten der Beispieldaten  
Sie müssen die folgenden neuen Artikel erstellen:  

-   2000, Rennradrahmen: chargenspezifische Verfolgung, Komponente von 1002  
-   1002, Rennrad: seriennummernspezifische Verfolgung  

Anschließend müssen Sie erstellen mit den beiden Artikeln verschiedene Einkaufs-, Produktions- und Verkaufstransaktionen.  

### <a name="to-create-the-items"></a>Serviceartikel anlegen  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Katalogartikel** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Geben Sie im Feld **Nr.** Geben Sie im Feld **2000** ein und füllen Sie dann die folgenden Felder aus.  

    |Beschreibung|Basiseinheiten|Produktbuchungsgruppe|MwSt.-Produktbuchungsgruppe|Lagerbuchungsgruppe|Artikelverfolgungscode|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|------------------------|  
    |Rennradrahmen|STÜCK|ROHMAT|MWST25|ROHMAT|CHARGEALLE|  

    > [!NOTE]  
    >  Um die Basismaßeinheit einzugeben, wählen Sie die Schaltfläche **Neu**, und wählen Sie dann **PSC** auf der Seite **Artikeleinheiten** aus.  

4.  Alle anderen Felder enthalten geeignete Standarddaten oder müssen nicht ausgefüllt werden.  
5.  Klicken Sie auf **OK**, um die erste neue Artikelkarte, 2000, zu erstellen.  
6.  Wählen Sie **Neu** aus.  
7.  Geben Sie im Feld **Nr.** Geben Sie im Feld **1002** ein und füllen Sie dann die folgenden Felder aus.  

    |Beschreibung|Basiseinheiten|Produktbuchungsgruppe|MwSt.-Produktbuchungsgruppe|Lagerbuchungsgruppe|Beschaffungsmethode|Artikelverfolgungscode|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Rennrad|STÜCK|HANDEL|MWST25|FERTIG|Fertigungsauftrag|SNALLE|  

    > [!NOTE]  
    >  Um die Basismaßeinheit einzugeben, wählen Sie die Schaltfläche **Neu**, und wählen Sie dann **PSC** auf der Seite **Artikeleinheiten** aus.  

    Als Nächstes müssen Sie die Produktionseinrichtung des Artikels definieren.

9. Geben Sie auf der Registerkarte B **eschaffung** **1000** in das Feld **Arbeitsplannr.** ein.  
10. Wählen Sie das Feld **Produktion Stückliste** und dann **Erweitert** aus.  
11. Auf der Seite **Fert.-Stücklistenübersicht** wählen Sie die erste Zeile, **1000** aus, und wählen Sie die **Bearbeiten** Aktion aus.  
12. Ändern Sie auf der Seite **Fertigungsstückliste** den Wert im Feld **Status** in **In Entwicklung**.  
13. Geben Sie in einer leeren Zeile **2000** im Feld **Nr.** ein und geben dann **1** im Feld **Komponentenmenge** ein.  
14. Ändern Sie den Wert im Feld **Status** wieder in **Zertifiziert**.  
15. Wählen Sie die Schaltfläche **OK**, um die Fertigungsstückliste auf der Artikelkarte einzufügen, und schließen Sie die Seite **Produktionsstückliste**.  

    Kaufen Sie als Nächstes Rennradrahmen vom Lieferanten Custom Metals Incorporated.  

### <a name="to-purchase-components"></a>Um Komponenten zu kaufen  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufaufträge** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Erstellen Sie eine Bestellung für den Kreditor Custom Metals Incorporated, indem Sie die folgenden Felder ausfüllen.  

    |Artikel|Menge|Chargennr.|  
    |----------|--------------|-------------|  
    |2000|10|CHARGE1|  

4.  Um die Chargennummer einzugeben, wählen Sie die **Artikelverfolgungszeilen** Aktion aus.  
5.  Klicken Sie auf der Seite **Artikelverfolgungszeilen** auf den Dropdownpfeil im Feld **Chargennr.**, wählen Sie **Menge (Basis)** aus und schließen Sie die Seite.  
6.  Füllen Sie das Feld **Kred.-Rechnungsnr.** aus.  
7.  Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Lieferung und Rechnung**, und wählen Sie dann die Schaltfläche **OK** aus.  

    Kaufen Sie als Nächstes Rennradrahmen von Coolwood Technologies.  
8.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufaufträge** ein, und wählen dann den zugehörigen Link aus.  
9. Wählen Sie die Aktion **Neu** aus.
10. Erstellen Sie eine Bestellung für den Kreditor Coolwood Technologies, indem Sie die folgenden Felder ausfüllen.  

    |Artikel|Menge|Chargennr.|  
    |----------|--------------|-------------|  
    |2000|11|CHARGE2|  

11. Um die Chargennummer einzugeben, wählen Sie im Inforegister **Zeilen**, in der Gruppe **Zeile**, die Aktion **Artikelverfolgungszeilen**.  
12. Klicken Sie auf der Seite **Artikelverfolgungszeilen** auf den Dropdownpfeil im Feld **Chargennr.**, wählen Sie **Menge (Basis)** aus und schließen Sie die Seite.  
13. Füllen Sie das Feld **Kred.-Rechnungsnr.** aus.  
14. Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Lieferung und Rechnung**, und wählen Sie dann die Schaltfläche **OK** aus.  

    Als Nächstes produzieren Sie zwei Rennräder, SN1 und SN2.  

### <a name="to-produce-end-items"></a>Um Endartikel zu produzieren  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Freigegebene FA** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Gruppe **Neu** aus.  
3.  Erstellen Sie einen neuen freigegebenen Fertigungsauftrag, indem Sie die folgenden Felder ausfüllen.  

    |-|-|-|  
    |Quellnummer|Menge|Seriennummer|  
    |1002|2|SN1|  
    |1002|2|SN2|  

4.  Wählen Sie die **FA berechnen** Aktion aus, und wählen Sie dann die Schaltfläche **OK** aus, um die Zeile zu befüllen.  
5.  Um die Seriennummern einzugeben, wählen Sie die **Artikelverfolgungszeilen** Aktion aus.  
6.  Klicken Sie auf der Seite **Artikelverfolgungszeilen** auf den Dropdownpfeil im Feld **Seriennr.**, wählen Sie **Menge (Basis)** aus und schließen Sie die Seite.  

    Als Nächstes müssen Sie den Verbrauch von Rennradrahmen aus CHARGE1 buchen.  
7.  Auf der Seite **Freigegebener FA** wählen Sie die **Produktions Buch.-Blatt** Aktion aus.  
8.  Auf der Seite **Produktions Buch.-Blatt** wählen Sie die Verbrauchszeile für Artikel 2000 aus, wählen Sie die Aktion **Artikelverfolgungszeilen** aus.
9. Klicken Sie auf der Seite **Artikelverfolgungszeilen** auf den Dropdownpfeil im Feld **Chargennr.**, wählen Sie **CHARGE1** aus, und klicken Sie dann auf **OK**.  
10. Lassen Sie alle anderen Standardeinstellungen auf der Seite **Produktions Buch.-Blatt** unverändert, und wählen Sie die **Buchen** Aktion aus.  

    Als Nächstes produzieren Sie zwei weitere Rennräder, SN3 und SN4.  

11. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Freigegebene FA** ein, und wählen dann den zugehörigen Link aus.  
12. Wählen Sie die Aktion **Neu** aus.  
13. Erstellen Sie einen neuen freigegebenen Fertigungsauftrag, indem Sie die folgenden Felder in der Kopfzeile ausfüllen.  

    |Herkunftsnr.|Menge|Seriennummer|  
    |----------------|--------------|----------------|  
    |1002|2|SN3|  
    |1002|2|SN4|  

14. Wählen Sie die **FA berechnen** Aktion aus, um die Zeile zu befüllen.  
15. Um die Seriennummern einzugeben, wählen Sie die Aktion **Artikelverfolgungszeilen** und dann die Nummern auf zwei Zeilen im Feld **Seriennummer** auf der Seite **Artikelnachverfolgungszeilen** aus.  

    Als Nächstes müssen Sie vermehrten Verbrauch von Rennradrahmen aus CHARGE1 buchen.  
16. Auf der Seite **Freigegebener FA** wählen Sie die **Produktions Buch.-Blatt** Aktion aus.  
17. Auf der Seite **Produktions Buch.-Blatt** wählen Sie die Verbrauchszeile für Artikel 2000 aus, wählen Sie die Aktion **Artikelverfolgungszeilen** aus.
18. Klicken Sie auf der Seite **Artikelverfolgungszeilen** auf den Dropdownpfeil im Feld **Chargennr.**, wählen Sie **CHARGE1** aus, und klicken Sie dann auf **OK**.  
19. Lassen Sie alle anderen Standardeinstellungen auf der Seite **Produktions Buch.-Blatt** unverändert, und wählen Sie die **Buchen** Aktion aus.  

    Sie haben jetzt vier Rennräder, SN1 bis SN4 produziert, und vier der zehn Rennradrahmen aus CHARGE1 verbraucht, zwei Rahmen in jedem Fertigungsauftrag.  

20. Schließen Sie das Produktionsbuchhaltungsblatt und die Fertigungsaufträge.  

    Als Nächstes verkaufen Sie Rennräder. Verkaufen Sie zuerst das Rennrad mit SN1 an Selangorian Ltd.  

### <a name="to-sell-the-end-items"></a>Um die Endartikel zu verkaufen  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus, und dann erstellen Sie einen Verkaufsauftrag, indem Sie die folgenden Felder ausfüllen.  

    |Debitor|Artikel|Menge|Seriennummer|  
    |--------------|----------|----------|----------------|  
    |Blütenhaus GmbH|1002|1|SN1|  

3.  Um die Seriennummer einzugeben, wählen Sie die Aktion **Artikelverfolgungszeilen** und dann die Nummer im Feld **Seriennummer** auf der Seite **Artikelnachverfolgungszeilen** aus.  
4.  Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Liefern und fakturieren**, und wählen Sie dann die Schaltfläche **OK** aus.  

    Als Nächstes verkaufen Sie das Rennrad mit SN2 an The Cannon Group PLC.  

5.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
6.  Wählen Sie die Aktion **Neu** aus, und dann erstellen Sie einen Verkaufsauftrag, indem Sie die folgenden Felder ausfüllen.  

    |Debitor|Artikel|Menge|Seriennummer|  
    |--------------|----------|----------|----------------|  
    |Möbel-Meller KG|1002|1|SN2|  

7.  Um die Seriennummer einzugeben, wählen Sie die Aktion **Artikelverfolgungszeilen** und dann die Nummer im Feld **Seriennummer** auf der Seite **Artikelnachverfolgungszeilen** aus.  
8.  Wählen Sie die Aktion **Buchen** aus, wählen Sie die Option **Liefern und fakturieren**, und wählen Sie dann die Schaltfläche **OK** aus.  

    Zum Schluss verkaufen Sie einige Rennradrahmen separat. Cannon Group PLC. bestellt zudem vier separate Rennradrahmen für ihre eigene Fertigungslinie.  

9. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
10. Wählen Sie die Aktion **Neu** aus, und dann erstellen Sie einen Verkaufsauftrag, indem Sie die folgenden Felder ausfüllen.  

    |Debitor|Artikel|Menge|Seriennr.|  
    |--------------|----------|----------|----------------|  
    |Möbel-Meller KG|2000|5|CHARGE1|  

11. Um die Seriennummer einzugeben, wählen Sie im Inforegister **Zeilen** in der Gruppe **Zeile** die Aktion **Artikelverfolgungszeilen** und dann die Nummern auf zwei Zeilen im Feld **Seriennummer** auf der Seite **Artikelnachverfolgungszeilen** aus.  

    > [!NOTE]  
    >  Buchen Sie den letzten Verkaufsauftrag für fünf Rennradrahmen nicht.  

    Damit ist die Vorbereitung der Daten für die exemplarische Vorgehensweise für die Funktionen "Artikelablaufverfolgung" und "Navigate" abgeschlossen.  

## <a name="tracing-from-usage-to-origin"></a>Verfolgung vom Verbrauch zum Ursprung  
 Von der Verkaufsabteilung weiß der Qualitätskontrolleur, dass das reklamierte Rennrad, Artikel 1002, die Seriennummer SN1 besitzt. Anhand dieser Basisinformation kann er feststellen, wo das fertige Rennrad zuletzt verwendet wurde, in diesem Fall in der Verkaufslieferung an die Blütenhaus GmbH. Anschließend muss der Qualitätskontrolleur das Rennrad zum frühesten Ursprung zurückverfolgen, um festzustellen, aus welcher Charge und von welchem Kreditor der fehlerhafte Rennradrahmen stammt.  

### <a name="to-determine-which-lot-included-the-faulty-frame-and-who-supplied-it"></a>So stellen Sie fest, aus welcher Charge und von welchem Lieferanten der fehlerhafte Rahmen stammt  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Artikelnachverfolgung** ein, und wählen dann den zugehörigen Link aus.  
2.  Geben Sie auf der Seite **Artikelablaufverfolgung** **SN1** in das Feld **Seriennr** ein, und geben Sie dann **1002** in das Feld **Artikelfilter** ein.  
3.  Übernehmen Sie die Standardeinstellung **Nur mit Artikelverfolgung** im Feld K **omponenten anzeigen** und die Standardverfolgungsmethode **Verbrauch - Ursprung** im Feld **Nachverfolgungsmethode**  
4.  Wählen Sie die Aktion **Ablaufverfolgung** aus.  

    Beachten Sie, dass ein Verkaufslieferkopf den Suchkriterien entspricht. Vergewissern Sie sich, dass es sich um die Lieferung handelt, in der das fehlerhafte Rennrad an die Blütenhaus GmbH geliefert wurde, bevor Sie mit der Verfolgung fortfahren.  

5.  Wählen Sie die Artikelverfolgungszeile aus, und wählen Sie dann die Aktion **Beleg anzeigen** aus.  

    Fahren Sie nun mit der Verfolgung des Ursprungs der Verkaufslieferung des Rennrads mit der Nummer SN1 fort.  
6.  Wählen Sie das Pluszeichen in den Verfolgungszeilen, um die Transaktionskette schrittweise zu erweitern und zum Ursprung der Verkaufslieferung zurückzuverfolgen.  

    Sie können die folgenden Buchungshistorie verfolgen:  

    -   Der nächste gebuchte Beleg in der Kette in Rückwärtsrichtung ist die Ausgangsbuchung von SN1 aus dem ersten freigegeben Fertigungsauftrag.  
    -   Der nächste gebuchte Beleg (in Rückwärtsrichtung) ist die Verbrauchsbuchung aus dem ersten freigegebenen Fertigungsauftrag. Hier sieht der Qualitätskontrolleur, dass ein Rennradrahmen aus CHARGE1 verwendet wurde.  
    -   Der letzte gebuchte Beleg in dieser Kette ist die gebuchte Einkaufslieferung, in der Rennradrahmen mit CHARGE1 in den Bestand eingegangen sind.  

    Der Qualitätskontrolleur hat nun festgestellt, welche Rennradrahmencharge fehlerhaft war, und kann nach der letzten Verfolgungszeile suchen, um den Lieferanten zu ermitteln (Custom Metals Incorporated).  

    > [!NOTE]  
    >  Nehmen Sie keine weiteren Änderungen am Ergebnis der Verfolgung vor, es wird im nächsten Abschnitt noch verwendet.  

     Damit ist die erste Aufgabe der Defektverwaltung auf der Seite **Artikelablaufverfolgung** abgeschlossen. Der Qualitätskontrolleur muss nun feststellen, ob in anderen gebuchten Belegen Rennradrahmen aus CHARGE1 verwendet wurden.  

## <a name="tracing-from-origin-to-usage"></a>Verfolgung vom Verbrauch zum Ursprung  
 Der Qualitätskontrolleur hat festgestellt, dass die fehlerhaften Rennradrahmen aus CHARGE1 stammen. Er muss jetzt alle anderen Rennräder ermitteln, die Rahmen aus der fehlerhaften Charge enthalten, damit Aufträge für diese Räder gestoppt oder zurückgerufen werden können.  

 Zum Vorbereiten dieser Aufgabe können Sie auf der Seite **Artikelnachverfolgung** Feld **Lot-Nr.Filter** manuell CHARGE1 und im Feld **Artikelfilter** 2000 eingeben. In dieser exemplarischen Vorgehensweise wird jedoch die Funktion **Trace Opposite - from Line** verwendet.  

### <a name="to-find-all-usage-of-the-faulty-lot"></a>So machen Sie alle Verbrauchsfälle der fehlerhaften Charge ausfindig  

1.  Wählen Sie auf der Seite **Artikelablaufverfolgung** die Zeile der Einkaufslieferung aus (die letzte Verfolgungszeile), und wählen Sie dann **Trace Opposite - from Line** aus.  

    Das Ergebnis der Verfolgung basiert nun auf den Filtern der Verfolgungszeile für die Einkaufslieferung, CHARGE1 und Artikel 2000, und der Verfolgungsmethode **Ursprung - Verbrauch**.  

    Erweitern Sie alle Verfolgungszeilen, um eine Übersicht aller Verbrauchsfälle von Artikel 2000 mit CHARGE1 zu erhalten.  

2.  Wählen Sie die Aktion **Alle aufklappen** aus.  

    Die ersten vier Verfolgungszeilen beziehen sich auf die bereits aufgelöste Verkaufslieferung an die Blütenhaus GmbH. Die letzte Zeile besagt, dass ein weiteres Rennrad, SN2, in demselben freigegebenen Fertigungsauftrag produziert und dann in einer anderen Verkaufslieferung verkauft und geliefert wurde.  

    Der Qualitätskontrolleur informiert umgehend die Verkaufsabteilung, sodass ein Rückruf des defekten Rennrads vom Debitoren Möbel-Meller KG eingeleitet werden kann.  

    Gleichzeitig kann er den letzten drei Verfolgungszeilen entnehmen, dass zwei weitere Artikel, SN3 und SN4, mit Rennradrahmen aus CHARGE1 produziert wurden. Er unternimmt die entsprechenden Schritte, um diese Endartikel im Lagerbestand zu sperren.  

    Damit ist die zweite Aufgabe der Defektverwaltung auf der Seite für **Artikelnachverfolgung** abgeschlossen. Da die Seite **Artikelnachverfolgung** nur auf gebuchten Posten basiert, muss der Qualitätskontrolleur zum Fenster **Navigieren** wechseln, um zu überprüfen, ob CHARGE1 in nicht nicht-gebuchten Belegen verwendet wird.  

## <a name="finding-all-records-of-a-seriallot-number"></a>Alle Datensätze einer Serien-/Chargennummer finden  
 Aus der Seite **Artikelnachverfolgung** erfuhr der Qualitätskontrolleur, dass CHARGE1 die fehlerhaften Rennradrahmen enthielt, von welchem Kreditor sie stammen, und in welcher gebuchten Transaktion sie verwendet wurden. Er muss nun feststellen, ob CHARGE1 in offenen Belegen enthalten ist, indem er die Ergebnisse Nachverfolgung auf die Seite **Navigieren** integriert, wo er eine Suche in allen Datenbankdatensätzen ausführen kann.  

### <a name="to-find-all-occurrences-of-lot1-in-non-posted-records-such-as-open-orders"></a>So suchen Sie nach allen Vorkommen von CHARGE1 in nicht gebuchten Datensätzen (z. B. offenen Aufträgen)  

1.  Wählen Sie auf der Seite **Artikelablaufverfolgung** den Verweis in der ersten Verfolgungszeile aus, der Einkaufslieferung von CHARGE1.  
2.  Wählen Sie die Aktion **Navigieren** aus.  

    Auf der Seite **Navigate** sind basierend auf dem Ergebnis der Verfolgung für CHARGE1 Suchfilter voreingestellt. Der Qualitätskontrolleur stellt fest, dass sich die meisten Datensätze auf Belege beziehen, die bereits auf der Seite **Artikelablaufverfolgung** identifiziert wurden. Die letzte Zeile vom Typ "Fertigungsauftrag" bezieht sich z. B. auf die beiden freigegebenen Fertigungsaufträge, in denen Rennradrahmen aus CHARGE1 verbraucht wurden.  

    Die zweite Zeile vom Typ **Verkaufszeile** im Fenster "Navigieren" ist jedoch eine nicht gebuchte Belegzeile, sodass der Qualitätskontrolleur die Untersuchung fortsetzt.  

3.  Wählen Sie zum Öffnen des Verkaufszeilendatensatzes die zweite Zeile im Fenster "Navigate" aus, wählen Sie dann die Aktion **Anzeigen:** aus. Alternativ können Sie den Wert im Feld **Anzahl Datensätze** wählen.  

    Hier sieht der Qualitätskontrolleur eine offene Verkaufszeile für die fehlerhaften Rennradrahmen. Er empfiehlt der Verkaufsabteilung umgehend, diesen Auftrag zu stornieren und einen neuen Fertigungsauftrag mit fehlerfreien Rennradrahmen zu initiieren.  

 Damit ist die exemplarische Vorgehensweise zur Verwendung der Seiten **Navigieren** und **Artikelablaufverfolgung** für die Defektverwaltung abgeschlossen.  

## <a name="see-also"></a>Siehe auch
[Arbeiten mit Chargennummern und Seriennummern](inventory-how-work-item-tracking.md)  
[Verfolgen von Artikeln mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md)  
[Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  

