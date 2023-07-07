---
title: So richten Sie allgemeine Lagerbestandsinformationen ein
description: 'Beschreibt, wie Sie die allgemeine Lagereinrichtung definieren, damit Sie Ihr Lager und Ihren Lagerbestand verwalten können.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.search.form: '30, 456, 461'
ms.date: 07/28/2021
ms.author: edupont
---
# <a name="set-up-general-inventory-information"></a>So richten Sie allgemeine Lagerbestandsinformationen ein

Sie geben Ihre allgemeine Lagerbestandseinrichtung auf der Seite **Lager Einrichtung** an.

## <a name="to-set-up-general-inventory-information"></a>So richten Sie allgemeine Lagerbestandsinformationen ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Lagerbestandseinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie auf der Seite **Lager Einrichtung** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Detaillierte Informationen zu den Kalkulationsfeldern **Automatische Kostenbuchung**, **Erwartete Kostenbuchung in Sachkonten** und **Standardmäßige Lagerabgangsmethode** finden Sie unter [Lagerkosten mit dem Hauptbuch abstimmen](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Entwurfsdetails: Lagernachkalkulation](design-details-inventory-costing.md) und [Entwurfsdetails: Buchung erwarteter Kosten](design-details-expected-cost-posting.md). Weitere Informationen zur Kalkulation im Allgemeinen finden Sie unter [Lagerkosten verwalten](finance-manage-inventory-costs.md).  

Wenn Sie möchten, dass die Anwendung die Lagerdurchlaufzeit bei der Berechnung der Lieferterminzusage in der Einkaufszeile berücksichtigt, können Sie sie als Vorgabewert für das Lager und für Ihren Lagerort im **Lager einrichten** einrichten. Weitere Informationen finden Sie unter [Berechnen von Lieferterminzusagen](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> Das Feld **Automatische Lagerregulierung** ist standardmäßig auf *Immer* gesetzt, um sicherzustellen, dass Bestandswerte in der Finanzbuchhaltung immer korrekt sind, wodurch Ihre Umsatz- und Gewinnstatistik auf dem neuesten Stand gehalten wird. Kostenänderungen aus eingehenden Posten, wie diejenigen für Einkäufe oder Produktionsausstoß werden den zugehörigen ausgehenden Posten zugewiesen, wie z. B. Verkäufe oder Umlagerungen. Dies ist hilfreich für neue [!INCLUDE[prod_short](includes/prod_short.md)]-Debitoren und kleine Unternehmen mit relativ geringem Lagerbestandstransaktionsumfang.
>
> Wenn ein Unternehmen jedoch wächst und die Lagerebenen zunehmen, kann dies die Systemleistung beeinträchtigen. Um die Leistungsminderung während der Buchung zu minimieren, wählen Sie eine Zeitoption aus, um zu definieren, wie weit zurück vor dem Arbeitsdatum eine eingehende Transaktion erfolgen kann, um möglicherweise einen Ausgleich verknüpfter ausgehender Wertposten auszulösen.
>
> Alternativ können Sie die Kosten in regelmäßigen Abständen manuell mit dem Stapelverarbeitungsauftrag „Kosten ausgleichen – Artikelposten“ ausgleichen. Sie können auch die automatische Kostenbuchung deaktivieren oder das Feld **Automatische Lagerregulierung** auf *Nie* setzen. In beiden Fällen wird eine Benachrichtigung angezeigt, über die Sie einen Leitfaden zur unterstützten Einrichtung starten können, der Sie beim Planen von Aufgaben für die Aufgabenwarteschlange unterstützt. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Weitere Informationen

[Lager einrichten](inventory-setup-inventory.md)  
[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)  
[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ändern, welche Funktionen angezeigt werden](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
