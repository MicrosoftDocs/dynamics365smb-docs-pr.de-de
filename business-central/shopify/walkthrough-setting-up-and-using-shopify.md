---
title: Festlegen und Verwenden des Shopify Konnektors
description: Verschiedene Integrationsszenarien zur Demonstration des Workflows zwischen Shopify und Business Central
ms.date: 08/01/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: bholtorf
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
8. Füllen Sie das Feld **Debitoren-/Unternehmensvorlagencode** mit der entsprechenden Vorlage aus.
9. Füllen Sie das Feld **Versandkostenkonto**, das Feld **Tippkonto** mit dem Umsatzkonto aus. In den USA verwenden Sie zum Beispiel `40210`.
10. Schalten Sie die Option **Bestellungen automatisch erstellen** ein.
11. Deaktivieren Sie den Umschalter **Verkaufsaufträge automatisch freigeben**.

Konfigurieren Sie die Zuordnung von Standorten:

1. Wählen Sie die Aktion **Standorte** aus, um **Shopify-Shop-Standorte** zu öffnen.
2. Wählen Sie die Aktion **Shopify Standorte abrufen** aus, um alle in Shopify festgelegten Standorte zu importieren. Wählen Sie einen Eintrag aus, bei dem der Umschalter **Ist primär** ausgewählt ist.
3. Geben Sie im **Ortsfilter** `''|EAST|MAIN` ein.
4. Wählen Sie *Geplanter verfügbarer Saldo heute* im Feld **Lagerbestandsberechnung** aus, um eine Lagerbestandssynchronisierung für einen ausgewählten Shopify-Standort zu aktivieren.

## Exemplarische Vorgehensweise: Mit dem Online-Verkauf von Produkten beginnen

### Szenario

Nehmen wir an, Sie möchten Shopify als Onlineshop ausprobieren, ohne viel Zeit mit der Einrichtung zu verbringen, vor allem, weil Sie Ihre Artikel in [!INCLUDE[prod_short](../includes/prod_short.md)] bereits gut pflegen. Nachdem Sie Ihren Shopify-Online-Store eröffnet haben, erhalten Sie sofort neue Kunden, die mit Ihrem Shop und ihrem Einkaufserlebnis zufrieden sind. Also beschließen sie, an der Kasse Tipps zu hinterlassen.

### Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol aus, geben Sie **Shopify Produkte** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie **Artikel hinzufügen**.
3. Geben Sie in das Feld **Shop-Code** `DEMO1` ein.
4. Legen Sie den Filter `CHAIR` auf dem Feld **Artikelkategoriencode** fest.
5. Schalten Sie den Umschalter **Produktbilder synchronisieren** ein.
6. Schalten Sie den Umschalter **Bestand synchronisieren** ein.
7. Auswählen **OK** und warten Sie, bis die erste Synchronisierung von Artikeln, Preisen, Bildern und Lagerbeständen abgeschlossen ist.

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
6. Behalten Sie *Standard* als Versandmethode bei.
8. Geben Sie im Feld **Kreditkartennummer** eine `1` ein, wenn Sie *(zu Testzwecken) Bogus Gateway* verwenden, oder geben Sie `5555 5555 5555 4444` ein, wenn Sie *Shopify Payments* im Testmodus verwenden.
9. Füllen Sie das Feld **Name auf der Karte** aus.
10. Geben Sie in das Feld **Ablaufdatum** den aktuellen Monat/Jahr ein.
11. In das Feld **Sicherheitscode** geben Sie `111` ein.
7. Optional: Wählen Sie `10%` Trinkgeld.
8. 12. Wählen Sie **Jetzt bezahlen**.

Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die nächsten Schritte aus:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Shopify-Aufträge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
3. Wählen Sie **OK** aus.

Die importierte Bestellung ist bereit zur Verarbeitung.

