---
title: "Vorgehensweise beim Berechnen der verfügbaren Menge für einen Inventurauftrag"
description: "Nachdem Sie den Inventurauftrag erstellt und die Inventurauftragszeilen eingegeben haben, müssen Sie vom Programm das Feld „Erwartete Menge (Basis)” für die einzelnen Inventurauftragszeilen berechnen lassen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 9aa60e5e7a206331e9f2423e8acaf1201f78056f
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="calculate-quantity-on-hand-for-a-physical-inventory-order"></a>Berechnen der verfügbaren Menge für einen Inventurauftrag
Nachdem Sie den Inventurauftrag erstellt und die Inventurauftragszeilen eingegeben haben, müssen Sie vom Programm das Feld „Erwartete Menge (Basis)” für die einzelnen Inventurauftragszeilen berechnen lassen.  

Wenn die Erstellung dieser Inventurauftragszeilen von [!INCLUDE[d365fin](../../includes/d365fin_md.md)] automatisch durchgeführt wurde, konnten Sie auf der Anforderungsseite für die Stapelverarbeitung festlegen, ob die erwartete Menge berechnet werden soll. Wenn Sie die Inventurauftragszeilen manuell erstellt oder zwischenzeitlich geändert haben, müssen Sie die erwarteten Mengen manuell berechnen. Sie können Mengen auf zwei Arten berechnen, wie im folgenden Abschnitt erläutert.  

## <a name="to-calculate-the-expected-quantity-on-the-physical-inventory-order"></a>So wird die erwartete Menge im Inventurauftrag berechnet  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”"), geben Sie **Bestandsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Öffnen Sie den Inventurauftrag, für den Sie die erwartete Menge berechnen möchten.  
3.  Um die erwartete Menge nur einer Inventurauftragszeile zu berechnen, wählen Sie auf der Registerkarte Aktionen in der Gruppe Funktionen die Option **Erwartete Menge berechnen**, und wählen Sie dann **Diese Zeile** aus.  
4.  Um die erwartete Menge aller Inventurauftragszeilen zu berechnen, wählen Sie auf der Registerkarte Aktionen in der Gruppe Funktionen die Option **Erwartete Menge berechnen**, und wählen Sie dann **Alle Zeile** aus.  

    Im Dialog, der angezeigt wird, wählen Sie aus, dass die Mengen für alle Zeilen oder für die Zeilen berechnet werden, die noch nicht berechnet wurden.  

Wenn [!INCLUDE[d365fin](../../includes/d365fin_md.md)] die erwartete Menge bereits berechnet hat, ist das Kontrollkästchen für **Berechnete erw. Menge** der Inventurauftragszeile aktiviert.  

> [!NOTE]  
>  Das Verfahren zur Durchführung der Inventur und zu deren Erfassung in der Inventurerfassung ist von der Berechnung der erwarteten Mengen unabhängig.  

Sie müssen die erwarteten Mengen für alle Inventurauftragszeilen eines Inventurauftrags berechnen, bevor Sie das Feld „Status” auf **Beendet** setzen. Der Grund hierfür ist, dass [!INCLUDE[d365fin](../../includes/d365fin_md.md)] die erwarteten und die erfassten Mengen vergleicht und die Differenzen zu Buchungszwecken berechnet.  

## <a name="see-also"></a>Siehe auch  
 [Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md)   
 [Inventurerfassung – Inventurzählung](physical-inventory-recording-counting-physical-inventory.md)   
 [So schließen Sie einen Inventurauftrag ab](how-to-finish-a-physical-inventory-order.md)   
 [So schließen Sie eine Inventurerfassung ab](how-to-finish-a-physical-inventory-recording.md)   
 [Inventurauftragszeilen mit Artikelverfolgungszeilen](physical-inventory-order-lines-with-item-tracking-lines.md)  
 [Erfassen, Regulieren und Umbuchen von Lagerbestand](../../inventory-how-count-adjust-reclassify.md)

