---
title: "Anlagen zurücksziehen| Microsoft Docs"
description: "Sie müssen einen Verkaufswert buchen, wenn Sie eine Anlage verkaufen oder ausrangieren, die storniert werden sollten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 5fc65c97e7c95a37d54b4084aaf8616169b625db
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-dispose-of-or-retire-fixed-assets"></a>So geht's: Anlagen entsorgen oder außer Dienst stellen
Wenn Sie eine Anlage verkaufen oder anderweitig entfernen, muss der Verkaufswert gebucht werden, um den Gewinn oder Verlust zu berechnen und zu erfassen. Ein Verkaufsposten muss der letzte gebuchte Posten einer Anlage sein. Für teilweise verkaufte Anlagen können Sie mehrere Verkaufsposten buchen. Die Summe aller gebuchten Verkaufsbeträge muss ein Habenposten sein.  

> [!NOTE]  
>   Falls Sie für den Verkauf einer Anlage eine andere Anlage in Zahlung nehmen, müssen Sie sowohl den Verkauf der alten Anlage als auch die Anschaffung der neuen Anlage buchen. Weitere Informationen finden Sie unter [So geht's: Beschaffen von Anlagen](fa-how-acquire.md).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>So buchen Sie einen Verkauf aus dem Anlagen Fibu Buch.-Blatt
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie im Feld **Anlagenbuchungsart** den **Verkauf**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung eines Verkaufs eingerichtet wird.  

    > [!NOTE]  
>   Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Im Fenster **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Kto. Verkauf** das Sollkonto im Sachkonto und das Feld **Gegenkto Verkauf** enthält das Sachkonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen. Weitere Informationen finden Sie im Abschnitt "So richten Sie Anlagenbuchungsgruppen ein" in [So geht's: Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).  
5. Wählen Sie die Aktion **Buchen** aus.  

    Wenn Sie eine Anlage zum Teil verkaufen, müssen Sie die Anlage aufteilen, bevor Sie die Verkaufstransaktion buchen können. Weitere Informationen finden Sie unter [So geht's: Übertragen, Teilen oder Kombinieren von Anlagen.](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>So zeigen Sie Verkaufsposten an
Wenn Sie eine Anlage verkaufen, wird der Verkaufswert in den Sachposten gebucht, wo Sie die Ergebnisse anzeigen können.  

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Anlage aus, für die Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **AfA-Bücher** aus.  
3. Wählen Sie das AfA-Buch aus, für das Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **Posten** aus.  
4. Wählen Sie im Feld **Anlagebuchungskategorie** die Zeile mit **Verkauf** aus, und klicken Sie auf die Aktion **Navigieren**.  
5. Wählen Sie im Fenster **Navigieren** die Sachpostenzeile aus, und klicken Sie auf die Aktion **Anzeigen**.  

Das Fenster **Sachposten** wird geöffnet, in dem Sie die Posten sehen können, die aus der Verkaufsbuchung resultieren.  

## <a name="see-also"></a>Siehe auch
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

