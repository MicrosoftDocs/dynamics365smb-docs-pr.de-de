---
title: 'Vorgehensweise: Planen der Ausführung eines Berichts | Microsoft Docs'
description: Geplante Aufgaben sind von der Aufgabenwarteschlange verwaltet. Diese Projektausführungsberichte und Codeunits. Die Projekte können entweder einmalig oder wiederholt ausgeführt werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 1cf5b75bc63acfa07a90cda1d03f45579a0aa51d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935375"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung
Die Aufgabenwarteschlangen in [!INCLUDE[d365fin](includes/d365fin_md.md)] ermöglichen es Benutzern, bestimmte Berichte und Codeunits zu planen und auszuführen. Die Projekte können entweder einmalig oder wiederholt ausgeführt werden. So kann es beispielsweise empfehlenswert sein, den Bericht **Verkäufer - Verkäuferstatistik** wöchentlich auszuführen, um jede Woche die Verkaufserfolge eines Verkäufers im Auge zu haben, während die Codenit **Service-E-Mail-Warteschlange** verarbeiten" täglich ausgeführt wird, um sicherzustellen, dass ausstehende, serviceauftragsbezogene E-Mails rechtzeitig an die entsprechenden Debitoren versendet werden.

Im Fenster **Projektwarteschlangeneinträge** sind alle aktuellen Aufgabenwarteschlangenposten aufgelistet. Wenn Sie eine neue Projektwarteschlange hinzufügen, die Sie planen möchten, müssen Sie die Informationen über die Art des Objekts, das Sie ausführen möchten, angeben, wie der Name und die Objekt-ID, die Sie ausführen möchten. Sie können auch Parameter hinzufügen, um das Verhalten eines Aufgabenwarteschlangenpostens festzulegen. So können Sie beispielsweise einen Parameter hinzufügen, um nur gebuchte Verkaufsaufträge zu senden. Sie benötigen die entsprechende Berechtigung zum Ausführen des jeweiligen Berichts oder der jeweiligen Codeunit, da ansonsten beim Ausführen der Projektwarteschlange ein Fehler auftritt.  

Eine Aufgabenwarteschlange kann mehrere Posten haben. Diese stellen die Projekte dar, die die Warteschlange verwaltet und ausführt. Informationen in dem Posten geben an, welche Codeunit oder welcher Bericht ausgeführt wird, wann und wie häufig der Posten ausgeführt wird, in welcher Kategorie das Projekt ausgeführt wird, und wie es ausgeführt wird.  

## <a name="to-set-up-background-posting-with-job-queues"></a>So richten Sie Hintergrundbuchung mit Projektwarteschlangen ein
Projektwarteschlangen sind ein effektives Werkzeug, um die Ausführung von Geschäftsprozessen im Hintergrund zu planen, z. B. wenn mehrere Benutzer versuchen, Verkaufsaufträge zu buchen, aber nur ein Auftrag gleichzeitig verarbeitet werden kann. Alternativ können Sie Buchungen zu bestimmten Betriebszeiten planen, wenn es für Ihre Organisation hilfreich ist. Beispielsweise kann es in Ihrem Unternehmen sinnvoll sein, bestimmte Routinen dann auszuführen, wenn ein Großteil der Dateneingaben für einen Arbeitstag abgeschlossen wurde.

