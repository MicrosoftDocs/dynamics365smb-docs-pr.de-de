---
title: 'Vorgehensweise: Zusammenfassen von Lieferungen in einer einzelnen Rechnung | Microsoft Docs'
description: 'Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/16/2021
ms.author: edupont
---
# <a name="combine-shipments-on-a-single-invoice" />Zusammenfassen von Lieferungen in einer einzelnen Rechnung

Wenn Sie mehr als eine Lieferung gleichzeitig fakturieren möchten, können Sie die Funktion zum Erstellen von Sammelrechnungen verwenden.  

Bevor Sie eine Sammelrechnung erstellen können, müssen Sie mehr als eine Verkaufslieferung für den gleichen Debitor in der gleichen Währung gebucht haben. Anders ausgedrückt, Sie müssen zwei oder mehr Verkaufsaufträge erstellt und als geliefert (aber nicht fakturiert) gebucht haben. 

## <a name="to-manually-combine-shipments-on-a-single-invoice" />So kombinieren Sie Lieferungen manuell auf einer einzigen Rechnung:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).
3. Wählen Sie im Feld **Verk. an Deb.-Nr.** Feld, geben Sie den Debitor ein, der die Rechnung für die gelieferten Artikel erhält.  
4. Klicken Sie im Inforegister **Zeilen** und wählen die Aktionen **Warenverandszeilen holen**.  
5. Wählen Sie die Lieferzeile aus, die in die Rechnung aufgenommen werden soll:  

    - Um alle Zeilen einzufügen, wählen Sie alle Zeilen aus, und wählen Sie die Schaltfläche **OK**.  
    - Um spezifische Zeilen einzufügen, wählen Sie die Zeilen aus, und wählen Sie die Schaltfläche **OK**. Sie können die STRG-Taste verwenden, um mehrere nicht unmittelbar aufeinander folgende Zeilen auszuwählen.  

    Wenn Sie eine falsche Lieferzeile ausgewählt haben oder von vorn beginnen möchten, können Sie einfach die Zeilen in der Rechnung löschen und die Funktion **Lieferzeilen holen** erneut ausführen.  
7. Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.  

> [!TIP]  
> Wenn Sie Aufträge versandt haben, bei denen die **Kunden-Nr.** von der **Rechnungsadresse** abweicht, werden diese Zeilen im Bericht **Sendungszeilen abrufen** nicht angezeigt. Verwenden Sie die Personalisierung, um das Feld **Verkauf an Kunde** auf der Seite hinzuzufügen und den Filter zu entfernen. Jetzt können Sie der Rechnung unabhängig vom Wert im Feld **Verkauf an Kunden-Nr.** Lieferzeilen hinzufügen, solange das Feld **Rechnung an Kunden-Nr.** Feld in den Versandzeilen mit dem Wert auf der Verkaufsrechnung übereinstimmt.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice" />So kombinieren Sie Lieferungen automatisch in einer einzigen Rechnung:

[!INCLUDE[prod_short](includes/prod_short.md)] wählt nur Verkaufsaufträge aus, bei denen **Sendungen kombinieren** gewählt ist. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Sammelrechnungen** ein und wählen Sie dann den zugehörigen Link. Die Anforderungsseite für die Stapelverarbeitung wird geöffnet.  
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie das Kontrollkästchen **Rechnungen buchen** aus.  
4. Wählen Sie die Schaltfläche **OK** aus.  

> [!NOTE]  
>  Die Rechnungen müssen manuell gebucht werden, wenn das Kontrollkästchen **Rechnungen buchen** für die Stapelverarbeitung nicht aktiviert wurde.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting" />Offene Verkaufsaufträge nach kombinierter Lieferungsbuchung entfernen

Wenn Lieferungen in einer Rechnung zusammengefasst und gebucht werden, wird für die fakturierten Zeilen eine gebuchte Verkaufsrechnung erstellt. Das Feld **Menge fakturiert** auf dem Ursprungsrahmenauftrag oder dem Auftrag wird ausgehend von der fakturierten Menge aktualisiert.  

Werden Lieferungen auf diese Weise fakturiert, bleiben die Aufträge, aus denen die Lieferungen gebucht werden, weiterhin bestehen, auch wenn sie vollständig geliefert und fakturiert wurden.   

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Erledigte Verkaufsaufträge löschen** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Feld **Kontonummer** Filterfeld an, welche Verkaufsaufträge zu löschen sind.  
3. Wählen Sie die Schaltfläche **OK** aus.  

Sie können die einzelnen Verkaufsaufträge auch manuell löschen.  

Wiederholen Sie die Schritte 1 bis 3 für alle betroffenen anderen Belege, wie z. B. leere Verkaufsaufträge.

## <a name="see-related-microsoft-training" />Siehe verwandte [Microsoft Schulungen](/training/modules/invoicing-customers-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
