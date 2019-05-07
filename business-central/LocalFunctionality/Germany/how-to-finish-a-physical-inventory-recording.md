---
title: 'Gewusst wie: So schließen Sie eine Inventurerfassung ab'
description: Nachdem alle Daten einer Inventurerfassung vollständig eingegeben wurden, können Sie die Erfassung abschließen, indem Sie das Feld Status auf Beendet setzen.
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
redirect_url: ../../inventory-how-count-inventory-with-documents
ms.openlocfilehash: 0171e5fa3bc4e50dc637600be2df720e26ece290
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "930103"
---
# <a name="finish-a-physical-inventory-recording"></a>So schließen Sie eine Inventurerfassung ab
Nachdem alle Daten einer Inventurerfassung vollständig eingegeben wurden, können Sie die Erfassung abschließen, indem Sie das Feld **Status** auf **Beendet** setzen.  

Dies ist nur möglich, wenn das Kontrollkästchen **Erfasst** für alle Inventurerfassungszeilen der aktuellen Inventurerfassung aktiviert ist.  

## <a name="to-finish-a-physical-inventory-recording"></a>So schließen Sie eine Inventurerfassung ab  

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Physische Inventurliste** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Öffnen Sie den Inventurauftrag, den Sie abschließen möchten, und wählen Sie die **Fertig stellen** Aktion aus.  

    Das Feld Status wird auf **Beendet** gesetzt. Sie können den Inventurerfassungskopf oder die Inventurerfassungszeilen nun nicht mehr ändern.  

Beim Abschluss der aktuellen Inventurerfassung weist die Anwendung jeder Inventurerfassungszeile eine Zeile des zugehörigen Inventurauftrags zu. Die Anwendung weist jeweils Inventurauftragszeilen mit den gleichen Werten in den 4 Feldern  **Artikelnr.**,  **Variantencode**, **Lagerortcode** und **Lagerplatzcode** wie in der Inventurerfassungszeile zu.  

Wenn keine entsprechende Inventurauftragszeile vorhanden ist und wenn das Feld **Erfassung ohne Auftrag erlaubt** im Inventurerfassungskopf aktiviert ist, wird automatisch eine neue Zeile eingefügt und das **Ohne Auftrag erfasst** der Inventurauftragszeile aktiviert. Andernfalls wird eine Fehlermeldung angezeigt, und der Prozess wird abgebrochen. Auch wenn es mehr als eine zugehörige Inventurauftragszeile gibt, wird eine Fehlermeldung angezeigt und die Verarbeitung gestoppt.  

## <a name="see-also"></a>Siehe auch  
 [So erstellen Sie eine physische Inventurerfassung](how-to-create-a-physical-inventory-recording.md)   
 [So erstellen Sie eine physische Inventurerfassung](how-to-create-a-physical-inventory-recording.md)   
 [So zeigen Sie doppelte Inventurauftragszeilen an](how-to-view-duplicate-physical-inventory-order-lines.md)   
 [Vorgehensweise beim Analysieren von Inventurdifferenzen](how-to-analyze-physical-inventory-differences.md)   
 [Inventurauftragszeilen mit Artikelverfolgungszeilen](physical-inventory-order-lines-with-item-tracking-lines.md)
