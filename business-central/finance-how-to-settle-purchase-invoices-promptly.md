---
title: Einkaufsrechnungen sofort ausgleichen
description: 'Wenn Sie den Kreditor bar oder per Scheck bezahlen, können Sie die notwendigen Buchungen gleichzeitig bei der Buchung der Rechnung vornehmen.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: '51, 9308'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="settle-purchase-invoices-promptly"></a>Einkaufsrechnungen sofort ausgleichen

Wenn Sie den Kreditor bar oder per Scheck bezahlen, können Sie die notwendigen Buchungen gleichzeitig bei der Buchung der Rechnung vornehmen.  

> [!NOTE]  
> Wenn Sie häufig Einkaufsrechnungen bar, per Scheck oder Banküberweisung bezahlen, ist es sinnvoll, eine bestimmte Zahlungsform mit einem Gegenkonto einzurichten und diese Methode im Feld **Zahlungsform** auf der Kreditorenkarte einzugeben. Die entsprechende Gegenkontonummer wird automatisch auf dem Rechnungskopf eingefügt, wenn Sie eine neue Rechnung erstellen. Weitere Informationen finden Sie unter [Zahlungsformen definieren](finance-payment-methods.md).  

## <a name="to-settle-purchase-invoices-promptly"></a>So gleichen Sie Einkaufsrechnungen sofort aus

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Um entweder bar oder per Banktransfer zu bezahlen, geben Sie die Nummer des Sachkontos für Barzahlungen oder die des Bankkontos in dem Feld **Gegenkontonr.** an.  

> [!IMPORTANT]  
> Die Felder **Gegenkontoart** und **Gegenkontonr.** sind im Rechnungskopf nicht im Standard enthalten. Um die Zahlung einer Rechnung zu buchen, müssen Sie sich an einen Microsoft-Partner wenden, der die Felder per Code hinzufügen kann.  
>
> Diese Anpassung ist nur erforderlich, wenn Sie keine Gegenkonten zu den Zahlungsformen, wie oben beschrieben, angeben.

## <a name="see-also"></a>Weitere Informationen

[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
