---
title: Einkaufsrechnungen sofort ausgleichen
description: Wenn Sie den Kreditor bar oder per Scheck bezahlen, können Sie die notwendigen Buchungen gleichzeitig bei der Buchung der Rechnung vornehmen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: 60d3cf3c9e141c8df36eaca2c1975b696fdb105b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387249"
---
# <a name="settle-purchase-invoices-promptly"></a>Einkaufsrechnungen sofort ausgleichen

Wenn Sie den Kreditor bar oder per Scheck bezahlen, können Sie die notwendigen Buchungen gleichzeitig bei der Buchung der Rechnung vornehmen.  

> [!NOTE]  
> Wenn Sie häufig Einkaufsrechnungen bar, per Scheck oder Banküberweisung bezahlen, ist es sinnvoll, eine bestimmte Zahlungsform mit einem Gegenkonto einzurichten und diese Methode im Feld **Zahlungsform** auf der Kreditorenkarte einzugeben. Die entsprechende Gegenkontonummer wird automatisch auf dem Rechnungskopf eingefügt, wenn Sie eine neue Rechnung erstellen. Weitere Informationen finden Sie unter [Zahlungsformen definieren](finance-payment-methods.md).  

## <a name="to-settle-purchase-invoices-promptly"></a>So gleichen Sie Einkaufsrechnungen sofort aus

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Einkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Um entweder bar oder per Banktransfer zu bezahlen, geben Sie die Nummer des Sachkontos für Barzahlungen oder die des Bankkontos in dem Feld **Gegenkontonr.** an.  

> [!IMPORTANT]  
> Die Felder **Gegenkontoart** und **Gegenkontonr.** sind im Rechnungskopf nicht im Standard enthalten. Um die Zahlung einer Rechnung zu buchen, müssen Sie sich an einen Microsoft-Partner wenden, der die Felder per Code hinzufügen kann.  
>
> Diese Anpassung ist nur erforderlich, wenn Sie keine Gegenkonten zu den Zahlungsformen, wie oben beschrieben, angeben.

## <a name="see-also"></a>Siehe auch

[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]