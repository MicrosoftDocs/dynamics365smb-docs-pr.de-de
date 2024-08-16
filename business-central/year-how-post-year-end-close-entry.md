---
title: Buchen Sie den Jahresabschlussposten
description: 'Beschreibt, wie Sie das Buchblatt öffnen, dass Sie in der Stapelverarbeitung "GuV-Konten Nullstellung" definier haben und dann den Jahresabschlusseintrag überprüfen und buchen.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: 100
ms.date: 08/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="post-the-year-end-closing-entry"></a>Buchen Sie den Jahresabschlussposten

Nachdem Sie die Stapelverarbeitung **GuV-Konten Nullstellung** ausgeführt haben, um den bzw. die Ultimoposten für den Jahresabschluss zu generieren, müssen Sie das in der Stapelverarbeitung angegebene Buchungsblatt öffnen und die Posten überprüfen und buchen.  

> [!TIP]
> Abhängig von den Arbeitsprozessen Ihres Unternehmens können Sie wählen, ob Abrechnungsperioden und Geschäftsjahre in [!INCLUDE [prod_short](includes/prod_short.md)] geschlossen werden sollen oder nicht. Das folgende Verfahren setzt voraus, dass Sie das Geschäftsjahr mit der Option *Buchhaltungsperioden* abgeschlossen haben, einen Jahresabschlusseintrag mit dem Batch-Job **Gewinn- und Verlustrechnung schließen** generiert haben und nun bereit sind, den Abschlusseintrag zum Jahresende zusammen mit den Gegenbuchungen des Eigenkapitalkontos zu buchen. Ihre Organisation kann sich dafür entscheiden, anders zu arbeiten, z. B. den Abschluss zum Jahresende als Teil des Abschlusses des Geschäftsjahres zu veröffentlichen.

## <a name="to-post-the-year-end-closing-entry"></a>So buchen Sie den Jahresabschlussposten

1. Wählen Sie das ![Glühbirne, die das „Sie wünschen ...“-Feature öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Allgemeine Erfassungen** ein, und wählen Sie dann den entsprechenden Link.
2. Geben Sie auf der Seite  **Allgemeine Journale**  im Feld  **Stapelname**  Auswählen den Stapel ein, der die Abschlussbuchungen enthält.
3. Überprüfen Sie die Posten.
4. Wählen Sie auf der Registerkarte **Start** die Option Buchen aus, um das Buch.-Blatt zu buchen.

> [!NOTE]  
> Wenn ein Fehler erkannt wird, wird eine Fehlermeldung angezeigt. Wurde die Buchung ordnungsgemäß durchgeführt, werden die gebuchten Posten aus dem Buch.-Blatt entfernt. Nachdem die Buchung abgeschlossen ist, wird ein Posten auf jedes GuV-Konto gebucht, sodass der Saldo des Kontos Null ist und das Jahresergebnis in die Bilanz übertragen wird.

## <a name="see-also"></a>Siehe auch

[Abrechnungszeiträume schließen](year-close-account-periods.md)    
[Bücher schließen](year-close-books.md)    
[Gewinn- und Verlustrechnung schließen](year-close-income-statement.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
