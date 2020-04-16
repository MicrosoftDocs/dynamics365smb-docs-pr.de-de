---
title: 'Vorgehensweise: Einlagerungsmethoden einrichten | Microsoft Docs'
description: Mit der Funktionalität der gesteuerten Einlagerung und Kommissionierung, wird jederzeit der geeignetsten Lagerplatz für Ihre Artikel vorgeschlagen, entsprechend der Einlagerungsvorlage, die Sie für dieses Lager eingerichtet haben, entsprechend den Lagerplatzprioritäten, die Sie den Lagerplätzen gegeben haben, und den minimalen und maximalen Mengen, die Sie für Standardlagerplätze eingerichtet haben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 168a330bdb85c8d5ed18a9ce2b65339c82b4055e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196139"
---
# <a name="set-up-put-away-templates"></a>Einlagerungsmethoden einzurichten
Mit der Funktionalität der gesteuerten Einlagerung und Kommissionierung, wird jederzeit der geeignetsten Lagerplatz für Ihre Artikel vorgeschlagen, entsprechend der Einlagerungsvorlage, die Sie für dieses Lager eingerichtet haben, entsprechend den Lagerplatzprioritäten, die Sie den Lagerplätzen gegeben haben, und den minimalen und maximalen Mengen, die Sie für Standardlagerplätze eingerichtet haben.  

Sie können eine Reihe von Einlagerungsmethoden einrichten und eine von diesen auswählen, mit der Sie im Allgemeinen Einlagerungen in Ihrem Lager steuern möchten. Sie können ebenfalls für solche Artikel oder Lagerhaltungsdaten, für die besondere Einlagerungsmethoden nötig sind, eine Einlagerungsvorlage auswählen.  

## <a name="to-set-up-put-away-templates"></a>So richten Sie Einlagerungsmethoden ein:  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Einlagerungsvorlagen** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Geben Sie einen Code ein, bei dem es sich um die eindeutige Kennung der neu zu erstellenden Vorlage handelt.  
4.  Geben Sie, wenn Sie möchten, eine kurze Beschreibung ein.  
5.  Füllen Sie die erste Zeile mit den Lagerplatzanforderungen aus, die vor allem erfüllt sein sollen, wenn eine Einlagerung vorgeschlagen wird.  
6.  Füllen Sie eine zweite Zeile mit den Lagerplatzanforderungen aus, die Ihre zweite Wahl bei der Auswahl eines Lagerplatzes für die Einlagerung sein soll. Die zweite Zeile wird nur berücksichtigt, wenn kein Lagerplatz gefunden wird, der die Anforderungen der ersten Zeile erfüllt.  
7.  Fahren Sie fort, die Zeilen auszufüllen, bis Sie alle gewünschten Lagerplatzeinlagerungen beschrieben haben, die im Einlagerungsprozess verwendet werden sollen.  
8.  Wählen Sie in der letzten Zeile der Einlagerungsvorlage das Kontrollkästchen **Chaot. Lagerplatz finden**.  

Sie können verschiedene Einlagerungsmethoden erstellen und diese dann anwenden, wie Sie es für richtig halten. Als Erstes wird die Einlagerungsmethode berücksichtigt, die Sie für den Artikel oder die Lagerhaltungsdaten ausgewählt haben (falls Sie dies getan haben). Wenn diese Felder nicht ausgefüllt sind, wird die Einlagerungsmethode berücksichtigt, die Sie für das Lager im Inforegister **Lagerplatzprüfung** auf der Lagerortkarte ausgewählt haben.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
