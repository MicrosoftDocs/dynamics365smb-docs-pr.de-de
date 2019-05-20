---
title: Ressourcenverbrauch und Preise aufzeichnen und anpassen | Microsoft Docs
description: Beschreibt, wie Sie den Ressourcenverbrauch oder den Verbrauch erfassen können, die einem Projekt zugeordnet sind, um Kosten, Preisen und Arbeitstypen zu verwalten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fc51b47b71d37daaccc4133d648c90b84d5a3494
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251745"
---
# <a name="use-resources-for-jobs"></a>Verwenden von Ressourcen für Projekte
Wenn Sie den Verbrauch von Ressourcen im Projekt Buch.-Blatt buchen, können Sie die Einstands- und Verkaufspreise, die Arbeitstypen und die damit verknüpften Projekte verfolgen. Weitere Informationen finden Sie unter [Nutzung von Projekten](projects-how-record-job-usage.md).

Sie können auch den Verbrauch einer Ressource in einem Ressourcen Buch.-Blatt buchen. Posten, die in einem Ressourcen Buch.-Blatt gebucht werden, haben keinen Einfluss auf die Finanzbuchhaltung.

## <a name="to-assign-resources-to-jobs"></a>So weisen Sie Projekten Ressourcen zu
Sie weisen Projekten Ressourcen zu, indem Sie Projektplanungszeilen für das Projekt erstellen. Weitere Informationen finden Sie unter  [Projekte erstellen](projects-how-create-jobs.md).

## <a name="to-record-resource-usage-for-a-job"></a>Um Ressourcenverbrauch für ein Projekt buchen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Job Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie das relevante Projekt-Buch.-Blatt und füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wenn der Verkaufsauftrag ausgeführt wurde, wählen Sie die Aktion **Buchen** aus.

## <a name="to-adjust-resource-prices"></a>Um Ressourcenpreise zu justieren:
Wenn Sie die Einstands- und Verkaufspreise für eine große Anzahl von Ressourcen ändern möchten, können Sie den Batchauftrag verwenden.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kosten/Preisressourcen anpassen** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.

> [!NOTE]  
>   Diese Stapelverarbeitung erzeugt oder aktualisiert keine alternativen Einkaufs- oder Verkaufspreise für Ressourcen. Sie ändert lediglich den Inhalt des Feldes auf der Ressourcenkarte für das Feld **Feld korrigieren**, das Sie in der Stapelverarbeitung ausgewählt haben. Die Änderung tritt für die Ressourcen sofort in Kraft, überprüfen Sie daher Ihre Korrekturfaktoren, bevor Sie die Stapelverarbeitung ausführen.

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a>Um Ressourcen-Preisänderungsvorschläge auf Basis bestehender alternativer Preise zu erstellen:
Wenn Sie bereits alternative Ressourcenpreise für mehrere Ressourcen eingerichtet haben, können Sie den Batchauftrag verwenden, um alternative Ressourcenpreise einzurichten.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kosten/Preisressourcen anpassen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Res. Preisänderung (Preis) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-Preisänderungen**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a>So erstellen Sie Ressourcenpreisvorschläge auf Basis bestehender Standard-VK-Preise
Wenn Sie einen oder mehrere alternative Ressourcenpreise basierend auf den Standardpreisen auf den Ressourcenkarten festlegen möchten, dann können Sie den Batchauftrag verwenden.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kosten/Preisressourcen anpassen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Res. Preisänderung (Res) vorschlagen** aus. Füllen Sie dann die Felder wie notwendig aus.  
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-VK-Preisvorschläge**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a>Um Ressourcenpreisvorschläge auf Basis alternierender Preise zu erhalten
Wenn Sie bereits alternative Ressourcenpreise für mehrere Ressourcen eingerichtet haben, können Sie den Batchauftrag verwenden, um alternative Ressourcenpreise einzurichten.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kosten/Preisressourcen anpassen vorschlagen** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus.
3. Wählen Sie die Schaltfläche **OK** aus.  
4. Wenn die Stapelverarbeitung beendet ist, öffnen Sie die Seite **Ressourcen-VK-Preisvorschläge**, um die Ergebnisse der Stapelverarbeitung anzuzeigen.

## <a name="see-also"></a>Siehe auch
[Projektmanagement](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)         
[Verkauf](sales-manage-sales.md)     
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
