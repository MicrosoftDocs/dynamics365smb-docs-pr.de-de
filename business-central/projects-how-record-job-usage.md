---
title: Datensatz-Verbrauch oder -Verwendung von Projektressourcen und -artikeln
description: 'Dieser Artikel beschreibt, wie der Verbrauch oder die Verwendung von Artikeln oder Ressourcen für Projekte in Projektmanagement erfasst werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 02/22/2024
ms.custom: bap-template
---
# <a name="record-consumption-or-usage-for-projects"></a>Verbrauch oder Nutzung für Projekt erfassen

Auf der Seite **Projektkarte** können Sie die Seite **Projektplanzeilen** öffnen, um die Nutzung verschiedener Teile Ihres Projekts zu überprüfen und zu erfassen. Diese Informationen werden automatisch aktualisiert, wenn Sie Informationen zwischen Projekten und Projekt-Buch.-Blättern oder Projektrechnungen ändern und übertragen. Dazu ist es erforderlich, dass Sie den Schalter **Link Verbrauch standardmäßig anwenden** auf der Seite **Projekteinrichtung** aktiviert ist. Erfahren Sie mehr unter [Projekte einrichten](projects-how-setup-jobs.md).  

Zum Beispiel können Sie für Planungszeilen der Art **Budget** die Menge einer Ressource eingeben und dann die Menge angeben, die in die Projekterfassung umgelagert wird. Wenn die Art der Planungszeile **Fakturierbar** ist, können Sie die Menge einer Ressource eingeben und dann die Menge angeben, die in das Projektbuchungsblatt umgelagert wird. Weitere Informationen zur Rechnungsstellung an den Debitor finden Sie unter [Projekte fakturieren](projects-how-invoice-jobs.md). Durch den Vergleich der ursprünglichen Menge, der verbleibenden Menge oder der gebuchten Menge können Sie die Verbrauchsinformationen schnell überprüfen. Weitere Informationen zur Einschätzung der geplante Werte bei der Planung, finden Sie unter [Verwalten von Projektbudgets](projects-how-manage-budgets.md)  

Die folgenden Verfahren beschreiben, wie Sie tatsächliche (budgetierte) Mengen und Kosten mit einer Projekterfassung aufzeichnen. Alternativ können Sie auch Einkaufsbelege verwenden, um Einkäufe für ein Projekt zu erfassen. Weitere Informationen finden Sie unter [Verwalten von Projektlieferungen](projects-how-manage-project-supplies.md).

## <a name="to-record-usage-for-a-project-planning-line-of-type-budget"></a>Den Verbrauch in einer Projektplanungszeile der Art „Budget“ erfassen

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") und geben Sie **Projekte** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie das Projekt und dann die Aktion **Projektplanzeilen** aus. 
3. Wählen Sie eine Projektplanungszeile der Art **Budget** aus oder geben Sie **Budgetiert und verrechenbar** ein, für die Sie den Verbrauch buchen möchten.   

    > [!NOTE]
    > Sie können den Datensatz auch für eine Projektplanungszeile vom Typ **Fakturierbar** verwenden. Normalerweise verwenden Sie diese Zeile, um Rechnungen zu erstellen, aber Sie können die Informationen auch in eine Erfassung übertragen. Erfahren Sie mehr unter [Projekte fakturieren](projects-how-invoice-jobs.md) 

4. Geben Sie im Feld **In das Journal zu übertragende Menge** die zu umzulagernde Menge ein. Der Standardwert ist der Wert, den Sie im Feld **Menge** angegeben haben.

    Das Feld **Restmenge** zeigt die Menge an, die verbleibt, um das Projekt abzuschließen und in das Buch.-Blatt umzulagern.
5. Wählen Sie die Aktion **Projekt-Buchungsblattzeilen erstellen** aus.

    > [!TIP]
    > Wenn Sie weitere Projektplanzeilen für dieses Projekt hinzufügen möchten, warten Sie mit diesem Schritt, bis Sie alle Projektplanzeilen hinzugefügt haben.
6. Auf der Seite **Projektumlagerung-Projektplanzeile** geben Sie die Felder wie nötig ein, und wählen Sie dann die Schaltfläche **OK** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Wählen Sie die Aktion **Projekterfassung öffnen** aus.  
8. Auf der Seite **Projekterfassung** wählen Sie die entsprechende Zeile und die Aktion **Buchen** aus.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

9. Auf der Seite **Projektplanungszeilen** überprüfen Sie den erfassten Verbrauch, indem Sie die Felder **Menge**, **Restmenge** und **Auf Buch.-Blatt zu übertragende Menge** kontrollieren.  
10. Um zusätzlichen Verbrauch zu erfassen, wiederholen Sie die Schritte 3 bis 8.  

## <a name="to-create-project-journal-lines-manually"></a>Projekt-Buchungsblattzeilen manuell erstellen

