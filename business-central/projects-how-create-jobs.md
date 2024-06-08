---
title: Projektkarte für ein Projekt erstellen und Aufgaben angeben
description: 'Für ein neues Projekt erstellen Sie eine Projektkarte, die Projektaufgaben enthält und Planungszeilen erstellt, um Ihnen zu helfen, Status und Budgets zu verwalten.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-projects"></a>Projekte erstellen

Wenn Sie mit einem neuen Projekt beginnen, müssen Sie eine Projektkarte mit integrierten Projektaufgaben und Projektplanungszeilen erstellen, strukturiert in zwei Ebenen.  

Die erste Ebene besteht aus Projektaufgaben. Sie müssen mindestens eine Projektaufgabe pro Projekt erstellen, da sich alle Buchungen auf eine Projektaufgabe beziehen. Ist für das Projekt mindestens eine Projektaufgabe vorhanden, haben Sie die Möglichkeit zum Einrichten von Projektplanungszeilen sowie zum Buchen des Verbrauchs für das Projekt.

Die zweite Ebene besteht aus Projektplanungszeilen, die zum Angeben des genauen Verbrauchs von Ressourcen, Artikeln sowie von verschiedenen Aufwandssachposten dienen.

Durch die Ebenenstruktur lässt sich das Projekt in kleinere Aufgaben unterteilen, was wiederum eine detaillierte Budgetierung, Angebotserstellung und Erfassung ermöglicht. Außerdem gibt sie Ihnen Einblick in den Fortschritt eines Projekt. So können Sie beispielsweise verfolgen, ob Sie die festgelegten Meilensteine erreichen oder ob Sie die Budgeterwartungen einhalten.

> [!TIP]
> Wählen Sie die Aktion **Neues Projekt** im Rollencenter **Projektmanager** aus, um einen Leitfaden für das unterstütze Setup zu starten, der Sie durch die Schritte zur Erstellung eines Projekts mit integrierten Aufgaben und Planungszeilen führt. Nachfolgend wird beschrieben, wie Sie die Schritte manuell ausführen. <!-- For an example of how to create a project manually, go to [Video: How to create a project in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).-->

## <a name="invoice-one-or-more-customers-for-project-tasks"></a>Einem oder mehreren Debitoren Projektaufgaben in Rechnung stellen

Manchmal unterscheidet sich die Partei, die eine Dienstleistung erhält, von der Partei, die die Rechnung bezahlt. Außerdem müssen Sie möglicherweise manchmal mehreren Debitoren Rechnungen für Aufgaben im Projekt ausstellen. Geben Sie auf der Seite **Projektkarte** im Feld **Aufgabenabrechnungsmethode** an, ob Sie einem oder mehreren Debitoren eine Rechnung stellen.

Wenn der Debitor, der die Dienstleistung erhält, auch die Rechnung bezahlen soll, wählen Sie in den Feldern **Rechnungsadresse** und **Lief. an** die Option **Standard (Debitor)** und **Standard (Verkauf an Adresse)** aus.

Wenn Sie mehreren Debitoren Rechnungen stellen, können Sie den Debitor angeben, der die Dienstleistung erhält, und den Debitor, der für jede Aufgabe im Projekt eine Rechnung stellen soll. Sie können auch die folgenden Informationen angeben:

* Wo die Arbeit stattfinden wird, indem Sie aus einer Liste von Lieferadressen für den Debitor auswählen.
* Fügen Sie Informationen über externe Referenzen hinzu, um die Kommunikation über das Projekt zu vereinfachen.
* Überschreiben Sie die finanziellen Standardbedingungen des Projekts.

## <a name="invoice-one-customer-for-multiple-project-tasks"></a>Einem Debitoren mehrere Projektaufgaben in Rechnung stellen

Sie können Ihren Rechnungsstellungsprozess vereinfachen, indem Sie eine Rechnung für mehrere Projekte an einen Debitoren senden. Fügen Sie Projektplanungszeilen aus mehreren Projekten auf einmal einer Verkaufsrechnung hinzu. Dieser Vorgang ähnelt dem Erstellen einer Verkaufsrechnung aus einer Projektplanungszeile und der Eingabe eines Werts in das Feld **An Verkaufsrechnungsnr. anfügen**.

Hier ist eine Übersicht über den Prozess.

1. Erstellen Sie einen neuen Verkaufsauftrag, und füllen Sie das Feld **Verk. an Deb.-Nr.** aus Feld Füllen Sie bei Bedarf auch die Felder **Rechnung an Debitor Nr.** und **Währungscode** aus.
2. Klicken Sie im Inforegister **Zeilen** und wählen die Aktion **Projektplanzeilen abrufen**. Auf der Seite **Projektplanzeilen abrufen** werden abrechenbare Projektplanungszeilen aus Projekten für den Verk. an Debitor, die Rechnung an den Debitor und die Rechnungswährung angezeigt, bei denen die in Rechnung zu stellende Menge mehr als null beträgt. 
3. Wählen Sie die Zeilen aus, die Sie der Rechnung hinzufügen möchten, und wählen Sie anschließend **OK** aus.

Wiederholen Sie diese Schritte, wenn Sie einen weiteren Satz Projektplanungszeilen hinzufügen möchten. Sie können die Rechnung oder ihre Zeilen auch löschen und von vorne beginnen.

