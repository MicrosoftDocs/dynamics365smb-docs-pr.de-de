---
title: Designdetails - Bestandberioden | Microsoft Docs
description: "Rückdatierte Transaktions- oder Kostenregulierungen beeinflussen häufig Salden und Bestandsbewertungen für Buchhaltungsperioden, die als geschlossen gelten. Dies kann nachteilige Auswirkungen auf eine genaue Berichterstellung haben, insbesondere innerhalb von weltweiten Unternehmen. Die Funktion „Bestandsperioden“ kann verwendet werden, um solche Probleme zu vermeiden, indem Bestandsperioden geöffnet oder geschlossen werden, um die Buchung in einer bestimmten Periode zu beschränken."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 99aa0cacdbe6933c5ba16443297d1838b8bfd3ac
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-periods"></a>Designdetails: Bestandsperioden
Rückdatierte Transaktions- oder Kostenregulierungen beeinflussen häufig Salden und Bestandsbewertungen für Buchhaltungsperioden, die als geschlossen gelten. Dies kann nachteilige Auswirkungen auf eine genaue Berichterstellung haben, insbesondere innerhalb von weltweiten Unternehmen. Die Funktion „Bestandsperioden“ kann verwendet werden, um solche Probleme zu vermeiden, indem Bestandsperioden geöffnet oder geschlossen werden, um die Buchung in einer bestimmten Periode zu beschränken.  

 Eine Lagerbuchungsperiode ist ein Zeitraum, der von einem Enddatum definiert ist, und innerhalb dessen Sie Lagertransaktionen buchen müssen. Wenn Sie eine Lagerbuchungsperiode schließen, können keine Wertänderungen in der geschlossenen Periode gebucht werden. Dazu gehören neue Wertbuchungen, erwartete oder fakturierte Buchungen, Änderungen bestehender Werte und Kostenregulierungen. Sie können jedoch dennoch mit einen offenen Artikelposten ausgleichen, der in die geschlossene Periode fällt. [Weitere Informationen finden Sie unter "Designdetails: Artikelverfolgung".](design-details-item-application.md)  

 Um sicherzustellen, dass alle Transaktionsposten in einer geschlossenen Periode endgültig sind, müssen die folgenden Bedingungen erfüllt sein, bevor eine Lagerbuchungsperiode abgeschlossen werden kann:  

-   Alle offenen ausgehenden Artikelposten in der Periode müssen geschlossen werden (d. h. kein negativer Lagerbestand).  
-   Alle Artikelkosten in der Periode müssen korrigiert werden.  
-   Alle freigegebenen und beendeten Fertigungsaufträge in der Periode müssen einer Kostenanpassung unterzogen werden.  

 Wenn Sie eine Lagerbuchungsperiode schließen, wird ein Lagerbuchungsperioden-Posten erstellt, indem die Nummer des letzten Artikeljournals verwendet wird, das in die Lagerbuchungsperiode fällt. Außerdem werden die Zeit, das Datum und der Benutzercode, die die Periode schließen, im Lagerbuchungsperioden-Posten erfasst. Wenn Sie diese Information mit dem letzten Artikelpostens für die vorherige Periode verwenden, können Sie sehen, welche Lagertransaktionen in der Lagerbuchungsperiode gebucht wurden. Es ist ebenfalls möglich, Lagerbuchungsperioden erneut zu öffnen, wenn Sie in einer geschlossenen Periode buchen müssen. Wenn Sie eine Lagerbuchungsperiode erneut öffnen, wird ein Lagerbuchungsperioden-Posten erstellt.  

## <a name="see-also"></a>Siehe auch  
 [Unter Designdetails: Lagerkosten](design-details-inventory-costing.md) [Verwalten der Lagerkosten](finance-manage-inventory-costs.md) [Finanzen](finance.md)  
 [Arbeiten mit Financials](ui-work-product.md)

