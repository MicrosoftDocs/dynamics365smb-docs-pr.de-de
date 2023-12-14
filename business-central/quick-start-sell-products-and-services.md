---
title: Verkauf Schnellstart (enthält Video)
description: 'Erfahren Sie, wie Sie die ersten wichtigen Felder zu Produkten und Kunden in Business Central ausfüllen, damit Sie mit Ihren Verkaufsprozessen beginnen können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: bholtorf
---

# <a name="sales-quick-start"></a>Schnellstart Verkauf

Um Produkte und Dienstleistungen verkaufen zu können, müssen Sie zunächst Artikel und Kunden festlegen. Sobald das geschehen ist, können Sie mit der Registrierung von Verkaufsaufträgen und dem Versand von Rechnungen beginnen.

## <a name="set-up-items-to-sell"></a>Festlegen von zu verkaufenden Elementen

Dieses Video zeigt Ihnen, wie Sie unter [!INCLUDE[prod_short](includes/prod_short.md)] einen Artikel zum Verkauf festlegen.

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### <a name="set-up-a-new-item"></a>Einen neuen Artikel festlegen

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Weitere Informationen und zusätzliche Möglichkeiten, die Sie beim Einrichten von Artikeln nutzen können, finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).  

## <a name="set-up-customers"></a>Kunden festlegen

Dieses Video zeigt, wie Sie in [!INCLUDE[prod_short](includes/prod_short.md)] einen neuen Debitor festlegen.  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### <a name="set-up-a-new-customer"></a>Einrichten eines neuen Debitors

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Weitere Informationen und zusätzliche Dinge, die Sie beim Einrichten von Kunden festlegen können, finden Sie unter [Neue Kunden registrieren](sales-how-register-new-customers.md)

## <a name="create-a-sales-order"></a>Einen Verkaufsauftrag erstellen

Wenn Sie etwas an einen Kunden verkaufen, haben Sie zwei Möglichkeiten. Die erste und einfachste ist, einfach eine Verkaufsrechnung zu erstellen. Wenn Ihr Verkaufsprozess jedoch komplexer ist, zum Beispiel wenn Sie nur Teile einer Bestellmenge versenden, verwenden Sie einen Verkaufsauftrag.

### <a name="to-create-a-sales-order"></a>So erstellen Sie einen Verkaufsauftrag

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 10.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Neu** aus, um einen neuen Eintrag zu erstellen.
3. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.

    Andere Felder auf der Seite **Verkaufsangebot** werden nun mit den Standardinformationen vom ausgewählten Debitor ausgefüllt.  

4. Füllen Sie auf der Seite **Verkaufsauftrag** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Wählen Sie im Inforegister **Zeilen** im Feld **Art** aus, welche Art des Produkts, der Kosten oder der Transaktion Sie für den Debitor mit der Verkaufszeile buchen werden.

6. Geben Sie im Feld **Nr.** die Nummer eines Lagerartikels oder Dienstes ein.

7. Geben Sie in dem Feld **Menge** die Anzahl des Artikels an, der verkauft werden soll.

8. Geben Sie im Feld **Zeilenrabatt in Prozent** einen Prozentsatz ein, wenn Sie dem Debitor einen Rabatt auf das Produkt gewähren möchten.

9. Um einen Kommentar zur Bestellzeile hinzuzufügen, den der Debitor auf dem gedruckten Verkaufsauftrag sehen kann, schreiben Sie einen Kommentar in das Feld **Beschreibung** in eine leere Zeile.

10. Wiederholen Sie die Schritte 5 bis 9 für jedes Element, das Sie an den Kunden verkaufen möchten.

11. Um nur einen Teil der Auftragsmenge zu liefern, geben Sie die Menge im Feld **Menge für Versand** ein. Der Wert wird in das Feld **Zu fakturierende Menge** kopiert.

12. Um nur einen Teil der Auftragsmenge zu fakturieren, geben Sie die Menge im Feld **Menge für Fakturierung** ein. Die zu fakturierende Menge kann nicht größer sein, als der Wert im Feld **Menge geliefert**.

13. Wenn die Verkaufsangebotszeilen ausgeführt werden, wählen Sie die Aktion **Buchen und Senden** aus.

Weitere Informationen und zusätzliche Möglichkeiten, die Sie beim Erstellen von Kundenverkaufsaufträgen haben, finden Sie unter [Produkte mit einem Verkaufsauftrag für Kunden verkaufen](sales-how-sell-products.md).  

## <a name="create-a-sales-invoice"></a>Eine Verkaufsrechnung erstellen

Wenn Sie eine Verkaufsrechnung erstellen und buchen, erstellen Sie nicht nur den Beleg, den Sie an den Kunden senden, sondern Sie erstellen auch die zugehörigen Mengen- und Wertangaben in [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="to-create-and-post-a-sales-invoice"></a>So erstellen und buchen Sie eine Verkaufsrechnung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 20.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.  

2. Wählen Sie **Neu** aus, um einen neuen Eintrag zu erstellen.

3. Geben Sie im Feld **Debitor** den Namen eines vorhandenen Debitors ein.

4. Füllen Sie auf der Seite **Verkaufsrechnung** die Felder wie benötigt aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Wählen Sie auf dem Inforegister **Zeilen** im Feld **Typ** aus, welche Art von Produkt, Gebühr oder Transaktion Sie für den Kunden mit der Verkaufszeile buchen möchten.

6. Geben Sie im Feld **Nr.** Feld, einen Datensatz auswählen, um entsprechend dem Wert im Feld **Art** zu buchen.

7. Geben Sie im Feld **Menge** ein, wie viele Einheiten des Produkts, der Kosten oder der Transaktion, in der Zeile des Debitors gespeichert werden soll.  

8. Wenn Sie Skonto gewähren möchten, geben Sie einen Prozentsatz im Feld **Zeilenrabatt %** ein. Der Wert im Feld **Zeilenbetrag** wird entsprechend aktualisiert.  

9. Wiederholen Sie die Schritte 5 bis 8 für jedes Produkt oder jede Gebühr, die Sie an den Debitoren verkaufen möchten.  

10. Geben Sie im Feld **Rabattbetrag in Rechnung stellen** einen Betrag ein, der vom Wert abgezogen werden soll, der im Feld **Total inklusive Mehrwertsteuer** im unteren Bereich der Rechnung angezeigt wird.

11. Wenn die Verkaufsrechnungszeilen ausgeführt werden, wählen Sie die Aktion **Buchen und Senden** aus.  

Weitere Informationen und zusätzliche Möglichkeiten beim Erstellen von Verkaufsrechnungen für Kunden finden Sie unter [Verkaufsrechnungen](sales-how-invoice-sales.md).

## <a name="see-also"></a>Weitere Informationen

[Business Central Schnellstarts](quick-start-business-central.md)  
[Vertrieb – Übersicht](sales-manage-sales.md)  
[Produkte mit einem Verkaufsauftrag des Debitors verkaufen](sales-how-sell-products.md)  
[Fakturieren eines Verkaufs](sales-how-invoice-sales.md)  
