---
title: Einlagerungsmethoden einzurichten
description: Verwenden Sie Einlagerungsvorlagen, um sich jederzeit die am besten geeigneten Lagerplätze für Ihre Artikel vorschlagen zu lassen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7312, 7313, 7314, 7321, 7322, 7323, 7329
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 59cb78989d4926f3155d5ca3eb195a185b0031bd
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971223"
---
# <a name="set-up-put-away-templates"></a>Einlagerungsmethoden einzurichten

Mit der Funktionalität der gesteuerten Einlagerung und Kommissionierung, wird jederzeit der geeignetsten Lagerplatz für Ihre Artikel vorgeschlagen, entsprechend der Einlagerungsvorlage, die Sie für dieses Lager eingerichtet haben, entsprechend den Lagerplatzprioritäten, die Sie den Lagerplätzen gegeben haben, und den minimalen und maximalen Mengen, die Sie für Standardlagerplätze eingerichtet haben.  

Sie können eine Reihe von Einlagerungsmethoden einrichten und eine von diesen auswählen, mit der Sie im Allgemeinen Einlagerungen in Ihrem Lager steuern möchten. Sie können ebenfalls für solche Artikel oder Lagerhaltungsdaten, für die besondere Einlagerungsmethoden nötig sind, eine Einlagerungsvorlage auswählen.  

## <a name="to-set-up-put-away-templates"></a>So richten Sie Einlagerungsmethoden ein:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einlagerungsvorlagen** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Geben Sie einen Code ein, bei dem es sich um die eindeutige Kennung der neu zu erstellenden Vorlage handelt.  
4. Geben Sie, wenn Sie möchten, eine kurze Beschreibung ein.  
5. Füllen Sie die erste Zeile mit den Lagerplatzanforderungen aus, die vor allem erfüllt sein sollen, wenn eine Einlagerung vorgeschlagen wird.

    Wenn die Standard-Einlagerungsmethode beispielsweise auf festen Lagerplätzen basieren soll, wählen Sie das Feld **Festen Lagerplatz finden** aus. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. Füllen Sie eine zweite Zeile mit den Lagerplatzanforderungen aus, die Ihre zweite Wahl bei der Auswahl eines Lagerplatzes für die Einlagerung sein soll. Die zweite Zeile wird nur berücksichtigt, wenn kein Lagerplatz gefunden wird, der die Anforderungen der ersten Zeile erfüllt.  
7. Fahren Sie fort, die Zeilen auszufüllen, bis Sie alle gewünschten Lagerplatzeinlagerungen beschrieben haben, die im Einlagerungsprozess verwendet werden sollen.  
8. Wählen Sie in der letzten Zeile der Einlagerungsvorlage das Kontrollkästchen **Chaot. Lagerplatz finden**.  

Sie können verschiedene Einlagerungsmethoden erstellen und diese dann anwenden, wie Sie es für richtig halten. Als Erstes wird die Einlagerungsmethode berücksichtigt, die Sie für den Artikel oder die Lagerhaltungsdaten ausgewählt haben (falls Sie dies getan haben). Wenn diese Felder nicht ausgefüllt sind, wird die Einlagerungsmethode berücksichtigt, die Sie für das Lager im Inforegister **Lagerplatzprüfung** auf der Lagerortkarte ausgewählt haben.  

## <a name="see-also"></a>Siehe auch

[Logistik](warehouse-manage-warehouse.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Designdetails: Lagerverwaltung](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]