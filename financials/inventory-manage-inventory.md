---
title: Bestand | Microsoft Docs
description: Beschreibt, wie mit physische Artikel verwaltet werden.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b53cae82cfa532fb0620cc9e1f305216c2321785
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017

---

# <a name="inventory"></a>Lagerbest
Für jedes physische Produkt, mit dem Sie handeln, müssen Sie eine Artikelkarte vom Typ **Lagerbestand** erstellen. Artikel, die Sie Debitoren anbieten, aber nicht im Lager führen, können als Katalogartikel erfassen werden und Sie können Sie bei Bedarf in Lagerartikel konvertieren. Sie können die Menge eines Artikels im Lager erhöhen oder vermindern, indem Sie direkt in den Artikelposten buchen, beispielsweise nach einer physischen Zählung oder falls keine erworbenen Mengen erfasst wurden.

Lagerzugänge und Abgänge werden natürlich auch erfasst, wenn Sie Einkaufs- und Verkaufsbelege buchen. Weitere Informationen finden Sie unter [So gehts: Erfassen eines Einkaufs](purchasing-how-record-purchases.md), [So gehts: Produkte verkaufen](sales-how-sell-products.md) und [So gehts: Fakturieren](sales-how-invoice-sales.md). Umlagerungen zwischen Lagerorten ändert Lagerbestandsmengen in den Lagern Ihres Mandanten.   

Um die Übersicht über Artikel zu erhöhen und die Suche zu erleichtern, können Sie Artikel kategorisieren und ihnen Attribute zuweisen, nach denen sie gesucht und sortiert werden können.

Sie möchten, dass die Kosten der Artikel an die zugehörigen ausgehenden Verkaufsvorgänge weitergeleitet werden, insbesondere in Fällen, in denen Sie Waren verkaufen, bevor der Kauf dieser Artikel fakturiert wird. Dies wird als Kostenregulierung bezeichnet. Sie können sie manuell ausführen oder sie so einrichten, dass sie automatisch erfolgt, wenn Sie eine Artikeltransaktion buchen.

Änderungen im Lagerwert vom Handel werden automatisch mit den Finanzbüchern Artikeltransaktionen ausgeglichen, wenn Sie buchen.

|Aufgabe |Siehe |
|---|----|
|Erstellen Sie Artikelkarten für Lagerartikel, mit denen Sie handeln.|[Vorgehensweise: Einen neuen Artikel registrieren](inventory-how-register-new-items.md)|
|Strukturieren Sie übergeordnete Artikel, die Sie als Sets verkaufen, die aus den Komponenten des übergeordneten Artikels bestehen oder für die Sie die Auftragsmontage oder das Lager haben.|[Vorgehensweise: Arbeiten mit Stücklisten](inventory-how-work-BOMs.md)|
|Aktualisert eine Übersicht über Artikel und erleichtert das Suchen und das Sortieren von Artikeln, indem diese in Kategorien organisiert werden.|[So geht's: Artikel kategorisieren](inventory-how-categorize-items.md)|
|Weisen Sie Ihren Artikeln Artikelattribute verschiedener Werttypen zu, um das Sortieren und Finden von Artikel zu erleichtern.|[Gewusst wie: Arbeiten mit Artikelattributen](inventory-how-work-item-attributes.md)|
|Erstellen Sie spezielle Artikelkarten, die Sie Debitoren anbieten, für die Sie aber keinen Bestand verwalten.|[So geht's: Arbeiten mit Katalogartikeln](inventory-how-work-nonstock-items.md)|
|Erhöhen oder Vermindern des Lagerbestands eines Artikels, etwa nach einer Inventur oder als einfaches Mittel zur Aufzeichnung von Einkaufsbelegen.|[Vorgehensweise: Anpassen des Bestands](inventory-how-adjust-inventory.md)|
|Zeigt die Verfügbarkeit der Artikel pro Lagerort, nach Periode, nach Verkaufs- oder Einkaufsereignis oder anhand ihrer Verwendung auf Montagestücklisten an.|[Vorgehensweise: Verschaffen Sie sich einen Überblick über die Verfügbarkeit](inventory-how-availability-overview.md)|
|Lagern Sie Artikel zwischen Lagerorten mit Umlagerungsaufträgen oder Artikel Umlag. Buch.-Blatt, um Lageraktivitäten zu verwalten.|[So geht's: Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)|
|Schreiben sie den Wert eines oder mehrerer Artikel im Lager ab oder bewerten sie ihn neu, indem Sie den aktuellen, berechneten Wert buchen.|[Vorgehensweise: Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md)|
|Regulieren Sie Artikelkosten, entweder automatisch oder manuell, um Kostenänderungen aus eingehenden Posten an die entsprechenden ausgehenden Posten weiterzuleiten.|[Gewusst wie: Artikelpreise anpassen](inventory-how-adjust-item-costs.md)|
|Erfahren, wie Änderungen im Lagerwert vom Handel automatisch mit den Finanzbüchern ausgeglichen werden.|[Erweitert: Bestandabgleich](advanced-inventory-reconciliation.md)|

## <a name="see-also"></a>Siehe auch  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)    
[Lieferkette](madeira-supply-chain.md)  
[Arbeitend mit [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md]  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
