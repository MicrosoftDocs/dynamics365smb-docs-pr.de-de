---
title: Verwaltung von Bestand | Microsoft Docs
description: Beschreibt, wie physischen Produkte verwaltet werden, die Sie im Lagerbestand in Ihrem Lager verwalten.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 1aa1a7c2ec56c3f123bde67a9870be4efd99bdb5
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---

# <a name="inventory"></a>Lagerbest
Für jedes physische Produkt, mit dem Sie handeln, müssen Sie eine Artikelkarte vom Typ **Lagerbestand** erstellen. Artikel, die Sie Debitoren anbieten, aber nicht im Lager führen, können als Katalogartikel erfassen werden und Sie können Sie bei Bedarf in Lagerartikel konvertieren. Sie können die Menge eines Artikels im Lager erhöhen oder vermindern, indem Sie direkt in den Artikelposten buchen, beispielsweise nach einer physischen Zählung oder falls keine erworbenen Mengen erfasst wurden.

Lagerzugänge und Abgänge werden natürlich auch erfasst, wenn Sie Einkaufs- und Verkaufsbelege buchen. Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md), [So gehts: Produkte verkaufen](sales-how-sell-products.md) und [So gehts: Fakturieren](sales-how-invoice-sales.md). Umlagerungen zwischen Lagerorten ändert Lagerbestandsmengen in den Lagern Ihres Mandanten.   

Um die Übersicht über Artikel zu erhöhen und die Suche zu erleichtern, können Sie Artikel kategorisieren und ihnen Attribute zuweisen, nach denen sie gesucht und sortiert werden können.

> [!NOTE]
> Die physische Bewegung der Artikel wird als Lageraktivitäten bezeichnet. Weitere Informationen finden Sie unter [Lagerortverwaltung](warehouse-manage-warehouse.md).

## <a name="inventory-reconciliation"></a>Abstimmung des Lagerbestands
Wenn Sie Lagertransaktionen buchen, z. B. Verkaufslieferungen, Einkaufsrechnungen oder Lagerregulierungen, werden die veränderten Artikelkosten in den Artikelwerteinträgen aufgezeichnet. Um diese Änderung des Lagerwerts in Ihren Finanzbüchern wiederzugeben, werden die Lagerkosten automatisch zu den entsprechenden Lagerkonten in der Finanzbuchhaltung gebucht. Für jede Lagertransaktion, die Sie buchen, werden die entsprechenden Werte in der Hauptbuchhaltung im Lagerkonto, im Korrekturkonto und im Lagerverbrauchskonto gebucht. Weitere Informationen finden Sie unter [So gehts: Lagerregulierung mit Finanzbuchhaltung abstimmen](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Selbst wenn Lagerkosten automatisch in die Finanzbuchhaltung gebucht werden, ist es immer noch notwendig sicherzustellen, dass die Kosten für Waren zur zugehörigen ausgehenden Transaktion weitergeleitet werden, insbesondere in Situationen, in denen Sie Waren verkaufen, bevor Sie den Kauf dieser Waren in Rechnung stellen. Dies wird als Kostenanpassung bezeichnet. Artikelkosten werden automatisch angepasst, wenn Sie Artikeltransaktionen buchen, Sie können jedoch auch Artikelpreise manuell anpassen. Weitere Informationen finden Sie unter [So geht's: Artikelkosten anpassen](inventory-how-adjust-item-costs.md).

|Aufgabe |Siehe |
|---|----|
|Erstellen Sie Artikelkarten für Lagerartikel, mit denen Sie handeln.|[Vorgehensweise: Neue Artikel registrieren](inventory-how-register-new-items.md)|
|Strukturieren Sie übergeordnete Artikel, die Sie als Sets verkaufen, die aus den Komponenten des übergeordneten Artikels bestehen oder für die Sie die Auftragsmontage oder das Lager haben.|[Vorgehensweise: Mit Stücklisten arbeiten](inventory-how-work-BOMs.md)|
|Aktualisert eine Übersicht über Artikel und erleichtert das Suchen und das Sortieren von Artikeln, indem diese in Kategorien organisiert werden.|[So geht's: Artikel kategorisieren](inventory-how-categorize-items.md)|
|Weisen Sie Ihren Artikeln Artikelattribute verschiedener Werttypen zu, um das Sortieren und Finden von Artikel zu erleichtern.|[Gewusst wie: Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)|
|Erstellen Sie spezielle Artikelkarten, die Sie Debitoren anbieten, für die Sie aber keinen Bestand verwalten.|[So geht's: Arbeiten mit Katalogartikeln](inventory-how-work-nonstock-items.md)|
|Beschreibt, wie eine physische Zählung ausgeführt wird, negative oder Zugängen gemacht werden und wie Informationen wie Lagerort oder Chargennummer in Artikelposten und Lagerplatzposten geändert werden.|[Vorgehensweise. Erfassen, Regulieren und Umbuchen von Lagerbestand](inventory-how-count-adjust-reclassify.md)|
|Zeigt die Verfügbarkeit der Artikel pro Lagerort, nach Periode, nach Verkaufs- oder Einkaufsereignis oder anhand ihrer Verwendung auf Produktionsstücklisten an.|[Vorgehensweise: Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)|
|Lagern Sie Artikel zwischen Lagerorten mit Umlagerungsaufträgen oder Artikel Umlag. Buch.-Blatt, um Lageraktivitäten zu verwalten.|[So geht's: Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)|
|Reservieren Sie Lager oder eingehenden Artikel für Verkaufsaufträge, Bestellungen, Serviceaufträge, Montageaufträge oder Fertigungsaufträge.|[Vorgehensweise: Artikel reservieren](inventory-how-to-reserve-items.md)|
|Serien- oder Chargennummern zu den einzelnen ausgehenden oder eingehende Belege oder Buch.-Blattzeile, beispielsweise um Artikel im Fall von Rückrufen nachzuverfolgen.|[Vorgehensweise: Arbeiten mit Chargennummern und Seriennummern](inventory-how-work-item-tracking.md)|
|Suchen Sie, wo eine Serien- oder Chargennummer in der gesamten Lieferkette verwendet wurde, z. B. in Rückrufsituationen.|[Vorgehensweise: Verfolgen von Artikeln mit Artikelverfolgung](inventory-how-to-trace-item-tracked-items.md)|
|Verwalten von Geschäften in den Verkaufsbüros, in den Einkaufsabteilungen oder in den Fabrikplanungsbüros von mehreren Standorten.|[So geht's: Mit Zuständigkeitseinheiten arbeiten](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)    
[Arbeiten mit [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

