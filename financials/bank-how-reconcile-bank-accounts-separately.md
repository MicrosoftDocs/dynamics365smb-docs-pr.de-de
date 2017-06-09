---
title: 'So gehts: Bankkonten separat abstimmen| Microsoft Docs'
description: 'Gewusst wie: Bankkonten separat abstimmen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 916f655f9dba80f7c227519372633913b11641ea
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-bank-accounts-separately"></a>Gewusst wie: Bankkonten separat abstimmen
Um Bankkonten im [!INCLUDE[d365fin](includes/d365fin_md.md)]mit den Kontoauszügen abzustimmen, die Sie von der Bank erhalten haben, müssen Sie die Zeilen im Fenster **Bankkontoabstimmung** ausfüllen.

**Hinweis**: Sie können Bankkonten auch im Fenster **Zahlungsabstimmungsbuch.-Blatt** abstimmen. Alle offnen Bankposten, die sich auf ausgeglichene Debitoren- oder Kreditorenposten beziehen, werden geschlossen, wenn Sie die Aktion **Zahlungen buchen und Bankkonto abstimmen** auswählen. Dies bedeutet, dass das Bankkonto mit Zahlungen abgestimmt wird, die Sie mit dem Buch.-Blatt buchen. Weitere Informationen finden Sie unter [So gehts: Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).

Um den Import von Bankkontoauszügen als Bankfeed zu aktivieren, müssen Sie den Bankfeeddienst Envestnet Yodlee einrichten und aktivieren und dann Ihr Bankkonto mit den entsprechenden Onlinebankkonten verbinden. Für weitere Informationen, siehe [So gehts: Einrichten des Envestnet Yodlee Bank-Feed-Service](bank-how-setup-bank-statement-service.md).

Die Zeilen im Fenster **Bankkontoabstimmung** sind in zwei Bereiche unterteilt. Der Bereich **Bankauszugspositionen** zeigt entweder importierte Banktransaktionen oder Posten mit ausstehenden Zahlungen an. Der Bereich **Bankposten** zeigt die Posten im Bankkonto an.

Die Aktivität der Suche und des Übernehmens der abzustimmenden Bankposten wird als *übereinstimmend* bezeichnet. Sie können auswählen, ob Sie einen automatischen Abgleich vornehmen wollen, indem Sie die Funktion **Automatisch abgleichen** verwenden. Alternativ können Sie in beiden Bereichen Zeilen manuell auswählen, um die Bankkontoauszugszeile mit einem oder mehreren entsprechenden Bankposten zu verknüpfen und anschließend die Funktion **Manuell abgleichen** verwenden. Das Kontrollkästchen **Ausgeglichen** ist in Zeilen ausgewählt, in denen Posten übereinstimmen.

Sie können den Bereich **Bankauszugspositionen** im Fenster **Bankkontoabstimmung** auf folgende Arten ausfüllen:

* Automatisch durch die Anwendung der Funktion **Bankauszug importieren**, um die Zeilen entsprechend der tatsächlichen Bankkontoauszügen auszufüllen, basierend auf einer Datei, die von der Bank bereitgestellt wird.
* Sie können die Funktion **Vorschlagszeilen** manuell verwenden, um die Zeilen mit Posten für Rechnungen auszufüllen, die noch zur Zahlung ausstehen.

Wenn der Wert im Feld **Gesamtsaldo** im Bereich **Bankauszugspositionen** dem Wert im Feld **Abzustimmender Saldo** im Bereich **Bankposten** entspricht, können Sie die Aktion **Buchen** auswählen, um die saldierten Bankposten abzugleichen.. Jeder nicht zugeordnete Bankposten wird weiterhin im Fenster angezeigt. Dies bedeutet, dass die Zahlungen, die für das Bankkonto verarbeitet werden, nicht im letzten Bankkontoauszug dargestellt sind, oder dass einige Zahlungen als Schecks eingegangen sind.

