---
title: Design Details – Lagerbuchungsperioden
description: 'Lagerbuchungsperioden hilft, Probleme mit Salden und Bestandsbewertungen zu vermeiden, indem Lagerbuchungsperioden geöffnet oder geschlossen werden, um Buchungen in einem festgelegten Zeitraum zu begrenzen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-inventory-periods"></a><a name="design-details-inventory-periods"></a>Designdetails: Bestandsperioden
Rückdatierte Transaktions- oder Kostenregulierungen beeinflussen häufig Salden und Bestandsbewertungen für Buchhaltungsperioden, die als geschlossen gelten. Dies kann nachteilige Auswirkungen auf eine genaue Berichterstellung haben, insbesondere innerhalb von weltweiten Unternehmen. Die Funktion „Bestandsperioden“ kann verwendet werden, um solche Probleme zu vermeiden, indem Bestandsperioden geöffnet oder geschlossen werden, um die Buchung in einer bestimmten Periode zu beschränken.  

 Eine Lagerbuchungsperiode ist ein Zeitraum, der von einem Enddatum definiert ist, und innerhalb dessen Sie Lagertransaktionen buchen müssen. Wenn Sie eine Lagerbuchungsperiode schließen, können keine Wertänderungen in der geschlossenen Periode gebucht werden. Dazu gehören neue Wertbuchungen, erwartete oder fakturierte Buchungen, Änderungen bestehender Werte und Kostenregulierungen. Sie können jedoch dennoch mit einen offenen Artikelposten ausgleichen, der in die geschlossene Periode fällt. Weitere Informationen finden Sie unter [Designdetails: Artikelverfolgung](design-details-item-application.md).  

 Um sicherzustellen, dass alle Transaktionsposten in einer geschlossenen Periode endgültig sind, müssen die folgenden Bedingungen erfüllt sein, bevor eine Lagerbuchungsperiode abgeschlossen werden kann:  

-   Alle offenen ausgehenden Artikelposten in der Periode müssen geschlossen werden (d. h. kein negativer Lagerbestand).  
-   Alle Artikelkosten in der Periode müssen korrigiert werden.  
-   Alle freigegebenen und beendeten Fertigungsaufträge in der Periode müssen einer Kostenanpassung unterzogen werden.  

 Wenn Sie eine Lagerbuchungsperiode schließen, wird ein Lagerbuchungsperioden-Posten erstellt, indem die Nummer des letzten Artikeljournals verwendet wird, das in die Lagerbuchungsperiode fällt. Außerdem werden die Zeit, das Datum und der Benutzercode, die die Periode schließen, im Lagerbuchungsperioden-Posten erfasst. Wenn Sie diese Information mit dem letzten Artikelpostens für die vorherige Periode verwenden, können Sie sehen, welche Lagertransaktionen in der Lagerbuchungsperiode gebucht wurden. Es ist ebenfalls möglich, Lagerbuchungsperioden erneut zu öffnen, wenn Sie in einer geschlossenen Periode buchen müssen. Wenn Sie eine Lagerbuchungsperiode erneut öffnen, wird ein Lagerbuchungsperioden-Posten erstellt.  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Design Details: Kalkulation des Bestandes](design-details-inventory-costing.md)  
[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Finanzen](finance.md)  
[Arbeiten mit Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
