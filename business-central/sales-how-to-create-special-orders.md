---
title: So erstellen Sie Sonderaufträge
description: 'Hier erfahren Sie, wie Sie einen Sonderauftrag für einen bestimmten Katalogartikel erstellen, der an einen bestimmten Kunden versandt werden soll.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 02/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Spezialaufträge erstellen

Sie können einen Spezialauftrag für einen bestimmten Katalogartikel erstellen, der an einen bestimmten Debitoren geliefert werden soll. Ihr Kreditor liefert den Artikel an Ihr Lager und Sie können den Artikel dann an Ihren Debitoren weiterleiten, entweder unabhängig von anderen Artikeln oder zusammen mit anderen Artikeln in einem anderen Auftrag.  

Spezialaufträge setzen voraus, dass die Bestellung und der Verkaufsauftrag verknüpft sind, um sicherzustellen, dass der bestimmte Katalogartikel entnommen und an den Debitor geliefert wird.  

Bevor Sie diese Funktion verwenden können, müssen Sie die Karten für den Debitor, den Kreditor und die Artikel in dem Auftrag erstellen.  

## So erstellen Sie Spezialaufträge:

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsauftrag** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**. Erstellen Sie einen Verkaufsauftrag für den Artikel, und füllen Sie diesen aus. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
3.  Geben Sie auf dem Inforegister **Zeilen** die Verkaufszeile ein. Wählen Sie im Feld **Einkaufscode** einen Einkaufscode mit einem Häkchen im Feld **Spezialauftrag** aus .

    Sie müssen nun aus einem Bestellarbeitsblatt eine Bestellung erstellen.  
4. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") , geben Sie **Bestellarbeitsblätter** ein, und wählen Sie dann den entsprechenden Link aus.  
5. Wählen Sie die Aktion **Spezialauftrag** aus, und dann die Aktion **Auftrag holen**.  
6.  Auf der Seite **Aufträge holen** werden Ergebnisse angezeigt, wobei **Belegnr.** die Verkaufsauftragsnummer ist. Wählen Sie die Schaltfläche **OK** aus. Es wird eine Bestellarbeitsblattszeile für den Artikel erstellt.  
7.  Wählen Sie in der Bestellarbeitsblattszeile im Feld **Ereignismeldung** die Option **Neu** aus.  
8.  Auf der Seite **Bestellauftrags-Arbeitsblätter** wählen Sie **Aktionsnachricht ausführen** aus. Auf der Seite **Ereignismeld. durchf. - Best.** wird geöffnet. Wählen Sie die Schaltfläche **OK** aus.  

    Es erscheint eine Meldung, dass die Einkaufsbestellungen erstellt wurden. Wählen Sie die Schaltfläche **OK** aus.  

Eine als Spezialauftrag für einen Verkaufsauftrag erstellte Bestellung wird vom Planungssystem berücksichtigt, da es Nachfrage und Angebot ausgleicht. Die Bestellung (Angebot) bleibt also auch dann mit dem Auftrag (Nachfrage) verknüpft, wenn sich mit der Bestellung eine frühere Nachfrage decken ließe. Weitere Informationen finden Sie unter [Designdetails: Behandlungs-Wiederbeschaffungsverfahren](design-details-reservation-order-tracking-and-action-messaging.md).  

> [!NOTE]  
>  Sie können die Spezialauftragsfunktion nicht verwenden, wenn der Artikel bereits reserviert ist. Stellen Sie daher für Artikel, die im Rahmen von Spezialaufträgen verkauft werden, sicher, dass das Feld **Reserve** auf der Artikelkarte nicht auf **Immer** gesetzt ist.  

## Siehe auch

[Mit Katalogartikeln arbeiten](inventory-how-work-nonstock-items.md)  
[Verkauf](sales-manage-sales.md)  
[Direktlieferungen machen](sales-how-drop-shipment.md)   
[Designdetails: Wiederbeschaffungsverfahren](design-details-reservation-order-tracking-and-action-messaging.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
