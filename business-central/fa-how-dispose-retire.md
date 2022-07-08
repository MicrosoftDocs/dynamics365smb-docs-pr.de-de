---
title: FA entsorgen oder ausmustern
description: Wenn Sie eine Anlage verkaufen oder anderweitig entfernen, muss der Verkaufswert gebucht werden, um den Gewinn oder Verlust zu berechnen und zu erfassen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.search.form: 5628, 5610, 5611, 5629, 5633
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: dd8e374a0f7124084d789858767d08c4935d1631
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077319"
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Anlagen entsorgen oder außer Dienst stellen

Wenn Sie eine Anlage verkaufen oder anderweitig veräußern, muss der Veräußerungswert gebucht werden, um den Gewinn oder Verlust zu berechnen und zu erfassen. Ein Verkaufsposten muss der letzte gebuchte Posten einer Anlage sein. Für teilweise verkaufte Anlagen können Sie mehrere Verkaufsposten buchen. Die Summe aller gebuchten Verkaufsbeträge muss ein Habenposten sein.  

> [!NOTE]  
> Falls Sie für den Verkauf einer Anlage eine andere Anlage in Zahlung nehmen, müssen Sie sowohl den Verkauf der alten Anlage als auch die Anschaffung der neuen Anlage buchen. Weitere Informationen finden Sie unter [Anlage erwerben](fa-how-acquire.md).  

Bei den folgenden Schritten wird davon ausgegangen, dass Sie die entsprechenden Buchungsgruppen auf der Seite **Anlagen-Buchungsgruppen** bereits eingerichtet haben. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>So buchen Sie einen Verkauf aus dem Anlagen Fibu Buch.-Blatt

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen-Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine ursprüngliche Buch.-Blattzeile und füllen Sie die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie im Feld **Anlagenbuchungsart** den **Verkauf**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Buch.-Blattzeile wird für das Gegenkonto erstellt, das für die Buchung eines Verkaufs eingerichtet wird.  

    > [!NOTE]  
    >  Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Kto. Verkauf** das Sollkonto im Sachkonto und das Feld **Gegenkto Verkauf** enthält das Sachkonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Wählen Sie die Aktion **Buchen** aus.  

Wenn Sie eine Anlage zum Teil verkaufen, müssen Sie die Anlage aufteilen, bevor Sie die Verkaufstransaktion buchen können. Weitere Informationen finden Sie unter [Übertragen, Teilen oder Kombinieren von Anlagen](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>So zeigen Sie Verkaufsposten an

Wenn Sie eine Anlage verkaufen, wird der Verkaufswert in den Sachposten gebucht, wo Sie die Ergebnisse anzeigen können.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Anlage aus, für die Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **AfA-Bücher** aus.  
3. Wählen Sie das AfA-Buch aus, für das Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **Posten** aus.  
4. Wählen Sie im Feld **Anlagebuchungskategorie** eine Zeile mit **Abgang** aus, und wählen Sie dann die Aktion **Posten finden** aus.  
5. Wählen Sie auf der Seite **Posten finden** die Sachpostenzeile aus, und wählen Sie dann die Aktion **Zugehörige Posten anzeigen** aus.  

Die Seite **Sachposten** wird geöffnet, in dem Sie die Posten sehen können, die aus der Verkaufsbuchung resultieren.  

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/dispose-fixed-assets/)

## <a name="see-also"></a>Siehe auch

[Anlagen](fa-manage.md)  
[Einrichten von Anlagen](fa-setup.md)  
[So richten Sie Anlagen-Buchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Finanzen](finance.md)  
[Vorbereiten auf die Geschäftsabwicklung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Posten finden](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]