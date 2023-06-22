---
title: Bank-Geldmittel überweisen
description: 'Sie können Überweisungsbeträge von einem Bankkonto auf ein anders übertragen, einschließlich verschiedene Währungen, indem Sie die Transaktion im Fibu Buch.-Blatt buchen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bank account transfer, multiple currencies'
ms.search.form: 39
ms.date: 04/29/2021
ms.author: edupont
---
# <a name="transfer-bank-funds" />Bank-Geldmittel überweisen

Manchmal ist es erforderlich, einen Betrag von einem Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] auf ein anderes Bankkonto zu überweisen. Dazu müssen Sie die Transaktion auf der Seite **Allgemeines Journal** buchen. Die Aufgabe variiert abhängig davon, ob die Bankkonten dieselbe Währung oder unterschiedlichen Währungen verwenden.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code" />So buchen Sie Überweisungen zwischen Bankkonten mit demselben Währungscode:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Fibu Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie in einer Buch.-Blattzeile die Felder **Buchungsdatum** und **Belegnr.** aus.
3. Wählen Sie im Feld **Kontoart** die Option **Bankkonto** aus.
4. Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.
5. Geben Sie im Feld **Betrag** den Betrag ein, der überwiesen werden soll.

    Als nächstes müssen Sie das Ausgleichskonto angeben. Wenn Sie die relevanten Felder nicht sehen können, dann wählen Sie die Aktion **Weitere Spalten anzeigen**, um alle verfügbaren Felder anzuzeigen.
6. Wählen Sie im Feld **Gegenkontoart** die Option **Bankkonto** aus.
7. Im Feld **Gegenkontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.
8. Buchen Sie das Buch.-Blatt.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes" />Überweisungen zwischen Bankkonten mit verschiedenen Währungscodes buchen:

Um Beträge zwischen Bankkonten zu transferieren, die unterschiedliche Währungen verwenden, müssen Sie zwei Fibu Buch.-Blattzeilen buchen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Fibu Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.
2. Erstellen Sie zwei Buch.-Bl.-Zeilen und füllen Sie die Felder **Buchungsdatum** und **Belegnr.** aus.
3. Wählen Sie in der ersten Buch.-Blattzeile des Feldes **Art** **Bankkonto** aus.
4. Im Feld **Kontonr.** wählen Sie das Bankkonto aus, von dem Sie die Beträge überweisen möchten.
5. Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos mit oder ohne Minuszeichen ein.

    > [!TIP]
    > Ein Betrag ohne Vorzeichen ist eine Belastung, ein Betrag mit Minuszeichen ist eine Gutschrift.

    > [!NOTE]
    > Einige Firmen ziehen es vor, Umlagerungen zwischen Konten in separaten Zeilen zu erfassen. Andere Firmen bevorzugen es, alles in einer Zeile zu erfassen, indem sie ein Ausgleichskonto verwenden. Fragen Sie Ihren Experten, wenn Sie sich nicht sicher sind, was Sie tun sollen.
    >
    > Wenn Ihre Firma es vorzieht, ein Ausgleichskonto zu verwenden, legen Sie das Feld **Saldokontotyp** auf **Bankkonto**, und legen Sie das Feld **Saldokontonr.** auf das Bankkonto, auf das Sie das Geld überweisen wollen. Fahren Sie dann mit Schritt 9 oder 10 fort.
    >
    > Wenn Ihre Firma es vorzieht, eine separate Zeile für die Erfassung zu verwenden, dann fahren Sie mit dem nächsten Schritt fort.
6. Wählen Sie in der zweiten Buch.-Blattzeile des Feldes **Art** **Bankkonto** aus.
7. Im Feld **Kontonr.** wählen Sie das Bankkonto aus, auf das Sie die Beträge überweisen möchten.
8. Geben Sie im Feld **Betrag** den Betrag in der Währung des Bankkontos mit oder ohne Minuszeichen ein.

    > [!TIP]
    > Ein Betrag ohne Vorzeichen ist eine Belastung, ein Betrag mit Minuszeichen ist eine Gutschrift.
9. Wenn die im Journal verwendeten Wechselkurse von den Sätzen auf der Seite **Wechselkursrate** abweichen, geben Sie eine neue Journalzeile für den Wechselkursgewinn oder -verlust ein.  

    1. Geben Sie **Sachkonto** im Feld **Kontoart** ein.  

    2. Geben Sie die Sachkontonummer für Wechselkursgewinn oder -verlust im Feld **Kontonr.** ein.  

    3. Geben Sie den Wechselkursgewinn oder -verlust in das Feld **Betrag** mit oder ohne Minuszeichen ein.

    > [!TIP]
    > Ein Betrag ohne Vorzeichen ist eine Belastung, ein Betrag mit Minuszeichen ist eine Gutschrift.
10. Buchen Sie das Buch.-Blatt.

## <a name="see-also" />Weitere Informationen

[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
