---
title: Abschließen der Buchhaltungsperioden für ein Geschäftsjahr | Microsoft Docs
description: Beschreibt, wie Sie die Buchhaltungsperioden schließen, die das Geschäftsjahr ausmachen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 336c6c8a4596aae26846d6a06091b6f5c4fff970
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386274"
---
# <a name="close-accounting-periods"></a>Schließen von Buchhaltungsperioden
Wenn ein Geschäftsjahr vorbei ist, müssen die Perioden, aus denen es besteht, geschlossen werden.

## <a name="to-close-accounting-periods"></a>Buchhaltungsperioden schließen:
1. Wählen Sie das Symbol ![Glühbirne, die die Tell Me Funktion öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Buchhaltungsperioden** ein und wählen Sie dann die entsprechende Verknüpfung.
2. Wählen Sie auf der Seite **Buchhaltungsperioden** die Aktion **Jahr auswählen** aus.

    Sind mehrere Geschäftsjahre offen, wird angenommen, dass das früheste automatisch abgeschlossen werden soll. Ein Mitteilungsfenster wird angezeigt, in dem das zu schließende Jahr angegeben wird und die Konsequenzen erklärt werden.
3. Wählen Sie die Schaltfläche **Ja** aus, um das Jahr zu schließen.

Das Geschäftsjahr ist geschlossen und die Felder **Abgeschlossen** und **Datum gesperrt** werden für alle Perioden des Jahres aktiviert. Das Geschäftsjahr kann nicht erneut geöffnet werden und Sie können das Häkchen aus den Feldern **Abgeschlossen** oder **Datum gesperrt** nicht mehr entfernen.

> [!NOTE]  
>   Sie können ein Geschäftsjahr erst abschließen, wenn Sie ein neues erstellt haben. Beachten Sie, dass Sie nach dem Abschluss eines Geschäftsjahres das Startdatum des folgenden Geschäftsjahres nicht mehr ändern können.

Auch wenn ein Geschäftsjahr abgeschlossen wurde, können hierfür noch Sachposten gebucht werden. In diesen Fällen wird in den Posten vermerkt, dass die Buchung in einem abgeschlossenen Geschäftsjahr erfolgte, d. h., das Feld **Nachbuchung** wird mit einem Häkchen versehen.

Nachdem ein Geschäftsjahr abgeschlossen wurde, müssen Sie die GuV-Kontennullstellung durchführen und das Ergebnis auf ein Bilanzkonto übertragen lassen. Dies können das jedes Mal wiederholen, wenn Sie in ein abgeschlossenes Geschäftsjahr gebucht haben.

## <a name="see-also"></a>Siehe auch

[Schließen der Bücher](year-close-books.md)  
[Jahresabschlussbuchung buchen](year-how-post-year-end-close-entry.md)  
[Arbeiten mit Buchhaltungsperioden und Geschäftsjahren](finance-accounting-periods-and-fiscal-years.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]