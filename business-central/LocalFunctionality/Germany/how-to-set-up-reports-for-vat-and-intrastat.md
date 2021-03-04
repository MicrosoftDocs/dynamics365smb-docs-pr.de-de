---
title: 'Gewusst wie: Einrichten von Berichten für MwSt. und Intrastat'
description: Sie können festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 5a05080b7882f2dbfa26c84964609b58787c89c2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747507"
---
# <a name="set-up-reports-for-vat-and-intrastat"></a>Richten Sie Berichte für MwSt ein.
In [!INCLUDE[prod_short](../../includes/prod_short.md)] können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.  

### <a name="to-set-up-reports-for-vat"></a>Richten Sie MwSt.-Berichte ein.  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Berichtsauswahl MwSt.** ein, und wählen Sie dann den entsprechenden Link.  

2.  Auf der Seite **Berichtsauswahl - MwSt.** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten. Dieses umfasst die MwSt.-Abrechnung und den MwSt.-Abrechnungsplan.  

3.  Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Reihenfolge**|Gibt an, wo in der Druckreihenfolge ein Bericht steht.|  
    |**Berichts-ID**|Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.|  
    |**Berichtsname**|Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird. Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.|  

4.  Wählen Sie die Schaltfläche **OK** aus.  

### <a name="to-set-up-reports-for-intrastat"></a>Richten Sie Intrastat-Berichte ein.  
> [!NOTE]
> Intrastat-Berichte können entweder das XML- oder das ASCII-Format verwenden. Geben Sie je nach verwendetem Format die Materialnummer in eines der folgenden Felder auf der Seite **Unternehmensinformationen** ein.  
> 
> |Format|Felder|
> |---------|---------|
> |XML|Unternehmensnummer|
> |ASCII|Verkaufsmaterial-Nr., Einkaufsmaterial-Nr.|

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Berichtsauswahl** ein, und wählen Sie dann den entsprechenden Link.  

2.  Auf der Seite **Berichtsauswahl - Intrastat** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten. Dieses umfasst die Intrastat-Checkliste und das Intrastat-Formular.  

3.  Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Reihenfolge**|Gibt an, wo in der Druckreihenfolge ein Bericht steht.|  
    |**Berichts-ID**|Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.|  
    |**Berichtsname**|Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird. Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.|  

4.  Wählen Sie die Schaltfläche **OK** aus.  

## <a name="see-also"></a>Siehe auch  
[Exportieren und Drucken von Intrastat-Berichten](how-to-export-and-print-intrastat-reports.md)  
[MwSt.-Abrechnung](vat-reporting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]