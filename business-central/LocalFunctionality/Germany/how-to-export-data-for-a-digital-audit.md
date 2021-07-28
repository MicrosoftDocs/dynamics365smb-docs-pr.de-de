---
title: So exportieren Sie Daten für eine digitale Betriebsprüfung [DE]
description: Sie können Finanz- und Steuerdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/18/2021
ms.author: edupont
ms.openlocfilehash: 3e5eaa78c41af3bf0e5e77128521e503e6c41372
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435877"
---
# <a name="export-data-for-a-digital-audit-in-the-german-version"></a>Datenexport für eine digitale Betriebsprüfung in der deutschen Version
Sie können Finanz- und Steuerdaten exportieren entsprechend dem Prozess für Datenzugriff und Testbarkeit von digitalen Dokumenten (GDPdU), der auf deutschen Steuergesetzen basiert. Zudem können verschiedene Optionen in eine XML-Datei eingeschlossen werden.  

Falls es keine Daten zum Exportieren gibt, erstellt [!INCLUDE[prod_short](../../includes/prod_short.md)] leere Dateien.  

### <a name="to-export-data-for-a-digital-audit"></a>Wie Sie Daten für eine Digital-Überwachung exportieren

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../../media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Geschäftsdaten exportieren** ein, und wählen Sie dann den entsprechenden Link.  

2.  Füllen Sie auf der Seite **Geschäftsdaten exportieren** im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Option|Description|  
    |----------------------------------|---------------------------------------|  
    |**Startdatum**|Gibt das Startdatum des Berichts für den Datenexport an.<br /><br /> **HINWEIS:** Wenn die Datenexportquell Periodenfelder einschließt, wird das Startdatum und das Enddatum als Filterwert für die Periodenfelder verwendet.|  
    |**Enddatum**|Gibt das Enddatum des Berichts für den Datenexport an.|  
    |**Abschlussdatum einschließen**|Gibt an, ob der Datenexport das Ultimodatum der Periode enthalten soll.|  

3.  Wählen Sie im Inforegister **Datenexport - Datensatzdefinition** die entsprechenden Filter aus, um den Datenexport zu identifizieren und Daten exportieren Datensatztyp. Weitere Informationen finden Sie unter [Prozess für Digital-Überwachung (GoBD/GDPdU)](process-for-digital-audits.md).  

4.  Um Daten zu exportieren, wählen Sie die Schaltfläche **OK**, um den Export zu starten.  

    > [!WARNING]  
    >  Während des Exports werden alle vorhandenen Dateien, einschließlich der Protokolldatei, überschrieben. Wenn Sie identische Daten mehrfach exportieren, werden die Dateien aus dem ersten Export überschrieben  

 Sie werden informiert, wenn der Export abgeschlossen ist. Wenn Sie den Export abbrechen oder die Seite schließen, werden Sie informiert, dass der Export abgeschlossen ist, aber der Protokollordner bleibt leer. Abhängig von Ihrer Konfiguration, wurden eventuell einige Dateien exportiert, aber der Export ist möglicherweise noch nicht abgeschlossen.  

## <a name="see-also"></a>Siehe auch  
[Prozess für Digital-Überwachung (GoBD/GDPdU)](process-for-digital-audits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]