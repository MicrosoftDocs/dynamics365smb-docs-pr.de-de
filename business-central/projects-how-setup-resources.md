---
title: 'Einrichten von Projektressourcenkosten, -preisen und -kapazitäten'
description: 'Um Ressourcen zu verwenden und Projektmanagement zu erleichtern, können Sie Kosten und Preisen für einzelne Ressourcen oder Ressourcengruppen angeben und die die Ressourcenkapazität festlegen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '72, 76, 77, 203, 204'
ms.date: 08/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="set-up-resources-for-projects"></a>Ressourcen für Projekte einrichten

Zur ordnungsgemäßen Verwaltung von Ressourcenaktivitäten ist die Einrichtung von Ressourcen sowie der zugehörigen Kosten und Preise erforderlich. Die projektbezogenen Preise, Rabatte und Kostenfaktorregeln werden auf der Projektkarte eingerichtet. Die Kosten und Preise können für einzelne Ressourcen, für Ressourcengruppen oder für alle verfügbaren Ressourcen des Unternehmens angegeben werden.

Wenn Ressourcen im Rahmen eines Projekts verbraucht oder verkauft werden, werden die zugehörigen Preise/Kosten aus den Informationen abgerufen, die Sie eingerichtet haben.

Der standardmäßige Betrag pro Stunde wird bei der Ressourcenerstellung angegeben. Wird also beispielsweise eine bestimmte Maschine fünf Stunden lang für ein Projekt verwendet, erfolgt die Berechnung des Projekts auf der Grundlage des Betrags pro Stunde.

> [!NOTE]
> Sie können keine externen Ressourcen für ein bestimmtes Projekt erwerben. Wir empfehlen Ihnen, stattdessen Elemente vom Typ „Dienstleistung“ zu verwenden.

## <a name="to-set-up-a-resource"></a>So richten Sie eine Ressource ein

Erstellen Sie für jede Ressource eine Karte,die Sie in " Projekte verwenden möchten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Ressourcen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu**.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Eine Ressourcengruppe einrichten

Mehrere Ressourcen können in einer Ressourcengruppe zusammengefasst werden. Alle Kapazitäten und Budgets der einzelnen Ressourcen werden für die Ressourcengruppe aufsummiert. Es ist ebenfalls möglich, Kapazitäten unabhängig von den summierten Werten oder zusätzlich einzugeben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Ressourcengruppen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-set-capacity-for-a-resource"></a>So legen Sie die Kapazität für eine Ressource fest

Um zu berechnen wie viel Zeit eine Ressource in Projekten verbringen kann, muss deren Kapazität zuerst als verfügbare Zeit pro Periode im Arbeitskalender eingerichtet werden. Diese Einstellungen werden verwendet, wenn Sie Projektplanungszeilen ausfüllen, die die Ressource enthalten. Weitere Informationen finden Sie unter [Projekte erstellen](projects-how-create-jobs.md).

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Ressourcen** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die entsprechende Debitorenkarte und klicken dann auf die Aktion **Ressourcenkapazität**.
3. Geben Sie auf der Seite **Ressourcenkapazität** im Feld **Anzeigen nach** die Länge der Periode an, wie beispielsweise **Tag**, die in Spalten im Inforegister **Ressourcenkapazität – Matrix** angezeigt wird.
4. Für jede Ressource in einer Zeile geben Sie für jede Periode in den Spalten die Anzahl von Stunden an, für die die Ressource verfügbar ist.
5. Alternativ, um die wöchentliche Kapazität der Ressource im Detail innerhalb eines Start- und Enddatums anzugeben, wählen Sie die Aktion **Kapazität festlegen** aus.
6. Füllen Sie auf der Seite **Res.-Kapazität Einstellungen** die Felder nach Bedarf aus.
7. Wählen Sie die Aktion **Kapazität aktualisieren** aus. Die Seite **Ressourcenkapazität** wird mit der eingegebenen Kapazität aktualisiert.
8. Schließen Sie die Seite.

