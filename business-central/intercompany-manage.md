---
title: Transaktionen zwischen Unternehmen in derselben Organisation| Microsoft Docs
description: Mit der Intercompany-Funktionalität können Sie die Geschäftsvorgänge und - transaktionen zwischen Unternehmen innerhalb derselben Organisation vereinfachen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fbe84deebc00b07536cda6cb36a3a0784450d62f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786148"
---
# <a name="managing-intercompany-transactions"></a>Intercompanytransaktionen verwalten
Möglicherweise besteht Ihre Organisation aus mehreren Unternehmen, verfügt jedoch nicht über die entsprechende Anzahl von Buchungs- und Verwaltungsteams. Die Intercompany-Funktionalität macht es möglich, Geschäfte mit Tochtergesellschaften und internen Partnerorganisationen genau so einfach zu tätigen wie mit externen Lieferanten und Kunden. Die Informationen zu Intercompanytransaktionen geben Sie nur ein einziges Mal in die entsprechenden Belege ein. Sie können die Funktionalität verwenden, mit der Sie bereits vertraut sind, zum Beispiel Debitoren- und Kreditorenverwaltung. Mithilfe der Zuordnungsfunktionen für den Kontenplan und für Dimensionen kann sichergestellt werden, dass die Informationen an der richtigen Stelle angezeigt werden.  

Intercompanybuchungen bieten die folgenden vier wichtigsten Vorteile:  

- Verbesserte Produktivität aufgrund von Zeitersparnis und vereinfachten Transaktionen  
- Minimales Fehlerpotential aufgrund von einmaliger Informationseingabe und systemweiten automatisierten Updates  
- Vollständiger Überwachungspfad und volle Einsehbarkeit von Geschäftsaktivitäten und des Transaktionsverlaufs  
- Effiziente und kosteneffektive Transaktionen mit Konzernunternehmen und Tochtergesellschaften  

Sie haben Vollzugriff auf alle Transaktionsbelege. So können Sie beispielsweise an Sie geschickte Belege ablehnen und auf diese Weise falsche Buchungen Belege/Lieferungen rückgängig machen. Wenn Sie zum Beispiel einen Einkauf von einem Partnerunternehmen oder einer Tochtergesellschaft aus durchführen, können Sie die Einkaufsbestellung so lange aktualisieren, bis das verkaufende Unternehmen die Waren versandt hat.  

Wenn Sie eine Transaktion eingeben, müssen Sie nicht die Konten für einen einzelnen Satz von Büchern angeben, sondern einfach die ID des Partnerunternehmens. Mithilfe von Intercompanybuchungen werden Fibu Buch.-Blattzeilen erstellt, die - sobald sie gebucht wurden - im Kontenabschluss beider Mandanten, die an einer Transaktion beteiligt sind, resultieren. In den Forderungen und Verbindlichkeiten weisen Sie jedem Debitor oder Kreditor einen Intercompanypartnercode zu. Von diesem Moment an erstellen alle Aufträge und Rechnungen, die nach Transaktionen mit diesen Unternehmen generiert werden, entsprechende Belege im Partnerunternehmen, mit dem Ergebnis des richtigen Regulierens der Konten.  

 Nachdem Sie Ihre Geschäftspartner im System als Debitoren und Kreditoren eingerichtet haben und ihnen IC-Partnercodes zugewiesen haben, können IC-Einkaufs- und Verkaufsbelege ausgetauscht werden, die Artikel und Zu- bzw. Abschläge für Artikel enthalten. Innerhalb dieses Bereichs werden durch Intercompanybuchungen Intercompanytransaktionen zwischen mehreren Datenbanken ermöglicht, beispielsweise in unterschiedlichen Ländern/Regionen sowie bei verschiedenen Währungen, Kontenplänen, Dimensionen und abweichender Artikelnummerierung.  

Die Konsolidierung von Finanzdaten kann insbesondere in Verbindung mit Intergesellschaftsvorgängen relevant sein. Weitere Informationen finden Sie unter [Konsolidieren von Finanzdaten aus mehreren Unternehmen](finance-consolidated-company-reporting.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Themen, die sie beschreiben..

|An |Siehe|
|---|---|
|Erstellen Sie Ihre Intercompanykreditoren und -debitoren als so genannte Intercompanypartner, und richten Sie einen Intercompanykontenplan ein.|[Intercompany einrichten](intercompany-how-setup.md)|
|Intercompanybelege werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwenden.|[Arbeiten mit Intercompany-Belegen und Buch.-Blättern](intercompany-how-work-documents-journals.md)|
|Organisieren Sie und verarbeiten Sie die eingehenden und ausgehenden Transaktionen, die Sie zwischen Intercompanypartnern austauschen.|[Intercompany-Ein- und -Ausgangstransaktionen verwalten](intercompany-how-manage-intercompany-inbox.md)|
|Verwenden Sie konzerninterne Buchungen, um die Kosten zwischen Partnerunternehmen zu verteilen.|[Kosten den Intercompanypartnern zuordnen](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Siehe auch
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit allgemeinen Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]