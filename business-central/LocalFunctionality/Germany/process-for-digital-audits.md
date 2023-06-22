---
title: Digital-Überwachung (/GoBD GDPdU)
description: 'Sie können Finanz- und Steuerdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '11002, 11003, 11004, 11007, 11008, 11009, 11014, 11026, 11027'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="process-for-digital-audits-gobdgdpdu" />Prozess für Digital-Überwachung (/GoBD GDPdU)
Sie können Daten aus [!INCLUDE[prod_short](../../includes/prod_short.md)] exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert.  

## <a name="overview" />Matrix
Nach §146 und 147 des deutschen Steuercodes (Abgabenordnung, AO) ist es der Finanzverwaltung möglich, die Daten von elektronischen Buchführungssystemen „digital“ zu prüfen. Sie können dies über ein Datenspeichergerät oder direkt oder indirekt über Zugriff auf das System tun. Für die Datenträgerüberlassung ist es notwendig, dass die Daten vom steuerpflichtigen Unternehmen (oder dem beauftragten Steuerberater, buchführenden (Sub-)Unternehmen, etc.) in „maschinell auswertbarer Form“ auf geeigneten Datenträgern bereitgestellt werden. Unter dem Begriff „maschineller Auswertbarkeit“ versteht die Finanzverwaltung den wahlfreien Zugriff auf alle gespeicherten Daten einschließlich der Stammdaten und Verknüpfungen mit Sortier- und Filterfunktionen. Um eine solche Auswertbarkeit oder Verwertbarkeit zu erreichen, ist es notwendig, dass die Dateiformate für die Datenträgerüberlassung definiert und standardisiert werden.  