## <a name="to-set-up-alternate-resource-costs"></a>Um alternative Ressourcenkosten einzurichten:

Zusätzlich zu den Kosten, die in der Ressourcenkarte angegeben werden, können Sie auch alternative Kosten für jede Ressource einrichten. Wenn z. B. ein Mitarbeiter einen anderen Stundensatz für Überstunden hat, können Sie für diesen Arbeitstyp einen Einstandspreis einrichten. Die alternativen Kosten, die Sie für die Ressource einrichten, übersteuert den Einstandspreis auf der Ressourcenkarte, wenn Sie die Ressource im Ressourcen Buch.-Blatt buchen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Ressourcen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Ressource, für die das Sie mindestens alternativen Einstandspreis einrichten möchten, und wählen die Aktion **Kosten** aus.  
3. Füllen Sie auf der Seite **Ressourcenkosten** die Felder auf einer Zeile nach Bedarf aus.  
4. Wiederholen Sie Schritt 3 für jeden alternativen Einstandspreis, den Sie einrichten möchten.

> [!NOTE]
> Um Ressourcenkosten einzurichten, die für alle Ressourcen und Ressourcengruppen gelten, öffnen Sie die Seite  **Ressourcenkosten**  und füllen Sie die Felder aus.

## <a name="to-set-up-alternate-resource-prices"></a>Um alternative Ressourcenkosten einzurichten:

Zusätzlich zu den Kosten, die in der Ressourcenkarte angegeben werden, können Sie auch alternative Kosten für jede Ressource einrichten. Diese alternativen Preise können von Bedingungen abhängig sein. D. h. sie können davon abhängen, ob diese Ressource in einem bestimmten Projekt oder für einen bestimmten Arbeitstyp verwendet wird.

1. Wählen Sie das Symbol ![Glühbirne, die die „Sie wünschen ...“-Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus Symbol. Geben Sie **Ressourcen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Ressource, für die das Sie mindestens alternativen Einstandspreis einrichten möchten, und wählen die Aktion **Kosten** aus.
3. Füllen Sie auf der Seite **Ressourcenpreise** die Felder auf einer Zeile nach Bedarf aus.
4. Wiederholen Sie Schritt 3 für jeden alternativen Ressourcenpreis, den Sie einrichten möchten.

## <a name="to-adjust-resource-prices"></a>Um Ressourcenpreise zu justieren:

Wenn Sie die Einstands- und Verkaufspreise für eine große Anzahl von Ressourcen ändern möchten, können Sie den Batchauftrag verwenden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Ressourcenpreise justieren** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.

> [!NOTE]  
> Dieser Batchauftrag erstellt oder Anpassen alternative Kosten oder Preise für Ressourcen. Sie ändert lediglich den Inhalt des Feldes auf der Ressourcenkarte für das Feld **Feld korrigieren**, das Sie in der Stapelverarbeitung ausgewählt haben. Die Anpassung wird für Ressourcen sofort wirksam. Überprüfen Sie daher Ihre Anpassungsfaktoren, bevor Sie den Batchauftrag ausführen.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Um Ressourcen-Preisänderungsvorschläge auf Basis bestehender alternativer Preise zu erstellen:

Wenn Sie für einige Ressourcen bereits alternative Ressourcenpreise eingerichtet haben, können Sie mithilfe eines Stapelverarbeitungsauftrags mehrere alternative Ressourcenpreise einrichten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Ressourcen-VK-Preisvorschläge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Res. Preisänderung (Preis) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>So erstellen Sie Ressourcenpreisvorschläge auf Basis bestehender Standard-VK-Preise

Wenn Sie einen oder mehrere alternative Ressourcenpreise basierend auf den Standardpreisen auf den Ressourcenkarten festlegen möchten, dann können Sie den Batchauftrag verwenden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Ressourcen-VK-Preisvorschläge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Res. Preisänderung (Res) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.  
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-VK-Preisarbeitsblätter**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="see-also"></a>Siehe auch

[Einrichten des Projektmanagements](projects-setup-projects.md)  
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
