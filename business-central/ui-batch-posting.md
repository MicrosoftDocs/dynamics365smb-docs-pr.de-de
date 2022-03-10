---
title: Mehrere Belege gleichzeitig buchen
description: Erfahren Sie, wie Sie mehrere nicht gebuchte Belege in einer Liste für die sofortige oder geplante Stapelbuchung in Business Central auswählen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9004, 9005, 9018, 9006, 9007, 9010, 9016, 9017
ms.reviewer: edupont
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 024588a5fcb565935a47f63a73b7287879c0db8c
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334956"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Mehrere Belege gleichzeitig buchen

Anstatt einzelne Belege einzeln zu buchen, können Sie mehrere nicht gebuchte Belege in einer Liste für die Stapelbuchung auswählen, entweder für die sofortige Buchung oder für die geplante Buchung zum Beispiel am Tagesende. Dies kann hilfreich sein, wenn nur ein Supervisor Dokumente veröffentlichen kann, die von anderen Benutzern erstellt wurden, oder um zu vermeiden, dass Systemleistungsprobleme während der Arbeitszeit veröffentlicht werden.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Mehrere Einkaufsbestellungen sofort buchen

Das folgende Verfahren erläutert, wie Sie mehrere Einkaufsbestellungen sofort buchen. Die Schritte sind für alle Einkaufs- und Verkaufsbelege ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Einkaufsbestellung** wählen Sie auf der folgenden Seite alle Bestellungen aus, die gebucht werden sollen:
3. Geben Sie im Feld **Nr.** Wählen Sie in diesem Feld die drei vertikalen Punkte aus, um das Kontextmenü zu öffnen, und wählen Sie dann die Aktion **Wählen Sie Mehr** aus.
4. Aktivieren Sie das Kontrollkästchen für alle Zeilen, die Aufträge darstellen, die Sie gleichzeitig buchen möchten.
5. Wählen Sie die zu **buchende** Aktion aus, und wählen Sie dann die Aktion **Buchen** aus.
6. Klicken Sie auf die Schaltfläche **Ja** auf der Bestätigungsnachricht.

## <a name="to-batch-post-multiple-purchase-orders"></a>Um mehrere Einkaufsbestellungen sofort zu buchen

Das folgende Verfahren erläutert, wie Sie mehrere Einkaufsbestellungen buchen. Die Schritte sind für alle Kauf- und Verkaufsbelege gleich, bei denen die Aktion **Stapelbuchung** verfügbar ist.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun") Symbol. Geben Sie **Einkaufsbestellungen** ein, und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Einkaufsbestellung** wählen Sie auf der folgenden Seite alle Bestellungen aus, die gebucht werden sollen:
3. Geben Sie im Feld **Nr.** Wählen Sie in diesem Feld die drei vertikalen Punkte aus, um das Kontextmenü zu öffnen, und wählen Sie dann die Aktion **Wählen Sie Mehr** aus.
4. Aktivieren Sie das Kontrollkästchen für alle Zeilen, die Aufträge darstellen, die Sie gleichzeitig buchen möchten.
5. Wählen Sie die zu **buchende** Aktion aus, und wählen Sie dann die Aktion **Stapelbuchung** aus.
6. Füllen Sie auf der Seite **Stapelbuchung Einkaufsbestellung** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Wählen Sie die Schaltfläche **OK** aus.
8. Um mögliche Probleme anzuzeigen, die bei der Stapelbuchung von Dokumenten aufgetreten sind, öffnen Sie die Seite **Fehlermeldungsregister**.

> [!NOTE]
> Das Buchen mehrerer Dokumente kann einige Zeit dauern und andere Benutzer blockieren. Erwägen Sie die Aktivierung der Hintergrundbuchung. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).

## <a name="to-set-up-background-posting-with-job-queues"></a>So richten Sie Hintergrundbuchung mit Projektwarteschlangen ein
Projektwarteschlangen sind ein effektives Werkzeug, um die Ausführung von Geschäftsprozessen im Hintergrund zu planen, z. B. wenn mehrere Benutzer versuchen, Verkaufsaufträge zu buchen, aber nur ein Auftrag gleichzeitig verarbeitet werden kann.  

