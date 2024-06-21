---
title: Verwalten von Intercompanytransaktionen
description: Mit der Intercompany-Funktionalität können Sie die Geschäftsvorgänge und - transaktionen zwischen Unternehmen innerhalb derselben Organisation vereinfachen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
ms.service: dynamics-365-business-central
---
# <a name="managing-intercompany-transactions"></a>Intercompanytransaktionen verwalten

Unternehmen mit mehr als einer juristischen Person mit getrennten Buchhaltungsfunktionen können von konzerninternen Transaktionen profitieren. Es ist beispielsweise nützlich für Unternehmen, die Niederlassungen in mehreren internationalen Märkten oder Regionen haben. Oder Ihre Organisation besteht aus mehreren Unternehmen, verfügt jedoch nicht über die entsprechende Anzahl von Buchungs- und Verwaltungsteams. Mithilfe von Intercompanytransaktionen können Sie die Geschäftsvorgänge und -transaktionen zwischen diesen Unternehmen in der Intercompanypartnerschaft vereinfachen und rationalisieren.

Wenn Sie die Debitoren- und Kreditorenbeziehungen für Intercompany-Transaktionen angegeben haben, geben Partner die Informationen einmal in Verkaufs- und Einkaufsdokumente ein. Beim anderen an der Transaktion beteiligten Partner wird ein entsprechendes Dokument erstellt. Mithilfe der Zuordnungsfunktionen für den Kontenplan und für Dimensionen kann sichergestellt werden, dass die Informationen an der richtigen Stelle angezeigt werden.  

Intercompanyfunktionen bieten die folgenden vier wichtigsten Vorteile:  

* Verbesserte Produktivität aufgrund von Zeitersparnis und vereinfachten Transaktionen  
* Minimales Fehler aufgrund von einmaliger Informationseingabe und systemweiten automatisierten Updates  
* Vollständiger Überwachungspfad und volle Einsehbarkeit von Geschäftsaktivitäten und des Transaktionsverlaufs  
* Effiziente und kosteneffektive Transaktionen mit Konzernunternehmen und Tochtergesellschaften  

## <a name="streamline-the-flow-of-business-activities"></a>Flow von Geschäftsaktivitäten optimieren

Mithilfe von Intercompanytransaktionen können Sie innerhalb der Anwendung Verkaufs- und Einkaufsbelege und Fibu-Buch.-Blattposten auf alle Außenstellen, Verkaufsbüros oder Tochtergesellschaften verteilen. Die Verteilung von Transaktionen spart Zeit und steigert die Effizienz im gesamten Unternehmen, indem die Dateneingabe reduziert wird. Es reduziert die Notwendigkeit, Verkaufs- und Einkaufsdokumente zu senden, zu empfangen, zu drucken und zu archivieren.  

Sie haben Vollzugriff auf alle Transaktionsbelege. So können Sie beispielsweise an Sie geschickte Belege ablehnen und die Aktionen **Falsche Buchungen** und **Belege/Lieferungen rückgängig machen**, um diese Korrekturen vorzunehmen. Wenn Sie zum Beispiel einen Einkauf von einem Partnerunternehmen oder einer Tochtergesellschaft aus durchführen, können Sie die Einkaufsbestellung so lange aktualisieren, bis das verkaufende Unternehmen die Waren versandt hat.  

Wenn Sie eine Transaktion eingeben, müssen Sie die zu verwendenden Konten nicht angeben. Sie wählen einfach den Intercompanypartner aus. Mithilfe von Intercompanyfunktionen werden Fibu Buch.-Blattzeilen erstellt, die - sobald sie gebucht wurden - im Kontenabschluss beider Mandanten, die an einer Transaktion beteiligt sind, resultieren. In den Forderungen und Verbindlichkeiten weisen Sie jedem Debitor oder Kreditor einen Intercompanypartnercode zu. Ab diesem Zeitpunkt erzeugen alle Bestellungen und Rechnungen für Transaktionen zwischen diesen Unternehmen entsprechende Dokumente im Partnerunternehmen. Das Ergebnis sind korrekt ausgeglichene Konten.  

Intercompany konzentriert sich auf Verkaufs- und Einkaufsdokumente und allgemeine Buchungszeilen und ermöglicht Transaktionen zwischen mehreren [!INCLUDE [prod_short](includes/prod_short.md)] Datenbanken. Beispiel:

* In verschiedenen Ländern/Regionen
* Mehrere Währungen
* Verschiedene Kontenpläne
* Verschiedene Dimensionen
* Verschiedene Artikelnummern  

Intercompany-Transaktionen verwenden mehrere Arten von Einträgen und Dokumenten:  

* Fibu-Buch.-Blattposten
* Einkaufsbestellungen und Verkaufsaufträge
* Einkaufs- und Verkaufsrechnungen
* Gutschriften
* Reklamationen

Bei der Einrichtung von Intercompanytransaktionen erstellen Sie eine Liste der Intercompanypartner, einen Intercompanykontenplan und Intercompanydimensionen. Anschließend können Sie Buchungen in Intercompany-Hauptbuchungen erstellen.

> [!NOTE]
> Das allgemeine Journal selbst enthält keine Währungen. Es rechnet alle Beträge zum aktuellen Wechselkurs in die Landeswährung um.

Nachdem Sie Ihre Geschäftspartner im System als Debitoren und Kreditoren eingerichtet haben und ihnen IC-Partnercodes zugewiesen haben, können IC-Einkaufs- und Verkaufsbelege ausgetauscht werden, die Artikel und Zu- bzw. Abschläge für Artikel enthalten. 

> [!NOTE]
> Unternehmen können nicht alle Arten von Daten zwischenbetrieblich austauschen. Einkaufsrechnungen werden nicht über konzerninterne Prozesse an Geschäftspartner übermittelt. Verkaufsrechnungen, die über konzerninterne Prozesse eingereicht werden, werden jedoch als Eingangsrechnungen im empfangenden Unternehmen erstellt.

Die Konsolidierung von Finanzdaten könnte insbesondere für Vorgänge innerhalb des Unternehmens relevant sein. Weitere Informationen finden Sie unter [Konsolidieren von Finanzdaten aus mehreren Unternehmen](finance-consolidated-company-reporting.md).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.

|Bis |Siehe|
|---|---|
|Erstellen Sie Ihre Intercompanykreditoren und -debitoren als so genannte Intercompanypartner, und richten Sie einen Intercompanykontenplan ein.|[Intercompany einrichten](intercompany-how-setup.md)|
|Intercompanybelege werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwenden.|[Arbeiten mit Intercompany-Belegen und Buch.-Blättern](intercompany-how-work-documents-journals.md)|
|Organisieren Sie und verarbeiten Sie die eingehenden und ausgehenden Transaktionen, die Sie zwischen Intercompanypartnern austauschen.|[Intercompany-Ein- und -Ausgangstransaktionen verwalten](intercompany-how-manage-intercompany-inbox.md)|
|Verwenden Sie konzerninterne Transaktionen, um die Kosten zwischen Partnerunternehmen zu verteilen.|[Kosten den Intercompanypartnern zuordnen](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Weitere Informationen

[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
