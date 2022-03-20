---
title: Direktlieferungen durchführen (enthält Video)
description: Beschreibt, wie Sie einen Verkaufsauftrag erstellen, der mit einer Bestellung verknüpft ist, um sicherzustellen, dass die Artikel vom Kreditor direkt an den Debitor versendet werden
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3fe45eb6403798a7e64b9604321440a2fff38c3f
ms.sourcegitcommit: 865b390b5571b08084bde93b539ec9898e201933
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8372043"
---
# <a name="make-drop-shipments"></a>Direktlieferungen machen

Eine Direktlieferung ist die Lieferung von Artikeln, von einem Ihrer Kreditoren direkt an einen Ihrer Debitoren.

Wenn ein Verkaufsauftrag für die Direktlieferung markiert ist und Sie einen Verkaufsauftrag erstellen, bei dem der Kunde im **Lief. an**-Feld, **Adresse Debitor** angegeben ist, können Sie die beiden Dokumente verknüpfen und so den Lieferanten anweisen, direkt an den Kunden zu senden.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>So erstellen Sie einen Verkaufsauftrag für eine Direktlieferung

Um eine Direktlieferung vorzubereiten, erstellen Sie einen normalen Verkaufsauftrag für einen Artikel und geben in der Verkaufsauftragszeile an, dass für den Verkauf Direktlieferung benötigt wird.

1. Legen Sie einen Verkaufsauftrag für einen Artikel an. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
2. Aktivieren Sie in der Verkaufsauftragszeile für den Direktlieferungsartikel das Kontrollkästchen **Direktlieferung**. Verwenden Sie die Funktion **Spalten auswählen**, wenn das Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>So erstellen Sie Bestellungen für Direktlieferungen:

Um eine Direktlieferung vorzubereiten, geben Sie auf der Bestellung an, dass sie an Ihren Kunden und nicht an Sie selbst versendet werden muss.

1. Erstellen Sie eine Bestellung. Füllen Sie keines dieser Felder in den Zeilen aus. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
2. Wählen Sie im Feld **Lief. an** **Adresse Debitor** aus.
3. Wählen Sie im Feld **Debitor** den Debitor aus, an den Sie verkaufen.
4. Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.
5. Auf der Seite **Verkaufsübersicht** wählen Sie den Auftrag aus, den Sie im Abschnitt [So erstellen Sie einen Verkaufsauftrag für Direktlieferung](#to-create-a-sales-order-for-drop-shipment) vorbereitet haben.
6. Wählen Sie die Schaltfläche **OK** aus.

Die Zeileninformation aus dem Auftrag werden in die Bestellzeile eingetragen.

Sie können nun den Kreditor anweisen, die Artikel an Ihren Debitoren zu versenden, indem Sie ihm beispielsweise die Bestellung als PDF-Datei senden. Wenn Ihr Kreditor eine Sendungsverfolgungsnummer oder ähnliche Informationen bereitstellt, können Sie diese in einer Bestellposition vom Typ *Kommentar* erfassen.  

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Um mehrere Bestellungen für Direktlieferungen zu erstellen

Sie können auch das Anforderungsarbeitsblatt verwenden, um die Bestellung für den Lieferanten zu erstellen. Der Vorteil der Verwendung des Anforderungsarbeitsblatts besteht darin, dass Bestellungen für alle ausstehenden Direktlieferungen erstellt werden können, sodass Sie nicht jede einzeln erstellen müssen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Bestellarbeitsblätter** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.
3. Wählen Sie die Schaltfläche **OK** aus.
4. Überprüfen Sie die Bestellpositionen und im Feld **Lieferanten-Nr.** wählen Sie den Lieferanten aus, der die erforderlichen Waren liefert. 
5. Wählen Sie zum Konvertieren überprüfter Zeilen in eine Einkaufsbestellung die Aktion **Ereignismeldung ausführen** aus.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>So zeigen Sie den verknüpften Auftrag aus der Bestellung an

* Wählen Sie die Verkaufsauftragszeile der Direktlieferung aus, dann die Aktion **Bestellung**, die Aktion **Direktlieferung** und die Aktion **Bestellung**.

## <a name="to-post-a-drop-shipment"></a>So buchen Sie eine Direktlieferung:

Wenn der Kreditor die Artikel geliefert hat, können Sie den Verkaufsauftrag als geliefert buchen. Sie können auch die Bestellung buchen, aber nur mit der Option **Erhalten** bis der Verkaufsauftrag fakturiert wurde.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie den Verkaufsauftrag, den Sie in [So erstellen Sie einen Verkaufsauftrag für Direktlieferung](#to-create-a-sales-order-for-drop-shipment) erstellt haben.
3. Geben Sie im Feld **Zu liefern** an, wieviele der Bestellmengen geliefert werden sollen, die gesamte Menge oder eine Teilmenge.
4. Wählen Sie die Aktion **Buchen** oder **Buchen und Senden** aus.
5. Wählen Sie dann entweder die Option **Liefern**, um zu einem späteren Zeitpunkt zu fakturieren oder **Liefern und Fakturieren**, um sofort zu fakturieren.

## <a name="see-also"></a>Siehe auch

[Spezialaufträge erstellen:](sales-how-to-create-special-orders.md)  
[Einkauf von Artikeln für einen Verkauf](purchasing-how-purchase-products-sale.md)  
[Produkte verkaufen](sales-how-sell-products.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Verkauf](sales-manage-sales.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]