Nachfolgend wird erklärt, wie die Hintergrundbuchung von Verkaufsaufträgen eingerichtet wird. Die Schritte sind für den Kauf ähnlich.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einrichtung Debitoren & Verkauf** ein und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Einrichtung von Vertrieb und Forderungen** aktivieren Sie das Kontrollkästchen **Mit Projektwarteschlange buchen**.
3. Wählen Sie das Feld **Projektwarteschlangen-Kategoriecode** aus und geben Sie dann den Code **SALESPOST** an.

    > [!NOTE]
    > Einige Aufträge ändern dieselben Daten und sollten nicht gleichzeitig ausgeführt werden, da dies zu Konflikten führen kann. Beispielsweise versuchen Hintergrundaufträge für Verkaufsbelege, dieselben Daten zur selben Zeit zu ändern. Auftragswarteschlangenkategorien tragen dazu bei, diese Art von Konflikten zu vermeiden, indem sichergestellt wird, dass bei der Ausführung eines Auftrags ein anderer Auftrag, der zur gleichen Auftragswarteschlangen-Kategorie gehört, erst nach Abschluss ausgeführt wird. Beispielsweise wartet ein Auftrag, der zu einer Vertriebsauftrags-Warteschlangenkategorie gehört, bis alle anderen vertriebsbezogenen Aufträge abgeschlossen sind. Sie geben eine Auftragswarteschlangenkategorie auf der Seite Inforegister **Hintergrundbuchung** auf der Seite **Vertrieb und Forderungen – Setup** ein.
    >
    > [!INCLUDE[prod_short](includes/prod_short.md)] stellt Auftragswarteschlangen-Kategorien für Vertrieb, Einkauf und Sachbuchung bereit. Es wird empfohlen, dass immer eine dieser Optionen oder eine von Ihnen erstellte angegeben wird. Wenn aufgrund von Konflikten Fehler auftreten, sollten Sie eine Kategorie für alle Verkäufe, Einkäufe und Hintergrundbuchungen in der Finanzbuchhaltung einrichten.

    Wenn zusätzlich Verkaufsbelege gedruckt werden sollen, wenn diese gebucht werden, aktivieren Sie das Kontrollkästchen **Mit Projektwarteschlange buchen und drucken** auf der Seite **Einrichtung von Vertrieb und Forderungen**.  
    Wenn Sie **PDF** in dem **Berichtausgabetyp** in diesem Feld auswählen, sind erfolgreich gebuchte Bestellungen im **Berichtseingang** Teil in Ihrem Rollencenter verfügbar.

    > [!IMPORTANT]  
    > Wenn Sie einen Beleg an einen Drucker senden und der Drucker ein Dialogfeld anzeigt, wie eine Anforderung für Anmeldeinformationen oder eine Warnung über geringe Druckertinte, wird der Beleg gebucht, aber nicht gedruckt. Die entsprechenden Aufgabenwarteschlangenposten überschreiten letztendlich die Zeit und das Feld **Status** ist auf **Fehler** festgelegt. Entsprechend empfiehlt es sich, dass Sie kein Druckersetup verwenden, das Aktivität mit der Anzeige von Druckerdialogfeldern in Verbindung mit Hintergrundbuchung benötigt.

    Wenn Sie das nächste Mal Verkaufsbelege veröffentlichen, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] automatisch einen Projektwarteschlangeneintrag für jedes Dokument und führt die Projekte nacheinander im Hintergrund aus.

4. Um sicherzustellen, dass die Aufgabenwarteschlange wie erwartet arbeitet, buchen Sie einen Verkaufsauftrag. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
    Die Verkaufsaufträge werden nun zu einem dedizierten Auftragswarteschlangeneintrag hinzugefügt, der festlegt, wann die Belege gebucht werden. 

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>So wird der Status aus einem Verkaufs- oder Einkaufsbeleg angezeigt
Wenn die Projektwarteschlange den Verkaufsauftrag nicht buchen kann, wird der Status auf **Fehler** geändert, und der Verkaufsauftrag wird der Liste von Verkaufsaufträgen hinzugefügt, die der Benutzer manuell verarbeiten muss.
1. Vom Beleg, den Sie versucht haben, mit einer Hintergrundbuchung zu buchen, wählen Sie das Feld **Projektwarteschlangenstatus** aus, das **Fehler** enthält.
2. Überprüfen Sie die Fehlermeldung und korrigieren Sie das Problem.

