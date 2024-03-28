---
title: Datensatz-Verbrauch oder -Verwendung von Job-Ressourcen und Elementen
description: 'Dieser Artikel beschreibt, wie der Verbrauch oder die Verwendung von Artikeln oder Ressourcen für Projekte in Projektmanagement erfasst werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
---
# <a name="record-consumption-or-usage-for-jobs"></a>Datensatz-Verbrauch oder -Verwendung für Jobs aufzeichnen

Auf der Seite **Auftragskarte** können Sie die Seite **Projektplanzeilen** öffnen, um die Nutzung verschiedener Teile Ihres Projekts zu überprüfen und zu erfassen. Diese Informationen werden automatisch aktualisiert, wenn Sie Informationen zwischen Projekten und Projekt-Buch.-Blättern oder Projektrechnungen ändern und übertragen. Dazu ist es erforderlich, dass Sie den Schalter **Link Verbrauch standardmäßig anwenden** auf der Seite **Projekteinrichtung** aktiviert ist. Erfahren Sie mehr unter [Projekte einrichten](projects-how-setup-jobs.md).  

Zum Beispiel können Sie für Planungszeilen der Art **Plan** die Menge einer Ressource eingeben und dann die Menge angeben, die in das Projektbuchungsblatt umgelagert wird. Wenn die Art der Planungszeile **Fakturierbar** ist, können Sie die Menge einer Ressource eingeben und dann die Menge angeben, die in das Projektbuchungsblatt umgelagert wird. Weitere Informationen zur Rechnungsstellung an den Debitor finden Sie unter [Projekte fakturieren](projects-how-invoice-jobs.md). Durch den Vergleich der ursprünglichen Menge, der verbleibenden Menge oder der gebuchten Menge können Sie die Verbrauchsinformationen schnell überprüfen. Weitere Informationen zur Einschätzung der geplante Werte bei der Planung, finden Sie unter [Verwalten von Projektbudgets](projects-how-manage-budgets.md)  

