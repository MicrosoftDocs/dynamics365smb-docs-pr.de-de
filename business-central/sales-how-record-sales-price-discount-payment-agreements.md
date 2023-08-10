---
title: Spezielle Verkaufspreise und Rabatte aufzeichnen
description: 'Beschreibt, wie Sie Preis- und Rabattvereinbarungen für Verkaufsbelege definieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.date: 06/13/2023
ms.custom: bap-template
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '7022, 7024'
---

# <a name="record-special-sales-prices-and-discounts"></a>Spezielle Verkaufspreise und Rabatte aufzeichnen

> [!NOTE]
> Im 2. Veröffentlichungszyklus 2020 wurden neue, optimierte Prozesse zum Einrichten und Verwalten von Preisen und Rabatten eingeführt. Wenn Sie ein neuer Kunde sind, der die aktuelle Version verwendet, nutzen Sie die neue Umgebung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Erfahren Sie mehr unter [Bevorstehende Funktionen vorzeitig aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management) im Verwaltungsinhalt.

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt verschiedene Preisstrategien, wie zum Beispiel:

* Ein-Preis-für-alle-Modelle, bei denen ein Artikel immer zum gleichen Preis verkauft wird.
* Besondere Preisvereinbarungen mit bestimmten Kunden oder Kundengruppen.
* Kampagnen, wenn ein Verkauf die Kriterien für ein Sonderangebot erfüllt. Beispielsweise könnten Sie die folgenden Kriterien für einen Auftrag haben:

  * Er erfüllt eine Mindestmenge
  * Er ist vor einem bestimmten Datum
  * Er enthält eine bestimmte Art von Artikel  

Um ein einfaches Preismodell zu verwenden, müssen Sie nur einen Stückpreis angeben, wenn Sie einen Artikel oder eine Ressource einrichten. Dieser Preis wird immer für Verkaufsbelege verwendet. Für fortgeschrittenere Modelle, z. B. wenn Sie Sonderpreise für eine Verkaufskampagne anbieten möchten, können Sie auf der Seite **Verkaufspreise** Kriterien angeben. Sie können Sonderpreise auf der Grundlage einer Kombination der folgenden Informationen anbieten:  

* Debitor
* Artikel
* Einheit
* Mindestmenge
* Daten, die den Zeitraum definieren, für den die Preise gültig sind.

