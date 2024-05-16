---
title: Verkaufsaufträge synchronisieren und erfüllen
description: Nehmen Sie die Einrichtung und Ausführung des Imports und die Verarbeitung von Verkaufsaufträgen über Shopify vor.
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
---

# Verkaufsaufträge synchronisieren und erfüllen

Dieser Artikel beschreibt die notwendigen Einstellungen und Schritte, die Sie durchführen müssen, um Verkaufsaufträge mit Shopify in [!INCLUDE[prod_short](../includes/prod_short.md)] zu synchronisieren und zu erfüllen.

## Legen Sie den Import von Bestellungen auf der Shopify Shop-Karte fest.

Geben Sie einen **Währungscode** ein, wenn Ihr Onlineshop eine andere Währung als die lokale Währung (MW) verwendet. Für die angegebene Währung müssen Wechselkurse konfiguriert sein. Wenn Ihr Onlineshop dieselbe Währung verwendet wie [!INCLUDE[prod_short](../includes/prod_short.md)], lassen Sie das Feld leer. 

Sie können auf die Shop-Währung in den [Shop-Details](https://www.shopify.com/admin/settings/general)-Einstellungen in Ihrem Shopify Admin zugreifen. Shopify kann so konfiguriert werden, dass verschiedene Währungen akzeptiert werden. Nach [!INCLUDE[prod_short](../includes/prod_short.md)] importierte Aufträge verwenden jedoch die Shop-Währung.

Eine reguläre Shopify-Bestellung kann zusätzlich zur Zwischensumme Kosten enthalten, z.B. Versandkosten oder, falls aktiviert, Trinkgelder. Diese Beträge werden direkt auf das Sachkonto gebucht, das Sie für bestimmte Vorgangsarten verwenden möchten:

* **Lieferkostenkonto**
* **Konto für verkaufte Geschenkkarte**, weitere Informationen unter [Geschenkkarte](synchronize-orders.md#gift-cards)
* **Konto für Trinkgelder**  

Aktivieren Sie **Aufträge automatisch erstellen**, um automatisch Verkaufsaufträge in [!INCLUDE[prod_short](../includes/prod_short.md)] zu erstellen, sobald der Shopify-Auftrag importiert ist.

Wenn Sie einen Verkaufsbeleg automatisch freigeben möchten, aktivieren Sie die Umschaltung **Kundenauftrag automatisch freigeben**.

Wenn Sie keine automatischen Versandbestätigungen an die Kundschaft senden möchten, deaktivieren Sie den Schalter **Versandbestätigung senden**. Das Ausschalten des Schalters kann nützlich sein, wenn Sie digitale Güter verkaufen oder einen anderen Benachrichtigungsmechanismus verwenden möchten.

Wenn Sie das Feld **Shopify-Auftragsnummer in Belegzeile** auswählen, fügt [!INCLUDE [prod_short](../includes/prod_short.md)] Verkaufszeilen vom Typ **Kommentar** mit der Shopify-Auftragsnummer ein.

> [!NOTE]
> Der Verkaufsbeleg in [!INCLUDE[prod_short](../includes/prod_short.md)] ist mit dem Shopify-Auftrag verknüpft, und Sie können die **Shopify-Auftragsnummer** hinzufügen Fügen Sie das Feld der Liste oder den Kartenseiten für Verkaufsaufträge, Rechnungen und Lieferungen hinzu. Um mehr über das Hinzufügen eines Felds zu erfahren, gehen Sie zu [Beginnen Sie mit der Personalisierung, indem Sie den Personalisierungsmodus verwenden](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode). 

Im Feld **Steuergebiet Priorität** können Sie die Priorität für die Auswahl des Steuergebietscodes auf Adressen in Aufträgen festlegen. Der von Ihnen importierte Shopify-Auftrag enthält Informationen zu Steuern. Die Steuern werden neu berechnet, wenn Sie Verkaufsbelege erstellen. Daher ist es wichtig, dass die MwSt.- oder Steuereinstellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] korrekt sind. Weitere Informationen über Steuern finden Sie unter [Steuern für die Shopify-Verbindung festlegen](setup-taxes.md).

Geben Sie an, wie Sie Rückgaben und Rückerstattungen bearbeiten:

* **Leer** bedeutet, dass Sie keine Rückgaben und Rückerstattungen importieren und verarbeiten.
* **Nur importieren** bedeutet, dass Sie Informationen importieren, die entsprechende Gutschrift jedoch manuell erstellen.
* **Gutschrift automatisch erstellen** bedeutet, dass Sie Informationen importieren und [!INCLUDE[prod_short](../includes/prod_short.md)] die Gutschriften automatisch erstellt. Für diese Option müssen Sie den Umschalter **Verkaufsauftrag automatisch erstellen** aktivieren.

Geben Sie einen Lagerort für Rückgaben und Sachkonten für Rückerstattungen für Waren und andere Rückerstattungen an.

* **Erstattungskonto nicht wieder eingelagerter Artikel** gibt eine Sachkontonummer für Artikel an, für die keine Lagerkorrektur durchgeführt werden soll.
* **Erstattungskonto** gibt ein Sachkonto für die Differenz zwischen dem Gesamtbetrag der Rückerstattung und dem Gesamtbetrag der Artikel an.

Weitere Informationen finden Sie unter [Rückgaben und Rückerstattungen](synchronize-orders.md#returns-and-refunds)

### Zuordnung von Versandmethoden

Der **Versandartencode** für aus Shopify importierte Verkaufsdokumente kann automatisch ausgefüllt werden. Sie müssen die **Zuordnung von Versandmethoden** konfigurieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop aus, für den Sie eine Zuordnung definieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Zuordnung von Versandmethoden** aus. Dadurch werden die Datensätze für Versandmethoden, die in den Einstellungen für den [**Versand**](https://www.shopify.com/admin/settings/payments) in Ihrer **Shopify-Verwaltung** definiert sind, automatisch erstellt.
4. Im Feld **Name** sehen Sie den Namen der Versandmethode aus Shopify.
5. Geben Sie den **Versandmethodencode** mit der entsprechenden Versandmethode in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Wenn einem Verkaufsauftrag mehrere Belastungen zugeordnet sind, wird nur eine als Versandart ausgewählt und dem Verkaufsbeleg zugewiesen.

### Zuordnung von Standorten

Die Lagerortzuordnung ist erforderlich, um den **Lagerortcode** für Verkaufsbelegzeilen auszufüllen, die aus Shopify importiert wurden. Dies ist wichtig, wenn die Option **Lagerplatz obligatorisch** auf der Karte **Inventareinrichtung** aktiviert ist, da Sie sonst keine Belege erstellen können.

1. Wählen Sie die ![Glühbirne, die die “Wie möchten Sie weiter verfahren“-Funktion 1 öffnet.](../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie die Zuordnung der Standorte konfigurieren möchten, um die Seite **Shopify Shop Card** zu öffnen.
3. Wählen Sie die Aktion **Standorte**, um die **Shopify Shop-Standorte** zu öffnen.
4. Wählen Sie die Aktion **Shopify Standorte abrufen**, um alle in Shopify definierten Standorte zu importieren. Sie finden sie in den [**Standorte**](https://www.shopify.com/admin/settings/locations)-Einstellungen in Ihrem **Shopify Admin**-Panel. 
5. Geben Sie den **Standardlagerplatzcode** mit dem entsprechenden Lagerplatz in [!INCLUDE[prod_short](../includes/prod_short.md)] ein.

> [!NOTE]  
> Die Lagerortzuordnung wird auch zur Synchronisierung des Bestands verwendet. Weitere Informationen finden Sie unter [Lagerbestand mit Shopify synchronisieren](synchronize-items.md#sync-inventory-to-shopify).
  
## Führen Sie die Auftragssynchronisation aus

Nachfolgend wird beschrieben, wie Sie die Verkaufsaufträge importieren und aktualisieren.

> [!NOTE]  
> Archivierte Bestellungen in Shopify können nicht importiert werden. Wenn Sie den Bestellstatus überprüfen müssen, öffnen Sie die Bestellung auf der Seite [Bestellungen](https://www.shopify.com/admin/orders) im **Shopify Adminbereich** und überprüfen Sie sie Bestelldetails.
> 
> Deaktivieren Sie die Option **Bestellung automatisch archivieren** im Abschnitt **Bestellverarbeitung** der **Checkout**-Einstellungen in Ihrem **Shopify Admin**-Panel, um sicherzustellen, dass alle Bestellungen in [!INCLUDE[prod_short](../includes/prod_short.md)] importiert werden. Wenn Sie archivierte Aufträge importieren müssen, verwenden Sie die Aktion **Auftragsarchivierung** auf der Seite [Auftrag](https://www.shopify.com/admin/orders) des **Shopify Admin** Panels. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie Bestellungen importieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen** aus.
4. Wählen Sie die Aktion **Aufträge von Shopify synchronisieren** aus.
5. Definieren Sie bei Bedarf Filter für Bestellungen. Sie können z.B. vollständig bezahlte Bestellungen importieren oder solche mit einem niedrigen Risikoniveau.

   > [!NOTE]  
   > Beim Filtern nach Tag sollten Sie die Filtertoken `@` und `*` verwenden. Wenn Sie beispielsweise Aufträge importieren möchten, die *tag1* enthalten, verwenden Sie `@*tag1*`. `@` stellt sicher, dass das Ergebnis die Groß- und Kleinschreibung berücksichtigt, während `*` Aufträge mit mehreren Tags findet.

6. Wählen Sie die Schaltfläche **OK**.

Alternativ können Sie nach dem Batchauftrag **Aufträge synchronisieren von Shopify** suchen.

Sie können planen, dass die Aufgabe automatisch ausgeführt wird. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

### Unter der Haube

Der Shopify Connector importiert Aufträge in zwei Schritten:

1. Er importiert Auftragsheader in die Tabelle **Zu importierende Shopify-Aufträge**, wenn sie bestimmte Bedingungen erfüllen:

   * Sie werden nicht archiviert. Das bedeutet, dass Sie Bestellungen in die Synchronisierung einschließen oder von ihr ausschließen können, indem Sie sie in der Shopify-Verwaltung archivieren oder dearchivieren.
   * Sie wurden nach der letzten Synchronisierung erstellt oder geändert. Dies bedeutet, dass Sie den erneuten Import einer bestimmten Reihenfolge erzwingen können, wenn Sie diese ändern, beispielsweise indem Sie **Notizen** oder **Tags** hinzufügen.

2. Er importiert Shopify Aufträge und zusätzliche Informationen.

   * Der Shopify Connector verarbeitet alle Datensätze in der Tabelle **Zu importierende Shopify-Aufträge**, die den Filterkriterien entsprechen, die Sie in der Anforderungsseite **Aufträge von Shopify synchronisieren** festgelegt haben. Zum Beispiel Tags, Kanal oder der Auftragserfüllungsstatus. Wenn Sie keine Filter angegeben haben, werden alle Datensätze verarbeitet.
   * Beim Importieren eines Shopify-Auftrags fordert der Shopify-Konnektor zusätzliche Informationen von Shopify an:

     * Auftragsheader
     * Auftragspositionen
     * Versand- und Auftragserfüllungsinformationen
     * Transaktionen
     * Rückgaben und Rückerstattungen, sofern konfiguriert

Die Seite **Zu importierender Shopify Auftrag** hilft bei der Behebung von Problemen beim Importieren von Aufträgen. Sie können die verfügbaren Aufträge bewerten und die nächsten Schritte planen:

* Überprüfen Sie, ob ein Fehler den Import eines bestimmten Auftrags blockiert hat, und erkunden Sie die Details des Fehlers. Überprüfen Sie das Feld **Fehler**.
* Bearbeiten Sie nur bestimmte Aufträge. Sie müssen das Feld **Shop-Code** ausfüllen, einen oder mehrere Aufträge ausfüllen und dann die Aktion **Ausgewählte Aufträge importieren** auswählen.
* Löschen Sie Aufträge von der Seite **Zu importierender Shopify Auftrag**, um sie von der Synchronisierung auszuschließen.

## Importierte Bestellungen überprüfen

Sobald der Import abgeschlossen ist, können Sie die Shopify-Bestellung durchsuchen und alle zugehörigen Informationen finden, wie z.B. die Transaktionen, die Versandkosten, die Risikostufe, die Bestellattribute und Tags oder die Erfüllungen, wenn die Bestellung bereits in Shopify erfüllt wurde. Sie können auch alle an den Debitor gesendeten Auftragsbestätigungen anzeigen, indem Sie die Aktion **Shopify-Statusseite** auswählen.

> [!NOTE]  
> Sie können direkt zum Fenster **Shopify Bestellungen** navigieren und sehen dort Bestellungen mit dem Status *offen* aus allen Geschäften. Um abgeschlossene Aufträge zu überprüfen, müssen Sie die Seite **Shopify-Aufträge** aus der jeweiligen Seite **Shopify Shop-Karte** öffnen.

Bevor Verkaufsbelege in [!INCLUDE[prod_short](../includes/prod_short.md)] erstellt werden, können Sie mit der Aktion **Auftrag von Shopify synchronisieren** auf der Seite **Shopify-Auftrag** bestimmte Aufträge erneut importieren.

Sie können einen Auftrag auch als bezahlt markieren, was in einem B2B-Szenario nützlich ist, in dem Zahlungen außerhalb des Shopify-Checkouts abgewickelt werden. Wählen Sie die Aktion **Als bezahlt markieren** auf der Seite **Shopify-Auftrag** aus. Sie können einen Auftrag auch als storniert markieren, um den Rückerstattungs-Flow in Shopify zu starten. Wählen Sie auf der Seite **Shopify-Auftrag** die Aktion **Auftrag stornieren** aus und füllen Sie auf der Seite **Shopify--Auftrag stornieren** die erforderlichen Felder aus und drücken Sie **OK**. Sie müssen die Auftragssynchronisierung ausführen, um die Aktualisierungen in [!INCLUDE[prod_short](../includes/prod_short.md)] zu importieren.

## Verkaufsbelege in Business Central erstellen

Wenn die Option **Automatische Erstellung von Aufträgen** auf der **Shopify Shop Card** aktiviert ist, versucht [!INCLUDE[prod_short](../includes/prod_short.md)] einen Verkaufsbeleg zu erstellen, nachdem der Auftrag importiert wurde. Wenn Probleme wie ein fehlender Debitor oder ein fehlendes Produkt auftreten, müssen Sie die Probleme beheben und dann den Verkaufsauftrag erneut erstellen.

### So erstellen Sie Verkaufsbelege

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Shopify Shops** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Shop, für den Sie Bestellungen synchronisieren möchten, um die Seite **Shopify Shop-Karte** zu öffnen.
3. Wählen Sie die Aktion **Bestellungen**.
4. Markieren Sie die Bestellung aus, für die Sie einen Verkaufsbeleg erstellen möchten, und wählen Sie die Aktion **Verkaufsbelege erstellen** aus.
5. Wählen Sie **Ja** aus.

Wenn die Shopify Bestellung erfüllt werden muss, wird ein **Verkaufsauftrag** erstellt. Für erfüllte Shopify-Bestellungen, z.B. solche, die nur eine Geschenkkarte enthalten oder die bereits in Shopify behandelt werden, wird eine **Verkaufsrechnung** erstellt.

Ein Verkaufsbeleg ist erstellt und kann mit Standarfunktionen von [!INCLUDE[prod_short](../includes/prod_short.md)] verwaltet werden.

Wenn Sie einen Verkaufsbeleg neu erstellen möchten, können Sie dies mit der Aktion **Verknüpfung verarbeiteter Belege aufheben** auf der Seite **Shopify-Auftrag** tun. Beachten Sie, dass durch diese Aktion der bereits erstellte Verkaufsbeleg nicht gelöscht wird. Sie müssen ihn manuell verarbeiten.

### Fehlende Debitoren verwalten

Wenn Ihre Einstellungen die automatische Erstellung eines Debitors verhindern und kein übereinstimmender Debitor gefunden werden kann, müssen Sie dem Shopify-Auftrag manuell einen Debitor zuweisen. Es gibt verschiedene Möglichkeiten, der Kundschaft Aufträge zuzuordnen:

* Weisen Sie dies zu: **Verk. an Deb.-Nr.** und **Rechnung an Debitor Nr.** direkt auf der Seite **Shopify-Bestellungen** zuweisen, indem Sie einen Debitor aus der Liste der vorhandenen Debitoren auswählen.
* Wählen Sie eine Kundenvorlage aus, erstellen Sie den Debitoren und weisen Sie sie dann über die Aktion **Neuen Kunden erstellen** auf der Seite **Shopify-Aufträge** zu. Der Shopify-Debitor über mindestens eine Adresse verfügen muss. Bei Aufträgen, die über den Shopify-Vertriebskanal POS erstellt wurden, fehlen häufig Adressangaben.
* Ordnen Sie einen bestehenden Debitor dem zugehörigen **Shopify-Kunden** auf der Seite **Shopify-Kunden** zu und wählen Sie dann die Aktion **Zuordnung finden** auf der Seite **Shopify-Aufträge** aus.

### Wie der Konnektor auswählt, welcher Kunde verwendet werden soll

Die Funktion *Bestellung aus Shopify importieren* versucht, die Debitoren in der folgenden Reihenfolge auszuwählen:

1. Wenn das Feld **Standarddebitorennr.** in der **Shopify Debitorenvorlage** für **Lieferung an Länder-/Regionscode** definiert ist, dann wird die **Standarddebitorennr.** verwendet, unabhängig von den Einstellungen in den Feldern **Kundenimport von Shopify** und **Kundenzuordnungstyp**. Weitere Informationen unter [Debitorenvorlage pro Land](synchronize-customers.md#customer-template-per-countryregion).
2. Wenn der **Kundenimport von Shopify** auf *Keine* festgelegt ist und die **Standardkunden-Nr.** auf der Seite **Shopify-Shop-Karte** definiert sind, wird die **Standarddebitorennr.** verwendet.

Die nächsten Schritte hängen von der **Kundenzuordnung Typ** ab.

* Wenn dies **Nehmen Sie immer den Standardkunden** ist, dann verwendet der Konnektor den in der **Standarddebitorennr.** definierten Debitor Feld auf der Seite **Shopify Shop-Karte**.
* **Nach E-Mail/Telefon**, der Konnektor versucht, den bestehenden Kunden zuerst nach der ID, dann nach der E-Mail und dann nach der Telefonnummer zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.
* **Nach Rechnungsinformationen** versucht der Konnektor, den bestehenden Kunden zunächst über die ID und dann über die Rechnungsadressinformationen zu finden. Wenn der Debitor nicht gefunden wird, erstellt der Konnektor einen neuen Debitor.

> [!NOTE]  
> Der Konnektor verwendet die Informationen aus der Rechnungsadresse und erstellt den Rechnungsempfänger in [!INCLUDE[prod_short](../includes/prod_short.md)]. Der Verk. an Debitor ist derselbe wie Rechnung an Debitor.

Für B2B-Aufträge ist der Flow ähnlich, allerdings verwendet der Konnektor die Felder **Standardmandantennr.**, **Mandantenimport aus Shopify**, **Mandantenzuordnungstyp** auf der Seite **Shopify Shop-Karte**. Beachten Sie, dass es keine **Standardmandantennr.** in der **Shopify-Kundenvorlage** gibt, da im B2B-Bereich erwartet wird, dass es benannte Debitoren gibt.

### Unterschiedliche Bearbeitungsregeln für Aufträge

Möglicherweise möchten Sie Aufträge anhand einer Regel anders verarbeiten. Beispielsweise sollte bei Aufträgen über einen bestimmten Vertriebskanal wie POS der Standarddebitor verwendet werden, Sie möchten jedoch, dass Ihr Onlineshop über echte Informationen über den Debitor verfügt.

Eine Möglichkeit, dieser Anforderung gerecht zu werden, besteht darin, eine zusätzliche Shopify Shop-Karte zu erstellen und Filter auf der Anfrageseite **Aufträge von Shopify synchronisieren** zu verwenden.

Beispiel: Sie haben einen Onlineshop und einen Shopify POS. Für Ihren POS möchten Sie einen festen Debitor verwenden, für Ihren Onlineshop möchten Sie jedoch Debitoren in [!INCLUDE[prod_short](../includes/prod_short.md)] erstellen. Das folgende Verfahren listet die allgemeinen Schritte auf. Weitere Informationen finden Sie in den entsprechenden Hilfeartikeln.

1. Erstellen Sie einen Shopify Shop mit dem Namen *STORE* und verknüpfen Sie ihn mit Ihrem Shopify Konto.
1. Konfigurieren Sie die Artikel-/Produktsynchronisierung, sodass dieser Shop Produktinformationen verwaltet.
1. Geben Sie an, dass Debitoren mit Aufträgen importiert werden. Der Connector soll Debitoren finden, indem er nach deren E-Mail-Adresse sucht. Wenn keine Adresse gefunden wird, wird mithilfe der Debitorenvorlage ein neuer Debitor erstellt.
1. Erstellen Sie einen Shopify Shop mit dem Namen *POS* und verknüpfen Sie ihn mit demselben Shopify Konto.
1. Stellen Sie sicher, dass die Artikel-/Produktsynchronisierung deaktiviert ist.
1. Wählen Sie den Connector aus, der den Standarddebitor verwendet.
1. Erstellen Sie einen wiederkehrenden Auftragswarteschlangeneintrag für Bericht 30104 **Aufträge von Shopify synchronisieren**. Wählen Sie **STORE** im Feld **Shopify Shop-Code** aus und verwenden Sie Filter, um alle Aufträge außer denen zu erfassen, die der POS-Vertriebskanal erstellt. Zum Beispiel: **<>-Verkaufsstelle**
1. Erstellen Sie einen wiederkehrenden Auftragswarteschlangeneintrag für Bericht 30104 **Aufträge von Shopify synchronisieren**. Wählen Sie **POS** im Feld **Shopify Shop-Code** aus und verwenden Sie Filter, um Aufträge zu erfassen, die vom POS-Vertriebskanal generiert wurden. Zum Beispiel: **<>Verkaufsstelle**.

Jede Auftragswarteschlange importiert und verarbeitet Aufträge innerhalb der definierten Filter und verwendet die Regeln der entsprechenden Shopify Shop-Karte. Sie erstellen beispielsweise Verkaufsstellenaufträge für den Standarddebitor.

> [!Important]
> Um Konflikte bei der Verarbeitung von Aufträgen zu vermeiden, verwenden Sie für beide Auftragswarteschlangeneinträge dieselbe Auftragswarteschlangenkategorie.

### Auswirkung der Bearbeitung von Bestellungen

In Shopify:

|Bearbeiten|Auswirkungen auf Shopify-Aufträge, die noch nicht in [!INCLUDE[prod_short](../includes/prod_short.md)] bearbeitet wurden | Auswirkungen auf Shopify-Aufträge, die bereits in [!INCLUDE[prod_short](../includes/prod_short.md)] bearbeitet wurden |
|------|-----------|-----------|
|Den Erfüllungsort ändern | Der Auftragserfüllungs-Standort ist mit [!INCLUDE[prod_short](../includes/prod_short.md)] synchronisiert. | Der Auftragserfüllungs-Standort ist mit [!INCLUDE[prod_short](../includes/prod_short.md)] synchronisiert.|
|Bearbeiten Sie eine Bestellung und erhöhen Sie die Menge|Der importierte Auftrag verwendet eine neue Menge.| Der Konnektor erkennt die Änderungen und markiert die Aufträge. |
|Bearbeiten Sie eine Bestellung und verringern Sie die Menge|Der importierte Auftrag verwendet eine neue Menge. Eine Shopify-Rückerstattung mit einem Betrag von 0 wird importiert, der nicht in eine Gutschrift umgewandelt werden kann.| Der Konnektor erkennt die Änderungen und markiert die Aufträge. |
|Bearbeiten Sie eine Bestellung und entfernen Sie einen bestehenden Artikel |Entfernte Artikel werden nicht importiert. Eine Shopify-Rückerstattung mit einem Betrag von 0 wird importiert, der nicht in eine Gutschrift umgewandelt werden kann.| Der Konnektor erkennt die Änderungen und markiert die Aufträge. |
|Bearbeiten Sie eine Bestellung und fügen Sie einen neuen Artikel hinzu | Ursprüngliche und hinzugefügte Elemente werden importiert. | Der Konnektor erkennt die Änderungen und markiert die Aufträge. |
|Bestellung bearbeiten: ausführen, Zahlungsinformationen aktualisieren | Der Auftragskopf wird aktualisiert. |Der Auftragskopf wird aktualisiert. Die Erfüllung wird nicht mit Shopify synchronisiert.|
|Bezahlten Auftrag stornieren | Der Auftragskopf wird aktualisiert und muss separat verarbeitet werden |Der Konnektor erkennt die Änderungen und markiert die Aufträge. |
|Unbezahlten Auftrag stornieren | Entfernte Artikel werden nicht importiert. Eine Shopify-Rückerstattung mit einem Betrag von 0 wird importiert, der nicht in eine Gutschrift umgewandelt werden kann. |Der Konnektor erkennt die Änderungen und markiert die Aufträge. |

Falls ein Auftrag bereits in [!INCLUDE[prod_short](../includes/prod_short.md)] verarbeitet wurde, zeigt der Konnektor die folgende Fehlermeldung an: *Der Auftrag wurde bereits in Business Central verarbeitet, aber es wurde eine Bearbeitung von Shopify empfangen. Die Änderungen wurden nicht in den verarbeiteten Auftrag in Business Central übernommen. Aktualisieren Sie die verarbeiteten Belege, damit sie mit den empfangenen Daten von Shopify übereinstimmen. Wenn Sie die Synchronisierung erzwingen möchten, verwenden Sie die Aktion „Aufträge von Shopify synchronisieren“ auf der Shopify-Auftragskartenseite.*

Abhängig vom Status des erstellten Verkaufsbelegs können Sie folgende Aktionen ausführen:

1. Erstellten Verkaufsbeleg löschen
2. Wählen Sie die Aktion **Verknüpfung verarbeiteter Belege aufheben** aus, um den Indikator **Verarbeitet** zurückzusetzen.
3. Wählen Sie die Aktion **Auftrag von Shopify synchronisieren** zum Aktualisieren einzelner Bestellungen mit aktuellen Daten von Shopify aus.

In [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Bearbeiten|Auswirkungen|
|------|-----------|
|Ändern Sie den Standort zu einem anderen Standort. Sendung buchen. | Der Auftrag wird als erfüllt markiert. Auftragserfüllungsort von Shopify wird verwendet. |
|Menge verkleinern Sendung buchen. | Die Reihenfolge Shopify wird als teilweise erfüllt gekennzeichnet. |
|Menge erhöhen. Sendung buchen. | Die Auftragserfüllung wird nicht mit Shopify synchronisiert. Das Gleiche gilt, wenn die Auftragserfüllung in Shopify aufgeteilt, aber als eine Zeile in [!INCLUDE[prod_short](../includes/prod_short.md)] verarbeitet wurde. |
|Ein neues Element hinzufügen. Sendung buchen. | Die Reihenfolge Shopify wird als erfüllt markiert. Neue Zeilen werden nicht hinzugefügt. |

## Lieferungen mit Shopify synchronisieren

Wenn ein Verkaufsauftrag, der aus einem Shopify-Auftrag erstellt wurde, versandt wird, können Sie die Sendungen mit Shopify synchronisieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](../media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Sendungen mit Shopify synchronisieren** ein und wählen Sie dann den entsprechenden Link.
2. Definieren Sie die Filter für Sendungen nach Bedarf. Sie können zum Beispiel eine Sendung aktualisieren, die zu einem bestimmten Datum gebucht wurde.
3. Wählen Sie **OK** aus.

Die Bestellung in Shopify wird als erfüllt markiert. Der Debitor erhält automatisch eine Versandbenachrichtigung per E-Mail oder Textnachricht (SMS). Wenn ein Zusteller und ein Verfolgungscode für die Lieferung angegeben sind, sind die Verfolgungsinformationen in der E-Mail enthalten.

Alternativ können Sie die Aktion **Sync Sendungen** auf den Seiten Shopify Verkaufsaufträge oder Shopify Shop verwenden.

Sie können die Aufgabe für eine automatische Ausführung planen. Erfahren Sie mehr unter [Planen Sie wiederkehrende Aufgaben](background.md#to-schedule-recurring-tasks).

> [!Important]
> Der Lagerplatz, einschließlich des leeren Lagerplatzes, der in der Zeile Gebuchte Sendung definiert ist, muss einen passenden Datensatz im Shopify Standort haben. Andernfalls wird diese Zeile nicht an Shopify zurückgeschickt. Erfahren Sie mehr unter [Zuordnung von Lagerplätzen](synchronize-orders.md#location-mapping).

Denken Sie daran, **Bestellungen aus Shopify** auszuführen, um den Erfüllungsstatus der Bestellung in [!INCLUDE[prod_short](../includes/prod_short.md)] zu aktualisieren. Die Konnektor-Funktionalität archiviert auch vollständig bezahlte und erfüllte Aufträge sowohl in Shopify als auch in [!INCLUDE[prod_short](../includes/prod_short.md)], sofern die Bedingungen erfüllt sind. 

### Zusteller und Verfolgungs-URL

Wenn das Dokument **Gebuchte Verkaufslieferung** den **Versandagentencode** und/oder die **Paketverfolgungsnummer** enthält, werden diese Informationen an Shopify und an den Kunden in der Versandbestätigungs-E-Mail gesendet.

Die verfolgende Firma wird auf der Grundlage des Datensatzes des Zustellers mit der folgenden Folge (von oben nach unten) eingetragen:

1. **Shopify-Nachverfolgungsunternehmen**
1. **Name**
1. **Code**

Wenn das Feld **Paketverfolgungs-URL** für den Datensatz des Zustellers ausgefüllt ist, dann enthält die Versandbestätigung ebenfalls eine Verfolgungs-URL.

## Rückgaben und Rückerstattungen

Bei einer Integration zwischen Shopify und [!INCLUDE[prod_short](../includes/prod_short.md)] ist es wichtig, möglichst viele Geschäftsdaten synchronisieren zu können. Dadurch ist es einfacher, Ihre Finanzen und Lagerebenen in [!INCLUDE[prod_short](../includes/prod_short.md)] auf dem neuesten Stand zu halten. Zu den Daten, die Sie synchronisieren können, gehören Rückgaben und Rückerstattungen, die im Shopify Administrator oder Shopify POS erfasst wurden.

Rückgaben und Rückerstattungen werden mit den zugehörigen Auftägen importiert, wenn Sie den Verarbeitungstyp auf der Shopify Shop-Karte aktiviert haben.

Rückgaben werden nur zu Informationszwecken importiert. Mit ihnen ist keine Verarbeitungslogik verbunden.

Finanz- und gegebenenfalls Lagerbuchungen werden über Rückerstattungen abgewickelt. Rückerstattungen können sich auf Produkte oder nur auf Beträge beziehen, beispielsweise wenn sich ein Händler entscheidet, Versandkosten oder einen anderen Betrag zu erstatten.

Sie können Verkaufsgutschriften für Rückerstattungen erstellen. Die Gutschriften können folgende Zeilentypen haben:

|Typ|Anz.|Kommentar|
|-|-|-|
|Sachkonto|Konto für verkaufte Geschenkkarte| Für Rückerstattungen im Zusammenhang mit Geschenkkarten verwenden.|
|Sachkonto|Erstattungskonto nicht eingelagert | Für Rückerstattungen im Zusammenhang mit Produkten verwenden, die nicht wieder eingelagert wurden. |
|Option |Artikelnummer| Für Rückerstattungen im Zusammenhang mit Produkten verwenden, die wieder eingelagert wurden. Gültig für direkte Rückerstattungen oder für mit Rückerstattungen verbundene Rückerstattungen. Der Lagerortcode für die Gutschrift-Zeile wird basierend auf dem für den Rückgabelagerort ausgewählten Wert festgelegt.|
|Sachkonto| Erstattungskonto | Für andere Rückerstattungsbeträge verwenden, die nichts mit Produkten oder Geschenkkarten zu tun haben. Zum Beispiel Trinkgelder oder wenn Sie in Shopify manuell einen zu erstattenden Betrag angegeben haben. |

> [!Note]
> Die auf der **Shopify Shop-Karte** festgelegte Rückgabelagerorte, einschließlich leerer Lagerorte, werden auf der erstellten Gutschrift verwendet. Das System ignoriert die ursprünglichen Lagerorte aus Aufträgen oder Lieferungen.

## Geschenkkarten

Im Shopify-Shop können Sie Geschenkgutscheine verkaufen, mit denen echte Produkte bezahlt werden können.

Wenn Sie mit Geschenkkarten arbeiten, ist es wichtig, dass Sie im Fenster **Shopify Shop-Karte** einen Wert in das Feld **Geschenkkartenkonto** eingeben. Die verkaufte Geschenkkarte wird zusammen mit den entsprechenden Bestellungen synchronisiert. Eine angewendete Geschenkkarte wird ebenfalls mit der Bestellung importiert, jetzt jedoch als Transaktion. Beachten Sie, dass die Geschenkkarte den Rechnungsbetrag nicht reduziert.

Um die ausgegebenen und angewendeten Geschenkkarten zu überprüfen, wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Geschenkkarten** ein, und wählen Sie dann den entsprechenden Link.

## Siehe auch

[Erste Schritte mit dem Shopify-Konnektor](get-started.md)  
