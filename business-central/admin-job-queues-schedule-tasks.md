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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5e8c611ed5d542436f470781c92d17095ecd1f5d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924578"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung

Die Aufgabenwarteschlangen in [!INCLUDE[d365fin](includes/d365fin_md.md)] ermöglichen es Benutzern, bestimmte Berichte und Codeunits zu planen und auszuführen. Die Projekte können entweder einmalig oder wiederholt ausgeführt werden. So kann es beispielsweise empfehlenswert sein, den Bericht **Verkäufer * Verkäuferstatistik** wöchentlich auszuführen, um die Verkaufserfolge eines Verkäufers zu beobachten, während die Codeunit **Genehmigungsanforderungen delegieren** täglich ausgeführt wird, um zu verhindern, dass sich Dokumente ansammeln oder anderweitig den Arbeitsablauf behindern.

Im Fenster **Projektwarteschlangeneinträge** sind alle aktuellen Aufgabenwarteschlangenposten aufgelistet. Wenn Sie eine neue Projektwarteschlange hinzufügen, die Sie planen möchten, müssen Sie die Informationen über die Art des Objekts, das Sie ausführen möchten, angeben, wie der Name und die Objekt-ID, die Sie ausführen möchten. Sie können auch Parameter hinzufügen, um das Verhalten eines Aufgabenwarteschlangenpostens festzulegen. So können Sie beispielsweise einen Parameter hinzufügen, um nur gebuchte Verkaufsaufträge zu senden. Sie benötigen die entsprechende Berechtigung zum Ausführen des jeweiligen Berichts oder der jeweiligen Codeunit, da ansonsten beim Ausführen der Projektwarteschlange ein Fehler auftritt.  

Eine Aufgabenwarteschlange kann mehrere Posten haben. Diese stellen die Projekte dar, die die Warteschlange verwaltet und ausführt. Informationen in dem Posten geben an, welche Codeunit oder welcher Bericht ausgeführt wird, wann und wie häufig der Posten ausgeführt wird, in welcher Kategorie das Projekt ausgeführt wird, und wie es ausgeführt wird.  

## <a name="to-set-up-background-posting-with-job-queues"></a>So richten Sie Hintergrundbuchung mit Projektwarteschlangen ein

Projektwarteschlangen sind ein effektives Werkzeug, um die Ausführung von Geschäftsprozessen im Hintergrund zu planen, z. B. wenn mehrere Benutzer versuchen, Verkaufsaufträge zu buchen, aber nur ein Auftrag gleichzeitig verarbeitet werden kann.  

Nachfolgend wird erklärt, wie die Hintergrundbuchung von Verkaufsaufträgen eingerichtet wird. Die Schritte sind für den Kauf ähnlich.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Einrichten von Verkauf und Forderungen** ein, und wählen Sie dann den zugehörigen Link aus.
2. Auf der Seite **Einrichtung von Vertrieb und Forderungen** aktivieren Sie das Kontrollkästchen **Mit Projektwarteschlange buchen** .
3. Wählen Sie das Feld **Projektwarteschlangen-Kategoriecode** aus und geben Sie dann den Code **SALESPOST** an.

    > [!NOTE]
    > Einige Aufträge ändern dieselben Daten und sollten nicht gleichzeitig ausgeführt werden, da dies zu Konflikten führen kann. Beispielsweise versuchen Hintergrundaufträge für Verkaufsbelege, dieselben Daten zur selben Zeit zu ändern. Auftragswarteschlangenkategorien tragen dazu bei, diese Art von Konflikten zu vermeiden, indem sichergestellt wird, dass bei der Ausführung eines Auftrags ein anderer Auftrag, der zur gleichen Auftragswarteschlangen-Kategorie gehört, erst nach Abschluss ausgeführt wird. Beispielsweise wartet ein Auftrag, der zu einer Vertriebsauftrags-Warteschlangenkategorie gehört, bis alle anderen vertriebsbezogenen Aufträge abgeschlossen sind. Sie geben eine Auftragswarteschlangenkategorie auf der Seite Inforegister **Hintergrundbuchung** auf der Seite **Vertrieb und Forderungen – Setup** ein.
    >
    > [!INCLUDE[d365fin](includes/d365fin_md.md)] stellt Auftragswarteschlangen-Kategorien für Vertrieb, Einkauf und Sachbuchung bereit. Es wird empfohlen, dass immer eine dieser Optionen oder eine von Ihnen erstellte angegeben wird. Wenn aufgrund von Konflikten Fehler auftreten, sollten Sie eine Kategorie für alle Verkäufe, Einkäufe und Hintergrundbuchungen in der Finanzbuchhaltung einrichten.

    Wenn zusätzlich Verkaufsbelege gedruckt werden sollen, wenn diese gebucht werden, aktivieren Sie das Kontrollkästchen **Mit Projektwarteschlange buchen und drucken** auf der Seite **Einrichtung von Vertrieb und Forderungen** .  

    > [!IMPORTANT]  
    > Wenn Sie einen Beleg an einen Drucker senden und der Drucker ein Dialogfeld anzeigt, wie eine Anforderung für Anmeldeinformationen oder eine Warnung über geringe Druckertinte, wird der Beleg gebucht, aber nicht gedruckt. Die entsprechenden Aufgabenwarteschlangenposten überschreiten letztendlich die Zeit und das Feld **Status** ist auf **Fehler** festgelegt. Entsprechend empfiehlt es sich, dass Sie kein Druckersetup verwenden, das Aktivität mit der Anzeige von Druckerdialogfeldern in Verbindung mit Hintergrundbuchung benötigt.

    Wenn Sie das nächste Mal Verkaufsbelege veröffentlichen, erstellt [!INCLUDE [prodshort](includes/prodshort.md)] automatisch einen Projektwarteschlangeneintrag für jedes Dokument und führt die Projekte nacheinander im Hintergrund aus.

