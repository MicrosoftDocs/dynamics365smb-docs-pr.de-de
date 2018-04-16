---
title: 'Vorgehensweise: Zusammenfassen von Lieferungen in einer einzelnen Rechnung | Microsoft Docs'
description: "Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c9f2464014f2078f2a86f2e7d8a72873fa4015a8
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a>Zusammenfassen von Lieferungen in einer einzelnen Rechnung
Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden.  

 Bevor Sie eine Sammelrechnung erstellen können, müssen Sie mehr als eine Verkaufslieferung für den gleichen Debitor in der gleichen Währung gebucht haben. Anders ausgedrückt, Sie müssen zwei oder mehr Verkaufsaufträge erstellt und als geliefert (aber nicht fakturiert) gebucht haben. Um Lieferungen zu kombinieren, muss das Kontrollkästchen **Sammelrechnung** im Inforegister **Lieferung** der Karte **Debitor** aktiviert sein.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>So kombinieren Sie Lieferungen manuell auf einer einzigen Rechnung:  
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsrechnung** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie die Aktion **Neu** aus. Weitere Informationen finden Sie unter [Verkaufsrechnungen](sales-how-invoice-sales.md).
3. Wählen Sie im Feld **Verk. an Deb.-Nr.** Feld, geben Sie den Debitor ein, der die Rechnung für die gelieferten Artikel erhält.  
4. Klicken Sie im Inforegister **Zeilen** und wählen die  Aktionen **Warenverandszeilen holen**.  
5. Wählen Sie die Lieferzeile aus, die in die Rechnung aufgenommen werden soll:  

   - Um alle Zeilen einzufügen, wählen Sie alle Zeilen aus, und wählen Sie die Schaltfläche **OK**.  
   - Um spezifische Zeilen einzufügen, wählen Sie die Zeilen aus, und wählen Sie die Schaltfläche **OK**. Sie können die STRG-Taste verwenden, um mehrere nicht unmittelbar aufeinander folgende Zeilen auszuwählen.  

     Wenn Sie eine falsche Lieferzeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Rechnung löschen und die Funktion **Lieferzeilen holen** erneut ausführen.  
6. Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>So kombinieren Sie Lieferungen automatisch in einer einzigen Rechnung:  
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Versand kombinieren** ein. Wählen Sie dann den zugehörigen Link aus. Das Anforderungsfenster "Batchauftrag" wird geöffnet.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie das Kontrollkästchen **Rechnungen buchen** aus.  
4. Wählen Sie die Schaltfläche **OK** aus.  

> [!NOTE]  
>  Die Rechnungen müssen manuell gebucht werden, wenn das Kontrollkästchen **Rechnungen buchen** für die Stapelverarbeitung nicht aktiviert wurde.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Offene Verkaufsaufträge nach kombinierter Lieferungsbuchung entfernen 
Wenn Lieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Verkaufsrechnung erstellt. Das Feld **Menge fakturiert** auf dem Ursprungsrahmenauftrag oder dem Auftrag wird ausgehend von der fakturierten Menge aktualisiert.  

Werden Lieferungen auf diese Weise fakturiert, bleiben die Aufträge, aus denen die Lieferungen gebucht werden, weiterhin bestehen, auch wenn sie vollständig geliefert und fakturiert wurden.   

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Ausgestellte Kundenrechnung löschen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie im Feld **Kontonummer** Filterfeld an, welche Verkaufsaufträge zu löschen sind.  
3. Wählen Sie die Schaltfläche **OK** aus.  

Sie können die einzelnen Verkaufsaufträge auch manuell löschen.  

Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. leere Verkaufsaufträge.

## <a name="see-also"></a>Siehe auch  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

