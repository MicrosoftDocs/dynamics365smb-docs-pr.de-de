---
title: Bestands- und Lagerberichte und Analysen
description: Sehen Sie, welche Bestands- und Lagerberichte und Analysen in der Standardversion von Business Central verfügbar sind, damit Sie Ihr Unternehmen im Auge behalten können.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 8a4418699f28acd3ede80616ba69c56f50781e43
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216362"
---
# <a name="inventory-and-warehouse-reports-and-analytics-in-business-central"></a>Bestands- und Lagerberichte und Analysen in Business Central

Die Bestands- und Lagerberichterstattung in [!INCLUDE [prod_short](includes/prod_short.md)] ermöglicht es Bestands- und Geschäftsfachleuten, Einblicke und Statistiken über aktuelle und vergangene Bestands- und Lageraktivitäten zu erhalten.  

## <a name="reports"></a>Berichte

In der folgenden Tabelle werden einige der wichtigsten Berichte in der Bestands- und Lagerberichterstattung beschrieben.

|Bericht |Objekt-ID|Beschreibung  |
|---------|---------|---------|
|**Gebuchte Lagereinlagerungen**|707|Wenn Sie sich einen Überblick über bestimmte Artikel/Lagermengeneinheiten und deren Verfügbarkeit verschaffen möchten. Dieser Bericht zeigt Ihnen kumulierte Werte wie Bruttobedarf, geplante und zeitlich geplante Zugänge , den Bestand usw. an. |
|**Lagerwert ermitteln**|1001|Zeigt den Lagerwert ausgewählter Artikel in Ihrem Lager an. Der Bericht zeigt auch Informationen über den Wert der Lagerzu- und -abgänge in einer ausgewählten Periode.|
|**Artikelablauf - Menge**|5809|Gibt einen Überblick darüber, in welchen Mengen die ausgewählten Artikel, deren Ablaufdaten in eine bestimmte Periode fallen, im Lagerbestand vorhanden sind. Die Liste zeigt, wie viele Einheiten des ausgewählten Artikels, der in der angegebenen Periode abläuft, vorhanden sind. Für jeden Artikel, den Sie beim Einrichten des Berichts angegeben haben, zeigt der Bericht die Anzahl der Einheiten, die innerhalb jeder von drei gleichlangen Perioden ablaufen, sowie die gesamte Lagerbestandsmenge des ausgewählten Artikels.<br>Durch Festlegen von Filtern kann angegeben werden, was im Bericht enthalten ist. Wenn keine Filter festgelegt werden, enthält der Bericht alle Datensätze. Die Mengen im Bericht sind ausschließlich Mengen des Artikels, für die Ablaufdaten definiert wurden.|
|**Artikellagerzeit - Menge** oder **Artikellagerzeit - Wert**|5807 oder 5808|Gibt Ihnen einen Überblick über die aktuelle Lagerzeit von ausgewählten Artikeln in Ihrem Lagerbestand. Die Liste zeigt die Anzahl von Einheiten oder den Wert der ausgewählten Artikel, die zum Lager hinzugefügt oder aus dem Lager entnommen wurden, sowie den Zeitpunkt der Lagerbewegung. Artikel können als Ergebnis von Einkäufen, Verkäufen sowie Zu- und Abgängen dem Lager hinzugefügt oder aus dem Lager entnommen werden.|
|**Lager EK-/VK-Preisliste**|716|Zeigt eine Liste mit Preisinformationen für die ausgewählten Artikel oder Lagerhaltungsdaten an: EK-Preis, letzte direkte Kosten, VK-Preis, Deckungsbeitrag in Prozent und Deckungsbeitrag. |
|**Lagerplatzübersicht**|7319|Zeigt eine Übersicht über Lagerplätze, deren Einrichtung und die Menge der Artikel in den Lagerplätzen an. Dieser Report kann für alle Standorte verwendet werden, die „Lagerplatz“ als Pflichtfeld haben. |
|**Warenausgangsstatus Lager**|7313|Zeigt für jeden Ort eine Übersicht der offenen Herkunftsbelege mit den gelieferten Artikeln oder für die Lieferung fälligen Artikeln an. Dieser Bericht kann für alle Standorte verwendet werden, an denen das Feld **Erforderliche Lieferungen** ausgewählt ist. **Warenausgangsstatus Lager** zeigt Standorte, Lagerplatzcodes, Belegstatus und Mengen an.|
|**Lager - Kommissionierliste**|813|Zeigt eine Liste der Verkaufsaufträge an, in denen ein Artikel enthalten ist. Die folgenden Informationen werden für jeden Artikel angezeigt: Verkaufsauftragszeile mit Namen des Debitors, Variantencode, Lagerortcode, Lagerplatzcode, Warenausgangsdatum, Menge zu liefern und Einheit. Die zu liefernde Menge wird für jeden Artikel aufsummiert. Der Bericht kann verwendet werden, wenn Artikel aus dem Lager entnommen werden sollen.<br>HINWEIS: Diese Funktion ist für erweiterte Lagerfunktionen nicht verfügbar.|
|**Ausgleichslagerplatz**|7320|Dieser Sonderbericht ist nur für ein erweitertes Lager vorgesehen und zeigt die Restmengen an, die noch am Ausgleichsplatz selbst gelagert sind. Normalerweise sollte dieser spezielle Lagerplatz leer sein. Der einzige Grund, aus dem dieser Lagerplatz gefüllt wird, ist das Ergebnis eines physischen Zählungsprozesses oder wenn Mengen von Artikeln entfernt oder dem Lager hinzugefügt wurden.|


## <a name="tasks"></a>Aufgaben

In den folgenden Artikeln werden einige der wichtigsten Aufgaben zur Analyse des Status Ihres Unternehmens beschrieben:

* [Analyseberichte erstellen](bi-how-create-analysis-views-reports.md)  
* [Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)


## <a name="see-also"></a>Siehe auch

[Bestand einrichten](inventory-setup-inventory.md)  
[Lagerbestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)  
[Logistik](warehouse-manage-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
