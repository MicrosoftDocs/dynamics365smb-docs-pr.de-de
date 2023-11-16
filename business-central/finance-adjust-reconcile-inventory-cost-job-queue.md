---
title: Aufträge für die Anpassung und Abstimmung der Kalkulation des Bestands einplanen
description: 'Erfahren Sie, wie Sie die Aufgabenwarteschlange verwenden können, um die Aufgaben zum Anpassen der Lagerkosten oder zum Abstimmen der Kosten mit dem Hauptbuch in den Hintergrund zu verlagern. Angenommen, Ihr Unternehmen führt viele Aufgaben aus oder verarbeitet viele Transaktionen.'
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.form: 461
ms.date: 09/19/2023
ms.author: bholtorf
---
# <a name="schedule-jobs-to-adjust-and-reconcile-inventory-cost"></a>Planen von Aufträgen zur Anpassung und zum Abgleich der Bestandskosten

Planen Sie Jobs für die automatische Kostenanpassung mit dem Hauptbuch, die Buchung ins Hauptbuch ist standardmäßig aktiviert.
Da sich jedoch im Laufe der Zeit Daten ansammeln, kann dies die Leistung beeinträchtigen. Um die Belastung der Anwendung zu reduzieren, ist es oft hilfreich, Aufgabenwarteschlangeneinträge zu verwenden, um Aufgaben in den Hintergrund zu verschieben.

## <a name="move-the-task-of-adjusting-item-costs-to-the-background-with-the-help-of-assisted-setup"></a>Verschieben der Aufgabe der Artikelkostenanpassung mithilfe der unterstützten Einrichtung in den Hintergrund

Das Erstellen der Aufgabenwarteschlangeneinträge kann selbst für einen erfahrenen Berater schwierig sein. Daher stellen wir einen Leitfaden für die unterstützte Einrichtung bereit, um den Prozess der Anpassung der Artikelkosten zu vereinfachen.  

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol öffnet, geben Sie **Bestandseinrichtung** ein und wählen Sie dann den entsprechenden Link.  
2. Schalten Sie auf der Seite **Lagereinrichtung** das Feld **Automatische Kostenbuchung** um, oder geben Sie **Nie** im Feld **Automatische Kostenregulierung** an.  
3. Wählen Sie in der Benachrichtigung, die jetzt oben auf der Seite angezeigt wird, die Verknüpfung **Einen Projektwarteschlangenposten planen** aus. Dies öffnet die Anleitung zur unterstützten Einrichtung **Kostenanpassung und -buchung planen**.  
4. Geben Sie die Aufgabe an, die Sie planen möchten.  

  > [!NOTE]
  > Sie können keinen neuen Aufgabenwarteschlangenposten erstellen, wenn bereits ein Aufgabenwarteschlangenposten für die angegebene Aufgabe vorhanden ist.

5. Wählen Sie das Feld **Zeigt die Projektwarteschlangenposten nach Fertigstellung an** aus, um die Einstellungen zu überprüfen und anzupassen. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md).  

## <a name="to-create-a-job-queue-entry-for-adjusting-and-reconciling-inventory-cost-manually"></a>So erstellen Sie einen Aufgabenwarteschlangenposten zum manuellen Anpassen und Abgleichen der Lagerkosten

Alternativ können Sie Aufgabenwarteschlangenposten manuell erstellen. Das folgende Verfahren zeigt, wie Sie den Batchauftrag **Lagerreg. fakt. Einst. Preise** einrichten, sodass er täglich ausgeführt wird, aber die gleichen Schritte gelten für den Batchauftrag **Lagerreg. buchen**.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") aus, geben Sie **Aufgabenwarteschlangeneinträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu**.  
3. Wählen Sie im Feld **Auszuführender Objekttyp** die Option *Bericht* aus.  
4. Wählen Sie im Feld **Auszuführende Objekt-ID** die ID *795*, **Lagerreg. fakt. Einst. Preise** aus.  
5. Geben Sie im Feld **Datumsformel für nächste Ausführung** *1D* ein.
6. Geben Sie im Feld **Startzeit** *02:00 Uhr* ein.
7. Wählen Sie die Aktion **Status auf bereit festlegen** aus.

Jetzt werden die Lagerkosten jede Nacht aktualisiert.  

Um eine Aufgabe für das Abstimmen des Bestands mit dem Hauptbuch zu planen, wählen Sie Codeunit 2846 **Lagerreg. buchen** aus.

> [!TIP]
> Um Sperren zu vermeiden, planen Sie Aufträge für den Batchauftrag **Kosten anpassen – Elemente buchen**, die Codeunit **Lagerkosten ins Hauptbuch buchen** und Aufträge für die Buchung von Verkaufs- oder Einkaufstransaktionen nicht zur gleichen Zeit. Stellen Sie außerdem sicher, dass sie dieselbe Kategorie der Auftragswarteschlange verwenden.

## <a name="see-also"></a>Siehe auch

[Artikelpreise anpassen](inventory-how-adjust-item-costs.md)  
[Mit der Finanzbuchhaltung Lagerkosten melden und abstimmen](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)  
[Suche nach Seiten und Informationen mit „Sie wünschen...“](ui-search.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
