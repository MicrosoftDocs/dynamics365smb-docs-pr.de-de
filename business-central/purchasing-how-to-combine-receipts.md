---
title: so fassen Sie Wareneingänge zusammen | Microsoft Docs
description: Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie die Funktion Sammelgutschrift verwenden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8c3158874dc83d634ea09cac986820c615c3924d
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758442"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Zusammenfassen von Lieferungen in einer einzelnen Rechnung

Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie die Funktion **Sammelgutschrift** verwenden.  

Bevor Sie eine zusammengefassten Einkaufslieferung erstellen können, müssen Sie mehrere Einkaufslieferungen für den gleichen Debitor in der gleichen Währung gebucht haben. Anders ausgedrückt: Sie müssen mindestens zwei Einkaufsbestellungen ausgefüllt und als geliefert (aber nicht fakturiert) gebucht haben.  

Wenn Einkaufslieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Einkaufsrechnung erstellt. Das Feld **Menge fakturiert** auf der Ursprungseinkaufsbestellung oder der Rahmenbestellung wird ausgehend von der fakturierten Menge aktualisiert. Der ursprüngliche Beleg wird jedoch nicht gelöscht, auch wenn er vollständig geliefert und fakturiert wurde, und Sie müssen daher den Einkaufsbeleg löschen.  

> [!NOTE]
> Die resultierende Einkaufsrechnung kann später nicht mehr korrigiert oder storniert werden. Wenn Sie eine auf diese Weise erstellte Einkaufsrechnung ändern möchten, müssen Sie Einkaufgutschriften verwenden. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Einkaufsrechnungen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>So fassen Sie Wareneingänge zusammen

1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Einkaufsrechnungen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).  
3. Klicken Sie im Inforegister **Zeilen** und wählen die  Aktionen **Wareneingangszeilen holen**.  
4. Wählen Sie die Wareneingangszeilen aus, die in der Rechnung enthalten sein sollen.  

    Wenn Sie eine falsche Wareneingangszeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Einkaufsrechnung löschen und die Funktion **Wareneingangszeilen holen** erneut ausführen.  
5. Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Offene Einkaufsreklamationen nach kombinierter Lieferungsbuchung entfernen

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Fakturierte Einkaufsbestellungen löschen** ein und wählen Sie den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Wählen Sie die Schaltfläche **OK** aus.  

Alternativ löschen Sie die jeweiligen Aufträge manuell.

Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. Rahmenbestellungen.

## <a name="see-also"></a>Siehe auch

[Einkauf](purchasing-manage-purchasing.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]