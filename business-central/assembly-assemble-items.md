---
title: Montageverwaltung
description: 'Erfahren Sie, wie Sie Produkte an Kunden liefern, indem Sie Komponenten in einfachen Prozessen kombinieren, ohne Fertigungsfunktionen zu verwenden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="assembly-management"></a><a name="assembly-management"></a>Montageverwaltung

Unternehmen können Produkte an Kunden liefern, indem sie Komponenten kombinieren, ohne Fertigungsfunktionen zu verwenden. Funktionen zum Zusammenstellen von Artikeln lassen sich in verwandte Funktionen wie Verkauf, Planung, Reservierungen und Lagerhaltung integrieren.  

Ein Montageartikel ist ein verkäuflicher Artikel, der eine Montagestückliste enthält. Weitere Informationen zu Montagestücklisten finden Sie unter [Arbeiten mit Montagestücklisten](assembly-how-work-assembly-boms.md).

Montageaufträge sind, wie Fertigungsaufträge, interne Aufträge. Verwenden Sie Montageaufträge, um den Montageprozess zu verwalten und Verkaufsanforderungen mit Lageraktivitäten zu verbinden. Montageaufträge beinhalten bei der Buchung sowohl Ausgabe als auch Verbrauch. Montageauftragskopfzeilen ähneln Ausgabeerfassungszeilen. Montageauftragszeilen ähneln Verbrauchserfassungszeilen.  

Sie können eine Just-in-Time-Bestandsstrategie verwenden und Produkte an Kundenwünsche anpassen. Montageaufträge können automatisch erstellt und bei der Erstellung einer Verkaufsauftragszeile verknüpft werden. Die Verbindung zwischen Verkaufsbedarf und Montagevorrat eröffnet mehrere Möglichkeiten bei der Abwicklung von Kundenaufträgen:

* Passen Sie Montageartikeln ad hoc an.
* Versprechen Sie Liefertermine gemäß der Komponentenverfügbarkeit.
* Buchen Sie die Ausgabe und den Versand des montierten Artikels direkt aus ihren Verkaufsaufträgen.

Weitere Informationen zum Verkauf von Montageartikeln finden Sie unter [Verkauf von Artikeln, die auf Bestellung gefertigt wurden](assembly-how-to-sell-items-assembled-to-order.md).  

Positionen in Kundenaufträgen können aus dem Lager zu entnehmende Artikel und für den Auftrag zu montierende Artikel enthalten. Die Auftragsmontagemengen haben bei Teillieferungen Vorrang vor Bestandsmengen. Weitere Informationen zum Verkauf von Lager- und Montageartikeln finden Sie unter [Kombinationsszenarien](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Sobald eine Auftragsmontagemenge für die Lieferung bereitsteht, kann ein Lagermitarbeiter die Lagerbestandskommissionierung für die Verkaufsauftragszeilen buchen. Das Buchen einer Lagerbestandskommissionierung bewirkt ein paar Dinge:

* Eine Lagerbestandsumlagerung für die Komponenten erstellen
* Buchen Sie die Montageausgabe und den Verkaufsauftragsversand.

Weitere Informationen zu Auftragsmontageartikeln und Lagerbestandskommissionierung finden Sie unter [Handhabung von Auftragsmontageartikeln mit Bestandskommissionierung](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

Die folgende Tabelle beschreibt eine Reihe von Aufgaben mit Links zu den Artikeln, die sie beschreiben.

|**Bis**|**Siehe**|  
|------------|-------------|  
|Erfahren Sie mehr über das Montieren von Artikeln für Verkaufsaufträge und Lagerung.|[Auftragsmontage und Lagermontage verstehen](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Verwenden Sie Lagerortkarten und Ihre Lagereinrichtung, um zu definieren, wie der Fluss der Artikel in der Montage ist.|[Einrichten von Basislagern mit Vorgangsbereichen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Bieten Sie einen anpgepassten Montageartikel an und konvertieren Sie das Angebot in einen Verkauf, wenn es vom Kunden akzeptiert wird.|[Angebot eines Auftragsmontageverkaufs](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Kombinieren Sie Komponenten, um einen Artikel für einen Auftrag oder für das Lager zu erstellen.|[Artikel montieren](assembly-how-to-assemble-items.md)|  
|Verkaufen Sie Montageartikel, die zu dem Zeitpunkt nicht verfügbar sind, indem Sie einen verknüpften Montageauftrag erstellen, um die gesamte oder einen Teil der Verkaufauftragsmenge zu beziehen.|[Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md)|
|Wenn Auftragsmontageartikel bereits im Lager vorhanden sind, dann ziehen Sie die Menge von dem Montageauftrag ab und reservieren sie aus dem Lager.|[So verkaufen Sie Lagerartikel in Programmfertigungs-Flüssen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Wenn sich Montageartikel nicht im Bestand befinden, verwenden Sie einen Montageauftrag, um einen Teil oder die gesamte Menge zu liefern.|[So verkaufen Sie Auftragsmontageartikel und Lagerartikel zusammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Erstellen Sie benutzerdefinierte Montageartikel für Rahmenaufträge, bevor Sie die Verkaufsaufträge erstellen.|[Erstellen von Montagerahmenaufträgen](assembly-how-to-create-blanket-assembly-orders.md)|
|Rückgängigmachen eines gebuchten Montageauftrags, beispielsweise wenn der Auftrag mit Fehlern gebucht wurde.|[Montagesbuchungen rückgängig machen](assembly-how-to-undo-assembly-posting.md)|
|Erfahren Sie, wie Sie mit Montagestücklisten arbeiten und wie sie sich von Fertigungsstücklisten unterscheiden.|[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)|
|Erfahren Sie mehr über das Buchen von Montageverbrauch und -ausgabe und wie [!INCLUDE [prod_short](includes/prod_short.md)] Artikel- und Ressourcenkosten auf das Hauptbuch verteilt.|[Designdetails: Montageauftragsbuchung](design-details-assembly-order-posting.md)|  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Siehe zugehörige [Microsoft Schulungen](/training/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Arbeiten mit Stücklisten](inventory-how-work-BOMs.md)  
[Bestand](inventory-manage-inventory.md)  
[Überblick über die Lagerverwaltung](design-details-warehouse-management.md)
[Designdetails: Beschaffungsplanung](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
