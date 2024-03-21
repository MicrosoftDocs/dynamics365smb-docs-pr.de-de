---
title: 'GDPdU Filter Beispiele [DE]'
description: 'Das folgende Thema enthält Beispiele, wie Sie unterschiedliche Filtertypen verwenden und kombinieren können, wenn Sie Ihre GPDdU-Exporte einrichten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '11002, 11003, 11004, 11007, 11008, 11009, 11014, 11026, 11027'
ms.date: 06/18/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="gdpdu-filter-examples-in-the-german-version"></a>GDPdU-Filter-Beispiele in der deutschen Version

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

Exportergebnisse:

- Sachposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.  
- Debitorenposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.  

### <a name="table-filter"></a>Tabellenfilter

In diesem Beispiel geben Sie, zusätzlich zu „Periodenfeldnr.“-Informationen auch einen Tabellenfilter an. Dies ist hilfreich, wenn Sie nicht nur ein Start- und Enddatum für Ihren Export einbeziehen möchten, sondern auch einen zusätzlichen Filter, um weitere Kriterien anzugeben, wie beispielsweise Beträge.  

|Tabellennr.|Tabellenname|Periodenfeldnr.|Periodenfeldname|Tabellenfilter|  
|---------------|----------------|----------------------|-----------------------|------------------|  
|17|Fibubuchung|4|Buchungsdatum||  
|21|Debitorenposten|||Debitorenposten: **Buchungsdatum=..31-12-13**|  

Exportergebnisse:

- Sachposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013.  
- Debitorenposten mit Buchungsdatum vor 01.01.2014.  

### <a name="date-filter-field-no-and-date-filter-handling"></a>Datumsfilter-Feldnummer und Behandlung von Datumsfiltern

Im folgenden Beispiel wird die Einstellung von Datumstyp-FlowFilters veranschaulicht. Wenn eine Tabelle mehr als einen Datums-FlowFilter hat, können Sie keinen zur Benutzung angeben, aber Sie können angeben, wie der Datumsfilter behandelt werden soll.  

|Tabellennr.|Tabellenname|Periodenfeldnr.|Periodenfeldname|Tabellenfilter|Behandlung von Datumsfiltern|  
|---------------|----------------|----------------------|-----------------------|------------------|--------------------------|  
|18|Debitor|||Debitor: **Bewegung (MW)**=<>0|**Periode**|  
|21|Debitorenposten|4|Buchungsdatum|Debitorenposten: **Restbetrag (MW)**=<>0|**Nur Enddatum**|  

Exportergebnisse:

- Debitoren, die eine Bewegung (MW) <> 0 in die Periode von 01.01.2013 bis 31.12.2013 haben.  
- Debitorenposten mit Buchungsdatum zwischen 01.01.2013 und 31.12.2013, die einen Restbetrag (MW) <> 0 am 31.12.2013 haben.  

### <a name="date-filter-handling-for-the-same-table"></a>Datumsfilterbehandlung für dieselbe Tabelle

In diesem Beispiel legen Sie mehrere Filterdefinitionen für dieselbe Tabelle fest.  

|Tabellennr.|Tabellenname|Tabellenfilter|Behandlung von Datumsfiltern|  
|---------------|----------------|------------------|--------------------------|  
|18|Debitor|Debitor: **Bewegung (MW)**=<>0|**Periode**|  
|18|Debitor|Debitor: **Bewegung (MW)**=<>0|**Nur Startdatum**|  

Exportergebnisse:

- Debitoren, die eine Bewegung (MW) <> 0 in der Periode vom 01.01.2013 bis 31.12.2013 haben.  
- Debitoren, die Bewegung (MW) <> 0 am Tag vor dem Startdatum versehen haben.  

## <a name="see-also"></a>Siehe auch

[Daten für eine digitale Prüfung (GoBD/GDPdU) einrichten](how-to-set-up-data-exports-for-digital-audits.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
