---
title: 'Gewusst wie: Einrichten von Berichten für MwSt. und Intrastat'
description: 'Sie können festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-reports-for-vat-and-intrastat"></a><a name="set-up-reports-for-vat-and-intrastat"></a>Richten Sie Berichte für MwSt ein.

[!INCLUDE[intrastat-2022w2](../../includes/intrastat-2022w2.md)]

In [!INCLUDE[prod_short](../../includes/prod_short.md)] können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.  

## <a name="to-set-up-reports-for-vat"></a><a name="to-set-up-reports-for-vat"></a>Richten Sie MwSt.-Berichte ein.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Berichtsauswahl – MwSt.** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Berichtsauswahl - MwSt.** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten. Dieses umfasst die MwSt.-Abrechnung und den MwSt.-Abrechnungsplan.  
3. Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Reihenfolge**|Gibt an, wo in der Druckreihenfolge ein Bericht steht.|  
    |**Berichts-ID**|Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.|  
    |**Berichtsname**|Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird. Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.|  

4. Wählen Sie die Schaltfläche **OK** aus.  

### <a name="to-set-up-reports-for-intrastat"></a><a name="to-set-up-reports-for-intrastat"></a>Richten Sie Intrastat-Berichte ein.

> [!NOTE]
> Intrastat-Berichte können entweder das XML- oder das ASCII-Format verwenden. Geben Sie je nach verwendetem Format die Materialnummer in eines der folgenden Felder auf der Seite **Unternehmensinformationen** ein.  
>
> |Format|Felder|
> |---------|---------|
> |XML|Unternehmensnummer|
> |ASCII|Verkaufsmaterial-Nr., Einkaufsmaterial-Nr.|

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Berichtsauswahl** ein und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Berichtsauswahl - Intrastat** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten. Dieses umfasst die Intrastat-Checkliste und das Intrastat-Formular.  
3. Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Reihenfolge**|Gibt an, wo in der Druckreihenfolge ein Bericht steht.|  
    |**Berichts-ID**|Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.|  
    |**Berichtsname**|Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird. Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.|  

4. Wählen Sie die Schaltfläche **OK**.  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Exportieren und Drucken von Intrastat-Berichten](how-to-export-and-print-intrastat-reports.md)  
[MwSt.-Abrechnung](vat-reporting.md)
[Lokale Funktion (Deutschland)](germany-local-functionality.md)  
[Intrastat-Berichte einrichten](../../finance-how-setup-report-intrastat.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
