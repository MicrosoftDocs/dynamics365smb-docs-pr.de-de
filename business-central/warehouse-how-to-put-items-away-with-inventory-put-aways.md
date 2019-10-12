---
title: 'Vorgehensweise: Einlagern von Artikeln mit Lagereinlagerungen | Microsoft Docs'
description: Wenn Ihr Lagerort so eingerichtet wurde, dass er Einlagerung erfordert, jedoch keinen Wareneingang, verwenden Sie den Beleg **Lagereinlagerung**, um die Wareneingangs- und Einlagerungsinformationen für Ihre Herkunftsbelege zu erfassen. Der eingehende Herkunftsbeleg kann eine Einkaufsbestellung, eine Verkaufsreklamation, ein eingehender Umlagerungsauftrag oder ein Fertigungsauftrag sein, dessen Endprodukt zur Einlagerung bereitsteht.
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
ms.openlocfilehash: aaf527802d9b49f84e0c4261d4658f01382efa45
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313876"
---
# <a name="put-items-away-with-inventory-put-aways"></a>Artikel mit Lagereinlagerungen einlagern
Wenn Ihr Lagerort so eingerichtet wurde, dass er Einlagerung erfordert, jedoch keinen Wareneingang, verwenden Sie den Beleg **Lagereinlagerung**, um die Wareneingangs- und Einlagerungsinformationen für Ihre Herkunftsbelege zu erfassen. Der eingehende Herkunftsbeleg kann eine Einkaufsbestellung, eine Verkaufsreklamation, ein eingehender Umlagerungsauftrag oder ein Montage- bzw. Fertigungsauftrag sein, dessen Endprodukt zur Einlagerung bereitsteht.  

Sie können eine Lagereinlagerung auf drei Arten erstellen:  

- Erstellen Sie die Einlagerung in zwei Schritten, indem Sie zuerst vom Herkunftsbeleg aus eine Erwartete Lagerbewegung erstellen, die für die Logistik als ein Signal dient, dass der Herkunftsbeleg zum Einlagern bereitsteht. Die Lagereinlagerung kann dann von der Seite **Lagereinlagerung** aus erstellt werden, die auf dem Herkunftsbeleg basiert.  
- Erstellen Sie die Lagereinlagerung direkt vom Herkunftsbeleg aus.  
- Erstellen Sie Lagereinlagerungen für mehrere Herkunftsbelege gleichzeitig, indem Sie eine Stapelverarbeitung verwenden.  

## <a name="to-request-an-inventory-put-away-by-releasing-the-source-document"></a>So fordern Sie eine Lagereinlagerung durch Freigabe des Herkunftsbelegs an
Bei Bestellungen, Verkaufsreklamationen, eingehenden Umlagerungsaufträgen und Montageaufträgen erstellen Sie die erwartete Lagerbewegung, indem Sie den Auftrag freigeben. Nachfolgend wird erläutert, wie dies mit einer Einkaufsbestellung erreicht wird.  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufaufträge** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Einkaufsbestellung, den Sie freigeben möchten, und wählen Sie die **Freigeben** Aktion aus.  

    Bei Fertigungsaufträgen erzeugen Sie die Lagerbewegung, indem Sie eine Einlagerungsanforderung aus dem freigegebenen Fertigungsauftrag erstellen.  
3.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Freigegebene FA** ein, und wählen dann den zugehörigen Link aus.  
4. Wählen Sie die **Lagereinlag.-Anforderung erstellen** Aktion aus.  

> [!NOTE]  
>  Sie können die Einlagerungsanforderung auch erstellen, indem Sie das Kontrollkästchen **Lagereinlag.-Anford. erstellen** aktivieren, wenn Sie den Fertigungsauftrag aktualisieren. Weitere Informationen finden Sie unter [Aktualisieren oder ersetzen von Produktionsaufträgen.](production-how-to-replan-refresh-production-orders.md)  

Sobald die erwartete Lagerbewegung erzeugt wurde, kann eine Lagermitarbeiter, der der Einlagerungen zugeiwesen wurde, sehen, dass der Herkunftsbeleg zum Einlagern bereitsteht, und einen neuen Einlagerungsbeleg erstellen.  

