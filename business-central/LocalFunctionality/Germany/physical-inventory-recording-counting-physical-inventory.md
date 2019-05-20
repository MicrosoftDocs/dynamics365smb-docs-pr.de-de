---
title: Inventurerfassung – Inventurzählung
description: Nach dem Erstellen eines Inventurauftrags und nach der Eingabe der Inventurauftragszeilen kann die eigentliche Inventur durchgeführt werden. In diesem Zusammenhang können die Inventurerfassungsbelege verwendet werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: a1eea5cfb4a3ed39e8cb012cc01ae5bae50998fb
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241715"
---
# <a name="physical-inventory-recording---counting-physical-inventory"></a>Inventurerfassung – Inventurzählung
Nach dem Erstellen eines Inventurauftrags und nach der Eingabe der Inventurauftragszeilen kann die eigentliche Inventur durchgeführt werden. In diesem Zusammenhang können die Inventurerfassungsbelege verwendet werden.  

Eine Inventurerfassung bezieht sich immer nur auf einen Inventurauftrag. Ein Inventurauftrag kann hingegen mit mehr als einer Inventurerfassung verknüpft sein.  

Jede Inventurerfassung setzt sich aus einem Inventurerfassungskopf und einer Reihe von Inventurerfassungszeilen zusammen. Der Inventurerfassungskopf enthält die Informationen, die für alle Inventurerfassungszeilen gültig sind.  

Die Zeilen enthalten die Artikel, die Lagerorte, die Lagerplätze und die erfassten Mengen.  

Diese können manuell oder von der Anwendung automatisch erstellt werden. Es können Inventurerfassungslisten gedruckt werden.  

Durch Festlegen des Status auf "Beendet" teilen Sie der Anwendung mit, dass die aktuelle Inventurerfassung abgeschlossen ist.  

> [!NOTE]  
>  Beim Abschluss der aktuellen Inventurerfassung weist die Anwendung jeder Inventurerfassungszeile eine Zeile des zugehörigen Inventurauftrags zu. Die Anwendung weist jeweils Inventurauftragszeilen mit den gleichen Werten in den 4 Feldern  Artikelnr.,  Variantencode,  Lagerortcode und  Lagerplatzcode wie in der Inventurerfassungszeile zu.  
>   
>  Wenn keine entsprechende Inventurauftragszeile vorhanden ist, fügt die Anwendung beim Abschluss der Inventurerfassung automatisch eine neue Zeile hinzu. Die Anwendung kennzeichnet diese Zeile durch Aktivierung des Kontrollkästchens Ohne Auftrag erfasst in der jeweiligen Inventurauftragszeile.  
>   
>  Ist mehr als eine entsprechende Inventurauftragszeile vorhanden, wird eine Fehlermeldung angezeigt. In diesem Fall können Sie die Anwendung anweisen, die doppelten Zeilen anzuzeigen.  

## <a name="see-also"></a>Siehe auch  
 [So erstellen Sie eine physische Inventurerfassung](how-to-create-a-physical-inventory-recording.md)   
 [So schließen Sie eine Inventurerfassung ab](how-to-finish-a-physical-inventory-recording.md)   
 [So zeigen Sie doppelte Inventurauftragszeilen an](how-to-view-duplicate-physical-inventory-order-lines.md)   
 [Inventurauftragszeilen mit Artikelverfolgungszeilen](physical-inventory-order-lines-with-item-tracking-lines.md)
