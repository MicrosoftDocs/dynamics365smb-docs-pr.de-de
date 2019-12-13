---
title: Designdetails - Tabellenstruktur | Microsoft Docs
description: Um zu erkennen, wie die Dimensionsposten-Einlagerungs- und Buchung neu entwickelt wurde, ist es wichtig, die Tabellenstruktur zu kennen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1f8067071f1c27baaab5a467fbf2751ffc7d3d2b
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880016"
---
# <a name="design-details-table-structure"></a>Designdetails: Tabellenstruktur
Um zu erkennen, wie die Dimensionsposten gespeichert und gebucht werden, ist es wichtig, die Tabellenstruktur zu kennen.  

## <a name="table-480-dimension-set-entry"></a>Tabelle 480, Dimensionssatzposten  
Sie können den Inhalt dieser Tabelle nicht ändern. Nachdem Daten in die Tabelle geschrieben wurden, können Sie sie nicht löschen oder bearbeiten.

|Feldnr.|Feldname|Datentyp|Bemerkung|  
|---------------|----------------|---------------|-------------|  
|1|**ID**|Ganzzahl|>0,0 wird für den leeren Dimensionssatz reserviert. Referenzfeld 3 in Tabelle 481.|  
|2|**Dimensionscode**|Code 20|Tabellenrelation zu Tabelle 348|  
|3|**Dimensionswertcode**|Code 20|Tabellenrelation zu Tabelle 349.|  
|4|**Dimensionswert-ID**|Ganzzahl|Referenzfeld 12 in Tabelle 349. Es ist der sekundäre Schlüssel, der verwendet wird, wenn die Tabelle 481 durchläuft.|  
|5|**Dimensionsname**|Text 30|CalcField. Lookup zu Tabelle 348.|  
|6|**Dimensionswertname**|Text 30|CalcField. Lookup zu Tabelle 349.|  

## <a name="table-481-dimension-set-tree-node"></a>Tabelle 481, Dimensionssatz-Strukturknoten  
Sie können den Inhalt dieser Tabelle nicht ändern. Sie wird verwendet, um nach einen Dimensionssatz zu suchen. Wenn der Dimensionssatz nicht gefunden wird, wird ein neuer Satz erstellt.  

|Feldnr.|Feldname|Datentyp|Bemerkung|  
|---------------|----------------|---------------|-------------|  
|1|**Übergeordnete Dimensionssatz-ID**|Ganzzahl|0 für Knoten der höchsten Ebene.|  
|2|**Dimensionswert-ID**|Ganzzahl|Tabellenrelation zu Feld 12 in Tabelle 349.|  
|3|**Dimensionssatz-ID**|Ganzzahl|AutoIncrement. Verwendet in Feld 1 in Tabelle 480.|  
|4|**In Benutzung**|Boolescher Wert|False, wenn nicht verwendet.|  

## <a name="table-482-reclas-dimension-set-buffer"></a>Tabelle 482 Umlag.-Dimensionssatzpuffer  
Diese Tabelle wird verwendet, wenn Sie einen Dimensionswertcode, beispielsweise zu einem Artikeleintrag ändern, indem Sie die Seite **Artikel Umlag. Buch.-Blatt** verwenden.  

|Feldnr.|Feldname|Datentyp|Bemerkung|  
|---------------|----------------|---------------|-------------|  
|1|**Dimensionscode**|Code 20|Tabellenrelation zu Tabelle 348|  
|2|**Dimensionswertcode**|Code 20|Tabellenrelation zu Tabelle 349.|  
|3|**Dimensionswert-ID**|Ganzzahl|Referenzfeld 12 in Tabelle 349.|  
|4|**Neuer Dimensionswertcode**|Code 20|Tabellenrelation zu Tabelle 349.|  
|5|**Neue Dimensionswert-ID**|Ganzzahl|Referenzfeld 12 in Tabelle 349.|  
|6|**Dimensionsname**|Text 30|CalcField. Lookup zu Tabelle 348.|  
|7|**Dimensionswertname**|Text 30|CalcField. Lookup zu Tabelle 349.|  
|8|**Neuer Dimensionswertname**|Text 30|CalcField. Lookup zu Tabelle 349.|  

## <a name="transaction-and-budget-tables"></a>Transaktions- und Budget-Tabellen  
Zusätzlich zu anderen Dimensionsfeldern in der Tabelle ist dieses Feld wichtig:  

|Feldnr.|Feldname|Datentyp|Bemerkung|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionssatz-ID**|Ganzzahl|Referenzfeld 1 in Tabelle 480.|  

### <a name="table-83-item-journal-line"></a>Tabelle 83, Artikel Buch.-Blattzeile  
Zusätzlich zu anderen Dimensionsfeldern in der Tabelle sind diese Felder wichtig.  

|Feldnr.|Feldname|Datentyp|Bemerkung|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensionssatz-ID**|Ganzzahl|Referenzfeld 1 in Tabelle 480.|  
|481|**Neue Dimensionssatz-ID**|Ganzzahl|Referenzfeld 1 in Tabelle 480.|  

### <a name="table-349-dimension-value"></a>Tabelle 349, Dimensionswert  
Zusätzlich zu anderen Dimensionsfeldern in der Tabelle sind diese Felder wichtig.  

|Feldnr.|Feldname|Datentyp|Bemerkung|  
|---------------|----------------|---------------|-------------|  
|12|**Dimensionswert-ID**|Ganzzahl|AutoIncrement. Verwendet als Referenzen in Tabelle 480 und in Tabelle 481.|  