> [!NOTE]
> Es gibt einige Einschränkungen:
>
> * Die Aktion **Projektplanzeilen abrufen** ist für Verkaufsaufträge oder Verkaufsangebote nicht verfügbar.
> * Sie können nicht nach **Neuer Lief. an Code** oder **Kontaktnr.** filtern Felder.

## <a name="to-create-a-project-card"></a>So erstellen Sie eine Projektkarte

Sie erstellen eine Projektkarte und erstellen dann Projektaufgabenzeilen und Projektplanungszeilen dafür.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Projekte** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Um das Projekt auf Informationen eines anderen Projekts zu basieren, wählen Sie die Aktion **Projekt kopieren** aus und ergänzen Sie die Felder wie nötig. Wählen Sie dann die Schaltfläche **OK** aus.

> [!NOTE]  
> Wenn Sie Arbeitszeittabellen bei Ihrem Projekt verwenden, müssen Sie auch eine verantwortliche Person angeben. Diese Person kann Arbeitszeittabellen für die Mitarbeiteraufgaben genehmigen, die dem Projekt zugeordnet sind. Weitere Informationen finden Sie unter [Zeittabellen festlegen](projects-how-setup-time-sheets.md).

Markieren Sie optional Aktionen für das Projekt als blockiert, indem Sie das Feld **Blockiert** verwenden. In den folgenden Tabelle werden Auswirkungen der Optionen für dieses Feld beschrieben.

|Option  |Description  |
|---------|---------|
|Leer |Alle Aktionen sind zulässig.|
|Buchen    |Sie können mit Planungszeilen arbeiten, doch ist das Projekt für Buchungen gesperrt. Wenn Sie diese Option auswählen, können Sie keinen Verbrauch oder Verkauf für das Projekt buchen.|
|Alle  |Alle Aktionen sind gesperrt.|

## <a name="to-create-tasks-for-a-project"></a>Aufgaben für ein Projekt erstellen

Beim Einrichten eines neuen Projekts ist es wichtig, auch die verschiedenen Aufgaben für das Projekt anzugeben. Sie legen Aufträge fest, indem Sie auf der Seite **Aufgaben** Inforegister auf der Seite **Projektkarte** eine Zeile pro Auftrag erstellen. Jedes Projekt muss mindestens eine Aufgabe haben.

1. Wählen Sie das ![Glühbirne, welche die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Projekte** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie die Projektkarte für ein entsprechendes Projekt.
3. Füllen Sie im Inforegister **Aufgaben** die Felder nach Bedarf auf einer neuen Zeile aus.
4. Um Aufgaben einzurücken und eine Hierarchie zu erstellen, wählen Sie die Aktion **Aufgaben** und **Projektaufgaben einrücken**.
5. Wiederholen Sie die Schritte 3 und 4 für alle Aufgaben, die Sie für das Projekt benötigen.
6. Um die Projektaufgaben mit Informationen über andere Projektaufgaben anzugeben, wählen Sie die Aktion **Projektaufgaben kopieren von** aus und ergänzen Sie die Felder wie nötig. Wählen Sie dann die Schaltfläche **OK** aus.

## <a name="to-create-planning-lines-for-a-project"></a>So erstellen Sie eine Planzeilen für ein Projekt

Sie können Ihre neuen Projektaufgaben für Projektplanzeilen neu definieren. Eine Planungszeile kann die Informationen erfassen, die Sie für ein Projekt verfolgen möchten. Sie können z. B. die Ressourcen, die das Projekt erfordert, oder die Artikel, die benötigt werden, verfolgen. Ein Beispiel: Sie haben eine Aufgabe, um einen Debitor dazu zu bringen, ein Projekt zu genehmigen. Sie verknüpfen die Aufgabe mit Planungszeilen für Artikel wie das Treffen mit dem Debitor und die Zuweisung einer Ressource.  

Eine Projektplanungszeile kann von einer der folgenden Arten sein.  

| Typ | Description |
| --- | --- |
| **Budget** |Dient zum Angeben der geschätzten Verbrauchswerte und der Kosten für das Projekt, üblicherweise in einem Aufwandsvertrag. Sie können keine Planungszeilen dieser Art in Rechnung stellen. |
| **Fakturierbar** |Dient zum Angeben der geschätzten Fakturierung für den Debitor, üblicherweise in einem Festpreisprojekt. |
| **Sowohl budgetiert und verrechenbar** |Dient zum Angeben des geplanten Verbrauchs, der dem zu fakturierenden Wert entspricht. |

> [!NOTE]
> Während Sie Informationen zu Projektplanungszeilen eingeben, werden die Informationen zur Kalkulation automatisch ausgefüllt. So basieren beispielsweise die Kosten, Preise und Rabatte für Ressourcen und Artikel auf den Informationen der Ressource und des Artikels.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") und geben Sie **Projekte** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie eine relevante Projektkarte.
3. Wählen Sie eine Projektaufgabe aus, deren Wert für das Feld **Projektaufgabenart** **Buchen** enthält und klicken Sie anschließend auf die Aktion **Projektplanzeilen**.  
4. In einer neuen Zeile auf der Seite **Projektplanungszeilen** füllen Sie die Felder nach Bedarf aus.
5. Wiederholen Sie die Schritte 3 und 4 für alle Planungszeilen für diese Projektaufgabe.

## <a name="see-also"></a>Siehe auch

[Projektmanagement](projects-manage-projects.md)  
[Video: Wie man ein Projekt in Dynamics 365 Business Central erstellt](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
