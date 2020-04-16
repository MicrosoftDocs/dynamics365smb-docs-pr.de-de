---
title: 'Vorgehensweise: Schließen von offenen Artikelposten aus einem festen Ausgleich im Artikel Buch.-Blatt | Microsoft Docs'
description: Sie können das Feld **Ausgegl. von Posten** auf der Seite **Artikel Buch.-Blatt** verwenden, um einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen. Beispielsweise um die ausgehende Transaktion zu korrigieren oder ihre Rückgabe zu verarbeiten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 4cec244feb09cf490692e92aa3b58429d4c3e16d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183452"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Schließen von offenen Artikelposten aus einem festen Ausgleich im Artikel Buch.-Blatt
Sie können das Feld **Ausgegl. von Posten** auf der Seite **Artikel Buch.-Blatt** verwenden, um einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen. Beispielsweise um die ausgehende Transaktion zu korrigieren oder ihre Rückgabe zu verarbeiten. Weitere Informationen finden Sie unter Ausgegl. von Posten.  

> [!IMPORTANT]  
>  Feste Ausgleiche, die auf diese Weise vorgenommen werden, gelten nur für die Kosten, nicht für die Menge. Entsprechend schließt der gebuchte positive Artikelposten nicht den angewendeten ausgehenden Posten und bleibt selbst offen. Dies gilt auch, wenn Sie einen festen Ausgleich für einen positiven Posten mit einem negativen Posten buchen, der nicht durch einen positiven regulären Posten geschlossen wurde. Dann bleiben die positiven und negativen Posten offen.  
>   
>  Dies bedeutet auch, dass Sie eine Lagerbuchungsperiode nicht schließen können, wenn ein solcher Posten vorhanden ist.  

Der folgende Ablauf zeigt, wie solche Posten durch Ausführen von zwei korrigierenden Buchungen im Artikel Buch.-Blatt geschlossen werden.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>So schließen Sie offene Artikelposten, die aus einem festen Ausgleich im Artikel Buch.-Blatt entstanden sind  

1.  Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Zugang mit der entsprechenden Menge zu buchen. Dadurch wird der ursprüngliche negative Posten mit einem festen Ausgleich geschlossen.  
2.  Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Abgang zu buchen. Dadurch wird der ursprüngliche korrigierende positive Posten mit einem festen Ausgleich geschlossen.  

## <a name="see-also"></a>Siehe auch  
[Entfernen und erneutes Ausgleichen von Artikelposten](finance-how-to-remove-and-reapply-item-entries.md)  
 [Verarbeiten von Verkaufsrücklieferung und Stornierungen](sales-how-process-sales-returns-cancellations.md)   
 [Einrichten der Lagerwertberechnung und der Kostenrechnung](finance-set-up-inventory-valuation-and-costing.md)   
 [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)   
 [Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)
