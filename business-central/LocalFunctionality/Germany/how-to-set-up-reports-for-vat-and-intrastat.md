---
title: "Gewusst wie: Einrichten von Berichten für MwSt. und Intrastat"
description: "In Business Central können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 482064c69f23b7b1856d5a71278601a005097973
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-reports-for-vat-and-intrastat"></a>Richten Sie Berichte für MwSt ein.
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] können Sie festlegen, welche Berichte verwendet werden sollen, um die Dokumente zu erstellen, die Sie an die Behörden, wie beispielsweise die MwSt.-Abrechnung und das Intrastat-Formular übermitteln müssen.  

### <a name="to-set-up-reports-for-vat"></a>Richten Sie MwSt.-Berichte ein.  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **Berichtauswahl MwSt** ein. Wählen Sie dann den zugehörigen Link aus.  

2.  Im Fenster **Berichtsauswahl - MwSt.** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten. Dieses umfasst die MwSt.-Abrechnung und den MwSt.-Abrechnungsplan.  

3.  Geben Sie den Bericht oder den Batchauftrag an, die ausgeführt werden müssen, wenn ein Benutzer die Aktivität für die Belegart startet, die Sie im Feld **Verbrauch** angegeben haben. Füllen Sie die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Reihenfolge**|Gibt an, wo in der Druckreihenfolge ein Bericht steht.|  
    |**Berichts-ID**|Gibt die ID des Berichts an, der für diese Belegart gedruckt wird.|  
    |**Berichtsname**|Gibt den Namen des Berichts an, der für diese Belegart gedruckt wird. Die **Berichtsname** Feldupdates auf Grundlage der Auswahl im **Berichts-ID**.|  

4.  Wählen Sie die Schaltfläche **OK** aus.  

### <a name="to-set-up-reports-for-intrastat"></a>Richten Sie Intrastat-Berichte ein.  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Berichtauswahl** ein. Wählen Sie dann den zugehörigen Link aus.  

2.  Im Fenster **Berichtsauswahl - Intrastat** im Feld **Verbrauch**, wählen Sie die Art des Belegs aus, für die Sie Berichte festlegen möchten. Dieses umfasst die Intrastat-Checkliste und das Intrastat-Formular.  

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
