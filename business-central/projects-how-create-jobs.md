---
title: Projektkarte für ein Projekt erstellen und Aufgaben angeben
description: 'Für ein neues Projekt erstellen Sie eine Projektkarte, die Projektaufgaben und enthält Planungszeilen erstellt, um Ihnen zu helfen, Status und Budgets zu verwalten.'
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.author: edupont
---
# <a name="create-jobs" />Projekt erstellen

Wenn Sie mit einem neuen Projekt beginnen, müssen Sie eine Projektkarte mit integrierten Projektaufgaben und Projektplanungszeilen erstellen, strukturiert in zwei Ebenen.  

Die erste Ebene besteht aus Projektaufgaben. Sie müssen mindestens eine Projektaufgabe pro Projekt erstellen, da sich alle Buchungen auf eine Projektaufgabe beziehen. Ist für das Projekt mindestens eine Projektaufgabe vorhanden, haben Sie die Möglichkeit zum Einrichten von Planungszeilen sowie zum Buchen des Verbrauchs für das Projekt.

Die zweite Ebene besteht aus Projektplanungszeilen, die zum Angeben des genauen Verbrauchs von Ressourcen, Artikeln sowie von verschiedenen Aufwandssachposten dienen.

Durch die Ebenenstruktur lässt sich das Projekt in kleinere Aufgaben unterteilen, was wiederum eine detaillierte Budgetierung, Angebotserstellung und Erfassung ermöglicht. Außerdem gibt sie Ihnen Einblick in den Fortschritt eines Projekt. So können Sie beispielsweise verfolgen, ob Sie die festgelegten Meilensteine erreichen oder ob Sie die Budgeterwartungen einhalten.

