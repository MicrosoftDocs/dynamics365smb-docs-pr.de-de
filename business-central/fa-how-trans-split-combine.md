---
title: Anlagen umbuchen
description: 'Beschreibt, wie eine Anlage umgelagert wird, um sie mit anderen Anlagen aufzusplitten oder zu kombinieren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5638, 5636, 5640, 5637'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="transfer-split-or-combine-fixed-assets"></a>Übertragen, Teilen oder Kombinieren von Anlagen.

Das Anlagenumbuchungs-Blatt wird zum Transferieren, Aufteilen und/oder Zusammenfassen von Anlagen verwendet. Sie können die Ergebnisse der Anlagenumbuchung mit dem Bericht **Anlagenspiegel** anzeigen oder ausdrucken.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>So übertragen Sie eine Anlage an eine andere Kostenstelle.

Es kann erforderlich sein, Anlagen an andere Kostenstellen zu transferieren, wenn Sie z. B. eine Anlage in der Bauzeit in der Produktion aufstellen und nach der Fertigstellung in die Verwaltung transferieren.  

1. Richten Sie eine neue Anlage ein. Geben Sie die neue Abteilung als Dimension ein.  
2. Weisen Sie der neuen Anlage ein Anlagen-AfA-Buch zu. Weitere Informationen finden Sie unter [Erwerben von Anlagen](fa-how-acquire.md).
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen Umbuch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
4. Erstellen Sie eine Buch.-Blattzeilen, in der das Feld **Anlagennr.** die ursprüngliche Anlage enthält und das Feld **Neue Anlagennr.** die neue Anlage, die verschoben werden soll. Füllen Sie die anderen Felder aus entsprechend aus.  
5. Wählen Sie die Aktion **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Buch.-Blatt unter Verwendung der Vorlage und dem Buch.-Blattnamen, die Sie auf der Seite **Anlagen Buch.-Blatt Einr.** für das gewählte AfA-Buch angegeben haben, erstellt. Weitere Informationen finden Sie unter [Abschreibungen für Anlagen festlegen](fa-how-setup-depreciation.md).
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.    
7. Auf der Seite **Anlagen Fibu Buch.-Blatt** wählen Sie die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 4 und 5 ausgeführt haben.

Falls Sie Anschaffungskosten für eine Anlage gebucht haben, können Sie das Anlagen Umbuch.-Blatt verwenden, um die Anschaffungskosten auf mehrere Anlagen aufzuteilen.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>So teilen Sie eine Anlage in drei Anlagen
Sie können eine Anlage in mehrere Anlagen aufteilen, zum Beispiel wenn Sie eine Anlage auf drei verschiedene Abteilungen verteilen müssen. In diesem Fall können Sie z. B. 25 Prozent der Anschaffungskosten und der AfA der ursprünglichen Anlage auf die zweite Anlage buchen und 45 Prozent auf die dritte Anlage. Die restlichen 30 Prozent verbleiben bei der ursprünglichen Anlage.

1. Richten Sie zwei neue Anlagen ein. Geben Sie die relevanten Abteilungen als Dimensionen ein.  
2. Weisen Sie den zwei neuen Anlagen Anlagen-AfA-Bücher zu. Weitere Informationen finden Sie unter [Anlagen erwerben](fa-how-acquire.md).
3. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Anlagen Umbuch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
4. Erstellen Sie zwei Umlagerungs Buch.-Blattzeilen, eine für jede neue Anlage.
5. Wählen Sie in der ersten Zeile die zweiten Anlage im Feld **Neue Anlagennr.** und 25 im Feld **Buchen Sie Anschaffungskosten um %** Feld ein.
6. Wählen Sie in der ersten Zeile die zweiten Anlage im Feld **Neue Anlagennr.** und 40 im Feld **Buchen Sie Anschaffungskosten um %** Feld ein.
7. In beiden Zeilen aktivieren Sie die Kontrollkästchen **Anschaffung umbuchen** und **Normal-AfA umbuchen**.  
8. Wählen Sie die Aktion **Umbuchen** aus.  

    Es werden zwei Zeilen im Anlagen Fibu Buch.-Blatt unter Verwendung der Vorlage und dem Buch.-Blattnamen, die Sie auf der Seite **Anlagen Buch.-Blatt Einr.** für das gewählte AfA-Buch angegeben haben, erstellt. Weitere Informationen finden Sie unter [Abschreibungen für Anlagen festlegen](fa-how-setup-depreciation.md).    
9. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagen Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.
10. Auf der Seite **Anlagen Fibu Buch.-Blatt** wählen Sie die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 4 und 8 ausgeführt haben.

## <a name="to-combine-two-fixed-assets-into-one"></a>So fassen Sie zwei Anlagen in einer zusammen

Sie können mehrere Anlage in einer Anlagen zusammenfassen, wenn Sie zum Beispiel verteilte Anlagen in eine Abteilung verschieben. Wenn Sie Anschaffungskosten und AfA für die Anlagen, die verschoben werden sollen, gebucht haben, werden diese Werte in einer einzelnen Anlage zusammengefasst.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagen Umbuch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Erstellt das Umlagerungs Buch.-Blatt, in dem das **Anlagennr.** Feld die urspr. Anlage enthält, und das Feld **Neue Anlagennr.** die neue Anlage enthält, die verschoben werden soll.
3. Lassen Sie das Feld **Anschaffung % umbuchen** leer, um die gesamten Anschaffungskosten zu verschieben/zusammenzufassen.  
4. Aktivieren Sie die Kontrollkästchen **Anschaffung umbuchen** und **Normal-AfA umbuchen**.
5. Wählen Sie die Aktion **Umbuchen** aus.

    Es werden zwei Zeilen im Anlagen Fibu Buch.-Blatt unter Verwendung der Vorlage und dem Buch.-Blattnamen, die Sie auf der Seite **Anlagen Buch.-Blatt Einr.** für das gewählte AfA-Buch angegeben haben, erstellt. Weitere Informationen finden Sie unter [Abschreibungen für Anlagen festlegen](fa-how-setup-depreciation.md).   
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagen-Fibu Buch.-Blätter** ein, und wählen Sie dann den zugehörigen Link.
7. Auf der Seite **Anlagen Fibu Buch.-Blatt** wählen Sie die Aktion **Buchen** aus, um die Umlagerungen zu buchen, die Sie in Schritt 2 und 5 ausgeführt haben.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>So zeigen Sie geänderte AfA-Buch-Werte aufgrund von Anlagenumbuchung an

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Anlagenspiegel 02** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder nach Bedarf aus.
3. Wählen Sie die Schaltfläche **Drucken** oder **Vorschau**.  

## <a name="see-also"></a>Siehe auch

[Anlagen](fa-manage.md)  
[Einrichten von Anlagen](fa-setup.md)  
[Finanzen](finance.md)  
[Bereitschaft für die Geschäftsabwicklung](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
