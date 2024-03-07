---
title: Festlegen und Verwenden des Shopify Konnektors
description: Verschiedene Integrationsszenarien zur Demonstration des Workflows zwischen Shopify und Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# Exemplarische Vorgehensweise: Festlegen und Verwenden des Shopify Konnektors

Dieser Abschnitt demonstriert einige typische Szenarien und führt Sie durch die Schritte, mit denen Sie den Workflow des integrierten [!INCLUDE[prod_short](../includes/prod_short.md)] und des Shopify Stores testen oder Benutzer schulen können.

## Voraussetzungen 

### Shopify

Sie benötigen Folgendes:

- Ein Shopify-Konto
- Ein Shopify-Online-Store

Erfahren Sie mehr darüber, wie Sie Shopify-Tests erstellen, und über die empfohlenen Einstellungen unter [Ein Shopify-Konto erstellen und einrichten](shopify-account.md).

### Business Central

Sie müssen ein [!INCLUDE[prod_short](../includes/prod_short.md)]-Konto haben. 

Sie können zum Beispiel ein Demokonto erstellen oder eine Testversion starten. Weitere Informationen finden Sie unter [Demonstrationsumgebung vorbereiten für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) und [Anmelden für den Test](../trial-signup.md). 

## Verbinden Sie Business Central mit dem Shopify-Laden

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den dazugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Geben Sie in das Feld **Code** `DEMO1` ein.
4. Geben Sie in das Feld **Shopify URL** die URL für den Onlineshop ein, mit dem Sie eine Verbindung herstellen möchten.
5. Aktivieren Sie den Schalter **Aktiviert** und lesen und akzeptieren Sie dann die Bestimmungen.

Gehen Sie wie folgt vor, um den Shopify-Shop zu konfigurieren.

1. Schalten Sie den Schalter **Hintergrundsynchronisationen zulassen** aus.
2. Wählen Sie *Zu Shopify* in dem Feld **Element synchronisieren**.
3. Wählen Sie *Bis Shopify* im Feld **Bilder von Elementen synchronisieren**.
4. Schalten Sie das Kontrollkästchen **Artikelattribute synchronisieren** ein.
5. Schalten Sie das Kontrollkästchen **Bestand verfolgen** ein.
6. Wählen Sie *Ablehnen* im Feld **Standardrichtlinie für den Bestand**.
7. Schalten Sie die Option **Unbekannte Kunden automatisch erstellen** ein.
8. Füllen Sie das Feld **Kundenvorlagencode** mit der entsprechenden Vorlage aus.
9. Füllen Sie das Feld **Versandkostenkonto**, das Feld **Tippkonto** mit dem Umsatzkonto aus. In den USA verwenden Sie zum Beispiel `40210`.
10. Schalten Sie die Option **Bestellungen automatisch erstellen** ein.

Konfigurieren Sie die Zuordnung von Standorten:

1. Wählen Sie die Aktion **Standorte** aus, um **Shopify-Shop-Standorte** zu öffnen.
2. Wählen Sie die Aktion **Shopify Standorte abrufen** aus, um alle in Shopify festgelegten Standorte zu importieren. Wählen Sie Ihren Standardstandort in Shopify aus.
3. Geben Sie im **Ortsfilter** `''|EAST|MAIN` ein.
4. Aktivieren Sie den Schalter **Standardproduktstandort**.
5. Wählen Sie *Geplanter verfügbarer Saldo heute* im Feld **Lagerbestandsberechnung** aus, um eine Lagerbestandssynchronisierung für einen ausgewählten Shopify-Standort zu aktivieren.

## Exemplarische Vorgehensweise: Mit dem Online-Verkauf von Produkten beginnen

### Szenario

Nehmen wir an, Sie möchten Shopify als Onlineshop ausprobieren, ohne viel Zeit mit der Einrichtung zu verbringen, vor allem, weil Sie Ihre Artikel in [!INCLUDE[prod_short](../includes/prod_short.md)] bereits gut pflegen. Nachdem Sie Ihren Shopify-Online-Store eröffnet haben, erhalten Sie sofort neue Kunden, die mit Ihrem Shop und ihrem Einkaufserlebnis zufrieden sind. Also beschließen sie, an der Kasse Tipps zu hinterlassen.

### Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol aus, geben Sie **Shopify Produkte** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie **Artikel hinzufügen**.
3. Geben Sie in das Feld **Shop Code** *DEMO1* ein.
4. Legen Sie den Filter `CHAIR` auf dem Feld **Element-Kategorie-Code** fest (fügen Sie bei Bedarf ein Filterfeld hinzu).
5. Wählen Sie **OK** und warten Sie, bis die anfängliche Synchronisierung von Artikeln und Preisen abgeschlossen ist.
6. Wählen Sie **Produktbilder synchronisieren** aus.
7. Wählen Sie **Lagerbestand synchronisieren** aus.

Tun Sie im **Shopify-Onlineshop** Folgendes:
> [!Tip]  
> Öffnen Sie **Shopify Verwaltung**, indem Sie die URL aufrufen, die im Feld **URL** auf der Seite **Shopify Shop-Karte** angegeben ist. Wählen Sie anschließend das Augensymbol neben dem Verkaufskanal **Onlineshop** aus, der sich in der Seitenleiste der **Shopify-Verwaltung** befindet. 

Öffnen Sie den Produktkatalog. Beachten Sie:

* Produkttitel, Bilder und Preise.
* Verfügbarkeitsanzeige (ausverkauft für Produkte, die nicht auf Lager sind).

Wählen Sie ein beliebiges Produkt, das verkauft werden kann, zum Beispiel den `BERLIN Swivel Chair, yellow`. Beachten Sie, dass die Beschreibung Artikelattribute enthält.

Wählen Sie **Jetzt kaufen** aus und gehen Sie zur Kasse.

1. Geben Sie in das Feld **E-Mail- oder Mobiltelefonnummer** die `cl@contoso.com` ein (oder die E-Mail, an die Sie Bestell- und Versandbestätigungen erhalten möchten).
2. Geben Sie in die Felder **Vorname** und **Nachname** `Claudia Lawson` ein.
3. Geben Sie die lokale Adresse ein.
4. Wählen Sie das Kontrollkästchen **Diese Informationen für das nächste Mal speichern** aus.
5. Wählen Sie **Weiter zum Versand** aus.
6. Behalten Sie `Standard` als Versandart bei und wählen Sie dann die Schaltfläche **Weiter zur Zahlung**.
7. Wählen Sie `10%` Tipp.
8. Geben Sie im Feld **Kreditkarte** eine `1` ein, wenn Sie *(zu Testzwecken) Bogus Gateway* verwenden oder geben Sie `5555 5555 5555 4444` ein, wenn Sie *Shopify Payments* im Testmodus verwenden.
9. Füllen Sie das Feld **Name auf der Karte** aus.
10. Geben Sie in das Feld **Ablaufdatum** den aktuellen Monat/Jahr ein.
11. In das Feld **Sicherheitscode** geben Sie `111` ein.
12. Wählen Sie **Jetzt bezahlen**.

Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die nächsten Schritte aus:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Shopify-Aufträge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
3. Wählen Sie **OK** aus.

Die importierte Bestellung ist bereit zur Verarbeitung.

1. Wählen Sie den importierten Auftrag, um das Fenster **Shopify Aufträge** zu öffnen.
2. Beachten Sie, dass die neue Kundschaft und die neuen Verkaufsaufträge erstellt wurden.
3. Erkunden Sie die Aktionen **Risiko** und **Versandkosten**.
4. Wählen Sie **Verkaufsauftrag** aus, um das Fenster **Verkaufsauftrag** zu öffnen. Ein Verkaufsauftrag ist ein Bedarf, der, falls erforderlich durch Montage, Produktion oder Kauf mit Hilfe des Planungsmoduls gedeckt werden kann. Es unterstützt auch verschiedene Lagerort-Verarbeitungsprozesse mit vollständiger Aufgabentrennung.
5. Wählen Sie die Aktion **Erneut öffnen** aus.
6. Geben Sie in das Feld **Bearbeiter** `DHL` ein.
7. Geben Sie in das Feld **Paketverfolgungsnummer** `123456789` ein.
8. Wählen Sie **Buchen**, behalten Sie die Option **Versand und Rechnung** bei und wählen Sie dann **OK** aus.

