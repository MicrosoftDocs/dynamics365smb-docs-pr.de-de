---
title: so fassen Sie Wareneingänge zusammen | Microsoft Docs
description: Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie die Funktion Sammelgutschrift verwenden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: c6a6707c9968bca856fda51984283277b27e8e84
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798082"
---
# <a name="combine-receipts-on-a-single-invoice"></a>Zusammenfassen von Lieferungen in einer einzelnen Rechnung
Wenn Sie mehrere Einkaufslieferungen gleichzeitig fakturieren möchten, können Sie die Funktion **Sammelgutschrift** verwenden.  

Bevor Sie eine zusammengefassten Einkaufslieferung erstellen können, müssen Sie mehrere Einkaufslieferungen für den gleichen Debitor in der gleichen Währung gebucht haben. Anders ausgedrückt: Sie müssen mindestens zwei Einkaufsbestellungen ausgefüllt und als geliefert (aber nicht fakturiert) gebucht haben.  

Wenn Einkaufslieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Einkaufsrechnung erstellt. Das Feld **Menge fakturiert** auf der Ursprungseinkaufsbestellung oder der Rahmenbestellung wird ausgehend von der fakturierten Menge aktualisiert. Der ursprüngliche Beleg wird jedoch nicht gelöscht, auch wenn er vollständig geliefert und fakturiert wurde, und Sie müssen daher den Einkaufsbeleg löschen.  

## <a name="to-combine-receipts"></a>So fassen Sie Wareneingänge zusammen  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufrechnung** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).  
3. Klicken Sie im Inforegister **Zeilen** und wählen die  Aktionen **Wareneingangszeilen holen**.  
4. Wählen Sie die Wareneingangszeilen aus, die in der Rechnung enthalten sein sollen.  

    Wenn Sie eine falsche Wareneingangszeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Einkaufsrechnung löschen und die Funktion **Wareneingangszeilen holen** erneut ausführen.  
5. Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a>Offene Einkaufsreklamationen nach kombinierter Lieferungsbuchung entfernen  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verrechnete Verkaufsaufträge löschen** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Wählen Sie die Schaltfläche **OK** aus.  

Alternativ löschen Sie die jeweiligen Aufträge manuell.

Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. Rahmenbestellungen.

## <a name="see-also"></a>Siehe auch  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
