---
title: 'Vorgehensweise: Artikel-Familien in der Produktion verwenden | Microsoft Docs'
description: "Die Hauptaufgabe beim Anpassen eines Basiskalenders für Ihre Firma oder einen Ihrer Geschäftspartner ist, alle Änderungen am Status der Daten als freie Tage oder Arbeitstage einzugeben."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 060c58991ae48ba768f5c1c0bd7442228e6bc976
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-production-families"></a>Vorgehensweise: Arbeiten mit Fertigungsfamilien
Eine Fertigungsfamilie ist eine Gruppe einzelner Artikel, deren Zusammenhang in der Ähnlichkeit ihres Fertigungsprozesses liegt. Wenn Sie Fertigungsfamilien zusammenstellen, können einzelne Artikel mehrfach, in einem Arbeitsschritt, gefertigt werden, womit Sie den Materialverbrauch optimieren können.

Geben Sie im **Menge**-Feld im **Familien**-Fenster die Menge ein, die gefertigt werden soll, wenn die gesamte Fertigungsfamilie einmal gefertigt wird.

## <a name="example"></a>Beispiel
Beim Stanzen können vier Teile eines Artikels und 10 Teile eines anderen Artikels aus einem Blech zur gleichen Zeit gestanzt werden. Die Stanzmaschine stanzt die kompletten 14 Teile in einem Arbeitsschritt.

Fertigungsfamilien verringern die Ausschussmenge, da der normalerweise bei der Fertigung großer Teile entstehende Ausschuss zur Fertigung kleiner Teile verwendet wird.

## <a name="to-set-up-a-production-family"></a>Fertigungsfamilien einrichten
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Familien** ein. Wählen Sie dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-familily"></a>Um auf Grundlage eine Produktion familily erzeugen
1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen ") aus und geben Sie **Feste Auftragsplanung** ein. Wählen Sie dann den zugehörigen Link aus.
2. Dient zum Erstellen eines neuen Produktionsauftrags. Weitere Informationen finden Sie unter [Gewusst wie: Erstellen von Montageaufträgen](production-how-to-create-production-orders.md).
3. Wählen Sie im Feld **Quelltyp** **Familie** aus.  
4. Wählen Sie im Feld **Quelle** die entsprechende Produktionsfamilien aus.

## <a name="see-also"></a>Siehe auch
[So wird's gemacht: Neue Fertigungsstücklisten erzeugen](production-how-to-create-production-boms.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planung](production-planning.md)   
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

