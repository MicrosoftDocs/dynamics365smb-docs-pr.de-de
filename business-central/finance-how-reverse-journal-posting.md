---
title: Rückgängigmachen einer Buchung durch Buchung einer Rückbuchung | Microsoft Docs
description: Wenn Sie fehlerhafte Buchungen im Fibu Buch.-Blatt vorgenommen haben, können Sie die Funktion verwenden, um die korrekte Buchung mit einem Protokoll zu stornieren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9a8a7967bdb0947fbfb0b86cc073fc4f96ea0595
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3920585"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Buchungen stornieren und Belege/Lieferungen rückgängig machen
Zum Stornieren (Rückgängig machen) fehlerhafter Buch.-Blattbuchungen wählen Sie einen Posten und erstellen einen Korrekturposten (ein Posten, die mit dem ursprünglichen Posten identisch ist, jedoch im Betragsfeld ein umgekehrtes Vorzeichen aufweist) mit derselben Belegnummer und demselben Belegdatum wie der ursprüngliche Posten. Nachdem Sie einen Posten storniert haben, müssen Sie den Korrekturposten erstellen.

Storniert werden können nur Posten, die in eine Zeile eines Fibu Buch.-Blattes gebucht wurden. Ein Posten kann nur einmal storniert werden.

Um eine Quittung oder Sendungsbuchung rückgängig zu machen, bevor sie als Rechnung gebucht werden, können Sie die **Rückgängig machen** Funktion auf dem gebuchten Beleg nutzen. Sie können Mengen des Typs **Artikel** und **Ressource** rückgängig machen.

Wenn Sie eine inkorrekte negative Mengenbuchung durchgeführt haben, das heißt, wenn Sie eine Einkaufsbestellung mit der falschen Artikelmenge erstellt und als Wareneingang gebucht (aber nicht fakturiert) haben, können Sie die Buchung dann umkehren.

Wenn Sie eine inkorrekte positive Mengenbuchung durchgeführt haben, wie eine Verkaufslieferung oder eine Rücklieferung mit der falschen Artikelmenge erstellt und als Warenausgang gebucht (aber nicht fakturiert) haben, können Sie die Buchung umkehren.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Um die Buch.-Blatt-Buchung eines Sachpostens zu stornieren
Posten können in allen Seiten **Posten** storniert werden. Das folgende Verfahren basiert auf der Seite **Sachposten** .
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Sachposten** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Posten, den Sie stornieren möchten, und wählen die **Transaktion stornieren** Aktion aus. Beachten Sie, das sie aus einer Buch.-Blatt-Buchung stammen muss.
3. Auf der Seite **Transaktionsposten stornieren** wählen Sie die Aktion **Stornieren** aus.
4. Klicken Sie auf die Schaltfläche **Ja** auf der Bestätigungsnachricht.

> [!NOTE]
> Sie können keine Buchungen stornieren, die mit Informationen aus einem Auftrag gebucht wurden oder die Gewinne und Verluste innerhalb derselben Transaktion realisiert haben.

## <a name="to-post-a-negative-entry"></a>So buchen Sie einen negativen Posten  
Im Feld **Storno** kann ein negativer Soll- anstelle eines Habenbetrags oder ein negativer Haben- anstelle eines Sollbetrags in einem Konto gebucht werden. Zur Einhaltung gesetzlicher Vorschriften wird das Feld standardmäßig in allen Buch.-Blättern angezeigt. Die Felder **Sollbetrag** und **Habenbetrag** enthalten jeweils den ursprünglichen und den stornierten Posten. Diese Felder haben keinen Einfluss auf den Kontensaldo.  

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Fibu Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link  
2.  Wählen Sie im Feld **Buch.-Blattname** den erforderlichen Buch.-Blattnamen aus.  
3.  Geben Sie die Informationen in die entsprechenden Felder ein.  
4.  Aktivieren Sie in der Buch.-Blattzeile, die Sie für negative Posten aktivieren möchten, das Kontrollkästchen **Storno** .  
5.  Prüfen Sie die erstellten Posten und wählen Sie dann die Aktion **Buchen** und dann **Ja** aus.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>So stornieren Sie eine Mengenbuchung einer gebuchten Einkaufslieferzeile  
Im Folgenden wird beschrieben, wie Sie einen gebuchten Beleg von Artikeln oder Ressourcen rückgängig machen. Die Schritte sind ähnlich wie für eine Einkaufsbestellung.

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Gebuchte Einkaufsbelege** ein und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie die gebuchte Lieferung, den Sie rückgängig machen möchten.  
3.  Wählen Sie die Zeile oder Zeilen aus, die Sie rückgängig machen möchten.  
4.  Wählen Sie die Aktion **Wareneingang stornieren** aus.

Eine Korrekturzeile wird unter der ausgewählten Lieferzeile eingefügt. Wenn die Menge in einem Wareneingang eingegangen ist, wird eine Korrekturzeile auf dem gebuchten Wareneingang eingefügt.  

Die Felder **Bereits gelief. Menge** und **Lief. nicht fakt. Menge** auf der zugehörigen Bestellung werden auf Null gesetzt.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Eine Mengenbuchung einer gebuchter Rücklieferungen stornieren und wiederholen
Im Folgenden wird beschrieben, wie Sie eine gebuchte Rücksendung von Artikeln und Ressourcen rückgängig machen und anschließend die Kaufrücksendung mit einer neuen Menge umbuchen. Die Schritte sind denen der gebuchten Rücksendungen ähnlich.

1.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Gebuchte Rücklieferungen** ein, und wählen Sie dann den zugehörigen Link.  
2.  Öffnen Sie die gebuchte Rücklieferung, den Sie rückgängig machen möchten.
3. Wählen Sie die Zeile oder Zeilen aus, die Sie rückgängig machen möchten.  

4.  Wählen Sie die Aktion **Rücklieferung stornieren** .  

    Eine Korrekturzeile wird in den gebuchten Beleg eingefügt, und die Mengen, die in der Reklamation in den Feldern **Rücklieferungsmenge geliefert** und **Lief. n. fakt. Rückl.-Betrag** enthalten sind, werden auf Null gesetzt.  

    Gehen Sie jetzt zurück zu der Einkaufsreklamation, um die Buchung erneut durchzuführen.  

5.  Beachten Sie auf der Seite **Gebuchte Rücklieferung** die Nummer im Feld **Reklamationsnr.** . Feld eingetragen.  
6.  Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Einkaufsreklamationen** ein und wählen Sie dann den entsprechenden Link.  
7.  Öffnen Sie die betreffende Rücklieferung und wählen Sie die Aktion **Erneut öffnen** .  
8.  Korrigieren Sie den Eintrag im Feld **Menge** und buchen Sie die Rücklieferung erneut.  

## <a name="see-also"></a>Siehe auch
[Montagesbuchungen rückgängig machen](assembly-how-to-undo-assembly-posting.md)  
[Buchen von Transaktionen direkt in der Finanzbuchhaltung](finance-how-post-transactions-directly.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
