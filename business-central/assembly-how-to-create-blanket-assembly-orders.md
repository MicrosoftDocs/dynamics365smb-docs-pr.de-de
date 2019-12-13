---
title: 'Vorgehensweise: Erstellen von Montageaufträgen| Microsoft Docs'
description: Erstellen Sie Rahmenaufträge für benutzerdefinierte Montageartikel, bevor Sie die tatsächlichen Verkaufsaufträge in regelmäßigen Abständen entsprechend der Rahmenbestellung erstellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: d15ecfe1d334c07c757cba10647267ae89fea629
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880880"
---
# <a name="create-blanket-assembly-orders"></a>Erstellen von Montagerahmenaufträgen
Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

 Wie für jedem anderen Artikel, können Sie auch Rahmenaufträge für benutzerdefinierte Montageartikel erstellen, bevor Sie die tatsächlichen Verkaufsaufträge in regelmäßigen Abständen entsprechend der Rahmenbestellung erstellen. Dieser Prozess beinhaltet im Vergleich zum Erstellen eines regulären Rahmenauftrag einige zusätzliche Schritte; er verwendet eine Variation eines verknüpften Montageauftrags, einen Montagerahmenauftrag.

> [!NOTE]  
>  Wie bei allen Rahmenaufträgen werden Mengen in Montagerahmenaufträgen nur prognostiziert und sind nicht operativ, bis sie in tatsächliche Montageaufträge umgewandelt werden. Daher sind die Bestellungsfunktionen, wie Verfügbarkeitsberechnung, Reservierung, Artikelverfolgung auf Montagerahmenaufträgen nicht aktiv.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>So erstellen Sie einen Montagerahmenauftrag für einen Auftrags\-\-montageartikel:  
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Verkauf Rahmenauftrag** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie einen neune Rahmenauftrag mit einer Zeile für einen Montageartikel. Weitere Informationen hierzu finden Sie unter [Rahmenaufträge erstellen](sales-how-to-create-blanket-sales-orders.md).  
3. Geben Sie im Feld **Menge für Montageauftrag** auf dem Montagerahmenauftrag die vollständige Menge ein.

    > [!NOTE]  
    >  Sie sollten keine Rahmenauftragsvereinbarungen für eine Teilmenge erstellen. Daher müssen Sie die gleiche Menge eingeben, die Sie im Feld **Menge** auf der Rahmenauftragszeile eingegeben haben.  

4. Wählen Sie auf dem Inforegister Zeilen die Option **Auftragsmontage** aus, und wählen Sie dann **Auftragsmontagezeilen**. Wählen Sie das Feld **Menge für Auftragsmontage** aus.  
5. Prüfen und ändern Sie bei Bedarf auf der Seiter **Auftragsmontagezeilen** die Auftragsmontagezeilen entsprechend der Rahmenauftragsvereinbarung, die Sie mit dem Debitor getroffen haben. Wenn Sie weitere Informationen wünschen, wählen Sie die Aktion **Dokument anzeigen**, um den vollständigen Rahmenangebotsauftrag zu öffnen. Sie können den Inhalt der meisten Felder nicht ändern, und Sie können nicht buchen.  
6. Wenn Sie die Montageauftragszeilen entsprechend der Rahmenauftragsvereinbarung angepasst haben, schließen Sie die Seite **Auftragsmontagezeilen**, um zur Seite **Rahmenauftrag** zurückzukehren.  
7. Wenn der Kunde anfragt, einen Verkaufsauftrag basierend auf dem vereinbarten Rahmenauftrag zu erstellen, erstellen Sie einen Verkaufsauftrag für die vereinbarten Montageartikel oder Artikel. Weitere Informationen hierzu finden Sie unter [Rahmenaufträge erstellen](sales-how-to-create-blanket-sales-orders.md).

Der verknüpfte Montagerahmenauftrag und alle eventuellen Anpassungen werden mit dem neuen Verkaufsauftrag verknüpft, um die Montage des/der zu verkaufenden Artikel vorzubereiten.  

## <a name="see-also"></a>Siehe auch
[Erstellen von Rahmenaufträgen](sales-how-to-create-blanket-sales-orders.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