Die folgenden Verfahren beschreiben, wie Sie tatsächliche (budgetierte) Mengen und Kosten mit eiem Projekt-Buch.-Blatt erfassen. Alternativ können Sie auch Einkaufsbelege verwenden, um Einkäufe für eine Projekt zu erfassen. Weitere Informationen finden Sie unter [Verwalten von Projektlieferungen](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-job-planning-line-of-type-budget"></a>Den Verbrauch in einer Projektplanungszeile der Art "Plan"erfassen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Markieren Sie das Projekt und wählen Sie dann die Aktion **Projektplanzeilen**. 
3. Wählen Sie eine Projektplanungszeile der Art **Plan** aus oder geben Sie **Plan und Fakturierbar** ein, für die Sie den Verbrauch buchen möchten.   

    > [!NOTE]
    > Sie können den Datensatz auch für eine Auftragsplanungszeile vom Typ **Abrechnungsfähig** verwenden. Normalerweise verwenden Sie diese Zeile, um Rechnungen zu erstellen, aber Sie können die Informationen auch in eine Erfassung übertragen. Erfahren Sie mehr unter [Fakturieren von Projekten](projects-how-invoice-jobs.md) 

4. Geben Sie im Feld **In das Journal zu übertragende Menge** die zu umzulagernde Menge ein. Der Standardwert ist der Wert, den Sie im Feld **Menge** angegeben haben.

    Das Feld **Restmenge** zeigt die Menge an, die verbleibt, um das Projekt abzuschließen und in das Buch.-Blatt umzulagern.
5. Wählen Sie die Aktion **Buch.-Blattzeilen erstellen** aus.

    > [!TIP]
    > Wenn Sie weitere Projektplanzeilen für dieses Projekt hinzufügen möchten, warten Sie mit diesem Schritt, bis Sie alle Projektplanzeilen hinzugefügt haben.
6. Auf der Seite **Projekt auf Projektplanung übertragen** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Wählen Sie die Aktion **Buch.-Blatt öffnen** aus.  
8. Auf der Seite **Projekt Buch,-Blatt** wählen Sie die entsprechende Zeile und wählen die Aktion **Buchen** aus.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. Auf der Seite **Projektplanungszeilen** überprüfen Sie den erfassten Verbrauch, indem Sie die Felder **Menge**, **Restmenge** und **Auf Buch.-Blatt zu übertragende Menge** kontrollieren.  
10. Um zusätzlichen Verbrauch zu erfassen, wiederholen Sie die Schritte 3 bis 8.  

## <a name="to-create-job-journal-lines-manually"></a>Projekt-Buchungsblattzeilen manuell erstellen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Projekt Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Feld **Stapelverarbeitungsname** einen entsprechenden Projekt-Buchungsblattnamen aus.  
3. Geben Sie in einer neuen Zeile die Belegnummer, Projektnummer, Projektaufgabennummer und die Art und Menge des verbrauchten Typs ein.  
4. Wenn die Projekt-Buch.-Blattzeilen vollständig sind, wählen Sie die Aktion **Buchen** aus.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-job-usage-estimates-and-post-updates"></a>So zeigen Sie Projektverbrauchschätzungen und Buchungsaktualisierungen an.

Der Projektverbrauch kann bis zum Projektabschluss in einem einzigen Schritt angezeigt werden. Verwenden Sie hierzu die Stapelverarbeitung **Restverbrauch für Projekt berechnen** für alle Aufgaben bis zum Projektende (einschließlich).  

Auf diese Weise können Sie die ursprüngliche Planung mit den tatsächlichen Ergebnissen vergleichen und ggf. Änderungen vornehmen oder neue Posten hinzufügen. Beispiel: Sie haben für ein Projekt eine Dauer von zehn Stunden geplant, aktueller Stand sind jedoch 15 Stunden. Sie können die fünf zusätzlichen Stunden entweder der bestehenden Buch.-Blattzeile hinzufügen oder eine neue Buch.-Blattzeile erstellen, um die fünf Stunden als Überstunden (anderer Arbeitstyp) zu melden. Die angemessenen Kosten und der Preis werden berechnet und dann können Sie sie in das Protokoll buchen.  

> [!NOTE]  
> Artikeleinträge erstellen Artikelposten und reduzieren die Lagerbestandmenge. Durch die Stapelverarbeitung **Lagerregulierung buchen** werden die Kosten aus dem Lagerbestand in die Finanzbuchhaltung gebucht. Aus Posten für Ressourcen werden Ressourcenposten erstellt.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Projekt Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie ein Buch.-Blatt des entsprechenden Projekts, und wählen Sie dann die Aktion **Verbleibender Verbrauch berechnen** aus.  
3. Geben Sie auf der Seite **Restverbrauch für Projekt berechnen** die Belegnummer und das Buchungsdatum ein, das in das Buch.-Blatt eingefügt werden soll und wählen Sie dann die Schaltfläche **OK**.  
4. Aktualisieren Sie das Buch.-Blatt mit sämtlichen Änderungen, die möglicherweise erforderlich sind.  
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-job"></a>Belege für Bestand und Lagerkommissionierungen für einen Auftrag erstellen

Um Bestands- und Lagerkommissionierungsbelege für Aufträge zu erstellen, muss Ihr Administrator die Funktion **Funktion Aktualisieren: Lagerbestand und Lagerkommissionierungen von Aufträgen aus aktivieren** auf der Seite **Funktionsverwaltung** aktivieren.

Die Funktion erstellt die Aktionen **Lagerkommissionierung erstellen** und **Lagerkommissionierungen erstellen** auf der **Jobkarte**. Um einen Beleg für eine Kommissionierung zu erstellen oder zu registrieren, verwenden Sie die Aktionen **Kommissionierlinien/Bewegungslinien** oder **Registrierte Kommissionierlinien**. Weitere Informationen finden Sie unter [Designdetails – Abläufe für Fertigung, Montage und Aufträge](design-details-internal-warehouse-flows.md).

Sie können die Aktionen unter den folgenden Bedingungen verwenden:

* Der **Status** des Auftrags ist **Offen**.
* Die **Zeilenart** der Auftragsplanungszeile ist **Budget** oder **Budget und abrechenbar**.
* Der **Typ** der Auftragsplanungszeile ist **Artikel**.
* **Kommissionieren erforderlich** ist für den entsprechenden Ort aktiviert.
* **Gerichtetes Kommissionieren und Einlagern** ist deaktiviert.

> [!NOTE] 
> Obwohl die Einstellung **Kommissionierung vorschreiben** heißt, können Sie den Verbrauch trotzdem direkt aus der Buchungsblattzeile für den Standort kommissionieren. Wenn Ihr Standort so festgelegt ist, dass eine Kommissionierung, aber keine Versandverarbeitung erforderlich ist, verwenden Sie die Seite **Lagerkommissionierung**, um die Kommissionierungsinformationen zu organisieren und zu drucken. Sie verwenden die Seite auch, um das Ergebnis der Kommissionierung einzugeben und zu verbuchen, was wiederum den Verbrauch der Artikel verbucht. 
> 
> Wenn Ihr Standort so festgelegt ist, dass sowohl die Kommissionierung als auch die Verarbeitung von Sendungen erforderlich ist, d.h. wenn Sie auf der Seite **Standortkarte** sowohl das Feld **Kommissionierung anfordern** als auch das Feld **Sendung anfordern** ausgewählt haben, verwenden Sie die Seite **Lager-Kommissionierung**, um die Kommissionierung zu bearbeiten. Lagerkommissionierungen sind ähnlich wie Bestandskommissionierungen. Der Unterschied besteht darin, dass Sie die Kommissionierung registrieren, anstatt die Kommissionierungsinformationen zu buchen. Mit dieser Registrierung wird kein Verbrauch gebucht, sondern die Artikel werden lediglich für die Buchung verfügbar gemacht. Als Manager eines Lagers können Sie ein Kommissionierarbeitsblatt verwenden, um die Kommissionierinformationen zu organisieren, bevor Sie die einzelnen Anweisungen für die Kommissionierung im Lager erstellen.

## <a name="to-review-planning-lines-for-a-job-ledger-entry"></a>Um Planungszeilen für einen Projektposten zu überprüfen

Nachdem Sie die Projekt-Planungszeilen gebucht haben, können Sie die gebuchten Projekt-Buchungszeilen sehen, die dem Projekt-Buchungsblatt zugeordnet sind.

> [!NOTE]  
> Dies setzt voraus, dass das Kontrollkästchen **Verwendungslink anwenden** für den Job aktiviert wurde. Weitere Informationen finden Sie unter [Jobs festlegen](projects-how-setup-jobs.md).  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projekt Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie ein Buch.-Blatt des entsprechenden Projekts aus, und wählen Sie dann die Aktion **Projektposten** aus.  
3. Auf der Seite **Projektposteneinträge** wählen Sie die Aktion **Anzeigen verknüpfter Projektplanungszeilen** aus.

## <a name="see-also"></a>Siehe auch

[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