**Hinweis**: Wenn sich Bankauszugspositionen auf Scheckposten beziehen, können Sie die entsprechenden Funktionen nicht verwenden. Stattdessen müssen Sie die Aktion **Posten ausgleichen** auswählen und im Inforegister Bankauszugspositionen auswählen und dann die entsprechenden Scheckposten auswählen, mit denen Sie die Bankkontoauszugszeile ausgleichen möchten.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>So füllen Sie Bankabstimmungszeilen mithilfe des Importierens eines Bankkontoauszugs aus
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen **aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen.") Geben Sie **Abstimmung Bankkonto** ein und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Wählen Sie im Feld **Bankkontonummer** das entsprechende Bankkonto aus. Die Bankposten, die im Bankkonto vorhanden sind, werden im Bereich **Bankposten** angezeigt.
4. Geben Sie im Feld **Auszugsdatum** das Datum des Kontoauszuges der Bank ein.
5. Geben Sie im Feld **Auszug Schluss-Saldo** den Saldo des Bankauszuges ein.
6. Wenn Sie eine Bankauszugsdatei haben, wählen Sie die Aktion **Bankauszug importieren**.
7. Suchen Sie die Datei und wählen Sie dann **Öffnen**, um die Banktransaktionen in die Zeilen des Fensters **Bankkontoabstimmung** zu importieren.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>So füllen Sie Bankabstimmungszeilen mit der Funktion "Vorschlagszeilen" aus.
1. Wählen Sie im Fenster **Bankkontoabstimmung** die Aktion **Vorschlagszeilen** aus.
2. Geben Sie im Feld **Startdatum** das früheste Buchungsdatum für die Posten ein, die bei der Abstimmung berücksichtigt werden sollen.
3. Geben Sie im Feld **Enddatum** das späteste Buchungsdatum für die Posten ein, die bei der Abstimmung berücksichtigt werden sollen.
4. Aktivieren Sie das Kontrollkästchen **Mit Schecks** für alle berücksichtigten Scheckposten anstelle der entsprechenden Bankposten.
5. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>So gleichen Sie Bankkontoauszugszeilen mit Bankposten automatisch ab
1. Wählen Sie im Fenster **Bankkontoabstimmung** die Aktion **Automatisch abgleichen** aus. Das Fenster **Bankposten abstimmen** wird geöffnet.
2. Geben Sie im Feld ** Toleranz Buchungsdaten in Tagen** die Anzahl der Tage vor und nach dem Bankpostenbuchungsdatum an, innerhalb dessen die Funktion nach entsprechenden Transaktionsdaten im Bankkontoauszug sucht.

    Wenn Sie "0" eingeben oder das Feld leer lassen, sucht die Funktion **Automatisch abgleichen** nur nach übereinstimmenden Buchungsdaten am Buchungsdatum des Bankpostens.  
3. Wählen Sie die Schaltfläche **OK** aus.  

    Alle Bankkontoauszugszeilen und Bankposten, die zugeordnet werden können, ändern ihre Schriftart zu grün, und das Kontrollkästchen **Ausgeglichen** ist aktiviert.
4. Um eine Übereinstimmung zu entfernen, wählen Sie die Bankkontoauszugszeile, und dann die Aktion **Übereinstimmung entfernen**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>So gleichen Sie manuell Bankauszugspositionen mit Bankposten ab
1. Wählen Sie im Fenster **Bankkontoabstimmung** eine nicht zugeordnete Zeile im Bereich **Bankauszugspositionen** aus.
2. Wählen Sie im Bereich **Bankposten** eine oder mehrere Bankkontoposten aus, die mit der ausgewählten Bankauszugszeile abgeglichen werden können. Um mehrere Zeilen auszuwählen, halten Sie die Strg-Taste gedrückt.  
3. Wählen Sie die Aktion **Manuell abgleichen** aus.

    Die ausgewählte Bankkontoauszugszeilen und die Bankposten ändern ihre Schriftart zu grün, und das Kontrollkästchen **Ausgeglichen** im rechten Fensterbereich ist aktiviert.
4. Wiederholen Sie die Schritte 1 bis 3 für alle Bankkontoauszugszeilen, die nicht abgeglichen wurden.
5. Um eine Übereinstimmung zu entfernen, wählen Sie die Bankkontoauszugszeile, und dann die Aktion **Übereinstimmung entfernen**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>So erzeugen Sie fehlende Posten, mit denen Sie die Banktransaktionen abgleichen können
Manchmal enthält ein Bankkontoauszug einen Betrag für berechnete Zinsen oder Gebühren. Solche Banktransaktionen können nicht abgeglichen werden, da keine entsprechenden Posten im [!INCLUDE[d365fin](includes/d365fin_md.md)] vorhanden sind. In diesem Fall müssen Sie eine Buch.-Blattzeile für jede Transaktion buchen, um einen entsprechenden Posten zu erstellen, mit dem abgeglichen werden kann.

1. Wählen Sie im Fenster **Bankkontoabstimmung** die Aktion **Übertragung an Fibu Buch.-Blatt** aus.  
2. Geben Sie im Fenster **Bankkto. Ausgl. Fibu Buch.-Bl.** an, welches Fibu Buch.-Blatt verwendet werden soll, und klicken Sie dann auf die Schaltfläche **OK** .

    Das Fenster **Fibu Buch.-Blatt** wird geöffnet und enthält neue Buch.-Blattzeilen für sämtliche Bankauszugspositionen mit fehlende Posten.
3. Vervollständigen Sie die Buch.-Blattzeile mit entsprechenden Informationen, wie z. B. dem Gegenkonto ab. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
4. Wählen Sie die Aktion **Buchen** aus.

    Nachdem der Posten gebucht ist, können Sie ihn mit der Banktransaktion abgleichen.
5. Aktualisieren oder öffnen Sie erneut das Fenster **Bankkontoabstimmung**. Der neue Posten erscheint im Bereich **Bankposten**.
6. Vergleichen Sie die Bankkontoauszugszeile mit dem Bankposten, entweder manuell oder automatisch.

## <a name="see-also"></a>Siehe auch
[Verwalten von Bankkonten](bank-manage-bank-accounts.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

