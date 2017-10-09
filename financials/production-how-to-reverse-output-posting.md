---
title: 'Vorgehensweise: Ausgangsbuchung stornieren | Microsoft Docs'
description: Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss. Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7ac453ff87d78e6be0567ba93b58c0f8938f4052
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-output-posting"></a>Vorgehensweise: Eine Ausgangsbuchung stornieren
Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss. Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.  

## <a name="to-reverse-an-output-posting"></a>Eine Ausgangsbuchung stornieren  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Ausgabe-Buchblatt** ein und wählen den zugehörenden Link aus. Wählen Sie Ihren Stapel aus.  
2. Füllen Sie die Felder je nach Bedarf aus. Weitere Informationen finden Sie unter [Vorgehensweise: Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen](production-how-to-post-output-quantity.md)
3.  Wählen Sie im Feld **Ausgleich mit Lfd. Nr.** den zugeordneten Artikelposten aus. Dadurch werden der Kapazitäts- und der Artikelposten storniert.  
4. Buchen Sie die Stornierung, indem Sie das Buch.-Blatt buchen.  

Die Posten im FA-Istmeldungsprotokoll werden im Hauptartikelposten als positiver Ausgleich gebucht.  

## <a name="see-also"></a>Siehe auch  
 [Produktion](production-manage-manufacturing.md)    
 [Produktion einrichten](production-configure-production-processes.md)  
 [Planung](production-planning.md)      
 [Lagerbest](inventory-manage-inventory.md)  
 [Einkauf](purchasing-manage-purchasing.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

