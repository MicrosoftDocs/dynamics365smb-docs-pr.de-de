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
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 920df314dc8b671d4e2d99d8449ee02a74cb9078
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017

---

# <a name="inventory"></a>Lagerbest
Für jedes physische Produkt, mit dem Sie handeln, müssen Sie eine Artikelkarte vom Typ **Lagerbestand** erstellen. Artikel, die Sie Debitoren anbieten, aber nicht im Lager führen, können als Katalogartikel erfassen werden und Sie können Sie bei Bedarf in Lagerartikel konvertieren. Sie können die Menge eines Artikels im Lager erhöhen oder vermindern, indem Sie direkt in den Artikelposten buchen, beispielsweise nach einer physischen Zählung oder falls keine erworbenen Mengen erfasst wurden.

Lagerzugänge und Abgänge werden natürlich auch erfasst, wenn Sie Einkaufs- und Verkaufsbelege buchen. Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md), [So gehts: Produkte verkaufen](sales-how-sell-products.md) und [So gehts: Fakturieren](sales-how-invoice-sales.md). Umlagerungen zwischen Lagerorten ändert Lagerbestandsmengen in den Lagern Ihres Mandanten.   

Um die Übersicht über Artikel zu erhöhen und die Suche zu erleichtern, können Sie Artikel kategorisieren und ihnen Attribute zuweisen, nach denen sie gesucht und sortiert werden können.

Sie möchten, dass die Kosten der Artikel an die zugehörigen ausgehenden Verkaufsvorgänge weitergeleitet werden, insbesondere in Fällen, in denen Sie Waren verkaufen, bevor der Kauf dieser Artikel fakturiert wird. Dies wird als Kostenregulierung bezeichnet. Sie können sie manuell ausführen oder sie so einrichten, dass sie automatisch erfolgt, wenn Sie eine Artikeltransaktion buchen.

## <a name="inventory-reconciliation"></a>Abstimmung des Lagerbestands
Wenn Sie Lagertransaktionen buchen, z. B. Verkaufslieferungen, Einkaufsrechnungen oder Lagerregulierungen, werden die veränderten Artikelkosten in den Artikelwerteinträgen aufgezeichnet. Um diese Änderung des Lagerwerts in Ihren Finanzbüchern wiederzugeben, werden die Lagerkosten automatisch zu den entsprechenden Lagerkonten in der Finanzbuchhaltung gebucht. Für jede Lagertransaktion, die Sie buchen, werden die entsprechenden Werte in der Hauptbuchhaltung im Lagerkonto, im Korrekturkonto und im Lagerverbrauchskonto gebucht.

Selbst wenn Lagerkosten automatisch in die Finanzbuchhaltung gebucht werden, ist es immer noch notwendig sicherzustellen, dass die Kosten für Waren zur zugehörigen ausgehenden Transaktion weitergeleitet werden, insbesondere in Situationen, in denen Sie Waren verkaufen, bevor Sie den Kauf dieser Waren in Rechnung stellen. Dies wird als Kostenanpassung bezeichnet. Artikelkosten werden automatisch angepasst, wenn Sie Artikeltransaktionen buchen, Sie können jedoch auch Artikelpreise manuell anpassen. Weitere Informationen finden Sie unter So geht's: Artikelkosten anpassen.

|An |Siehe |
|---|----|
|Erstellen Sie Artikelkarten für Lagerartikel, mit denen Sie handeln.|[Vorgehensweise: Einen neuen Artikel registrieren](inventory-how-register-new-items.md)|
|Strukturieren Sie übergeordnete Artikel, die Sie als Sets verkaufen, die aus den Komponenten des übergeordneten Artikels bestehen oder für die Sie die Auftragsmontage oder das Lager haben.|[Vorgehensweise: Arbeiten mit Stücklisten](inventory-how-work-BOMs.md)|
|Aktualisert eine Übersicht über Artikel und erleichtert das Suchen und das Sortieren von Artikeln, indem diese in Kategorien organisiert werden.|[So geht's: Artikel kategorisieren](inventory-how-categorize-items.md)|
|Weisen Sie Ihren Artikeln Artikelattribute verschiedener Werttypen zu, um das Sortieren und Finden von Artikel zu erleichtern.|[Gewusst wie: Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)|
|Erstellen Sie spezielle Artikelkarten, die Sie Debitoren anbieten, für die Sie aber keinen Bestand verwalten.|[So geht's: Arbeiten mit Katalogartikeln](inventory-how-work-nonstock-items.md)|
|Beschreibt, wie eine physische Zählung ausgeführt wird, negative oder Zugängen gemacht werden und wie Informationen wie Lagerort oder Chargennummer in Artikelposten und Lagerplatzposten geändert werden.|[Vorgehensweise. Erfassen, Regulieren und Umbuchen von Lagerbestand](inventory-how-count-adjust-reclassify.md)|
|Zeigt die Verfügbarkeit der Artikel pro Lagerort, nach Periode, nach Verkaufs- oder Einkaufsereignis oder anhand ihrer Verwendung auf Montagestücklisten an.|[Vorgehensweise: Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)|
|Lagern Sie Artikel zwischen Lagerorten mit Umlagerungsaufträgen oder Artikel Umlag. Buch.-Blatt, um Lageraktivitäten zu verwalten.|[So geht's: Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)|
|Schreiben sie den Wert eines oder mehrerer Artikel im Lager ab oder bewerten sie ihn neu, indem Sie den aktuellen, berechneten Wert buchen.|[Vorgehensweise: Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md)|
|Regulieren Sie Artikelkosten, entweder automatisch oder manuell, um Kostenänderungen aus eingehenden Posten an die entsprechenden ausgehenden Posten weiterzuleiten.|[Gewusst wie: Artikelpreise anpassen](inventory-how-adjust-item-costs.md)|

## <a name="see-also"></a>Siehe auch  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)    
[Lieferkette](madeira-supply-chain.md)  
[Arbeiten mit [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
