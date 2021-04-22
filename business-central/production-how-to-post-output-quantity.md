---
title: Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen
description: Die fertig gestellte Menge repräsentiert den Arbeitsfortschritt in Form der fertigen Menge und der genutzten Kapazität der Arbeit oder des Arbeitsplatzes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787877"
---
# <a name="batch-post-output-and-run-times"></a>Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen
Die fertig gestellte Menge repräsentiert den Arbeitsfortschritt in Form der fertigen Menge und der genutzten Kapazität der Arbeit oder des Arbeitsplatzes.

Sie können das Ausgabejournal für Folgendes verwenden:
*  Regulieren Sie Lagerbestand in Verbindung mit der Ausgabe fertiger Artikel aus der Produktion.
*  Registrieren Sie Mengen und Ausschuss für jeden Vorgang im Fertigungsarbeitsgang.
*  Registrieren Sie Setup und Laufzeit für Arbeit und Arbeitsplätze.

> [!NOTE]
> Wenn der Fertigungsarbeitsgang verwendet wird, aktualisiert die Anwendung automatisch den Lagerbestand nur wenn Sie die fertig gestellte Menge für den letzten Arbeitsgang buchen.

Im Fenster **Produktions Buch.-Blatt** können Sie die gleichen Aufgaben wie im Fenster **FA-Istmeldungs Buch.-Blatt** ausführen und gleichzeitig die entsprechenden Verbrauchsbuchungsaufgaben ausführen. Weitere Informationen finden Sie unter [Gemeinsames Erfassen und Buchen von Verbrauch und Istmeldungen für eine einzelne freigegebene Fertigungsauftragszeile](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Die fertig gestellte Mengen und/oder Erfassungslaufzeiten für eine oder mehrere Fertigungsauftragszeilen buchen
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **FA-Istmeldungs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Ausgabedaten und/oder der Laufzeit aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Sie können die Funktion **Arbeitsplan auflösen** Generieren von Journalzeilen aus Fertigungsaufträgen verwenden.
  
4. Wenn der Arbeitsgang beendet ist, wählen Sie das Feld **Beendet** aus.  
5. Um die Vorgänge zu buchen, wählen Sie die Aktion **Buchen** aus. 
 
Kapazitätsposten werden für die verwendeten Arbeitsplätze mit Informationen zu Zeit und Menge der Ausgabe und des Ausschusses aktualisiert. Wenn Sie den letzten Vorgang gebucht haben, wird der Artikel dem Lager hinzugefügt. 

## <a name="see-also"></a>Siehe auch  
[Ausschuss manuell buchen](production-how-to-post-scrap.md)
[Gebuchte fertig gestellte Menge stornieren](production-how-to-reverse-output-posting.md)
[Produktion](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
