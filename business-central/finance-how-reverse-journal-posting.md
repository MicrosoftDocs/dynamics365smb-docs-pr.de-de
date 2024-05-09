---
title: Rückgängigmachen einer Buchung durch Buchung einer Umkehrbuchung
description: 'Wenn Sie fehlerhafte Buchungen im Fibu Buch.-Blatt finden, können Sie die Aktion Transaktion zurückbuchen verwenden, um die korrekte Buchung mit einem Protokoll zu stornieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Buchungen stornieren und Belege/Lieferungen rückgängig machen

Stornierte Journalbuchungen sind z.B. nützlich, um Fehler zu korrigieren und eine alte Erfassung zu löschen, bevor Sie eine neue erfassen. Eine stornierte Buchung ist die gleiche wie die ursprüngliche Buchung, hat aber ein umgekehrtes Vorzeichen im Feld **Betrag**. Die stornierte Buchung muss die gleiche Belegnummer und das gleiche Buchungsdatum haben wie die ursprüngliche Buchung. Nachdem Sie eine Buchung storniert haben, müssen Sie die richtige Buchung vornehmen.

Storniert werden können nur Posten, die in eine Zeile eines Fibu Buch.-Blattes gebucht wurden. Eine Buchung kann nur ein einziges Mal storniert werden.

Um eine Beleg- oder Versandbuchung rückgängig zu machen, bevor sie als Rechnung gebucht wird, können Sie die Funktion **Rückgängig** auf dem gebuchten Beleg verwenden. Sie können Mengen des Typs **Artikel** und **Ressource** rückgängig machen.

Wenn Sie eine falsche negative Menge, z.B. eine Bestellung mit der falschen Anzahl von Artikeln, als Eingang, aber nicht als Rechnung gebucht haben, können Sie diese Buchung rückgängig machen.

Wenn Sie eine falsche positive Menge gebucht haben, z.B. einen Verkaufslieferschein oder eine Gebuchte Rücklieferung mit der falschen Anzahl von Artikeln, als versandt, aber nicht in Rechnung gestellt, können Sie die Buchung rückgängig machen.

## Um die Buch.-Blatt-Buchung eines Sachpostens zu stornieren

Posten können in allen Seiten **Posten** storniert werden. Das folgende Verfahren basiert auf der Seite **Sachposten**.

> [!NOTE]
> Der Eintrag muss aus einer Journalbuchung stammen.
>
> Außerdem können Sie keine Buchungen rückgängig machen, die mit Informationen aus einem Projekt gebucht wurden oder die Gewinne und Verluste innerhalb derselben Transaktion realisiert haben.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Hauptbuchhaltungsposten** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Posten, den Sie stornieren möchten, und wählen die **Transaktion stornieren** Aktion aus.
3. Auf der Seite **Transaktionsposten stornieren** wählen Sie die Aktion **Stornieren** aus.
4. Wählen Sie **Ja**, um die Stornierung zu bestätigen.

## So buchen Sie einen negativen Posten  

Verwenden Sie das Feld **Korrektur**, um ein negatives Soll anstelle eines Guthabens zu buchen oder um ein negatives Haben anstelle eines Solls auf einem Konto zu buchen. Das Feld ist standardmäßig in allen Erfassungen verfügbar. Die Felder **Sollbetrag** und **Habenbetrag** enthalten jeweils den ursprünglichen und den stornierten Posten. Diese Felder haben keinen Einfluss auf den Kontensaldo.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Fibu Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link  
2. Wählen Sie im Feld **Buch.-Blattname** den erforderlichen Buch.-Blattnamen aus.  
3. Geben Sie die Informationen in die entsprechenden Felder ein.  
4. Aktivieren Sie in der Buch.-Blattzeile, die Sie für negative Posten aktivieren möchten, das Kontrollkästchen **Storno**.  
5. Prüfen Sie die erstellten Posten und wählen Sie dann die Aktion **Buchen** und dann **Ja** aus.

## So machen Sie eine Menge auf einem gebuchten Kauf-Eingang rückgängig  

Die folgenden Schritte beschreiben, wie Sie einen gebuchten Eingang von Artikeln oder Ressourcen rückgängig machen können. Die Schritte sind ähnlich wie für eine Einkaufsbestellung.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") Symbol. Geben Sie **Geb. Einkaufslieferungen** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die gebuchte Lieferung, den Sie rückgängig machen möchten.  
3. Wählen Sie die Zeile oder Zeilen aus, die Sie rückgängig machen möchten.  
4. Wählen Sie die Aktion **Wareneingang stornieren** aus.

Unter der ausgewählten Eingangszeile wird eine korrigierende Zeile hinzugefügt. Wenn die Menge in einem Lagerort-Eingang eingegangen ist, wird eine Korrekturzeile auf dem gebuchten Lagerort-Eingang hinzugefügt.  

Die Felder **Bereits gelief. Menge** und **Lief. nicht fakt. Menge** auf der zugehörigen Bestellung werden auf Null gesetzt.

## Eine Mengenbuchung einer gebuchter Rücklieferungen stornieren und wiederholen

Die folgenden Schritte beschreiben, wie Sie vorgehen:

* Eine gebuchte Rücklieferung von Artikeln oder Ressourcen rückgängig machen.
* Buchen Sie die Kauf-Retoure mit einer neuen Menge neu ein.

Die Schritte sind denen der gebuchten Rücksendungen ähnlich.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Gebuchte Rücklieferungen** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie die gebuchte Retourensendung zum Rückgängigmachen.
3. Wählen Sie die Zeile(n) aus, die Sie rückgängig machen möchten.  

4. Wählen Sie die Aktion **Rücklieferung stornieren**.  

    Eine Korrekturzeile wird in den gebuchten Beleg eingefügt, und die Mengen, die in der Reklamation in den Feldern **Rücklieferungsmenge geliefert** und **Lief. n. fakt. Rückl.-Betrag** enthalten sind, werden auf Null gesetzt.  

    Gehen Sie jetzt zurück zu der Einkaufsreklamation, um die Buchung erneut durchzuführen.  

5. Beachten Sie auf der Seite **Gebuchte Rücklieferung** die Nummer im Feld **Reklamationsnr.**. Feld eingetragen.  
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsbestellungen** ein und wählen Sie dann den zugehörigen Link.  
7. Öffnen Sie die betreffende Rücklieferung und wählen Sie die Aktion **Erneut öffnen**.  
8. Korrigieren Sie den Eintrag im Feld **Menge** und buchen Sie die Rücklieferung erneut.  

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

## Siehe auch

[Montagesbuchungen rückgängig machen](assembly-how-to-undo-assembly-posting.md)  
[Buchen von Transaktionen direkt in der Finanzbuchhaltung](finance-how-post-transactions-directly.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]