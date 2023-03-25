---
title: Projekte für die automatische Ausführung planen
description: Geplante Aufgaben sind von der Aufgabenwarteschlange verwaltet. Diese Projektausführungsberichte und Codeunits. Die Projekte können entweder einmalig oder wiederholt ausgeführt werden.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '672, 673, 674, 671'
ms.date: 10/01/2021
ms.author: edupont
---
# Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung

Die Seite Aufgabenwarteschlangenposten ermöglicht es Benutzern, bestimmte Berichte und Codeunits zu planen und auszuführen. Die Projekte können entweder einmalig oder wiederholt ausgeführt werden. So kann es beispielsweise empfehlenswert sein, den Bericht **Verkäufer * Verkäuferstatistik** wöchentlich auszuführen, um die Verkaufserfolge eines Verkäufers zu beobachten, oder die Codeunit **Genehmigungsanforderungen delegieren** täglich auszuführen, um zu verhindern, dass sich Belege ansammeln.

Im Fenster **Projektwarteschlangeneinträge** sind alle aktuellen Aufgabenwarteschlangenposten aufgelistet. Wenn Sie eine neue Aufgabenwarteschlangeneintrag hinzufügen, den Sie planen möchten, müssen Sie einige Informationen bereitstellen. Beispiel:

* Der Objekttyp, den Sie ausführen möchten, z. B. ein Bericht oder eine Codeunit. Sie müssen über die Berechtigung zum Ausführen des jeweiligen Berichts oder der Codeunit verfügen.
* Der Name und die Objekt-ID des Objekts. 
* Parameter, um das Verhalten des Aufgabenwarteschlangenpostens festzulegen. So können Sie beispielsweise einen Parameter hinzufügen, um nur gebuchte Verkaufsaufträge zu senden. 
* Wann und wie oft wird der Jobwarteschlangenposten ausgeführt.

> [!IMPORTANT]  
> Wenn Sie den SUPER Berechtigungs-Satz mit dem Wert [!INCLUDE[prod_short](includes/prod_short.md)] festgelegt haben, sind Sie berechtigt, alle in Ihrer Lizenz enthaltenen Objekte auszuführen. Wenn Sie die Rolle Delegierter Admin haben, können Sie Einträge für die Aufgabenwarteschlange erstellen und planen, aber nur Administratoren und lizenzierte Benutzer können sie ausführen. Benutzer mit der Gerätelizenz können keine Aufträge erstellen oder ausführen.

Nachdem Projektwarteschlangen eingerichtet sind und ausgeführt werden, kann sich der Status innerhalb jedes wiederkehrenden Zeitraums folgendermaßen ändern:

* **Abwarten**  
* **Bereit**  
* **In Bearbeitung**  
* **Fehler**  
* **Erledigt**  

Nachdem eine Aufgabe erfolgreich abgeschlossen wurde, wird sie aus der Liste der Aufgabenwarteschlangenposten entfernt, es sei denn, es handelt sich um ein wiederkehrendes Projekt. Bei mehrfach ausführbaren Einzelvorgängen wird das Feld **Früheste Startzeit** angepasst, um anzuzeigen, wann der Einzelvorgang erwartungsgemäß das nächste Mal ausgeführt wird.  

## Überwachen von Status oder Fehlern in der Projektwarteschlange

Von der Aufgabenwarteschlange generierte Daten werden in der Datenbank gespeichert, sodass Sie Fehler der Aufgabenwarteschlange beheben können.  

Für jeden Projektwarteschlangeneintrag können Sie den Status anzeigen und ändern. Wenn Sie eine Projektwarteschlangenposten erstellen, wird der zugehörige Status auf **Warten** festgelegt. Sie können den Status beispielsweise auf **Bereit** und wieder auf **Warten** setzen. Andernfalls werden die Statusinformationen in diesem Feld automatisch aktualisiert.

Die folgende Tabelle beschreibt die Werte im Feld **Status**.

