---
title: Festlegen und Verwenden des Shopify Konnektors
description: Verschiedene Integrationsszenarien zur Demonstration des Workflows zwischen Shopify und Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector" />Exemplarische Vorgehensweise: Festlegen und Verwenden des Shopify Konnektors

Dieser Abschnitt demonstriert einige typische Szenarien und führt Sie durch die Schritte, mit denen Sie den Workflow des integrierten [!INCLUDE[prod_short](../includes/prod_short.md)] und des Shopify Stores testen oder Benutzer schulen können.

## <a name="prerequisites" />Voraussetzungen

### <a name="shopify" />Shopify

Sie benötigen Folgendes:

- Ein Shopify-Konto
- Ein Shopify-Online-Store

Erfahren Sie mehr darüber, wie Sie Shopify-Tests erstellen, und über die empfohlenen Einstellungen unter [Erstellen und Einrichten eines Shopify-Kontos](shopify-account.md).

### <a name="business-central" />Business Central

Sie müssen ein [!INCLUDE[prod_short](../includes/prod_short.md)]-Konto haben. 

Sie können zum Beispiel ein Demokonto erstellen oder einen Test starten. Weitere Informationen finden Sie unter [Demonstrationsumgebung vorbereiten für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) und [Anmelden für den Test](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop" />Verbinden Sie Business Central mit dem Shopify-Laden

Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die folgenden Schritte aus:

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu**.
3. Geben Sie in das Feld **Code** `DEMO1` ein.
4. Geben Sie in das Feld **Shopify URL** die URL des Online-Shops ein, mit dem Sie sich verbinden möchten.
5. Aktivieren Sie den Schalter **Aktiviert**, lesen und akzeptieren Sie die Bestimmungen.

Konfigurieren Sie den Shopify Shop wie in den folgenden Schritten beschrieben:

1. Schalten Sie den Schalter **Log Enabled** ein.
2. Schalten Sie den Schalter **Hintergrundsynchronisationen zulassen** aus.
3. Wählen Sie **Zu Shopify** in dem Feld **Element synchronisieren**.
4. Wählen Sie **Bis Shopify** im Feld **Bilder von Elementen synchronisieren**.
5. Schalten Sie das Kontrollkästchen **Artikelattribute synchronisieren** ein.
6. Schalten Sie das Kontrollkästchen **Bestand verfolgen** ein.
7. Wählen Sie **Ablehnen** im Feld **Standardrichtlinie für den Bestand**.
8. Schalten Sie die Option **Unbekannte Kunden automatisch erstellen** ein.
9. Füllen Sie das Feld **Kundenvorlagencode** mit der entsprechenden Vorlage aus.
10. Füllen Sie das Feld **Versandkostenkonto**, das Feld **Tippkonto** mit dem Umsatzkonto aus. In den USA verwenden Sie zum Beispiel `40100`.
11. Schalten Sie die Option **Bestellungen automatisch erstellen** ein.

Konfigurieren Sie die Zuordnung von Standorten:

1. Wählen Sie die Aktion **Standorte** aus, um **Shopify-Shop-Standorte** zu öffnen.
2. Wählen Sie die Aktion **Abrufen Shopify Standorte**, um alle in Shopify definierten Standorte zu importieren.
3. Geben Sie im **Ortsfilter** `''|EAST|MAIN` ein.
4. Schalten Sie den Schalter **Deaktiviert** aus, um die Synchronisierung des Bestands für den ausgewählten Shopify-Ort zu aktivieren.

## <a name="walkthrough-start-selling-products-online" />Exemplarische Vorgehensweise: Mit dem Online-Verkauf von Produkten beginnen

### <a name="scenario" />Szenario

Nehmen wir an, Sie möchten Shopify als Online Store ausprobieren, ohne viel Zeit mit der Einrichtung zu verbringen, vor allem, weil Sie Ihre Elemente in [!INCLUDE[prod_short](../includes/prod_short.md)] bereits gut pflegen. Nachdem Sie Ihren Shopify-Online-Store eröffnet haben, erhalten Sie sofort neue Kunden, die mit Ihrem Shop und ihrem Einkaufserlebnis zufrieden sind. Also beschließen sie, an der Kasse Tipps zu hinterlassen.

### <a name="steps" />Schritte

Gehen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die folgenden Schritte durch:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Shopify Produkte** ein und wählen Sie den entsprechenden Link.
2. Wählen Sie die Aktion **Artikel hinzufügen** aus.
3. Geben Sie in das Feld **Shop Code** *DEMO1* ein.
4. Legen Sie den Filter `CHAIR` auf dem Feld **Element-Kategorie-Code** fest (fügen Sie bei Bedarf ein Filterfeld hinzu).
5. Wählen Sie **OK** und warten Sie, bis die anfängliche Synchronisierung von Artikeln und Preisen abgeschlossen ist.
6. Wählen Sie die Aktion **Produktbilder synchronisieren**.
7. Wählen Sie die Aktion **Bestand synchronisieren**.

In **Shopify-Onlineshop**
> [!Tip]  
> Öffnen Sie **Shopify Verwaltung**, indem Sie die URL aufrufen, die im Feld **URL** auf der Seite **Shopify Shop-Karte** angegeben ist. Wählen Sie anschließend das Augensymbol neben dem Verkaufskanal **Onlineshop** aus, der sich in der Seitenleiste der **Shopify-Verwaltung** befindet. 

Öffnen Sie den Produktkatalog. Beachten Sie:

* Produkttitel, Bilder und Preise.
* Verfügbarkeitsanzeige (ausverkauft für Produkte, die nicht auf Lager sind).

Wählen Sie ein beliebiges Produkt, das verkauft werden kann, zum Beispiel die `BERLIN Swivel Chair, yellow`. Beachten Sie, dass die Beschreibung Artikelattribute enthält.

Wählen Sie die Schaltfläche **Jetzt kaufen** und gehen Sie zur Kasse.

1. Geben Sie in das Feld **E-Mail- oder Mobiltelefonnummer** die `cl@contoso.com` ein (oder die E-Mail, an die Sie Bestell- und Versandbestätigungen erhalten möchten).
2. Geben Sie in die Felder **Vorname** und **Nachname** `Claudia Lawson` ein.
3. Geben Sie die lokale Adresse ein.
4. Wählen Sie das Kontrollkästchen **Diese Informationen für das nächste Mal speichern**.
5. Wählen Sie die Schaltfläche **Weiter zum Versand**.
6. Behalten Sie `Standard` als Versandart bei und wählen Sie dann die Schaltfläche **Weiter zur Zahlung**.
7. Wählen Sie `10%` Tipp.
8. Geben Sie im Feld **Kreditkarte** eine `1` ein, wenn Sie *(zu Testzwecken) Bogus Gateway* verwenden oder geben Sie `5555 5555 5555 4444` ein, wenn Sie *Shopify Payments* im Testmodus verwenden.
9. Füllen Sie das Feld **Name auf der Karte** aus.
10. Geben Sie in das Feld **Ablaufdatum** den aktuellen Monat/Jahr ein.
11. In das Feld **Sicherheitscode** geben Sie `111` ein.
12. Wählen Sie die Schaltfläche **Jetzt bezahlen**.

Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die nächsten Schritte aus:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Shopify Bestellungen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
3. Wählen Sie **OK** aus.

Die importierte Bestellung ist bereit zur Verarbeitung.

1. Wählen Sie den importierten Auftrag, um das Fenster **Shopify Aufträge** zu öffnen.
2. Beachten Sie, dass der neue Kunde und der neue Verkaufsauftrag erstellt wurden.
3. Erkunden Sie die Aktionen **Risiko** und **Versandkosten**.
4. Wählen Sie die Aktion **Verkaufsauftrag**, um das Fenster **Verkaufsauftrag** zu öffnen. Ein Verkaufsauftrag ist ein Bedarf, der bei Bedarf durch Montage, Produktion oder Kauf mit Hilfe der Planungs-Engine gedeckt werden kann. Es unterstützt auch verschiedene Lagerort-Verarbeitungsprozesse mit vollständiger Aufgabentrennung.
5. Wählen Sie die Aktion **Wiedereröffnen**.
6. Geben Sie in das Feld **Bearbeiter** `DHL` ein.
7. Geben Sie in das Feld **Paketverfolgungsnummer** `123456789` ein.
8. Wählen Sie die Aktion **Buchen**, behalten Sie die Option **Versand und Rechnungen** bei und wählen Sie dann die Schaltfläche **OK**.

Jetzt sind die physischen und finanziellen Daten in [!INCLUDE[prod_short](../includes/prod_short.md)] registriert. Jetzt ist es an der Zeit, Shopify über die Änderungen zu informieren.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") , geben Sie **Lieferungen mit Shopify synchronisieren** ein, und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie **OK** aus.

In **Shopify Admin** sehen Sie, dass die Bestellung jetzt als *Erfüllt* markiert ist. Sie können auch die Details der Sendung einsehen und die URL der Sendungsverfolgung sehen. Wenn Sie **Bestellungen von Shopify synchronisieren** erneut ausführen, wird die Bestellung in beiden Systemen archiviert.

## <a name="walkthrough-invite-your-customers-to-your-new-online-store" />Exemplarische Vorgehensweise: Laden Sie Ihre Kunden in Ihren neuen Online Store ein

### <a name="scenario" />Szenario

Nach einem erfolgreichen Schnellstart Ihres neuen Online Stores möchten Sie, dass Ihre derzeitigen Kunden ihn besuchen und Bestellungen aufgeben.

### <a name="steps" />Schritte

Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die folgenden Schritte aus:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Shopify Shops** ein, und wählen Sie den entsprechenden Link.
2. Wählen Sie den **DEMO1** Shop, für den Sie Kunden synchronisieren möchten, um die **Shopify Shop Card** Seite zu öffnen.
3. Wählen Sie die Aktion **Debitoren synchronisieren** aus.

In **Shopify Admin** sehen Sie, dass die Kunden importiert wurden. Öffnen Sie einen der Kunden und stellen Sie fest, dass der Vor- und Nachname des Kunden aus dem Feld **Kontaktname** der **Kundenkarte** stammt. Der Name der Firma ist in der Standardadresse zu finden, die mit dem Kunden verknüpft ist. Wählen Sie **Kontoeinladung senden**, um den Kunden einzuladen.

## <a name="walkthrough-fine-tuning-of-item-management" />Exemplarische Vorgehensweise: Feinabstimmung der Element-Verwaltung

### <a name="scenario" />Szenario

Sie möchten Ihren Prozessen rund um die Verwaltung von Elementen mehr Flexibilität und Steuerelemente hinzufügen. Sie möchten die Produktbeschreibungen verbessern und weitere Überprüfungsschritte hinzufügen, bevor die Produkte für den Endkunden verfügbar sind.

### <a name="steps" />Schritte

Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die folgenden Schritte aus:

Bereiten Sie die Daten vor.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Kundenpreisgruppe** ein und wählen Sie den entsprechenden Link.
2. Fügen Sie eine neue Preisgruppe hinzu. Geben Sie in das Feld **Code** `SHOPIFY` ein.
3. Schließen Sie das Fenster **Kundenpreisgruppe**.
4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Elemente** ein und wählen Sie den zugehörigen Link.

Wählen Sie Artikel **1896-S, Athens Desk** aus und führen Sie die folgenden Schritte aus.

1. Wählen Sie die Aktion **Varianten** und fügen Sie dann zwei Varianten `PREMIUM, Athens Desk, Premium edition` und `ESSENTIAL, Athens Desk, Essential edition` hinzu.
2. Wählen Sie die Aktion **Erweiterter Text**, erstellen Sie einen neuen erweiterten Text, der für alle Sprachcodes gilt. Geben Sie in das Feld **Beschreibung** `Shopify` ein. 
3. Fügen Sie den folgenden Text mit HTML-Tags hinzu: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`.
4. Wählen Sie die Aktion **Verkaufspreise** und fügen Sie neue Preise hinzu, wie in der folgenden Tabelle gezeigt:

  |Auftrag|**Verkaufsart**|**Verkaufscode**|Typ|Code|Variantencode<br>(fügen Sie das Feld über die Personalisierung hinzu)|VK-Preis|
  |------|------------|------------|------------|------------|------------|------------|
  |0|Debitorenpreisgruppe|SHOPIFY|Option|1896-S|ESSENTIAL|700|
  |2|Debitorenpreisgruppe|SHOPIFY|Artikel|1896-S|PREMIUM|1000|

5. Wählen Sie die Aktion **Verkaufsrabatte** und fügen Sie einen neuen Rabatt hinzu:

* **Verkaufstyp** *Kundenrab. Gruppe*
* **Verkaufscode** *RETAIL*
* **Typ** *Artikel*
* **Code** *1896-S*
* **Code der Maßeinheit** *STK*
* **Zeilenrabatt %** *10*

6. Wählen Sie die Aktion **Element Referenzen** und fügen Sie die folgenden Zeilen hinzu:

  |Auftrag|**Referenztyp**|**Referenz Nr.**|Variantencode|
  |------|------------|------------|------------|
  |0|Strichcode|77777777|ESSENTIAL|
  |2|Strichcode|11111111|PREMIUM|


Wählen Sie das Element **1920-S, Konferenztisch ANTWERPEN** und führen Sie die folgenden Schritte aus.

1. Wählen Sie **Bestand anpassen** und geben Sie im Feld **Neuer Bestand** `100` für die Standorte *Ost* und *West* ein. 
2. Wählen Sie **OK** aus.

Passen Sie die Synchronisationseinstellungen an.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Shopify Shops** ein, und wählen Sie den entsprechenden Link.
2. Wählen Sie den *DEMO1* Shop, für den Sie Artikel synchronisieren möchten, um die Seite Shopify Shop Card zu öffnen.
3. Wählen Sie *SHOPIFY* im Feld **Kundenpreisgruppe**.
4. Wählen Sie *RETAIL* im Feld **Kundenrabattgruppe**.
5. Aktivieren Sie das Feld **Erweiterter Text des Elements synchronisieren**.
6. Wählen Sie *Artikel Nr.+ Variantencode* im Feld **SKU Zuordnung**.
7. Wählen Sie *Entwurf* im Feld **Status für erstellte Produkte**.
8. Wählen Sie *Status auf Archiviert* im Feld **Aktion für entferntes Produkt**.

Führen Sie die Synchronisierung aus.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Shopify Shops** ein, und wählen Sie den entsprechenden Link.
2. Wählen Sie den *DEMO1* Shop, für den Sie Artikel synchronisieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Produkte**, um das Fenster **Shopify Produkte** zu öffnen.
4. Wählen Sie die Aktion **Elemente hinzufügen**.
5. Legen Sie den Filter *TABLE* auf dem Feld **Elementkategorie Code** fest.
6. Wählen Sie die Aktion **Produktbilder synchronisieren**.
7. Wählen Sie die Aktion **Bestand synchronisieren**.

Die Produkte werden hinzugefügt. Beachten Sie, dass der Status auf *Entwurf* festgelegt ist, so dass die Elemente im Online Store Shopify nicht sichtbar sind.

1. Wählen Sie die Zeile mit dem Element *1920-S, ANTWERP Konferenztisch*. Geben Sie im **SEO Titel** `Rectangular meeting table Antwerp, 10 seats, black` ein.
2. Wählen Sie *Aktiv* im Feld **Status**.
3. Markieren Sie die Zeile mit dem Element *1906-S, ATHENS, Mobile Pedestal* und wählen Sie dann die Aktion **Löschen**.

Beachten Sie in **Shopify Admin**, dass alle Produkte unterschiedliche Status haben.

* *ANTWERP Konferenztisch* ist *Aktiv*, weil wir den Status im Fenster **Shopify Produkt** geändert haben.
* *ATHENS Schreibtisch* ist *Entwurf*, weil wir den Standardstatus für alle hinzugefügten Produkte auf *Entwurf* gesetzt haben.
* *ATHENS Mobile Pedestal* ist *Archiviert*, weil wir den Shop so konfiguriert haben, dass er gelöschten Produkten automatisch den Status *Archiviert* zuweist.

Beachten Sie, dass der Bestand für ANTWERP Konferenztisch 100 beträgt, da wir das System so konfiguriert haben, dass es nur den Bestand von zwei Standorten (MAIN und EAST) verwendet. Der Bestand an anderen Standorten (WEST) wird ignoriert.

* Öffnen Sie *ANTWERP Konferenztisch*, beachten Sie die Felder **Benutzerdefinierter Typ**, **Lieferant**, **Gewicht**, **Kosten pro Element** und den Abschnitt **Suchmaschinenauflistung Vorschau**.
* Öffnen Sie *Athens Schreibtisch*, scrollen Sie nach unten zum Abschnitt **Varianten** und beachten Sie, wie **SKU** ausgefüllt ist.
* Wählen Sie **Bearbeiten**, um Barcode und Preise zu überprüfen.
* Ändern Sie den Status von *Athens Schreibtisch* auf *Aktiv* und wählen Sie die Aktion **Vorschau**.

Öffnen Sie im **Shopify Online Store** den Produktkatalog und suchen Sie das Produkt *ATHENS Schreibtisch*. Beachten Sie, dass verschiedene Optionen verfügbar sind. Für die verschiedenen Optionen gelten auch unterschiedliche Preise. Achten Sie auf die Rabattinformationen.

## <a name="walkthrough-import-items-from-shopify" />Exemplarische Vorgehensweise: Elemente aus Shopify importieren

### <a name="scenario" />Szenario

Sie haben bereits einen erfolgreichen Online-Store und möchten [!INCLUDE[prod_short](../includes/prod_short.md)] als Software für die Unternehmensverwaltung einsetzen. Sie möchten so viele Daten wie möglich aus Shopify importieren. 

### <a name="steps" />Schritte

Dies ist eine Fortsetzung von [Beispielhafte Vorgehensweise: Mit dem Online-Verkauf von Produkten beginnen](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). Sie können es auch mit Ihren eigenen Daten versuchen, zum Beispiel mit Ihrem Shopify Store oder Ihrer Sandbox.

Führen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die folgenden Schritte aus:

#### <a name="prepare-data" />Daten vorbereiten

1. Wechseln Sie zu einem kostenlosen 30-tägigen Test ohne Beispieldaten. Weitere Informationen finden Sie unter [Eigene Daten zu einem leeren Test hinzufügen](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
3. Wählen Sie die Aktion **Neu**.
4. Geben Sie in das Feld **Code** `DEMO2` ein.
5. Geben Sie in das Feld **Shopify URL** die URL des Online-Shops ein, mit dem Sie sich verbinden möchten.
6. Aktivieren Sie den Schalter **Aktiviert**, lesen und akzeptieren Sie die Bestimmungen.

Konfigurieren Sie den Shopify Shop wie in den nächsten Schritten beschrieben:

7. Aktivieren Sie das **Log Enabled** Kippschalter.
8. Deaktivieren Sie das Kippschalter **Hintergrundsynchronisationen zulassen**.
9. Wählen Sie **Aus Shopify** im Feld **Sync Element**.
5. Aktivieren Sie das Umschaltkästchen **Unbekannte Elemente automatisch erstellen**.
11. Füllen Sie das Feld **Element Vorlagencode** mit der entsprechenden Vorlage aus.
12. Wählen Sie **Aus Shopify** im Feld **Artikelbilder synchronisieren**.
13. Wählen Sie **Alle Kunden** im Feld **Kundenimport ab Shopify**.
14. Aktivieren Sie die Umschaltfunktion **Unbekannte Kunden automatisch erstellen**.
15. Füllen Sie das Feld **Kundenvorlagencode** mit der entsprechenden Vorlage aus.
16. Füllen Sie das **Versandkostenkonto**, das **Tippkonto** mit dem Umsatzkonto aus. Verwenden Sie in den USA zum Beispiel `40100`.
17. Aktivieren Sie das Kästchen **Bestellungen automatisch erstellen**.

#### <a name="run-the-synchronization" />Führen Sie die Synchronisierung aus

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Shopify Shops** ein, und wählen Sie den entsprechenden Link.
2. Wählen Sie den *DEMO2* Shop, für den Sie Daten synchronisieren möchten, um die **Shopify Shop Card** Seite zu öffnen.
3. Wählen Sie die Aktion **Produkte synchronisieren** aus.
4. Wählen Sie die Aktion **Produktbilder synchronisieren**.
5. Wählen Sie die Aktion **Kunden synchronisieren**.

### <a name="results" />Ergebnisse

* Shopify Produkte werden importiert. Zur Überprüfung wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Shopify Produkte** ein und wählen Sie den entsprechenden Link.
* Es werden Elemente mit Bildern erstellt. Wählen Sie zum Überprüfen die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Element** ein und wählen Sie den zugehörigen Link.
* Shopify Kunden werden importiert. Um dies zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Shopify Kunden** ein und wählen Sie den zugehörigen Link.
* Die Kunden werden erstellt. Wählen Sie zum Überprüfen die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Kunden** ein und wählen Sie den zugehörigen Link.


## <a name="see-also" />Siehe auch

[Einstieg in den Konnektor Shopify](get-started.md)  
