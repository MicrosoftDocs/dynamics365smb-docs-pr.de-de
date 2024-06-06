---
title: 'Schließen Sie Artikelbucheinträge, die aus einer festen Anwendung stammen'
description: 'Erfahren Sie, wie Sie einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion im Artikel-Buch erstellen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 40
ms.date: 12/12/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Offene Artikelposten aus einem festen Ausgleich im Artikel Buch.-Blatt schließen

Sie können das Feld **Ausgegl. von Posten** auf der Seite **Artikel Buch.-Blatt** verwenden, um einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen. Beispielsweise um die ausgehende Transaktion zu korrigieren oder ihre Rückgabe zu verarbeiten.  

> [!IMPORTANT]  
> Feste Ausgleiche, die auf diese Weise vorgenommen werden, gelten nur für die Kosten, nicht für die Menge. Entsprechend schließt der gebuchte positive Artikelposten nicht den angewendeten ausgehenden Posten und bleibt selbst offen. Dies gilt auch, wenn Sie einen festen Ausgleich für einen positiven Posten mit einem negativen Posten buchen, der nicht durch einen positiven regulären Posten geschlossen wurde. Dann bleiben die positiven und negativen Posten offen.  
>
> Dies bedeutet auch, dass Sie eine Lagerbuchungsperiode nicht schließen können, wenn ein solcher Posten vorhanden ist.  

Sie können Ausgleichsposten unter bestimmten Bedingungen ändern und erneut anwenden, indem Sie die Seite **Anwendungs-Arbeitsblatt** verwenden.  

Der folgende Ablauf zeigt, wie solche Posten durch Ausführen von zwei korrigierenden Buchungen im Artikel Buch.-Blatt geschlossen werden.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>So schließen Sie offene Artikelposten, die aus einem festen Ausgleich im Artikel Buch.-Blatt entstanden sind

1. Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Zugang mit der entsprechenden Menge zu buchen. Dadurch wird der ursprüngliche negative Posten mit einem festen Ausgleich geschlossen.  

    Das Feld **Ausgegl.-von-Posten** gibt die Nummer des ausgehenden Artikelpostens an, dessen Einstandspreis dem eingehenden Artikelposten weitergeleitet wird, wenn Sie eine eingehende Transaktion des Typs **Zugang** oder **Einkauf** mit dem Artikel Buch.-Blatt buchen.  
2. Verwenden Sie das Feld **Ausgegl. von Posten**, um einen Abgang zu buchen. Dadurch wird der ursprüngliche korrigierende positive Posten mit einem festen Ausgleich geschlossen.  

    Das Feld **Ausgegl.-von-Posten** gibt an, ob die Menge in der Artikel Buch.-Blattzeile mit einem bereits gebuchten Beleg ausgeglichen werden soll. Geben Sie in diesem Fall die Postennummer des Artikelpostens ein, der mit der Artikel Buch.-Blattzeile ausgeglichen werden soll.

## <a name="see-also"></a>Siehe auch

[Artikelposten entfernen und erneut ausgleichen](finance-how-to-remove-and-reapply-item-entries.md)  
[Verarbeiten von Verkaufsrücklieferung und Stornierungen](sales-how-process-sales-returns-cancellations.md)  
[Einrichten der Lagerwertberechnung und der Kostenrechnung](finance-set-up-inventory-valuation-and-costing.md)  
[Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)  
[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
