---
title: Anlagen neu klassieren | Microsoft Docs
description: Beschreibt, wie eine Anlage umgelagert wird, um sie mit anderen Anlagen aufzusplitten oder zu kombinieren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 08374662c35dfbdab85097b628a0e0691d75e794
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-split-or-combine-fixed-assets"></a>Übertragen, Teilen oder Kombinieren von Anlagen.
Das Anlagenumbuchungs-Blatt wird zum Transferieren, Aufteilen und/oder Zusammenfassen von Anlagen verwendet. Sie können die Ergebnisse der Anlagenumbuchung mit dem Bericht **Anlagenspiegel** anzeigen oder ausdrucken.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>So übertragen Sie eine Anlage an eine andere Kostenstelle.
Es kann erforderlich sein, Anlagen an andere Kostenstellen zu transferieren, wenn Sie z. B. eine Anlage in der Bauzeit in der Produktion aufstellen und nach der Fertigstellung in die Verwaltung transferieren.  

1. Richten Sie eine neue Anlage ein. Geben Sie die neue Kostenstelle im Feld **Abteilungscode** ein.
2. Weisen Sie der neuen Anlage ein Anlagen-AfA-Buch zu. Weitere Informationen finden Sie unter [Anschaffen von Anlagen](fa-how-acquire.md).
3. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlage Buchblatt neu klassieren** ein und wählen den zugehörenden Link aus.
4. Erstellt das Umlagerungs Buch.-Blatt, in dem das **Anlagennr.** Feld die urspr. Anlage enthält, und das Feld **Neue Anlagennr.** die neue Anlage enthält, die verschoben werden soll.  
5. Wählen Sie die Aktion **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Buch.-Blatt unter Verwendung der Vorlage und dem Buch.-Blattnamen, die Sie in dem Fenster **Anlagen Buch.-Blatt Einr.** für das gewählte AfA-Buch angegeben haben, erstellt. Weitere Informationen finden Sie unter [Anlagen-AfA-Bücher automatisch einrichten](fa-how-setup-depreciation.md).
6. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.    
7. Im Fenster **Anlagen Fibu Buch.-Blatt** wählen Sie die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 4 und 5 ausgeführt haben.

Falls Sie Anschaffungskosten für eine Anlage gebucht haben, können Sie das Anlagen Umbuch.-Blatt verwenden, um die Anschaffungskosten auf mehrere Anlagen aufzuteilen.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>So teilen Sie eine Anlage in drei Anlagen
Sie können eine Anlage in mehrere Anlagen aufteilen, zum Beispiel wenn Sie eine Anlage auf drei verschiedene Abteilungen verteilen müssen. In diesem Fall können Sie z. B. 25 Prozent der Anschaffungskosten und der AfA der ursprünglichen Anlage auf die zweite Anlage buchen und 45 Prozent auf die dritte Anlage. Die restlichen 30 Prozent verbleiben bei der ursprünglichen Anlage.

1. Richten Sie zwei neue Anlagen ein. Geben Sie die neue Kostenstelle im Feld **Abteilungscode** ein.
2. Weisen Sie den zwei neuen Anlagen Anlagen-AfA-Bücher zu. Weitere Informationen finden Sie unter [Anschaffen von Anlagen](fa-how-acquire.md).
3. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlage Buchblatt neu klassieren** ein und wählen den zugehörenden Link aus.
4. Erstellen Sie zwei Umlagerungs Buch.-Blattzeilen, eine für jede neue Anlage.
5. Wählen Sie in der ersten Zeile die zweiten Anlage im Feld **Neue Anlagennr.** und 25 im Feld **Buchen Sie Anschaffungskosten um %** Feld ein.
6. Wählen Sie in der ersten Zeile die zweiten Anlage im Feld **Neue Anlagennr.** und 40 im Feld **Buchen Sie Anschaffungskosten um %** Feld ein.
7. In beiden Zeilen aktivieren Sie die Kontrollkästchen **Anschaffung umbuchen** und **Normal-AfA umbuchen**.   
8. Wählen Sie die Aktion **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Buch.-Blatt unter Verwendung der Vorlage und dem Buch.-Blattnamen, die Sie in dem Fenster **Anlagen Buch.-Blatt Einr.** für das gewählte AfA-Buch angegeben haben, erstellt. Weitere Informationen finden Sie unter [Anlagen-AfA-Bücher automatisch einrichten](fa-how-setup-depreciation.md).    
9. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.
10. Wählen Sie im Fenster **Anlagen Fibu Buch.-Blatt** die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 4 bis 8 ausgeführt haben.

## <a name="to-combine-two-fixed-assets-into-one"></a>So fassen Sie zwei Anlagen in einer zusammen
Sie können mehrere Anlage in einer Anlagen zusammenfassen, wenn Sie zum Beispiel verteilte Anlagen in eine Abteilung verschieben. Wenn Sie Anschaffungskosten und AfA für die Anlagen, die verschoben werden sollen, gebucht haben, werden diese Werte in einer einzelnen Anlage zusammengefasst.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlage Buchblatt neu klassieren** ein und wählen den zugehörenden Link aus.
2. Erstellt das Umlagerungs Buch.-Blatt, in dem das **Anlagennr.** Feld die urspr. Anlage enthält, und das Feld **Neue Anlagennr.** die neue Anlage enthält, die verschoben werden soll.
3. Lassen Sie das Feld **Anschaffung % umbuchen** leer, um die gesamten Anschaffungskosten zu verschieben/zusammenzufassen.    
4. Aktivieren Sie die Kontrollkästchen **Anschaffung umbuchen** und **Normal-AfA umbuchen**.
5. Wählen Sie auf der Registerkarte **Aktionen** die Option **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Buch.-Blatt unter Verwendung der Vorlage und dem Buch.-Blattnamen, die Sie in dem Fenster **Anlagen Buch.-Blatt Einr.** für das gewählte AfA-Buch angegeben haben, erstellt. Weitere Informationen finden Sie unter [Anlagen-AfA-Bücher automatisch einrichten](fa-how-setup-depreciation.md).   
6. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen G/L-Buchblatt** ein und wählen den zugehörenden Link aus.
7. Wählen Sie im Fenster **Anlagen Fibu Buch.-Blatt** die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 2 bis 5 ausgeführt haben.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>So zeigen Sie geänderte AfA-Buch-Werte aufgrund von Anlagenumbuchung an
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlage Buchblatt neu klassieren** ein und wählen den zugehörenden Link aus.
2. Füllen Sie die Felder je nach Bedarf aus.
3. Klicken Sie auf die Schaltfläche **Drucken** oder **Vorschau**.  

## <a name="see-also"></a>Siehe auch
[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Erste Schritte](product-get-started.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