1. Wählen Sie den importierten Auftrag, um das Fenster **Shopify Aufträge** zu öffnen.
2. Beachten Sie, dass die neue Kundschaft und die neuen Verkaufsaufträge erstellt wurden.
3. Informieren Sie sich über die  **Risiken**  und  **Versandkosten** .
4. Wählen Sie **Verkaufsauftrag** aus, um das Fenster **Verkaufsauftrag** zu öffnen. Ein Verkaufsauftrag ist ein Bedarf, der, falls erforderlich durch Montage, Produktion oder Kauf mit Hilfe des Planungsmoduls gedeckt werden kann. Es unterstützt auch verschiedene Lagerort-Verarbeitungsprozesse mit vollständiger Aufgabentrennung.
6. Geben Sie in das Feld **Bearbeiter** `DHL` ein. Öffnen Sie den Auftrag bei Bedarf erneut, indem Sie die Aktion **Erneut öffnen** auswählen.
7. Geben Sie in das Feld **Paketverfolgungsnummer** `123456789` ein.
8. Wählen Sie **Buchen**, behalten Sie die Option **Versand und Rechnung** bei und wählen Sie dann **OK** aus.

Jetzt sind die physischen und finanziellen Daten in [!INCLUDE[prod_short](../includes/prod_short.md)] registriert. Jetzt ist es an der Zeit, Shopify über die Änderungen zu informieren.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol aus. Geben Sie **Lieferungen mit Shopify synchronisieren** ein und wählen Sie dann den dazugehörigen Link aus.
2. Wählen Sie **OK** aus.

Beachten Sie, dass in der **Shopify-Verwaltung** die Bestellung jetzt als *Erfüllt* gekennzeichnet ist. Sie können auch die Details der Sendung einsehen und die URL der Sendungsverfolgung sehen. Wenn Sie **Bestellungen von Shopify synchronisieren** erneut ausführen, wird die Bestellung in beiden Systemen archiviert.

## Exemplarische Vorgehensweise: Debitoren Ihrem neuen Onlineshop hinzufügen

### Szenario

Nach einem erfolgreichen Schnellstart Ihres neuen Online Stores möchten Sie, dass Ihre derzeitigen Kunden ihn besuchen und Bestellungen aufgeben. Je nach Ihrem Shopify-Plan und -Prozess können Sie B2B- und DTC-Flows ausprobieren.

### DTC-Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Debitoren** ein und wählen Sie den entsprechenden Link aus.
2. Wählen Sie **Debitoren hinzufügen** aus.
3. Geben Sie in das Feld **Shop-Code** `DEMO1` ein.
4. Legen Sie den Filter `20000` auf das Feld **Nr.** fest.
5. Wählen Sie **OK** und warten Sie, bis die anfängliche Synchronisierung von Debitoren abgeschlossen ist.

Beachten Sie, dass der Debitor in die **Shopify-Verwaltung** importiert wurden. Öffnen Sie den Debitor und stellen Sie fest, dass der Vor- und Nachname des Debitoren aus dem Feld **Kontaktname** der **Kundenkarte** stammt. Der Name der Firma ist in der Standardadresse zu finden, die mit dem Kunden verknüpft ist. Wenn Sie *klassische Debitorenkonten* verwenden, können Sie **Kontoeinladung senden** auswählen, um den Debitor einzuladen. Bei  *Neukundenkonten* ist für die Anmeldung der Kunden kein Kennwort erforderlich. Stattdessen Shopify ermöglicht die Anmeldung Ihrer Kunden mit einem einmaligen 6-stelligen Bestätigungscode, der per E-Mail gesendet wird. 

### B2B-Schritte

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Unternehmen** ein und wählen Sie den entsprechenden Link aus.
2. Wählen Sie **Unternehmen hinzufügen** aus.
3. Geben Sie im Feld Shop- **Code**  `DEMO1` ein.
4. Legen Sie den Filter `30000` auf das Feld **Nr.** fest.
5. Wählen Sie **OK** und warten Sie, bis die anfängliche Synchronisierung von Debitoren abgeschlossen ist.