1. Wählen Sie das ![Glühbirne, welche die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Projekterfassungen** ein und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie im Feld **Stapelverarbeitungsname** einen entsprechenden Projekt-Buchungsblattnamen aus.  
3. Geben Sie in einer neuen Zeile die Belegnummer, Projektnummer, Projektaufgabennummer und die Art und Menge des verbrauchten Typs ein.  
4. Wenn die Projekt-Buchungsblattzeilen vollständig sind, wählen Sie die Aktion **Buchen** aus.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-view-project-usage-estimates-and-post-updates"></a>So zeigen Sie Projektverbrauchschätzungen und Buchungsaktualisierungen an

Der Projektverbrauch kann bis zum Projektabschluss in einem einzigen Schritt angezeigt werden. Verwenden Sie hierzu die Stapelverarbeitung **Restverbrauch für Projekt berechnen** für alle Aufgaben bis zum Projektende (einschließlich).  

Auf diese Weise können Sie die ursprüngliche Planung mit den tatsächlichen Ergebnissen vergleichen und ggf. Änderungen vornehmen oder neue Posten hinzufügen. Beispiel: Sie haben für ein Projekt eine Dauer von zehn Stunden geplant, aktueller Stand sind jedoch 15 Stunden. Sie können die fünf zusätzlichen Stunden entweder der bestehenden Buch.-Blattzeile hinzufügen oder eine neue Buch.-Blattzeile erstellen, um die fünf Stunden als Überstunden (anderer Arbeitstyp) zu melden. Die angemessenen Kosten und der Preis werden berechnet und dann können Sie sie in das Protokoll buchen.  

> [!NOTE]  
> Artikeleinträge erstellen Artikelposten und reduzieren die Lagerbestandmenge. Durch die Stapelverarbeitung **Lagerregulierung buchen** werden die Kosten aus dem Lagerbestand in die Finanzbuchhaltung gebucht. Aus Posten für Ressourcen werden Ressourcenposten erstellt.  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Projekterfassungen** ein und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie ein Buch.-Blatt des entsprechenden Projekts und dann die Aktion **Verbleibender Verbrauch berechnen** aus.  
3. Geben Sie auf der Seite **Restverbrauch für Projekt berechnen** die Belegnummer und das Buchungsdatum ein, das in das Buch.-Blatt eingefügt werden soll und wählen Sie dann die Schaltfläche **OK** aus.  
4. Aktualisieren Sie das Buch.-Blatt mit sämtlichen Änderungen, die möglicherweise erforderlich sind.  
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="create-inventory-and-warehouse-pick-documents-for-a-project"></a>Belege für Bestand und Lagerkommissionierungen für ein Projekt erstellen

Verwenden Sie die Aktionen **Lagerkommissionierung erstellen** und **Lagerkommissionierungen erstellen** auf der Seite **Projektkarte**. Um einen Beleg für eine Kommissionierung zu erstellen oder zu registrieren, verwenden Sie die Aktionen **Kommissionierlinien/Bewegungslinien** oder **Registrierte Kommissionierlinien**. Weitere Informationen finden Sie unter [Flows für Produktion, Montage und Projekte](design-details-internal-warehouse-flows.md).

Sie können die Aktionen unter den folgenden Bedingungen verwenden:

* Der **Status** des Projekts ist **Offen**.
* Die **Zeilenart** der Projektplanungszeile ist **Budget** oder **Budgetiert und verrechenbar**.
* Der **Typ** der Projektplanungszeile ist **Artikel**.
* **Kommissionieren erforderlich** ist für den entsprechenden Ort aktiviert.
* **Gerichtetes Kommissionieren und Einlagern** ist deaktiviert.

> [!NOTE] 
> Obwohl die Einstellung **Kommissionierung vorschreiben** heißt, können Sie den Verbrauch trotzdem direkt aus der Projekt-Buchungsblattzeile für den Standort kommissionieren. Wenn Ihr Standort so festgelegt ist, dass eine Kommissionierung, aber keine Versandverarbeitung erforderlich ist, verwenden Sie die Seite **Lagerkommissionierung**, um die Kommissionierungsinformationen zu organisieren und zu drucken. Sie verwenden die Seite auch, um das Ergebnis der Kommissionierung einzugeben und zu verbuchen, was wiederum den Verbrauch der Artikel verbucht. 
> 
> Wenn Ihr Standort so festgelegt ist, dass sowohl die Kommissionierung als auch die Verarbeitung von Sendungen erforderlich ist, d.h. wenn Sie auf der Seite **Standortkarte** sowohl das Feld **Kommissionierung anfordern** als auch das Feld **Sendung anfordern** ausgewählt haben, verwenden Sie die Seite **Lager-Kommissionierung**, um die Kommissionierung zu bearbeiten. Lagerkommissionierungen sind ähnlich wie Bestandskommissionierungen. Der Unterschied besteht darin, dass Sie die Kommissionierung registrieren, anstatt die Kommissionierungsinformationen zu buchen. Mit dieser Registrierung wird kein Verbrauch gebucht, sondern die Artikel werden lediglich für die Buchung verfügbar gemacht. Als Manager eines Lagers können Sie ein Kommissionierarbeitsblatt verwenden, um die Kommissionierinformationen zu organisieren, bevor Sie die einzelnen Anweisungen für die Kommissionierung im Lager erstellen.

## <a name="to-review-planning-lines-for-a-project-ledger-entry"></a>So überprüfen Sie Planungszeilen für einen Projektposten

Nachdem Sie die Projekt-Buchungsblattzeilen gebucht haben, können Sie die gebuchten Planungszeilen sehen, die den Projekt-Buchungsblattposten zugeordnet sind.

> [!NOTE]  
> Dies setzt voraus, dass das Kontrollkästchen **Verwendungslink anwenden** für das Projekt aktiviert wurde. Weitere Informationen finden Sie unter [Projekte einrichten](projects-how-setup-jobs.md).  

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Projekterfassungen** ein und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie ein Buch.-Blatt des entsprechenden Projekts aus, und wählen Sie dann die Aktion **Projektposten** aus.  
3. Auf der Seite **Projektposten** wählen Sie die Aktion **Anzeigen verknüpfter Projektplanungszeilen** aus.

## <a name="see-also"></a>Siehe auch

[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