Sie können dies erreichen, indem Sie die Projektwarteschlange so einrichten, dass verschiedene Stapelbuchungsberichte ausgeführt werden, wie beispielsweise **Stapelbuchungsaufträge**-, **Stapelbuchungsverkaufsrechnungen**-, **Stapelbuchungsverkaufs-Rücklieferungen**- und **Stapelbuchungsverkaufs-Gutschriften**-Berichte. Weitere Informationen finden Sie unter [So erstellen Sie einen Projektwarteschlangeneintrag für Hintergrund-Verkaufsauftragsbuchung](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt die Hintergrundbuchung für alle Verkaufs-, Einkaufs- und Servicebelege.

Nachfolgend wird erklärt, wie die Hintergrundbuchung von Verkaufsaufträgen eingerichtet wird. Die Schritte sind für Einkauf und Service ähnlich.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Debitoren & Verkauf einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Auf der Seite **Einrichtung von Vertrieb und Forderungen** aktivieren Sie das Kontrollkästchen **Mit Projektwarteschlange buchen**.
3. Um nach Projektwarteschlangeneinträgen für Verkaufsauftragsbuchung zu filtern, aktivieren Sie das Feld **Projektwarteschlangen-Kategoriecode**, und wählen Sie dann die Kategorie **SalesPost** aus.

    Ein Projektwarteschlangenobjekt, codeunit 88 **Verkaufsbuchung über Projektwarteschlange**, wird erstellt. Fahren Sie fort, um es auf der Seite **Projektwarteschlangeneinträge** zu aktivieren.
4. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Projektwarteschlangeneinträge** ein, und wählen dann den zugehörigen Link aus.
5. Wählen Sie auf der Seite **Projektwarteschlangeneinträge** die Aktion **Neu**.
6. Wählen Sie im Feld **Auszuführender Objekttyp** die Option **Codeunit** aus.  
7. Wählen Sie im Feld **Auszuführende Objekt-ID** 88 aus, **Verkaufsbuchung über Projektwarteschlange** aus.

    Keine anderen Felder sind für dieses Szenario relevant.
8. Wählen Sie die Aktion **Status auf bereit festlegen** aus.
9. Um sicherzustellen, dass die Aufgabenwarteschlange wie erwartet arbeitet, buchen Sie einen Verkaufsauftrag. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
10. Überprüfen Sie auf der Seite **Projektwarteschlangen-Protokolleinträge**, ob der Verkaufsauftrag erfolgreich gebucht wurde. Weitere Informationen finden Sie unter [So wird der Status oder Fehler in der Projektwarteschlange angezeigt](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Wenn zusätzlich Verkaufsbelege gedruckt werden sollen, wenn diese gebucht werden, aktivieren Sie das Kontrollkästchen **Mit Projektwarteschlange buchen und drucken** auf der Seite **Einrichtung von Vertrieb und Forderungen**.  

> [!IMPORTANT]  
> Wenn Sie einen Beleg an einen Drucker senden und der Drucker ein Dialogfeld anzeigt, wie eine Anforderung für Anmeldeinformationen oder eine Warnung über geringe Druckertinte, wird der Beleg gebucht, aber nicht gedruckt. Die entsprechenden Aufgabenwarteschlangenposten überschreiten letztendlich die Zeit und das Feld **Status** ist auf **Fehler** festgelegt. Entsprechend empfiehlt es sich, dass Sie kein Druckersetup verwenden, das Aktivität mit der Anzeige von Druckerdialogfeldern in Verbindung mit Hintergrundbuchung benötigt.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>So wird ein Projektwarteschlangeneintrag für die Stapelbuchung von Verkaufsaufträgen erstellt
Der folgende Ablauf zeigt an, wie Sie den Bericht **Aufträge stapelbuchen** so festlegen, dass freigegebene Verkaufsaufträge um 16:00 Uhr an Wochentagen automatisch gebucht werden.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Projektwarteschlangeneinträge** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie im Feld **Auszuführender Objekttyp** die Option **Bericht** aus.  
4. Wählen Sie im Feld **Auszuführende Objekt-ID** 296 aus, **Stapelbuchung von Verkaufsaufträgen**.
5. Aktivieren Sie das Kontrollkästchen **Berichtsanforderungsseite**.
6. Auf der Anforderungsseite **Stapelbuchung von Verkaufsaufträgen** definieren Sie, was während der automatischen Buchung von Verkaufsaufträgen einbezogen wird, und wählen Sie dann die Schaltfläche **OK**.
7. Aktivieren Sie alle Kontrollkästchen von **Montags ausführen** bis **Freitags ausführen**.
8. In dem Feld **Startzeit** geben Sie 16:00 Uhr ein.
9. Wählen Sie die Aktion **Status auf bereit festlegen** aus.

Verkaufsaufträge, die bereit sind, gebucht zu werden, werden jetzt an jedem Wochentag um 16:00 Uhr gebucht.

> [!NOTE]
> Wenn die Projektwarteschlange den Verkaufsauftrag nicht buchen kann, wird der Status auf **Fehler** geändert, und der Verkaufsauftrag wird der Liste von Verkaufsaufträgen hinzugefügt, die der Benutzer manuell verarbeiten muss. Weitere Informationen finden Sie unter [So wird der Status oder Fehler in der Projektwarteschlange angezeigt](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Nachdem Projektwarteschlangen eingerichtet sind und ausgeführt werden, kann sich der Status innerhalb jedes wiederkehrenden Zeitraums folgendermaßen ändern:

* **Abwarten**  
* **Bereit**  
* **In Bearbeitung**  
* **Fehler**  
* **Erledigt**  

Nachdem ein Projekt erfolgreich abgeschlossen wurde, wird dieses aus der Liste der Projektwarteschlangeneinträge entfernt, es sei denn, es handelt sich um ein wiederkehrendes Projekt. Wenn es sich um ein wiederkehrendes Projekt handelt, wird das Feld **Früheste Startzeit** angepasst, um anzuzeigen, wann das Projekt erwartungsgemäß das nächste Mal ausgeführt wird.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>So werden Status oder Fehler in der Projektwarteschlange angezeigt
Daten, die erstellt werden, wenn eine Projektwarteschlange ausgeführt wird, werden in der Datenbank gespeichert, sodass Sie Projektwarteschlangenfehler beheben können.

### <a name="to-view-status-for-any-job"></a>So wird der Status für jedes beliebige Projekt angezeigt
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Projektwarteschlangeneinträge** ein, und wählen dann den zugehörigen Link aus.
2. Auf der Seite **Projektwarteschlangeneinträge** wählen Sie einen Projektwarteschlangeneintrag aus, und wählen die dann die Aktion **Protokolleinträge** aus.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>So wird der Status aus einem Verkaufs- oder Einkaufsbeleg angezeigt
1. Vom Beleg, den Sie versucht haben, mit der Projektwarteschlange zu buchen, wählen Sie das Feld **Projektwarteschlangenstatus** aus, das **Fehler** enthält.
2. Überprüfen Sie die Fehlermeldung und korrigieren Sie das Problem.

## <a name="the-my-job-queue-part"></a>Der „Mein Projektwarteschlangenteil”
Der Teil **Meine Projektwarteschlange** in Ihrem Rollencenter zeigt die Projektwarteschlangeneinträge an, die Sie gestartet haben, die jedoch noch nicht abgeschlossen sind. Standardmäßig ist dieser Teil nicht sichtbar, Sie müssen ihn also Ihrem Rollencenter hinzufügen. Weitere Informationen finden Sie unter [Ändern von Grundeinstellungen](ui-change-basic-settings.md).  

Der Teil zeigt, welche Dokumente mit Ihrer ID im Feld **Zugewiesene Benutzer-ID** verarbeitet oder in die Warteschlange gestellt werden, einschließlich solcher, die zur Hintergrundbuchung gehören. Dieser Teil informiert Sie auf einen Blick darüber, ob bei der Buchung eines Belegs ein Fehler aufgetreten ist, oder ob ein Projektwarteschlangenposten einen Fehler enthält. Mit diesem Teil können Sie auch eine Buchung stornieren, wenn diese nicht ausgeführt wird.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>So zeigen Sie einen Fehler aus dem Bereich Meine Projektwarteschlange an.
1. Bei einem Eintrag mit dem Status **Fehler** wählen Sie die Aktion **Fehler anzeigen** aus.
2. Überprüfen Sie die Fehlermeldung und korrigieren Sie das Problem.

## <a name="security"></a>Sicherheit  
Aufgabenwarteschlangenposten werden auf Basis von Berechtigungen ausgeführt. Diese Berechtigungen müssen die Ausführung des Berichts oder der Codeunit ermöglichen.  

Wenn eine Aufgabenwarteschlange manuell aktiviert wird, wird sie mit den Anmeldeinformationen des Benutzers ausgeführt. Wenn eine Aufgabenwarteschlange über NAS aktiviert wird, wird sie mit den Anmeldeinformationen der Serverinstanz ausgeführt. Wenn ein Projekt ausgeführt wird, wird es mit den Anmeldeinformationen der Aufgabenwarteschlange ausgeführt, mit der das Projekt aktiviert wird. Jedoch muss der Benutzer, der den Aufgabenwarteschlangenposten erstellt hat, auch über Berechtigungen verfügen. Wenn ein Projekt in einer Benutzersession ausgeführt wird (zum Beispiel bei der Hintergrundbuchung), wird es mit den Anmeldeinformationen des Benutzers ausgeführt, der dieses Projekt erstellt hat.  

> [!IMPORTANT]  
>  Wenn Sie den SUPER-Zugriffsrechtsatz der Demolizenz für [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, sind Sie und Ihre Benutzer zum Ausführen aller Objekte berechtigt. In diesem Fall ist der Zugriff für jeden Benutzer nur durch Berechtigungen für Daten beschränkt.  

## <a name="using-job-queues-effectively"></a>Effektive Verwendung von Aufgabenwarteschlangen  
Der Aufgabenwarteschlangenposten hat viele Felder, deren Zweck darin besteht, Parameter in die Codeunit zu übertragen, die Sie für die Ausführung mit einer Aufgabenwarteschlange festgelegt haben. Dies bedeutet auch, dass Codeunits, die über die Aufgabenwarteschlange ausgeführt werden sollen, beim Warteschlangenposten als Parameter im **OnRun**-Trigger angegeben werden müssen. Dies gewährleistet ein zusätzliches Maß an Sicherheit, da so Benutzer über die Aufgabenwarteschlange keine beliebigen Codeunits ausführen können. Wenn der Benutzer Parameter einem Bericht weiterleiten muss, besteht hierfür die einzige Möglichkeit darin, die Berichtsausführung in eine Codeunit einzubinden, die anschließend die Eingabeparameter analysiert und in den Bericht einfügt, bevor dieser ausgeführt wird.  

## <a name="see-also"></a>Siehe auch  
[Verwaltung](admin-setup-and-administration.md)  
[Einrichten von Business Central](setup.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
