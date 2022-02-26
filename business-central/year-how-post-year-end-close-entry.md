---
title: So buchen Sie den Jahresabschlussposten
description: Beschreibt, wie Sie das Buchblatt öffnen, dass Sie in der Stapelverarbeitung "GuV-Konten Nullstellung" definier haben und dann den Jahresabschlusseintrag überprüfen und buchen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.search.form: 100
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 6290bf334e3b309f1b4ed3eec426e6b3f60d6041
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971758"
---
# <a name="posting-the-year-end-closing-entry"></a>Buchen der Jahresendabschlussbuchung

Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.  

> [!TIP]
> Abhängig von den Arbeitsprozessen Ihres Unternehmens können Sie wählen, ob Abrechnungsperioden und Geschäftsjahre in [!INCLUDE [prod_short](includes/prod_short.md)] geschlossen werden sollen oder nicht. Das folgende Verfahren setzt voraus, dass Sie das Geschäftsjahr mit der Option *Buchhaltungsperioden* abgeschlossen haben, einen Jahresabschlusseintrag mit dem Batch-Job **Gewinn- und Verlustrechnung schließen** generiert haben und nun bereit sind, den Abschlusseintrag zum Jahresende zusammen mit den Gegenbuchungen des Eigenkapitalkontos zu buchen. Ihre Organisation kann sich dafür entscheiden, anders zu arbeiten, z. B. den Abschluss zum Jahresende als Teil des Abschlusses des Geschäftsjahres zu veröffentlichen.

## <a name="to-post-the-year-end-closing-entry"></a>So buchen Sie den Jahresabschlussposten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Fibu Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie auf der Seite **Fibu Buch.Blatt** im Feld **Buch.-Blattname** das Buch.-Blatt mit den Abschlussposten aus.
3. Überprüfen Sie die Posten.
4. Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Buch.-Blatt zu buchen.

> [!NOTE]  
> Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt. Wurde die Buchung ordnungsgemäß durchgeführt, werden die gebuchten Posten aus dem Buch.-Blatt entfernt. Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes GuV-Konto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.

## <a name="see-also"></a>Siehe auch

[Schließen von Buchhaltungsperioden](year-close-account-periods.md)  
[Schließen der Bücher](year-close-books.md)  
[GuV-Konten Nullstellung](year-close-income-statement.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]