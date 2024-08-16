---
title: Korrekte Vorauszahlungen
description: 'Sie können eine Korrektur an einem Auftrag vornehmen, nachdem Sie eine Vorauszahlungsrechnung für den Auftrag gebucht haben und neue Zeilen zu einem Auftrag hinzufügen, nachdem Sie eine Vorauszahlung ausgegeben haben.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '44, 48, 42, 50, 52, 9305, 9307'
ms.date: 07/24/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="correct-prepayments"></a>Korrekte Vorauszahlungen

Sie können eine Korrektur an einem Auftrag vornehmen, nachdem Sie eine Vorauszahlungsrechnung für den Auftrag gebucht haben. Sie können einer Bestellung nach der Leistung einer Vorauszahlung neue Positionen hinzufügen und anschließend eine weitere Vorauszahlungsrechnung buchen. Sie können jedoch keine Position aus einer Bestellung löschen, nachdem für die Position eine Vorauszahlung in Rechnung gestellt wurde.  

> [!TIP]
> Wenn Sie eine Vorauszahlungsrechnung für eine Verkaufsrechnung gebucht haben, die Sie dann korrigieren oder stornieren, müssen Sie auch die Vorauszahlung korrigieren oder stornieren.

## <a name="to-correct-a-prepayment"></a>So korrigieren Sie eine Vorauszahlung

Das folgende Verfahren zeigt, wie Sie eine Vorauszahlungsgutschrift ausstellen, um alle fakturierten Vorauszahlungen für einen Auftrag zu stornieren.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den entsprechenden Verkaufsauftrag.
3. Wählen Sie die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsgutschrift buchen** oder **Vorauszahlungsgutschrift buchen und drucken**.  
4. Korrigieren Sie auf der Seite **Verkaufsgutschrift** alle relevanten Positionen für alle Verkaufsgutschriften. Weitere Informationen finden Sie unter [Retouren verarbeiten oder Stornieren](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > Um den Betrag im Feld **Positionsbetrag** zu reduzieren, müssen Sie zuerst den Vorauszahlungsprozentsatz in der Zeile erhöhen, damit der Wert im Feld **Vorauszahlungszeilenbetrag** nicht unter den Wert im Feld **Fakt. Vorauszahlungsbetrag** fällt.

5. Um eine Vorauszahlungsrechnung für neuen Zeilen in der Vorauszahlungsgutschrift zu erstellen, wählen Sie die Aktion **Vorauszahlung**, und dann die Aktion **Vorauszahlungsrechnung buchen** oder **Vorauszahlungsrechnung buchen und drucken**.  
6. Um eine zusätzliche Vorauszahlungsrechnung zu erstellen, erhöhen Sie den Vorauszahlungsbetrag in einer oder mehreren Zeilen, und buchen die Vorauszahlungsrechnung. Für die Differenz zwischen dem fakturierten Vorauszahlungsbetrag und den neuen Vorauszahlungsbeträgen wird eine neue Rechnung erstellt.  

## <a name="see-also"></a>Siehe auch

[Vorauszahlungen fakturieren](finance-invoice-prepayments.md)  
[Beispielhafte Vorgehensweise: Verkaufsvorauszahlungen einrichten und in Rechnung stellen](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