4. Um sicherzustellen, dass die Aufgabenwarteschlange wie erwartet arbeitet, buchen Sie einen Verkaufsauftrag. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)

5. Überprüfen Sie auf der Seite **Projektwarteschlangen-Protokolleinträge** , ob der Verkaufsauftrag erfolgreich gebucht wurde. Weitere Informationen finden Sie unter [So wird der Status oder Fehler in der Projektwarteschlange angezeigt](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>So wird ein Projektwarteschlangeneintrag für die Stapelbuchung von Verkaufsaufträgen erstellt

Alternativ können Sie Buchungen verschieben, wenn es für Ihre Organisation hilfreich ist. Beispielsweise kann es in Ihrem Unternehmen sinnvoll sein, bestimmte Routinen dann auszuführen, wenn ein Großteil der Dateneingaben für einen Arbeitstag abgeschlossen wurde. Sie können dies erreichen, indem Sie die Projektwarteschlange so einrichten, dass verschiedene Stapelbuchungsberichte ausgeführt werden, wie beispielsweise **Stapelbuchung von Verkaufsaufträgen** , **Stapelbuchungsverkaufsrechnungen** und ähnliche Berichte. [!INCLUDE[d365fin](includes/d365fin_md.md)] unterstützt die Hintergrundbuchung für alle Verkaufs-, Einkaufs- und Servicebelege.

Der folgende Ablauf zeigt, wie Sie den Bericht **Stapelbuchung von Verkaufsaufträgen** so festlegen, dass Verkaufsaufträge automatisch an Wochentagen um 16:00 Uhr gebucht werden.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Aufgabenwarteschlangeneinträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie im Feld **Auszuführender Objekttyp** die Option **Bericht** aus.  
4. Wählen Sie im Feld **Auszuführende Objekt-ID** 296 aus, **Stapelbuchung von Verkaufsaufträgen** .

   Sie können auch folgende Berichte verwenden:
  
   * 900 **Montageaufträge stapelbuchen**
   * 497 **Eink. Rechnungen stapelbuchen**
   * 496 **Bestellungen stapelbuchen**
   * 498 **Eink.Gutschriften stapelbuchen**
   * 6665 **Eink.-Rekl. stapelbuchen**
   * 298 **Stapelbuchungsverkaufs-Gutschriften**
   * 297 **Stapelbuchungsverkaufsrechnungen**
   * 296 **Stapelbuchung von Verkaufsaufträgen**
   * 6655 **Stapelbuchungsverkaufsrechnungen**
   * 6005 **Servicegutschriften stapelbuchen**
   * 6004 **Servicerechnungen stapelbuchen**
   * 6001 **Serviceaufträge stapelbuchen**

5. Aktivieren Sie das Kontrollkästchen **Berichtsanforderungsseite** .
6. Auf der Anforderungsseite **Stapelbuchung von Verkaufsaufträgen** definieren Sie, was während der automatischen Buchung von Verkaufsaufträgen einbezogen wird, und wählen Sie dann die Schaltfläche **OK** .

    > [!IMPORTANT]
    > Denken Sie daran, strenge Filter festzulegen. Andernfalls bucht [!INCLUDE [prodshort](includes/prodshort.md)] alle Dokumente, selbst wenn sie noch nicht fertig sind. Ziehen Sie in Betracht, für das Feld **Status** einen Filter für den Wert *Freigegeben* zu setzen, sowie einen Filter für das Feld **Buchungsdatum** für den Wert *Heute* . Weitere Informationen finden Sie unter [Sortieren, Durchsuchen und Filtern](ui-enter-criteria-filters.md).
7. Aktivieren Sie alle Kontrollkästchen von **Montags ausführen** bis **Freitags ausführen** .
8. In dem Feld **Startzeit** geben Sie 16:00 Uhr ein.
9. Wählen Sie die Aktion **Status auf bereit festlegen** aus.

Verkaufsaufträge, die unter definierte Filter fallen, werden jetzt an jedem Wochentag um 16:00 Uhr gebucht.

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
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Aufgabenwarteschlangeneinträge** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Projektwarteschlangeneinträge** wählen Sie einen Projektwarteschlangeneintrag aus, und wählen die dann die Aktion **Protokolleinträge** aus.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>So wird der Status aus einem Verkaufs- oder Einkaufsbeleg angezeigt
1. Vom Beleg, den Sie versucht haben, mit einer Hintergrundbuchung zu buchen, wählen Sie das Feld **Projektwarteschlangenstatus** aus, das **Fehler** enthält.
2. Überprüfen Sie die Fehlermeldung und korrigieren Sie das Problem.

## <a name="the-my-job-queue-part"></a>Der „Mein Projektwarteschlangenteil“
Der Teil **Meine Projektwarteschlange** in Ihrem Rollencenter zeigt die Projektwarteschlangeneinträge an, die Sie gestartet haben, die jedoch noch nicht abgeschlossen sind. Standardmäßig ist dieser Teil nicht sichtbar, Sie müssen ihn also Ihrem Rollencenter hinzufügen. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).  

