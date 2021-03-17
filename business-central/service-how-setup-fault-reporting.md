---
title: Einrichten von Fehlermeldungsberichten in Service Management | Microsoft Docs
description: 'Gewusst wie: Einrichten von Problemberichtsprozessen.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: dc0222b14d5c67149797b1f3ceb3813699a171d2
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392124"
---
# <a name="set-up-fault-reporting"></a>Fehlerberichte einrichten
Mit Fehlermeldung können Standards für das Erfassen von Fehlerinformationen für Serviceartikel einrichten. Beispielsweise können Sie festlegen, was das Problem ist, die Symptome, die Sie sehen, die Ursache für das Problem und wie es gelöst werden soll.  

Fehlercodes beschreibt die verschiedenen Serviceartikelprobleme oder die Arbeiten, die an Serviceartikeln durchgeführt wurden. Abhängig von der Problembeschreibungsebene in Ihrer Firma müssen Sie eventuell Problembereichs- und Symptomcodes definieren, bevor Sie Problemcodes erfassen. Beschreibt Problembereiche von Serviceartikelproblemen. Problemursachencodes beschreiben die Ursache der Serviceartikelprobleme und ob bei Bedarf Garantie- und Vertragsrabatten gewährt werden. Beispielsweise können Garantie- und Vertragsrabatte ausgeschlossen werden, wenn der Debitor in gewisser Weise für den Fehler beim Serviceartikel verantwortlich ist. Sie weisen Problemursachencodes für Serviceaufträge zu. Weitere Informationen finden Sie unter [Einrichten von Servicekosten](service-how-to-work-on-service-tasks.md)  

## <a name="to-specify-the-overall-level-of-fault-reporting-to-use"></a>Um den Gesamtniveau der Problemberichte festlegen, die verwendet werden
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceeinrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie im Feld **Fehlerebenenbericht** eine der Optionen aus, die in der folgenden Tabelle beschrieben werden.  

    |**Fehlerebene**|**Beschreibung**|  
    |------------|-------------|  
    |Keine | Es werden keine Berichtscodes werden verwendet.|  
    |Problemursache | Codes werden in derTabelle **Problemcode** aufgelistet. Durch diese Codes können Probleme bei Serviceartikeln oder Aktionen bestimmt werden, die für Serviceartikel auszuführen sind. Verwandte Codes können in Gruppierungen des **Problembereichscodes** gruppiert werden.|  
    |Problem u. Symptom | Sie stellen eine Kombination aus Codes in den Tabellen **Problemcodes** und **Symptomcodes** bereit. Zu den typischen Symptomcodes gehören Indikatoren, die ein Debitor zur Beschreibung eines Problems nutzen kann, beispielsweise bzgl. Lärm oder Qualität.|  
    |Problem u. Symptom u. Bereich | Verwenden Sie Problem-, Symptom- und Problembereichcodes als Implementierung des internationalen Reparaturcodierungssystems (IRIS).|  

Um die Einrichtung des Problemberichtwesens abzuschließen, kann auch angegeben werden, welche Reparaturen oder Lösungen bei einem Problem oder Fehler zum Einsatz kommen sollen. Setzen Sie das auf der Seite **Problem/Lösungen Zuordnungen** auf, wo Sie die Kombinationen von Codes für die Serviceartikelgruppe des Serviceartikels eingeben, von dem Sie auf witndow sowie die Häufigkeit für jede einzelne Kombination zugreifen.

## <a name="to-create-fault-and-resolution-code-relationships"></a>Einfügen von Problem/Lösungscode-Beziehungen
<!--this needs to go in a working with topic-->
Um die üblichsten Reparaturmethoden für Fehler an Serviceartikeln anzeigen zu können, ist es notwendig, Informationen über die Problem/Lösungscode Zuordnungen zu erstellen. Verwenden Sie die Stapelverarbeitung **Prob.-/Lösungszuord. ermitteln**, um alle Kombinationen von Problem- und Lösungscodes in gebuchten Serviceaufträgen zu ermitteln und sie im Fenster **Problem-/Lösungszuordnungen** zu erfassen.

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Prob.-/Lösungszuord. ermitteln** ein und wählen Sie dann den entsprechenden Link.  
2. Geben Sie die daten ein, um den Zeitraum zu definieren, der von der Stapelverarbeitung berücksichtigt werden soll.  
3. Aktivieren Sie das Feld **Zuordnung basierend auf Serviceartikelgruppe**, wenn die Zuordnungen nach Serviceartikelgruppen sortiert werden sollen.  
4. Um bereits manuell auf der Seite **Problem-/Lösungszuordnungscodebeziehungen** eingefügte Datensätze zu behalten, aktivieren Sie das Kontrollkästchen **Manuell eingefügte Datensätze behalten**.  

## <a name="see-also"></a>Siehe auch
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Service](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]