Beachten Sie in  **Shopify Admin**, dass sowohl das Unternehmen als auch der Kunde importiert wurden. Öffnen Sie die Debitoren und sehen Sie sich die Infobox „Unternehmen“ mit einem Link zum Unternehmen, dem Standort und den zugewiesenen Berechtigungen an. Auswählen **[...]** in der  ** Unternehmensinfobox, dann Auswählen **B2B-Zugangs-E-Mail senden**, um den Kunden einzuladen.

## Exemplarische Vorgehensweise: Feinabstimmung der Artikelverwaltung

### Szenario 

Sie möchten Ihren Prozessen rund um die Verwaltung von Artikeln mehr Flexibilität und Kontrolle hinzufügen. Sie möchten die Produktbeschreibungen verbessern und weitere Überprüfungsschritte hinzufügen, bevor die Produkte für alle Debitoren verfügbar sind.

### Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

Bereiten Sie die Daten vor.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitorenpreisgruppe** ein und wählen Sie den entsprechenden Link.
2. Fügen Sie eine neue Preisgruppe hinzu. Geben Sie in das Feld **Code** `SHOPIFY` ein.
3. Schließen Sie das Fenster **Kundenpreisgruppe**.
4. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Artikel** ein und wählen Sie den entsprechenden Link aus.
5. Wählen Sie Artikel *1896-S, Athens Desk* aus und gehen Sie wie folgt vor:

6. Wählen Sie die Aktion **Varianten** aus und fügen Sie dann zwei Varianten hinzu: `PREMIUM, Athens Desk, Premium edition` und `ESSENTIAL, Athens Desk, Essential edition`.
7. Wählen Sie die Aktion **Marketingtext** und verwenden Sie **Entwurf mit Copilot**, um einen kreativen und ansprechenden Text zu erhalten. Wenn die Funktion für Marketingtextvorschläge nicht aktiviert ist, geben Sie einfach ein: ‚**Einfaches, stilvolles Design** passt zu jedem Ensemble. *Erhältlich in zwei Ausführungen.*“ 
8. Wählen Sie die Aktion **Verkaufspreise** und fügen Sie neue Preise hinzu, wie in der folgenden Tabelle gezeigt:

   |Auftrag|Verkaufsart|Verkaufscode|Typ|Code|Variantencode<br>(fügen Sie das Feld über die Personalisierung hinzu)|VK-Preis|
   |------|------------|------------|------------|----------------|------------|------------|
   |0|Debitorenpreisgruppe|SHOPIFY|Option|1896-S|ESSENTIAL|700|
   |2|Debitorenpreisgruppe|SHOPIFY|Option|1896-S|PREMIUM|1000|

9. Wählen Sie die Aktion **Verkaufsrabatte** und fügen Sie einen neuen Rabatt hinzu:

   * **Verkaufstyp** *Kundenrab. Gruppe*
   * **Verkaufscode** *RETAIL*
   * **Typ** *Artikel*
   * **Code** *1896-S*
   * **Code der Maßeinheit** *STK*
   * **Zeilenrabatt %** *10*

10. Wählen Sie die Aktion **Artikelreferenzen** und fügen Sie die folgenden Zeilen hinzu:

   |Auftrag|Referenzart|Referenz Nr.|Variantencode|
   |------|------------|------------|------------|
   |0|Strichcode|77777777|ESSENTIAL|
   |2|Strichcode|11111111|PREMIUM|

11. Wählen Sie den Artikel *1920-S, ANTWERP Conference Table* aus und gehen Sie wie folgt vor:
12. Wählen Sie **Bestand anpassen** und geben Sie im Feld **Neuer Bestand** `100` für die Standorte *OST* und *WEST* ein. 
13. Wählen Sie **OK** aus.