| Status | Beschreibung |
|--|--|
| Bereit | Die Aufgabenwarteschlange für die Ausführung bereit ist. |
| In Bearbeitung | Der Aufgabenwarteschlangenposten ist in Bearbeitung. Dieses Feld wird aktualisiert, während die Aufgabenwarteschlange ausgeführt wird. |
| Abwarten | Der Standardstatus des Aufgabenwarteschlangenpostens bei dessen Erstellung. Wählen Sie die Aktion **Status auf 'Bereit' festlegen**, um den Status auf **Bereit** zu ändern. Wählen Sie die Aktion **Auf „Abwarten“ setzen**, um den Status **Abwarten** wiederherzustellen. |
| Fehler | Ein Fehler ist aufgetreten. Wählen Sie **Fehler anzeigen** aus, um die Fehlermeldung anzuzeigen. |
| Fertig | Der Aufgabenwarteschlangenposten ist abgeschlossen. |

> [!Tip]  
> Die Ausführung von Aufgabenwarteschlangenposten wird beendet, wenn ein Fehler auftritt. Dies kann beispielsweise ein Problem sein, wenn ein Posten eine Verbindung zu einem externen Dienst herstellt, beispielsweise einem Bankfeed. Wenn der Dienst vorübergehend nicht verfügbar ist und der Aufgabenwarteschlangenposten keine Verbindung herstellen kann, zeigt der Eintrag einen Fehler an und wird nicht mehr ausgeführt. Sie müssen den Aufgabenwarteschlangenposten manuell neu starten. Diese Situation kann jedoch mit den Feldern **Maximale Anzahl von Versuchen** und **Verzögerung der erneuten Ausführung (Sek.)** vermieden werden. Im Feld **Maximale Anzahl von Versuchen** können Sie angeben, wie oft der Aufgabenwarteschlangenposten fehlschlagen kann, bevor dessen Ausführungsversuche beendet werden. Im Feld **Verzögerung der erneuten Ausführung (Sek.)** können Sie die Zeitspanne zwischen den Versuchen in Sekunden angeben. Durch die Kombination dieser beiden Felder kann der Aufgabenwarteschlangenposten weiter ausgeführt werden, bis der externe Dienst verfügbar wird.

### So wird der Status für jedes beliebige Projekt angezeigt

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun") Symbol. Geben Sie **Auftragswarteschlangenposten** ein und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Projektwarteschlangeneinträge** wählen Sie einen Projektwarteschlangeneintrag aus, und wählen die dann die Aktion **Protokolleinträge** aus.  

> [!TIP]
> Sie können den Status von Projektwarteschlangeneinträgen auch anzeigen, indem Sie Application Insights in Microsoft Azure für tiefergehende Analysen basierend auf Telemetrie verwenden. Weitere Informationen finden Sie unter [Überwachung und Analyse der Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) und [Analysieren der Projektwarteschlangen-Lebenszyklus-Nachverfolgungs-Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace) in den Entwickler- und Verwaltungsinhalten von [!INCLUDE [prod_short](includes/prod_short.md)].

## Geplante Aufgaben anzeigen

Die Seite **Geplante Aufgaben** in [!INCLUDE [prod_short](includes/prod_short.md)] zeigt an, welche Aufgaben in der Auftragswarteschlange zum Ausführen bereit sind. Die Seite enthält auch Informationen über die Firma, für die jede Aufgabe zum Ausführen festgelegt ist. Es können jedoch nur Aufgaben ausgeführt werden, die als zur aktuellen Umgebung gehörig markiert sind.  

Wenn sich das aktuelle Unternehmen beispielsweise in einer Umgebung befindet, die eine Kopie einer anderen Umgebung ist, werden alle geplanten Aufgaben beendet. Verwenden Sie die Seite **Geplante Aufgaben**, um Aufgaben als bereit zum Ausführen in der Auftragswarteschlange festzulegen.  

> [!NOTE]
> Interne Administratoren und lizenzierte Benutzer können Aufgaben zum Ausführen planen. Delegierte Administratoren können Aufgaben festlegen und deren Ausführung planen, aber nur lizenzierte Benutzer können sie ausführen.

