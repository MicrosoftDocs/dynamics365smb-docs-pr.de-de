---
title: Einkaufsberichte und Analysen
description: Sehen Sie, welche Einkaufsberichte und Analysen in der Standardversion von Business Central verfügbar sind, damit Sie Ihr Unternehmen im Auge behalten können.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 3f818e556b2ebe3f50189b0057f1302a5598d904
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543170"
---
# <a name="purchase-reports-and-analytics-in-business-central"></a>Einkaufsberichte und Analysen in Business Central

Die Einkaufsberichterstattung in [!INCLUDE [prod_short](includes/prod_short.md)] ermöglicht es Prokuristen und Experten, Einblicke in und Statistiken über aktuelle und vergangene Einkaufsaktivitäten zu erhalten.  

## <a name="reports"></a>Berichte

In der folgenden Tabelle werden einige der wichtigsten Berichte in der Einkaufsberichterstattung beschrieben.

|Bericht |Objekt-ID|Beschreibung  |
|---------|---------|---------|
|**Einkaufsstatistik**|312|[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]|
|**Kreditor – Top-10-Liste**|311|Zeigt Daten zu den Einkäufen und Salden von Kreditoren für einen ausgewählten Zeitraum an. Sie können die Anzahl der Kreditoren festlegen, die in den Bericht aufgenommen werden sollen.<br>Die Kreditoren werden nach Beträgen sortiert, und Sie können wählen, ob die Sortierung nach Einkaufsbeträgen oder nach Saldo erfolgen soll. Der Bericht verschafft Ihnen einen schnellen Überblick der Kreditoren, von denen Sie am meisten kaufen oder welchen Sie am meisten schulden.|
|**Kreditoren/Artikel Katalog** oder **Artikel/Lieferanten Katalog**|320 oder 720|Zeigt eine Liste der Kreditoren für die ausgewählten Artikel oder Artikel für ausgewählte Kreditoren an. Für jede Kombination von Artikel und Kreditor zeigt er den EK-Preis, die Durchlaufzeit und die Artikelnummer des Kreditors an.<br>In den USA, Kanada und Mexiko ist dieser Bericht nicht verfügbar. Verwenden Sie stattdessen die **Artikel-/Lieferantenkatalog** (10164) Bericht.|
|**Kreditor/Artikel Einkäufe**|313|Zeigt eine Übersicht der Artikelposten jedes Kreditors in der ausgewählten Periode an. Der Bericht enthält Angaben zur fakturierten Menge, zum Rechnungsbetrag und zu möglichen Rabatten. Der Bericht kann z. B. zur Analyse der Artikeleinkäufe verwendet werden, so dass Sie erfahren, ob es eine Beziehung zwischen Rabatten und Artikeleinkäufen gibt.|
|**Lager EK-/VK-Preisliste**|716|Zeigt eine Liste mit Preisinformationen für die ausgewählten Artikel oder Lagerhaltungsdaten an: EK-Preis, letzte direkte Kosten, VK-Preis, Deckungsbeitrag in Prozent und Deckungsbeitrag.|
|**Gebuchte Lagereinlagerungen**|707|Wenn Sie sich einen Überblick über bestimmte Artikel/Lagermengeneinheiten und deren Verfügbarkeit verschaffen möchten. Dieser Bericht zeigt Ihnen kumulierte Werte wie Bruttobedarf, geplante und zeitlich geplante Zugänge , den Bestand usw. an. |
|**Lager - Kreditoreneinkäufe**|714|Zeigt eine Liste der Kreditoren, von denen Ihr Unternehmen in der ausgewählten Periode Artikel gekauft hat. Er zeigt die fakturierte Menge, den Betrag und den Rabatt. Der Bericht kann dazu verwendet werden, die Einkäufe eines Unternehmens zu analysieren.|
|**Lager - Bestellungen**|709|Zeigt eine Liste von Artikeln, die sich in Bestellungen bei Kreditoren befinden. Er zeigt darüber hinaus das erwartete Wareneingangsdatum und die Menge und den Betrag im Rückstand an. Verwenden Sie den Bericht beispielsweise, um anzeigen, wann der Wareneingang von Artikeln erfolgen sollte und ob eine Mahnung aufgrund einer Menge in Rückstand ausgestellt werden sollte.|
|**Einkaufsreserv.-Verfügbarkeit**|409|Zeigt die Verfügbarkeit von zu liefernden Artikeln in Einkaufsbelegen (z. B. Reklamationen) an. Sie können festlegen, ob der Bericht den Status der Belege oder den der einzelnen Einkaufszeilen anzeigen soll. <br>Wenn Sie den Bericht drucken, können Sie auch die Menge, die zur Lieferung zur Verfügung steht, im Feld **Menge akt. Lieferung** in den Einkaufszeilen aktualisieren. In Zeilen der Einkaufsgutschriften oder negativen Mengen in Einkaufsbestellungen enthält das Feld **Menge akt. Lieferung** die zu liefernde Menge. Sie können den Bericht verwenden, um festzulegen, welche Belege geliefert werden sollen. **Hinweis**: Dieser Bericht ist für erweiterte Lagerfunktionen nicht verfügbar.|
<!--|**Kreditor – Fällige Posten**|11006| DACH-spezifisch: Ein Bericht, der vom Teamleiter Ihrer Einkaufsabteilung sowie der Buchhaltung verwendet werden kann. Hier erhalten Sie einen Überblick über die unbezahlten Kreditorenrechnungen einschließlich der Fälligkeitstermine, Währungen und Beträge. Die Grundlage bilden die offenen Kreditorenposten.| -->




## <a name="tasks"></a>Aufgaben

In den folgenden Artikeln werden einige der wichtigsten Aufgaben zur Analyse des Status Ihres Unternehmens beschrieben:

* [Analyseberichte erstellen](bi-how-create-analysis-views-reports.md)  
* [Artikelverfügbarkeit anzeigen](inventory-how-availability-overview.md)  


## <a name="see-also"></a>Siehe auch

[Einrichten des Einkaufs](purchasing-setup-purchasing.md)  
[Einkauf](purchasing-manage-purchasing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
