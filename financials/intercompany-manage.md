---
title: Transaktionen zwischen Unternehmen in derselben Organisation| Microsoft Docs
description: "Mit der Intercompany-Funktionalität können Sie die Geschäftsvorgänge und - transaktionen zwischen Unternehmen innerhalb derselben Organisation vereinfachen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/20/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: 5ffaed472ab61d086e2b57579523340504bde119
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="managing-intercompany-transactions"></a>Intercompanytransaktionen verwalten
Möglicherweise besteht Ihre Organisation aus mehreren Unternehmen, verfügt jedoch nicht über die entsprechende Anzahl von Buchungs- und Verwaltungsteams. Die Intercompany-Funktionalität macht es möglich, Geschäfte mit Tochtergesellschaften und internen Partnerorganisationen genau so einfach zu tätigen wie mit externen Lieferanten und Kunden. Die Informationen zu Intercompanytransaktionen geben Sie nur ein einziges Mal in die entsprechenden Belege ein. Sie können die Funktionalität verwenden, mit der Sie bereits vertraut sind, zum Beispiel Debitoren- und Kreditorenverwaltung. Mithilfe der Zuordnungsfunktionen für den Kontenplan und für Dimensionen kann sichergestellt werden, dass die Informationen an der richtigen Stelle angezeigt werden.  

Intercompanybuchungen bieten die folgenden vier wichtigsten Vorteile:  

- Verbesserte Produktivität aufgrund von Zeitersparnis und vereinfachten Transaktionen  
- Minimales Fehlerpotential aufgrund von einmaliger Informationseingabe und systemweiten automatisierten Updates  
- Vollständiger Überwachungspfad und volle Einsehbarkeit von Geschäftsaktivitäten und des Transaktionsverlaufs  
- Effiziente und kosteneffektive Transaktionen mit Konzernunternehmen und Tochtergesellschaften  

Sie haben Vollzugriff auf alle Transaktionsbelege. So können Sie beispielsweise an Sie geschickte Belege ablehnen und auf diese Weise falsche Buchungen rückgängig machen. Wenn Sie zum Beispiel einen Einkauf von einem Partnerunternehmen oder einer Tochtergesellschaft aus durchführen, können Sie die Einkaufsbestellung so lange aktualisieren, bis das verkaufende Unternehmen die Waren versandt hat.  

Wenn Sie eine Transaktion eingeben, müssen Sie nicht die Konten für einen einzelnen Satz von Büchern angeben, sondern einfach die ID des Partnerunternehmens. Mithilfe von Intercompanybuchungen werden Fibu Buch.-Blattzeilen erstellt, die - sobald sie gebucht wurden - im Kontenabschluss beider Mandanten, die an einer Transaktion beteiligt sind, resultieren. In den Forderungen und Verbindlichkeiten weisen Sie jedem Debitor oder Kreditor einen Intercompanypartnercode zu. Von diesem Moment an erstellen alle Aufträge und Rechnungen, die nach Transaktionen mit diesen Unternehmen generiert werden, entsprechende Belege im Partnerunternehmen, mit dem Ergebnis des richtigen Regulierens der Konten.  

 Nachdem Sie Ihre Geschäftspartner im System als Debitoren und Kreditoren eingerichtet haben und ihnen IC-Partnercodes zugewiesen haben, können IC-Einkaufs- und Verkaufsbelege ausgetauscht werden, die Artikel und Zu- bzw. Abschläge für Artikel enthalten. Innerhalb dieses Bereichs werden durch Intercompanybuchungen Intercompanytransaktionen zwischen mehreren Datenbanken von  ermöglicht, beispielsweise in unterschiedlichen Ländern/Regionen sowie bei verschiedenen Währungen, Kontenplänen, Dimensionen und abweichender Artikelnummerierung.  

Die folgende Tabelle enthält eine Abfolge von Aufgaben sowie Links zu den entsprechenden Themen, in denen diese Aufgaben erläutert werden.

 |An |Siehe|
 |---|---|
 |Erstellen Sie Ihre Intercompanykreditoren und -debitoren als so genannte Intercompanypartner, und richten Sie einen Intercompanykontenplan ein.|[Vorgehensweise: Intercompany einrichten](intercompany-how-setup.md)|
 |Intercompanybelege werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwenden.|[Vorgehensweise: Arbeiten mit Intercompany-Belegen und Buch.-Blättern](intercompany-how-work-documents-journals.md)|
 |Organisieren Sie und verarbeiten Sie die eingehenden und ausgehenden Transaktionen, die Sie zwischen Intercompanypartnern austauschen.|[So geht's: Intercompany-Ein- und -Ausgangstransaktionen verwalten](intercompany-how-manage-intercompany-inbox.md)|

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

