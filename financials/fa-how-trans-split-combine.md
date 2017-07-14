---
title: "Beschreibt, wie Anlagen übertragen, geteilt oder kombiniert werden| Microsoft Docs"
description: Beschreibt, wie eine Anlage umgelagert wird, um sie mit anderen Anlagen aufzusplitten oder zu kombinieren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/29/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 50e1a8d7012394b4b3f710991f7d45ae244656c9
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So geht's: Übertragen, Teilen oder Kombinieren von Anlagen.
<a id="how-to-transfer-split-or-combine-fixed-assets" class="xliff"></a>
Das Anlagenumbuchungs-Blatt wird zum Transferieren, Aufteilen und/oder Zusammenfassen von Anlagen verwendet. Sie können die Ergebnisse der Anlagenumbuchung mit dem Bericht **Anlagenspiegel** anzeigen oder ausdrucken.

## So übertragen Sie eine Anlage an eine andere Kostenstelle.
<a id="to-transfer-a-fixed-asset-to-a-different-department" class="xliff"></a>
Es kann erforderlich sein, Anlagen an andere Kostenstellen zu transferieren, wenn Sie z. B. eine Anlage in der Bauzeit in der Produktion aufstellen und nach der Fertigstellung in die Verwaltung transferieren.  

1. Richten Sie eine neue Anlage ein. Geben Sie die neue Kostenstelle im Feld **Abteilungscode** ein.
2. Weisen Sie der neuen Anlage ein Anlagen-AfA-Buch zu. Weitere Informationen finden Sie unter [So geht's: Beschaffen von Anlagen](fa-how-acquire.md).
3. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link aus.
4. Erstellen Sie ein Umbuch.-Blatt erstellt, in dem das Feld **Anlagennr.** die ursprüngliche Anlage enthält und das Feld **Neue Anlagennr.** die neue Anlage enthält, die umgelagert werden soll.  
5. Wählen Sie die Aktion **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Buch.-Blatt unter Verwendung der Vorlage und dem Buch.-Blattnamen, die Sie in dem Fenster **Anlagen Buch.-Blatt Einr.** für das gewählte AfA-Buch angegeben haben, erstellt. Weitere Informationen finden Sie unter [So geht's: Anlagen-AfA-Bücher automatisch einrichten](fa-how-setup-depreciation.md).
6. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen-Journalkonto** ein und wählen Sie dann den entsprechenden Link aus.    
7. Im Fenster **Anlagen Fibu Buch.-Blatt** wählen Sie die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 4 und 5 ausgeführt haben.

Falls Sie Anschaffungskosten für eine Anlage gebucht haben, können Sie das Anlagen Umbuch.-Blatt verwenden, um die Anschaffungskosten auf mehrere Anlagen aufzuteilen.  

## So teilen Sie eine Anlage in drei Anlagen
<a id="to-split-a-fixed-asset-into-three-fixed-assets" class="xliff"></a>
Sie können eine Anlage in mehrere Anlagen aufteilen, zum Beispiel wenn Sie eine Anlage auf drei verschiedene Abteilungen verteilen müssen. In diesem Fall können Sie z. B. 25 Prozent der Anschaffungskosten und der AfA der ursprünglichen Anlage auf die zweite Anlage buchen und 45 Prozent auf die dritte Anlage. Die restlichen 30 Prozent verbleiben bei der ursprünglichen Anlage.

1. Richten Sie zwei neue Anlagen ein. Geben Sie die neue Kostenstelle im Feld **Abteilungscode** ein.
2. Weisen Sie den zwei neuen Anlagen Anlagen-AfA-Bücher zu. Weitere Informationen finden Sie unter [So geht's: Beschaffen von Anlagen](fa-how-acquire.md).
3. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link aus.
4. Erstellen Sie zwei Umlagerungs Buch.-Blattzeilen, eine für jede neue Anlage.
5. Geben Sie in der ersten Zeile die zweite Anlage im Fenster **Neue Anlagennr.** ein und 25 und im Fenster **Anschaffung % umbuchen**.
6. Geben Sie in der zweiten Zeile die dritte Anlage im Fenster **Neue Anlagennr.** ein und 40 und im Fenster **Anschaffung % umbuchen**.
7. In beiden Zeilen aktivieren Sie die Kontrollkästchen **Anschaffung umbuchen** und **Normal-AfA umbuchen**.   
8. Wählen Sie die Aktion **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Buch.-Blatt unter Verwendung der Vorlage und dem Buch.-Blattnamen, die Sie in dem Fenster **Anlagen Buch.-Blatt Einr.** für das gewählte AfA-Buch angegeben haben, erstellt. Weitere Informationen finden Sie unter [So geht's: Anlagen-AfA-Bücher automatisch einrichten](fa-how-setup-depreciation.md).    
9. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen-Journalkonto** ein und wählen Sie dann den entsprechenden Link aus.
10. Wählen Sie im Fenster **Anlagen Fibu Buch.-Blatt** die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 4 bis 8 ausgeführt haben.

## So fassen Sie zwei Anlagen in einer zusammen
<a id="to-combine-two-fixed-assets-into-one" class="xliff"></a>
Sie können mehrere Anlage in einer Anlagen zusammenfassen, wenn Sie zum Beispiel verteilte Anlagen in eine Abteilung verschieben. Wenn Sie Anschaffungskosten und AfA für die Anlagen, die verschoben werden sollen, gebucht haben, werden diese Werte in einer einzelnen Anlage zusammengefasst.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link aus.
2. Erstellen Sie ein Umbuch.-Blatt erstellt, in dem das Feld **Anlagennr.** die Anlage enthält, die verschoben/zusammengefasst werden soll und das Feld **Neue Anlagennr.** enthält die Anlage, mit der sie zusammengefasst wird.
3. Lassen Sie das Feld **Anschaffung % umbuchen** leer, um die gesamten Anschaffungskosten zu verschieben/zusammenzufassen.    
4. Aktivieren Sie die Kontrollkästchen **Anschaffung umbuchen** und **Normal-AfA umbuchen**.
5. Wählen Sie auf der Registerkarte **Aktionen** die Option **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Buch.-Blatt unter Verwendung der Vorlage und dem Buch.-Blattnamen, die Sie in dem Fenster **Anlagen Buch.-Blatt Einr.** für das gewählte AfA-Buch angegeben haben, erstellt. Weitere Informationen finden Sie unter [So geht's: Anlagen-AfA-Bücher automatisch einrichten](fa-how-setup-depreciation.md).   
6. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen-Journalkonto** ein und wählen Sie dann den entsprechenden Link aus.
7. Wählen Sie im Fenster **Anlagen Fibu Buch.-Blatt** die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 2 bis 5 ausgeführt haben.

## So zeigen Sie geänderte AfA-Buch-Werte aufgrund von Anlagenumbuchung an
<a id="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen"). Geben Sie **Anlagen-Buchwert 02** ein und wählen Sie dann den entsprechenden Link aus.
2. Füllen Sie die Felder je nach Bedarf aus.
3. Klicken Sie auf die Schaltfläche **Drucken** oder **Vorschau**.  

## Siehe auch
<a id="see-also" class="xliff"></a>
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

