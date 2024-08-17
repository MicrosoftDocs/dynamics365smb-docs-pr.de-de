---
title: Informationen zum Berechnen der Standardkosten
description: Ein Standard-Kostensystem bestimmt die Kosten der Einheit des Bestandes auf der Grundlage angemessener historischer oder erwarteter Kosten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.author: bholtorf
ms.date: 07/26/2024
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="about-calculating-standard-cost"></a>Informationen zum Berechnen der Standardkosten

Viele Produktionsbetriebe verwenden feste Einstandspreise als Bewertungsbasis. Dies gilt auch für Unternehmen, die Leichtproduktion ausführen, wie Montage und Kitting. Ein Einstandspreissystem bestimmt die Kosten einer Lagerbestandseinheit anhand fundierter früherer oder erwarteter Kosten. Untersuchungen der früheren oder der erwarteten zukünftigen Kosten können dann die Basis für feste Einstandspreise bereitstellen. Diese Kosten bleiben unverändert, bis entschieden wird, sie zu ändern. Die Ist-Produktionskosten eines Produkts können von den erwarteten Einstandspreisen (fest) abweichen. Damit das Management steuernd eingreifen kann, werden die Ist-Kosten eines bestimmten Artikels mit dessen festem Einstandspreis verglichen. Dabei entdeckte Unterschiede oder *Abweichungen* werden gekennzeichnet und analysiert.  

Feste Einstandspreise können für Artikel verwaltet werden, die durch Einkauf, Montage und Produktion beschafft werden. Für jede Beschaffungsmethode können feste Einstandspreise aus den folgenden Elementen bestehen.  

|Beschaffungsmethode|Standardkostenelemente|  
|--------------------------|----------------------------|  
|**Einkauf**|Direkte Materialkosten und indirekte Materialkosten, falls erforderlich.|  
|**Montage**|Direkte Materialkosten, direkte oder feste Arbeitskosten und Gemeinkosten.|  
|**Fertigungsauftrag**|Direkte Materialkosten, Arbeitskosten, Subunternehmerkosten und Gemeinkosten.|  

## <a name="set-up-standard-costs"></a>Einrichten von Standardkosten

Da der Einstandspreis eines produzierten oder montierten Artikels aus mehreren Kostenelementen - Material-, Kapzitäts- und Fremdarbeitskosten (EK-Preise und Gemeinkosten) - besteht, muss der Einstandspreis für jedes dieser Elemente festgelegt werden.  

Die Kalkulationsaufgabe für einen Artikelproduktionsbetrieb, in dem Einstandspreise verwendet werden, besteht aus:  

- Kalkulieren Sie einen Einstandspreis für einen fertigen Artikel und richten sie ihn auf der Artikelkarte ein.  
- Erfassen und Zuordnen der Ist-Kosten der Produktionskostenelemente und genaues Feststellen von Abweichungen.  

Zum Bestimmen der direkten Kosten eines fertigen Artikels müssen alle Komponentenkosten summiert werden. Ein montierter oder hergestellter Artikel kann Unterbaugruppen umfassen, die auch aus mehreren Komponenten bestehen.  

Die folgenden wesentlichen Kostenelemente bilden die direkten Kosten eines fertig bearbeiteten Artikels:  

- Materialkosten.  
- Kapazitätskosten.  
- Fremdarbeitskosten nur für gefertigte Artikel.  

### <a name="material-costs"></a>Stoffkosten

Materialkosten sind Kosten, die Halbfabrikaten und gekauftem Rohmaterial zugeordnet sind. Materialeinstandspreise können aus direkten und indirekten Kostenelementen bestehen.  

- Direkte Materialkosten entsprechen dem in Rechnung gestellten Betrag für gekauftes Rohmaterial oder den Produktionskosten bei Halbfabrikaten.  
- Indirekte Materialkosten (oder *Gemeinkosten*) entsprechen beispielsweise den Logistikkosten für den produzierten fertigen Artikel.  

Das Konfigurieren der Materialkosten für Einkaufsartikel hinsichtlich der direkten und der indirekten Kosten hängt von der Lagerabgangsmethode ab, die für den fraglichen Artikel ausgewählt ist. Die Kosteninformationen für jede Lagerabgangsmethode auf der Artikelkarte. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

