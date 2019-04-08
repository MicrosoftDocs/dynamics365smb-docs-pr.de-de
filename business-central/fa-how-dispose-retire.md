---
title: Anlagen zurücksziehen| Microsoft Docs
description: Sie müssen einen Verkaufswert buchen, wenn Sie eine Anlage verkaufen oder ausrangieren, die storniert werden sollten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: bc3f97ab76117854cd7a9dd4584149b79e4b5066
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "798303"
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Anlagen entsorgen oder außer Dienst stellen
Wenn Sie eine Anlage verkaufen oder anderweitig entfernen, muss der Verkaufswert gebucht werden, um den Gewinn oder Verlust zu berechnen und zu erfassen. Ein Verkaufsposten muss der letzte gebuchte Posten einer Anlage sein. Für teilweise verkaufte Anlagen können Sie mehrere Verkaufsposten buchen. Die Summe aller gebuchten Verkaufsbeträge muss ein Habenposten sein.  

> [!NOTE]  
>   Falls Sie für den Verkauf einer Anlage eine andere Anlage in Zahlung nehmen, müssen Sie sowohl den Verkauf der alten Anlage als auch die Anschaffung der neuen Anlage buchen. Weitere Informationen finden Sie unter [Anschaffen von Anlagen](fa-how-acquire.md).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>So buchen Sie einen Verkauf aus dem Anlagen Fibu Buch.-Blatt
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **FA Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie im Feld **Anlagenbuchungsart** den **Verkauf**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung eines Verkaufs eingerichtet wird.  

    > [!NOTE]  
    >   Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Kto. Verkauf** das Sollkonto im Sachkonto und das Feld **Gegenkto Verkauf** enthält das Sachkonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Wählen Sie die Aktion **Buchen** aus.  

Wenn Sie eine Anlage zum Teil verkaufen, müssen Sie die Anlage aufteilen, bevor Sie die Verkaufstransaktion buchen können. Weitere Informationen finden Sie unter [Übertragen, Teilen oder Kombinieren von Anlagen.](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>So zeigen Sie Verkaufsposten an
Wenn Sie eine Anlage verkaufen, wird der Verkaufswert in den Sachposten gebucht, wo Sie die Ergebnisse anzeigen können.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Anlagen** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Anlage aus, für die Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **AfA-Bücher** aus.  
3. Wählen Sie das AfA-Buch aus, für das Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **Posten** aus.  
4. Wählen Sie im Feld **Anlagebuchungskategorie** die Zeile mit **Verkauf** aus, und klicken Sie auf die Aktion **Navigieren**.  
5. Wählen Sie auf der Seite **Navigieren** die Sachpostenzeile aus, und klicken Sie auf die Aktion **Anzeigen**.  

Die Seite **Sachposten** wird geöffnet, in dem Sie die Posten sehen können, die aus der Verkaufsbuchung resultieren.  

## <a name="see-also"></a>Siehe auch
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
