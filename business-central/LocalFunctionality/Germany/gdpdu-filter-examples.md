---
title: GDPdU-Filterbeispiele
description: Das folgende Thema enthält Beispiele, wie Sie unterschiedliche Filtertypen verwenden und kombinieren können, wenn Sie Ihre GPDdU-Exporte einrichten. Wenn Sie Filter passend einsetzen, können Sie die Leistung verbessern.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b22d9315453133de4b77f2fe00209bc188cabce3
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778618"
---
# <a name="gdpdu-filter-examples"></a>GDPdU-Filterbeispiele
Das folgende Thema enthält Beispiele, wie Sie unterschiedliche Filtertypen verwenden und kombinieren können, wenn Sie Ihre GPDdU-Exporte einrichten. Wenn Sie Filter passend einsetzen, können Sie die Leistung verbessern.  

In den folgenden Beispielen werden für Daten die Tabellen für Sachposten und Debitorenposten verwendet. Sie gehen davon aus, dass Sie das nächste Datum in der Stapelverarbeitung **Geschäftsdaten exportieren** angegeben haben.  

Startdatum = 01.01.2013  

Enddatum = 31.12.2013  

## <a name="setting-up-export-record-source-examples"></a>Einrichten von Beispielen für Datensatzquellen für den Export  

### <a name="period-field-no"></a>Periodenfeldnr.  
Auf der Seite **Datenexport – Datensatzherkunft** erfolgt die Einrichtung wie in folgender Tabelle beschrieben.  

|Tabellennr.|Tabellenname|Periodenfeldnr.|Periodenfeldname|Tabellenfilter|  
|---------------|----------------|----------------------|-----------------------|------------------|  
|17|Fibubuchung|4|Buchungsdatum|Kein Filter festgelegt.|  
|21|Debitorenposten|4|Buchungsdatum|Kein Filter festgelegt.|  

**Ergebnisse exportieren**  

- Sachposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.  
- Debitorenposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.  

### <a name="table-filter"></a>Tabellenfilter  
In diesem Beispiel geben Sie, zusätzlich zu „Periodenfeldnr.“-Informationen auch einen Tabellenfilter an. Dies ist hilfreich, wenn Sie nicht nur ein Start- und Enddatum für Ihren Export einbeziehen möchten, sondern auch einen zusätzlichen Filter, um weitere Kriterien anzugeben, wie beispielsweise Beträge.  

|Tabellennr.|Tabellenname|Periodenfeldnr.|Periodenfeldname|Tabellenfilter|  
|---------------|----------------|----------------------|-----------------------|------------------|  
|17|Fibubuchung|4|Buchungsdatum||  
|21|Debitorenposten|||Debitorenposten: **Buchungsdatum=..31-12-13**|  

**Ergebnisse exportieren**  

- Sachposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.  
- Debitorenposten mit Buchungsdatum vor 01.01.2014.  

### <a name="date-filter-field-no-and-date-filter-handling"></a>Datumsfilter-Feldnummer und Behandlung von Datumsfiltern  
Im folgenden Beispiel wird die Einstellung von Datumstyp-FlowFilters veranschaulicht. Wenn eine Tabelle mehr als einen Datums-FlowFilter hat, können Sie keinen zur Benutzung angeben, aber Sie können angeben, wie der Datumsfilter behandelt werden soll.  

|Tabellennr.|Tabellenname|Periodenfeldnr.|Periodenfeldname|Tabellenfilter|Behandlung von Datumsfiltern|  
|---------------|----------------|----------------------|-----------------------|------------------|--------------------------|  
|18|Debitor|||Debitor: **Bewegung (MW)**=<>0|**Periode**|  
|21|Debitorenposten|4|Buchungsdatum|Debitorenposten: **Restbetrag (MW)**=<>0|**Nur Enddatum**|  

**Ergebnisse exportieren**  

- Debitoren, die eine Bewegung (MW) <> 0 in die Periode von 01.01.2013 bis 31.12.2013 haben.  
- Debitorenposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013, die einen Restbetrag (MW) <> 0 am 31.12.2013 haben.  

### <a name="date-filter-handling-for-the-same-table"></a>Datumsfilterbehandlung für dieselbe Tabelle  
In diesem Beispiel legen Sie mehrere Filterdefinitionen für dieselbe Tabelle fest.  

|Tabellennr.|Tabellenname|Tabellenfilter|Behandlung von Datumsfiltern|  
|---------------|----------------|------------------|--------------------------|  
|18|Debitor|Debitor: **Bewegung (MW)**=<>0|**Periode**|  
|18|Debitor|Debitor: **Bewegung (MW)**=<>0|**Nur Startdatum**|  

**Ergebnisse exportieren**  

- Debitoren, die eine Bewegung (MW) <> 0 in die Periode von 01.01.2013 bis 31.12.2013 haben.  
- Debitoren, die Bewegung (MW) <> 0 am Tag vor dem Startdatum versehen haben.  

## <a name="see-also"></a>Siehe auch  
 [Gewusst wie: Einrichten von Datenexporten für GDPdU](how-to-set-up-data-exports-for-gdpdu.md)