Ausschusskosten (nur Fertigung) sind ein anderer Faktor, der bei der Berechnung der Gesamtmaterialkosten zu berücksichtigen ist. Wenn bei der Montage oder Herstellung eines Artikels eine bestimmte Menge Rohmaterial als Ausschuss anfällt, hat dies zur Folge, dass mehr Komponenten benötigt werden, um den Artikel zu produzieren. Dadurch erhöhen sich auch dadurch die Materialkosten für die Komponenten, die beim Produzieren eines übergeordneten Artikels verbraucht werden. Ausschusskosten für Materialien können entweder auf der Fertigungsstückliste oder auf dem Arbeitsplan eingerichtet werden.  

Die Materialkosten eines Produktionsartikels können auf zwei Arten dargestellt werden, die den folgenden Berechnungsgrundlagen für feste Einstandspreise entsprechen.  

|Kostenberechnungsgrundlage|Materialkostenberechnung|  
|----------------------------|-------------------------------|  
|Einstufig|Der gefertigte Artikel entspricht den Gesamtkosten aller gekauften oder als Unterbaugruppen verbauten Artikel in der Fertigungsstückliste dieses Artikels.|  
|Mehrstufige Ebene oder mehrstufig|"Gefertigter Artikel" ist die Summe der Materialkosten aller Halbfabrikate in der Stückliste dieses Artikels und der Kosten aller Einkaufsartikel in der Fertigungsstückliste dieses Artikels.|  

### <a name="capacity-costs"></a>Kalkulation von Kapazitäten

Kapazitätskosten entsprechen den internen Bearbeitungs- und den Maschinenkosten. Sie müssen diese Kosten für jede Ressource (in der Montageverwaltung) und jeden Arbeitsplatz bzw. jede Arbeitsplatzgruppe im Arbeitsgang (in der Fertigung) einrichten. Wie bei den Materialien können Sie sowohl direkte als auch indirekte Elemente für die Kapazitätskosten angeben. Beispielsweise können die direkten Kosten für eine Arbeitsplatzgruppe gleich dem „Werkstattsatz“ sein, der für das Ausführen einer bestimmten Funktion anfällt. Die indirekten Kosten für eine Arbeitsplatzgruppe können den allgemeinen Unternehmensausgaben wie Beleuchtung, Heizung usw. entsprechen. Analog zu Materialkosten können Kapazitätsgemeinkosten als Prozentsatz indirekter Kosten und/oder als feststehender Gemeinkostenbetrag ausgedrückt werden.  

Die Einrichtung der Kapazitätskosten für montierte Artikel besteht aus den folgenden Elementen:  

- Direkter und indirekter Einstandspreis der Ressource.  
- Feste oder direkte Ressourcenverbrauchsart.  

Die Einrichtung der Kapazitätskosten für produzierte Artikel besteht aus den folgenden Elementen:  

- Direkter und indirekter Einstandspreis des Arbeitsplatzes bzw. der Arbeitsplatzgruppe.  
- Zeit und Losgröße einrichten.  

Zum Berechnen der Standardkapazitätskosten müssen Sie die Standardzeitlöhne festlegen, die zum Ausführen von Arbeitsgängen an Arbeitsplätzen oder Arbeitsplatzgruppen erforderlich sind. Die Gesamtzeit, die für einen Arbeitsgang erforderlich ist, besteht üblicherweise aus der Rüst- und der Bearbeitungszeit sowie der Warte- und der Transportzeit.  

Sie können die Sätze für diese Zeitarten für jeden Arbeitsplatz bzw. jede Arbeitsplatzgruppe in einem eigenen Arbeitsplan einrichten.  

> [!NOTE]  
>  Während Bearbeitungszeitsätze pro produziertem Artikel gelten, gelten Rüstzeitsätze pro Los. Daher muss die Arbeitsplanrüstzeit für jeden Arbeitsgang entsprechend der Losgröße umgelegt werden. Die Losgröße wird im entsprechenden Feld im Inforegister **Beschaffung** der Seite **Artikelkarte** angegeben.  

Um Rüstzeiten im Arbeitsgang für die Planung anzugeben, jedoch nicht bei der Einstandspreisberechnung zu berücksichtigen, leeren Sie das Feld **Kosten inkl. Rüsten** auf der Seite **Produktion Einrichtung**.  

Auf einer einstufigen Grundlage sind dies die Bearbeitungskosten, die erforderlich sind, um den fertigen Produktionsartikel herzustellen, und die im Arbeitsplan des Produktionsartikels angegeben werden. Auf einer mehrstufigen Grundlage, sind dies die Kapazitätskosten, die für jeden einzeln gefertigten Artikel, der in der Stückliste des übergeordneten Artikels enthalten ist, angegeben werden.  

