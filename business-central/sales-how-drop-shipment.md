---
title: Direktlieferungen durchführen
description: 'Beschreibt, wie Sie einen Verkaufsauftrag erstellen, der mit einer Bestellung verknüpft ist, um sicherzustellen, dass die Artikel vom Kreditor direkt an den Debitor versendet werden'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: direct shipment
ms.date: 05/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-drop-shipments"></a>Direktlieferungen durchführen

Eine Direktlieferung ist die Lieferung von Artikeln, von einem Ihrer Kreditoren direkt an einen Ihrer Debitoren.

Wenn ein Verkaufsauftrag für die Direktlieferung markiert ist und Sie einen Verkaufsauftrag erstellen, bei dem der Kunde im **Lief. an**-Feld, **Adresse Debitor** angegeben ist, können Sie die beiden Dokumente verknüpfen und so den Lieferanten anweisen, direkt an den Kunden zu senden.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>So erstellen Sie einen Verkaufsauftrag für eine Direktlieferung

Um eine Direktlieferung vorzubereiten, erstellen Sie einen normalen Verkaufsauftrag für einen Artikel und geben in der Verkaufsauftragszeile an, dass für den Verkauf Direktlieferung benötigt wird.

1. Legen Sie einen Verkaufsauftrag für einen Artikel an. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
2. Aktivieren Sie in der Verkaufsauftragszeile für den Direktlieferungsartikel das Kontrollkästchen **Direktlieferung**. Wählen Sie alternativ im Feld **Einkaufscode** einen Einkaufscode mit einem Häkchen im Feld **Direktlieferung** aus.

> [!TIP]
> Das Kontrollkästchen „Direktlieferung“ und das Feld „Einkaufscode“ sind standardmäßig nicht in den Zeilen verfügbar. Sind sie es nicht, können Sie sie hinzufügen, indem Sie den Abschnitt der Seite personalisieren, die die Zeilen enthält. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>So erstellen Sie Bestellungen für Direktlieferungen:

Um eine Direktlieferung vorzubereiten, geben Sie auf der Bestellung an, dass sie an Ihren Kunden und nicht an Sie selbst versendet werden muss.

1. Erstellen Sie eine Bestellung. Füllen Sie keines dieser Felder in den Zeilen aus. Weitere Informationen finden Sie unter [Käufe erfassen](purchasing-how-record-purchases.md).
2. Wählen Sie im Feld **Lief. an** **Adresse Debitor** aus.
3. Wählen Sie im Feld **Debitor** den Debitor aus, an den Sie verkaufen.
4. Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.
5. Auf der Seite **Verkaufsübersicht** wählen Sie den Auftrag aus, den Sie im Abschnitt [So erstellen Sie einen Verkaufsauftrag für Direktlieferung](#to-create-a-sales-order-for-drop-shipment) vorbereitet haben.
6. Wählen Sie die Schaltfläche **OK** aus.

Die Zeileninformation aus dem Auftrag werden in die Bestellzeile eingetragen.

Sie können Ihren Kreditor jetzt anweisen, die Artikel direkt an den Debitor zu versenden. Sie können ihnen beispielsweise die Bestellung per E-Mail senden.

Wenn Ihr Kreditor zusätzliche Informationen wie eine Verfolgungsnummer bereitstellt, können Sie diese Informationen als Kommentar in einer Bestellposition hinzufügen. Um einer Zeile einen Kommentar hinzuzufügen, wählen Sie im Feld **Typ** die Option **Kommentar** aus, und geben Sie die Informationen anschließend in das Feld **Beschreibung** ein.  

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Um mehrere Bestellungen für Direktlieferungen zu erstellen

Sie können auch das Anforderungsarbeitsblatt verwenden, um Bestellungen zu erstellen. Der Vorteil der Verwendung des Anforderungsarbeitsblatts besteht darin, dass Bestellungen für alle ausstehenden Direktlieferungen erstellt werden können. Das heißt, sie müssen nicht jede Bestellung einzeln erstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") , geben Sie **Bestellarbeitsblätter** ein, und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.
3. Geben Sie bei Bedarf Filterkriterien für die Bestellungen ein, die Sie erhalten möchten, und wählen Sie dann die Schaltfläche **OK** aus.
4. Überprüfen Sie die Bestellpositionen und im Feld **Lieferanten-Nr.** wählen Sie den Kreditor aus, der die Waren liefert.
5. Wählen Sie zum Konvertieren der Zeilen in eine Einkaufsbestellung die Aktion **Ereignismeldung ausführen** aus.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>So zeigen Sie den verknüpften Auftrag aus der Bestellung an

Wählen Sie die Verkaufsauftragszeile der Direktlieferung aus, dann die Aktion **Bestellung**, die Aktion **Direktlieferung** und die Aktion **Bestellung**.

## <a name="to-post-a-drop-shipment"></a>So buchen Sie eine Direktlieferung:

Wenn der Kreditor die Artikel geliefert hat, können Sie den Verkaufsauftrag als geliefert buchen. Sie können auch die Bestellung buchen, aber nur mit der Option **Erhalten** bis der Verkaufsauftrag fakturiert wurde.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie den Verkaufsauftrag, den Sie in [So erstellen Sie einen Verkaufsauftrag für Direktlieferung](#to-create-a-sales-order-for-drop-shipment) erstellt haben.
3. Geben Sie im Feld **Zu liefern** an, wieviele der Bestellmengen geliefert werden sollen, die gesamte Menge oder eine Teilmenge.
4. Wählen Sie die Aktion **Buchen** oder **Buchen und Senden** aus.
5. Wählen Sie dann entweder die Option **Liefern**, um zu einem späteren Zeitpunkt zu fakturieren oder **Liefern und Fakturieren**, um sofort zu fakturieren.

> [!TIP]
> Vergessen Sie nicht, die Einkaufsrechnung zu buchen.

## <a name="see-also"></a>Siehe auch

[Spezialaufträge erstellen](sales-how-to-create-special-orders.md)  
[Artikel für einen Verkauf einkaufen](purchasing-how-purchase-products-sale.md)  
[Produkte verkaufen](sales-how-sell-products.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Verkauf](sales-manage-sales.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
