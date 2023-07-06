---
title: Projekte für die automatische Ausführung planen
description: 'Erfahren Sie, wie Sie Aufgabenwarteschlangenposten verwenden, um Berichte und Codeunits auszuführen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 03/20/2023
ms.custom: bap-template
ms.search.form: '672, 673, 674, 671'
---
# <a name="use-job-queues-to-schedule-tasks"></a><a name="use-job-queues-to-schedule-tasks"></a><a name="use-job-queues-to-schedule-tasks"></a>Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung

Verwenden Sie die Seite **Aufgabenwarteschlangenposten** um bestimmte Berichte und Codeunits zu planen und auszuführen. Die Projekte können entweder einmalig oder wiederholt ausgeführt werden. So kann es beispielsweise empfehlenswert sein, den Bericht **Verkäufer * Verkäuferstatistik** wöchentlich auszuführen, um die Verkaufserfolge eines Verkäufers zu beobachten, oder die Codeunit **Genehmigungsanforderungen delegieren** täglich auszuführen, um zu verhindern, dass sich Belege ansammeln.

Im Fenster Projektwarteschlangeneinträge sind alle aktuellen Aufgabenwarteschlangenposten aufgelistet. Wenn Sie eine neue Aufgabenwarteschlangenposten hinzufügen, der nach einem Zeitplan ausgeführt wird, müssen Sie einige Informationen bereitstellen. Beispiel:

* Der Objekttyp, der ausgeführt werden soll, z. B. ein Bericht oder eine Codeunit. Sie müssen über die Berechtigung zum Ausführen des jeweiligen Berichts oder der Codeunit verfügen.
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

Nachdem eine Aufgabe erfolgreich abgeschlossen wurde, wird sie aus der Liste der Aufgabenwarteschlangenposten entfernt, es sei denn, es handelt sich um ein wiederkehrendes Projekt. Bei mehrfach ausführbaren Einzelvorgängen wird das Feld **Früheste Startzeit** angepasst, um anzuzeigen, wann die Aufgabe das nächste Mal ausgeführt wird.  

## <a name="monitor-status-or-errors-in-the-job-queue"></a><a name="monitor-status-or-errors-in-the-job-queue"></a><a name="monitor-status-or-errors-in-the-job-queue"></a>Überwachen von Status oder Fehlern in der Projektwarteschlange

Von der Aufgabenwarteschlange generierte Daten werden gespeichert, sodass Sie Fehler beheben können.  

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

### <a name="to-view-status-for-any-job"></a><a name="to-view-status-for-any-job"></a><a name="to-view-status-for-any-job"></a>So wird der Status für jedes beliebige Projekt angezeigt

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Auftragswarteschlangenposten** ein und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Projektwarteschlangeneinträge** wählen Sie einen Projektwarteschlangeneintrag aus, und wählen die dann die Aktion **Protokolleinträge** aus.  