## Der „Mein Projektwarteschlangenteil“

Der Teil **Meine Projektwarteschlange** in Ihrem Rollencenter zeigt die Projektwarteschlangeneinträge an, die Sie gestartet haben, die jedoch nicht abgeschlossen sind. Dieser Teil wird standardmäßig nicht angezeigt, Sie können ihn jedoch Ihrem Rollencenter hinzufügen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).  

Der Teil zeigt die folgenden Informationen an:

* Welche Belege mit Ihrer ID im Feld **Zugewiesene Benutzer-ID** verarbeitet oder in die Warteschlange gestellt werden, einschließlich der Belege, die im Hintergrund gebucht werden. 
* Ob beim Buchen eines Belegs oder im Aufgabenwarteschlangenposten ein Fehler aufgetreten ist. 

Im Teil „Meine Aufgabenwarteschlange“ können Sie eine Belegbuchung auch stornieren.

### So zeigen Sie einen Fehler aus dem Bereich Meine Projektwarteschlange an.

1. Bei einem Eintrag mit dem Status **Fehler** wählen Sie die Aktion **Fehler anzeigen** aus.
2. Überprüfen Sie die Fehlermeldung und korrigieren Sie das Problem.

## Beispiele dafür, was mithilfe der Projektwarteschlange geplant werden kann

### Berichte planen

Sie können einen Bericht oder einen Stapelverarbeitungsauftrag planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird. Geplante Berichte und Stapelverarbeitungsaufträge werden in der Projektwarteschlange eingegeben und zu der geplanten Zeit verarbeitet, wie vergleichbare andere Aufträge auch. Sie wählen die **Zeitplan** Option aus, nachdem Sie die Schaltfläche **Senden an** gewählt haben und geben Sie dann Informationen wie den Drucker sowie Uhrzeit und Datum und Serienmuster ein.  

Weitere Informationen finden Sie unter [Bericht für die Ausführung planen](ui-work-report.md#ScheduleReport)

### Die Synchronisierung planen zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)]

Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] in [!INCLUDE[prod_short](includes/cds_long_md.md)] integriert haben, können Sie über die Aufgabenwarteschlange planen, wann Daten synchronisiert werden sollen. Je nach Richtung und Regeln, die Sie definiert haben, kann der Auftgabenwarteschlangenposten Datensätze in einer Anwendung erstellen, die mit Datensätzen in der anderen Anwendung übereinstimmen. Wenn Sie beispielsweise einen Kontakt in [!INCLUDE[crm_md](includes/crm_md.md)] registrieren, kann der Aufgabenwarteschlangenposten diesen Kontakt für Sie in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten. Weitere Informationen finden Sie unter [Planen einer Synchronisierung zwischen Business Central und Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### Planen Sie die Buchung von Verkaufsaufträgen und Einkaufsbestellungen

Anhand von Aufgabenwarteschlangenposten können Sie die Ausführung von Geschäftsprozessen im Hintergrund planen. Hintergrundaufgaben sind beispielsweise hilfreich, wenn mehrere Benutzer Verkaufsaufträge gleichzeitig buchen, aber nur ein Auftrag gleichzeitig verarbeitet werden kann. Weitere Informationen finden Sie unter [Hintergrund-Buchung mit Aufgabenwarteschlangen](ui-batch-posting.md#to-set-up-background-posting-with-job-queues)

## Überwachen der Projektwarteschlange mit Telemetrie

Als Administrator können Sie [Application Insights](/azure/azure-monitor/app/app-insights-overview) zum Sammeln und Analysieren von Telemetriedaten verwenden, mit denen Sie Probleme identifizieren können. Weitere Informationen finden Sie in den Entwickler- und Verwaltungsinhalten unter [Überwachung und Analyse der Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-overview).  

## Weitere Informationen

[Verwaltung](admin-setup-and-administration.md)  
[Einrichten von Business Central](setup.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Analysieren der Projektwarteschlangen-Lebenszyklus-Nachverfolgungs-Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  


[!INCLUDE[footer-include](includes/footer-banner.md)]