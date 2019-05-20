---
title: 'So geht es: Fertigungsauftragsüberschriften herstellen | Microsoft Docs'
description: Sie können Fertigungsaufträge manuell erstellen, und der erste Schritt in diesem Ablauf ist das Erstellen des Fertigungsauftragskopfs.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 70a6f2e583e5ba78eecae0a25d6533d8265414ca
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253309"
---
# <a name="create-production-order-headers"></a>Fertigungsauftragsköpfe erstellen
Sie können Fertigungsaufträge manuell erstellen, und der erste Schritt in diesem Ablauf ist das Erstellen des Fertigungsauftragskopfs.

Fertigungsaufträge werden üblicherweise bei einem dieser Planungsfunktion erstellt, um einen bekannten Bedarf zu erfüllen. Weitere Informationen finden Sie unter [Planung](production-planning.md).   

Im weiteren Prozess wird ein fest geplanter Fertigungsauftrag erstellt. Sie können auch Fertigungsaufträge mit einem anderen Status erstellen.  

## <a name="to-create-a-production-order-header"></a>Fertigungsauftragsköpfe erstellen  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Fest geplante Produktionsaufträge** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Geben Sie im Feld **Nr.** die nächste Nummer aus der Serie ein.  
4.  Wählen Sie im Feld **Herkunftsart.** die Herkunft des Fertigungsauftrags.

    Hier können Sie auswählen, eine Fertigungsfamilie zu erzeugen. Weitere Informationen finden Sie unter [Mit Stücklisten arbeiten](production-how-work-family.md).
5.  Wählen Sie im Feld **Herkunftsnr.** die Artikelnummer, Fertigungsfamilie oder den Verkaufskopf aus, für die/den der Fertigungsauftrag erstellt werden soll.  
6.  Füllen Sie die Felder **Menge** und **Fälligkeitsdatum** entsprechend Ihren Anforderungen aus.  

Wenn Sie Produktionsanforderungen, wie Komponenten oder Arbeitsgänge ändern, können Sie schnell  einen Fertigungsauftrag neu planen. Weitere Informationen finden Sie unter [Direktes Aktualisieren oder ersetzen von Produktionsaufträgen](production-how-to-replan-refresh-production-orders.md). 

## <a name="see-also"></a>Siehe auch  
[Produktion](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
