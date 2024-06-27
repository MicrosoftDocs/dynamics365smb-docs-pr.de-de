---
title: Elementtypen verstehen
description: 'Erfahren Sie mehr über die Arten von Artikeln, die Sie im Bestand verwalten können, und deren Auswirkungen. Sie können die Bestandsbewertung eines Artikels mit der Lagerabgangsmethode „FIFO“ oder „Durchschnitt“ anpassen, wenn sich die Artikelkosten aus anderen Gründen als Transaktionen ändern.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Info zu Artikeltypen

Im Feld **Typ** auf der Seite **Artikelkarte** können Sie auswählen, wofür das Element in Ihrem Unternehmen verwendet wird, was sich auf den Grad auswirkt, in dem Sie das Element im Bestand verwalten können. In der folgenden Tabelle sind die drei verfügbaren Arten von Elementen aufgeführt und beschrieben.

|Option|Typischer Zweck|
|------|-----------|
|Bestand|Physische Dinge, wie Fahrräder, Telefone und Schreibtische, für die Sie alle Bestandsprozesse nutzen können möchten. Lagerartikel können auch nicht-physische Elemente wie Softwarelizenzen und Abonnements umfassen, wenn die Elemente über Identifikationsnummern, wie z.B. Seriennummern, verfügen. Sie können die Werte und die Verfügbarkeit von Elementen im Bestand vollständig verfolgen.|
|Kein Lagerbestand|In der Regel handelt es sich bei nicht inventarisierten Elementen um physische Gegenstände wie Schrauben oder Stifte, die Ihr Unternehmen verbraucht, aber nicht vollständig im Bestand verfolgt. Zum Beispiel, weil es sich um preisgünstige Elemente handelt, die nur intern verwendet werden.|
|Dienst|Eine Arbeitszeiteinheit, wie eine Beratungsstunde, für begrenzte Geschäftsunterstützung.|

> [!NOTE]
> Die Typen **Dienstleistung** und **Nicht-Bestand** lassen keine Verfolgung von Bestandsmengen und -werten zu. Es werden nur ausgewählte Transaktionstypen und Funktionen für Artikel unterstützt. In der folgenden Tabelle sind die Funktionen aufgeführt, die die drei Artikelarten unterstützen.

|Artikelart|Verkauf|Einkauf|Job-Verbrauch|Serviceverbrauch|Verbrauch für Montage|Produktions-Verbrauch|Montageausstoß|Fertig produzierte Artikel (Istmeldungen)|Lagerortumlagerung|Physische Zählung|Bestandsneubewertung|Bestandskosten|Artikelverfolgung|Reservierung|Lagerhaus|Planung|Auftragsplanung|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Inventar|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Kein Lagerbestand|Ja|Ja|Ja|Ja|Ja|Ja|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Ja|
|Dienst|Ja|Ja|Ja|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Ja|

## Kalkulationsmethoden für Artikeltypen

Wenn Sie Lagerbuchungen vornehmen, werden die Mengen- und Wertänderungen des Bestands in den Artikelposten bzw. Wertposten erfasst.

Die Kosten für Bestandsartikel werden im Feld **Einstandsbetrag (tatsächl.)** auf der Seite **Wertposten** erfasst. Wenn Sie den Eintrag mit dem Hauptbuch abgleichen, werden die Kosten im Feld **Gebuchte Lagerregulierung** angezeigt. Weitere Informationen zur Lagerkostenberechnung finden Sie unter [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md).

Für Nicht-Bestands- und Serviceartikel werden die Kosten im Feld **Einst.-Betr. (lagerwertunabh.)** auf der Seite **Wertposten** erfasst. Geben Sie für Nicht-Bestands- und Serviceartikel die Kosten in den Verkaufs-, Montage- und Produktionsbelegen und -buchungsblättern an. Geben Sie die Standardkosten im Feld **Einstandspreis** auf den Seiten **Artikelkarte** und **Lagerhaltungsdaten** an. Die Kosten für diese Arten von Artikeln werden nicht mit der Finanzbuchhaltung abgeglichen.

## Katalog- und Serviceartikel

Sie können Artikel einrichten, die Sie Ihren Debitoren zwar anbieten, aber erst verwalten, wenn Sie sie als Katalogartikel verkaufen. Obwohl Katalogartikel in dieser Hinsicht normalen Artikeln vom Typ **Nicht-Bestand** ähneln, sollten Sie die beiden nicht verwechseln, da es Unterschiede gibt. Weitere Informationen finden Sie unter [Mit Katalogartikeln arbeiten](inventory-how-work-nonstock-items.md).

Debitorenartikel, die Sie warten, z. B Drucker, werden als Serviceartikel bezeichnet. Serviceartikel haben nichts mit regulärem oder Katalogelementen zu tun. Aber Servicekomponenten können normale Artikel sein. Weitere Informationen finden Sie unter [Serviceartikel und Serviceartikelkomponenten einrichten](service-how-setup-service-items.md).

## Siehe auch

[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand einrichten](inventory-setup-inventory.md)  
[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
