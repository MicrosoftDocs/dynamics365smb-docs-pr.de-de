---
title: Festlegen von Fehlerberichten im Service Management
description: Mit der Fehlerberichterstattung können Sie Standards für die Aufzeichnung von Fehlerinformationen für Serviceartikel mit Fehlercodes und mehr einrichten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---

# <a name="set-up-fault-reporting"></a><a name="set-up-fault-reporting"></a>Fehlerberichte einrichten
Mit Fehlermeldung können Standards für das Erfassen von Fehlerinformationen für Serviceartikel einrichten. Beispielsweise können Sie festlegen, was das Problem ist, die Symptome, die Sie sehen, die Ursache für das Problem und wie es gelöst werden soll.  

Fehlercodes beschreibt die verschiedenen Serviceartikelprobleme oder die Arbeiten, die an Serviceartikeln durchgeführt wurden. Abhängig von der Problembeschreibungsebene in Ihrer Firma müssen Sie eventuell Problembereichs- und Symptomcodes definieren, bevor Sie Problemcodes erfassen. Fehlerbereiche beschreiben Bereiche von Fehlern bei Service-Elementen. Problemursachencodes beschreiben die Ursache der Serviceartikelprobleme und ob bei Bedarf Garantie- und Vertragsrabatten gewährt werden. Beispielsweise können Garantie- und Vertragsrabatte ausgeschlossen werden, wenn der Debitor in gewisser Weise für den Fehler beim Serviceartikel verantwortlich ist. Sie weisen Problemursachencodes für Serviceaufträge zu. Weitere Informationen finden Sie unter [Einrichten von Servicekosten](service-how-to-work-on-service-tasks.md)  

## <a name="to-specify-the-overall-level-of-fault-reporting"></a><a name="to-specify-the-overall-level-of-fault-reporting"></a>So legen Sie die Gesamtebene der Fehlerberichterstattung fest
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Service Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie im Feld **Fehlerebenenbericht** eine der Optionen aus, die in der folgenden Tabelle beschrieben werden.  

    |**Fehlerebene**|**Beschreibung**|  
    |------------|-------------|  
    |Keine | Es werden keine Berichtscodes werden verwendet.|  
    |Problemursache | Codes werden in derTabelle **Problemcode** aufgelistet. Durch diese Codes können Probleme bei Serviceartikeln oder Aktionen bestimmt werden, die für Serviceartikel auszuführen sind. Verwandte Codes können in Gruppierungen des **Problembereichscodes** gruppiert werden.|  
    |Problem u. Symptom | Sie stellen eine Kombination aus Codes in den Tabellen **Problemcodes** und **Symptomcodes** bereit. Zu den typischen Symptomcodes gehören Indikatoren, die ein Debitor zur Beschreibung eines Problems nutzen kann, beispielsweise bzgl. Lärm oder Qualität.|  
    |Problem u. Symptom u. Bereich | Verwenden Sie Problem-, Symptom- und Problembereichcodes als Implementierung des internationalen Reparaturcodierungssystems (IRIS).|  

Um die Einrichtung des Problemberichtwesens abzuschließen, kann auch angegeben werden, welche Reparaturen oder Lösungen bei einem Problem oder Fehler zum Einsatz kommen sollen. Sie legen das auf der Seite **Fehler-/Lösungscode-Beziehungen** fest, wo Sie Kombinationen von Codes für die Serviceartikel-Gruppe des Serviceartikels, von dem aus Sie auf das Fenster zugegriffen haben, und die Anzahl des Auftretens für jeden einzelnen festlegen.

## <a name="to-create-fault-and-resolution-code-relationships"></a><a name="to-create-fault-and-resolution-code-relationships"></a>Einfügen von Problem/Lösungscode-Beziehungen
<!--this needs to go in a working with topic-->
Um die üblichsten Reparaturmethoden für Fehler an Serviceartikeln anzeigen zu können, ist es notwendig, Informationen über die Problem/Lösungscode Zuordnungen zu erstellen. Verwenden Sie die Stapelverarbeitung **Prob.-/Lösungszuord. ermitteln**, um alle Kombinationen von Problem- und Lösungscodes in gebuchten Serviceaufträgen zu ermitteln und sie im Fenster **Problem-/Lösungszuordnungen** zu erfassen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Fehler/Resol. Codes Relationships** ein und wählen Sie dann den entsprechenden Link.  
2. Geben Sie die daten ein, um den Zeitraum zu definieren, der von der Stapelverarbeitung berücksichtigt werden soll.  
3. Aktivieren Sie das Feld **Zuordnung basierend auf Serviceartikelgruppe**, wenn die Zuordnungen nach Serviceartikelgruppen sortiert werden sollen.  
4. Um bereits manuell auf der Seite **Problem-/Lösungszuordnungscodebeziehungen** eingefügte Datensätze zu behalten, aktivieren Sie das Kontrollkästchen **Manuell eingefügte Datensätze behalten**.  

## <a name="see-also"></a><a name="see-also"></a>Siehe auch
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Service](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