Passen Sie die Synchronisationseinstellungen an.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den `DEMO1`-Shop aus, für den Sie Artikel synchronisieren möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Aktivieren Sie das Feld **Marketingtext synchronisieren**.
4. Wählen Sie *Artikel Nr.+ Variantencode* im Feld **SKU Zuordnung**.
5. Wählen Sie *Weiter* im Feld **Standardrichtlinie für den Bestand**.
6. Wählen Sie *Entwurf* im Feld **Status für erstellte Produkte**.
7. Wählen Sie *Status auf Archiviert* im Feld **Aktion für entferntes Produkt**.
8. Wählen Sie *SHOPIFY* im Feld **Kundenpreisgruppe**.
9. Wählen Sie *RETAIL* im Feld **Kundenrabattgruppe**.
 
Führen Sie die Synchronisierung aus.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den `DEMO1`-Shop aus, für den Sie Artikel synchronisieren möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie **Produkte**, um das Fenster **Shopify Produkte** zu öffnen.
4. Wählen Sie die Aktion **Artikel hinzufügen**.
5. Legen Sie den Filter *TABLE|DESK* im Feld **Artikelkategoriencode** fest.
6. Schalten Sie den Umschalter **Produktbilder synchronisieren** ein.
7. Schalten Sie den Umschalter **Bestand synchronisieren** ein.
8. Auswählen **OK** und warten Sie, bis die erste Synchronisierung von Artikeln, Preisen, Bildern und Lagerbeständen abgeschlossen ist.

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

### Zusätzliche Schritte für B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Sie können den Konnektor so konfigurieren, dass automatisch Kataloge für exportierte Unternehmen erstellt und zugewiesen werden. Die folgenden Schritte sind hilfreich, wenn Sie eine genauere Kontrolle darüber wünschen, was für B2B-Debitoren verfügbar ist.

Erstellen Sie in der **Shopify-Verwaltung** einen Katalog und weisen Sie ihn zu.

1. Wählen Sie **Produkte** und dann **Kataloge** in der Seitenleiste der **Shopify-Verwaltung** aus.
2. Erstellen Sie einen Katalog für bestimmte Produkte. Geben Sie als Titel „B2B“ ein. 
3. Wählen Sie **Verwalten** und dann **Produkte und Preise verwalten**.
4. Wählen Sie den Filter *Ausgeschlossen* , suchen Sie nach *ATHERN Desk* und wählen Sie **In Katalog aufnehmen**.
5. Wählen Sie **Debitoren** und dann **Unternehmen** in der Seitenleiste der **Shopify-Verwaltung** aus.
6. Wählen Sie *School of Fine Art*, **[...]** und dann **Kataloge hinzufügen** aus und fügen Sie einen zuvor erstellten *B2B*-Katalog hinzu.

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

Bereiten Sie die Daten vor.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Artikel** ein und wählen Sie den entsprechenden Link aus.

2. Wählen Sie Artikel **1896-S, Athens Desk** aus und gehen Sie wie folgt vor:

3. Wählen Sie die Aktion **Verkaufsrabatte** und fügen Sie einen neuen Rabatt hinzu:

   * **Verkaufstyp** *Kundenrab. Gruppe*
   * **Verkaufscode** *LARGE ACC*
   * **Typ** *Artikel*
   * **Code** *1896-S*
   * **Code der Maßeinheit** *STK*
   * **Zeilenrabatt %** *25*

4. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Kataloge** ein und wählen Sie den entsprechenden Link aus.
5. Wählen Sie **Kataloge abrufen** aus.
6. Geben Sie in das Feld **Shop-Code** `DEMO1` ein.
7. Wählen Sie den Eintrag mit dem Namen „*B2B*-Katalog“ aus, für den Sie die Preise synchronisieren möchten.
8. Aktivieren Sie den Umschalter **Preise synchronisieren**.
9. Wählen Sie *SHOPIFY* im Feld **Debitorenpreisgruppe**.
10. Wählen Sie *LARGE ACC* im Feld **Debitorenrabattgruppe**.
11. Wählen Sie **Preis synchronisieren** und warten Sie, bis die Synchronisierung von Preisen abgeschlossen ist.

