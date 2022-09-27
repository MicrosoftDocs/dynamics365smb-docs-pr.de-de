---
title: Zusammenfassen von Lieferungen in einer einzelnen Rechnung
description: Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie die Funktion Sammelgutschrift verwenden.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 136, 145, 146, 9308
ms.date: 08/03/2022
ms.author: edupont
ms.openlocfilehash: dc1fa2e308ce0920815a5766d4e077a2eb0ce62a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534534"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Zusammenfassen von Lieferungen in einer einzelnen Rechnung

Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie mehrere Belegposten in der Rechnung auswählen.  

Bevor Sie eine zusammengefassten Einkaufslieferung erstellen können, müssen Sie mehrere Einkaufslieferungen für den gleichen Debitor in der gleichen Währung gebucht haben. Anders ausgedrückt: Sie müssen mindestens zwei Einkaufsbestellungen ausgefüllt und als geliefert (aber nicht fakturiert) gebucht haben.  

Wenn Einkaufslieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Einkaufsrechnung erstellt. Das Feld **Menge fakturiert** auf der Ursprungseinkaufsbestellung oder der Rahmenbestellung wird ausgehend von der fakturierten Menge aktualisiert. Der ursprüngliche Beleg wird jedoch nicht gelöscht, auch wenn er vollständig geliefert und fakturiert wurde, und Sie müssen daher den Einkaufsbeleg löschen.  

> [!NOTE]
> Die resultierende Einkaufsrechnung kann später nicht mehr korrigiert oder storniert werden. Wenn Sie eine auf diese Weise erstellte Einkaufsrechnung ändern möchten, müssen Sie Einkaufgutschriften verwenden. Weitere Informationen finden Sie unter [Ändern oder löschen von unbezahlten Einkaufsrechnungen](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts"></a>So fassen Sie Wareneingänge zusammen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).  
3. Klicken Sie im Inforegister **Zeilen** und wählen die  Aktionen **Wareneingangszeilen holen**.  
4. Wählen Sie die Wareneingangszeilen aus, die in der Rechnung enthalten sein sollen.  

    Wenn Sie eine falsche Wareneingangszeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Einkaufsrechnung löschen und die Funktion **Wareneingangszeilen holen** erneut ausführen.  
5. Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Offene Einkaufsreklamationen nach kombinierter Lieferungsbuchung entfernen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Löschen Sie Erledigte Bestellungen** ein und wählen Sie den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Wählen Sie die Schaltfläche **OK** aus.  

Alternativ löschen Sie die jeweiligen Aufträge manuell.

Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. Rahmenbestellungen.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/processing-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Einkauf](purchasing-manage-purchasing.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
