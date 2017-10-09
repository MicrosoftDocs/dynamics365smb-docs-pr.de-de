---
title: "Vorgehensweise: Buchen und überprüfen des Jahresabschlusspostens | Microsoft Docs"
description: "Beschreibt, wie Sie das Buchblatt öffnen, dass Sie in der Stapelverarbeitung \"GuV-Konten Nullstellung\" definier haben und dann den Jahresabschlusseintrag überprüfen und buchen."
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
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 68017b8b031ee4bd368936b6fb4de157328d7030
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-the-year-end-closing-entry"></a>Vorgehensweise: Buchen des Jahresabschlusspostens
Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.

## <a name="to-post-the-year-end-closing-entry"></a>So buchen Sie den Jahresabschlussposten
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite ober Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Fibu Buch.Blatt** im Feld **Buch.-Blattname** das Buch.-Blatt mit den Abschlussposten aus.
3. Überprüfen Sie die Posten.
4. Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Buch.-Blatt zu buchen.

> [!NOTE]  
>   Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt. Wurde die Buchung ordnungsgemäß durchgeführt, werden die gebuchten Posten aus dem Buch.-Blatt entfernt. Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes GuV-Konto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.

## <a name="see-also"></a>Siehe auch
[So geht's: Buchhaltungsperioden schließen](year-close-account-periods.md)  
[Schließen der Bücher](year-close-books.md)  
[GuV-Konten Nullstellung](year-close-income-statement.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

