---
title: Info zu Kosten des beendeten Produktionsauftrags | Microsoft Docs
description: Das Beenden eines Fertigungsauftrages ist eine wichtige Aufgabe beim Abschließen der Gesamtkostenbewertung des Artikels, der gefertigt wird. Endeinstandspreise (Abweichungen in einer Einstandspreisumgebung; Ist-Kosten in einer FIFO-, Durchschnitt- oder LIFO-Einstandspreisumgebung) werden mit der Stapelverarbeitung  Kosten anpassen Lagerreg. fakt berechnet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 2f84ca5cf44dcbab1c85b24a8e00f674b115918a
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788496"
---
# <a name="about-finished-production-order-costs"></a>Info zu Kosten des beendeten FA
Das Beenden eines Fertigungsauftrages ist eine wichtige Aufgabe beim Abschließen der Gesamtkostenbewertung des Artikels, der gefertigt wird. Endeinstandspreise einschließlich Abweichungen in einer Einstandspreisumgebung; Ist-Kosten in einer FIFO-, Durchschnitt- oder LIFO-Einstandspreisumgebung, werden mit der Stapelverarbeitung **Artikelkosteneinträge anpassen** berechnet, die eine finanzielle Abstimmung der Kosten der Artikelfertigung ermöglicht. Damit ein Fertigungsauftrag für die Einstandspreisregulierung berücksichtigt wird, muss er den Status **Beendet** haben. Es ist daher unbedingt erforderlich, dass nach Beendigung die Änderung des Status eines Fertigungsauftrags in **Beendet** erfolgt.  

## <a name="example"></a>Beispiel  
 Wenn Sie z. B. in einer Einstandspreis-Umgebungen Material verbrauchen, um einen Artikel zu fertigen, gehen, einfach gesagt, der Einstandspreis des Artikels sowie die Bearbeitungs- und die Gemeinkosten in die WIP ein. Wenn der Artikel gefertigt wird, wird WIP um den Betrag Einstandspreises des Artikels verringert. Normalerweise sind diese Kosten nicht gleich Null. Damit diese Kosten sich zu Null saldieren können, müssen Sie die Stapelverarbeitung **Artikelkosteneinträge anpassen**, wobei zu beachten ist, dass nur Fertigungsaufträge mit dem Status **Beendet** für die Regulierung berücksichtigt werden.  

## <a name="see-also"></a>Siehe auch  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Produktion](production-manage-manufacturing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
