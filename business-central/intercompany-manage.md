---
title: Verwalten von Intercompanytransaktionen
description: Mit der Intercompany-Funktionalität können Sie die Geschäftsvorgänge und - transaktionen zwischen Unternehmen innerhalb derselben Organisation vereinfachen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: 605
ms.date: 08/11/2021
ms.author: edupont
---
# Intercompanytransaktionen verwalten

Die Funktionen für Intercompanytransaktionen sind für Benutzer vorgesehen, die mehr als eine juristische Geschäftseinheit steuern und mehrere Unternehmen eingerichtet haben, um die Buchungsfunktionen dieser Unternehmen voneinander zu trennen. Diese weitgefasste Beschreibung trifft auf viele Benutzer zu, insbesondere diejenigen, die Geschäfte in internationalen Märkten oder Regionen mit sehr unterschiedlichen Unternehmenskulturen und gesetzlichen Bestimmungen tätigen.

Möglicherweise besteht Ihre Organisation aus mehreren Unternehmen, verfügt jedoch nicht über die entsprechende Anzahl von Buchungs- und Verwaltungsteams. Mithilfe von Intercompanytransaktionen können Sie die Geschäftsvorgänge und -transaktionen zwischen diesen Unternehmen vereinfachen und rationalisieren.

Sobald Sie Intercompanytransaktionen verwenden, können Sie mit Tochtergesellschaften und internen Partnerorganisationen genau so einfach Geschäfte tätigen wie mit externen Lieferanten und Kunden. Die Informationen zu Intercompanytransaktionen geben Sie nur ein einziges Mal in die entsprechenden Belege ein. Sie können die Funktionalität verwenden, mit der Sie bereits vertraut sind, zum Beispiel Debitoren- und Kreditorenverwaltung. Mithilfe der Zuordnungsfunktionen für den Kontenplan und für Dimensionen kann sichergestellt werden, dass die Informationen an der richtigen Stelle angezeigt werden.  

Intercompanybuchungen bieten die folgenden vier wichtigsten Vorteile:  

- Verbesserte Produktivität aufgrund von Zeitersparnis und vereinfachten Transaktionen  
- Minimales Fehlerpotential aufgrund von einmaliger Informationseingabe und systemweiten automatisierten Updates  
- Vollständiger Überwachungspfad und volle Einsehbarkeit von Geschäftsaktivitäten und des Transaktionsverlaufs  
- Effiziente und kosteneffektive Transaktionen mit Konzernunternehmen und Tochtergesellschaften  

## Flow von Geschäftsaktivitäten optimieren  

Mithilfe von Intercompanytransaktionen können Sie innerhalb der Anwendung Verkaufs- und Einkaufsbelege sowie Fibu-Buch.-Blattposten auf alle Außenstellen, Verkaufsbüros oder Tochtergesellschaften verteilen. Zeitersparnis und Effektivitätssteigerung sind überall in der Organisation zu verzeichnen, da die redundante Dateneingabe überflüssig wird und der Versand, Erhalt und Ausdruck sowie die Archivierung von Verkaufs- und Einkaufsbelegen auf Papier nicht mehr erforderlich sind.  

Sie haben Vollzugriff auf alle Transaktionsbelege. So können Sie beispielsweise an Sie geschickte Belege ablehnen und auf diese Weise falsche Buchungen Belege/Lieferungen rückgängig machen. Wenn Sie zum Beispiel einen Einkauf von einem Partnerunternehmen oder einer Tochtergesellschaft aus durchführen, können Sie die Einkaufsbestellung so lange aktualisieren, bis das verkaufende Unternehmen die Waren versandt hat.  

Wenn Sie eine Transaktion eingeben, müssen Sie nicht die Konten für einen einzelnen Satz von Büchern angeben, sondern einfach die ID des Partnerunternehmens. Mithilfe von Intercompanyfunktionen werden Fibu Buch.-Blattzeilen erstellt, die - sobald sie gebucht wurden - im Kontenabschluss beider Mandanten, die an einer Transaktion beteiligt sind, resultieren. In den Forderungen und Verbindlichkeiten weisen Sie jedem Debitor oder Kreditor einen Intercompanypartnercode zu. Von diesem Moment an erstellen alle Aufträge und Rechnungen, die nach Transaktionen mit diesen Unternehmen generiert werden, entsprechende Belege im Partnerunternehmen, mit dem Ergebnis des richtigen Regulierens der Konten.  

