---
title: So zeigen Sie doppelte Inventurauftragszeilen an
description: Werden Inventurauftragszeilen manuell erstellt oder automatisch erstellte Zeilen später geändert, müssen Sie darauf achten, dass keine doppelten Zeilen vorkommen. Sie haben die Möglichkeit, doppelte Inventurauftragszeilen durch die Anwendung anzeigen zu lassen.
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
ms.openlocfilehash: f13283f219f5913add0a267db27f44f6dfb8eba8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "927303"
---
# <a name="view-duplicate-physical-inventory-order-lines"></a>So zeigen Sie doppelte Inventurauftragszeilen an
Werden Inventurauftragszeilen manuell erstellt oder automatisch erstellte Zeilen später geändert, müssen Sie darauf achten, dass keine doppelten Zeilen vorkommen. Sie haben die Möglichkeit, doppelte Inventurauftragszeilen durch die Anwendung anzeigen zu lassen.  

Die Arbeitsweise der Anwendung basiert darauf, dass die Kombination der 4 Felder  Artikelnr.,  Variantencode,  Lagerortcode und  Lagerplatzcode in den Inventurauftragszeilen in jedem Inventurauftrag nur einmal vorkommt. Aus diesem Grund führt die Anwendung beim Zuweisen von Inventurerfassungszeilen zu Inventurauftragszeilen eine entsprechende Prüfung durch.  

## <a name="to-view-duplicate-physical-inventory-order-lines"></a>So zeigen Sie doppelte Inventurauftragszeilen an  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol „Nach Seite oder Bericht suchen”"), geben Sie **Bestandsauftrag** ein, und wählen Sie dann den zugehörigen Link aus.  
2.  Öffnen Sie den Inventurauftrag, dessen duplizierten Zeilen Sie anzeigen möchten.  
3.  Wählen Sie die **Doppelte Zeilen anzeigen** Aktion aus.  

Alle doppelten Inventurauftragszeilen werden angezeigt.  

## <a name="see-also"></a>Siehe auch  
 [Physische Inventuraufträge eingeben](how-to-enter-physical-inventory-orders.md)   
 [So schließen Sie eine Inventurerfassung ab](how-to-finish-a-physical-inventory-recording.md)   
 [Inventurerfassung – Inventurzählung](physical-inventory-recording-counting-physical-inventory.md)
