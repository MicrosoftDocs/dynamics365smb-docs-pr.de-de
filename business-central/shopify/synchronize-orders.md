---
title: Verkaufsaufträge synchronisieren und erfüllen
description: Nehmen Sie die Einrichtung und Ausführung des Imports under der Verarbeitung von Verkaufsaufträgen über Shopify vor.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30124, 30125, 30128, 30129, 30130, 30131, 30132, 30133, 30134,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 3a8f6b2188c2a315bbed1ef99e23b6bbfafae40f
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361392"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Verkaufsaufträge synchronisieren und erfüllen

Dieser Artikel beschreibt die notwendigen Einstellungen und Schritte, die Sie durchführen müssen, um Verkaufsaufträge mit Shopify in [!INCLUDE[prod_short](../includes/prod_short.md)] zu synchronisieren und zu erfüllen.

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Legen Sie den Import von Bestellungen auf der Shopify Shop-Karte fest.

Zu einer regulären Shopify-Bestellung können zusätzliche Beträge zur Zwischensumme hinzukommen, darunter Versandkosten oder Trinkgelder, falls aktiviert. Diese Beträge werden direkt auf das Sachkonto gebucht, das Sie für bestimmte Vorgangsarten verwenden möchten:

- **Versandkostenkonto**
- **Konto für verkaufte Geschenkkarte**, weitere Informationen unter [Geschenkkarte](synchronize-orders.md#gift-cards)
- **Konto für Trinkgelder**  

Aktivieren Sie **Aufträge automatisch erstellen**, um automatisch Verkaufsaufträge in [!INCLUDE[prod_short](../includes/prod_short.md)] zu erstellen, sobald der Shopify-Auftrag importiert ist.
Der Verkaufsbeleg in [!INCLUDE[prod_short](../includes/prod_short.md)] enthält einen Link zur Shopify- Bestellung. Wenn Sie das Feld **Shopify-Auftragsnummer in Belegzeile** auswählen, werden diese Informationen in den Verkaufszeilen vom Typ *Kommentar* wiederholt.

Im Feld **Steuergebietsquelle** können Sie die Priorität für die Auswahl des Steuergebietscodes oder der MwSt.-Geschäftsbuchungsgruppe basierend auf der Adresse festlegen. Dieser Schritt ist sowohl für Länder mit Umsatzsteuer als auch für Länder mit Mehrwertsteuer relevant. Erfahren Sie mehr unter [Steuerliche Bemerkungen](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Zuordnung von Versandmethoden

Der **Versandartencode** für aus Shopify importierte Verkaufsdokumente kann automatisch ausgefüllt werden. Sie müssen die **Zuordnung von Versandmethoden** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop aus, für den Sie die Zuordnung definieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung von Versandmethoden** aus. Dadurch werden die Datensätze für Versandmethoden, die in den Einstellungen für den [**Versand**](https://www.shopify.com/admin/settings/payments) in Ihrer **Shopify-Verwaltung** definiert sind, automatisch erstellt.
4. Im Feld **Name** sehen Sie den Namen der Versandmethode aus Shopify.
5. Geben Sie den **Versandmethodencode** mit der entsprechenden Versandmethode in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Wenn einem Verkaufsauftrag mehrere Belastungen zugeordnet sind, wird nur eine als Versandart ausgewählt und dem Verkaufsbeleg zugewiesen.

### <a name="payment-method-mapping"></a>Zuordnung der Zahlungsform

Zum Ausfüllen des Felds **Zahlungsformcode** für Verkaufsbelege, die automatisch aus Shopify importiert wurden, müssen Sie **Zuordnung der Zahlungsform** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop aus, für den Sie die Zuordnung definieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung der Zahlungsform** aus.
4. Geben Sie in die Felder **Gateway** und **Kreditkartenfirma** den Namen der Zahlungsmethode aus Shopify ein. Der Datensatz wird automatisch erstellt, wenn Sie Shopify-Bestellungen importieren.
5. Geben Sie den **Zahlungsformcode** mit der entsprechenden Zahlungsform in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.
6. Legen Sie die **Priorität** für den Fall fest, dass der Kunde mehrere Zahlungsmittel verwendet. Im Verkaufsbeleg wird die Zahlungsform mit der höchsten Priorität ausgewählt. Wenn beide Zahlungsformen dieselbe Priorität aufweisen, wird die Zahlungsform mit dem höchsten Betrag verwendet.

> [!NOTE]  
> Bei entsprechender Zahlungsart in [!INCLUDE[prod_short](../includes/prod_short.md)] hat **Bal. Konto Typ** und **Bal. Konto Nr.** ausgefüllt, dann erstellt das Rechnungssystem beim Buchen eine Ausgleichsbuchung der *Zahlung* und wendet sie auf den *Rechnung* Typ in den Kundenbucheintrag ein.

### <a name="location-mapping"></a>Zuordnung von Standorten

Um den **Lagerplatzcode** für aus Shopify importierte Verkaufsdokumente automatisch auszufüllen, müssen Sie die **Shopify Shop-Standorte** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie die Zuordnung der Standorte konfigurieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Standorte**, um die **Shopify Shop-Standorte** zu öffnen.
4. Wählen Sie die Aktion **Shopify Standorte abrufen**, um alle in Shopify definierten Standorte zu importieren. Sie finden sie in den [**Standorte**](https://www.shopify.com/admin/settings/locations)-Einstellungen in Ihrem **Shopify Admin**-Panel. Beachten Sie, dass der als *Standard* markierte Speicherort beim Import von unerfüllten Shopify-Bestellungen verwendet wird.
5. Geben Sie den **Standardlagerplatzcode** mit dem entsprechenden Lagerplatz in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Sie müssen die Zuordnung des Standorts konfigurieren, wenn die Option **Standort obligatorisch** in der Karte **Lagerbestandseinrichtung** aktiviert ist, andernfalls können Sie keine Verkaufsdokumente erstellen.

## <a name="run-the-order-synchronization"></a>Führen Sie die Auftragssynchronisation aus

Nachfolgend wird beschrieben, wie Sie die Verkaufsaufträge importieren und aktualisieren.

> [!NOTE]  
> Archivierte Bestellungen in Shopify können nicht importiert werden. Deaktivieren Sie die Option **Bestellung automatisch archivieren** im Abschnitt **Bestellverarbeitung** der **Checkout**-Einstellungen in Ihrem **Shopify Admin**-Panel, um sicherzustellen, dass alle Bestellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] importiert werden. Wenn Sie archivierte Aufträge importieren müssen, verwenden Sie die Aktion **Auftragsarchivierung aufheben** auf der Seite [Aufträge](https://www.shopify.com/admin/orders) im **Shopify Admin** Bereich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie Bestellungen importieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen** aus.
4. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
5. Definieren Sie bei Bedarf Filter für Bestellungen. Sie können z.B. vollständig bezahlte Bestellungen importieren oder solche mit einem niedrigen Risikoniveau.
6. Wählen Sie die Schaltfläche **OK**.

Alternativ können Sie nach dem Batchauftrag **Aufträge synchronisieren von Shopify** suchen.

Sie können die Aufgabe für eine automatische Ausführung planen. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Importierte Bestellungen überprüfen

Nachdem der Import abgeschlossen wurde, können Sie die Shopify-Bestellung erkunden, wo Sie alle zugehörigen Informationen wie Zahlungsbuchungen, Versandkosten, Risikostufen oder Auftragserfüllungen, wenn die Bestellung schon in Shopify abgeschlossen ist. Sie können auch alle an den Debitor gesendeten Auftragsbestätigungen anzeigen, indem Sie die Aktion **Shopify-Statusseite** auswählen.

> [!NOTE]  
> Sie können direkt zum Fenster **Shopify Bestellungen** navigieren und sehen dort Bestellungen mit dem Status *offen* aus allen Geschäften. Um abgeschlossene Bestellungen zu überprüfen, müssen Sie die Seite **Shopify Bestellungen** aus dem jeweiligen **Shopify Shop Card** Fenster öffnen.

## <a name="create-sales-documents-in-business-central"></a>Verkaufsbelege in Business Central erstellen

Wenn die Option **Automatische Erstellung von Aufträgen** auf der **Shopify Shop Card** aktiviert ist, versucht [!INCLUDE[prod_short](../includes/prod_short.md)] einen Verkaufsbeleg zu erstellen, sobald der Auftrag importiert wurde. Treten Probleme auf, wenn beispielsweise ein fehlender Debitor oder ein Produkt fehlt, müssen Sie das Problem beheben und dann die Bestellung erneut erstellen.

### <a name="to-create-sales-documents"></a>So erstellen Sie Verkaufsbelege

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie Bestellungen synchronisieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen**.
4. Markieren Sie die Bestellung aus, für die Sie einen Verkaufsbeleg erstellen möchten, und wählen Sie die Aktion **Verkaufsbelege erstellen** aus.
5. Wählen Sie **Ja** aus.

Wenn die Shopify Bestellung erfüllt werden muss, wird ein **Verkaufsauftrag** erstellt. Für erfüllte Shopify-Bestellungen, z.B. solche, die nur eine Geschenkkarte enthalten oder die bereits in Shopify behandelt werden, wird eine **Verkaufsrechnung** erstellt.

Ein Verkaufsbeleg ist nun erstellt und kann mit Standarfunktionen von [!INCLUDE[prod_short](../includes/prod_short.md)] verwaltet werden.

### <a name="manage-missing-customers"></a>Fehlende Debitoren verwalten

Wenn Ihre Einstellungen die automatische Erstellung eines Debitors verhindern und kein entsprechender vorhandener Debitor gefunden werden kann, müssen Sie der Shopify-Bestellung manuell einen Debitor zuweisen. Es gibt einige Möglichkeiten, dies zu tun:

- Sie können die **Verk. an Deb.-Nr.** direkt auf der Seite **Shopify-Bestellungen** zuweisen, indem Sie einen Debitor aus der Liste der vorhandenen Debitoren auswählen.
- Sie können einen Kundenvorlagencode auswählen, erstellen und dann den Kunden über die Aktion **Neuen Kunden erstellen** auf der Seite **Shopify Aufträge** zuordnen.
- Sie können einen bestehenden Kunden dem zugehörigen **Shopify Kunden** im Fenster **Shopify Kunden** zuordnen und dann die Aktion **Zuordnung finden** auf der Seite **Shopify Aufträge** wählen.

### <a name="tax-remarks"></a>Anmerkungen zu Steuern

Die importierte Shopify Bestellung enthält Informationen zu Steuern, aber die Steuern werden neu berechnet, wenn Sie den Verkaufsbeleg erstellen, daher ist es wichtig, dass die Mehrwertsteuer-/Steuereinstellungen korrekt sind [!INCLUDE[prod_short](../includes/prod_short.md)].

- Mehrere Produktsteuer-/MwSt.-Steuersätze. Beispielsweise unterliegen einige Produktkategorien ermäßigten Steuersätzen. Diese Artikel müssen in [!INCLUDE[prod_short](../includes/prod_short.md)] vorhanden und Shopify-Produkten zugeordnet sein. Andernfalls wird bei der automatischen Erstellung fehlender Artikel die MwSt-Produktbuchungsgruppe verwendet.

- Adressabhängige Steuersätze. Verwenden Sie das Feld **Steuergebiet Priorität** zusammen mit der Tabelle **Kundenvorlagen**, um die Standardlogik zu überschreiben, die den **Steuergebietscode** im Verkaufsdokument ausfüllt. Das Feld **Steuergebiet Priorität** gibt die Priorität an, mit der die Informationen über das Land/die Region und den Staat/die Provinz übernehmen soll. Dann wird der entsprechende Datensatz in den Kundenvorlagen Shopify gefunden und die **Steuerkennziffer**, **Steuerpflichtig** und **MwSt Bus. Buchungsgruppe** werden verwendet, wenn ein Verkaufsbeleg erstellt wird.

- Preis einschließlich Steuer. Das Feld **Preise inkl. MwSt.**/**Preise inkl. MwSt.** im erstellten Verkaufsdokument hängt nicht vom Kunden ab, sondern von der **Kundenvorlage** aus der **Shopify Shop-Karte** oder der Kundenvorlage pro Land.

### <a name="impact-of-order-editing"></a>Auswirkung der Bearbeitung von Bestellungen

In Shopify:

|Bearbeiten|Auswirkungen|
|------|-----------|
|Den Erfüllungsort ändern | Der ursprüngliche Standort wird mit [!INCLUDE[prod_short](../includes/prod_short.md)] synchronisiert. |
|Bearbeiten Sie eine Bestellung und ändern Sie die Menge| Der Auftragskopf und die Zusatztabellen werden in [!INCLUDE[prod_short](../includes/prod_short.md)] aktualisiert, die Zeilen nicht. |
|Bearbeiten Sie eine Bestellung und fügen Sie einen neuen Artikel hinzu | Der Auftragskopf wird aktualisiert, die Zeilen nicht. |

In [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Bearbeiten|Auswirkungen|
|------|-----------|
|Ändern Sie den Standort in einen anderen Standort, der den Shopify Orten zugeordnet ist. Sendung buchen. | Nach der Synchronisierung der Erfüllung wird der Ort in Shopify aktualisiert. |
|Ändern Sie den Ort in einen anderen Ort, der nicht den Shopify Orten zugeordnet ist. Sendung buchen. | Die Erfüllung wird nicht mit Shopify synchronisiert. |
|Ändern der Abnahmemenge. Sendung buchen. | Die Reihenfolge Shopify wird als teilweise erfüllt gekennzeichnet. |
|Ein neues Element hinzufügen. Sendung buchen. | Die Reihenfolge Shopify wird als erfüllt markiert. Die Zeilen werden nicht aktualisiert. |

## <a name="synchronize-shipments-to-shopify"></a>Lieferungen mit Shopify synchronisieren

Wenn ein Verkaufsauftrag, der aus einem Shopify-Auftrag erstellt wurde, versandt wird, können Sie die Sendungen mit Shopify synchronisieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Sendungen mit Shopify synchronisieren** ein und wählen Sie dann den zugehörigen Link.
2. Definieren Sie die Filter für Sendungen nach Bedarf. Sie können zum Beispiel eine Sendung aktualisieren, die zu einem bestimmten Datum gebucht wurde.
3. Wählen Sie die Schaltfläche **OK**.

Die Bestellung in Shopify wird als erfüllt markiert. Der Debitor erhält automatisch eine Versandbenachrichtigung per E-Mail oder Textnachricht (SMS). Wenn ein Zusteller und ein Verfolgungscode für die Lieferung angegeben sind, sind die Verfolgungsinformationen in der E-Mail enthalten.

> [!NOTE]  
> Denken Sie daran, **Bestellungen aus Shopify** auszuführen, um den Erfüllungsstatus der Bestellung in [!INCLUDE[prod_short](../includes/prod_short.md)] zu aktualisieren. Mithilfe der Konnektorfunktionen werden auch vollständig bezahlte und erfüllte Bestellungen in Shopify und in [!INCLUDE[prod_short](../includes/prod_short.md)] archiviert, sofern die entsprechenden Bedingungen erfüllt sind.

### <a name="shipping-agents-and-tracking-url"></a>Zusteller und Verfolgungs-URL

Wenn das Dokument **Gebuchte Verkaufslieferung** den **Versandagentencode** und/oder die **Paketverfolgungsnummer** enthält, werden diese Informationen an Shopify und an den Kunden in der Versandbestätigungs-E-Mail gesendet.

Die verfolgende Firma wird auf der Grundlage des Datensatzes des Zustellers mit der folgenden Folge (von oben nach unten) eingetragen:

- **Shopify-Nachverfolgungsunternehmen**
- **Name**
- **Code**

Wenn das Feld **Paketverfolgungs-URL** für den Datensatz des Zustellers ausgefüllt ist, dann enthält die Versandbestätigung ebenfalls eine Verfolgungs-URL.

## <a name="gift-cards"></a>Geschenkkarten

Im Shopify-Shop können Sie Geschenkgutscheine verkaufen, mit denen echte Produkte bezahlt werden können.

Wenn Sie mit Geschenkkarten arbeiten, ist es wichtig, dass Sie im Fenster **Shopify Shop-Karte** einen Wert in das Feld **Geschenkkartenkonto** eingeben. Die verkaufte Geschenkkarte wird zusammen mit den entsprechenden Bestellungen synchronisiert. Eine angewendete Geschenkkarte wird ebenfalls mit der Bestellung importiert, jetzt jedoch als Transaktion. Beachten Sie, dass die Geschenkkarte den Rechnungsbetrag nicht reduziert.

Um die ausgestellten und verwendeten Geschenkkarten zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Geschenkkarten** ein, und wählen Sie dann den entsprechende Link aus.

## <a name="transactions-and-payouts"></a>Transaktionen und Auszahlungen

Wenn ein Kunde seinen Checkout im Online-Shop abschließt, werden die Informationen zu Zahlungen als **Transaktion** gespeichert. Mit der Bestellung können mehrere Transaktionen verknüpft sein, z. B. wenn ein Kunde eine Geschenkkarte verwendet, um einen Teil der Kosten zu bezahlen, und dann eine Kreditkarte oder PayPal für den Restbetrag verwendet. 

Wenn Sie Shopify Zahlung als Zahlungsanbieter verwenden, dann können Sie neben Informationen über Gelder, die der Kunde vom Zahlungsanbieter erhalten hat, auch Auszahlungen von Shopify auf Ihr Bankkonto sehen. 

### <a name="transactions"></a>Transaktionen

Die Transaktionen, die in Shopify stattfinden, werden mit den Aufträgen synchronisiert und können auf der Seite *Shopify Aufträge* eingesehen werden.

Um alle Transaktionen zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](../media/ui-search/search_small.png "Was möchten Sie tun?"). aus, geben Sie **Transaktionen** ein, und wählen Sie den entsprechenden Link aus.

Wenn Sie die Zahlungsmethodenzuordnung konfiguriert haben, wird dem erstellten Verkaufsbeleg ein Zahlungsmethodencode zugewiesen. Erfahren Sie mehr unter [Zuordnung von Zahlungsmethoden](#payment-method-mapping).

### <a name="payouts"></a>Auszahlungen

Wenn für Ihren Store Shopify Payment verwendet wird, erhalten Sie Zahlungen durch *Shopify-Auszahlungen*, wenn ein Debitor mit Shopify Payments und beschleunigten Checkouts bezahlt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie Auszahlungen synchronisieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Auszahlungen synchronisieren** aus.

Um alle Auszahlungen zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Auszahlungen** ein, und wählen Sie den entsprechenden Link aus.

**Auszahlungen** dienen nur zu Informationszwecken und wirken sich nicht auf das Hauptbuch oder das Bankbuch aus, können jedoch hilfreich sein, wenn Sie Ihren Kontoauszug bearbeiten.

## <a name="see-also"></a>Siehe auch

[Einstieg mit dem Konnektor für Shopify](get-started.md)  
