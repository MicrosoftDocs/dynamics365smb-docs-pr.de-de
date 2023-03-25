---
title: Verkaufsaufträge synchronisieren und erfüllen
description: Nehmen Sie die Einrichtung und Ausführung des Imports under der Verarbeitung von Verkaufsaufträgen über Shopify vor.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Verkaufsaufträge synchronisieren und erfüllen

Dieser Artikel beschreibt die notwendigen Einstellungen und Schritte, die Sie durchführen müssen, um Verkaufsaufträge mit Shopify in [!INCLUDE[prod_short](../includes/prod_short.md)] zu synchronisieren und zu erfüllen.

## Legen Sie den Import von Bestellungen auf der Shopify Shop-Karte fest.

Geben Sie einen **Währungscode** ein, wenn Ihr Onlineshop eine andere Währung als die lokale Währung (MW) verwendet. Für die angegebene Währung müssen Wechselkurse konfiguriert sein. Wenn Ihr Onlineshop dieselbe Währung verwendet wie [!INCLUDE[prod_short](../includes/prod_short.md)], lassen Sie das Feld leer. 

Sie können die Store-Währung in den [Store-Details](https://www.shopify.com/admin/settings/general) Einstellungen in Ihrem Shopify Admin sehen. Shopify kann so konfiguriert werden, dass verschiedene Währungen akzeptiert werden, aber importierte Bestellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] verwenden die Store-Währung.

Eine reguläre Shopify-Bestellung kann zusätzlich zur Zwischensumme Kosten enthalten, z.B. Versandkosten oder, falls aktiviert, Trinkgelder. Diese Beträge werden direkt auf das Sachkonto gebucht, das Sie für bestimmte Vorgangsarten verwenden möchten:

* **Lieferkostenkonto**
* **Konto für verkaufte Geschenkkarte**, weitere Informationen unter [Geschenkkarte](synchronize-orders.md#gift-cards)
* **Konto für Trinkgelder**  

Aktivieren Sie **Aufträge automatisch erstellen**, um automatisch Verkaufsaufträge in [!INCLUDE[prod_short](../includes/prod_short.md)] zu erstellen, sobald der Shopify-Auftrag importiert ist.

Der Verkaufsbeleg in [!INCLUDE[prod_short](../includes/prod_short.md)] enthält einen Link zur Shopify- Bestellung. Wenn Sie das Feld **Shopify-Auftragsnummer in Belegzeile** auswählen, werden diese Informationen in den Verkaufszeilen vom Typ *Kommentar* wiederholt.

Im Feld **Steuergebietsquelle** können Sie die Priorität für die Auswahl des Steuergebietscodes oder der MwSt.-Geschäftsbuchungsgruppe basierend auf der Adresse festlegen. Die importierte Shopify Bestellung enthält Informationen zu Steuern, aber die Steuern werden neu berechnet, wenn Sie den Verkaufsbeleg erstellen, daher ist es wichtig, dass die Mehrwertsteuer-/Steuereinstellungen korrekt sind [!INCLUDE[prod_short](../includes/prod_short.md)]. Weitere Informationen über Steuern finden Sie unter [Steuern für die Shopify-Verbindung festlegen](setup-taxes.md).

### Zuordnung von Versandmethoden

Der **Versandartencode** für aus Shopify importierte Verkaufsdokumente kann automatisch ausgefüllt werden. Sie müssen die **Zuordnung von Versandmethoden** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop aus, für den Sie eine Zuordnung definieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung von Versandmethoden** aus. Dadurch werden die Datensätze für Versandmethoden, die in den Einstellungen für den [**Versand**](https://www.shopify.com/admin/settings/payments) in Ihrer **Shopify-Verwaltung** definiert sind, automatisch erstellt.
4. Im Feld **Name** sehen Sie den Namen der Versandmethode aus Shopify.
5. Geben Sie den **Versandmethodencode** mit der entsprechenden Versandmethode in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Wenn einem Verkaufsauftrag mehrere Belastungen zugeordnet sind, wird nur eine als Versandart ausgewählt und dem Verkaufsbeleg zugewiesen.

### Zuordnung von Standorten

Die Zuordnung des Lagerplatzes ist für drei Zwecke erforderlich:

* Um den Bestand zu synchronisieren, weitere Informationen finden Sie unter [Bestand mit Shopify](synchronize-items.md#sync-inventory-to-shopify) synchronisieren
* Um den **Lagerplatz-Code** für aus Shopify importierte Belege einzugeben. Dies ist wichtig, wenn die Option **Lagerplatz obligatorisch** auf der Karte **Inventareinrichtung** aktiviert ist, da Sie sonst keine Belege erstellen können.
* So aktualisieren Sie den Auftrag Shopify mit den Erfüllungsinformationen auf der Seite **Gebuchte Verkaufslieferungen**.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie die Zuordnung der Standorte konfigurieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Standorte**, um die **Shopify Shop-Standorte** zu öffnen.
4. Wählen Sie die Aktion **Shopify Standorte abrufen**, um alle in Shopify definierten Standorte zu importieren. Sie finden sie in den [**Standorte**](https://www.shopify.com/admin/settings/locations)-Einstellungen in Ihrem **Shopify Admin**-Panel. Beachten Sie, dass der als *Standard* markierte Speicherort beim Import von unerfüllten Shopify-Bestellungen verwendet wird.
5. Geben Sie den **Standardlagerplatzcode** mit dem entsprechenden Lagerplatz in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

## Führen Sie die Auftragssynchronisation aus

Nachfolgend wird beschrieben, wie Sie die Verkaufsaufträge importieren und aktualisieren.

> [!NOTE]  
> Archivierte Bestellungen in Shopify können nicht importiert werden. Deaktivieren Sie die Option **Bestellung automatisch archivieren** im Abschnitt **Bestellverarbeitung** der **Checkout**-Einstellungen in Ihrem **Shopify Admin**-Panel, um sicherzustellen, dass alle Bestellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] importiert werden. Wenn Sie archivierte Aufträge importieren müssen, verwenden Sie die Aktion **Auftragsarchivierung** auf der Seite [Auftrag](https://www.shopify.com/admin/orders) des **Shopify Admin** Panels.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie Bestellungen importieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen** aus.
4. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
5. Definieren Sie bei Bedarf Filter für Bestellungen. Sie können z.B. vollständig bezahlte Aufträge oder solche mit einem niedrigen Risikoniveau importieren.

> [!NOTE]  
> Beim Filtern nach Tag sollten Sie die Filtertoken `@` und `*` verwenden. Wenn Sie beispielsweise Bestellungen importieren möchten, die *tag1* enthalten, verwenden Sie `@*tag1*`. `@` stellt sicher, dass das Ergebnis die Groß-/Kleinschreibung berücksichtigt, während `*` Aufträge mit mehreren Tags findet.

7. Wählen Sie die Schaltfläche **OK**.

Alternativ können Sie nach dem Batchauftrag **Aufträge synchronisieren von Shopify** suchen.

Sie können die Aufgabe für eine automatische Ausführung planen. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

## Importierte Bestellungen überprüfen

Sobald der Import abgeschlossen ist, können Sie die Shopify-Bestellung durchsuchen und alle zugehörigen Informationen finden, wie z.B. die Transaktionen, die Versandkosten, die Risikostufe, die Bestellattribute und Tags oder die Erfüllungen, wenn die Bestellung bereits in Shopify erfüllt wurde. Sie können auch alle an den Debitor gesendeten Auftragsbestätigungen anzeigen, indem Sie die Aktion **Shopify-Statusseite** auswählen.

> [!NOTE]  
> Sie können direkt zum Fenster **Shopify Bestellungen** navigieren und sehen dort Bestellungen mit dem Status *offen* aus allen Geschäften. Um abgeschlossene Bestellungen zu überprüfen, müssen Sie die Seite **Shopify Bestellungen** aus dem jeweiligen **Shopify Shop Card** Fenster öffnen.

## Verkaufsbelege in Business Central erstellen

Wenn die Option **Automatische Erstellung von Aufträgen** auf der **Shopify Shop Card** aktiviert ist, versucht [!INCLUDE[prod_short](../includes/prod_short.md)] einen Verkaufsbeleg zu erstellen, sobald der Auftrag importiert wurde. Wenn Probleme wie ein fehlender Debitor oder ein fehlendes Produkt auftreten, müssen Sie die Probleme beheben und dann den Verkaufsauftrag erneut erstellen.

### So erstellen Sie Verkaufsbelege

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie Bestellungen synchronisieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen**.
4. Markieren Sie die Bestellung aus, für die Sie einen Verkaufsbeleg erstellen möchten, und wählen Sie die Aktion **Verkaufsbelege erstellen** aus.
5. Wählen Sie **Ja** aus.

Wenn die Shopify Bestellung erfüllt werden muss, wird ein **Verkaufsauftrag** erstellt. Für erfüllte Shopify-Bestellungen, z.B. solche, die nur eine Geschenkkarte enthalten oder die bereits in Shopify behandelt werden, wird eine **Verkaufsrechnung** erstellt.

Ein Verkaufsbeleg ist nun erstellt und kann mit Standarfunktionen von [!INCLUDE[prod_short](../includes/prod_short.md)] verwaltet werden.

### Fehlende Debitoren verwalten

Wenn Ihre Einstellungen die automatische Erstellung eines Debitors verhindern und kein entsprechender vorhandener Debitor gefunden werden kann, müssen Sie der Shopify-Bestellung manuell einen Debitor zuweisen. Es gibt einige Möglichkeiten, dies zu tun:

* Sie können die **Verk. an Deb.-Nr.** und **Rechnung an Debitor Nr.** direkt auf der Seite **Shopify-Bestellungen** zuweisen, indem Sie einen Debitor aus der Liste der vorhandenen Debitoren auswählen.
* Sie können einen Kundenvorlagencode auswählen, erstellen und dann den Kunden über die Aktion **Neuen Kunden erstellen** auf der Seite **Shopify Aufträge** zuordnen. Beachten Sie, dass der Shopify-Debitor über mindestens eine Adresse verfügen muss. Bei Bestellungen, die über den Shopify-Vertriebskanal POS erstellt wurden, fehlen häufig Adressangaben.
* Sie können einen bestehenden Debitor dem zugehörigen **Shopify Kunden** im Fenster **Shopify Kunden** zuordnen und dann die Aktion **Zuordnung finden** auf der Seite **Shopify Aufträge** wählen.

### Wie der Konnektor auswählt, welcher Kunde verwendet werden soll

Die Funktion *Bestellung aus Shopify importieren* versucht, die Debitoren in der folgenden Reihenfolge auszuwählen:

1. Wenn das Feld **Standarddebitorennr.** Feld in der **Shopify Kundenvorlage** für das entsprechende Land definiert ist, dann wird die **Standardkunden-Nr.** wird verwendet, unabhängig von den Einstellungen in den Feldern **Kundenimport von Shopify** und **Kundenzuordnungstyp**. Weitere Informationen unter [Debitorenvorlage pro Land](synchronize-customers.md#customer-template-per-country).
2. Wenn der **Kundenimport von Shopify** auf *Keine* festgelegt ist und die **Standardkunden-Nr.** auf der Seite **Shopify-Shop-Karte** definiert sind, wird die **Standarddebitorennr.** verwendet.

Die nächsten Schritte hängen von der **Kundenzuordnung Typ** ab.

* Wenn dies **Nehmen Sie immer den Standardkunden** ist, dann verwendet der Konnektor den in der **Standarddebitorennr.** definierten Debitor Feld auf der Seite **Shopify Shop-Karte**.
* **Nach E-Mail/Telefon**, der Konnektor versucht, den bestehenden Kunden zuerst nach der ID, dann nach der E-Mail und dann nach der Telefonnummer zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.
* **Nach Rechnungsinformationen** versucht der Konnektor, den bestehenden Kunden zunächst über die ID und dann über die Rechnungsadressinformationen zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.

> [!NOTE]  
> Der Konnektor verwendet die Informationen aus der Rechnungsadresse und erstellt den Rechnungsempfänger in [!INCLUDE[prod_short](../includes/prod_short.md)]. Der Verk. an Debitor ist derselbe wie Rechnung an Debitor.

### Auswirkung der Bearbeitung von Bestellungen

In Shopify:

|Bearbeiten|Auswirkungen|
|------|-----------|
|Den Erfüllungsort ändern | Der ursprüngliche Standort wird mit [!INCLUDE[prod_short](../includes/prod_short.md)] synchronisiert. |
|Ändern Sie den Erfüllungsort und registrieren Sie die Auftragserfüllung in Shopify.| Wenn die Bestellung bereits importiert wurde, werden die Zeilen nicht aktualisiert. Andernfalls wird für den importierten Auftrag der Erfüllungsort verwendet. |
|Bearbeiten Sie eine Bestellung und ändern Sie die Menge| Der Auftragskopf und die Zusatztabellen werden in [!INCLUDE[prod_short](../includes/prod_short.md)] aktualisiert, die Zeilen nicht. |
|Bearbeiten Sie eine Bestellung und fügen Sie einen neuen Artikel hinzu | Der Auftragskopf wird aktualisiert, die Zeilen nicht. |

In [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Bearbeiten|Auswirkungen|
|------|-----------|
|Ändern Sie den Standort in einen anderen Standort, der den Shopify Orten zugeordnet ist. Sendung buchen. | Nach der Synchronisierung der Erfüllung wird der Lagerplatz in Shopify aktualisiert. |
|Ändern Sie den Ort in einen anderen Ort, der nicht den Shopify Orten zugeordnet ist. Sendung buchen. | Die Erfüllung wird nicht mit Shopify synchronisiert. |
|Ändern der Abnahmemenge. Sendung buchen. | Die Reihenfolge Shopify wird als teilweise erfüllt gekennzeichnet. |
|Ein neues Element hinzufügen. Sendung buchen. | Die Reihenfolge Shopify wird als erfüllt markiert. Die Zeilen werden nicht aktualisiert. |

## Lieferungen mit Shopify synchronisieren

Wenn ein Verkaufsauftrag, der aus einem Shopify-Auftrag erstellt wurde, versandt wird, können Sie die Sendungen mit Shopify synchronisieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Sendungen mit Shopify synchronisieren** ein und wählen Sie dann den entsprechenden Link.
2. Definieren Sie die Filter für Sendungen nach Bedarf. Sie können zum Beispiel eine Sendung aktualisieren, die zu einem bestimmten Datum gebucht wurde.
3. Wählen Sie die Schaltfläche **OK**.

Die Bestellung in Shopify wird als erfüllt markiert. Der Debitor erhält automatisch eine Versandbenachrichtigung per E-Mail oder Textnachricht (SMS). Wenn ein Zusteller und ein Verfolgungscode für die Lieferung angegeben sind, sind die Verfolgungsinformationen in der E-Mail enthalten.

Alternativ können Sie die Aktion **Sync Sendungen** auf den Seiten Shopify Verkaufsaufträge oder Shopify Shop verwenden.

Sie können die Aufgabe für eine automatische Ausführung planen. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

>[Wichtig] Der Lagerplatz, einschließlich des leeren Lagerplatzes, der in der Zeile “Gebuchte Sendung„ definiert ist, muss einen passenden Datensatz in der Shopify Location haben. Andernfalls wird diese Zeile nicht an Shopify zurückgeschickt. Erfahren Sie mehr unter [Zuordnung von Lagerplätzen](synchronize-orders.md#location-mapping).

Denken Sie daran, **Bestellungen aus Shopify** auszuführen, um den Erfüllungsstatus der Bestellung in [!INCLUDE[prod_short](../includes/prod_short.md)] zu aktualisieren. Die Konnektor-Funktionalität archiviert auch vollständig bezahlte und erfüllte Bestellungen sowohl in Shopify als auch in [!INCLUDE[prod_short](../includes/prod_short.md)], sofern die Bedingungen erfüllt sind.

### Zusteller und Verfolgungs-URL

Wenn das Dokument **Gebuchte Verkaufslieferung** den **Versandagentencode** und/oder die **Paketverfolgungsnummer** enthält, werden diese Informationen an Shopify und an den Kunden in der Versandbestätigungs-E-Mail gesendet.

Die verfolgende Firma wird auf der Grundlage des Datensatzes des Zustellers mit der folgenden Folge (von oben nach unten) eingetragen:

* **Shopify-Nachverfolgungsunternehmen**
* **Name**
* **Code**

Wenn das Feld **Paketverfolgungs-URL** für den Datensatz des Zustellers ausgefüllt ist, dann enthält die Versandbestätigung ebenfalls eine Verfolgungs-URL.

## Geschenkkarten

Im Shopify-Shop können Sie Geschenkgutscheine verkaufen, mit denen echte Produkte bezahlt werden können.

Wenn Sie mit Geschenkkarten arbeiten, ist es wichtig, dass Sie im Fenster **Shopify Shop-Karte** einen Wert in das Feld **Geschenkkartenkonto** eingeben. Die verkaufte Geschenkkarte wird zusammen mit den entsprechenden Bestellungen synchronisiert. Eine angewendete Geschenkkarte wird ebenfalls mit der Bestellung importiert, jetzt jedoch als Transaktion. Beachten Sie, dass die Geschenkkarte den Rechnungsbetrag nicht reduziert.

Um die ausgegebenen und angewendeten Geschenkkarten zu überprüfen, wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Geschenkkarten** ein, und wählen Sie dann den entsprechenden Link.

## Siehe auch

[Einstieg in den Konnektor für Shopify](get-started.md)  
