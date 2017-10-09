---
title: Aktualisieren von festen Einstandspreisen | Microsoft Docs
description: "Sie müssen die festen Einstandspreise von Komponenten in regelmäßigen Abständen aktualisieren und die neuen Einstandspreise auf den übergeordneten Artikel übertragen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 57da88de6a3bbb22cea7c12a2b579206ca5d7766
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-update-standard-costs"></a>Vorgehensweise: Aktualisieren von festen Einstandspreisen
Sie müssen die festen Einstandspreise von Komponenten in regelmäßigen Abständen aktualisieren und die neuen Einstandspreise auf den übergeordneten Artikel übertragen. Der Prozess besteht in der Regel aus den folgenden vier Schritten:  

1.  Aktualisieren von Kosten auf der Komponenten- und Kapazitätsebene. Weitere Informationen finden Sie unter dem Stapelverarbeitungsauftrag **Artikel Einst.-Preis (fest) vorschlagen**.  
2.  Konsolidieren Sie und rollen Sie Komponenten- und Kapazitätskosten auf, um die Gesamtkosten für Herstellung oder Montage der Artikel zu berechnen.  
3.  Implementieren der festen Einstandspreise, die bei der Ausführung der obigen Batchaufträge eingegeben werden. Die festen Einstandspreise treten erst in Kraft, wenn Sie implementiert werden. Weitere Informationen finden Sie unter Mehrstufigen Einstandspreisänderungen implementieren.  
4.  Implementieren der Änderungen, um das Feld **Einstandspreis** auf der Artikelkarte zu aktualisieren und eine Lagerneubewertung durchzuführen. Weitere Informationen finden Sie unter [Gewusst wie: Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md).  

Weitere Informationen finden Sie unter [Über das Berechnen von festen Einstandspreisen](finance-about-calculating-standard-cost.md).  
## <a name="to-update-standard-costs"></a>Einstandspreise aktualisieren  
1.  Führen Sie die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** aus.  
2.  Aufruf der Stapelverarbeitung **Lagerregulierung buchen**.  
3.  Öffnen Sie den **Einst.-Preis (fest) Vorschlag** und verwenden Sie eine oder mehrere der folgenden Funktionen:  

    1.  Führen Sie die Stapelverarbeitung **Art. Einst.-Pr. (fest) vorschlagen** aus.  
    2.  Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.  
    3.  Führen Sie die Stapelverarbeitung **Einstandspreis (fest) für Kapazität vors&chlagen** aus.  
    4.  Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.
    5. Führen Sie die Stapelverarbeitung **Mehrstufigen Einstandspreis berechnen** aus.
    6.  Sehen Sie sich die Ergebnisse an, und nehmen Sie ggf. Änderungen vor.
    7.  Führen Sie die Stapelverarbeitung **Einst.-Preis (fest) Vorschlag übernehmen** aus.  
4.  Sehen Sie sich das Fenster **Neubewertungs Buch.-Blatt** an, das mit Posten aus vorherigen Schritten in diesem Verfahren gefüllt wurde, und buchen Sie es.  

## <a name="see-also"></a>Siehe auch  
 [Informationen zur Berechnung von festen Einstandspreisen](finance-about-calculating-standard-cost.md)   
 [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)   
 [Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md) [[Finance](finance.md)]  
 [Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

