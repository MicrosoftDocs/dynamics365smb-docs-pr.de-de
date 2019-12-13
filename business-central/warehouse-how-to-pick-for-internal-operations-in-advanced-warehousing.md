---
title: 'Vorgehensweise: Kommissionierung für interne Arbeitsgänge in erweiterter Lagerkonfigurationen | Microsoft Docs'
description: In der erweiterten Lagerkonfigurationen, in der der Lagerort für Kommissionierung und Lieferung eingerichtet wurde, können Sie Komponenten für Produktions- und Montageaktivitäten auf der Seite **Kommissionierung** kommissionieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 4272512046a3951eb933fb25c869d5e9d7a3b416
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876607"
---
# <a name="pick-for-production-or-assembly-in-advanced-warehouse-configurations"></a>Kommissionierung für Montage oder Produktion in erweiterter Lagerkonfiguration
In der erweiterten Lagerkonfigurationen, in der der Lagerort für Kommissionierung und Lieferung eingerichtet wurde, können Sie Komponenten für Produktions- und Montageaktivitäten auf der Seite **Kommissionierung** kommissionieren.  

Alternativ können Sie die Seite **Lagerplatzumlagerungsvorschlag** verwenden, um die Artikel ohne Bezug zu einem Herkunftsbeleg zwischen Lagerplätzen ad hoc zu verschieben. Weitere Informationen finden Sie unter [Umlagern von Artikeln in erweiterten Lagerkonfigurationen](warehouse-how-to-move-items-in-advanced-warehousing.md).  

Allgemeine Informationen über das Kommissionieren von Artikeln für interne Arbeitsgänge an den Basislagerorten, die ausschließlich für die Kommissionierung eingerichtet sind, finden Sie unter [Vorgehensweise: Umlagern von Komponenten in einen Arbeitsgangbereich in den Basis-Lagerkonfigurationen](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

Sie können einen Kommissionierungsbeleg nicht von Grund auf neu erstellen, da eine Kommissionierungsaktivität immer Teil eines Workflows ist, entweder in einem Abruf- oder Push-Szenario.  

Sie können den Kommissionierungsbeleg Push-artig erstellen, indem Sie im Herkunftsbeleg, wie einem freigegebenen Montageauftrag oder einem Warenausgang, **Kommissionierung erstellen** auswählen. Weitere Informationen finden Sie unter [Entnahme von Artikeln mit Kommissionierungen](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

Alternativ können Sie den Kommissionierungsbeleg abrufartig erstellen, indem Sie die Seite **Kommissioniervorschlag** verwenden, um Kommissionieranforderungen für den Warenausgang und für interne Arbeitsgänge zu ermitteln, und dann die erforderlichen Kommissionierungsbelege zu erstellen.  

Nachfolgend wird ein Abrufszenario beschrieben, in dem Sie Komponenten für einen freigegebenen FA über die Seite **Kommissioniervorschlag** kommissionieren. Das Verfahren gilt auch für einen Montageauftrag.  

Um Kommissionieranforderungen zu erstellen, müssen für Abruf- und Push-Szenarien die betreffenden Herkunftsbelege freigegeben werden. Die Freigabe von Herkunftsbelegen für interne Arbeitsgänge geschieht auf die folgenden Arten.  

|Herkunftsbeleg|Freigabeverfahren|  
|---------------------|--------------------|  
|Fertigungsauftrag|Änderung des Auftragstyps in einen freigegebenen Fertigungsauftrag.|  
|Montageauftrag|Änderung des Status in "Freigegeben".|  

## <a name="to-pick-components-using-the-pick-worksheet"></a>So kommissionieren Sie Komponenten vom Kommissioniervorschlag aus:  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Kommissionierungsvorschlag** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Logistikbeleg holen** aus, und wählen Sie anschließend die Komponentenzeilen des freigegebenen Fertigungsauftrags aus.  
3.  Prüfen Sie die Zeilen, sortieren Sie sie so, dass sie eine effiziente Kommissionierrunde ergeben, und kombinieren Sie sie, falls erforderlich, mit anderen Kommissionierzeilen, um die Arbeitszeit der Mitarbeiter bestmöglich zu nutzen.  
4.  Wählen Sie die Aktion **Kommissionierung erstellen** aus.  
5.  Legen Sie fest, wie die Kommissionierungsbelege erstellt und wie Kommissionierzeilen sortiert werden, indem Sie die Felder auf der Seite **Kommissionierung erstellen** ausfüllen.  
6.  Wählen Sie die Schaltfläche **OK** aus. Kommissionierungsbelege werden mit Kommissionierzeilen für jede Komponente erstellt, die im internen Arbeitsgang erforderlich ist.  

Wenn der interne Vorgangsbereich, wie ein Produktionsfertigungsbereich, mit einem Lagerplatz eingerichtet ist, der für die Lagerung von Komponenten für den Arbeitsgang verwendet wird, dann wird dieser Lagerplatzcode in die Einlagerungszeilen des Kommissionierungsbelegs eingefügt, der Lagermitarbeiter anweist, wo sie die Artikel einlagern sollen. Weitere Informationen finden Sie im Feld **Fert.-Bereitst.-Lagerplatzcode** oder **Mont.-Bereitst.-Lagerplatzcode**.

## <a name="filling-the-consumption-bin"></a>Auffüllen des Verbrauchslagerplatzes
Dieses Flussdiagramm zeigt, wie das Feld **Lagerplatzcode** in FA-Komponentenzeilen entsprechend Ihrer Einrichtung ausgefüllt wird.

![Lagerplatzflussdiagramm](media/binflow.png "BinFlow")  

## <a name="see-also"></a>Siehe auch
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