Alternativ können Sie auf der Seite **Projektwarteschlangen-Protokolleinträge** prüfen, ob der Verkaufsauftrag erfolgreich gebucht wurde. Weitere Informationen finden Sie im Abschnitt [Überwachen der Projektwarteschlange](#monitor-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>So wird ein Projektwarteschlangeneintrag für die Stapelbuchung von Verkaufsaufträgen erstellt

Alternativ können Sie Buchungen verschieben, wenn es für Ihre Organisation hilfreich ist. Beispielsweise kann es in Ihrem Unternehmen sinnvoll sein, bestimmte Routinen dann auszuführen, wenn ein Großteil der Dateneingaben für einen Arbeitstag abgeschlossen wurde. Sie können dies erreichen, indem Sie die Projektwarteschlange so einrichten, dass verschiedene Stapelbuchungsberichte ausgeführt werden, wie beispielsweise **Stapelbuchung von Verkaufsaufträgen**, **Stapelbuchungsverkaufsrechnungen** und ähnliche Berichte. [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt die Hintergrundbuchung für alle Verkaufs-, Einkaufs- und Servicebelege.

Der folgende Ablauf zeigt, wie Sie den Bericht **Stapelbuchung von Verkaufsaufträgen** so festlegen, dass Verkaufsaufträge automatisch an Wochentagen um 16:00 Uhr gebucht werden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Auftragswarteschlangenposten** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie im Feld **Auszuführender Objekttyp** die Option **Bericht** aus.  
4. Wählen Sie im Feld **Auszuführende Objekt-ID** 296 aus, **Stapelbuchung von Verkaufsaufträgen**.

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

5. Aktivieren Sie das Kontrollkästchen **Berichtsanforderungsseite**.
6. Auf der Anforderungsseite **Stapelbuchung von Verkaufsaufträgen** definieren Sie, was während der automatischen Buchung von Verkaufsaufträgen einbezogen wird, und wählen Sie dann die Schaltfläche **OK**.

    > [!IMPORTANT]
    > Denken Sie daran, strenge Filter festzulegen. Andernfalls bucht [!INCLUDE [prod_short](includes/prod_short.md)] alle Dokumente, selbst wenn sie noch nicht fertig sind. Ziehen Sie in Betracht, für das Feld **Status** einen Filter für den Wert *Freigegeben* zu setzen, sowie einen Filter für das Feld **Buchungsdatum** für den Wert *Heute*. Weitere Informationen finden Sie unter [Sortieren, Durchsuchen und Filtern](ui-enter-criteria-filters.md).
7. Aktivieren Sie alle Kontrollkästchen von **Montags ausführen** bis **Freitags ausführen**.
8. In dem Feld **Startzeit** geben Sie 16:00 Uhr ein.
9. Wählen Sie die Aktion **Status auf bereit festlegen** aus.

Verkaufsaufträge, die unter definierte Filter fallen, werden jetzt an jedem Wochentag um 16:00 Uhr gebucht.

## <a name="monitor-the-job-queue"></a>Überwachen der Projektwarteschlange

Wenn Sie die Hintergrundbuchung mit Projektwarteschlangen einrichten, sollten Sie die Projektwarteschlange regelmäßig überwachen, um Probleme zu erkennen. Sie können den Status auf der Seite **Projektwarteschlangeneinträge** nachverfolgen. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)  

Als Administrator können Sie [Application Insights](/azure/azure-monitor/app/app-insights-overview) zum Sammeln und Analysieren von Telemetriedaten verwenden, mit denen Sie Probleme identifizieren können. Weitere Informationen finden Sie in den Entwickler- und Verwaltungsinhalten unter [Überwachung und Analyse der Telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-overview).  

## <a name="see-also"></a>Weitere Informationen

[Dokumente und Buch.-Blatt verbuchen](ui-post-documents-journals.md)  
[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)  
[Gebuchte Belege bearbeiten](across-edit-posted-document.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Suche nach Seiten und Informationen mit Tell Me](ui-search.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]