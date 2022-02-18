---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ae96e5a3fc1cc7f4b17e5ef208650248cbe0b3c2
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104161"
---
In der folgenden Tabelle werden einige der wichtigsten Berichte in der Einkaufsberichterstattung beschrieben.

|Bericht |Objekt-ID|Beschreibung  |
|---------|---------|---------|
|**Einkaufsstatistik**|312|[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]|
|**Kreditor – Top-10-Liste**|311|Zeigt Daten zu den Einkäufen und Salden von Kreditoren für einen ausgewählten Zeitraum an. Sie können die Anzahl der Kreditoren festlegen, die in den Bericht aufgenommen werden sollen.<br>Die Kreditoren werden nach Beträgen sortiert, und Sie können wählen, ob die Sortierung nach Einkaufsbeträgen oder nach Saldo erfolgen soll. Der Bericht verschafft Ihnen einen schnellen Überblick der Kreditoren, von denen Sie am meisten kaufen oder welchen Sie am meisten schulden.|
|**Kreditoren/Artikel Katalog** oder **Artikel/Lieferanten Katalog**|320 oder 720|Zeigt eine Liste der Kreditoren für die ausgewählten Artikel oder Artikel für ausgewählte Kreditoren an. Für jede Kombination von Artikel und Kreditor zeigt er den EK-Preis, die Durchlaufzeit und die Artikelnummer des Kreditors an.<br>In den USA, Kanada und Mexiko ist dieser Bericht nicht verfügbar. Verwenden Sie stattdessen die **Artikel-/Lieferantenkatalog** (10164) Bericht.|
|**Kreditor/Artikel Einkäufe**|313|Zeigt eine Übersicht der Artikelposten jedes Kreditors in der ausgewählten Periode an. Der Bericht enthält Angaben zur fakturierten Menge, zum Rechnungsbetrag und zu möglichen Rabatten. Der Bericht kann z. B. zur Analyse der Artikeleinkäufe verwendet werden, so dass Sie erfahren, ob es eine Beziehung zwischen Rabatten und Artikeleinkäufen gibt.|
|**Lager EK-/VK-Preisliste**|716|Zeigt eine Liste mit Preisinformationen für die ausgewählten Artikel oder Lagerhaltungsdaten an: EK-Preis, letzte direkte Kosten, VK-Preis, Deckungsbeitrag in Prozent und Deckungsbeitrag.|
|**Gebuchte Lagereinlagerungen**|707|Wenn Sie sich einen Überblick über bestimmte Artikel/Lagermengeneinheiten und deren Verfügbarkeit verschaffen möchten. Dieser Bericht zeigt Ihnen kumulierte Werte wie Bruttobedarf, geplante und zeitlich geplante Zugänge , den Bestand usw. an. |
|**Lager - Kreditoreneinkäufe**|714|Zeigt eine Liste der Kreditoren, von denen Ihr Unternehmen in der ausgewählten Periode Artikel gekauft hat. Er zeigt die fakturierte Menge, den Betrag und den Rabatt. Der Bericht kann dazu verwendet werden, die Einkäufe eines Unternehmens zu analysieren.|
|**Lager - Bestellungen**|709|Zeigt eine Liste von Artikeln, die sich in Bestellungen bei Kreditoren befinden. Er zeigt darüber hinaus das erwartete Wareneingangsdatum und die Menge und den Betrag im Rückstand an. Verwenden Sie den Bericht beispielsweise, um anzeigen, wann der Wareneingang von Artikeln erfolgen sollte und ob eine Mahnung aufgrund einer Menge in Rückstand ausgestellt werden sollte.|
|**Einkaufsreserv.-Verfügbarkeit**|409|Zeigt die Verfügbarkeit von zu liefernden Artikeln in Einkaufsbelegen (z. B. Reklamationen) an. Sie können festlegen, ob der Bericht den Status der Belege oder den der einzelnen Einkaufszeilen anzeigen soll. <br>Wenn Sie den Bericht drucken, können Sie auch die Menge, die zur Lieferung zur Verfügung steht, im Feld **Menge akt. Lieferung** in den Einkaufszeilen aktualisieren. In Zeilen der Einkaufsgutschriften oder negativen Mengen in Einkaufsbestellungen enthält das Feld **Menge akt. Lieferung** die zu liefernde Menge. Sie können den Bericht verwenden, um festzulegen, welche Belege geliefert werden sollen. **Hinweis**: Dieser Bericht ist für erweiterte Lagerfunktionen nicht verfügbar.|
<!--|**Kreditor – Fällige Posten**|11006| DACH-spezifisch: Ein Bericht, der vom Teamleiter Ihrer Einkaufsabteilung sowie der Buchhaltung verwendet werden kann. Hier erhalten Sie einen Überblick über die unbezahlten Kreditorenrechnungen einschließlich der Fälligkeitstermine, Währungen und Beträge. Die Grundlage bilden die offenen Kreditorenposten.| -->

