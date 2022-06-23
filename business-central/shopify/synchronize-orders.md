---
title: Verkaufsaufträge synchronisieren und erfüllen
description: Nehmen Sie die Einrichtung und Ausführung des Imports under der Verarbeitung von Verkaufsaufträgen über Shopify vor.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 4e8d640f6de61d642037a55fdfeb09e32f197a96
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809013"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Verkaufsaufträge synchronisieren und erfüllen

In diesem Artikel werden die notwendigen Einstellungen und Schritte beschrieben, die für die Synchronisierung und Erfüllung von Verkaufsaufträgen erforderlich sind.

## <a name="set-import-of-orders-on-the-shopify-shop-card"></a>Import von Bestellungen auf der Shopify-Shop-Karte festlegen

Zu einer regulären Shopify-Bestellung können zusätzliche Beträge hinzukommen, darunter Versandkosten oder Trinkgelder, falls aktiviert. Diese Beträge werden direkt auf Sachkonten gebucht. Wählen Sie das Sachkonto aus, das für bestimmte Transaktionen verwendet werden soll:

- **Versandkostenkonto**
- **Konto für verkaufte Geschenkkarte**, für weitere Informationen finden Sie unter [Geschenkkarte](synchronize-orders.md#gift-cards).
- **Konto für Trinkgelder**  

Aktivieren Sie **Bestellungen automatisch erstellen**, um Verkaufsbelege automatisch in [!INCLUDE[prod_short](../includes/prod_short.md)] zu erstellen, nachdem die Shopify-Bestellung importiert wurde.
Der Verkaufsbeleg in [!INCLUDE[prod_short](../includes/prod_short.md)] enthält einen Link zur Shopify- Bestellung. Wenn Sie das Feld **Shopify-Auftragsnummer in Belegzeile** auswählen, werden diese Informationen in den Verkaufszeilen vom Typ *Kommentar* wiederholt.

Im Feld **Steuergebietsquelle** können Sie die Priorität für die Auswahl des Steuergebietscodes oder der MwSt.-Geschäftsbuchungsgruppe basierend auf der Adresse definieren. Dieser Schritt ist für Länder mit Mehrwertsteuer relevant, kann aber für MwSt.-Länder verwendet werden. Weitere Informationen finden Sie unter [Anmerkungen zu Steuern](synchronize-orders.md#tax-remarks).

### <a name="shipment-method-mapping"></a>Zuordnung von Versandmethoden

Der **Versandmethodencode** für Verkaufsbelege, die aus Shopify wurden, kann automatisch ausgefüllt werden. Sie müssen **Zuordnung von Versandmethoden** konfigurieren.

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie die Zuordnung definieren möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung von Versandmethoden** aus. Die Datensätze für Versandmethoden, die in den Einstellungen für den [**Versand**](https://www.shopify.com/admin/settings/payments) in Ihrer **Shopify-Verwaltung** definiert sind, werden automatisch erstellt.
4. Im Feld **Name** können Sie den Namen der Versandmethode über Shopify anzeigen.
5. Geben Sie den **Versandmethodencode** mit der entsprechenden Versandmethode in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Wenn mehrere Versandkosten mit einem Verkaufsauftrag verknüpft sind, wird nur eine als Versandmethode ausgewählt und dem Verkaufsbeleg zugewiesen.

### <a name="payment-method-mapping"></a>Zuordnung der Zahlungsform

Zum Ausfüllen des Felds **Zahlungsformcode** für Verkaufsbelege, die automatisch aus Shopify importiert wurden, müssen Sie **Zuordnung der Zahlungsform** konfigurieren.

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie die Zuordnung definieren möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung der Zahlungsform** aus.
4. Geben Sie in den Feldern **Gateway** und **Kreditkartenunternehmen** den Namen der Zahlungsform über Shopify ein. Der Datensatz wird automatisch erstellt, wenn Sie Shopify-Bestellungen importieren.
5. Geben Sie den **Zahlungsformcode** mit der entsprechenden Zahlungsform in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.
6. Legen Sie die **Priorität** für Fälle fest, in denen der Debitor mehrere Zahlungsmittel verwendet. Im Verkaufsbeleg wird die Zahlungsform mit der höchsten Priorität ausgewählt. Wenn beide Zahlungsformen dieselbe Priorität aufweisen, wird die Zahlungsform mit dem höchsten Betrag verwendet.

## <a name="run-order-synchronization"></a>Bestellungssynchronisierung ausführen

Nachfolgend wird beschrieben, wie Sie die Verkaufsaufträge importieren und aktualisieren.

> [!NOTE]  
> Archivierte Bestellungen in Shopify können nicht importiert werden. Deaktivieren Sie **Bestellung automatisch archivieren** im Abschnitt **Auftragsabwicklung** in den Einstellungen für die **Kasse** in Ihrer **Shopify-Verwaltung**, um sicherzustellen, dass alle Bestellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] importiert werden. Wenn Sie archivierte Bestellungen importieren müssen, verwenden Sie die Aktion **Archivierung von Bestellungen aufheben** auf der Seite [Bestellungen](https://www.shopify.com/admin/orders) der Shopify-Verwaltung.

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie die Bestellungen importieren möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen** aus.
4. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
5. Definieren Sie bei Bedarf Filter für Bestellungen. Sie können beispielsweise vollständig bezahlte Bestellungen oder solche mit geringem Risiko importieren.
6. Wählen Sie die Schaltfläche **OK**.

Alternativ können Sie nach dem Stapelverarbeitungsauftrag **Bestellungen aus Shopify synchronisieren** suchen.

Sie können die durchzuführende Aufgabe so planen, dass sie automatisiert ausgeführt werden. Weitere Informationen finden Sie unter [Wiederkehrende Aufgaben planen](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Importierte Bestellungen überprüfen

Sobald der Import abgeschlossen ist, können Sie die Shopify-Bestellung erkunden und alle zugehörigen Informationen finden. Suchen Sie beispielsweise die Zahlungstransaktionen, Versandkosten, Risikostufe oder Auftragserfüllungen, wenn die Bestellung bereits in Shopify ausgeführt wurde. Sie können auch alle an den Debitor gesendeten Auftragsbestätigungen anzeigen, indem Sie die Aktion **Shopify-Statusseite** auswählen.

> [!NOTE]  
> Sie können direkt zum Fenster **Shopify-Bestellungen** navigieren und Bestellungen mit dem Status *offen* aus allen Shops anzeigen. Um abgeschlossene Bestellungen zu überprüfen, müssen Sie die Seite **Shopify-Bestellungen** über das spezifische Fenster **Shopify-Shop-Karte** öffnen.

## <a name="create-sales-documents-in-business-central"></a>Verkaufsbelege in Business Central erstellen

Wenn der Umschalter **Bestellungen automatisch erstellen** auf der **Shopify-Shop-Karte** aktiviert ist, versucht [!INCLUDE[prod_short](../includes/prod_short.md)], einen Verkaufsbeleg zu erstellen, nachdem die Bestellung importiert wurde. Treten während des Prozesses Probleme auf, wenn beispielsweise ein Debitor oder ein Produkt fehlt, müssen Sie das Problem beheben. Sie können dann versuchen, den Verkaufsauftrag erneut zu erstellen.

### <a name="to-create-sales-documents"></a>So erstellen Sie Verkaufsbelege

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Was möchten Sie tun?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie Bestellungen synchronisieren möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen** aus.
4. Markieren Sie die Bestellung aus, für die Sie einen Verkaufsbeleg erstellen möchten, und wählen Sie die Aktion **Verkaufsbelege erstellen** aus.
5. Wählen Sie **Ja** aus.

Wenn die Shopify-Bestellung ausgefüllt werden muss, wird der **Verkaufsauftrag** erstellt. Für vollständig ausgefüllte Shopify-Bestellungen, z. B. Bestellungen, die nur einen Geschenkgutschein enthalten oder die bereits in Shopify bearbeitet wurden, wird die **Verkaufsrechnung** erstellt.

Ein Verkaufsbeleg ist nun erstellt und kann mit den Standarfunktionen von [!INCLUDE[prod_short](../includes/prod_short.md)] verwaltet werden.

### <a name="manage-missing-customers"></a>Fehlende Debitoren verwalten

Wenn Ihre Einstellungen die automatische Erstellung eines Debitors verhindern und kein entsprechender vorhandener Debitor gefunden werden kann, weisen Sie der Shopify-Bestellung manuell einen Debitor zu. Es sind einige Optionen verfügbar:

- Sie können die **Verk. an Deb.-Nr.** direkt in der **Shopify-Bestellung** zuweisen, indem Sie einen Debitor aus der Liste der vorhandenen Debitoren auswählen.
- Sie können einen Debitorenvorlagencode auswählen, erstellen und den entsprechenden Debitor über die Aktion **Neuen Debitor erstellen** in der **Shopify-Bestellung** zuweisen.
- Sie können einen vorhandenen Debitor dem zugehörigen **Shopify-Debitor** im Fenster **Shopify-Debitoren** zuordnen und anschließend die Aktion **Zuordnung suchen** in der **Shopify-Bestellung** auswählen.

### <a name="tax-remarks"></a>Anmerkungen zu Steuern

Während die importierte Shopify-Bestellung Informationen zu Steuern enthält, werden die Steuern neu berechnet, wenn Sie den Verkaufsbeleg erstellen. Für die Neuberechnung ist es wichtig, dass die Mehrwertsteuer-/Steuereinstellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] korrekt sind.

- Mehrere Produktsteuer-/MwSt.-Sätze. Beispielsweise unterliegen einige Produktkategorien ermäßigten Steuersätzen. Diese Artikel müssen in [!INCLUDE[prod_short](../includes/prod_short.md)] vorhanden und Shopify-Produkten zugeordnet sein. Andernfalls wird bei der automatischen Erstellung fehlender Artikel die MwSt-Produktbuchungsgruppe verwendet.

- Adressabhängige Steuersätze. Verwenden Sie das Feld **Priorität des Steuergebiets** zusammen mit der Tabelle **Debitorenvorlagen**, um die Standardlogik zu überschreiben, die im **Steuergebietscode** des Verkaufsbelegs ausgefüllt wird. Das Feld **Priorität des Steuergebiets** legt die Priorität fest, mit der die Funktion Informationen über Land/Region und Bundesland/Provinz beziehen soll. Anschließend befindet sich der entsprechende Datensatz in den Shopify-Debitorenvorlagen und ein Verkaufsbeleg wird mit **Steuergebietscode**, **Steuerpflichtig** und **MwSt.-Produktbuchungsgruppe** erstellt.

## <a name="synchronize-shipments-to-shopify"></a>Lieferungen mit Shopify synchronisieren

Wenn ein Verkaufsauftrag, der über eine Shopify-Bestellung erstellt wurde, geliefert wird, können Sie die Lieferungen mit Shopify synchronisieren.

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Was möchten Sie tun?") , geben Sie **Lieferungen mit Shopify synchronisieren** ein, und wählen Sie dann den zugehörigen Link aus.
2. Definieren Sie bei Bedarf Filter für Lieferungen. Sie können beispielsweise Lieferungen aktualisieren, die zu einem bestimmten Datum gebucht wurden.
3. Wählen Sie die Schaltfläche **OK**.

Die Bestellung in Shopify wird als erfüllt markiert. Der Debitor erhält automatisch eine Versandbenachrichtigung per E-Mail oder Textnachricht (SMS). Wenn ein Zusteller und ein Verfolgungscode für die Lieferung angegeben sind, sind die Verfolgungsinformationen in der E-Mail enthalten.

> [!NOTE]  
> Denken Sie daran, die Aktion **Bestellungen über Shopify synchronisieren** auszuführen, um den Erfüllungsstatus der Bestellung in [!INCLUDE[prod_short](../includes/prod_short.md)] zu aktualisieren. Mithilfe der Konnektorfunktionen werden auch vollständig bezahlte und erfüllte Bestellungen in Shopify und in [!INCLUDE[prod_short](../includes/prod_short.md)] archiviert, sofern die entsprechenden Bedingungen erfüllt sind.

### <a name="shipping-agents-and-tracking-url"></a>Zusteller und Verfolgungs-URL

Wenn das Dokument **Geb. Verkaufslieferung** den **Zustellercode** und/oder die **Paketverfolgungsnr.** enthält, werden diese Informationen an Shopify und an den Endkunden in der Versandbestätigungs-E-Mail gesendet.

Das Nachverfolgungsunternehmen wird basierend auf dem Zustellerdatensatz mit den folgenden Prioritäten (von der höchsten zur niedrigsten) ausgefüllt:

- **Shopify-Nachverfolgungsunternehmen**
- **Name**
- **Code**

Wenn das Feld **Paketverfolgungs-URL** für den Zustellerdatensatz ausgefüllt ist, enthält die Versandbestätigung auch eine Nachverfolgungs-URL.

## <a name="gift-cards"></a>Geschenkkarten

Im Shopify-Shop können Sie Geschenkgutscheine verkaufen, mit denen später echte Produkte bezahlt werden können.

Beim Umgang mit Geschenkkarten ist es wichtig, einen Wert in das Feld **Konto für verkaufte Geschenkkarte** im Fenster **Shopify-Shop-Karte** einzugeben. Die verkaufte Geschenkkarte wird zusammen mit den entsprechenden Bestellungen synchronisiert. Eine angewendete Geschenkkarte wird ebenfalls mit der Bestellung importiert, jetzt jedoch als Transaktion. Beachten Sie, dass die Geschenkkarte den Rechnungsbetrag nicht reduziert.

Um die ausgegebenen und angewendeten Geschenkkarten zu überprüfen, wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Geschenkkarten** ein, und wählen Sie dann den entsprechende Link aus.

## <a name="transactions"></a>Transaktionen

Die Zahlungsbuchungen, die in Shopify vorgenommen wurden, werden zusammen mit den Bestellungen synchronisiert und können in der *Shopify-Bestellung* angezeigt werden.

Um alle Transaktionen zu überprüfen, wählen Sie das Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Transaktionen** ein, und wählen Sie den entsprechenden Link aus.

## <a name="payouts"></a>Auszahlungen

Wenn für Ihren Store Shopify Payments aktiviert sind, erhalten Sie Zahlungen durch *Shopify-Auszahlungen*, wenn ein Debitor mit Shopify Payments und beschleunigten Checkouts bezahlt.

1. Wechseln Sie zum Suchsymbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Was möchten Sie tun?") , geben Sie **Shopify-Shop** ein, und wählen Sie den entsprechenden Link aus.
2. Wählen Sie den Shop aus, für den Sie Auszahlungen synchronisieren möchten, um die Seite **Shopify-Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Auszahlungen synchronisieren** aus.

Um alle Auszahlungen zu überprüfen, wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Auszahlungen** ein, und wählen Sie den entsprechenden Link aus.

## <a name="see-also"></a>Siehe auch

[Erste Schritte mit dem Konnektor für Shopify](get-started.md)  
