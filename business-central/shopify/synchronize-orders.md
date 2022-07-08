---
title: Verkaufsaufträge synchronisieren und erfüllen
description: Nehmen Sie die Einrichtung und Ausführung des Imports under der Verarbeitung von Verkaufsaufträgen über Shopify vor.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ce11aa8766550e72cab2f811ef6602dba4271211
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076305"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Verkaufsaufträge synchronisieren und erfüllen

Dieser Artikel beschreibt die notwendigen Einstellungen und Schritte, die Sie durchführen müssen, um Verkaufsaufträge von Shopify in [!INCLUDE[prod_short](../includes/prod_short.md)] zu synchronisieren und zu erfüllen.

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Legen Sie den Import von Bestellungen auf der Shopify Shop-Karte fest.

Zu einer regulären Shopify-Bestellung können zusätzliche Beträge hinzukommen, darunter Versandkosten oder Trinkgelder, falls aktiviert. Diese Beträge werden dann direkt auf die Sachkonten gebucht. Wählen Sie das Sachkonto aus, das für bestimmte Transaktionen verwendet werden soll:

- **Versandkostenkonto**
- **Konto für verkaufte Geschenkkarte**, für weitere Informationen finden Sie unter [Geschenkkarte](synchronize-orders.md#gift-cards).
- **Konto für Trinkgelder**  

Aktivieren Sie **Aufträge automatisch erstellen**, um automatisch Verkaufsaufträge in [!INCLUDE[prod_short](../includes/prod_short.md)] zu erstellen, sobald der Shopify-Auftrag importiert ist.
Der Verkaufsbeleg in [!INCLUDE[prod_short](../includes/prod_short.md)] enthält einen Link zur Shopify- Bestellung. Wenn Sie das Feld **Shopify Bestellnr. auf Dok. Zeile** wählen, wird diese Information in den Verkaufszeilen des Typs *Kommentar* wiederholt.

Im Feld **Steuergebietsquelle** können Sie die Priorität für die Auswahl des Steuergebietscodes oder der MwSt.-Geschäftsbuchungsgruppe basierend auf der Adresse definieren. Dieser Schritt ist für Länder mit Mehrwertsteuer relevant, kann aber für MwSt.-Länder verwendet werden. Weitere Informationen finden Sie unter [Anmerkungen zu Steuern](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Zuordnung von Versandmethoden

Der **Versandartencode** für aus Shopify importierte Verkaufsdokumente kann automatisch ausgefüllt werden. Sie müssen die **Zuordnung von Versandmethoden** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop aus, für den Sie die Zuordnung definieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung von Versandmethoden** aus. Die Datensätze für Versandmethoden, die in den Einstellungen für den [**Versand**](https://www.shopify.com/admin/settings/payments) in Ihrer **Shopify-Verwaltung** definiert sind, werden automatisch erstellt.
4. Im Feld **Name** sehen Sie den Namen der Versandmethode aus Shopify.
5. Geben Sie den **Versandmethodencode** mit der entsprechenden Versandmethode in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Wenn einem Verkaufsauftrag mehrere Belastungen zugeordnet sind, wird nur eine als Versandart ausgewählt und dem Verkaufsbeleg zugewiesen.

### <a name="payment-method-mapping"></a>Zuordnung der Zahlungsform

Um den **Zahlungsartencode** für aus Shopify importierte Verkaufsdokumente automatisch auszufüllen, müssen Sie die **Zahlungsartenzuordnung** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop aus, für den Sie die Zuordnung definieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung der Zahlungsform** aus.
4. Geben Sie in die Felder **Gateway** und **Kreditkartenfirma** den Namen der Zahlungsmethode aus Shopify ein. Der Datensatz wird automatisch erstellt, wenn Sie Shopify-Bestellungen importieren.
5. Geben Sie den **Zahlungsformcode** mit der entsprechenden Zahlungsform in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.
6. Legen Sie die **Priorität** für den Fall fest, dass der Kunde mehrere Zahlungsmittel verwendet. Im Verkaufsbeleg wird die Zahlungsform mit der höchsten Priorität ausgewählt. Wenn beide Zahlungsformen dieselbe Priorität aufweisen, wird die Zahlungsform mit dem höchsten Betrag verwendet.

### <a name="location-mapping"></a>Zuordnung von Standorten

Um den **Lagerplatzcode** für aus Shopify importierte Verkaufsdokumente automatisch auszufüllen, müssen Sie die **Shopify Shop-Standorte** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie die Zuordnung der Standorte konfigurieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Standorte**, um die **Shopify Shop-Standorte** zu öffnen.
4. Wählen Sie die Aktion **Shopify Standorte abrufen**, um alle in Shopify definierten Standorte zu importieren. Sie finden sie in den [**Standorte**](https://www.shopify.com/admin/settings/locations)-Einstellungen in Ihrem **Shopify Admin**-Panel. Beachten Sie, dass der als *Standard* markierte Speicherort beim Import von unerfüllten Shopify-Bestellungen verwendet wird.
5. Geben Sie den **Standardlagerplatzcode** mit dem entsprechenden Lagerplatz in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Sie müssen die Zuordnung des Standorts konfigurieren, wenn die Option **Standort obligatorisch** in der Karte **Lagerbestandseinrichtung** aktiviert ist, sonst können Sie keine Verkaufsdokumente erstellen.

## <a name="run-the-order-synchronization"></a>Führen Sie die Auftragssynchronisation aus

Nachfolgend wird beschrieben, wie Sie die Verkaufsaufträge importieren und aktualisieren.

> [!NOTE]  
> Archivierte Bestellungen in Shopify können nicht importiert werden. Deaktivieren Sie die Option **Bestellung automatisch archivieren** im Abschnitt **Bestellverarbeitung** der **Checkout**-Einstellungen in Ihrem **Shopify Admin**-Panel, um sicherzustellen, dass alle Bestellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] importiert werden. Wenn Sie archivierte Aufträge importieren müssen, verwenden Sie die Aktion **Auftragsarchivierung aufheben** auf der Seite [Aufträge](https://www.shopify.com/admin/orders) im Admin-Panel Shopify.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie Bestellungen importieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen** aus.
4. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
5. Definieren Sie bei Bedarf Filter für Bestellungen. Sie können z.B. vollständig bezahlte Bestellungen importieren oder solche mit einem niedrigen Risikoniveau.
6. Wählen Sie die Schaltfläche **OK**.

Alternativ können Sie nach dem Batchauftrag **Aufträge synchronisieren von Shopify** suchen.

Sie können die Aufgabe für eine automatische Ausführung planen. Weitere Informationen finden Sie unter [Wiederkehrende Aufgaben planen](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Importierte Bestellungen überprüfen

Sobald der Import abgeschlossen ist, können Sie die Shopify-Bestellung erkunden und alle zugehörigen Informationen finden. Suchen Sie beispielsweise die Zahlungstransaktionen, Versandkosten, Risikostufe oder Auftragserfüllungen, wenn die Bestellung bereits in Shopify ausgeführt wurde. Sie können auch alle an den Debitor gesendeten Auftragsbestätigungen anzeigen, indem Sie die Aktion **Shopify-Statusseite** auswählen.

> [!NOTE]  
> Sie können direkt zum Fenster **Shopify Bestellungen** navigieren und sehen dort Bestellungen mit dem Status *offen* aus allen Geschäften. Um abgeschlossene Bestellungen zu überprüfen, müssen Sie die Seite **Shopify Bestellungen** aus dem jeweiligen **Shopify Shop Card** Fenster öffnen.

## <a name="create-sales-documents-in-business-central"></a>Verkaufsbelege in Business Central erstellen

Wenn die Option **Automatische Erstellung von Aufträgen** auf der **Shopify Shop Card** aktiviert ist, versucht [!INCLUDE[prod_short](../includes/prod_short.md)] einen Verkaufsbeleg zu erstellen, sobald der Auftrag importiert wurde. Treten während des Prozesses Probleme auf, wenn beispielsweise ein Debitor oder ein Produkt fehlt, müssen Sie das Problem beheben. Sie können dann versuchen, den Verkaufsauftrag erneut zu erstellen.

### <a name="to-create-sales-documents"></a>So erstellen Sie Verkaufsbelege

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie Bestellungen synchronisieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen**.
4. Markieren Sie die Bestellung aus, für die Sie einen Verkaufsbeleg erstellen möchten, und wählen Sie die Aktion **Verkaufsbelege erstellen** aus.
5. Wählen Sie **Ja** aus.

Wenn die Shopify Bestellung erfüllt werden muss, wird ein **Verkaufsauftrag** erstellt. Für erfüllte Shopify-Bestellungen, z.B. solche, die nur eine Geschenkkarte enthalten oder die bereits in Shopify behandelt werden, wird eine **Verkaufsrechnung** erstellt.

Ein Verkaufsbeleg ist nun erstellt und kann mit den Standarfunktionen von [!INCLUDE[prod_short](../includes/prod_short.md)] verwaltet werden.

### <a name="manage-missing-customers"></a>Fehlende Debitoren verwalten

Wenn Ihre Einstellungen die automatische Erstellung eines Debitors verhindern und kein entsprechender vorhandener Debitor gefunden werden kann, weisen Sie der Shopify-Bestellung manuell einen Debitor zu. Es sind einige Optionen verfügbar:

- Sie können die **Verk. an Deb.-Nr.** direkt in der **Shopify-Bestellung** zuweisen, indem Sie einen Debitor aus der Liste der vorhandenen Debitoren auswählen.
- Sie können einen Kundenvorlagencode auswählen, erstellen und den Kunden über die Aktion **Neuen Kunden erstellen** auf der Seite **Shopify Aufträge** zuordnen.
- Sie können einen bestehenden Kunden dem zugehörigen **Shopify Kunden** im Fenster **Shopify Kunden** zuordnen und dann die Aktion **Zuordnung finden** auf der Seite **Shopify Aufträge** wählen.

### <a name="tax-remarks"></a>Anmerkungen zu Steuern

Während die importierte Shopify-Bestellung Informationen zu Steuern enthält, werden die Steuern neu berechnet, wenn Sie den Verkaufsbeleg erstellen. Durch diese Neuberechnung ist es wichtig, dass die Einstellungen für Mehrwertsteuer/Steuern in [!INCLUDE[prod_short](../includes/prod_short.md)] richtig sind.

- Mehrere Produktsteuer-/MwSt.-Sätze. Beispielsweise unterliegen einige Produktkategorien ermäßigten Steuersätzen. Diese Artikel müssen in [!INCLUDE[prod_short](../includes/prod_short.md)] vorhanden und Shopify-Produkten zugeordnet sein. Andernfalls wird bei der automatischen Erstellung fehlender Artikel die MwSt-Produktbuchungsgruppe verwendet.

- Adressabhängige Steuersätze. Verwenden Sie das Feld **Steuergebiet Priorität** zusammen mit der Tabelle **Kundenvorlagen**, um die Standardlogik zu überschreiben, die den **Steuergebietscode** im Verkaufsdokument ausfüllt. Das Feld **Steuergebiet Priorität** gibt die Priorität an, aus der die Funktion die Informationen über das Land/die Region und den Staat/die Provinz übernehmen soll. Dann wird der entsprechende Datensatz in den Kundenvorlagen Shopify gefunden und die **Steuerkennziffer**, **Steuerpflichtig** und **MwSt Bus. Buchungsgruppe** wird verwendet, wenn ein Verkaufsbeleg erstellt wird.

- Preis einschließlich Steuer. Das Feld **Preise inkl. MwSt.**/**Preise inkl. MwSt.** im erstellten Verkaufsdokument hängt nicht vom Kunden ab, sondern von der **Kundenvorlage** aus der Shopify Shop-Karte oder der Kundenvorlage pro Land.

### <a name="impact-of-edits-of-orders"></a>Auswirkung der Bearbeitung von Bestellungen

|Bearbeiten|Auswirkungen|
|------|-----------|
|In Shopify, ändern Sie den Erfüllungsort | Der ursprüngliche Standort wird mit [!INCLUDE[prod_short](../includes/prod_short.md)] synchronisiert. |
|In Shopify, bearbeiten Sie eine Bestellung und ändern Sie die Menge.| Der Auftragskopf und die Zusatztabellen werden in [!INCLUDE[prod_short](../includes/prod_short.md)] aktualisiert, die Zeilen nicht. |
|In Shopify, bearbeiten Sie eine Bestellung und fügen Sie einen neuen Artikel hinzu. | Der Auftragskopf wird aktualisiert, die Zeilen nicht. |
|Ändern Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] den Ort in einen anderen Ort, der den Shopify Orten zugeordnet ist. Sendung buchen. | Nach der Synchronisierung der Erfüllung wird der Ort in Shopify aktualisiert. |
|In [!INCLUDE[prod_short](../includes/prod_short.md)], ändern Sie den Ort in einen anderen Ort, der nicht den Shopify Orten zugeordnet ist. Sendung buchen. | Die Erfüllung wird nicht mit Shopify synchronisiert. |
|Ändern Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] die Abnahmemenge. Sendung buchen. | Die Reihenfolge Shopify wird als teilweise erfüllt gekennzeichnet. |
|Fügen Sie in [!INCLUDE[prod_short](../includes/prod_short.md)] ein neues Element hinzu. Sendung buchen. | Die Reihenfolge Shopify wird als erfüllt markiert. Die Zeilen werden nicht aktualisiert. |

## <a name="synchronize-shipments-to-shopify"></a>Lieferungen mit Shopify synchronisieren

Wenn ein Verkaufsauftrag, der aus einem Shopify-Auftrag erstellt wurde, versandt wird, können Sie die Sendungen mit Shopify synchronisieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Sendungen mit Shopify synchronisieren** ein und wählen Sie dann den zugehörigen Link.
2. Definieren Sie die Filter für Sendungen nach Bedarf. Sie können zum Beispiel eine Sendung aktualisieren, die zu einem bestimmten Datum gebucht wurde.
3. Wählen Sie die Schaltfläche **OK**.

Die Bestellung in Shopify wird als erfüllt markiert. Der Debitor erhält automatisch eine Versandbenachrichtigung per E-Mail oder Textnachricht (SMS). Wenn ein Zusteller und ein Verfolgungscode für die Lieferung angegeben sind, sind die Verfolgungsinformationen in der E-Mail enthalten.

> [!NOTE]  
> Denken Sie daran, **Bestellungen aus Shopify** auszuführen, um den Erfüllungsstatus der Bestellung in [!INCLUDE[prod_short](../includes/prod_short.md)] zu aktualisieren. Mithilfe der Konnektorfunktionen werden auch vollständig bezahlte und erfüllte Bestellungen in Shopify und in [!INCLUDE[prod_short](../includes/prod_short.md)] archiviert, sofern die entsprechenden Bedingungen erfüllt sind.

### <a name="shipping-agents-and-tracking-url"></a>Zusteller und Verfolgungs-URL

Wenn das Dokument **Gebuchte Verkaufslieferung** den **Versandagentencode** und/oder die **Paketverfolgungsnummer** enthält, werden diese Informationen an Shopify und an den Endkunden in der Versandbestätigungs-E-Mail gesendet.

Die verfolgende Firma wird auf der Grundlage des Datensatzes des Zustellers mit den folgenden Prioritäten (von oben nach unten) eingetragen:

- **Shopify-Nachverfolgungsunternehmen**
- **Name**
- **Code**

Wenn das Feld **Paketverfolgungs-URL** für den Datensatz des Zustellers ausgefüllt ist, dann enthält die Versandbestätigung ebenfalls eine Verfolgungs-URL.

## <a name="gift-cards"></a>Geschenkkarten

Im Shopify-Shop können Sie Geschenkgutscheine verkaufen, mit denen später echte Produkte bezahlt werden können.

Wenn Sie mit Geschenkkarten arbeiten, ist es wichtig, dass Sie im Fenster **Shopify Shop-Karte** einen Wert in das Feld **Geschenkkartenkonto** eingeben. Die verkaufte Geschenkkarte wird zusammen mit den entsprechenden Bestellungen synchronisiert. Eine angewendete Geschenkkarte wird ebenfalls mit der Bestellung importiert, jetzt jedoch als Transaktion. Beachten Sie, dass die Geschenkkarte den Rechnungsbetrag nicht reduziert.

Um die ausgestellten und verwendeten Geschenkkarten zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Geschenkkarten** ein, und wählen Sie dann den entsprechende Link aus.

## <a name="transactions"></a>Transaktionen

Die Transaktionen, die bei Shopify stattgefunden haben, werden mit den Aufträgen synchronisiert und können auf der Seite *Shopify Aufträge* eingesehen werden.

Um alle Transaktionen zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 1.](../media/ui-search/search_small.png "Was möchten Sie tun?"). aus, geben Sie **Transaktionen** ein, und wählen Sie den entsprechenden Link aus.

## <a name="payouts"></a>Auszahlungen

Wenn für Ihren Store Shopify Payments aktiviert sind, erhalten Sie Zahlungen durch *Shopify-Auszahlungen*, wenn ein Debitor mit Shopify Payments und beschleunigten Checkouts bezahlt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Shop, für den Sie Auszahlungen synchronisieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Auszahlungen synchronisieren** aus.

Um alle Auszahlungen zu überprüfen, wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Auszahlungen** ein, und wählen Sie den entsprechenden Link aus.

## <a name="see-also"></a>Siehe auch

[Einstieg mit dem Konnektor für Shopify](get-started.md)  
