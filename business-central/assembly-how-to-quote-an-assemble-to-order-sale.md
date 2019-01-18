---
title: 'Vorgehensweise: Angebot eines Auftragsmontageverkaufs | Microsoft Docs'
description: "Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5c6cebdb3bdadc9a8b3830a1ff0cb9fb4649e863
ms.contentlocale: de-de
ms.lasthandoff: 11/26/2018

---
# <a name="quote-an-assemble-to-order-sale"></a>Angebot eines Auftragsmontageverkaufs
Sie können Montageverwaltung verwenden, um einen Montageartikel auf Anforderung eines Debitors während des Vertriebsprozesses anzupassen. Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).  

Wie beim Verkauf beliebiger Artikel können Sie auch eine Verkaufsangebot für einen angepassten Montageartikel erstellen, bevor Sie dieses in einen Verkaufsauftrag umwandeln. Dieser Prozess beinhaltet einige zusätzliche Schritte, wenn Sie ihn mit dem Erstellen eines regulären Verkaufsangebots vergleichen; er verwendet eine Variation eines verknüpften Montageauftrags, ein Montageangebot.

> [!NOTE]  
>  Wie alle Arten von Angeboten, werden die Mengen in Montageangeboten nicht für die Verfügbarkeit, in der Planung oder für Reservierungen verwendet.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a>So erstellen Sie ein Verkaufsangebot für einen Auftragsmontageartikel:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkaufsangebote** ein, und wählen dann den zugehörigen Link aus.  
2.  Erstellen Sie eine Verkaufsangebotzeile mit einer Zeile für einen Montageartikel. Weitere Informationen finden Sie unter [Verkaufsangebote machen](sales-how-make-offers.md).  
3.  Geben Sie im Feld **Menge für Auftragsmontage** die vollständige Menge ein.

    > [!NOTE]  
    >  Sie sollten keine Teilmenge eingeben. Daher müssen Sie die gleiche Menge eingeben, die Sie im Feld **Menge** auf der Verkaufsangebotzeile eingegeben haben.  

4.  Wählen Sie auf dem Inforegister **Zeilen** **Zeile** aus, wählen Sie **Auftragsmontage**, und klicken Sie anschließend auf **Auftragsmontagezeilen**. Wählen Sie das Feld **Menge für Auftragsmontage** aus.  
5.  Prüfen und ändern Sie bei Bedarf auf der Seite **Auftragsmontagezeilen** die Auftragsmontagezeilen anhand des Angebots, das der Debitor anfragt. Wenn Sie weitere Informationen wünschen, wählen Sie die Aktion **Dokument anzeigen**, um den vollständigen Rahmenangebotsauftrag zu öffnen. Sie können den Inhalt der meisten Felder nicht ändern, und Sie können nicht buchen.  
6.  Wenn Sie die Montageauftragszeilen entsprechend dem Angebot angepasst haben, schließen Sie die Seite **Auftragsmontagezeilen**, um zur Seite **Verkaufsangebot** zurückzukehren.  
7.  Wenn der Debitor das Angebot annimmt, erstellen Sie einen Verkaufsauftrag für den angebotenen Montageartikel. Weitere Informationen finden Sie unter [Verkaufsangebote machen](sales-how-make-offers.md). Das verknüpfte Montageangebot und alle eventuellen Anpassungen werden mit dem neuen Verkaufsauftrag verknüpft, um die Montage des/der zu verkaufenden Artikel vorzubereiten.  

## <a name="see-also"></a>Siehe auch  
[Montageverwaltung](assembly-assemble-items.md)  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