### <a name="subcontractor-costs"></a>Kosten für Subunternehmer

Fremdarbeitskosten sind die Kosten, die Serviceleistungen zugeordnet sind, die von externen Kreditoren oder von Subunternehmern bereitgestellt werden. Ähnlich wie Material- und Kapazitätskosten können Fremdarbeitskosten sowohl aus direkten Kosten (Einstandspreise) als auch aus Gemeinkosten bestehen. Direkte Subunternehmerkosten entsprechen den tatsächlichen Kosten, pro bereitgestellter Serviceeinheit anfallen. Subunternehmergemeinkosten können z. B. den Fracht- und/oder Transportkosten entsprechen, die dem Unternehmen im Zusammenhang mit einem Auftrag entstehen, der einem Subunternehmer erteilt wurde.  

Da Fremdarbeit im Wesentlichen eine ausgelagerte Kapazität ist, werden die Kosten der Fremdarbeitsservices (sowohl direkte als auch indirekte Kosten) auf der Subunternehmer-Arbeitsplatzkarte eingerichtet.  

## <a name="update-standard-costs"></a>Standardkosten aktualisieren

Um den festen Einstandspreis von Montageartikeln zu aktualisieren oder zu berechnen, verwenden Sie die Funktion auf der Artikelkarte.  

Die Aktualisierung oder Berechnung von festen Einstandspreisen umfasst üblicherweise die folgenden Aufgaben:  

