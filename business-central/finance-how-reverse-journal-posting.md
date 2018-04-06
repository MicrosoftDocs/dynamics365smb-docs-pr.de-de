---
title: "Rückgängigmachen einer Buchung durch Buchung einer Rückbuchung | Microsoft Docs"
description: "Wenn Sie fehlerhafte Buchungen im Fibu Buch.-Blatt vorgenommen haben, können Sie die Funktion verwenden, um die korrekte Buchung mit einem Protokoll zu stornieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9a4a7001ab5a752bf2e2acdd273d2a584a1e0b8a
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="reverse-postings"></a>Buchungen stornieren
Zum Stornieren (Rückgängig machen) fehlerhafter Buch.-Blattbuchungen wählen Sie einen Posten und erstellen einen Korrekturposten (ein Posten, die mit dem ursprünglichen Posten identisch ist, jedoch im Betragsfeld ein umgekehrtes Vorzeichen aufweist) mit derselben Belegnummer und demselben Belegdatum wie der ursprüngliche Posten. Nachdem Sie einen Posten storniert haben, müssen Sie den Korrekturposten erstellen.

Storniert werden können nur Posten, die in eine Zeile eines Fibu Buch.-Blattes gebucht wurden. Ein Posten kann nur einmal storniert werden.

Weitere Informationen zum Buchen eines Fibu Buch.-Blatt, siehe [Transaktionen direkt in die Finanzbuchhaltung buchen](finance-how-post-transactions-directly.md).

Wenn Sie eine inkorrekte negative Mengenbuchung durchgeführt haben, das heißt, wenn Sie eine Einkaufsbestellung mit der falschen Artikelmenge erstellt und als Wareneingang gebucht (aber nicht fakturiert) haben, können Sie die Buchung umkehren.

Wenn Sie eine inkorrekte positive Mengenbuchung durchgeführt haben, das heißt, wenn Sie einen Rückgabeauftrag mit der falschen Artikelmenge erstellt und als Warenausgang gebucht (aber nicht fakturiert) haben, können Sie die Buchung umkehren.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Um die Buch.-Blatt-Buchung eines Sachpostens zu stornieren
Posten können in allen **Posten** storniert werden. Das folgende Verfahren basiert auf dem **Sachposten** Fenster.
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Finanzbuchhaltung einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den Posten, den Sie stornieren möchten, und wählen die **Transaktion stornieren** Aktion aus. Beachten Sie, das sie aus einer Buch.-Blatt-Buchung stammen muss.
3. Im Fenster **Transaktionsposten stornieren** wählen Sie den entsprechenden Posten, und wählen die **Stornieren** Aktion aus.
4. Klicken Sie auf die Schaltfläche **Ja** auf der Bestätigungsnachricht.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>So stornieren Sie eine Mengenbuchung einer gebuchten Einkaufslieferzeile  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Geb. Einkaufslieferungen** ein und wählen dann den zugehörigen Link aus.  
2.  Öffnen Sie die gebuchte Lieferung, den Sie rückgängig machen möchten.  
3.  Wählen Sie die Zeile oder Zeilen aus, die Sie rückgängig machen möchten.  
4.  Wählen Sie die Aktion **Wareneingang stornieren** aus.

    Eine Korrekturzeile wird unter der ausgewählten Lieferzeile eingefügt.  

    Wenn die Menge in einem Wareneingang eingegangen ist, wird eine Korrekturzeile in den gebuchten Wareneingang eingefügt.  

    Die Felder **Bereits gelief. Menge** und **Lief. nicht fakt. Menge** auf der zugehörigen Bestellung werden auf Null gesetzt.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Eine Mengenbuchung einer gebuchter Rücklieferungen stornieren und wiederholen

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Gebuchte Rücklieferungen** ein und wählen dann den zugehörigen Link aus.  
2.  Öffnen Sie die gebuchte Rücklieferung, den Sie rückgängig machen möchten.
3. Wählen Sie die Zeile oder Zeilen aus, die Sie rückgängig machen möchten.  

4.  Wählen Sie die Aktion **Rücklieferung stornieren**.  

    Eine Korrekturzeile wird in den gebuchten Beleg eingefügt, und die Mengen, die in der Reklamation in den Feldern **Rücklieferungsmenge geliefert** und **Lief. n. fakt. Rückl.-Betrag** enthalten sind, werden auf Null gesetzt.  

    Gehen Sie jetzt zurück zu der Einkaufsreklamation, um die Buchung erneut durchzuführen.  

5.  Beachten Sie im Fenster **Gebuchte Rücklieferung** die Nummer im Feld **Reklamationsnr.**. Feld  
6.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Einkaufsreklamationen** ein und wählen dann den zugehörigen Link aus.  
7.  Öffnen Sie die betreffende Rücklieferung und wählen Sie die Aktion **Erneut öffnen**.  
8.  Korrigieren Sie den Eintrag im Feld **Menge** und buchen Sie die Rücklieferung erneut.  

## <a name="to-post-a-negative-entry"></a>So buchen Sie einen negativen Posten  
Im Feld **Storno** kann ein negativer Soll- anstelle eines Habenbetrags oder ein negativer Haben- anstelle eines Sollbetrags in einem Konto gebucht werden. Zur Einhaltung gesetzlicher Vorschriften wird das Feld standardmäßig in allen Buch.-Blättern angezeigt. Die Felder **Sollbetrag** und **Habenbetrag** enthalten jeweils den ursprünglichen und den stornierten Posten. Diese Felder haben keinen Einfluss auf den Kontensaldo.  

1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie im Feld **Buch.-Blattname** den erforderlichen Buch.-Blattnamen aus.  
3.  Geben Sie die Informationen in die entsprechenden Felder ein.  
4.  Aktivieren Sie in der Buch.-Blattzeile, die Sie für negative Posten aktivieren möchten, das Kontrollkästchen **Storno**.  
5.  Prüfen Sie die erstellten Posten und wählen Sie dann die Aktion **Buchen**  und dann **Ja**aus.

## <a name="see-also"></a>Siehe auch
[Buchen von Transaktionen direkt in der Finanzbuchhaltung](finance-how-post-transactions-directly.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

