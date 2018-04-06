---
title: "Abschließen der Buchhaltungsperioden für ein Geschäftsjahr | Microsoft Docs"
description: "Beschreibt, wie Sie die Buchhaltungsperioden schließen, die das Geschäftsjahr ausmachen."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23a9cd7a8a7f579f63937ac4fc28e6d4958f3f9a
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="close-accounting-periods"></a>Schließen von Buchhaltungsperioden
Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden.

## <a name="to-close-accounting-periods"></a>Buchhaltungsperioden schließen:
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Buchungsperioden** ein. Wählen Sie dann den zugehörigen Link aus.
2. Im Fenster **Buchhaltungsperioden** wählen Sie die Aktion **Jahr abschließen**.

    Sind mehrere Geschäftsjahre offen, wird angenommen, dass das früheste automatisch abgeschlossen werden soll. Ein Mitteilungsfenster wird angezeigt, in dem das zu schließende Jahr angegeben wird und die Konsequenzen erklärt werden.
3. Wählen Sie die Schaltfläche **Ja** aus, um das Jahr zu schließen.

Das Geschäftsjahr ist geschlossen und die Felder **Abgeschlossen** und **Datum gesperrt** werden für alle Perioden des Jahres aktiviert. Das Geschäftsjahr kann nicht erneut geöffnet werden und Sie können das Häkchen aus den Feldern **Abgeschlossen** oder **Datum gesperrt** nicht mehr entfernen.

> [!NOTE]  
>   Sie können ein Geschäftsjahr erst abschließen, wenn Sie ein neues erstellt haben. Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.

Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden. In diesen Fällen wird in den Posten vermerkt, dass die Buchung in einem abgeschlossenen Geschäftsjahr erfolgte, d. h., das Feld **Nachbuchung** wird mit einem Häkchen versehen.

Nachdem ein Geschäftsjahr abgeschlossen wurde, müssen Sie die GuV-Kontennullstellung durchführen und das Ergebnis auf ein Bilanzkonto übertragen lassen. Dies können das jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.

## <a name="see-also"></a>Siehe auch
[Schließen der Bücher](year-close-books.md)  
[So buchen Sie den Jahresabschlussposten](year-how-post-year-end-close-entry.md)  
[Ein neues Geschäftsjahres eröffnen](finance-how-open-new-fiscal-year.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

