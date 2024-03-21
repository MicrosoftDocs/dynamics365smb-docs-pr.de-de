---
title: Ressourcenverbrauch und Preise aufzeichnen und anpassen
description: 'Beschreibt, wie Sie den Ressourcenverbrauch oder den Verbrauch erfassen können, die einem Projekt zugeordnet sind, um Kosten, Preisen und Arbeitstypen zu verwalten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '201,206, 207, 271, 493'
ms.date: 03/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="use-resources-for-jobs"></a>Verwenden von Ressourcen für Projekte

Wenn Sie den Verbrauch von Ressourcen im Projekt Buch.-Blatt buchen, können Sie die Einstands- und Verkaufspreise, die Arbeitstypen und die damit verknüpften Projekte verfolgen. Weitere Informationen finden Sie unter [Verwendung von Datensätzen für Projekte](projects-how-record-job-usage.md).

> [!NOTE]
> Sie können auch externe Ressourcen einkaufen, z.B. um einem Kreditor die gelieferte Arbeit in Rechnung zu stellen. Weitere Informationen finden Sie unter [Käufe erfassen](purchasing-how-record-purchases.md).

Sie können auch den Verbrauch einer Ressource in einem Ressourcen Buch.-Blatt buchen. Posten, die in einem Ressourcen Buch.-Blatt gebucht werden, haben keinen Einfluss auf die Finanzbuchhaltung.

## <a name="to-assign-resources-to-jobs"></a>So weisen Sie Projekten Ressourcen zu

Sie weisen Projekten Ressourcen zu, indem Sie Projektplanungszeilen für das Projekt erstellen. Weitere Informationen finden Sie unter  [Projekte erstellen](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Um Ressourcenverbrauch für ein Projekt buchen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Projekt Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie das relevante Projekt-Buch.-Blatt und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="to-adjust-resource-prices"></a>Um Ressourcenpreise zu justieren:

Wenn Sie die Einstands- und Verkaufspreise für eine große Anzahl von Ressourcen ändern möchten, können Sie den Batchauftrag verwenden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Ressourcenpreise justieren** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.

> [!NOTE]  
> Diese Stapelverarbeitung erzeugt oder aktualisiert keine alternativen Einkaufs- oder Verkaufspreise für Ressourcen. Sie ändert lediglich den Inhalt des Feldes auf der Ressourcenkarte für das Feld **Feld korrigieren**, das Sie in der Stapelverarbeitung ausgewählt haben. Die Änderung tritt für die Ressourcen sofort in Kraft, überprüfen Sie daher Ihre Korrekturfaktoren, bevor Sie die Stapelverarbeitung ausführen.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Um Ressourcen-Preisänderungsvorschläge auf Basis bestehender alternativer Preise zu erstellen:

Wenn Sie bereits einen alternativen Ressourcenpreis für einige Ressourcen eingerichtet haben, können Sie einen Batch-Job verwenden, um mehrere alternative Ressourcenpreise einzurichten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Ressourcen-VK-Preisvorschläge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Res. Preisänderung (Preis) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>So erstellen Sie Ressourcenpreisvorschläge auf Basis bestehender Standard-VK-Preise

Wenn Sie einen oder mehrere alternative Ressourcenpreise basierend auf den Standardpreisen auf den Ressourcenkarten festlegen möchten, dann können Sie den Batchauftrag verwenden.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Ressourcen-VK-Preisvorschläge** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Res. Preisänderung (Res) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.  
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-VK-Preisarbeitsblätter**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Um Ressourcenpreisvorschläge auf Basis alternierender Preise zu erhalten

Wenn Sie bereits alternative Ressourcenpreise für einige Ressourcen festgelegt haben, können Sie einen Batchauftrag verwenden, um mehrere alternative Ressourcenpreise festzulegen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Vorschlag Res.-VK-Preisvorschlag (Preis) Chg. (Preis)** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus.
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-VK-Preisarbeitsblätter**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="see-also"></a>Weitere Informationen

[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)     
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