Steuerbehörden in Deutschland verwenden Analysesoftware mit der Bezeichnung IDEA, mit der Daten aus ASCII-Dateien importiert werden. Die IDEA-Software kann Daten mit festem oder variablem Längenformat importieren. Dazu wird eine XML-Datei, index.xml benötigt, die die Struktur der Datendateien beschreibt. Weitere Informationen finden Sie unter [Audicon-Website für GDPdU](https://go.microsoft.com/fwlink/?LinkId=245841).  

## <a name="defining-gdpdu-export-data" />Gewusst wie: Exportieren von GDPdU-Daten
Sie können [!INCLUDE[prod_short](../../includes/prod_short.md)] konfigurieren, ums GDPdU-Daten zu exportieren, um Ihren Anforderungen zu entsprechen. Sie können große Datenbestände exportieren, und kleine Datenbestände exportieren. Sie können Daten aus einer einzelnen Tabelle oder aus einer Tabelle und den verknüpften Tabellen exportieren.  

Für jeden Datenexport definieren Sie die Tabellen und Felder, die Sie exportieren möchten. Dies hängt von den Anforderungen des Steuerprüfers ab. Die ausgewählten Daten werden in die ASCII-Dateien exportiert. Eine entsprechende XML-Datei, INDEX.XML, wird ebenfalls erstellt, um die ASCII-Datei-Struktur zu beschreiben.  

Die Elemente in der INDEX.XML-Datei definieren die Namen der Tabellen und die Felder, die exportiert werden. Da das aktuelle Überwachungstool Einschränkungen auf diesen Feldnamen, wie der Länge und die Zeichen hat, die verwendet werden, entfernt [!INCLUDE[prod_short](../../includes/prod_short.md)] Leerzeichen und Sonderzeichen und schneidet dann die Namen, um die Beschränkung mit 20 Zeichen zu finden. Sie können die vorgeschlagenen Tabellen- und Feldnamen ändern, wenn Sie einer Tabellendefinition Felder hinzufügen.  

In den meisten Fällen richten Sie den GDPdU-Datenexport einmal ein, und dann kann eine Person in Ihrem Unternehmen den Export ausführen, wenn der Steuerprüfer neue Daten anfordert. Es wird empfohlen, dass die Einrichtung nicht nur von Personen mit einem Verständnis der Datenbankstruktur und der technischen Hardware in Ihrem Unternehmen durchgeführt wird, sondern auch gemeinsam mit Personen, die die Geschäftsdaten verstehen, wie der Buchhalter.  

## <a name="configuration" />Konfiguration
Sie können verschiedene GDPdU-Datenexporte abhängig vom Datentyp einrichten, der exportiert werden soll. Beispielsweise können Sie zwei GDPdU-Datenexporte erstellen:  

- Einer exportiert allgemeine Informationen über alle Sachposten, Debitorenposten, Kreditorenposten und MwSt.-Posten.  
- Der andere exportiert detaillierte Informationen über die Sachposten.  

> [!NOTE]  
>  Wie Sie die GDPdU-Datenexporte einrichten müssen, hängt von den Anforderungen des Mandanten und von den Anforderungen des Wirtschaftsprüfers ab.  

Als Beispiel, wie Einrichtungsdatenexporten für GDPdU eingerichtet werden, siehe. [Exemplarische Vorgehensweise: Exportieren von GDPdU-Daten für digitale Übeprüfungen](walkthrough-exporting-data-for-a-digital-audit.md).  

### <a name="data-export-filters" />Datenexportfilter
Wenn Sie einen Datenexport einrichten, können Sie Daten für verschiedene Stufen filtern, wie in der folgenden Tabelle beschrieben.  

|Filterebene|Description|  
|------------------|---------------------------------------|  
|Periodenfilter|Sie können ein Start- und Enddatum für die Daten angeben, die exportiert werden. Sie können diesen Periodenfilter verwenden, um die Daten zu filtern. Wenn Sie beispielsweise einen Periodenfilter für den Export festlegen, können Sie dann Tabellenfilter festlegen, die die Periode verwenden.|  
|Tabellenfilter|Sie können Filter in jeder Tabelle im Export festlegen. Beispielsweise können Sie nur offene Posten einbeziehen oder Posten, die ein Buchungsdatum im angegebenen Filter haben. Sie können einen Filter setzen, der auf FlowFields basiert, wie **Nettoveränderung (MW)**, werden nur auf die Exportdebitoren, in denen noch eine Änderung gegeben hat, angezeigt. **Wichtig:** Die können Sie Tabellenfilter festlegen, der auf einem FlowFilter basiert. <br /><br /> Wenn Sie Tabellenfilter hinzufügen, können Sie Leistung erhöhen, indem Sie die Felder angeben, anhand derer die exportierten Daten durch den Wert **Schlüsselnr.** werden Die Beschreibung der Datensatzdefinition. Welche Schlüssel Sie verwenden, hängt von der Tabelle ab. Wenn die Tabelle beispielsweise nur zwei Schlüsselfelder und relativ wenige Posten aufweist, dann beeinflusst die Sortierreihenfolge nicht die Geschwindigkeit des Exports. Bei der Tabelle als Sachposten, ist der Export schneller, wenn Sie den Schlüssel im Voraus als den `G/L Account No.,Posting Date` Schlüssel festlegen. Wenn Sie keinen Schlüssel angeben, dann wird der Primärschlüssel verwendet, was möglicherweise nicht die beste Auswahl sein kann.<br /><br /> Andere Tabellen, in denen es hilfreich sein kann, den Schlüssel anzugeben, enthalten den Debitor. Posten und Tabelle Kreditorenposten.|  
|FlowField filters|Sie können FlowFields in den Export einbeziehen und Filter auf Basis der Periode festlegen. Beispielsweise können Sie den Periodenfilter auf das Feld**Saldo bis Datum** im **Sachkonto** anwenden.|  

Wenn Sie ein FlowField wie das Feld **Nettoveränderung (MW)** in der Tabelle **Debitor** einbeziehen, können Sie festlegen, dass die Einträge basierend auf dem Restbetrag am Enddatum der GDPdU-Periode gefiltert werden müssen. Wenn Sie dies als Feldfilter hinzufügen, basieren die Berechnungsformeln auf den Daten, die während des Exports angegeben werden.

Weitere Informationen finden Sie unter [GDPdU-Filterbeispiele](gdpdu-filter-examples.md).

## <a name="export-performance" />Export-Leistung
 Wenn Sie große Datenbestände exportieren möchten, kann dies sehr lange Zeit dauern. Es ist empfehlenswert, dass Sie Datenexporte basierend auf den Ratschlägen Ihres Steuerberaters  exportieren, um Ihre Geschäftsanforderungen einzurichten, und die Anforderungen des Steuerprüfers einzurichten. Die Anzahl der Datensätze in einer Tabelle ist auch etwas, das Sie berücksichtigen sollten.  

## <a name="see-also" />Siehe auch
 [Wie Sie Daten für eine Digital-Überwachung einrichten](how-to-set-up-data-exports-for-digital-audits.md)   
 [Wie Sie Daten für eine Digital-Überwachung exportieren](how-to-export-data-for-a-digital-audit.md)   
 [Wie Sie Daten für eine Digital-Überwachung exportieren](walkthrough-exporting-data-for-a-digital-audit.md)   
 [Lokale Funktion (Deutschland)](germany-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
