---
title: 'Vorgehensweise: Zusammenfassen von Lieferungen in einer einzelnen Rechnung | Microsoft Docs'
description: Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6a9f4d6ee49b8958b3dcc33697db5ce0d77ae2c8
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312028"
---
# <a name="combine-shipments-on-a-single-invoice"></a>Zusammenfassen von Lieferungen in einer einzelnen Rechnung
Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden.  

 Bevor Sie eine Sammelrechnung erstellen können, müssen Sie mehr als eine Verkaufslieferung für den gleichen Debitor in der gleichen Währung gebucht haben. Anders ausgedrückt, Sie müssen zwei oder mehr Verkaufsaufträge erstellt und als geliefert (aber nicht fakturiert) gebucht haben. Um Lieferungen zu kombinieren, muss das Kontrollkästchen **Sammelrechnung** im Inforegister **Lieferung** der Karte **Debitor** aktiviert sein.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>So kombinieren Sie Lieferungen manuell auf einer einzigen Rechnung:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkaufsrechnung** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).
3. Wählen Sie im Feld **Verk. an Deb.-Nr.** Feld, geben Sie den Debitor ein, der die Rechnung für die gelieferten Artikel erhält.  
4. Klicken Sie im Inforegister **Zeilen** und wählen die  Aktionen **Warenverandszeilen holen**.  
5. Wählen Sie die Lieferzeile aus, die in die Rechnung aufgenommen werden soll:  

    - Um alle Zeilen einzufügen, wählen Sie alle Zeilen aus, und wählen Sie die Schaltfläche **OK**.  
    - Um spezifische Zeilen einzufügen, wählen Sie die Zeilen aus, und wählen Sie die Schaltfläche **OK**. Sie können die STRG-Taste verwenden, um mehrere nicht unmittelbar aufeinander folgende Zeilen auszuwählen.  

    Wenn Sie eine falsche Lieferzeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Rechnung löschen und die Funktion **Lieferzeilen holen** erneut ausführen.  
7. Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>So kombinieren Sie Lieferungen automatisch in einer einzigen Rechnung:  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Versände kombinieren** ein, und wählen dann den zugehörigen Link aus. Die Anforderungsseite für die Stapelverarbeitung wird geöffnet.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie das Kontrollkästchen **Rechnungen buchen** aus.  
4.  Wählen Sie die Schaltfläche **OK** aus.  

> [!NOTE]  
>  Die Rechnungen müssen manuell gebucht werden, wenn das Kontrollkästchen **Rechnungen buchen** für die Stapelverarbeitung nicht aktiviert wurde.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Offene Verkaufsaufträge nach kombinierter Lieferungsbuchung entfernen 
Wenn Lieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Verkaufsrechnung erstellt. Das Feld **Menge fakturiert** auf dem Ursprungsrahmenauftrag oder dem Auftrag wird ausgehend von der fakturierten Menge aktualisiert.  

Werden Lieferungen auf diese Weise fakturiert, bleiben die Aufträge, aus denen die Lieferungen gebucht werden, weiterhin bestehen, auch wenn sie vollständig geliefert und fakturiert wurden.   

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verrechnete Verkaufsaufträge löschen** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie im Feld **Kontonummer** Filterfeld an, welche Verkaufsaufträge zu löschen sind.  
3. Wählen Sie die Schaltfläche **OK** aus.  

Sie können die einzelnen Verkaufsaufträge auch manuell löschen.  

Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. leere Verkaufsaufträge.

## <a name="see-also"></a>Siehe auch  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