Nachdem Sie Sonderpreise eingerichtet haben, kann [!INCLUDE[prod_short](includes/prod_short.md)] den besten Preis für Verkaufs- und Einkaufsbelege sowie für Zeilen in der Auftrags- und Artikelerfassung berechnen. Erfahren Sie mehr unter [Bestpreisberechnung](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Für Verkaufsrabatte können Sie zwei Arten einrichten:

| Rabatttyp | Description |
| --- | --- |
| **Verkaufszeilenrabatt** |Fügt einen Betrag auf den Verkaufszeilen hinzu, die eine bestimmte Kombination aus Debitor, Artikel, Mindestmenge, Einheit oder des Start- und Enddatum haben. Dieser Typ gilt auf gleiche Weise für Verkaufsbelege. |
| **Rechnungsrabatt** |Ein Rabattprozentsatz, der von der Gesamtsumme des Verkaufsbelegs abgezogen wird, wenn die Summe aller Zeilen des Belegs einen bestimmten Mindestwert übersteigt. |

> [!TIP]  
> Wenn ein Artikel nie mit einem Rabatt verkauft werden sollte, lassen Sie die Skontofelder auf der Artikelseite leer und schließen Sie den Artikel nicht in einer Zeilenrabatteinrichtung ein.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Um Verkaufspreise für einen Debitor zu erstellen:

Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte „Aktuelle Erfahrung“. 

#### [Aktuelle Erfahrung](#tab/current-experience/)

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Kunden und klicken dann auf die Aktion **Preise**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Preis gewährt.

#### [Neue Erfahrung](#tab/new-experience/)  

Standardmäßig lautet der Status neuer Preislisten **Entwurf**. Preislistenentwürfe gehen nicht in die Preiskalkulation ein. Wenn Sie mit dem Hinzufügen von Zeilen fertig sind und die Preise verwenden möchten, können Sie den Status in **Aktiv** ändern.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?"), geben Sie **Debitoren** ein, und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Debitor und wählen Sie dann die Aktion **Verkaufspreislisten**. 
3. Wählen Sie **Neu**, um eine neue Verkaufspreisliste zu erstellen.
4. Füllen Sie bei Bedarf die Felder in den Inforegistern **Allgemein** und **Steuern** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Führen Sie einen der folgenden Schritte aus, um Elemente zur Liste hinzuzufügen:
   * Um viele Elemente hinzuzufügen, wählen Sie **Linien vorschlagen**. Geben Sie anschließend Filterkriterien ein, um die hinzuzufügenden Elementtypen anzugeben. Optional können Sie auch andere Einstellungen für die Artikel eingeben, die für die Preisliste spezifisch sind. Bei Bedarf können Sie diese Einstellungen später ändern.
   * Um Artikel aus einer anderen Preisliste zu kopieren, wählen Sie **Zeilen kopieren** und wählen Sie dann die zu kopierende Preisliste aus.
   * Um Elemente manuell hinzuzufügen, wählen Sie im Raster im Feld **Produkt-Typ** den Produkttyp aus, für den die Preisliste bestimmt ist. Füllen Sie je nach Auswahl die restlichen Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Um die Preisliste zu verwenden, klicken Sie auf das Feld **Status** und wählen Sie **Aktiv**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Verwenden von Verkaufs- und Einkaufspreislisten

> [!NOTE]
> Die Verwendung von Preislisten erfordert, dass Ihr Administrator das Funktionsupdate **Neue Verkaufspreis-Erfahrung** in der **Funktionsverwaltung** aktiviert. Erfahren Sie mehr unter [Bevorstehende Funktionen vorzeitig aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management) im Verwaltungsinhalt.

Die meisten der neuen Erfahrungen mit Verkaufspreisen ähneln der aktuellen Erfahrung, es gibt jedoch einige Unterschiede. In den folgenden Abschnitten werden diese Unterschiede erläutert.

Die **Ausgleich mit Typ** und **Ausgleich mit Nummer** In den Feldern können Sie auswählen, für was eine Preisliste gelten soll, z. B. Debitor oder Debitorenpreisgruppe. Mit **Spalten anzeigen für** können Sie Spalten ein- oder ausblenden, die für das Festlegen von Preisen, Rabatten oder Preisen und Rabatten relevant sind.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Konvertieren vorhandener Preise, wenn Sie die Aktualisierung der Preisfunktion aktivieren

Wenn Sie das Funktionsupdate **Neue Verkaufspreis-Erfahrung** auf der Seite **Funktionsverwaltung** aktivieren, wird die Anleitung **Funktionsdatenupdate** geöffnet. Verwenden Sie den Umschalter **Standardpreise verwenden** wie folgt:

* Wenn Sie mit allen Preisen auf einer einzigen Seite arbeiten möchten, aktivieren Sie sie. Bestehende Preise werden in eine Standardpreisliste für jedes der folgenden Dokumente umgewandelt:

  * Verkauf
  * Einkauf
  * Projektumsätze
  * Projekteinkäufe

  Sie können alle Preise für diese Bereiche auf der Seite **Preise Arbeitsblatt** bearbeiten. Die Standardpreislisten werden auf den Seiten **Einrichtung von Verkäufen und Forderungen**, **Einrichtung von Käufen und Verbindlichkeiten** und **Projekteinrichtung** festgelegt.

> [!NOTE]
> Wenn Preise nur für Artikel- oder Ressourcenkarten festgelegt sind, werden die Standardpreislisten während der Datenaktualisierung nicht mit diesen Preisen ausgefüllt. Sie können jedoch jede der Standardpreislisten oder die Seite **Preisarbeitsblatt** öffnen und die Aktion **Zeilen vorschlagen** nutzen, um die auf Artikel- oder Ressourcenkarten festgelegten Preise hinzuzufügen.

* Um Verkaufspreislisten zu verwenden, deaktivieren Sie sie. Bestehende Preise werden in eine neue Preisliste für jede Kombination von Folgendem umgewandelt:

  * Debitor
  * Debitorengruppe oder Kampagne
  * Start- und Enddaten
  * Währungen

Wenn Sie viele Kombinationen haben, haben Sie viele Preislisten.

Wenn Sie die neue Preisgestaltung bereits aktiviert haben, können Sie Standardpreislisten manuell erstellen oder eine vorhandene Preisliste als Standard angeben. Um eine vorhandene Preisliste als Standard festzulegen, aktivieren Sie den Schalter **Aktualisieren von Standardeinstellungen zulassen** auf der Preisliste. Setzen Sie dann auf den Seiten **Einrichtung von Verkäufen und Forderungen**, **Einrichtung von Käufen und Verbindlichkeiten** und **Projekteinrichtung** die Preisliste als standardmäßig.

### <a name="editing-active-price-lists"></a>Bearbeiten der aktiven Preislisten

Damit Bearbeiter Preise in aktiven Preislisten für Artikel, Ressourcen, Debitoren, Kreditoren und andere Entitäten, die Preise verwenden, bearbeiten können, aktivieren Sie den Umschalter **Bearbeiten des aktiven Preises zulassen** auf den Seiten **Einrichtung von Verkäufen und Forderungen** und **Einrichtung von Käufen und Verbindlichkeiten**.

Wenn der Umschalter **Bearbeiten des aktiven Preises zulassen** deaktiviert ist, müssen Sie, um Preise in einer Preisliste zu aktualisieren, den Status der Preisliste in **Entwurf** ändern, Ihre Änderung vornehmen und die Preisliste erneut aktivieren.

Die **Preisübersicht** Seite bietet eine Übersicht über alle Preise in Preislisten. Sie können Filter setzen, um die Preisliste einzugrenzen, die Sie ändern oder ergänzen möchten. Nachdem Sie die Preise geändert haben, verwenden Sie die Aktion **Zeilen überprüfen**, um die Preise mit anderen Preislistenzeilen zu vergleichen. Die Überprüfung von Preisen hilft, Duplikate und Mehrdeutigkeiten bei der Preisberechnung zu vermeiden.

> [!NOTE]
> Wenn Sie eine Zeile in einer aktiven Preisliste bearbeiten, wird der Status der Zeile auf **Entwurf** gesetzt, und die Zeile wird bei der Preisberechnung erst berücksichtigt, wenn Sie die Aktion **Zeilen überprüfen** verwenden. Nachdem Sie den Preis überprüft haben, wird der Status der Position **Aktiv** und in Preisberechnungen berücksichtigt.

Um neue Preise hinzuzufügen, verwenden Sie auf der Seite **Preisübersicht** die Aktion **Neue Zeilen hinzufügen**. Die Seite **Arbeitsblatt Preise** öffnet sich und Sie können Preiszeilen hinzufügen, indem Sie sie entweder anhand von Kriterien vorschlagen, aus anderen Preislisten kopieren oder manuell eingeben. Anschließend können Sie mit der Aktion **Preisvorschlag übernehmen** die neuen Preise mit anderen Preislisten vergleichen, um Duplikate und Unklarheiten bei der Preisberechnung zu vermeiden.

#### <a name="create-sales-price-lines-based-on-the-unit-price"></a>Erstellen Sie Verkaufspreiszeilen basierend auf dem Stückpreis

1. Auf der Seite **Preisarbeitsblatt** wählen Sie die Aktion **Vorgeschlagene Zeilen** aus.
2. Füllen Sie auf der Seite **Preiszeilen - Neu erstellen** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Legen Sie im Feld **Produktfilter** die Filter für den ausgewählten **Produkttyp** fest.
4. Wählen Sie das Feld **Standardwerte** zum Festlegen von Einstellungen wie:
   * Welchen Entitäten die Preisliste zugeordnet wird.
   * Daten, an denen der Preis gültig ist.
   * Der Währungscode.
   * Der Betragstypfilter an, der die in den Preislistenzeilen angezeigten Spalten definiert.
5. Wählen Sie **OK** aus. Neue Zeilen werden auf der Seite **Preis Arbeitsblatt** mit den gewählten Einstellungen und den Stückpreisen aus den Artikelkarten hinzugefügt.
6. Bearbeiten Sie die erstellten Zeilen mit den neuen Stückpreisen oder Rabatten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="create-sales-price-lines-based-on-existing-price-lists"></a>Erstellen Sie Verkaufspreiszeilen basierend auf vorhandenen Preislisten

1. Wählen Sie auf der Seite **Preisarbeitsblatt** die Aktion **Zeilen kopieren** aus.
2. Auf der Seite **Preiszeilen – Vorhandene kopieren** wählen Sie eine vorhandene Preisliste im Feld **Aus Preisliste** aus.
3. Im Feld **Preiszeilenfilter** definieren Sie Filter für die Produkte in der ausgewählten Preisliste.
4. Wählen Sie das Feld **Standardwerte** zum Festlegen von Einstellungen wie:
   * Welchen Entitäten die Preisliste zugeordnet wird.
   * Daten, an denen der Preis gültig ist.
   * Der Währungscode.
   * Der Betragstypfilter an, der die in den Preislistenzeilen angezeigten Spalten definiert.
5. Füllen Sie die anderen Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Wählen Sie **OK** aus. Neue Zeilen werden der Seite **Preis Arbeitsblatt** mit den gewählten Einstellungen hinzugefügt.
7. Bearbeiten Sie die erstellten Zeilen mit den neuen Stückpreisen oder Rabatten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-sales-prices"></a>Verkaufspreise kopieren

Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte „Aktuelle Erfahrung“.

#### [Aktuelle Erfahrung](#tab/current-experience/)  

Falls Sie Verkaufspreise kopieren möchten, wie z. B. den Preis eines einzelnen Debitors, um ihn in einer Debitorengruppe zu verwenden, müssen Sie die Stapelverarbeitung **VK-Preis vorschlagen** ausführen. Stapelverarbeitung auf der Seite **VK-Preisarbeitsblatt**.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufspreisarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den **Vorgeschlagenen Verkaufspreis auf dem Arbeitsblatt.** Aktion  
3. Füllen Sie im Inforegister **Verkaufspreise** die Felder mit der **Verkaufsart** und dem **Verkaufscode** der ursprünglichen Preise aus, die Sie kopieren möchten.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.  
5. Wenn Sie mit dem Stapelverarbeitungsauftrag neue Preise erstellen wollen, wählen Sie in das Kästchen **Neue Preise generieren**.  
6. Wählen Sie die Schaltfläche **OK**, um die Zeilen auf der Seite **VK-Preisarbeitsblatt** mit den neuen Preisvorschlägen auszufüllen, und geben Sie an, dass diese für die gewählte Verkaufsart gültig sind.  

   > [!NOTE]  
   > Die Stapelverarbeitung erzeugt nur Vorschläge, implementiert die vorgeschlagenen Änderungen aber nicht. Falls Sie die Vorschläge annehmen möchten, d. h. sie auf die Seite **VK-Preise** übernehmen möchten, können Sie die Aktion **Preisvorschlag übernehmen** verwenden, die Sie …auf der Seite **VK-Preisarbeitsblatt** finden.

#### [Neue Erfahrung](#tab/new-experience/)  

Sie können die Einstellungen festlegen, die die Preisliste verwenden soll:

* Verwenden Sie die Einstellungen aus der Kopfzeile der Liste, die Sie kopieren.
* Verwenden Sie die Einstellungen aus der Liste, in die Sie kopieren. Um die Einstellungen aus der Preisliste zu verwenden, in die Sie Preise kopieren, aktivieren Sie den Umschalter **Standardwerte aus Ziel verwenden** verwenden.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufspreislisten** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die zu kopierende Preisliste aus und wählen Sie dann **Zeilen kopieren**.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Es dürfen keine zwei Artikel mit identischen Einstellungen, aber unterschiedlichen Preisen vorhanden sein. In diesem Fall wird eine Meldung angezeigt, wenn Sie die Preisliste aktivieren. Sie können den zu verwendenden Preis auswählen, indem Sie die Liste öffnen und den falschen Preis löschen.  
  
---

## <a name="to-bulk-update-item-prices"></a>So aktualisieren Sie Debitorenartikelpreise auf einmal

Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte „Aktuelle Erfahrung“.

#### [Aktuelle Erfahrung](#tab/current-experience/)

Wenn Sie Artikelpreise, wie alle Lagerzugangs-Artikelpreise durch einen Prozentsatz auf einmal aktualisieren möchten, müssen Sie Verkaufspreisarbeitsblatt mithilfe der folgenden Batchvorgänge ausfüllen:

* **VK-Preis vorschlagen** schlägt Änderungen auf eine von zwei Arten vor:

  * Durch Anwendung eines Korrekturfaktors auf bestehende Verkaufspreise.
  * Durch Kopieren bestehender Verkaufspreisvereinbarungen auf andere Debitoren, Debitorenpreisgruppen oder Verkaufsaktionen.

* **Artikelpreis vorschlagen** schlägt Änderungen auf eine von zwei Arten vor:

  * Durch Anwendung eines Korrekturfaktors auf bestehende Einheitspreise auf Artikelkarten.
  * Indem Sie Preise für neue Kombinationen aus Währung, Maßeinheiten usw. vorschlagen.

  Dieser Stapelverarbeitungsauftrag ändert die Einheitspreise für Artikel nicht.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkaufspreisarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Artikelpreis auf dem Arbeitsblatt vorschlagen** aus.  
3. Füllen Sie im Inforegister **Artikel** die **Nr.** oder **Bestand-Buchungsgruppe** oder andere Felder mit den ursprünglichen Artikelpreisen aus, die Sie aktualisieren möchten ein.  
4. Füllen Sie im oberen Bereich der Anforderungsseite die Felder **Verkaufsart** und **Verkaufscode** mit der Art und dem Namen aus, in die Sie die Verkaufspreise kopieren möchten.
5. Wenn Sie möchten, dass die Stapelverarbeitung automatisch eingegeben wird, geben Sie Anpassung ein im Feld **Korrekturfaktor**. Beispielsweise geben Sie entsprechend 1.15 unter **Korrekturfaktor** für die Preiserhöhung für den Artikelpreis um 15 % ein.  
6. Wenn Sie mit dem Batchauftrag neue Preise erstellen wollen, aktivieren Sie den Schalter **Neue Preise generieren**.  
7. Wählen Sie die Schaltfläche **OK**, um die Zeilen auf der Seite **Verkaufspreisarbeitsblatt** mit den vorgeschlagenen neuen Preisen auszufüllen.
8. Um die Vorschläge umzusetzen, verwenden Sie die Aktion **Preisänderungen implementieren**. Der Batch-Job erstellt Vorschläge, setzt diese jedoch nicht um. 

#### [Neue Erfahrung](#tab/new-experience/)

Um die Preise für mehrere Artikel zu aktualisieren, müssen Sie eine neue Preisliste erstellen und dann die Zeilen aus einer vorhandenen Preisliste kopieren. Wenn Sie die Zeilen kopieren, können Sie mithilfe von Filtern angeben, was kopiert werden soll, und Sie können eine Ganzzahl oder eine Dezimalzahl im Feld **Anpassungsfaktor** zum Erhöhen oder Verringern der Preise angeben. Die Preisliste muss sich im Status **Entwurf** befinden. Bei Bedarf können Sie dann die alte Preisliste deaktivieren.

> [!NOTE]
> Sie können nicht zwei Zeilen mit denselben Einstellungen, aber unterschiedlichen Preisen verwenden. In diesem Fall wird eine Meldung angezeigt, wenn Sie eine Preisliste aktivieren. Sie können den zu verwendenden Preis auswählen, indem Sie die Liste öffnen und den falschen Preis löschen.  

---

## <a name="best-price-calculation"></a>Berechnung des besten Preises

Nachdem Sie Sonderpreise und Zeilenrabatte für Verkäufe und Käufe erfasst haben,, berechnet [!INCLUDE[prod_short](includes/prod_short.md)] den besten Preis für Verkaufs- und Einkaufsbelege sowie für Auftrags- und Artikelerfassungszeilen berechnen.

Der beste Preis ist der niedrigste Preis mit dem höchsten Zeilenrabatt an einem bestimmten Datum. [!INCLUDE[prod_short](includes/prod_short.md)] berechnet die besten Preise, wenn Sie den Verkaufspreis und die prozentualen Zeilenrabatte für Artikel auf neuen Beleg- und Buch.-Blattzeilen eingefügt haben.

> [!NOTE]  
> Nachfolgend wird erläutert, wie die besten Preise für Verkäufe berechnet werden. Für Einkäufe ist die Berechnung ähnlich, basiert jedoch auf den verfügbaren Parametern. Beispielsweise werden Artikelrabattgruppen für den Einkauf nicht unterstützt.

1. [!INCLUDE[prod_short](includes/prod_short.md)] prüft die Kombination aus Rechnungsempfänger und Artikel und wählt den entsprechenden Verkaufspreis/Rabatt unter Verwendung der folgenden Kriterien:

    * Hat dieser Debitor eine spezielle Vereinbarung für Preise oder Zeilenrabatte oder gehört der Debitor zu einer Gruppe, die solche Vereinbarungen hat?
    * Ist der Artikel oder die Artikelrabattgruppe in der Zeile in einer dieser Prei-/Rabattvereinbarungen enthalten?
    * Liegt das Datum innerhalb des Start- und Enddatums der Preis-/Rabattvereinbarung? Bei Rechnungen und Gutschriften handelt es sich um das Datum im Feld **Buchungsdatum** in der Dokumentkopfzeile. Bei allen anderen Dokumenten handelt es sich um das Datum im Feld **Auftragsdatum** in ihren Kopfzeilen.
    * Wurde ein Einheitencode angegeben? Falls dies der Fall ist, prüft [!INCLUDE[prod_short](includes/prod_short.md)] Preise/Rabatte mit dem gleichen Einheitencode und die Preise und Rabatte, bei denen kein Einheitencode angegeben wurde.

2. [!INCLUDE[prod_short](includes/prod_short.md)] prüft, ob Preis-/Rabattvereinbarungen für Informationen auf der Beleg- oder Journalzeile gelten. Anschließend fügt es den anwendbaren Einheitspreis und den Zeilenrabattprozentsatz unter Verwendung der folgenden Kriterien ein:

    * Gibt es eine Mindestanzahl in der Preis-/Rabattvereinbarung, die erfüllt ist?
    * Gibt es eine Währungsanforderung in der Preis-/Rabattvereinbarung, die erfüllt ist? In diesem Fall werden der niedrigste Preis und der höchsten Zeilenrabatt für diese Währung eingefügt, selbst wenn lokale Währung einen besseren Preis liefern würde. Falls es für den angegebenen Währungscode keine Preis-/Zeilenrabatte gibt, verwendet [!INCLUDE[prod_short](includes/prod_short.md)] den niedrigsten Preis und den höchsten Zeilenrabatt in Ihrer lokalen Währung.

Wenn keine Spezialpreise für die Artikel in der Zeile gefunden werden, werden entweder die letzten direkten Kosten oder der VK-Preis von der Artikelkarte oder der Lagerhaltungsdatenkarte verwendet.

## <a name="sales-invoice-discounts-and-service-charges"></a>Verkaufsrechnungsrabatte und Servicegebühren

Wenn Sie Rechnungsrabatte verwenden, bestimmt der Gesamtbetrag des Rechnungsbetrages die Höhe des Rabattes, der gewährt wird. Auf der Seite **Debitorenrechnungsrabatte** können Sie eine Servicegebühr für Rechnungen über einem bestimmten Betrag einrichten.  

Bevor Sie Rechnungsrabatte mit Verkäufen verwenden können, müssen Sie einige Informationen in der Anwendung definieren. Sie müssen Folgendes entscheiden:  

* Welchen Debitoren diese Art von Rabatt gewährt wird?  
* Welche Rabattprozentsätze Sie verwenden möchten?  

Wenn Sie Rechnungsrabatte automatisch berechnen möchten, aktivieren Sie auf der Seite **Debitoren & Verkauf Einr.** den Umschalter für **Rechnungsrabatt berechnen**.  

Sie können für jeden Debitor festlegen, ob Sie Rechnungsrabatte gewähren, wenn eine Rechnung bestimmte Kriterien erfüllt. Zum Beispiel, wenn der Rechnungsbetrag groß genug ist. Rechnungsrabatte können in Landeswährung für inländische Debitoren oder in Fremdwährung für ausländische Debitoren gewährt werden.  

Sie verknüpfen Rabattprozentsätze mit bestimmten Rechnungsbeträgen auf den Seiten **Debitorenrechnungsrabatte** für jeden Debitor. Sie können eine beliebige Anzahl von Prozentsätzen auf jeder Seite eingeben. Jeder Debitor kann eine eigene Seite haben, oder Sie können verschiedene Debitoren mit der gleichen Seite verknüpfen.  

Zusätzlich (oder anstatt) eines Rabattprozentsatzes können Sie eine Servicegebühr mit einem bestimmten Rechnungsbetrag verknüpfen.  

> [!TIP]  
> Bevor Sie diese Informationen eingeben, ist es sinnvoll, eine Skizze der Rabattstruktur vorzubereiten, die Sie verwenden möchten. Die Struktur erleichtert es Ihnent, zu bestimmen, welche Debitoren mit derselben Rechnungsrabattseite verknüpft werden können. Wenn Sie weniger Seiten einrichten müssen, können Sie die Basisinformationen schneller eingeben.

Weitere Informationen zur Schulung für Rabatte bei Verkäufen finden Sie unter [Einrichten von Rabatten für Ihre Debitoren](/training/modules/customer-discounts-dynamics-365-business-central/index).

### <a name="calculating-invoice-discounts-on-sales"></a>Rechnungsrabatte bei Verkäufen berechnen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>So erstellen Sie Verkaufszeilenrabatte für einen Debitor:

Diese Schritte unterscheiden sich je nachdem, ob Ihr Administrator das Feature-Update **Neues Verkaufspreiserlebnis** aktiviert hat. Wenn das Funktionsupdate nicht aktiviert ist, befolgen Sie die Schritte auf der Registerkarte „Aktuelle Erfahrung“.

#### [Aktuelle Erfahrung](#tab/current-experience/)  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf **Zeilenrabatte**.
3. Füllen Sie die Felder in der Zeile wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Füllen Sie eine Zeile für jede Kombination aus, die dem Debitor einen besonderen Verkaufszeilenrabatt gewährt.

> [!NOTE]
> Wenn Sie die Seiten **Verkaufspreise** und **Verkaufszeilenrabatte** von einem bestimmten Debitoren öffnen, werden die Felder **Verkaufsartfilter** und **Verkaufscodefilter** für den Debitor festgelegt und können nicht geändert oder entfernt werden.
>
> Um Preise oder Zeilenrabatte für alle Debitoren, eine Debitorenpreisgruppe oder Kampagne einzurichten, müssen Sie die Seiten von einer Artikelkarte aus öffnen. Verwenden Sie alternativ für Verkaufspreise die Seite **VK-Preisarbeitsblatt**. Weitere Informationen finden Sie unter [So führen Sie eine Sammelaktualisierung von Artikelpreisen durch](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Neue Erfahrung](#tab/new-experience/)  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Debitor und dann die Aktion **Verkaufspreislisten**.
3. Öffnen Sie die Preisliste, für die der Zeilenrabatt angegeben werden soll.
4. Erstellen Sie eine neue Zeile oder wählen Sie eine vorhandene Zeile aus und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Wählen Sie im Feld **Definiert** entweder **Preis und Rabatt** oder einfach **Rabatt**. 
6. Legen Sie im Feld **Zeilenrabatt %** den Rabattprozentsatz fest.

    > [!TIP]
    > Wenn Sie eine vorhandene Zeile bearbeiten, können Sie die Zeilen filtern, indem Sie die entsprechende Option im Feld **Spalten anzeigen für** auswählen.

    > [!NOTE]  
    > Rechnungsrabattcodes werden durch BestandsDebitorenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt. Um debitorenspezifische Rechnungsrabattbedingungen einzurichten, setzen Sie das Feld **Rechnungs-Rabatt-Code** auf den Debitorencode des Debitoren und fahren Sie dann mit dem nächsten Schritt fort.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Um Rechnungsrabattkonditionen für Einkäufe einzurichten

Nachdem Sie entschieden haben, welche Kunden für Rechnungsrabatte in Frage kommen, geben Sie den Rechnungsrabattcode auf den Debitorenkartenseiten ein. Legen Sie dann die Bedingungen für jeden Code fest.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Wie möchten Sie weiter verfahren“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Debitorenseite für einen Debitor, der für Rechnungsrabatte in Frage kommt.
3. Geben Sie im Feld **Rechnungsrabattcode** einen Code für das jeweilige Rechnungsrabattfenster ein, das die Anwendung verwenden soll, um Rechnungsrabatte für den Debitor zu berechnen.

> [!NOTE]  
> Rechnungsrabattcodes werden durch BestandsDebitorenkarten dargestellt. Dies ermöglicht es Ihnen, Rechnungsrabattbedingungen schnell einem Debitor zuzuweisen, indem es den Namen eines anderen Debitors mit den selben Konditionen auswählt.

Fahren Sie fort, um neue Verkaufsrechnungsrabatt-Bedingungen einzurichten.

1. Auf der Seite **Debitoren** wählen Sie die Aktion **Rechnungsrabatt** aus. Die Seite **Debitorenrechnungsrabatte** wird geöffnet.
2. Geben Sie in dem Feld **Währungscode** den Code für die Währung ein, für die die Rechnungsrabattkonditionen gelten sollen. Wenn Sie Rechnungsrabattbedingungen in EUR einrichten möchten, dann lassen Sie das Feld leer.
3. Geben Sie im Feld **Minimalbetrag** den Mindestbetrag ein, den eine Rechnung aufweisen muss, um für einen Rabatt in Frage zu kommen.
4. Geben Sie im Feld **Rabatt %** den Rechnungsrabatt als Prozentsatz des Rechnungsbetrages ein.
5. Wiederholen Sie die Schritte 5 bis 7 für jede Währung, für die der Debitor einen Rechnungsrabatt erhält.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Einrichten von Verkäufen](sales-setup-sales.md)  
[Verkauf](sales-manage-sales.md)  
[Einrichten von Debitorenpreisgruppen](sales-how-to-set-up-customer-price-groups.md)  
[Einrichten von Debitorenrabattgruppen](sales-how-to-set-up-customer-discount-groups.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