> [!TIP]
> Um tiefergehende Analysen basierend Telemetrie zu erhalten, können Sie Application Insights in Microsoft Azure verwenden, um den Status von Augabenwarteschlangenposten zu erhalten. Weitere Informationen zur Telemetrie finden Sie unter [Überwachung und Analyse der Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) und [Analysieren der Projektwarteschlangen-Lebenszyklus-Nachverfolgungs-Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

## <a name="view-scheduled-tasks"></a><a name="view-scheduled-tasks"></a><a name="view-scheduled-tasks"></a>Geplante Aufgaben anzeigen

Die Seite **Geplante Aufgaben** in [!INCLUDE [prod_short](includes/prod_short.md)] zeigt an, welche Aufgaben in der Auftragswarteschlange zum Ausführen bereit sind. Die Seite enthält auch Informationen über die Firma, für die jede Aufgabe zum Ausführen festgelegt ist. Es können jedoch nur Aufgaben ausgeführt werden, die als zur aktuellen Umgebung gehörig markiert sind.  

Wenn sich das aktuelle Unternehmen beispielsweise in einer Umgebung befindet, die eine Kopie einer anderen Umgebung ist, werden alle geplanten Aufgaben beendet. Verwenden Sie die Seite **Geplante Aufgaben**, um Aufgaben als bereit zum Ausführen in der Auftragswarteschlange festzulegen.  

> [!NOTE]
> Interne Administratoren und lizenzierte Benutzer können Aufgaben zum Ausführen planen. Delegierte Administratoren können Aufgaben festlegen und deren Ausführung planen, aber nur lizenzierte Benutzer können sie ausführen.

## <a name="the-my-job-queue-part"></a><a name="the-my-job-queue-part"></a><a name="the-my-job-queue-part"></a>Der „Meine Aufgabenwarteschlangen“-Teil

Der Teil **Meine Projektwarteschlange** in Ihrem Rollencenter zeigt die Projektwarteschlangeneinträge an, die Sie gestartet haben, die jedoch nicht abgeschlossen sind. Dieser Teil wird standardmäßig nicht angezeigt, Sie können ihn jedoch Ihrem Rollencenter hinzufügen. Weitere Informationen zur Personalisierung finden Sie unter [Ihren Arbeitsbereich personalisieren](ui-personalization-user.md).  

Der Teil zeigt die folgenden Informationen an:

* Welche Belege mit Ihrer ID im Feld **Zugewiesene Benutzer-ID** verarbeitet oder in die Warteschlange gestellt werden, einschließlich der Belege, die im Hintergrund gebucht werden. 
* Ob beim Buchen eines Belegs oder im Aufgabenwarteschlangenposten ein Fehler aufgetreten ist. 

Im Teil „Meine Aufgabenwarteschlange“ können Sie eine Belegbuchung auch stornieren.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a><a name="to-view-an-error-from-the-my-job-queue-part"></a><a name="to-view-an-error-from-the-my-job-queue-part"></a>So zeigen Sie einen Fehler aus dem Bereich Meine Projektwarteschlange an.

1. Bei einem Eintrag mit dem Status **Fehler** wählen Sie die Aktion **Fehler anzeigen** aus.
2. Überprüfen Sie die Fehlermeldung und korrigieren Sie das Problem.

## <a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a><a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a><a name="examples-of-what-you-can-schedule-using-job-queue-entries"></a>Beispiele dafür, was Sie mithilfe von Projektwarteschlangenposten planen können

### <a name="schedule-reports"></a><a name="schedule-reports"></a><a name="schedule-reports"></a>Berichte planen

Sie können einen Bericht oder einen Stapelverarbeitungsauftrag planen, sodass er an einem bestimmten Datum und zu einer festgelegten Uhrzeit ausgeführt wird. Geplante Berichte und Stapelverarbeitungsaufträge werden in der Projektwarteschlange eingegeben und zu der geplanten Zeit verarbeitet, wie vergleichbare andere Aufträge auch. Sie wählen die **Zeitplan** Option aus, nachdem Sie die Schaltfläche **Senden an** gewählt haben und geben Sie dann Informationen wie den Drucker sowie Uhrzeit und Datum und Serienmuster ein.  

Weitere Informationen zum Planen finden Sie unter [Bericht für die Ausführung planen](ui-work-report.md#ScheduleReport)

### <a name="schedule-synchronization-between--and-includeprod_short"></a><a name="schedule-synchronization-between--and-includeprod_short"></a><a name="schedule-synchronization-between--and-includeprod_short"></a>Die Synchronisierung planen zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)]

Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] in [!INCLUDE[prod_short](includes/cds_long_md.md)] integriert haben, können Sie über die Aufgabenwarteschlange planen, wann Daten synchronisiert werden sollen. Je nach Richtung und Regeln, die Sie definiert haben, kann der Auftgabenwarteschlangenposten Datensätze in einer Anwendung erstellen, die mit Datensätzen in der anderen Anwendung übereinstimmen. Wenn Sie beispielsweise einen Kontakt in [!INCLUDE[crm_md](includes/crm_md.md)] registrieren, kann der Aufgabenwarteschlangenposten diesen Kontakt für Sie in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten. Mehr über die Zeitplanung erfahren Sie unter [Planen einer Synchronisierung zwischen Business Central und Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

### <a name="schedule-when-to-post-sales-and-purchase-orders"></a><a name="schedule-when-to-post-sales-and-purchase-orders"></a><a name="schedule-when-to-post-sales-and-purchase-orders"></a>Planen, wann Verkaufsaufträgen und Bestellungen gebucht werden sollen

Anhand von Aufgabenwarteschlangenposten können Sie die Ausführung von Geschäftsprozessen im Hintergrund planen. Hintergrundaufgaben sind beispielsweise hilfreich, wenn mehrere Benutzer Verkaufsaufträge gleichzeitig buchen, aber nur ein Auftrag gleichzeitig verarbeitet werden kann. Mehr über die Buchung im Hintergrund erfahren Sie unter [So richten Sie Hintergrundbuchungen mit Aufgabenwarteschlangen ein](ui-batch-posting.md#to-set-up-background-posting-with-job-queues).

## <a name="handle-job-queue-entry-issues"></a><a name="handle-job-queue-entry-issues"></a><a name="handle-job-queue-entry-issues"></a>Probleme mit Aufgabenwarteschlangenposten beheben

Wenn ein Aufgabenwarteschlangenposten einen Fehler anzeigt, versuchen Sie als Erstes, den Aufgabenwarteschlangenposten neu zu starten. Sie können den Status des Aufgabenwarteschlangenposten auf **Angehalten** und dann auf **Bereit** setzen oder ihn einfach neu starten.

Wenn ein Neustart nicht hilft, liegt das Problem möglicherweise im Code. Sie finden den Besitzer (auch *Herausgeber* genannt) des Codes in der AL-Stapelüberwachung im Aufgabenwarteschlangenprotokoll. Wenn der Fehler von einer App/Erweiterung stammt, wenden Sie sich an Ihren Microsoft-Partner. Wenn der Fehler von einer Microsoft-Anwendung stammt, öffnen Sie eine Supportanfrage bei Microsoft.

Wenn Sie sich wegen Unterstützung an Ihren Microsoft-Partner oder an Microsoft wenden, geben Sie bitte die folgenden Informationen an:

* Die ID des Aufgabenwarteschlangenpostens, in dem der Fehler auftritt
* Der Zeitstempel, wann der Fehler aufgetreten ist
* Ihre Zeitzone

> [!TIP]
> Erfassen Sie die Informationen, je nachdem, ob Ihre [!INCLUDE [prod_short](includes/prod_short.md)] Version älter oder höher als 22.1 ist, auf folgende Weise:
>
> * Stellen Sie für frühere Versionen einen Screenshot der Seite **Auftragswarteschlangenprotokollposten** bereit.
> * Verwenden Sie für neuere Versionen die Aktion **Details kopieren** auf der Seite „Auftragswarteschlangenprotokollposten“, um die Informationen (Auftragswarteschlangen-ID, Zeitstempel und Ihre Zeitzone) zu kopieren.

## <a name="monitor-the-job-queue-with-telemetry"></a><a name="monitor-the-job-queue-with-telemetry"></a><a name="monitor-the-job-queue-with-telemetry"></a>Überwachen der Projektwarteschlange mit Telemetrie

Administratoren können [Azure Application Insights](/azure/azure-monitor/app/app-insights-overview) verwenden, um Telemetrie zu erfassen und zu analysieren, die hilft, Probleme zu identifizieren. Weitere Informationen zur Telemetrie finden Sie unter [Überwachung und Analyse der Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) und [Analysieren der Projektwarteschlangen-Lebenszyklus-Nachverfolgungs-Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace).

Mit Telemetrie können Administratoren Warnungen zu Problemen mit der Auftragswarteschlange einrichten, die eine SMS, E-Mail oder eine Nachricht in Teams senden, wenn etwas nicht stimmt. Weitere Informationen zu diesen Warnungen finden Sie unter [Warnung zu Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-alert).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Weitere Informationen

[Verwaltung](admin-setup-and-administration.md)  
[Einrichten von Business Central](setup.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Analysieren der Projektwarteschlangen-Lebenszyklus-Nachverfolgungs-Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-job-queue-lifecycle-trace)  
[Wartung zu Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-alert)

[!INCLUDE[footer-include](includes/footer-banner.md)]
