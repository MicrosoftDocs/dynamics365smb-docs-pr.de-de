---
title: Verkaufsaufträge synchronisieren und erfüllen
description: Nehmen Sie die Einrichtung und Ausführung des Imports under der Verarbeitung von Verkaufsaufträgen über Shopify vor.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="synchronize-and-fulfill-sales-orders"></a>Verkaufsaufträge synchronisieren und erfüllen

Dieser Artikel beschreibt die notwendigen Einstellungen und Schritte, die Sie durchführen müssen, um Verkaufsaufträge mit Shopify in [!INCLUDE[prod_short](../includes/prod_short.md)] zu synchronisieren und zu erfüllen.

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>Legen Sie den Import von Bestellungen auf der Shopify Shop-Karte fest.

Geben Sie einen **Währungscode** ein, wenn Ihr Onlineshop eine andere Währung als die lokale Währung (MW) verwendet. Für die angegebene Währung müssen Wechselkurse konfiguriert sein. Wenn Ihr Onlineshop dieselbe Währung verwendet wie [!INCLUDE[prod_short](../includes/prod_short.md)], lassen Sie das Feld leer. 

Sie können auf die Store-Währung in den [Store-Details](https://www.shopify.com/admin/settings/general) Einstellungen in Ihrem Shopify Admin zugreifen. Shopify kann so konfiguriert werden, dass verschiedene Währungen akzeptiert werden, aber importierte Bestellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] verwenden die Store-Währung.

Eine reguläre Shopify-Bestellung kann zusätzlich zur Zwischensumme Kosten enthalten, z.B. Versandkosten oder, falls aktiviert, Trinkgelder. Diese Beträge werden direkt auf das Sachkonto gebucht, das Sie für bestimmte Vorgangsarten verwenden möchten:

* **Lieferkostenkonto**
* **Konto für verkaufte Geschenkkarte**, weitere Informationen unter [Geschenkkarte](synchronize-orders.md#gift-cards)
* **Konto für Trinkgelder**  

Aktivieren Sie **Aufträge automatisch erstellen**, um automatisch Verkaufsaufträge in [!INCLUDE[prod_short](../includes/prod_short.md)] zu erstellen, sobald der Shopify-Auftrag importiert ist.

Wenn Sie einen Verkaufsbeleg automatisch freigeben möchten, aktivieren Sie die Umschaltung **Kundenauftrag automatisch freigeben**.

Wenn Sie das Feld **Shopify-Auftragsnummer in Belegzeile** auswählen, fügt [!INCLUDE [prod_short](../includes/prod_short.md)] Verkaufszeilen vom Typ **Kommentar** mit der Shopify-Auftragsnummer ein.

>[!NOTE]
>Der Verkaufsbeleg in [!INCLUDE[prod_short](../includes/prod_short.md)] ist mit dem Shopify-Auftrag verknüpft, und Sie können die **Shopify-Auftragsnummer** hinzufügen Fügen Sie das Feld der Liste oder den Kartenseiten für Verkaufsaufträge, Rechnungen und Lieferungen hinzu. Um mehr über das Hinzufügen eines Felds zu erfahren, gehen Sie zu [Um mit der Personalisierung einer Seite über das Banner **Personalisierung** zu beginnen](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

Im Feld **Steuergebiet Priorität** können Sie die Priorität für die Auswahl des Steuergebietscodes auf Adressen in Aufträgen festlegen. Der von Ihnen importierte Shopify-Auftrag enthält Informationen zu Steuern. Die Steuern werden neu berechnet, wenn Sie Verkaufsbelege erstellen. Daher ist es wichtig, dass die MwSt.- oder Steuereinstellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] korrekt sind. Weitere Informationen über Steuern finden Sie unter [Steuern für die Shopify-Verbindung festlegen](setup-taxes.md).

Geben Sie an, wie Sie Rückgaben und Rückerstattungen bearbeiten:

* **Leer** bedeutet, dass Sie keine Rückgaben und Rückerstattungen importieren und verarbeiten.
* **Nur importieren** bedeutet, dass Sie Informationen importieren, die entsprechende Gutschrift jedoch manuell erstellen.
* **Gutschrift automatisch erstellen** bedeutet, dass Sie Informationen importieren und [!INCLUDE[prod_short](../includes/prod_short.md)] die Gutschriften automatisch erstellt. Für diese Option müssen Sie den Umschalter **Verkaufsauftrag automatisch erstellen** aktivieren.

Geben Sie einen Lagerort für Rückgaben und Sachkonten für Rückerstattungen für Waren und andere Rückerstattungen an.

* **Erstattungskonto nicht wieder eingelagerter Artikel**: Gibt eine Sachkontonummer für Artikel an, für die keine Lagerkorrektur durchgeführt werden soll.
* **Erstattungskonto**: Gibt ein Sachkonto für die Differenz zwischen dem Gesamtbetrag der Rückerstattung und dem Gesamtbetrag der Artikel an.

Weitere Informationen finden Sie unter [Rückgaben und Rückerstattungen](synchronize-orders.md#returns-and-refunds)

### <a name="shipment-method-mapping"></a>Zuordnung von Versandmethoden

Der **Versandartencode** für aus Shopify importierte Verkaufsdokumente kann automatisch ausgefüllt werden. Sie müssen die **Zuordnung von Versandmethoden** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop aus, für den Sie eine Zuordnung definieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung von Versandmethoden** aus. Dadurch werden die Datensätze für Versandmethoden, die in den Einstellungen für den [**Versand**](https://www.shopify.com/admin/settings/payments) in Ihrer **Shopify-Verwaltung** definiert sind, automatisch erstellt.
4. Im Feld **Name** sehen Sie den Namen der Versandmethode aus Shopify.
5. Geben Sie den **Versandmethodencode** mit der entsprechenden Versandmethode in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Wenn einem Verkaufsauftrag mehrere Belastungen zugeordnet sind, wird nur eine als Versandart ausgewählt und dem Verkaufsbeleg zugewiesen.

### <a name="location-mapping"></a>Zuordnung von Standorten

Die Lagerortzuordnung ist erforderlich, um den **Lagerortcode** für Verkaufsbelegzeilen auszufüllen, die aus Shopify importiert wurden. Dies ist wichtig, wenn die Option **Lagerplatz obligatorisch** auf der Karte **Inventareinrichtung** aktiviert ist, da Sie sonst keine Belege erstellen können.

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1 öffnet.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie die Zuordnung der Standorte konfigurieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Standorte**, um die **Shopify Shop-Standorte** zu öffnen.
4. Wählen Sie die Aktion **Shopify Standorte abrufen**, um alle in Shopify definierten Standorte zu importieren. Sie finden sie in den [**Standorte**](https://www.shopify.com/admin/settings/locations)-Einstellungen in Ihrem **Shopify Admin**-Panel. 
5. Geben Sie den **Standardlagerplatzcode** mit dem entsprechenden Lagerplatz in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Die Lagerortzuordnung wird auch für die Synchronisierung des Lagerbestands verwendet. Weitere Informationen finden Sie unter [Lagerbestand mit Shopify synchronisieren](synchronize-items.md#sync-inventory-to-shopify).
  
## <a name="run-the-order-synchronization"></a>Führen Sie die Auftragssynchronisation aus

Nachfolgend wird beschrieben, wie Sie die Verkaufsaufträge importieren und aktualisieren.

> [!NOTE]  
> Archivierte Bestellungen in Shopify können nicht importiert werden. Deaktivieren Sie die Option **Bestellung automatisch archivieren** im Abschnitt **Bestellverarbeitung** der **Checkout**-Einstellungen in Ihrem **Shopify Admin**-Panel, um sicherzustellen, dass alle Bestellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] importiert werden. Wenn Sie archivierte Aufträge importieren müssen, verwenden Sie die Aktion **Auftragsarchivierung** auf der Seite [Auftrag](https://www.shopify.com/admin/orders) des **Shopify Admin** Panels.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie Bestellungen importieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen** aus.
4. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
5. Definieren Sie bei Bedarf Filter für Bestellungen. Sie können z.B. vollständig bezahlte Aufträge oder solche mit einem niedrigen Risikoniveau importieren.

> [!NOTE]  
> Beim Filtern nach Tag sollten Sie die Filtertoken `@` und `*` verwenden. Wenn Sie beispielsweise Bestellungen importieren möchten, die *tag1* enthalten, verwenden Sie `@*tag1*`. `@` stellt sicher, dass das Ergebnis die Groß- und Kleinschreibung berücksichtigt, während `*` Aufträge mit mehreren Tags findet.

6. Wählen Sie die Schaltfläche **OK**.

Alternativ können Sie nach dem Batchauftrag **Aufträge synchronisieren von Shopify** suchen.

Sie können planen, dass die Aufgabe automatisch ausgeführt wird. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

### <a name="under-the-hood"></a>Unter der Haube

Der Shopify Connector importiert Aufträge in zwei Schritten:

1.  Er importiert Auftragsheader in die Tabelle **Zu importierende Shopify-Aufträge**, wenn sie bestimmte Bedingungen erfüllen:
    
* Sie werden nicht archiviert. Das bedeutet, dass Sie Bestellungen in die Synchronisierung einschließen oder von ihr ausschließen können, indem Sie sie in der Shopify-Verwaltung archivieren oder dearchivieren.
* Sie wurden nach der letzten Synchronisierung erstellt oder geändert. Dies bedeutet, dass Sie den erneuten Import einer bestimmten Reihenfolge erzwingen können, wenn Sie diese ändern, beispielsweise durch Hinzufügen von **Notizen** oder **Tags**.

2.  Er importiert Shopify Aufträge und zusätzliche Informationen.
* Der Shopify Connector verarbeitet alle Datensätze in der Tabelle **Zu importierende Shopify-Aufträge**, die den Filterkriterien entsprechen, die Sie in der Anforderungsseite **Aufträge von Shopify synchronisieren** festgelegt haben. Zum Beispiel Tags, Kanal oder der Auftragserfüllungsstatus. Wenn Sie keine Filter angegeben haben, werden alle Datensätze verarbeitet.
* Beim Importieren eines Shopify-Auftrags fordert der Shopify Connector zusätzliche Informationen von Shopify an:

    * Auftragsheader
    * Auftragspositionen
    * Versand- und Auftragserfüllungsinformationen
    * Transaktionen
    * Rückgaben und Rückerstattungen, sofern konfiguriert

Die Seite **Zu importierender Shopify Auftrag** hilft bei der Behebung von Problemen beim Importieren von Aufträgen. Sie können die verfügbaren Aufträge bewerten und die nächsten Schritte planen:

* Überprüfen Sie, ob ein Fehler den Import eines bestimmten Auftrags blockiert hat, und erkunden Sie die Details des Fehlers. Überprüfen Sie das Feld **Fehler**.
* Bearbeiten Sie nur bestimmte Aufträge. Sie müssen das Feld **Shop-Code** ausfüllen, einen oder mehrere Aufträge ausfüllen und dann die Aktion **Ausgewählte Aufträge importieren** auswählen.
* Löschen Sie Aufträge von der Seite **Zu importierender Shopify Auftrag**, um sie von der Synchronisierung auszuschließen.

## <a name="review-imported-orders"></a>Importierte Bestellungen überprüfen

Sobald der Import abgeschlossen ist, können Sie die Shopify-Bestellung durchsuchen und alle zugehörigen Informationen finden, wie z.B. die Transaktionen, die Versandkosten, die Risikostufe, die Bestellattribute und Tags oder die Erfüllungen, wenn die Bestellung bereits in Shopify erfüllt wurde. Sie können auch alle an den Debitor gesendeten Auftragsbestätigungen anzeigen, indem Sie die Aktion **Shopify-Statusseite** auswählen.

> [!NOTE]  
> Sie können direkt zum Fenster **Shopify Bestellungen** navigieren und sehen dort Bestellungen mit dem Status *offen* aus allen Geschäften. Um abgeschlossene Bestellungen zu überprüfen, müssen Sie die Seite **Shopify Bestellungen** aus dem jeweiligen **Shopify Shop Card** Fenster öffnen.

## <a name="create-sales-documents-in-business-central"></a>Verkaufsbelege in Business Central erstellen

Wenn die Option **Automatische Erstellung von Aufträgen** auf der **Shopify Shop Card** aktiviert ist, versucht [!INCLUDE[prod_short](../includes/prod_short.md)] einen Verkaufsbeleg zu erstellen, nachdem der Auftrag importiert wurde. Wenn Probleme wie ein fehlender Debitor oder ein fehlendes Produkt auftreten, müssen Sie die Probleme beheben und dann den Verkaufsauftrag erneut erstellen.

### <a name="to-create-sales-documents"></a>So erstellen Sie Verkaufsbelege

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie Bestellungen synchronisieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen**.
4. Markieren Sie die Bestellung aus, für die Sie einen Verkaufsbeleg erstellen möchten, und wählen Sie die Aktion **Verkaufsbelege erstellen** aus.
5. Wählen Sie **Ja** aus.

Wenn die Shopify Bestellung erfüllt werden muss, wird ein **Verkaufsauftrag** erstellt. Für erfüllte Shopify-Bestellungen, z.B. solche, die nur eine Geschenkkarte enthalten oder die bereits in Shopify behandelt werden, wird eine **Verkaufsrechnung** erstellt.

Ein Verkaufsbeleg ist nun erstellt und kann mit Standarfunktionen von [!INCLUDE[prod_short](../includes/prod_short.md)] verwaltet werden.

### <a name="manage-missing-customers"></a>Fehlende Debitoren verwalten

Wenn Ihre Einstellungen die automatische Erstellung eines Debitors verhindern und kein entsprechender vorhandener Debitor gefunden werden kann, müssen Sie der Shopify-Bestellung manuell einen Debitor zuweisen. Es gibt einige Möglichkeiten, dies zu tun:

* Sie können die **Verk. an Deb.-Nr.** und **Rechnung an Debitor Nr.** direkt auf der Seite **Shopify-Bestellungen** zuweisen, indem Sie einen Debitor aus der Liste der vorhandenen Debitoren auswählen.
* Sie können einen Kundenvorlagencode auswählen, erstellen und dann den Kunden über die Aktion **Neuen Kunden erstellen** auf der Seite **Shopify Aufträge** zuordnen. Beachten Sie, dass der Shopify-Debitor über mindestens eine Adresse verfügen muss. Bei Bestellungen, die über den Shopify-Vertriebskanal POS erstellt wurden, fehlen häufig Adressangaben.
* Sie können einen bestehenden Debitor dem zugehörigen **Shopify Kunden** im Fenster **Shopify Kunden** zuordnen und dann die Aktion **Zuordnung finden** auf der Seite **Shopify Aufträge** wählen.

### <a name="how-the-connector-chooses-which-customer-to-use"></a>Wie der Konnektor auswählt, welcher Kunde verwendet werden soll

Die Funktion *Bestellung aus Shopify importieren* versucht, die Debitoren in der folgenden Reihenfolge auszuwählen:

1. Wenn das Feld **Standarddebitorennr.** in der **Shopify Debitorenvorlage** für **Lieferung an Länder-/Regionscode** definiert ist, dann wird die **Standarddebitorennr.** verwendet, unabhängig von den Einstellungen in den Feldern **Kundenimport von Shopify** und **Kundenzuordnungstyp**. Weitere Informationen unter [Debitorenvorlage pro Land](synchronize-customers.md#customer-template-per-countryregion).
2. Wenn der **Kundenimport von Shopify** auf *Keine* festgelegt ist und die **Standardkunden-Nr.** auf der Seite **Shopify-Shop-Karte** definiert sind, wird die **Standarddebitorennr.** verwendet.

Die nächsten Schritte hängen von der **Kundenzuordnung Typ** ab.

* Wenn dies **Nehmen Sie immer den Standardkunden** ist, dann verwendet der Konnektor den in der **Standarddebitorennr.** definierten Debitor Feld auf der Seite **Shopify Shop-Karte**.
* **Nach E-Mail/Telefon**, der Konnektor versucht, den bestehenden Kunden zuerst nach der ID, dann nach der E-Mail und dann nach der Telefonnummer zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.
* **Nach Rechnungsinformationen** versucht der Konnektor, den bestehenden Kunden zunächst über die ID und dann über die Rechnungsadressinformationen zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.

> [!NOTE]  
> Der Konnektor verwendet die Informationen aus der Rechnungsadresse und erstellt den Rechnungsempfänger in [!INCLUDE[prod_short](../includes/prod_short.md)]. Der Verk. an Debitor ist derselbe wie Rechnung an Debitor.

### <a name="different-processing-rules-for-orders"></a>Unterschiedliche Bearbeitungsregeln für Aufträge

Möglicherweise möchten Sie Aufträge anhand einer Regel anders verarbeiten. Beispielsweise sollte bei Aufträgen über einen bestimmten Vertriebskanal wie POS der Standarddebitor verwendet werden, Sie möchten jedoch, dass Ihr Onlineshop über echte Informationen über den Debitor verfügt.

Eine Möglichkeit, dieser Anforderung gerecht zu werden, besteht darin, eine zusätzliche Shopify Shop-Karte zu erstellen und Filter auf der Anfrageseite **Aufträge von Shopify synchronisieren** zu verwenden.

Beispiel: Sie haben einen Onlineshop und einen Shopify POS. Für Ihren POS möchten Sie einen festen Debitor verwenden, für Ihren Onlineshop möchten Sie jedoch Debitoren in [!INCLUDE[prod_short](../includes/prod_short.md)] erstellen. Das folgende Verfahren listet die allgemeinen Schritte auf. Weitere Informationen finden Sie in den entsprechenden Hilfeartikeln.

1. Erstellen Sie einen Shopify Shop mit dem Namen *STORE* und verknüpfen Sie ihn mit Ihrem Shopify Konto.
2. Konfigurieren Sie die Artikel-/Produktsynchronisierung, sodass dieser Shop Produktinformationen verwaltet.
3. Geben Sie an, dass Debitoren mit Aufträgen importiert werden. Der Connector soll Debitoren finden, indem er nach deren E-Mail-Adresse sucht. Wenn keine Adresse gefunden wird, wird mithilfe der Debitorenvorlage ein neuer Debitor erstellt.
4. Erstellen Sie einen Shopify Shop mit dem Namen *POS* und verknüpfen Sie ihn mit demselben Shopify Konto.
6. Stellen Sie sicher, dass die Artikel-/Produktsynchronisierung deaktiviert ist.
7. Wählen Sie den Connector aus, der den Standarddebitor verwendet.
8. Erstellen Sie einen wiederkehrenden Auftragswarteschlangeneintrag für Bericht 30104 **Aufträge von Shopify synchronisieren**. Wählen Sie **STORE** im Feld **Shopify Shop-Code** aus und verwenden Sie Filter, um alle Aufträge außer denen zu erfassen, die der POS-Vertriebskanal erstellt. Zum Beispiel: **<>-Verkaufsstelle**
9. Erstellen Sie einen wiederkehrenden Auftragswarteschlangeneintrag für den Bericht 30104 **Aufträge von Shopify synchronisieren**. Wählen Sie **POS** im Feld **Shopify Shop-Code** aus und verwenden Sie Filter, um Aufträge zu erfassen, die vom POS-Vertriebskanal generiert wurden. Zum Beispiel: **<>Verkaufsstelle**.

Jede Auftragswarteschlange importiert und verarbeitet Aufträge innerhalb der definierten Filter und verwendet die Regeln der entsprechenden Shopify Shop-Karte. Sie erstellen beispielsweise Verkaufsstellenaufträge für den Standarddebitor.

>[!Important]
> Um Konflikte bei der Verarbeitung von Aufträgen zu vermeiden, denken Sie daran, für beide Auftragswarteschlangeneinträge dieselbe Auftragswarteschlangenkategorie zu verwenden.

### <a name="impact-of-order-editing"></a>Auswirkung der Bearbeitung von Bestellungen

In Shopify:

|Bearbeiten|Auswirkung auf bereits importierte Bestellung|Auswirkungen auf Bestellungen, die zum ersten Mal importiert werden|
|------|-----------|-----------|
|Den Erfüllungsort ändern | Ursprünglicher Standort ist in Linien | Der Fulfillment-Standort ist synchronisiert [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Bearbeiten Sie eine Bestellung und erhöhen Sie die Menge| Der Auftragskopf und die Zusatztabellen werden in [!INCLUDE[prod_short](../includes/prod_short.md)] aktualisiert, die Zeilen nicht.| Die importierte Bestellung verwendet eine neue Menge|
|Bearbeiten Sie eine Bestellung und verringern Sie die Menge| Der Auftragskopf und die Zusatztabellen werden in [!INCLUDE[prod_short](../includes/prod_short.md)] aktualisiert, die Zeilen nicht.| Die importierte Bestellung verwendet die ursprüngliche Menge, das Feld „Erfüllbare Menge“ enthält einen neuen Wert.|
|Bearbeiten Sie eine Bestellung und entfernen Sie einen bestehenden Artikel | Der Auftragskopf und die Zusatztabellen werden in [!INCLUDE[prod_short](../includes/prod_short.md)] aktualisiert, die Zeilen nicht.| Entfernte Artikel werden weiterhin importiert, das Feld Erfüllbare Menge Null enthält. |
|Bearbeiten Sie eine Bestellung und fügen Sie einen neuen Artikel hinzu | Der Auftragskopf wird aktualisiert, die Zeilen nicht. | Ursprüngliche und hinzugefügte Elemente werden importiert. |
|Bestellung bearbeiten: ausführen, Zahlungsinformationen aktualisieren | Der Auftragskopf wird aktualisiert, aber die Zeilen nicht. |Die Änderung hat keinen Einfluss darauf, wie die Bestellung importiert wird.|
|Auftrag stornieren | Der Auftragskopf wird aktualisiert, aber die Zeilen nicht. |Stornierte Bestellung wird nicht importiert |

Wie Sie sehen, kann es in manchen Fällen sinnvoll sein, die bearbeitete Bestellung in [!INCLUDE[prod_short](../includes/prod_short.md)] zu löschen und als neue zu importieren.

In [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Bearbeiten|Auswirkungen|
|------|-----------|
|Ändern Sie den Standort in einen anderen Standort, der den Shopify Orten zugeordnet ist. Sendung buchen. | Der Auftrag wird als erfüllt markiert. Der ursprüngliche Standort wird verwendet. |
|Ändern Sie den Ort in einen anderen Ort, der nicht den Shopify Orten zugeordnet ist. Sendung buchen. | Die Erfüllung wird nicht mit Shopify synchronisiert. |
|Menge verkleinern Sendung buchen. | Die Reihenfolge Shopify wird als teilweise erfüllt gekennzeichnet. |
|Menge erhöhen. Sendung buchen. | Die Erfüllung wird nicht mit Shopify synchronisiert. |
|Ein neues Element hinzufügen. Sendung buchen. | Die Reihenfolge Shopify wird als erfüllt markiert. Die Zeilen werden nicht aktualisiert. |

## <a name="synchronize-shipments-to-shopify"></a>Lieferungen mit Shopify synchronisieren

Wenn ein Verkaufsauftrag, der aus einem Shopify-Auftrag erstellt wurde, versandt wird, können Sie die Sendungen mit Shopify synchronisieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Sendungen mit Shopify synchronisieren** ein und wählen Sie dann den entsprechenden Link.
2. Definieren Sie die Filter für Sendungen nach Bedarf. Sie können zum Beispiel eine Sendung aktualisieren, die zu einem bestimmten Datum gebucht wurde.
3. Wählen Sie die Schaltfläche **OK**.

Die Bestellung in Shopify wird als erfüllt markiert. Der Debitor erhält automatisch eine Versandbenachrichtigung per E-Mail oder Textnachricht (SMS). Wenn ein Zusteller und ein Verfolgungscode für die Lieferung angegeben sind, sind die Verfolgungsinformationen in der E-Mail enthalten.

Alternativ können Sie die Aktion **Sync Sendungen** auf den Seiten Shopify Verkaufsaufträge oder Shopify Shop verwenden.

Sie können die Aufgabe für eine automatische Ausführung planen. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

>[!Important]
>Der Lagerplatz, einschließlich des leeren Lagerplatzes, der in der Zeile Gebuchte Sendung definiert ist, muss einen passenden Datensatz im Shopify Standort haben. Andernfalls wird diese Zeile nicht an Shopify zurückgeschickt. Erfahren Sie mehr unter [Zuordnung von Lagerplätzen](synchronize-orders.md#location-mapping).

Denken Sie daran, **Bestellungen aus Shopify** auszuführen, um den Erfüllungsstatus der Bestellung in [!INCLUDE[prod_short](../includes/prod_short.md)] zu aktualisieren. Die Konnektor-Funktionalität archiviert auch vollständig bezahlte und erfüllte Bestellungen sowohl in Shopify als auch in [!INCLUDE[prod_short](../includes/prod_short.md)], sofern die Bedingungen erfüllt sind. 

### <a name="shipping-agents-and-tracking-url"></a>Zusteller und Verfolgungs-URL

Wenn das Dokument **Gebuchte Verkaufslieferung** den **Versandagentencode** und/oder die **Paketverfolgungsnummer** enthält, werden diese Informationen an Shopify und an den Kunden in der Versandbestätigungs-E-Mail gesendet.

Die verfolgende Firma wird auf der Grundlage des Datensatzes des Zustellers mit der folgenden Folge (von oben nach unten) eingetragen:

* **Shopify-Nachverfolgungsunternehmen**
* **Name**
* **Code**

Wenn das Feld **Paketverfolgungs-URL** für den Datensatz des Zustellers ausgefüllt ist, dann enthält die Versandbestätigung ebenfalls eine Verfolgungs-URL.

## <a name="returns-and-refunds"></a>Rückgaben und Rückerstattungen

Bei einer Integration zwischen Shopify und [!INCLUDE[prod_short](../includes/prod_short.md)] ist es wichtig, möglichst viele Geschäftsdaten synchronisieren zu können. Dadurch ist es einfacher, Ihre Finanzen und Lagerebenen in [!INCLUDE[prod_short](../includes/prod_short.md)] auf dem neuesten Stand zu halten. Zu den Daten, die Sie synchronisieren können, gehören Rückgaben und Rückerstattungen, die im Shopify Administrator oder Shopify POS erfasst wurden.

Rückgaben und Rückerstattungen werden mit den zugehörigen Auftägen importiert, wenn Sie den Verarbeitungstyp auf der Shopify Shop-Karte aktiviert haben.

Rückgaben werden nur zu Informationszwecken importiert. Ihnen ist keine Verarbeitungslogik zugeordnet.

Finanz- und gegebenenfalls Lagerbuchungen werden über Rückerstattungen abgewickelt. Rückerstattungen können sich auf Produkte oder nur auf Beträge beziehen, beispielsweise wenn sich ein Händler entschieden hat, Versandkosten oder einen anderen Betrag zu erstatten.
Sie können Verkaufsgutschriften für Rückerstattungen erstellen. Die Gutschriften können folgende Zeilentypen haben:

|Typ|Anz.|Kommentar|
|-|-|-|
|Sachkonto|Konto für verkaufte Geschenkkarte| Für Rückerstattungen im Zusammenhang mit Geschenkkarten verwenden.|
|Sachkonto|Erstattungskonto nicht eingelagert | Für Rückerstattungen im Zusammenhang mit Produkten verwenden, die nicht wieder eingelagert wurden. |
|Option |Artikelnummer| Für Rückerstattungen im Zusammenhang mit Produkten verwenden, die wieder eingelagert wurden. Gültig für direkte Rückerstattungen oder für mit Rückerstattungen verbundene Rückerstattungen. Der Lagerortcode für die Gutschrift-Zeile wird basierend auf dem für den Rückgabelagerort ausgewählten Wert festgelegt.|
|Sachkonto| Erstattungskonto | Für andere Rückerstattungsbeträge verwenden, die nichts mit Produkten oder Geschenkkarten zu tun haben. Zum Beispiel Trinkgelder oder wenn Sie in Shopify manuell einen zu erstattenden Betrag angegeben haben. |

>[!Note]
>Der unter **Shopify Shop-Karte** festgelegte Rückgabelagerort, einschließlich leerer Lagerorte, wird auf der erstellten Gutschrift verwendet. Das System ignoriert die ursprünglichen Lagerorte aus Aufträgen oder Lieferungen.

## <a name="gift-cards"></a>Geschenkkarten

Im Shopify-Shop können Sie Geschenkgutscheine verkaufen, mit denen echte Produkte bezahlt werden können.

Wenn Sie mit Geschenkkarten arbeiten, ist es wichtig, dass Sie im Fenster **Shopify Shop-Karte** einen Wert in das Feld **Geschenkkartenkonto** eingeben. Die verkaufte Geschenkkarte wird zusammen mit den entsprechenden Bestellungen synchronisiert. Eine angewendete Geschenkkarte wird ebenfalls mit der Bestellung importiert, jetzt jedoch als Transaktion. Beachten Sie, dass die Geschenkkarte den Rechnungsbetrag nicht reduziert.

Um die ausgegebenen und angewendeten Geschenkkarten zu überprüfen, wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Geschenkkarten** ein, und wählen Sie dann den entsprechenden Link.

## <a name="see-also"></a>Siehe auch

[Einstieg in den Konnektor für Shopify](get-started.md)  
