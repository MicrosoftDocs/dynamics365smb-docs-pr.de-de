---
title: Aktualisieren von festen Einstandspreisen | Microsoft Docs
description: Sie müssen die festen Einstandspreise von Komponenten in regelmäßigen Abständen aktualisieren und die neuen Einstandspreise auf den übergeordneten Artikel übertragen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 99783deca985a630a46b745b1e7f0a92eb327642
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784567"
---
# <a name="update-standard-costs"></a>Standardkosten aktualisieren
Sie müssen die festen Einstandspreise von Komponenten in regelmäßigen Abständen aktualisieren und die neuen Einstandspreise auf den übergeordneten Artikel übertragen. Der Prozess besteht in der Regel aus den folgenden vier Schritten:  

1.  Aktualisieren von Kosten auf der Komponenten- und Kapazitätsebene. Weitere Informationen finden Sie unter dem Stapelverarbeitungsauftrag **Artikel Einst.-Preis (fest) vorschlagen**.  
2.  Konsolidieren Sie und rollen Sie Komponenten- und Kapazitätskosten auf, um die Gesamtkosten für Herstellung oder Montage der Artikel zu berechnen.  
3.  Implementieren der festen Einstandspreise, die bei der Ausführung der obigen Batchaufträge eingegeben werden. Die festen Einstandspreise treten erst in Kraft, wenn Sie implementiert werden. Weitere Informationen finden Sie unter Mehrstufigen Einstandspreisänderungen implementieren.  
4.  Implementieren der Änderungen, um das Feld **Einstandspreis** auf der Artikelkarte zu aktualisieren und eine Lagerneubewertung durchzuführen. Weitere Informationen finden Sie unter [Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md).  

Weitere Informationen finden Sie unter [Über das Berechnen von festen Einstandspreisen](finance-about-calculating-standard-cost.md).  
## <a name="to-update-standard-costs"></a>Einstandspreise aktualisieren  
1.  Führen Sie die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** aus.  
2.  Aufruf der Stapelverarbeitung **Lagerregulierung buchen**.  
3.  Öffnen Sie das **Einst.-Preis (fest) Arbeitsblatt** und verwenden Sie eine oder mehrere der folgenden Funktionen:  

    1.  Führen Sie die Stapelverarbeitung **Art. Einst.-Pr. (fest) vorschlagen** aus.  
    2.  Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.  
    3.  Führen Sie die Stapelverarbeitung **Einstandspreis (fest) für Kapazität vors&chlagen** aus.  
    4.  Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.
    5. Führen Sie die Stapelverarbeitung **Mehrstufigen Einstandspreis berechnen** aus.
    6.  Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.
    7.  Führen Sie die Stapelverarbeitung **Einst.-Preis (fest) Vorschlag übernehmen** aus.  
4.  Sehen Sie sich das  **Neubewertungs Buch.-Blatt** an, das mit Posten aus vorherigen Schritten in diesem Verfahren gefüllt wurde, und buchen Sie es.  

## <a name="see-also"></a>Siehe auch  
 [Informationen zur Berechnung von festen Einstandspreisen](finance-about-calculating-standard-cost.md)   
 [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)   
 [Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md) [Finance](finance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]