1.  Aktualisieren von Kosten auf der Komponenten- und Kapazitätsebene. Weitere Informationen finden Sie unter Stapelverarbeitungen **Artikel Einst.-Preis vorschlagen** und **Einstandspreis für Kapazität vorschlagen**.  
2.  Konsolidieren und mehrstufiges Berechnen der Komponenten- und Kapazitätskosten, um die Gesamtproduktionskosten der Artikel zu berechnen. Weitere Informationen finden Sie unter Weitere Informationen finden Sie unter [So berechnen Sie die Standardkosten für ein Montage-Element](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Implementieren der festen Einstandspreise, die bei der Ausführung der vorherigen Batchaufträge eingegeben werden. Die Einstandspreise (fest) treten erst in Kraft, wenn sie implementiert werden. Verwenden Sie den Stapelverarbeitungsauftrag **Einst.-Preis (fest) Vorschlag übernehmen**, der die Änderungen der Standardkosten für Artikel mit denen aus der Tabelle „Einst.-Preis (fest) Arbeitsblatt“ aktualisiert.  
4.  Implementieren der Änderungen, um das Feld **Einstandspreis** auf der Artikelkarte zu aktualisieren und eine Lagerneubewertung durchzuführen. Weitere Informationen finden Sie unter [Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md).

## <a name="use-batch-jobs-to-update-standard-costs"></a>Verwenden Sie Stapelverarbeitungsaufträge, um Einstandspreise (fest) zu aktualisieren
In den folgenden Abschnitten werden die Stapelverarbeitungsaufträge beschrieben, mit denen Sie Einstandspreise (fest) aktualisieren können.
### <a name="suggest-item-standard-cost"></a>Art. Einst.-Pr. (fest) vorschl

 Erstellt Vorschläge zum Ändern der Kosten und der Kostenanteile von Einstandspreisen (fest) auf Artikelkarten. Wenn die Stapelverarbeitung abgeschlossen ist, können Sie die Ergebnisse im Fenster „Einst.-Preis (fest) Arbeitsblatt“ anzeigen.

> [!NOTE]  
> Diese Stapelverarbeitung ist nur für Einkaufsartikel gedacht. Wenn Sie einen Artikel mit einer Fertigungsstückliste oder Montagestückliste aktualisieren möchten, müssen Sie zuerst das Arbeitsblatt mit allen Komponenten ausfüllen und anschließend die Stapelverarbeitung „Mehrstufigen Einstandspreis berechnen“ ausführen.

Diese Stapelverarbeitung erzeugt nur Vorschläge. Die vorgeschlagenen Änderungen werden nicht implementiert. Wenn Sie mit den Vorschlägen einverstanden sind und diese übernehmen möchten, sie also auf den Artikelkarten aktualisieren und sie im „Neubewertungs Buch.-Blatt“ einzufügen, wählen Sie dann „Einst.-Preis (fest) Vorschlag übernehmen“ im Fenster „Einst.-Preis (fest) Arbeitsblatt“.
#### <a name="options"></a>Optionen

**Einstandspreis (fest)**: Geben Sie den Korrekturfaktor ein, den Sie zur Aktualisierung des Einstandspreises (fest) verwenden möchten. Sie können auch eine Rundungsmethode für den neuen Einstandspreis (fest) verwenden. Sie müssen dieses Feld ausfüllen, indem Sie Nachkommastellen für die prozentuale Erhöhung verwenden, z. B. 1,1.

**Indirekte Kosten %**: Geben Sie den Korrekturfaktor ein, den Sie zur Aktualisierung der indirekten Kosten % verwenden möchten. Sie können auch eine Rundungsmethode für die neuen Kosten % verwenden. Sie müssen dieses Feld ausfüllen, indem Sie Nachkommastellen für die prozentuale Erhöhung verwenden, z. B. 1,1.

**Gemeinkostensatz**: Geben Sie den Korrekturfaktor ein, den Sie zur Aktualisierung des Gemeinkostensatzes verwenden möchten. Sie können auch eine Rundungsmethode für den neuen Gemeinkostensatz verwenden. Sie müssen dieses Feld ausfüllen, indem Sie Nachkommastellen für die prozentuale Erhöhung verwenden, z. B. 1,1.

### <a name="suggest-workmach-ctr-std-cost"></a>Kapazitätseinst.-Preis vorschlagen

Erstellt Vorschläge zum Ändern der Kosten und der Kostenanteile von Einstandspreis (fest) auf Arbeitsplatzgruppe, Arbeitsplatz oder Ressourcenkarten. Wenn die Stapelverarbeitung abgeschlossen ist, können Sie die Ergebnisse im Fenster **Einst.-Preis (fest) Arbeitsblatt** anzeigen.

Diese Stapelverarbeitung erzeugt nur Vorschläge. Die vorgeschlagenen Änderungen werden nicht implementiert. Wenn Sie mit den Vorschlägen einverstanden sind und diese übernehmen möchten, sie also auf den Arbeitsplatzgruppen-/Arbeitsplatz- und Ressourcenkarten aktualisieren und sie im Fenster „Neubewertungs Buch.-Blatt“ einzufügen, wählen Sie dann **Einst.-Preis (fest) Vorschlag übernehmen** im Fenster **Einst.-Preis (fest) Arbeitsblatt**.

Wenn Sie die Stapelverarbeitung ausgeführt haben und die Auswirkungen auf Ihre Produktions- oder Montageabteilungen sehen möchten, können Sie die Stapelverarbeitung **Mehrstufigen Einstandspreis berechnen** ausführen, um Einstandspreise (fest) in Arbeitsplatzgruppen, Arbeitsplätzen, Montageressourcen, Fertigungsstücklisten und Montagestücklisten zu aktualisieren.
#### <a name="options-1"></a>Optionen
**Einstandspreis (fest)**: Geben Sie den Korrekturfaktor ein, den Sie zur Aktualisierung des Einstandspreises (fest) verwenden möchten. Sie können auch eine **Rundungsmethode** für den neuen Einstandspreis (fest) verwenden. Sie müssen dieses Feld ausfüllen, indem Sie Nachkommastellen für die prozentuale Erhöhung verwenden, z. B. 1,1.

**Indirekte Kosten %**: Geben Sie den Korrekturfaktor ein, den Sie zur Aktualisierung der indirekten Kosten % verwenden möchten. Sie können auch eine Rundungsmethode für die neuen Kosten % verwenden. Sie müssen dieses Feld ausfüllen, indem Sie Nachkommastellen für die prozentuale Erhöhung verwenden, z. B. 1,1.

**Gemeinkostensatz**: Geben Sie den Korrekturfaktor ein, den Sie zur Aktualisierung des Gemeinkostensatzes verwenden möchten. Sie können auch eine Rundungsmethode für den neuen Gemeinkostensatz verwenden. Sie müssen dieses Feld ausfüllen, indem Sie Nachkommastellen für die prozentuale Erhöhung verwenden, z. B. 1,1.

### <a name="post-inventory-cost-to-gl"></a>Lagerregulierung auf Sachkonto buchen

 Bucht die Mengen- und Wertänderungen des Lagerbestands in den Artikelposten bzw. Wertposten, wenn Sie Lagerbestandstransaktionen wie Verkaufslieferungen oder Einkaufslieferungen buchen.

Sofern Sie das Kontrollkästchen **Automatische Lagerbuchung** im Fenster **Lagereinrichtung** ausgewählt haben, werden Lagerkosten nicht dynamisch in der Finanzbuchhaltung erfasst, und der Lagerverbrauch wird nicht mit einem Verkauf berechnet. Daher müssen Sie in die Finanzbuchhaltung manuell buchen, indem Sie die Stapelverarbeitung **Lagerregulierung buchen** ausführen, um die Finanzbuchhaltung zu aktualisieren und einen Bericht zu den Wertposten zu drucken, die gebucht werden.

Die Stapelverarbeitung verwendet Wertposten als ihre Ausgangspunkte. Zum Berechnen des zu buchenden Wertes verwendet die Stapelverarbeitung die Differenz zwischen den Wertposten in den Feldern **Einstandsbetrag (tatsächl.)** und **Gebuchte Lagerregulierung**. Wenn Sie das Kontrollkästchen **Soll-Kosten buchen** im Fenster **Lagereinrichtung** ausgewählt haben, bucht die Stapelverarbeitung auch die Differenz zwischen dem Feld **Einstandsbetrag (erwartet)** und dem Feld **Auf Sachkto. geb. Soll-K.** in den Interimskonten in der Finanzbuchhaltung.

> [!NOTE]
> Wenn Sie das Kontrollkästchen **Soll-Kosten buchen** im Fensterfeld **Lagereinrichtung** nicht gewählt haben, führt der letzte Abschnitt des Berichts Wertposten auf, die übersprungen werden, da sie Soll-Kosten darstellen.

> [!NOTE] 
> Stellt die Stapelvereinbarung beim Buchen von Lagerwerten in der Finanzbuchhaltung unter Einschluss von Dimensionen oder Dimensionseinrichtungen einen Fehler fest, setzt er den Fehler außer Kraft und verwendet für das Buchen des Postens in der Finanzbuchhaltung die Dimensionen des Wertpostens.

Wenn Sie sicherstellen möchten, dass die Stapelverarbeitung keine Fehler entdeckt, können Sie den Bericht **Lagerreg. buchen – Test** ausführen, um alle Fehler zu sehen, die auftreten können. Sie können die Fehler dann beheben und die Stapelverarbeitung **Lagerregulierung buchen** mit dem Wissen ausführen, dass alle Posten verarbeitet werden.
 
> [!IMPORTANT]  
> Bevor Sie diese Stapelverarbeitung verwenden, sollten Sie die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** ausführen. Dadurch stellen Sie sicher, dass die Werte, die von dieser Stapelverarbeitung in der Finanzbuchhaltung gebucht werden, auf dem aktuellsten Stand sind.
#### <a name="options-2"></a>Optionen

|Option  |Description  |
|--------------|---------|
|**Buchungsmethode**|Diese Stapelverarbeitung kann den Lagerwert entweder pro Buchungsgruppe oder pro gebuchtem Posten in die Finanzbuchhaltung buchen. Wenn Sie pro Posten buchen, erhalten Sie detaillierte Aufstellungen darüber, wie das Lager die Finanzbuchhaltung beeinflusst, Sie erhalten jedoch auch zahlreiche Posten in der Finanzbuchhaltung. Wenn Sie pro Buchungsgruppe buchen, erstellt die Stapelverarbeitung einen Sachposten pro Buchungsdatum und Buchungsgruppenkombination. Das heißt, für jede Kombination aus Buchungsdatum, Geschäftsbuchungsgruppe, Produktbuchungsgruppe, Lagerbuchungsgruppe und Lagerortcode wird ein Sachposten erstellt. Außerdem erstellt die Stapelverarbeitung getrennte Sachposten für Kosten mit unterschiedlichen Vorzeichen.|
|**Belegnr.**|In diesem Feld können Sie eine Belegnummer eingeben, wenn Sie die Option "Pro Lagerbuchungsgruppe" gewählt haben. Die Belegnummer erscheint auf den gebuchten Posten.|
|**Buchen**|Wählen Sie dieses Feld, wenn Sie möchten, dass die Stapelverarbeitung die Buchung in die Finanzbuchhaltung automatisch vornimmt. Wenn Sie nicht ausgewählt haben, dass die „Lagerregulierung“ in die Finanzbuchhaltung gebucht wird, wird von der Stapelverarbeitung nur ein Testbericht ausgedruckt, der die Werte enthält, die in die Finanzbuchhaltung gebucht werden können, und auf dem folgende Angabe erscheint: **Testbericht (nicht gebucht)**.|

### <a name="roll-up-standard-cost"></a>Standardkosten zusammenrechnen

Berechnet die Einstandspreise (fest) von montierten und gefertigten Artikeln. Diese werden beeinflusst durch Änderungen der Komponenteneinstandspreise, die von der Stapelverarbeitung **Art. Einst.-Pr. (fest) vorschlagen** vorgeschlagen wurden. Darüber hinaus werden sie von der Änderung des Einstandspreises (fest) der Produktionskapazität und Montageressourcen beeinflusst, die von der Stapelverarbeitung **Kapazitätseinst.-Preis vorschlagen** vorgeschlagen werden.

Sobald Sie eine Stapelverarbeitung (oder beide) ausgeführt haben und Sie die mehrstufige Berechnung durchführen, werden alle Änderungen der Einstandspreise (fest) im Arbeitsschein in die verknüpften Fertigungs- oder Montagestücklisten eingefügt und die Einstandspreise werden auf jeder Stücklistenebene angepasst.

> [!NOTE] 
> Diese Funktion berechnet nur die mehrstufigen Einstandspreise auf den Artikelkarten, nicht auf den Lagerhaltungsdatenkarten.

Diese Stapelverarbeitung erzeugt nur Vorschläge. Die vorgeschlagenen Änderungen werden nicht implementiert. Wenn Sie mit den Vorschlägen einverstanden sind und diese übernehmen möchten, sie also auf den Artikelkarten aktualisieren und sie im Fenster **Neubewertungs Buch.-Blatt** einzufügen, können Sie die Stapelverarbeitung **Einst.-Preis (fest) Vorschlag übernehmen** verwenden. Sie können diese Stapelverarbeitung aus dem Fenster **Einst.-Preis (fest) Vorschlag** aufrufen.
#### <a name="options-3"></a>Optionen

**Berechnungsdatum**: Geben Sie das Datum ein, das für die Stücklistenversionen gelten soll, für die Sie die mehrstufige Berechnung durchführen möchten.
 
### <a name="implement-standard-cost-change"></a>Standardkostenänderung implementieren

Aktualisiert die Einstandspreise der Tabelle **Artikel** mit denen aus der Tabelle **Einst.-Preis (fest) Arbeitsblatt**. Die Einstandspreisvorschläge können mit Hilfe der Stapelverarbeitung **Art. Einst.-Pr. (fest) vorschl** und/oder der Stapelverarbeitung **Kapazitätseinst.-Preis vorschlagen** erstellt und auch geändert werden. Der Inhalt aller Felder in den Einstandspreisvorschlägen wird übertragen. Wenn Sie Änderungen an Einstandspreisen implementieren, können Sie diese auf der Artikelkarte und/oder auf der Arbeitsplatzgruppen-/Arbeitsplatzkarte sehen. Darüber hinaus wird ein Neubewertungs-Buch.-Blatt erzeugt, mit dem Sie den Wert des vorhandenen Bestands aktualisieren können.
#### <a name="options-4"></a>Optionen

**Buchungsdatum**: Geben Sie das Datum ein, an dem die Neubewertung stattfinden soll.

**Belegnr.**: Geben Sie die Nummer der Neubewertungs Buch.-Blattzeilen ein. Wenn im Artikel Buch.-Blattnamen eine Nummernserie eingerichtet wurde, wird die Belegnummer auf die Nummer der Posten folgen, die beim Buchen des Neubewertungs Buch.-Blattes entstanden sind. Sonst können Sie manuell eine Nummer eingeben.

**Artikel Buch.-Blattvorlage**: Geben Sie den Namen der Neubewertungs Buch.-Blattvorlage ein.

**Artikel Buch.-Blattname**: Geben Sie den Namen des tatsächlichen Neubewertungs Buch.-Blatts ein

Wählen Sie **OK**, um die Stapelverarbeitung zu starten. Wenn Sie die Stapelverarbeitung nicht sofort starten möchten, wählen Sie **Abbrechen** aus, um das Fenster zu schließen.

## <a name="see-also"></a>Siehe auch

[Designdetails: Lagerabgangsmethoden](design-details-costing-methods.md)  
[Einst.-Preis (fest) aktual.](finance-how-to-update-standard-costs.md)  
[Design Details: Kalkulation des Bestandes](design-details-inventory-costing.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)  
[Arbeiten mit Stücklisten](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