Erkunden Sie in der **Shopify-Verwaltung** die Preise für den *B2B*-Katalog aus.

Öffnen Sie im **Shopify Onlineshop** den Produktkatalog und suchen Sie das Produkt *ATHENS Desk*. Bei Hinweispreisen handelt es sich um Rabattangaben.

## Exemplarische Vorgehensweise: Zur Kasse gehen und Auftragssynchronisierung für einzelne Kaufende und Unternehmensvertreter
Dies ist eine Fortsetzung von [Beispielhafte Vorgehensweise: Mit dem Online-Verkauf von Produkten beginnen](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Sie können es auch mit Ihren eigenen Daten versuchen, zum Beispiel mit Ihrem Shopify Shop oder Ihrer Sandbox.

Einzelner Kaufender

1. Tun Sie im **Shopify-Onlineshop** Folgendes. Wählen Sie das Symbol **Konto** aus. Geben Sie eine E-Mail-Adresse ein, auf die Sie Zugriff haben.
2. Melden Sie sich mit einem einmaligen 6-stelligen Bestätigungscode an, der Ihnen per E-Mail zugesandt wurde.
3. Durchsuchen Sie den Produktkatalog. Sie sollten alle Produkte mit Einzelhandelspreisen sehen können.
4. Wählen Sie die Variante „Essential“ und dann **Jetzt kaufen** und gehen Sie zur Kasse.
5. Füllen Sie die Felder **Vorname** und **Nachname** aus.
6. Geben Sie die lokale Adresse ein.
7. Behalten Sie *Standard* als Versandmethode bei.
8. Geben Sie im Feld **Kreditkartennummer** eine `1` ein, wenn Sie *(zu Testzwecken) Bogus Gateway* verwenden, oder geben Sie `5555 5555 5555 4444` ein, wenn Sie *Shopify Payments* im Testmodus verwenden.
9. Geben Sie in das Feld **Ablaufdatum** den aktuellen Monat/Jahr ein.
10. In das Feld **Sicherheitscode** geben Sie `111` ein.
11. Füllen Sie das Feld **Name auf der Karte** aus.
12. Wählen Sie **Jetzt bezahlen**.
 
Unternehmensvertreter

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. Gehen Sie in der **Shopify-Verwaltung** wie folgt vor.
2. Wählen Sie **Debitoren** und dann **Unternehmen** in der Seitenleiste der **Shopify-Verwaltung** aus.
3. Öffnen Sie den Eintrag *School of Fine Arts*.
4. Wählen Sie in der Infobox  **School of Fine Art**  **[...]**  und anschließend  **Zahlungsbedingungen bearbeiten**  und Auswählen *Fällig am Auftragserfüllung*.
5. Wählen Sie  **[...]**  im Infofeld  **Kunden**  und dann  **Kunden hinzufügen**  und fügen Sie einen Kunden mit der E-Mail-Adresse hinzu, die Sie zuvor für die Anmeldung im Geschäft verwendet haben.
6. Tun Sie im **Shopify-Onlineshop** Folgendes. Wählen Sie das Symbol **Konto** aus. Geben Sie eine E-Mail-Adresse ein, auf die Sie Zugriff haben.
7. Melden Sie sich mit einem einmaligen 6-stelligen Bestätigungscode an, der Ihnen per E-Mail zugesandt wurde.
8. Durchsuchen Sie den Produktkatalog. Sie sollten nur die dem *B2B*-Katalog hinzugefügten Produkte mit Einzelhandelssonderpreisen sehen.
9. Wählen Sie die Variante „Essential“ und dann **Jetzt kaufen** und gehen Sie zur Kasse.
10. Beachten Sie, dass „Konto“, „Lief. an“ und „Zahlungsmethode“ ausgefüllt sind.
11. Füllen Sie das Feld  **Bestellnummer**  mit  `PO-12345` aus.
12. Wählen Sie **Auftrag absenden**.
 
Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die nächsten Schritte aus:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Aufträge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
3. Wählen Sie **OK** aus.

Die importierte Bestellung ist bereit zur Verarbeitung.

1. Wählen Sie den importierten Auftrag, um das Fenster **Shopify Aufträge** zu öffnen.
2. Beachten Sie, dass beide Bestellungen von derselben Person aufgegeben wurden und mit zwei verschiedenen Kunden verknüpft sind. 
3. In dem im Namen des Unternehmens eingereichten Auftrag sehen Sie den Wert im Feld **Auftragsnummer**, der auch an das Feld **Externe Belegnr.** des erstellten Verkaufsbelegs übertragen wird.
4. Weil wir das B2B-Unternehmen so konfiguriert haben, dass es Zahlungen außerhalb von Shopify handhabt, ist **Finanzstatus** auf *Ausstehend* gesetzt. Sobald Sie die Zahlung erhalten haben, Auswählen die Aktion  **Als bezahlt markieren** . Der Finanzstatus wird auf Shopify aktualisiert. 

## Exemplarische Vorgehensweise: Artikel, Debitoren, Unternehmen aus Shopify importieren

### Szenario 

Sie haben bereits einen erfolgreichen Online-Store und möchten [!INCLUDE[prod_short](../includes/prod_short.md)] als Software für die Unternehmensverwaltung einsetzen. Sie möchten so viele Daten wie möglich aus Shopify importieren. 

### Schritte

Dies ist eine Fortsetzung von [Exemplarische Vorgehensweise: Mit dem Onlineverkauf von Produkten beginnen](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) und [Exemplarische Vorgehensweise: Debitoren Ihrem neuen Onlineshop hinzufügen](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). Sie können es auch mit Ihren eigenen Daten versuchen, zum Beispiel mit Ihrem Shopify-Shop oder Ihrer Sandbox.

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
2. Wählen Sie *Aus Shopify* im Feld **Sync Element**.
3. Aktivieren Sie das Umschaltkästchen **Unbekannte Elemente automatisch erstellen**.
4. Füllen Sie das Feld **Element Vorlagencode** mit der entsprechenden Vorlage aus.
5. Wählen Sie *Aus Shopify* im Feld **Artikelbilder synchronisieren**.
6. Wählen Sie *Artikelnr. und Variantencode* im Feld **SKU-Zuordnung**.
7. Wählen Sie *Alle Debitoren* und **Debitorenimport aus Shopify**.
8. Aktivieren Sie die Umschaltfunktion **Unbekannte Kunden automatisch erstellen**.
9. Füllen Sie das Feld **Debitoren-/Unternehmensvorlagencode** mit der entsprechenden Vorlage aus.
10. Wählen Sie *Alle Debitoren* und **Unternehmensimport aus Shopify**.
11. Aktivieren Sie den Umschalter **Unbekanntes Unternehmen automatisch erstellen**.

#### Führen Sie die Synchronisierung aus

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den *DEMO2*-Shop, für den Sie Daten synchronisieren möchten, um die Seite **Shopify Shopkarte** zu öffnen.
3. Wählen Sie **Produkte synchronisieren**.
4. Wählen Sie **Produktbilder synchronisieren** aus.
5. Wählen Sie **Debitoren synchronisieren**.
6. Wählen Sie **Unternehmen synchronisieren**

### Ergebnisse

* Shopify Produkte werden importiert. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol aus, geben Sie **Shopify Produkte** ein und wählen Sie den entsprechenden Link.
* Es werden Elemente mit Bildern erstellt. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Artikel** ein und wählen Sie den entsprechenden Link aus.
* Shopify Kunden werden importiert. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Debitoren** ein und wählen Sie den entsprechenden Link aus.
* Shopify-Unternehmen werden importiert. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Unternehmen** ein und wählen Sie den entsprechenden Link aus.
* Die Kunden werden erstellt. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitoren** ein und wählen Sie den entsprechenden Link aus.


## Siehe auch

[Erste Schritte mit dem Shopify-Konnektor](get-started.md)  
