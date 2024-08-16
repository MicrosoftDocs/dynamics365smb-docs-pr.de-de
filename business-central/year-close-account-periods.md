---
title: Buchhaltungsperioden für ein Geschäftsjahr schließen
description: 'Dieser Artikel beschreibt, wie Sie die Buchhaltungsperioden, aus denen das Geschäftsjahr besteht, für den Jahresabschluss schließen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: '100,'
ms.date: 08/05/2024
ms.service: dynamics-365-business-central
---

# <a name="close-accounting-periods"></a>Buchhaltungsperioden abschließen

Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden.

## <a name="to-close-accounting-periods"></a>Buchhaltungsperioden schließen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Buchhaltungsperioden** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Buchhaltungsperioden** die Aktion **Jahr auswählen** aus.

    Sind mehrere Geschäftsjahre offen, wird angenommen, dass das früheste automatisch abgeschlossen werden soll. In einer Mitteilung sind das Jahr, das abgeschlossen wird, und die Folgen des Abschlusses angegeben.
3. Wählen Sie die Schaltfläche **Ja** aus, um das Jahr zu schließen.

Das Geschäftsjahr ist geschlossen und die Felder **Abgeschlossen** und **Datum gesperrt** werden für alle Perioden des Jahres aktiviert. Das Geschäftsjahr kann nicht erneut geöffnet werden und Sie können die Häkchen aus den Feldern  **Geschlossen**  bzw.  **Sperrdatum**  nicht entfernen.

> [!NOTE]  
> Sie können ein Geschäftsjahr erst abschließen, wenn Sie ein neues erstellt haben. Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.

Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden. In diesen Fällen werden die Posten als in einem abgeschlossenen Geschäftsjahr gebucht gekennzeichnet, d. h., das Feld **Nachbuchung** ist ausgewählt.

Nachdem ein Geschäftsjahr abgeschlossen wurde, müssen Sie die GuV-Kontennullstellung durchführen und das Ergebnis auf ein Bilanzkonto übertragen lassen. Dies können das jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.

## <a name="see-also"></a>Siehe auch

[Bücher schließen](year-close-books.md)    
[Buchen des Jahresabschlusspostens](year-how-post-year-end-close-entry.md)    
[Arbeiten mit Abrechnungsperioden und Geschäftsjahren](finance-accounting-periods-and-fiscal-years.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