Jetzt sind die physischen und finanziellen Daten in [!INCLUDE[prod_short](../includes/prod_short.md)] registriert. Jetzt ist es an der Zeit, Shopify über die Änderungen zu informieren.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol aus. Geben Sie **Lieferungen mit Shopify synchronisieren** ein und wählen Sie dann den dazugehörigen Link aus.
2. Wählen Sie **OK** aus.

Beachten Sie, dass in der **Shopify-Verwaltung** die Bestellung jetzt als *Erfüllt* gekennzeichnet ist. Sie können auch die Details der Sendung einsehen und die URL der Sendungsverfolgung sehen. Wenn Sie **Bestellungen von Shopify synchronisieren** erneut ausführen, wird die Bestellung in beiden Systemen archiviert.

## Exemplarische Vorgehensweise: Laden Sie Ihre Kunden in Ihren neuen Online Store ein

### Szenario

Nach einem erfolgreichen Schnellstart Ihres neuen Online Stores möchten Sie, dass Ihre derzeitigen Kunden ihn besuchen und Bestellungen aufgeben.

### Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den **DEMO1** Shop, für den Sie Kunden synchronisieren möchten, um die **Shopify Shop Card** Seite zu öffnen.
3. Wählen Sie **Debitoren synchronisieren**.

Beachten Sie, dass die Debitoren in der **Shopify-Verwaltung** importiert wurden. Öffnen Sie einen der Kunden und stellen Sie fest, dass der Vor- und Nachname des Kunden aus dem Feld **Kontaktname** der **Kundenkarte** stammt. Der Name der Firma ist in der Standardadresse zu finden, die mit dem Kunden verknüpft ist. Wählen Sie **Kontoeinladung senden**, um den Debitor einzuladen.

## Exemplarische Vorgehensweise: Feinabstimmung der Artikelverwaltung

### Szenario 

Sie möchten Ihren Prozessen rund um die Verwaltung von Artikeln mehr Flexibilität und Kontrolle hinzufügen. Sie möchten die Produktbeschreibungen verbessern und weitere Überprüfungsschritte hinzufügen, bevor die Produkte für die Debitoren verfügbar sind.

### Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

Bereiten Sie die Daten vor.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitorenpreisgruppe** ein und wählen Sie den entsprechenden Link.
2. Fügen Sie eine neue Preisgruppe hinzu. Geben Sie in das Feld **Code** `SHOPIFY` ein.
3. Schließen Sie das Fenster **Kundenpreisgruppe**.
4. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Artikel** ein und wählen Sie den entsprechenden Link aus.

Wählen Sie Artikel **1896-S, Athens Desk** aus und gehen Sie wie folgt vor:

