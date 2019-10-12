---
title: So senden Sie mehrere Dokumente gleichzeitig | Microsoft Docs
description: Anstatt einzelne Belege einzeln zu buchen, können Sie mehrere nicht gebuchte Belege in einer Liste für die Stapelbuchung auswählen, entweder für die sofortige Buchung oder für die geplante Buchung zum Beispiel bis zum Tagesende.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 15b0afcf04ad279000de227523f977fdb695fe01
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316787"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Mehrere Dokumente gleichzeitig buchen
Anstatt einzelne Belege einzeln zu buchen, können Sie mehrere nicht gebuchte Belege in einer Liste für die Stapelbuchung auswählen, entweder für die sofortige Buchung oder für die geplante Buchung zum Beispiel am Tagesende. Dies kann hilfreich sein, wenn nur ein Supervisor Dokumente veröffentlichen kann, die von anderen Benutzern erstellt wurden, oder um zu vermeiden, dass Systemleistungsprobleme während der Arbeitszeit veröffentlicht werden.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Mehrere Einkaufsbestellungen sofort buchen
Das folgende Verfahren erläutert, wie Sie mehrere Einkaufsbestellungen sofort buchen. Die Schritte sind für alle Einkaufs- und Verkaufsbelege ähnlich.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufaufträge** ein, und wählen dann den zugehörigen Link aus.
2. Auf der Seite **Einkaufsbestellung** wählen Sie auf der folgenden Seite alle Bestellungen aus, die gebucht werden sollen:
3. Geben Sie im Feld **Nr.** Wählen Sie in diesem Feld die drei vertikalen Punkte aus, um das Kontextmenü zu öffnen, und wählen Sie dann die Aktion **Wählen Sie Mehr** aus.
4. Aktivieren Sie das Kontrollkästchen für alle Zeilen, die Aufträge darstellen, die Sie gleichzeitig buchen möchten.
5. Wählen Sie die zu **buchende** Aktion aus, und wählen Sie dann die Aktion **Buchen** aus.
6. Klicken Sie auf die Schaltfläche **Ja** auf der Bestätigungsnachricht.

## <a name="to-batch-post-multiple-purchase-orders"></a>Um mehrere Einkaufsbestellungen sofort zu buchen
Das folgende Verfahren erläutert, wie Sie mehrere Einkaufsbestellungen buchen. Die Schritte sind für alle Kauf- und Verkaufsbelege gleich, bei denen die Aktion **Stapelbuchung** verfügbar ist.

> [!NOTE]
> Die Stapelverbuchung von Dokumenten erfolgt im Hintergrund, wie durch einen Jobwarteschlangeneintrag definiert, der zuerst eingerichtet werden muss. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufaufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Auf der Seite **Einkaufsbestellung** wählen Sie auf der folgenden Seite alle Bestellungen aus, die gebucht werden sollen:
3. Geben Sie im Feld **Nr.** Wählen Sie in diesem Feld die drei vertikalen Punkte aus, um das Kontextmenü zu öffnen, und wählen Sie dann die Aktion **Wählen Sie Mehr** aus.
4. Aktivieren Sie das Kontrollkästchen für alle Zeilen, die Aufträge darstellen, die Sie gleichzeitig buchen möchten.
5. Wählen Sie die zu **buchende** Aktion aus, und wählen Sie dann die Aktion **Stapelbuchung** aus.
6. Füllen Sie auf der Seite **Stapelbuchung Einkaufsbestellung** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Um zugehörige Berichte beim Buchen zu drucken, wie die **Bestellbestätigung** wählen Sie für Kundenaufträge das Kontrollkästchen **Drucken** aus.<br /><br /> In dem Feld **Berichtausgabetyp** auf der Seite **Vertriebs- und Forderungseinrichtung** oder der Seite **Einrichten von Einkäufen und Verbindlichkeiten** legen Sie fest, ob der Bericht gedruckt oder als PDF ausgegeben werden soll.<br /><br /> Beachten Sie auch, dass das direkte Drucken auf einem ausgewählten Drucker nur in lokalen Installationen möglich ist.

7. Wählen Sie die Schaltfläche **OK** aus.
8. Um mögliche Probleme anzuzeigen, die bei der Stapelbuchung von Dokumenten aufgetreten sind, öffnen Sie die Seite **Fehlermeldungsregister**.

Die Bestellungen werden nun zu einem dedizierten Auftragswarteschlangeneintrag hinzugefügt, der festlegt, wann die Belege gebucht werden. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)

Wenn Sie **PDF** in dem **Berichtausgabetyp** in diesem Feld auswählen, sind erfolgreich gebuchte Bestellungen im **Berichtseingang** Teil in Ihrem Rollencenter verfügbar.

## <a name="see-also"></a>Siehe auch
[Journale und Dokumente buchen](ui-post-documents-journals.md)  
[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)  
[Gebuchte Belege bearbeiten](across-edit-posted-document.md)  
[Ändern oder Löschen einer unbezahlten Einkaufsrechnung](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Suchen von Seiten und Informationen mit Wie möchten Sie weiter verfahren](ui-search.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
