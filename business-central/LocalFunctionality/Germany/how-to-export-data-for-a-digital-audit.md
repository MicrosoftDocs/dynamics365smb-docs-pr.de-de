---
title: Wie Sie Daten für eine Digital-Überwachung exportieren
description: Sie können Finanz- und Steuerdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert. Zudem können verschiedene Optionen in eine XML-Datei eingeschlossen werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 669f1adf020cafb253a69289487c7d82972f1d0d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920076"
---
# <a name="export-data-for-a-digital-audit"></a>Wie Sie Daten für eine Digital-Überwachung exportieren
Sie können Finanz- und Steuerdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert. Zudem können verschiedene Optionen in eine XML-Datei eingeschlossen werden.  

Falls es keine Daten zum Exportieren gibt, erstellt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] leere Dateien.  

### <a name="to-export-data-for-a-digital-audit"></a>Wie Sie Daten für eine Digital-Überwachung exportieren

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Geschäftsdaten exportieren** ein, und wählen Sie dann den entsprechenden Link.  

2.  Füllen Sie auf der Seite **Geschäftsdaten exportieren** im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Startdatum**|Gibt das Startdatum des Berichts für den Datenexport an.<br /><br /> **HINWEIS:** Wenn die Datenexportquell Periodenfelder einschließt, wird das Startdatum und das Enddatum als Filterwert für die Periodenfelder verwendet.|  
    |**Enddatum**|Gibt das Enddatum des Berichts für den Datenexport an.|  
    |**Abschlussdatum einschließen**|Gibt an, ob der Datenexport das Ultimodatum der Periode enthalten soll.|  

3.  Wählen Sie im Inforegister **Datenexport - Datensatzdefinition** die entsprechenden Filter aus, um den Datenexport zu identifizieren und Daten exportieren Datensatztyp. Weitere Informationen finden Sie unter [Prozess für Digital-Überwachung (GoBD/GDPdU)](process-for-digital-audits.md).  

4.  Um Daten zu exportieren, wählen Sie die Schaltfläche **OK** , um den Export zu starten.  

    > [!WARNING]  
    >  Während des Exports werden alle vorhandenen Dateien, einschließlich der Protokolldatei, überschrieben. Wenn Sie identische Daten mehrfach exportieren, werden die Dateien aus dem ersten Export überschrieben  

 Sie werden informiert, wenn der Export abgeschlossen ist. Wenn Sie den Export abbrechen oder die Seite schließen, werden Sie informiert, dass der Export abgeschlossen ist, aber der Protokollordner bleibt leer. Abhängig von Ihrer Konfiguration, wurden eventuell einige Dateien exportiert, aber der Export ist möglicherweise noch nicht abgeschlossen.  

## <a name="see-also"></a>Siehe auch  
[Prozess für Digital-Überwachung (GoBD/GDPdU)](process-for-digital-audits.md)
