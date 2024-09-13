---
title: Festlegen und Verwenden des Shopify Konnektors
description: Verschiedene Integrationsszenarien zur Demonstration des Workflows zwischen Shopify und Business Central
ms.date: 08/30/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Exemplarische Vorgehensweise: Festlegen und Verwenden des Shopify Konnektors

Dieser Abschnitt demonstriert einige typische Szenarien und führt Sie durch die Schritte, mit denen Sie den Workflow des integrierten [!INCLUDE[prod_short](../includes/prod_short.md)] und des Shopify Stores testen oder Benutzer schulen können.

## <a name="prerequisites"></a>Voraussetzungen

### <a name="shopify"></a>Shopify

Sie benötigen Folgendes:

- Ein Shopify-Konto
- Ein Shopify-Online-Store

Erfahren Sie mehr darüber, wie Sie Shopify-Tests erstellen, und über die empfohlenen Einstellungen unter [Ein Shopify-Konto erstellen und einrichten](shopify-account.md).

### <a name="business-central"></a>Business Central

Sie müssen ein [!INCLUDE[prod_short](../includes/prod_short.md)]-Konto haben.

Sie können zum Beispiel ein Demokonto erstellen oder eine Testversion starten. Weitere Informationen finden Sie unter [Demonstrationsumgebung vorbereiten für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) und [Anmelden für den Test](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a>Verbinden Sie Business Central mit dem Shopify-Laden

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den dazugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Geben Sie in das Feld **Code** **DEMO1** ein.
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
9. Füllen Sie das Feld **Versandkostenkonto**, das Feld **Tippkonto** mit dem Umsatzkonto aus. Verwenden Sie in den USA beispielsweise  **40210**.
10. Schalten Sie die Option **Bestellungen automatisch erstellen** ein.
11. Deaktivieren Sie den Umschalter **Verkaufsaufträge automatisch freigeben**.

Konfigurieren Sie die Zuordnung von Standorten:

1. Wählen Sie die Aktion **Standorte** aus, um **Shopify-Shop-Standorte** zu öffnen.
2. Wählen Sie die Aktion **Shopify Standorte abrufen** aus, um alle in Shopify festgelegten Standorte zu importieren. Wählen Sie einen Eintrag aus, bei dem der Umschalter **Ist primär** ausgewählt ist.
3. Geben Sie im  **Standortfilter** „|EAST|MAIN“ ein **.**
4. Um eine Bestandssynchronisierung für einen ausgewählten Shopify Standort zu aktivieren, geben Sie im Feld **Bestandsberechnung**  Auswählen **Voraussichtlicher verfügbarer Bestand heute** ein.

## <a name="walkthrough-start-selling-products-online"></a>Exemplarische Vorgehensweise: Mit dem Online-Verkauf von Produkten beginnen

### <a name="scenario"></a>Szenario

Nehmen wir an, Sie möchten Shopify als Onlineshop ausprobieren, ohne viel Zeit mit der Einrichtung zu verbringen, vor allem, weil Sie Ihre Artikel in [!INCLUDE[prod_short](../includes/prod_short.md)] bereits gut pflegen. Nachdem Sie Ihren Shopify-Online-Store eröffnet haben, erhalten Sie sofort neue Kunden, die mit Ihrem Shop und ihrem Einkaufserlebnis zufrieden sind. Also beschließen sie, an der Kasse Tipps zu hinterlassen.

### <a name="steps"></a>Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol aus, geben Sie **Shopify Produkte** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie **Artikel hinzufügen**.
3. Geben Sie im Feld  **Shop-Code**  **DEMO1** ein.
4. Legen Sie im Feld  **Artikelkategoriecode**  den Filter  **STUHL** fest.
5. Schalten Sie den Umschalter **Produktbilder synchronisieren** ein.
6. Schalten Sie den Umschalter **Bestand synchronisieren** ein.
7. Auswählen **OK** und warten Sie, bis die erste Synchronisierung von Artikeln, Preisen, Bildern und Lagerbeständen abgeschlossen ist.

Tun Sie im **Shopify-Onlineshop** Folgendes:
> [!Tip]  
> Öffnen Sie **Shopify Verwaltung**, indem Sie die URL aufrufen, die im Feld **URL** auf der Seite **Shopify Shop-Karte** angegeben ist. Wählen Sie anschließend das Augensymbol neben dem Verkaufskanal **Onlineshop** aus, der sich in der Seitenleiste der **Shopify-Verwaltung** befindet. 

Öffnen Sie den Produktkatalog. Beachten Sie:

* Produkttitel, Bilder und Preise.
* Verfügbarkeitsanzeige (ausverkauft für Produkte, die nicht auf Lager sind).

Wählen Sie ein beliebiges Produkt aus, das verkauft werden kann. Zum Beispiel der  **Drehstuhl BERLIN, gelb**. Beachten Sie, dass die Beschreibung Artikelattribute enthält.

Wählen Sie **Jetzt kaufen** aus und gehen Sie zur Kasse.

1. Geben Sie im Feld  **E-Mail-Adresse oder Mobiltelefonnummer**  Folgendes ein:  **cl@contoso.com**  (oder eine E-Mail-Adresse, an die Sie Bestell- und Versandbestätigungen erhalten möchten).
2. Geben Sie in den Feldern  **Vorname**  und  **Nachname**  **Claudia**  und  **Lawson** ein.
3. Geben Sie die lokale Adresse ein.
4. Wählen Sie das Kontrollkästchen **Diese Informationen für das nächste Mal speichern** aus.
6. Behalten Sie *Standard* als Versandmethode bei.
8. Geben Sie im Feld  **Kredit-Karte-Nummer**  **1**  ein, wenn Sie  **(zum Testen) Bogus Gateway** verwenden, oder geben Sie  **5555 5555 5555 4444**  ein, wenn Sie  **Shopify Zahlungen**  im Testmodus verwenden.
9. Füllen Sie das Feld **Name auf der Karte** aus.
10. Geben Sie in das Feld **Ablaufdatum** den aktuellen Monat/Jahr ein.
11. Geben Sie im Feld  **Sicherheitscode** die Zahl  **111** ein.
12. Optional: Auswählen **10 %** Trinkgeld.
13. Wählen Sie **Jetzt bezahlen**.

Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die nächsten Schritte aus:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Shopify-Aufträge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
3. Wählen Sie **OK** aus.

Die importierte Bestellung ist bereit zur Verarbeitung.

1. Wählen Sie den importierten Auftrag, um das Fenster **Shopify Aufträge** zu öffnen.
2. Beachten Sie, dass die neue Kundschaft und die neuen Verkaufsaufträge erstellt wurden.
3. Informieren Sie sich über die  **Risiken** und  **Versandkosten** Aktionen.
4. Wählen Sie **Verkaufsauftrag** aus, um das Fenster **Verkaufsauftrag** zu öffnen. Ein Verkaufsauftrag ist ein Bedarf, der, falls erforderlich durch Montage, Produktion oder Kauf mit Hilfe des Planungsmoduls gedeckt werden kann. Es unterstützt auch verschiedene Lagerort-Verarbeitungsprozesse mit vollständiger Aufgabentrennung.
6. Geben Sie im Feld  **Agent**  **DHL** ein. Öffnen Sie den Auftrag bei Bedarf erneut, indem Sie die Aktion **Erneut öffnen** auswählen.
7. Geben Sie in das Feld  **Paketverfolgungsnummer** **123456789** ein.
8. Wählen Sie **Buchen**, behalten Sie die Option **Versand und Rechnung** bei und wählen Sie dann **OK** aus.

Jetzt sind die physischen und finanziellen Daten in [!INCLUDE[prod_short](../includes/prod_short.md)] registriert. Jetzt ist es an der Zeit, Shopify über die Änderungen zu informieren.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol aus. Geben Sie **Lieferungen mit Shopify synchronisieren** ein und wählen Sie dann den dazugehörigen Link aus.
2. Wählen Sie **OK** aus.

Beachten Sie, dass in der **Shopify-Verwaltung** die Bestellung jetzt als *Erfüllt* gekennzeichnet ist. Sie können auch die Details der Sendung einsehen und die URL der Sendungsverfolgung sehen. Wenn Sie **Bestellungen von Shopify synchronisieren** erneut ausführen, wird die Bestellung in beiden Systemen archiviert.

## <a name="walkthrough-add-your-customers-to-your-new-online-store"></a>Exemplarische Vorgehensweise: Debitoren Ihrem neuen Onlineshop hinzufügen

### <a name="scenario-1"></a>Szenario

Nach einem erfolgreichen Schnellstart Ihres neuen Online Stores möchten Sie, dass Ihre derzeitigen Kunden ihn besuchen und Bestellungen aufgeben. Je nach Ihrem Shopify-Plan und -Prozess können Sie B2B- und DTC-Flows ausprobieren.

### <a name="dtc-steps"></a>DTC-Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Debitoren** ein und wählen Sie den entsprechenden Link aus.
2. Wählen Sie **Debitoren hinzufügen** aus.
3. Geben Sie im Feld  **Shop-Code**  **DEMO1** ein.
4. Wählen Sie im Feld **Nr.** Legen Sie im Feld den Filter  **20000** fest.
5. Wählen Sie **OK** und warten Sie, bis die anfängliche Synchronisierung von Debitoren abgeschlossen ist.

Beachten Sie, dass der Debitor in die **Shopify-Verwaltung** importiert wurden. Öffnen Sie den Debitor und stellen Sie fest, dass der Vor- und Nachname des Debitoren aus dem Feld **Kontaktname** der **Kundenkarte** stammt. Der Name der Firma ist in der Standardadresse zu finden, die mit dem Kunden verknüpft ist. Wenn Sie  **klassische Kundenkonten** verwenden, können Sie Auswählen **eine Kontoeinladung senden** an den Kunden einladen. Bei  **Neukundenkonten** ist für die Anmeldung der Kunden kein Passwort erforderlich. Stattdessen Shopify können sich Ihre Kunden mit einem einmaligen, 6-stelligen Bestätigungscode anmelden, der per E-Mail gesendet wird. 

### <a name="b2b-steps"></a>B2B-Schritte

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Unternehmen** ein und wählen Sie den entsprechenden Link aus.
2. Wählen Sie **Unternehmen hinzufügen** aus.
3. Geben Sie im Feld Shop- **Code**  **DEMO1** ein.
4. Stellen Sie den Filter **30000** auf der **Nr. ein.** Feld
5. Wählen Sie **OK** und warten Sie, bis die anfängliche Synchronisierung von Debitoren abgeschlossen ist.

Beachten Sie in **Shopify Admin**, dass sowohl das Unternehmen als auch der Kunde importiert wurden. Öffnen Sie die Kunden und beachten Sie, dass die Firmen-Infobox Links zur Firma, zum Standort und den zugewiesenen Berechtigungen enthält.
Um den Kunden einzuladen, Auswählen **[...]** in der **Firma** FactBox und dann Auswählen **B2B-Zugriffs-E-Mail senden**.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Exemplarische Vorgehensweise: Feinabstimmung der Artikelverwaltung

### <a name="scenario-2"></a>Szenario

Sie möchten Ihren Prozessen rund um die Verwaltung von Artikeln mehr Flexibilität und Kontrolle hinzufügen. Sie möchten die Produktbeschreibungen verbessern und weitere Überprüfungsschritte hinzufügen, bevor die Produkte für alle Debitoren verfügbar sind.

### <a name="steps-1"></a>Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

Bereiten Sie die Daten vor.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitorenpreisgruppe** ein und wählen Sie den entsprechenden Link.
2. Fügen Sie eine neue Preisgruppe hinzu. Geben Sie im Feld  **Code**  **SHOPIFY** ein.
3. Schließen Sie das Fenster **Kundenpreisgruppe**.
4. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Artikel** ein und wählen Sie den entsprechenden Link aus.
5. Auswählen item **1896-S, Athens Desk**, und dann folgen diese Schritte:

6. Auswählen die Aktion  **Varianten**  und fügen Sie dann zwei Varianten hinzu:  **PREMIUM, Athens Desk, Premium Edition** und  **ESSENTIAL, Athens Desk, Essential Edition**.
7. Wählen Sie die Aktion **Marketingtext** und verwenden Sie **Entwurf mit Copilot**, um einen kreativen und ansprechenden Text zu erhalten. Wenn die Funktion für Marketingtextvorschläge nicht aktiviert ist, geben Sie einfach Folgendes ein: ‚**Einfaches, stilvolles Design** passt zu jedem Ensemble. *In zwei Editionen verfügbar.*.
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

10. Auswählen die Aktion  **Artikelverweise**  und fügen Sie die folgenden Zeilen hinzu:

   |Auftrag|Referenzart|Referenznr.|Variantencode|
   |------|------------|------------|------------|
   |0|Strichcode|77777777|ESSENTIAL|
   |2|Strichcode|11111111|PREMIUM|

11. Wählen Sie den Artikel **1920-S, ANTWERP Conference Table** aus und gehen Sie wie folgt vor:
12. Auswählen **Anpassen Inventar** und geben Sie im Feld  **Neues Inventar**  **100** für die Standorte  **OST** und  **WEST** ein.
13. Wählen Sie **OK** aus.

Passen Sie die Synchronisationseinstellungen an.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Auswählen der  **DEMO1** Shop, für den Sie Artikel synchronisieren möchten, um die Seite  **Shopify Shop Karte**  zu öffnen.
3. Aktivieren Sie das Feld **Marketingtext synchronisieren**.
4. In der  **SKU Zuordnung** field, Auswählen **Artikelnr. + Variantencode**.
5. Geben Sie im Feld  **Standardinventarrichtlinie**  Auswählen **Weiter** ein.
6. Geben Sie im Feld  **Status für erstellte Produkte**  Auswählen **Entwurf** ein.
7. Setzen Sie im Feld  **Aktion für entferntes Produkt**  den Status von Auswählen auf „Archiviert“ **.**
8. Geben Sie im Feld  **Kundenpreisgruppe**  Auswählen **SHOPIFY** ein.
9. Geben Sie im Feld  **Kundenrabattgruppe**  Auswählen **RETAIL** ein.

Führen Sie die Synchronisierung aus.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Auswählen der  **DEMO1** Shop, für den Sie Artikel synchronisieren möchten, um die Seite  **Shopify Shop Karte**  zu öffnen.
3. Auswählen **Produkte**, um die Seite **Shopify Produkte**  zu öffnen.
4. Wählen Sie die Aktion **Artikel hinzufügen**.
5. Setzen Sie den Filter  **TISCH|SCHREIBTISCH**  auf das Feld  **Artikelkategoriecode** .
6. Schalten Sie den Umschalter **Produktbilder synchronisieren** ein.
7. Schalten Sie den Umschalter **Bestand synchronisieren** ein.
8. Auswählen **OK** und warten Sie, bis die erste Synchronisierung von Artikeln, Preisen, Bildern und Lagerbeständen abgeschlossen ist.

Die Produkte werden hinzugefügt. Beachten Sie, dass der Status auf  **Entwurf** gesetzt ist und daher Artikel im  Shopify Online-Shop nicht sichtbar sind.

1. Auswählen die Zeile mit dem Artikel  **1920-S, ANTWERP Konferenztisch**. Geben Sie im  **SEO-Titel** **Rechteckiger Besprechungstisch Antwerpen, 10 Plätze, schwarz** ein.
2. Geben Sie im Feld  **Status**  Auswählen **Aktiv** ein.
3. Auswählen die Zeile mit dem Artikel **1906-S, ATHEN, Mobiler Sockel** und dann Auswählen **Löschen**.

Beachten Sie, dass in **Shopify-Verwaltung** alle Produkte unterschiedliche Status haben.

* *ANTWERP-Konferenztisch* ist *Aktiv*, weil wir seinen Status auf der **Shopify Produkt** seite geändert haben.
* *ATHENS Schreibtisch* ist *Entwurf*, weil wir den Standardstatus für alle hinzugefügten Produkte auf *Entwurf* gesetzt haben.
* *ATHENS Mobile Pedestal* ist *Archiviert*, weil wir den Shop so konfiguriert haben, dass er gelöschten Produkten automatisch den Status *Archiviert* zuweist.

Beachten Sie, dass der Bestand für den ANTWERP-Konferenztisch 100 beträgt, da wir das System so konfiguriert haben, dass nur Bestände von zwei Standorten, MAIN und EAST, verwendet werden. Der Bestand am anderen Standort (WEST) wird ignoriert.

* Öffnen Sie *ANTWERP Conference Table* und achten Sie auf die Felder **Benutzerdefinierter Typ**, **Kreditor**, **Gewicht** und **Kosten pro Artikel** und den Abschnitt **Suchmaschinenauflistung Vorschau**.
* Öffnen Sie *Athens Desk*, scrollen Sie nach unten zum Abschnitt **Varianten** und beachten Sie, wie **SKU** ausgefüllt ist.
* Um Barcode und Preise zu überprüfen, Auswählen **Bearbeiten**.
* Ändern Sie den Status von  **Athens Desk**  in  **Aktiv** und Auswählen **Vorschauversion**.

Öffnen Sie im  Shopify Online-Shop den Produktkatalog und suchen Sie das Produkt  **ATHENS Desk** . Beachten Sie, dass verschiedene Optionen verfügbar sind. Für die verschiedenen Optionen gelten auch unterschiedliche Preise. Achten Sie auf die Rabattinformationen.

### <a name="additional-steps-for-b2b"></a>Zusätzliche Schritte für B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

Sie können den Konnektor so konfigurieren, dass automatisch Kataloge für exportierte Unternehmen erstellt und zugewiesen werden. Die folgenden Schritte sind hilfreich, wenn Sie eine genauere Kontrolle darüber wünschen, was für B2B-Debitoren verfügbar ist.

Erstellen Sie im  **Shopify Administrator** einen Katalog und weisen Sie ihn zu.

1. Wählen Sie **Produkte** und dann **Kataloge** in der Seitenleiste der **Shopify-Verwaltung** aus.
2. Erstellen Sie einen Katalog für bestimmte Produkte. Geben Sie ihm den Titel „B2B“. 
3. Wählen Sie  **Verwalten** und dann  **Produkte und Preise verwalten**.
4. Auswählen den Filter  **Ausgeschlossen**, suchen Sie  **ATHENS Desk** und wählen Sie  **In Katalog aufnehmen**.
5. Auswählen **Kunden** und dann  **Unternehmen**  in der Seitenleiste von  **Shopify admin**.
6. Auswählen **School of Fine Art**, wählen Sie **[...]** und dann  **Kataloge hinzufügen**  und fügen Sie den zuvor erstellten  **B2B** Katalog hinzu.

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor:

Bereiten Sie die Daten vor.

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Artikel** ein und wählen Sie den entsprechenden Link aus.
2. Auswählen item **1896-S, Athens Desk**, und dann folgen diese Schritte:
3. Wählen Sie die Aktion **Verkaufsrabatte** und fügen Sie einen neuen Rabatt hinzu:

   * **Verkaufstyp** *Kundenrab. Gruppe*
   * **Verkaufscode** *LARGE ACC*
   * **Typ** *Artikel*
   * **Code** *1896-S*
   * **Code der Maßeinheit** *STK*
   * **Zeilenrabatt %** *25*

4. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Kataloge** ein und wählen Sie den entsprechenden Link aus.
5. Wählen Sie **Kataloge abrufen** aus.
6. Geben Sie im Feld  **Shop-Code**  **DEMO1** ein.
7. Auswählen der Eintrag mit dem *B2B* Katalog, für den Sie Preise synchronisieren möchten.
8. Aktivieren Sie den Umschalter **Preise synchronisieren**.
9. Geben Sie im Feld  **Kundenpreisgruppe**  Auswählen **SHOPIFY** ein.
10. Geben Sie im Feld  **Kundenrabattgruppe**  Auswählen **GROSSES KUNDENBUCH** ein.
11. Wählen Sie **Preis synchronisieren** und warten Sie, bis die Synchronisierung von Preisen abgeschlossen ist.

Erkunden Sie im  **Shopify Admin** die Preise für den  **B2B** Katalog.

Öffnen Sie im **Shopify Onlineshop** den Produktkatalog und suchen Sie das Produkt *ATHENS Desk*. Beachten Sie die Preis- und Rabatthinweise.

## <a name="walkthrough-check-out-and-order-synchronization-for-individual-buyer-and-company-representative"></a>Exemplarische Vorgehensweise: Zur Kasse gehen und Auftragssynchronisierung für einzelne Kaufende und Unternehmensvertreter

Dies ist eine Fortsetzung von [Beispielhafte Vorgehensweise: Mit dem Online-Verkauf von Produkten beginnen](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Sie können es auch mit Ihren eigenen Daten versuchen, beispielsweise mithilfe Ihres Shopify Stores oder Ihrer Sandbox.

Einzelner Kaufender

1. Tun Sie im **Shopify-Onlineshop** Folgendes. Wählen Sie das Symbol **Konto** aus. Geben Sie eine E-Mail-Adresse ein, auf die Sie Zugriff haben.
2. Melden Sie sich mit einem einmaligen 6-stelligen Bestätigungscode an, der Ihnen per E-Mail zugesandt wurde.
3. Durchsuchen Sie den Produktkatalog. Sie sollten alle Produkte mit Einzelhandelspreisen sehen können.
4. Wählen Sie die Variante „Essential“ und dann **Jetzt kaufen** und gehen Sie zur Kasse.
5. Füllen Sie die Felder **Vorname** und **Nachname** aus.
6. Geben Sie die lokale Adresse ein.
7. Behalten Sie *Standard* als Versandmethode bei.
8. Geben Sie im Feld  **Kredit-Karte-Nummer**  **1**  ein, wenn Sie  **(zum Testen) Bogus Gateway** verwenden, oder geben Sie  **5555 5555 5555 4444**  ein, wenn Sie  **Shopify Zahlungen** im Testmodus verwenden.
9. Geben Sie in das Feld **Ablaufdatum** den aktuellen Monat/Jahr ein.
10. Geben Sie im Feld  **Sicherheitscode** die Zahl  **111** ein.
11. Füllen Sie das Feld **Name auf der Karte** aus.
12. Wählen Sie **Jetzt bezahlen**.

Unternehmensvertreter

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. Gehen Sie in der **Shopify-Verwaltung** wie folgt vor.
2. Wählen Sie **Debitoren** und dann **Unternehmen** in der Seitenleiste der **Shopify-Verwaltung** aus.
3. Öffnen Sie den Eintrag *School of Fine Arts*.
4. Wählen Sie **[...]** in der **School of Fine Art** FactBox, dann  **Zahlungsbedingungen bearbeiten** und anschließend Auswählen **Fällig am Auswählen**.
5. Wählen Sie in der Infobox  **Kunden**  **[...]**  und dann  **Kunden hinzufügen**. Fügen Sie anschließend den Kunden mit der E-Mail-Adresse hinzu, mit der Sie sich zuvor im Geschäft angemeldet haben.
6. Tun Sie im **Shopify-Onlineshop** Folgendes. Wählen Sie das Symbol **Konto** aus. Geben Sie eine E-Mail-Adresse ein, auf die Sie Zugriff haben.
7. Melden Sie sich mit einem einmaligen 6-stelligen Bestätigungscode an, der Ihnen per E-Mail zugesandt wurde.
8. Durchsuchen Sie den Produktkatalog. Sie sollten nur Produkte sehen können, die dem B2B-Katalog mit Sonderpreisen für den Einzelhandel hinzugefügt wurden.
9. Auswählen die Essential-Variante, Auswählen **Sofort-Kaufen**, und zur Kasse gehen.
10. Beachten Sie, dass Konto, Lieferadresse und Zahlungsmethode ausgefüllt sind.
11. Füllen Sie das Feld  **PO-Nummer**  mit  **PO-12345** aus.
12. Wählen Sie **Auftrag absenden**.

Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die nächsten Schritte aus:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Aufträge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
3. Wählen Sie **OK** aus.

Die importierte Bestellung ist bereit zur Verarbeitung.

1. Auswählen die importierte Bestellung, um die Seite  **Shopify Bestellung**  zu öffnen.
2. Beachten Sie, dass beide Bestellungen von derselben Person aufgegeben wurden und mit zwei verschiedenen Kunden verknüpft sind.
3. In der im Namen des Unternehmens übermittelten Bestellung können Sie im Feld  **Bestellnummer**  einen Wert sehen, der auch in das Feld  **Externe Belegnummer**  des erstellten Verkaufsbelegs übertragen wird.
4. Da wir das B2B-Unternehmen für die Abwicklung von Zahlungen außerhalb von  Shopify konfiguriert haben, wird der  **Finanzstatus**  auf  **Ausstehend** gesetzt. Nachdem Sie die Zahlung erhalten haben, führen Sie die Aktion  **Als bezahlt markieren**  aus. Der Finanzstatus wird in Shopify aktualisiert.

## <a name="walkthrough-import-items-customers-companies-from-shopify"></a>Exemplarische Vorgehensweise: Artikel, Debitoren, Unternehmen aus Shopify importieren

### <a name="scenario-3"></a>Szenario

Sie haben bereits einen erfolgreichen Online-Store und möchten [!INCLUDE[prod_short](../includes/prod_short.md)] als Software für die Unternehmensverwaltung einsetzen. Sie möchten so viele Daten wie möglich aus Shopify importieren.

### <a name="steps-2"></a>Schritte

Dies ist eine Fortsetzung von [Exemplarische Vorgehensweise: Mit dem Onlineverkauf von Produkten beginnen](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) und [Exemplarische Vorgehensweise: Debitoren Ihrem neuen Onlineshop hinzufügen](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). Sie können es auch mit Ihren eigenen Daten versuchen, beispielsweise mithilfe Ihres Shopify Stores oder Ihrer Sandbox.

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] wie folgt vor.

#### <a name="prepare-data"></a>Daten vorbereiten

1. Wechseln Sie zu einem kostenlosen 30-tägigen Test ohne Beispieldaten. Weitere Informationen finden Sie unter [Eigene Daten zu einem leeren Test hinzufügen](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den dazugehörigen Link.
3. Wählen Sie **Neu** aus.
4. Geben Sie in das Feld **Code** **DEMO2** ein.
5. Geben Sie in das Feld **Shopify URL** die URL des Online-Shops ein, mit dem Sie sich verbinden möchten.
6. Aktivieren Sie den Schalter **Aktiviert**, lesen und akzeptieren Sie die dann die Bestimmungen.

Konfigurieren Sie den Shopify-Shop wie hier beschrieben:

1. Schalten Sie den Schalter **Hintergrundsynchronisationen zulassen** aus.
2. Geben Sie im Feld  **Element synchronisieren**  Auswählen **Von Shopify** ein.
3. Aktivieren Sie den Schalter  **Unbekannte Elemente automatisch erstellen** .
4. Füllen Sie das Feld **Element Vorlagencode** mit der entsprechenden Vorlage aus.
5. Geben Sie im Feld  **Elementbilder synchronisieren**  Auswählen **Von Shopify** ein.
6. In der  **SKU Zuordnung** field, Auswählen **Artikelnr. + Variantencode**.
7. Im Feld  **Kundenimport von Shopify**, Auswählen **Alle Kunden**.
8. Schalten Sie die Option **Unbekannte Kunden automatisch erstellen** ein.
9. Füllen Sie das Feld **Debitoren-/Unternehmensvorlagencode** mit der entsprechenden Vorlage aus.
10. Geben Sie im Feld  **Firmenimport von Shopify**  Auswählen **Alle Kunden** ein.
11. Aktivieren Sie den Schalter  **Unbekanntes Unternehmen automatisch erstellen** .

#### <a name="run-the-synchronization"></a>Führen Sie die Synchronisierung aus

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify Shops** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie den *DEMO2*-Shop, für den Sie Daten synchronisieren möchten, um die Seite **Shopify Shopkarte** zu öffnen.
3. Wählen Sie **Produkte synchronisieren**.
4. Wählen Sie **Produktbilder synchronisieren** aus.
5. Wählen Sie **Debitoren synchronisieren**.
6. Wählen Sie **Unternehmen synchronisieren**

### <a name="results"></a>Ergebnisse

* Shopify Produkte werden importiert. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol aus, geben Sie **Shopify Produkte** ein und wählen Sie den entsprechenden Link.
* Es werden Elemente mit Bildern erstellt. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Artikel** ein und wählen Sie den entsprechenden Link aus.
* Shopify Kunden werden importiert. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Debitoren** ein und wählen Sie den entsprechenden Link aus.
* Shopify Unternehmen werden importiert. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Shopify-Unternehmen** ein und wählen Sie den entsprechenden Link aus.
* Die Kunden werden erstellt. Wählen Sie zur Überprüfung die ![Glühbirne, welche die „Sie wünschen ...“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Debitoren** ein und wählen Sie den entsprechenden Link aus.

## <a name="see-also"></a>Siehe auch

[Erste Schritte mit dem Shopify-Konnektor](get-started.md)  