### <a name="tables-that-contain-the-dimension-set-id-field"></a>Tabellen, die Dimensionssatz-ID-Feld enthalten
 Das Feld **Dimensionssatz-ID** (480) ist in den folgenden Tabellen vorhanden. Für die Tabellen, die gebuchte Daten speichern, bietet das Feld nur eine nicht-bearbeitbare Anzeige von Dimensionen, die als DrillDown markiert ist. Für die Tabellen, die Arbeitsdokumente speichern, ist das Feld editierbar. Die Puffertabellen, die intern verwendet werden, benötigen keine bearbeitbaren oder nicht-bearbeitbaren Funktionen.  

 Feld 480 ist in den folgenden Tabellen nicht editierbar.  

|Tabellennr.|Tabellenname|  
|---------------|----------------|  
|17|**Fibubuchung**|  
|21|**Debitorenposten**|  
|25|**Kreditorenposten**|  
|32|**Artikelposten**|  
|110|**Verkaufslieferkopf**|  
|111|**Verkaufslieferzeile**|  
|112|**Verkaufsrechnungskopf**|  
|113|**Verkaufsrechnungszeile**|  
|114|**Verkaufsgutschriftskopf**|  
|115|**Verkaufsgutschriftszeile**|  
|120|**Einkaufslieferkopf**|  
|121|**Einkaufslieferzeile**|  
|122|**Einkaufsrechnungskopf**|  
|123|**Einkaufsrechnungszeile**|  
|124|**Einkaufsgutschriftskopf**|  
|125|**Einkaufsgutschriftszeile**|  
|169|**Projektposten**|  
|203|**Ressourcenposten**|  
|271|**Bankposten**|  
|281|**Inventurposten**|  
|297|**Registrierter Mahnungskopf**|  
|304|**Reg. Zinsrechnungskopf**|  
|5107|**Verkaufskopfarchiv**|  
|5108|**Verkaufszeilenarchiv**|  
|5109|**Einkaufskopfarchiv**|  
|5110|**Einkaufszeilenarchiv**|  
|5601|**Anlagenposten**|  
|5625|**Wartungsposten**|  
|5629|**Versicherungsposten**|  
|5744|**Umlagerungsausgangskopf**|  
|5745|**Umlagerungsausgangszeile**|  
|5746|**Umlagerungseingangskopf**|  
|5747|**Umlagerungeingangszeile**|  
|5802|**Wertposten**|  
|5832|**Kapazitätsposten**|  
|5907|**Serviceposten**|  
|5908|**Servicekopf**|  
|5933|**Serviceauftragsbuchungspuffer**|  
|5970|**Archiv. Servicevertragskopf**|  
|5990|**Servicelieferungskopf**|  
|5991|**Servicelieferungszeile**|  
|5992|**Servicerechnungskopf**|  
|5993|**Servicerechnungszeile**|  
|5994|**Servicegutschriftskopf**|  
|5995|**Servicegutschriftszeile**|  
|6650|**Rücklieferkopf**|  
|6651|**Rücklieferzeile**|  
|6660|**Rücksendungskopf**|  
|6661|**Rücksendungszeile**|  

Feld 480 ist in den folgenden Tabellen editierbar.  

|Tabellennr.|Tabellenname|  
|---------------|----------------|  
|36|**Verkaufskopf**|  
|37|**Verkauf**|  
|38|**Einkaufskopf**|  
|39|**Einkauf**|  
|81|**Fibu Buch.-Blattzeile**|  
|83|**Artikel Buch.-Blattzeile**|  
|89|**Stücklisten-Blattzeile**|  
|96|**Finanzbudgetposten**|  
|207|**Res. Buch.-Blattzeile**|  
|210|**Projekt Buch.-Blattzeile**|  
|221|**Fibu Buch.-Blatt Verteilungen**|  
|246|**Bestellvorschlagszeile**|  
|295|**Mahnungskopf**|  
|302|**Zinsrechnungskopf**|  
|5405|**Fertigungsauftrag**|  
|5406|**FA-Zeile**|  
|5407|**FA-Komponente**|  
|5615|**Anlagenverteilungen**|  
|5621|**Anlagen Buch.-Blattzeile**|  
|5635|**Vers. Buch.-Blattzeile**|  
|5740|**Umlagerungskopf**|  
|5741|**Umlagerungszeile**|  
|5900|**Servicekopf**|  
|5901|**Serviceartikelzeile**|  
|5902|**Servicezeile**|  
|5965|**Servicevertragskopf**|  
|5997|**Standardservicezeile**|  
|7134|**Artikelbudgetposten**|  
|99000829|**Planungskomponente**|  

Feld 480 ist in den folgenden Puffertabellen vorhanden.  

|Tabellennr.|Tabellenname|  
|---------------|----------------|  
|49|**Rechnungsbuchungspuffer**|  
|212|**Projektregulierungspuffer**|  
|372|**Zahlungspuffer**|  
|382|**Deb.-/Kred.-Postenpuffer**|  
|461|**Zeilenpuffer Vorauszahlungsrechnung**|  
|5637|**Anlagen Fibu-Buchungspuffer**|  
|7136|**Artikelbudgetpuffer**|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Dimensionssatzposten](design-details-dimension-set-entries.md)   
 [Dimensionssatz-Eintrags-Übersicht](design-details-dimension-set-entries-overview.md)   
 [Designdetails: Suche nach Dimensionskombinationen](design-details-searching-for-dimension-combinations.md)   
 
