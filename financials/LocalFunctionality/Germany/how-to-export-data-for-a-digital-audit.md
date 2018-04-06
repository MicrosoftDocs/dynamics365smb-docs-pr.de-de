---
title: "Wie Sie Daten für eine Digital-Überwachung exportieren"
description: "Sie können Finanz- und Steuerdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert. Zudem können verschiedene Optionen in eine XML-Datei eingeschlossen werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: 88b8566d0143b5ca8301fb2a16da727ed2d8f2f8
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="export-data-for-a-digital-audit"></a>Wie Sie Daten für eine Digital-Überwachung exportieren
Sie können Finanz- und Steuerdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert. Zudem können verschiedene Optionen in eine XML-Datei eingeschlossen werden.  

Falls es keine Daten zum Exportieren gibt, erstellt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] leere Dateien.  

### <a name="to-export-data-for-a-digital-audit"></a>Wie Sie Daten für eine Digital-Überwachung exportieren

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Geschäftsdaten exportieren** ein. Wählen Sie dann den zugehörigen Link aus.  

2.  Füllen Sie im Stapelverarbeitungsauftrag **Datenexport** im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Startdatum**|Gibt das Startdatum des Berichts für den Datenexport an.<br /><br /> **HINWEIS:** Wenn die Datenenexportquell Periodenfelder einschließt, wird das Startdatum und das Enddatum als Filterwert für die Periodenfelder verwendet.|  
    |**Enddatum**|Gibt das Enddatum des Berichts für den Datenexport an.|  
    |**Abschlussdatum einschließen**|Gibt an, ob der Datenexport das Ultimodatum der Periode enthalten soll.|  

3.  Wählen Sie im Inforegister **Datenexport - Datensatzdefinition** die entsprechenden Filter aus, um den Datenexport zu identifizieren und Daten exportieren Datensatztyp. Weitere Informationen finden Sie unter [Prozess für Digital-Überwachung (/GoBD GDPdU)](process-for-digital-audits.md).  

4.  Um Daten zu exportieren, wählen Sie die Schaltfläche **OK**, um den Export zu starten.  

    > [!WARNING]  
    >  Während des Exports werden alle vorhandenen Dateien, einschließlich der Protokolldatei, überschrieben. Wenn Sie identische Daten mehrfach exportieren, werden die Dateien aus dem ersten Export überschrieben  

 Sie werden informiert, wenn der Export abgeschlossen ist. Wenn Sie den Export abbrechen oder das Fenster schließen, werden Sie informiert, dass der Export abgeschlossen ist, aber der Protokollordner bleibt leer. Abhängig von Ihrer Konfiguration, wurden eventuell einige Dateien exportiert, aber der Export ist möglicherweise noch nicht abgeschlossen.  

## <a name="see-also"></a>Siehe auch  
[Prozess für Digital-Überwachung (/GoBD GDPdU)](process-for-digital-audits.md)

