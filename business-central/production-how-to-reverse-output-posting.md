---
title: 'Vorgehensweise: Ausgangsbuchung stornieren | Microsoft Docs'
description: Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss. Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 33be858c687381a50f42d1c59ca735358f113d72
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788750"
---
# <a name="reverse-output-posting"></a>Gebuchte fertig gestellte Menge stornieren
Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss. Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.  

## <a name="to-reverse-an-output-posting"></a>Eine Ausgangsbuchung stornieren  
1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **FA-Istmeldungs Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link. Wählen Sie Ihren Stapel aus.  
2. Füllen Sie die Felder je nach Bedarf aus. Weitere Informationen finden Sie unter [Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen](production-how-to-post-output-quantity.md)
3.  Wählen Sie im Feld **Ausgleich mit Lfd. Nr.** den zugeordneten Artikelposten aus. Dadurch werden der Kapazitäts- und der Artikelposten storniert.  
4. Buchen Sie die Stornierung, indem Sie das Buch.-Blatt buchen.  

Die Posten im FA-Istmeldungsprotokoll werden im Hauptartikelposten als positiver Ausgleich gebucht.  

## <a name="see-also"></a>Siehe auch  
 [Produktion](production-manage-manufacturing.md)    
 [Produktion einrichten](production-configure-production-processes.md)  
 [Planung](production-planning.md)      
 [Lagerbestand](inventory-manage-inventory.md)  
 [Einkauf](purchasing-manage-purchasing.md)  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
