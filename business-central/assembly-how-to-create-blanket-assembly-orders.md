---
title: Erstellen von Montagerahmenaufträgen
description: 'Erstellen Sie Rahmenaufträge für benutzerdefinierte Montageartikel, bevor Sie die tatsächlichen Verkaufsaufträge in regelmäßigen Abständen entsprechend der Rahmenbestellung erstellen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="create-blanket-assembly-orders"></a><a name="create-blanket-assembly-orders"></a><a name="create-blanket-assembly-orders"></a>Erstellen von Montagerahmenaufträgen

Sie können die Montageverwaltung verwenden, um ein Montageelement während des Verkaufsprozesses an die Wünsche eines Kunden anzupassen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

 Wie für jedem anderen Artikel, können Sie auch Rahmenaufträge für benutzerdefinierte Montageartikel erstellen, bevor Sie die tatsächlichen Verkaufsaufträge in regelmäßigen Abständen entsprechend der Rahmenbestellung erstellen. Dieser Prozess beinhaltet im Vergleich zum Erstellen eines regulären Rahmenauftrag einige zusätzliche Schritte; er verwendet eine Variation eines verknüpften Montageauftrags, einen Montagerahmenauftrag.

> [!NOTE]  
>  Wie bei allen Rahmenaufträgen werden Mengen in Montagerahmenaufträgen nur prognostiziert und sind nicht operativ, bis sie in tatsächliche Montageaufträge umgewandelt werden. Daher sind die Bestellungsfunktionen, wie Verfügbarkeitsberechnung, Reservierung, Artikelverfolgung auf Montagerahmenaufträgen nicht aktiv.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a><a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a><a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>So erstellen Sie einen Montagerahmenauftrag\-für\-einen Auftragsmontageartikel

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Verkaufsrahmenaufträge** ein und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie einen neune Rahmenauftrag mit einer Zeile für einen Montageartikel. Weitere Informationen hierzu finden Sie unter [Rahmenaufträge erstellen](sales-how-to-create-blanket-sales-orders.md).  
3. Geben Sie im Feld **Menge für Montageauftrag** auf dem Montagerahmenauftrag die vollständige Menge ein.

    > [!NOTE]  
    >  Sie sollten keine Rahmenauftragsvereinbarungen für eine Teilmenge erstellen. Daher müssen Sie die gleiche Menge eingeben, die Sie im Feld **Menge** auf der Rahmenauftragszeile eingegeben haben.  

4. Wählen Sie auf dem Inforegister Zeilen die Option **Auftragsmontage** aus, und wählen Sie dann **Auftragsmontagezeilen**. Wählen Sie das Feld **Menge für Auftragsmontage** aus.  
5. Prüfen und ändern Sie bei Bedarf auf der Seiter **Auftragsmontagezeilen** die Auftragsmontagezeilen entsprechend der Rahmenauftragsvereinbarung, die Sie mit dem Debitor getroffen haben. Wenn Sie weitere Informationen wünschen, wählen Sie die Aktion **Dokument anzeigen**, um den vollständigen Rahmenangebotsauftrag zu öffnen. Sie können den Inhalt der meisten Felder nicht ändern, und Sie können nicht buchen.  
6. Wenn Sie die Montageauftragszeilen entsprechend der Rahmenauftragsvereinbarung angepasst haben, schließen Sie die Seite **Auftragsmontagezeilen**, um zur Seite **Rahmenauftrag** zurückzukehren.  
7. Wenn der Kunde anfragt, einen Verkaufsauftrag basierend auf dem vereinbarten Rahmenauftrag zu erstellen, erstellen Sie einen Verkaufsauftrag für die vereinbarten Montageartikel oder Artikel. Weitere Informationen hierzu finden Sie unter [Rahmenaufträge erstellen](sales-how-to-create-blanket-sales-orders.md).

Der verknüpfte Montagerahmenauftrag und alle eventuellen Anpassungen werden mit dem neuen Verkaufsauftrag verknüpft, um die Montage des/der zu verkaufenden Artikel vorzubereiten.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Erstellen von Rahmenaufträgen](sales-how-to-create-blanket-sales-orders.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Bestand](inventory-manage-inventory.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