> [!TIP]
> Wählen Sie die Aktion **Neues Projekt** im Rollencenter **Projektmanager** aus, um einen Leitfaden für das unterstütze Setup zu starten, der Sie durch die Schritte zur Erstellung eines Projekts mit integrierten Aufgaben und Planungszeilen führt. Nachfolgend wird beschrieben, wie Sie die Schritte manuell ausführen. Ein Beispiel dazu, wie Sie ein Projekt manuell erstellen, finden im [Video: So erstellen Sie ein Projekt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

Manchmal unterscheidet sich die Partei, die eine Dienstleistung erhält, von der Partei, die die Rechnung bezahlt. Auf der **Projekte**-Seite können Sie den Debitor, der von dem Projekt profitieren wird, in den Feldern **Verk. an** angeben und den Rechnungssteller in den Feldern **Rech. an**. Sie können auch die folgenden Informationen angeben: 

* Wo die Arbeit stattfinden wird, indem Sie aus einer Liste von Lieferadressen für den Debitor auswählen.
* Fügen Sie Informationen über externe Referenzen hinzu, um die Kommunikation über das Projekt zu vereinfachen.
* Überschreiben Sie die finanziellen Standardbedingungen des Projekts.

## <a name="to-create-a-job-card" />So erstellen Sie eine Projektkarte

Sie erstellen eine Projektkarte und erstellen dann Projektaufgabenzeilen und Projektplanungszeilen dafür.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um das Projekt mit Informationen über andere Projekte anzugeben, wählen Sie die Aktion **Projekt kopieren** aus und ergänzen Sie die Felder wie nötig. Wählen Sie dann die Schaltfläche **OK** aus.

> [!NOTE]  
> Wenn Sie Arbeitszeittabellen bei Ihrem Projekt verwenden, müssen Sie auch eine verantwortliche Person angeben. Diese Person kann Arbeitszeittabellen für die Mitarbeiteraufgaben genehmigen, die dem Projekt zugeordnet sind. Weitere Informationen finden Sie unter [Zeittabellen festlegen](projects-how-setup-time-sheets.md).

Markieren Sie optional Aktionen für das Projekt als blockiert, indem Sie das Feld **Blockiert** verwenden. In den folgenden Tabelle werden Auswirkungen der Optionen für dieses Feld beschrieben.

|Option  |Description  |
|---------|---------|
|Leer |Alle Aktionen sind zulässig.|
|Buchen    |Sie können mit Planungszeilen arbeiten, doch ist das Projekt für Buchungen gesperrt. Wenn Sie diese Option auswählen, können Sie keinen Verbrauch oder Verkauf für das Projekt buchen.|
|Alle  |Alle Aktionen sind gesperrt.|

## <a name="to-create-tasks-for-a-job" />Aufgaben für ein Projekt erstellen

Beim Einrichten eines neuen Projekts ist es wichtig, auch die verschiedenen Aufgaben für das Projekt anzugeben. Sie legen Aufträge fest, indem Sie auf der Seite **Aufgaben** Inforegister auf der Seite **Auftragskarte** eine Zeile pro Auftrag erstellen. Jedes Objekt muss mindestens eine Aufgabe haben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Projektkarte für ein entsprechendes Projekt.
3. Füllen Sie im Inforegister **Aufgaben** die Felder nach Bedarf auf einer neuen Zeile aus.
4. Um Aufgaben einzurücken und eine Hierarchie zu erstellen, wählen Sie die Aktion **Aufgaben** und **Projektaufgaben einrücken**.
5. Wiederholen Sie die Schritte 3 und 4 für alle Aufgaben, die Sie für das Projekt benötigen.
6. Um die Projektaufgaben mit Informationen über andere Projektaufgaben anzugeben, wählen Sie die Aktion **Projektaufgaben kopieren von** aus und ergänzen Sie die Felder wie nötig. Wählen Sie dann die Schaltfläche **OK** aus.

## <a name="to-create-planning-lines-for-a-job" />So erstellen Sie eine Projektplanzeile für ein Projekt

Sie können Ihre neuen Projektaufgaben für Projektplanzeilen neu definieren. Eine Planungszeile kann die Informationen erfassen, die Sie für einen Auftrag verfolgen möchten. Sie können z.B. die Ressourcen, die der Auftrag erfordert, oder die Artikel, die benötigt werden, verfolgen. Ein Beispiel: Sie haben eine Aufgabe, um einen Debitor dazu zu bringen, einen Auftrag zu genehmigen. Sie verknüpfen die Aufgabe mit Planungszeilen für Artikel wie das Treffen mit dem Debitor und die Zuweisung einer Ressource.  

Eine Projektplanungszeile kann von einer der folgenden Arten sein.  

| Typ | Beschreibung |
| --- | --- |
| **Budget** |Dient zum Angeben der geschätzten Verbrauchswerte und der Kosten für das Projekt, üblicherweise in einem Aufwandsvertrag. Planungszeilen dieser Art können nicht in Rechnung gestellt werden. |
| **Fakturierbar** |Dient zum Angeben der geschätzten Fakturierung für den Debitor, üblicherweise in einem Festpreisprojekt. |
| **Sowohl budgetiert und verrechenbar** |Dient zum Angeben des geplanten Verbrauchs, der dem zu fakturierenden Wert entspricht. |

> [!NOTE]
> Während Sie Informationen zu Auftragsplanungszeilen eingeben, werden die Informationen zur Kalkulation automatisch ausgefüllt. So basieren beispielsweise die Kosten, Preise und Rabatte für Ressourcen und Artikel auf den Informationen der Ressource und des Artikels. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie eine entsprechende Jobkarte.
3. Wählen Sie eine Projektaufgabe aus, deren Wert für das Feld **Projektaufgabenart** **Buchen** enthält und klicken Sie anschließend auf die Aktion **Projektplanzeilen**.  
4. Auf einer neuen Zeile auf der Seite **Projektplanungszeilen** füllen Sie die Felder nach Bedarf aus.
5. Wiederholen Sie die Schritte 3 und 4 für alle Planungszeilen für diese Projektaufgabe.

## <a name="see-related-microsoft-trainingtrainingmodulescreate-new-job" />Siehe verwandte [Microsoft Schulungen](/training/modules/create-new-job/)

## <a name="see-also" />Siehe auch

[Projektmanagement](projects-manage-projects.md)  
[Video: Wie man einen Auftrag in Dynamics 365 Business Central erstellt](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
