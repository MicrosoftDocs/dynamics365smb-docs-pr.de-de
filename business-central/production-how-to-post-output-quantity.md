---
title: 'Vorgehensweise: Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen| Microsoft Docs'
description: Die fertig gestellte Menge stellt den Arbeitsfortschritt in Form der gefertigten Menge dar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 83354217bac3b27457303083163cf5eae4494e79
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380456"
---
# <a name="batch-post-output-and-run-times"></a>Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen
Die fertig gestellte Menge stellt den Arbeitsfortschritt in Form der gefertigten Menge dar.  

> [!NOTE]
> Nur wenn Sie die fertig gestellte Menge für den letzten Arbeitsgang buchen, dann aktualisiert die Anwendung automatisch den Lagerbestand.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Die fertig gestellte Mengen für eine oder mehrere Fertigungsauftragszeilen buchen
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **FA-Istmeldungs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Ausgabedaten aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wenn der Arbeitsgang beendet ist, wählen Sie das Feld **Beendet** aus.  

    Wenn der Lagerort, in den die Artikel eingelagert werden sollen, Lagerplätze verwendet, die Bearbeitung der Einlagerung jedoch nicht erforderlich ist, weisen Sie der Buch.-Blattzeile einen Lagerplatzcode zu, um festzulegen, wo die Artikel im Lagerort eingelagert werden sollen. Weitere Informationen finden Sie unter [Produktionseinlagerung oder Montageausgabe](warehouse-how-to-put-away-production-output.md).  

4. Wählen Sie **Buchen** aus, um die Vorgänge zu buchen. Die fertig gestellte Menge wird gebucht. Der Artikel ist jetzt versandbereit.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Die Laufzeit für eine oder mehrere Fertigungsauftragszeilen buchen
Die Bearbeitungszeit stellt den Arbeitsfortschritt in Form der benötigten Arbeitszeit dar.    

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **FA-Istmeldungs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Ausgabedaten aus.  
3.  Wenn der Arbeitsgang beendet ist, wählen Sie das Feld **Beendet** aus.  
4. Wählen Sie die **Buchen** Aktion aus, um die Zeit zu buchen, die je Arbeitsgang aufgewendet wurde. Kapazitätsposten werden für die benötigte Arbeitsplätzen oder Arbeitsplatzgruppen aktualisiert.

## <a name="see-also"></a>Siehe auch  
[Produktion](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]