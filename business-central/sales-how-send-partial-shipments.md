---
title: Teillieferungen verarbeiten
description: 'Die Lieferungen von Verkaufsaufträgen können in Business Central mit Teillieferungen verarbeitet werden, indem Versandhinweis- und Zu liefern-Felder verwendet werden.'
author: brentholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 02/14/2024
ms.author: bholtorf
ms.reviewer: bholtorf
---
# <a name="process-partial-shipments"></a>Teillieferungen verarbeiten

Bei einer Teillieferung wird eine Bestellung nicht auf einmal versandt. Sie liefern z. B. bei einem Auftrag von 100 Einheiten sofort 40 Einheiten und 60 Einheiten zu einem späteren Zeitpunkt. Es gibt keine Begrenzung für die Anzahl der Lieferungen, die für einen Auftrag gebucht werden können.

Vorher können Sie jedoch Teillieferungen in [!INCLUDE [prod_short](includes/prod_short.md)] verwenden, müssen Sie angeben, dass der Kunde Teillieferungen akzeptiert, indem Sie **Versandhinweis** auf der **Debitorenkarte** festlegen. Alternativ, wenn der Debitor nur komplette Lieferungen akzeptiert, dann aber eine Teillieferung für einen bestimmten Kundenauftrag wünscht oder zustimmt, können Sie das Feld **Versandhinweisen** vor dem Buchen ändern.

Standardmäßig, setzt [!INCLUDE [prod_short](includes/prod_short.md)] das Feld auf der **Debitorenkarte** als **Teilweise**, wodurch Teillieferungen möglich sind. Wenn jedoch das Feld zur Angabe von **Vollständig** angepasst wurde, wird das Feld **Zu liefern** Verkaufsaufträgen für diesen Debitor als gesperrt angezeigt.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## <a name="see-also"></a>Siehe auch

[Produkte mit einem Verkaufsauftrag des Debitors verkaufen](sales-how-sell-products.md)  
[Versenden von Artikeln](warehouse-how-ship-items.md)  
[Direktlieferungen machen](sales-how-drop-shipment.md)  
[Verkauf](sales-manage-sales.md)  
[Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md)  
[Verwaltung](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
