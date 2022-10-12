---
title: Kommissionierung für interne Arbeitsgänge in erweiterter Lagerkonfigurationen
description: Wenn Ihre Standorte sowohl Kommissionierung als auch Versand verwenden, wählen Sie Komponenten für Produktions- und Montageaktivitäten auf der Seite Lagerauswahl aus.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/02/2022
ms.author: bholtorf
ms.openlocfilehash: 2ef879e5dbabb9281114d62a956ad4b10113c199
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607553"
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Kommissionierung für Montage, Produktion oder Projekte in erweiterter Lagerkonfiguration

In der erweiterten Lagerkonfigurationen, in der der Lagerort für Kommissionierung und Lieferung eingerichtet wurde, können Sie Komponenten für Produktions- und Montageaktivitäten auf der Seite **Kommissionierung** kommissionieren.  

Alternativ können Sie die Seite **Lagerplatzumlagerungsarbeitsblatt** verwenden, um die Artikel spontan ohne Bezug zu einem Herkunftsbeleg zwischen Lagerplätzen ad hoc zu verschieben. Weitere Informationen finden Sie unter [Umlagern von Artikeln in erweiterten Lagerkonfigurationen](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Allgemeine Informationen über das Kommissionieren von Artikeln an den Basislagerorten, die ausschließlich für die Kommissionierung eingerichtet sind, finden Sie unter [Vorgehensweise: Umlagern von Komponenten in einen Arbeitsgangbereich in den Basis-Lagerkonfigurationen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

> [!NOTE]
> Sie können einen Kommissionierungsbeleg nicht von Grund auf neu erstellen, da eine Kommissionierungsaktivität immer Teil eines Workflows ist, entweder in einem Abruf- oder Push-Szenario.  

Sie können den Kommissionierungsbeleg Push-artig erstellen, indem Sie im Herkunftsbeleg, wie einem freigegebenen Montageauftrag oder einem Warenausgang, **Kommissionierung erstellen** auswählen. Weitere Informationen finden Sie unter [Entnahme von Artikeln mit Kommissionierungen](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Sie können einen Lagerentnahmebeleg auch im Pull-Modus erstellen, indem Sie die Seite **Arbeitsblatt auswählen** zum Erkennen von Entnahmeanforderungen verwenden. Diese Methode ist für den Versand und interne Vorgänge nützlich. Anschließend können Sie die erforderlichen Kommissionierbelege erstellen.  

Nachfolgend wird ein Abrufszenario beschrieben, in dem Sie Komponenten für einen freigegebenen FA über die Seite **Kommissionierarbeitsblatt** kommissionieren. Das Verfahren gilt auch für einen Montageauftrag.  

Um Kommissionieranforderungen zu erstellen, müssen für Abruf- und Push-Szenarien die betreffenden Herkunftsbelege freigegeben werden. Die Freigabe von Herkunftsbelegen für interne Arbeitsgänge geschieht auf die folgenden Arten.  

|Herkunftsbeleg|Freigabeverfahren|  
|---------------------|--------------------|  
|Fertigungsauftrag|Änderung des Auftragstyps in einen freigegebenen Fertigungsauftrag.|  
|Montageauftrag|Änderung des Status in "Freigegeben".|
|Aufträge | Änderung des Status in „Offen“.|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>So kommissionieren Sie Komponenten vom Kommissionierarbeitsblatt aus:

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kommissionierarbeitsblatt** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Logistikbeleg holen** aus, und wählen Sie anschließend die Komponentenzeilen des freigegebenen Fertigungsauftrags aus.  
3. Sortieren Sie die Zeilen, um eine effiziente Kommissionierung zu gewährleisten. Möglicherweise möchten Sie Zeilen kombinieren, um Mitarbeiterzeit zu sparen.  
4. Wählen Sie die Aktion **Kommissionierung erstellen** aus.  
5. Legen Sie fest, wie die Kommissionierungsbelege erstellt und wie Kommissionierzeilen sortiert werden, indem Sie die Felder auf der Seite **Kommissionierung erstellen** ausfüllen.  
6. Wählen Sie die Schaltfläche **OK** aus. Kommissionierungsbelege werden mit Kommissionierzeilen für jede Komponente erstellt, die im internen Arbeitsgang erforderlich ist.  

Betriebsbereiche wie Produktionshallen verfügen möglicherweise über einen Standardlagerplatz für die benötigten Komponenten. Wenn dies der Fall ist, wird der Standard-Lagerplatzcode zum Lagerentnahmedokument hinzugefügt, um anzugeben, wo die Artikel abgelegt werden sollen. Weitere Informationen finden Sie in den Tooltips für **Fert.-Bereitst.-Lagerplatzcode** oder **Mont.-Bereitst.-Lagerplatzcode**.

## <a name="filling-the-consumption-bin"></a>Auffüllen des Verbrauchslagerplatzes

Dieses Flow-Diagramm zeigt, wie das Feld **Lagerplatzcode** auf den Zeilen der Produktionsauftragskomponenten entsprechend der Einrichtung Ihres Standorts gefüllt wird.

![Flowdiagramm Lagerplatz.](media/binflow.png "BinFlow")  

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Siehe auch

[Logistik](warehouse-manage-warehouse.md)  
[Bestand](inventory-manage-inventory.md)  
[Einrichten von Warehouse Management](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Designdetails: Warehouse Management](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