## <a name="to-create-an-inventory-put-away-based-on-the-source-document"></a>Eine Lagereinlagerung vom Herkunftsbeleg aus erstellen
Nachdem die Anforderung erstellt wurde, kann der Lagermitarbeiter eine neue Lagereinlagerungen auf Grundlage des freigegebenen Herkunftsbelegs erstellen.   
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagereinlagerung** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie im Feld **Herkunftsbeleg** die Art des Herkunftsbelegs aus, auf dem die Einlagerung basiert.  
4. Wählen Sie im Feld **Herkunftsnr.** den Herkunftsbeleg aus.  
5. Oder wählen Sie die Aktion **Herkunftsbeleg holen** aus, um den Beleg aus einer Liste von eingehenden Herkunftsbelegen auszuwählen, die zur Einlagerung am Lagerort bereit sind.  
6. Wählen Sie die Schaltfläche **OK**, um die Einlagerungszeilen gemäß dem ausgewählten Herkunftsbeleg auszufüllen.  

## <a name="to-create-an-inventory-put-away-from-the-source-document"></a>Eine Lagereinlagerung vom Herkunftsbeleg aus erstellen  
1.  Im Herkunftsbeleg, der ein Einkaufsbestellung, eine Verkaufsreklamation, ein eingehender Umlagerungsauftrag oder ein Fertigungsauftrag sein kann, klicken Sie auf die Aktion **Lagerbelege erstellen**.  
2. Aktivieren Sie das Kontrollkästchen **Lagerbelege erstellen**
3. Wählen Sie die Schaltfläche **OK** aus. Eine neue Lagereinlagerung wird erstellt.

## <a name="to-create-multiple-inventory-put-aways-with-a-batch-job"></a>So erstellen Sie mehrere Lagereinlagerungen mit einer Stapelverarbeitung  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerbelege erstellen** ein, und wählen dann den zugehörigen Link aus.  
2.  Im Inforegister **Erwartete Lagerbewegung** der Anforderungsseite können Sie die Felder **Herkunftsbeleg** und **Herkunftsnr.** verwenden, um Filter auf bestimmte Arten von Belegen oder auf Bereiche von Belegnummern zu setzen.  
3.  Aktivieren Sie im Inforegister **Optionen** das Kontrollkästchen **Lagereinlag. erst.** aus.
4.  Wählen Sie die Schaltfläche **OK** aus. Die angegebenen Lagereinlagerungen werden erstellt.

## <a name="to-record-the-inventory-put-away"></a>So erfassen Sie die Lagereinlagerung  
1. Öffnen Sie einen zuvor erstellten Einlagerungsbeleg, indem Sie diesen auf der Seite **Lagereinlagerungen** auswählen.  
2. Geben Sie im Feld **Lagerplatzcode** auf den Einlagerungszeilen wird der Lagerplatz entsprechend des Standardlagerplatzes des Artikels vorgeschlagen. Sie können – falls erforderlich – auf dieser Seite den Lagerplatz ändern.  
3. Führen Sie die Einlagerung durch und geben Sie die Informationen über die tatsächlich eingelagerte Menge in das Feld **Bewegungsmenge** ein.

    Wenn es erforderlich ist, die Artikel einer Zeile in mehr als einem Lagerplatz einzulagern, beispielsweise, da der freie Lagerplatz voll ist, verwenden Sie die Funktion **Zeile aufteilen** im Inforegister **Zeilen**. Weitere Informationen über das Aufteilen von Zeilen finden Sie unter [Aufteilen von Lageraktivitätszeilen](warehouse-how-to-split-warehouse-activity-lines.md).  
4. Wenn Sie die Einlagerung durchgeführt haben, wählen Sie die **Buchen** Aktion aus.  

Der Buchungsprozess bucht den Wareneingang, oder für Fertigungsaufträge die Istmeldung, der Herkunftsbelegzeilen, die eingelagert wurden, und wenn der Lagerort Lagerplätze verwendet, erzeugt der Buchungsvorgang darüber hinaus Lagerplatzposten über die Mengenänderungen in den Lagerplätzen.

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