Der Teil zeigt, welche Dokumente mit Ihrer ID im Feld **Zugewiesene Benutzer-ID** verarbeitet oder in die Warteschlange gestellt werden, einschließlich solcher, die zur Hintergrundbuchung gehören. Dieser Teil informiert Sie auf einen Blick darüber, ob bei der Buchung eines Belegs ein Fehler aufgetreten ist, oder ob ein Projektwarteschlangenposten einen Fehler enthält. Mit diesem Teil können Sie auch eine Buchung stornieren, wenn diese nicht ausgeführt wird.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>So zeigen Sie einen Fehler aus dem Bereich Meine Projektwarteschlange an.
1. Bei einem Eintrag mit dem Status **Fehler** wählen Sie die Aktion **Fehler anzeigen** aus.
2. Überprüfen Sie die Fehlermeldung und korrigieren Sie das Problem.

## <a name="security"></a>Sicherheit  
Aufgabenwarteschlangenposten werden auf Basis von Berechtigungen ausgeführt. Diese Berechtigungen müssen die Ausführung des Berichts oder der Codeunit ermöglichen.  

Wenn eine Aufgabenwarteschlange manuell aktiviert wird, wird sie mit den Anmeldeinformationen des Benutzers ausgeführt. Wenn eine Aufgabenwarteschlange über NAS aktiviert wird, wird sie mit den Anmeldeinformationen der Serverinstanz ausgeführt. Wenn ein Projekt ausgeführt wird, wird es mit den Anmeldeinformationen der Aufgabenwarteschlange ausgeführt, mit der das Projekt aktiviert wird. Jedoch muss der Benutzer, der den Aufgabenwarteschlangenposten erstellt hat, auch über Berechtigungen verfügen. Wenn ein Projekt in einer Benutzersession ausgeführt wird (zum Beispiel bei der Hintergrundbuchung), wird es mit den Anmeldeinformationen des Benutzers ausgeführt, der dieses Projekt erstellt hat.  

> [!IMPORTANT]  
> Wenn Sie den SUPER-Zugriffsrechtsatz der Demolizenz für [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, sind Sie und Ihre Benutzer zum Ausführen aller Objekte berechtigt. In diesem Fall ist der Zugriff für jeden Benutzer nur durch Berechtigungen für Daten beschränkt.  

## <a name="using-job-queues-effectively"></a>Effektive Verwendung von Aufgabenwarteschlangen  
Der Aufgabenwarteschlangenposten hat viele Felder, deren Zweck darin besteht, Parameter in die Codeunit zu übertragen, die Sie für die Ausführung mit einer Aufgabenwarteschlange festgelegt haben. Dies bedeutet auch, dass Codeunits, die über die Aufgabenwarteschlange ausgeführt werden sollen, beim Warteschlangenposten als Parameter im **OnRun** -Trigger angegeben werden müssen. Dies gewährleistet ein zusätzliches Maß an Sicherheit, da so Benutzer über die Aufgabenwarteschlange keine beliebigen Codeunits ausführen können. Wenn der Benutzer Parameter einem Bericht weiterleiten muss, besteht hierfür die einzige Möglichkeit darin, die Berichtsausführung in eine Codeunit einzubinden, die anschließend die Eingabeparameter analysiert und in den Bericht einfügt, bevor dieser ausgeführt wird.  

## <a name="scheduling-synchronization-between-d365fin-and-d365fin"></a>Synchronisierung planen zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[d365fin](includes/cds_long_md.md)]

Wenn Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] in [!INCLUDE[d365fin](includes/cds_long_md.md)] integriert haben, können Sie die Projektwarteschlange verwenden, um zu planen, wann Sie Daten für die Datensätze synchronisieren möchten, die Sie in den beiden Geschäftsanwendungen gekoppelt haben. Abhängig von der Richtung und den Regeln, die Sie für die Integration definiert haben, können die Synchronisationsaufträge auch neue Datensätze in der Ziel-App erstellen, die denen in der Quelle entsprechen. Zum Beispiel, wenn ein Verkäufer einen neuen Kontakt in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt, kann der Synchronisierungsauftrag diesen Kontakt für den gekoppelten Verkäufer in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen. Weitere Informationen finden Sie unter [Planen einer Synchronisierung zwischen Business Central und Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

## <a name="see-also"></a>Siehe auch

[Verwaltung](admin-setup-and-administration.md)  
[Einrichten von Business Central](setup.md)  
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
