---
title: "So geht's: Buchhaltungsperioden schließen |Microsoft Docs"
description: "Erklärt, wie Buchhaltungsperioden abgeschlossen werden."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 69bea225084f239523c4ed67471b52ad91e914d9
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# So geht's: Buchhaltungsperioden schließen
<a id="how-to-close-accounting-periods" class="xliff"></a>
Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden.

## Buchhaltungsperioden schließen:
<a id="to-close-accounting-periods" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen.") Geben Sie **Buchungsperioden** ein und wählen Sie dann den entsprechenden Link aus.
2. Im Fenster **Buchhaltungsperioden** wählen Sie die Aktion **Jahr abschließen**.

    Sind mehrere Geschäftsjahre offen, wird angenommen, dass das früheste automatisch abgeschlossen werden soll. Ein Mitteilungsfenster wird angezeigt, in dem das zu schließende Jahr angegeben wird und die Konsequenzen erklärt werden.
3. Wählen Sie die Schaltfläche **Ja** aus, um das Jahr zu schließen.

Das Geschäftsjahr ist geschlossen und die Felder **Abgeschlossen** und **Datum gesperrt** werden für alle Perioden des Jahres aktiviert. Das Geschäftsjahr kann nicht erneut geöffnet werden und Sie können das Häkchen aus den Feldern **Abgeschlossen** oder **Datum gesperrt** nicht mehr entfernen.

**Hinweis:** Sie können ein Geschäftsjahr erst abschließen, wenn Sie ein neues erstellt haben. Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.

Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden. In diesen Fällen wird in den Posten vermerkt, dass die Buchung in einem abgeschlossenen Geschäftsjahr erfolgte, d. h., das Feld **Nachbuchung** wird mit einem Häkchen versehen.

Nachdem ein Geschäftsjahr abgeschlossen wurde, müssen Sie die GuV-Kontennullstellung durchführen und das Ergebnis auf ein Bilanzkonto übertragen lassen. Dies können das jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Schließen der Bücher](year-close-books.md)  
[Vorgehensweise: Buchen des Jahresabschlusspostens](year-how-post-year-end-close-entry.md)  
[So geht's: Ein neues Geschäftsjahr eröffnen](finance-how-open-new-fiscal-year.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

