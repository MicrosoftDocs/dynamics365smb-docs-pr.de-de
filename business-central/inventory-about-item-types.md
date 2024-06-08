---
title: Verstehen von Element-Typen
description: 'Sie können die Bestandsbewertung eines Elements mit der FIFO- oder Durchschnittskalkulation anpassen, wenn sich die Kosten des Elements aus anderen Gründen als Transaktionen ändern.'
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="about-item-types"></a>Info zu Elementtypen
Im Feld **Typ** auf der Seite **Artikelkarte** können Sie auswählen, wofür das Element in Ihrem Unternehmen verwendet wird, was sich auf den Grad auswirkt, in dem Sie das Element im Bestand verwalten können. In der folgenden Tabelle sind die drei verfügbaren Arten von Elementen aufgeführt und beschrieben.

|Option|Typischer Zweck|
|------|-----------|
|Bestand|Physische Dinge, wie Fahrräder, Telefone und Schreibtische, für die Sie alle Bestandsprozesse nutzen können möchten. Dazu können auch nicht-physische Elemente wie Softwarelizenzen und Abonnements gehören, wenn die Elemente über Identifikationsnummern, wie z.B. Seriennummern, verfügen. Sie können die Werte und die Verfügbarkeit von Elementen im Bestand vollständig verfolgen.|
|Kein Bestand|In der Regel handelt es sich bei nicht inventarisierten Elementen um physische Gegenstände wie Schrauben oder Stifte, die ein Unternehmen verbraucht, aber nicht vollständig im Bestand verfolgen möchte. Zum Beispiel, weil es sich um preisgünstige Elemente handelt, die nur intern verwendet werden.|
|Service|Eine Arbeitszeiteinheit, wie eine Beratungsstunde, für begrenzte Geschäftsunterstützung.|

> [!NOTE]
> Die Typen **Dienstleistung** und **Nicht-Bestand** unterstützen die Verfolgung von Bestandsmengen und -werten nicht. Es werden nur ausgewählte Transaktionstypen und Funktionen für Artikel unterstützt.

In der folgenden Tabelle sind die Funktionen aufgeführt, die die drei Artikelarten unterstützen.

|Artikelart|Verkauf|Einkauf|Job-Verbrauch|Serviceverbrauch|Verbrauch für Montage|Produktions-Verbrauch|Montageausstoß|Fertig produzierte Artikel (Istmeldungen)|Lagerortumlagerung|Physische Zählung|Bestandsneubewertung|Bestandskosten|Artikelverfolgung|Reservierung|Lagerhaus|Planung|Auftragsplanung|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Inventar|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Kein Lagerbestand|Ja|Ja|Ja|Ja|Ja|Ja|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Ja|
|Dienst|Ja|Ja|Ja|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Nein|Ja|

## <a name="costing-methods-for-types-of-items"></a>Kalkulationsmethoden für Artikeltypen
Wenn Sie Lagerbuchungen vornehmen, werden die Mengen- und Wertänderungen des Bestands in den Artikelposten bzw. Wertposten erfasst. 

Für Lagerartikel werden die Kosten im Feld **Einstandsbetrag (tatsächl.)** auf der Seite **Wertposten** erfasst und bei der Abstimmung mit der Finanzbuchhaltung werden die Kosten im Feld **Gebuchte Lagerregulierung** angezeigt. Weitere Informationen finden Sie unter [Designdetails: Bestandskosten](design-details-inventory-costing.md).

Für Nicht-Bestands- und Serviceartikel werden die Kosten im Feld **Einst.-Betr. (lagerwertunabh.)** auf der Seite **Wertposten** erfasst. Für Nicht-Bestands- und Serviceartikel werden die Kosten in den Verkaufs-, Montage- und Produktionsbelegen und -buchungsblättern angegeben. Die Standardkosten können im Feld **Einstandspreis** auf den Seiten **Artikelkarte** und **Lagerhaltungsdaten** angegeben werden. Die Kosten für diese Arten von Artikeln werden nicht mit der Finanzbuchhaltung abgeglichen. 

## <a name="catalog-and-service-items"></a>Katalog- und Serviceartikel
Sie können Ihren Debitoren bestimmte Artikel als Dienstleistung anbieten, die Sie nicht im Lager verwalten möchten, bis Sie den Verkauf sie starten. Katalogelemente sollen nicht mit regulären Artikel der Art Kein Bestand verwechselt werden. Weitere Informationen finden Sie unter [Arbeiten mit Katalogelementen](inventory-how-work-nonstock-items.md).

Die Artikel der Debitoren, die Sie im Service, wie z. B Drucker anbieten, werden Serviceartikel genannt. Serviceartikel haben nichts mit regulärem oder Katalogelementen zu tun. Aber Servicekomponenten können normale Artikel sein. Weitere Informationen finden Sie unter [Serviceartikelkomponenten und Serviceartikel einrichten](service-how-setup-service-items.md).

## <a name="see-also"></a>Siehe auch
[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Bestand einrichten](inventory-setup-inventory.md)  
[Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