1. Wählen Sie die Aktion **Varianten** aus und fügen Sie dann zwei Varianten hinzu: `PREMIUM, Athens Desk, Premium edition` und `ESSENTIAL, Athens Desk, Essential edition`.
2. Wählen Sie die Aktion **Erweiterter Text** und erstellen Sie dann einen neuen erweiterten Text, der für alle Sprachcodes gilt. Geben Sie in das Feld **Beschreibung** `Shopify` ein. 
3. Fügen Sie den folgenden Text mit HTML-Tags hinzu: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`. Schließen Sie die Seite **Erweiterter Text** und kehren Sie zur Artikelkarte zurück.
4. Wählen Sie die Aktion **Verkaufspreise** und fügen Sie neue Preise hinzu, wie in der folgenden Tabelle gezeigt:

   |Auftrag|Verkaufsart|Verkaufscode|Typ|Code|Variantencode<br>(fügen Sie das Feld über die Personalisierung hinzu)|VK-Preis|
   |------|------------|------------|------------|------------|------------|------------|
   |0|Debitorenpreisgruppe|SHOPIFY|Option|1896-S|ESSENTIAL|700|
   |2|Debitorenpreisgruppe|SHOPIFY|Option|1896-S|PREMIUM|1000|

5. Wählen Sie die Aktion **Verkaufsrabatte** und fügen Sie einen neuen Rabatt hinzu:

   * **Verkaufstyp** *Kundenrab. Gruppe*
   * **Verkaufscode** *RETAIL*
   * **Typ** *Artikel*
   * **Code** *1896-S*
   * **Code der Maßeinheit** *STK*
   * **Zeilenrabatt %** *10*

6. Wählen Sie die Aktion **Artikelreferenzen** und fügen Sie die folgenden Zeilen hinzu:

   |Auftrag|Referenzart|Referenz Nr.|Variantencode|
   |------|------------|------------|------------|
   |0|Strichcode|77777777|ESSENTIAL|
   |2|Strichcode|11111111|PREMIUM|


Wählen Sie den Artikel **1920-S, ANTWERP Conference Table** aus und gehen Sie wie folgt vor:

1. Wählen Sie **Bestand anpassen** und geben Sie im Feld **Neuer Bestand** `100` für die Standorte *OST* und *WEST* ein. 
2. Wählen Sie **OK** aus.

Passen Sie die Synchronisationseinstellungen an.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den *DEMO1*-Shop, für den Sie Artikel synchronisieren möchten, um die Seite **Shopify Shopkarte** zu öffnen.
3. Wählen Sie *SHOPIFY* im Feld **Kundenpreisgruppe**.
4. Wählen Sie *RETAIL* im Feld **Kundenrabattgruppe**.
5. Aktivieren Sie das Feld **Erweiterter Text des Elements synchronisieren**.
6. Wählen Sie *Artikel Nr.+ Variantencode* im Feld **SKU Zuordnung**.
7. Wählen Sie *Entwurf* im Feld **Status für erstellte Produkte**.
8. Wählen Sie *Status auf Archiviert* im Feld **Aktion für entferntes Produkt**.

Führen Sie die Synchronisierung aus.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den *DEMO1*-Shop, für den Sie Artikel synchronisieren möchten, um die Seite **Shopify Shopkarte** zu öffnen.
3. Wählen Sie **Produkte**, um das Fenster **Shopify Produkte** zu öffnen.
4. Wählen Sie die Aktion **Artikel hinzufügen**.
5. Legen Sie den Filter *TABLE|DESK* im Feld **Artikelkategoriencode** fest.
6. Wählen Sie **Produktbilder synchronisieren** aus.
7. Wählen Sie **Lagerbestand synchronisieren** aus.

Die Produkte werden hinzugefügt. Beachten Sie, dass der Status auf *Entwurf* festgelegt ist, so dass die Elemente im Online Store Shopify nicht sichtbar sind.

1. Wählen Sie die Zeile mit dem Element *1920-S, ANTWERP Konferenztisch*. Geben Sie im **SEO Titel** `Rectangular meeting table Antwerp, 10 seats, black` ein.
2. Wählen Sie *Aktiv* im Feld **Status**.
3. Markieren Sie die Zeile mit dem Artikel *1906-S, ATHENS, Mobile Pedestal* und wählen Sie dann **Löschen** aus.

Beachten Sie, dass in **Shopify-Verwaltung** alle Produkte unterschiedliche Status haben.

* *ANTWERP Conference Table* ist *Aktiv*, weil wir seinen Status im Fenster **Shopify Produkt** geändert haben.
* *ATHENS Schreibtisch* ist *Entwurf*, weil wir den Standardstatus für alle hinzugefügten Produkte auf *Entwurf* gesetzt haben.
* *ATHENS Mobile Pedestal* ist *Archiviert*, weil wir den Shop so konfiguriert haben, dass er gelöschten Produkten automatisch den Status *Archiviert* zuweist.

Beachten Sie, dass der Bestand für ANTWERP Conference Table 100 beträgt, da wir das System so konfiguriert haben, dass es nur den Bestand von zwei Standorten (HAUPT und OST) verwendet. Der Bestand am anderen Standort (WEST) wird ignoriert.

* Öffnen Sie *ANTWERP Conference Table* und achten Sie auf die Felder **Benutzerdefinierter Typ**, **Kreditor**, **Gewicht** und **Kosten pro Artikel** und den Abschnitt **Suchmaschinenauflistung Vorschau**.
* Öffnen Sie *Athens Desk*, scrollen Sie nach unten zum Abschnitt **Varianten** und beachten Sie, wie **SKU** ausgefüllt ist.
* Wählen Sie **Bearbeiten**, um Barcode und Preise zu überprüfen.
* Ändern Sie den Status von *Athens Desk* auf *Aktiv* und wählen Sie **Vorschau**.

Öffnen Sie im **Shopify Onlineshop** den Produktkatalog und suchen Sie das Produkt *ATHENS Desk*. Beachten Sie, dass verschiedene Optionen verfügbar sind. Für die verschiedenen Optionen gelten auch unterschiedliche Preise. Achten Sie auf die Rabattinformationen.

## Exemplarische Vorgehensweise: Elemente aus Shopify importieren

### Szenario 

Sie haben bereits einen erfolgreichen Online-Store und möchten [!INCLUDE[prod_short](../includes/prod_short.md)] als Software für die Unternehmensverwaltung einsetzen. Sie möchten so viele Daten wie möglich aus Shopify importieren. 

### Schritte

Dies ist eine Fortsetzung von [Beispielhafte Vorgehensweise: Mit dem Online-Verkauf von Produkten beginnen](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Sie können es auch mit Ihren eigenen Daten versuchen, zum Beispiel mit Ihrem Shopify Shop oder Ihrer Sandbox.

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor.

#### Daten vorbereiten

1. Wechseln Sie zu einem kostenlosen 30-tägigen Test ohne Beispieldaten. Weitere Informationen finden Sie unter [Eigene Daten zu einem leeren Test hinzufügen](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den dazugehörigen Link.
3. Wählen Sie **Neu** aus.
4. Geben Sie in das Feld **Code** `DEMO2` ein.
5. Geben Sie in das Feld **Shopify URL** die URL des Online-Shops ein, mit dem Sie sich verbinden möchten.
6. Aktivieren Sie den Schalter **Aktiviert** und lesen und akzeptieren Sie dann die Bestimmungen.

Konfigurieren Sie den Shopify-Shop wie hier beschrieben:

1. Deaktivieren Sie das Kippschalter **Hintergrundsynchronisationen zulassen**.
1. Wählen Sie *Aus Shopify* im Feld **Sync Element**.
1. Aktivieren Sie das Umschaltkästchen **Unbekannte Elemente automatisch erstellen**.
1. Füllen Sie das Feld **Element Vorlagencode** mit der entsprechenden Vorlage aus.
1. Wählen Sie *Aus Shopify* im Feld **Artikelbilder synchronisieren**.
1. Wählen Sie *Alle Debitoren* und **Debitorenimport aus Shopify**.
1. Aktivieren Sie die Umschaltfunktion **Unbekannte Kunden automatisch erstellen**.

#### Führen Sie die Synchronisierung aus

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den *DEMO2*-Shop, für den Sie Daten synchronisieren möchten, um die Seite **Shopify Shopkarte** zu öffnen.
3. Wählen Sie **Produkte synchronisieren**.
4. Wählen Sie **Produktbilder synchronisieren** aus.
5. Wählen Sie **Debitoren synchronisieren**.

### Ergebnisse

* Shopify Produkte werden importiert. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol aus, geben Sie **Shopify Produkte** ein und wählen Sie den entsprechenden Link.
* Es werden Elemente mit Bildern erstellt. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Artikel** ein und wählen Sie den entsprechenden Link aus.
* Shopify Kunden werden importiert. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Debitoren** ein und wählen Sie den entsprechenden Link aus.
* Die Kunden werden erstellt. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitoren** ein und wählen Sie den entsprechenden Link aus.


## Siehe auch

[Erste Schritte mit dem Shopify-Konnektor](get-started.md)  
