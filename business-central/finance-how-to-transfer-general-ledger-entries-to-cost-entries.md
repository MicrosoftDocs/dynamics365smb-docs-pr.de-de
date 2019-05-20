---
title: 'Vorgehensweise: Übertragen von Sachposten in Kostenposten | Microsoft Docs'
description: Sie können Sachposten in Kostenposten übertragen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: a33fb434cc239de951d18783911c879587a3ace0
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242599"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>So übertragen Sie Sachposten in Kostenposten
Sie können Sachposten in Kostenposten übertragen.  

Bevor Sie den Vorgang für das Übertragen von Sachposten in Kostenposten durchführen, müssen Sie die Übertragung vorbereiten, um manuelle Korrekturbuchungen zu vermeiden.  

## <a name="to-prepare-the-transfer"></a>So bereiten Sie die Übertragung vor  

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kostenrechnung einrichten** ein, und wählen dann den zugehörigen Link aus.  
2.  Stellen Sie auf der Seite **Kostenrechnungseinrichtung** sicher, dass im Feld **Startdatum für Sachkontenübertragung** der richtige Wert eingetragen ist.  
3.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan Kontenarten** ein, und wählen dann den zugehörigen Link aus.  
4.  Auf der Seite **Kostenartkarte** prüfen Sie, dass das **Sachkontobereich** Feld für jede Kostenart korrekt verknüpft ist, um Posten aus dem Sachkonto zu übernehmen.  
5.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.  
6.  Überprüfen Sie für jedes Sachkonto auf der Seite **Sachkontokarte**, ob die **Kostenartnr.** Feld wird korrekt zu einer Kostenart verknüpft. Weitere Informationen finden Sie unter [Einrichten von Kostenrechnung](finance-set-up-cost-accounting.md).  
7.  Vergewissern Sie sich, dass alle entsprechenden Sachposten Dimensionswerte haben, die einer Kostenstelle und zu einem Kostenträger entsprechen.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>So übertragen Sie Sachposten in Kostenposten  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Transfer-Einträge‌ in CA** ein, und wählen dann den zugehörigen Link aus.  
2.  Wählen Sie auf Schaltfläche **OK**, um die Umlagerung zu starten. Der Prozess überträgt alle Sachposten, die nicht bereits übertragen wurden.  

    Während der Übertragung erstellt der Vorgang Verknüpfungen in den Posten **Posteneintrag** und **Kostentabelle**. Dies ermöglicht es Ihnen, die Herkunft von Kostenposten nachzuverfolgen.  

## <a name="see-also"></a>Siehe auch  
[Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md)   
[Einrichten der Kostenrechnung](finance-set-up-cost-accounting.md)   