Die Funktionen für Intercompanytransaktionen konzentrieren sich in erster Linie auf die Unterstützung von Intercompanytransaktionen mithilfe von Einkaufs- und Verkaufsbelegen und Fibu-Buch.-Blattzeilen. Innerhalb dieses Bereichs werden durch Intercompanytransaktionen Intercompanytransaktionen zwischen mehreren Datenbanken von [!INCLUDE [prod_short](includes/prod_short.md)] ermöglicht, beispielsweise in unterschiedlichen Ländern/Regionen sowie bei verschiedenen Währungen, Kontenplänen, Dimensionen und abweichender Artikelnummerierung.  

Bei Intercompanytransaktionen werden die folgenden Posten und Belege in Intercompanytransaktionen verwendet:  

- Fibu-Buch.-Blattposten
- Einkaufsbestellungen und Verkaufsaufträge
- Einkaufs- und Verkaufsrechnungen
- Gutschriften
- Reklamationen

Bei der Einrichtung von Intercompanytransaktionen erstellen Sie eine Liste der Intercompanypartner (auch als IC-Partner bezeichnet) und einen Intercompanykontenplan. Anschließend können Sie Intercompanytransaktionen in Fibu-Buch.-Blättern durchführen. Ggf. erforderliche Dimensionen richten Sie separat ein.  

> [!NOTE]
> Das Fibu-Buch.-Blatt selbst keine Währungsfunktionalität beinhaltet, jedoch alle Beträge zu dem gültigen Kurs in die lokale Währung umgerechnet werden.

Nachdem Sie Ihre Geschäftspartner im System als Debitoren und Kreditoren eingerichtet haben und ihnen IC-Partnercodes zugewiesen haben, können IC-Einkaufs- und Verkaufsbelege ausgetauscht werden, die Artikel und Zu- bzw. Abschläge für Artikel enthalten. [!INCLUDE [prod_short](includes/prod_short.md)] unterstützt Intercompanybuchungen zwischen mehreren Datenbanken, beispielsweise in unterschiedlichen Ländern/Regionen sowie bei verschiedenen Währungen, Kontenplänen, Dimensionen und abweichender Artikelnummerierung.  

> [!NOTE]
> Nicht alle Datentypen können auf diese Weise zwischen Unternehmen ausgetauscht werden. Einkaufsrechnungen werden nicht über konzerninterne Prozesse an Geschäftspartner übermittelt. Verkaufsrechnungen, die über konzerninterne Prozesse eingereicht werden, werden jedoch als Eingangsrechnungen im empfangenden Unternehmen erstellt.

Die Konsolidierung von Finanzdaten kann insbesondere für Vorgänge innerhalb des Unternehmens relevant sein. Weitere Informationen finden Sie unter [Konsolidieren von Finanzdaten aus mehreren Unternehmen](finance-consolidated-company-reporting.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben..

|Aktion |Siehe|
|---|---|
|Erstellen Sie Ihre Intercompanykreditoren und -debitoren als so genannte Intercompanypartner, und richten Sie einen Intercompanykontenplan ein.|[Intercompany einrichten](intercompany-how-setup.md)|
|Intercompanybelege werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwenden.|[Arbeiten mit Intercompany-Belegen und Buch.-Blättern](intercompany-how-work-documents-journals.md)|
|Organisieren Sie und verarbeiten Sie die eingehenden und ausgehenden Transaktionen, die Sie zwischen Intercompanypartnern austauschen.|[Intercompany-Ein- und -Ausgangstransaktionen verwalten](intercompany-how-manage-intercompany-inbox.md)|
|Verwenden Sie konzerninterne Transaktionen, um die Kosten zwischen Partnerunternehmen zu verteilen.|[Kosten den Intercompanypartnern zuordnen](intercompany-allocate-costs.md)|

## Weitere Informationen

[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
