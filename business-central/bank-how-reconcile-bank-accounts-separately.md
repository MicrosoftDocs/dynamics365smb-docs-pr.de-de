---
title: Bankkontenabstimmung | Microsoft Docs
description: Beschreibt wie der Lagerwert mit der Finanzbuchhaltung abgestimmt wird.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 08b7f6c092267b965af491cd80144950db138c3d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388699"
---
# <a name="reconcile-bank-accounts"></a>Bankkonten abstimmen

Sie führen eine Bankabstimmung durch, um sicherzustellen, dass Ihre verschiedenen Geschäftsvorfälle und Aufwendungen korrekt in den Unternehmensbüchern ausgewiesen werden. Sie tun dies, indem Sie die Einträge in Ihren internen Bankkonten mit den Banktransaktionen in Ihrer Bank vergleichen und abgleichen und dann die Salden auf Ihre internen Bankkonten buchen, um den Finanzmanagern Gesamtsummen zur Verfügung zu stellen. Der Bankabgleich ist auch eine praktische Methode, um fehlende Zahlungen und Buchhaltungsfehler zu ermitteln und zu beheben.

Im Folgenden wird beschrieben, wie Sie eine Bankabstimmung mit der Seite **Bankkontoabstimmung** durchführen.

> [!TIP]
> Sie können auch Bankkonten auf der Seite **Zahlungsabstimmungsbuch.-Blatt** in Zusammenhang mit der Zahlungsverarbeitung abgleichen. Alle offnen Bankposten, die sich auf ausgeglichene Debitoren- oder Kreditorenposten beziehen, werden geschlossen, wenn Sie die Aktion **Zahlungen buchen und Bankkonto abstimmen** auswählen. Dies bedeutet, dass das Bankkonto automatisch mit Zahlungen abgestimmt wird, die Sie mit dem Buch.-Blatt buchen. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> In den nordamerikanischen Versionen können Sie auf der Seite **Bank Rec. Arbeitsblatt** durchführen, das besser für Schecks und Einzahlungen-Vorgänge geeignet ist, jedoch keine Bankkontoauszugsdateien bietet. Um diese Seite **Bankkonto Abstimmen** anstelle des Fensters zu verwenden, wählen Sie das Feld **Bank Recon. mit Auto. Entsprechung** auf der Seite **Finanzbuchhaltung Einrichtung**. Weitere Informationen finden Sie im Abschnitt [Abstimmen von Bankkonten](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) unter der lokalen USA-Funktionalität.

Die Zeilen auf der Seite **Bankkontoabstimmung** sind in zwei Bereiche unterteilt. Der Bereich **Bankauszugspositionen** zeigt entweder importierte Banktransaktionen oder Posten mit ausstehenden Zahlungen an. Der Bereich **Bankposten** zeigt die Posten im internen Bankkonto an.

Die Aktivität zum Abstimmen von Bankgeschäften mit internen Bankeinträgen wird als *Zuordnung* bezeichnet. Sie können auswählen, ob Sie einen automatischen Abgleich vornehmen wollen, indem Sie die Funktion **Automatisch abgleichen** verwenden. Alternativ können Sie in beiden Bereichen Zeilen manuell auswählen, um die Bankkontoauszugszeile mit einem oder mehreren entsprechenden Bankposten zu verknüpfen und anschließend die Funktion **Manuell abgleichen** verwenden. Das Kontrollkästchen **Ausgeglichen** ist in Zeilen ausgewählt, in denen Posten übereinstimmen. Weitere Informationen finden Sie unter [Einrichten von Regeln für die automatische Anwendung von Zahlungen](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Wenn sich Bankkontoauszugszeilen auf Scheckposten beziehen, können Sie die entsprechenden Funktionen nicht verwenden. Stattdessen müssen Sie die Aktion **Posten ausgleichen** auswählen und im Inforegister Bankauszugspositionen auswählen und dann die entsprechenden Scheckposten auswählen, mit denen Sie die Bankkontoauszugszeile ausgleichen möchten.

Wenn der Wert im Feld **Gesamtsaldo** im Bereich **Bankauszugspositionen** dem Wert im Feld **Abzustimmender Saldo** im Bereich **Bankposten** entspricht, können Sie die Aktion **Buchen** auswählen. Alle nicht übereinstimmenden Bankkontenbucheinträge verbleiben auf der Seite, was auf eine Diskrepanz hinweist, die Sie bei der Abstimmung des Bankkontos beheben sollten.

Alle nicht übereinstimmenden Zeilen, die durch einen Wert im Feld **Unterschied** angegeben werden, bleiben auf nach der Buchung der Seite **Bankkontoabstimmung**. Sie stellen eine Art von Diskrepanz dar, die Sie beheben müssen, bevor Sie die Bankkontenabstimmung abschließen können. Typische Geschäftssituationen, die zu Unterschieden führen können:

|Abweichung|Grund|Auflösung|
|-|-|
|Eine Transaktion auf dem internen Bankkonto befindet sich nicht auf dem Kontoauszug.|Die Banktransaktion ist nicht erfolgt, obwohl eine Buchung in [!INCLUDE[prod_short](includes/prod_short.md)]vorgenommen wurde .|Führen Sie die fehlende Geldtransaktion durch (oder fordern Sie einen Debitor dazu auf), und importieren Sie die Kontoauszugsdatei erneut, oder geben Sie die Transaktion manuell ein.|
|Eine Transaktion auf dem Kontoauszug existiert nicht als Beleg- oder Buchungszeile in [!INCLUDE[prod_short](includes/prod_short.md)].|Es wurde eine Banküberweisung ohne entsprechende Buchung in [!INCLUDE[prod_short](includes/prod_short.md)]getätigt, zum Beispiel eine Buch.-Blattzeilenbuchung für eine Ausgabe.|Erstellen und buchen Sie den fehlenden Eintrag. Informationen zur schnellen Initiierung finden Sie unter [So erzeugen Sie fehlende Posten, mit denen Sie die Banktransaktionen abgleichen können](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with).|
|Eine Transaktion auf dem internen Bankkonto entspricht einer Banktransaktion, doch sind einige Informationen zu unterschiedlich, um eine Übereinstimmung zu erzielen.|Informationen wie der Betrag oder der Kundenname wurden im Zusammenhang mit dem Bankvorgang oder der internen Buchung unterschiedlich eingegeben.|Überprüfen Sie die Informationen und passen Sie sie dann manuell an. Korrigieren Sie optional den Informationsfehler.||

Sie müssen die Unterschiede beheben, indem Sie beispielsweise fehlende Einträge erstellen und nicht übereinstimmende Informationen korrigieren oder fehlende Geldtransaktionen durchführen, bis der Bankkontenabgleich abgeschlossen und gebucht ist.

Sie können den Bereich **Bankauszugspositionen** auf der Seite **Bankkontoabstimmung** auf folgende Arten ausfüllen:

* Automatisch durch Verwendung der Funktion **Bankauszug importieren**, um den Bereich **Bankauszugszeile** mit Banktransaktionen entsprechend einer importierten Datei oder eines von der Bank bereitgestellten Streams auszufüllen.
* Manuell durch Verwendung der Funktion **Zeilen vorschlagen**, um den Bereich **Bankauszugszeilen** entsprechend zu Rechnungen in [!INCLUDE[prod_short](includes/prod_short.md)] mit ausstehenden Zahlungen auszufüllen.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>So füllen Sie Bankabstimmungszeilen mithilfe des Importierens eines Bankkontoauszugs aus

Der Bereich **Kontoauszugszeilen** wird entsprechend einer importierten Datei oder eines von der Bank bereitgestellten Streams mit Banktransaktionen gefüllt.

Um den Import von Bankkontoauszügen als Bankfeed zu aktivieren, müssen Sie den Envestnet Yodlee Bank Feeds Service einrichten und aktivieren und dann Ihr Bankkonto mit den entsprechenden Onlinebankkonten verbinden. Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md).

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Bankkontoabstimmung** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Wählen Sie im Feld **Bankkontonummer** den entsprechenden Bankkontocode aus. Die Bankposten, die im Bankkonto vorhanden sind, werden im Bereich **Bankposten** angezeigt.
4. Geben Sie im Feld **Auszugsdatum** das Datum des Kontoauszuges der Bank ein.
5. Geben Sie im Feld **Auszug Schluss-Saldo** den Saldo des Bankauszuges ein.
6. Wenn Sie eine Bankauszugsdatei haben, wählen Sie die Aktion **Bankauszug importieren**.
7. Suchen Sie die Datei und wählen Sie dann **Öffnen**, um die Banktransaktionen in den Beriech **Bankauszugszeilen** auf der Seite **Bankkontoabstimmung** zu importieren.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>So füllen Sie Bankabstimmungszeilen mit der Funktion "Vorschlagszeilen" aus.

Der Beriech **Kontoauszugszeilen** wird entsprechend den Rechnungen in [!INCLUDE[prod_short](includes/prod_short.md)], die ausstehende Zahlungen aufweisen, gefüllt.  

1. Wählen Sie auf der Seite **Bankkontoabstimmung** die Aktion **Vorschlagszeilen** aus.
2. Geben Sie im Feld **Startdatum** das früheste Buchungsdatum für die Posten ein, die bei der Abstimmung berücksichtigt werden sollen.
3. Geben Sie im Feld **Enddatum** das späteste Buchungsdatum für die Posten ein, die bei der Abstimmung berücksichtigt werden sollen.
4. Aktivieren Sie das Kontrollkästchen **Mit Schecks** für alle berücksichtigten Scheckposten anstelle der entsprechenden Bankposten.
5. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>So gleichen Sie Bankkontoauszugszeilen mit Bankposten automatisch ab

Die Seite **Bankkontoabstimmung** bietet automatisch Zuordnungsfunktionen auf Grundlage einer Zuordnung des Textes in einer Bankkontoauszugszeile (linker Bereich) zu Text auf einer oder mehreren offenen Posten (rechter Bereich). Beachten Sie, dass die vorgeschlagenen automatischen Zuordnungen überschrieben können, und Sie können wählen, dass die Zuordnung nicht automatisch verwendet wird. Weitere Informationen finden Sie unter [So gleichen Sie manuell Bankauszugspositionen mit Bankposten ab](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

1. Wählen Sie auf der Seite **Bankkontoabstimmung** die Aktion **Automatisch abgleichen** aus. Die Seite **Bankposten abstimmen** wird geöffnet.
2. Geben Sie im Feld **Toleranz Buchungsdaten in Tagen** die Anzahl der Tage vor und nach dem Bankpostenbuchungsdatum an, innerhalb dessen die Funktion nach entsprechenden Transaktionsdaten im Bankkontoauszug sucht.

    Wenn Sie "0" eingeben oder das Feld leer lassen, sucht die Funktion **Automatisch abgleichen** nur nach übereinstimmenden Buchungsdaten am Buchungsdatum des Bankpostens.
3. Wählen Sie die Schaltfläche **OK** aus.

    Alle Bankkontoauszugszeilen und Bankposten, die zugeordnet werden können, ändern ihre Schriftart zu grün, und das Kontrollkästchen **Ausgeglichen** ist aktiviert.
4. Um eine Übereinstimmung zu entfernen, wählen Sie die Bankkontoauszugszeile, und dann die Aktion **Übereinstimmung entfernen**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>So gleichen Sie manuell Bankauszugspositionen mit Bankposten ab

1. Wählen Sie auf der Seite **Bankkontoabstimmung** eine nicht zugeordnete Zeile im Bereich **Bankauszugspositionen** aus.
2. Wählen Sie im Bereich **Bankposten** eine oder mehrere Bankkontoposten aus, die mit der ausgewählten Bankauszugszeile abgeglichen werden können. Um mehrere Zeilen auszuwählen, halten Sie die Strg-Taste gedrückt.
3. Wählen Sie die Aktion **Manuell abgleichen** aus.

    Die ausgewählte Bankkontoauszugszeilen und die Bankposten ändern ihre Schriftart zu grün, und das Kontrollkästchen **Ausgeglichen** im rechten Fensterbereich ist aktiviert.
4. Wiederholen Sie die Schritte 1 bis 3 für alle Bankkontoauszugszeilen, die nicht abgeglichen wurden.
5. Um eine Übereinstimmung zu entfernen, wählen Sie die Bankkontoauszugszeile, und dann die Aktion **Übereinstimmung entfernen**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>So erzeugen Sie fehlende Posten, mit denen Sie die Bankauszugszeilen abgleichen können

Manchmal enthält ein Bankkontoauszug einen Betrag für berechnete Zinsen oder Gebühren. Solche Bankauszugszeilen können nicht abgeglichen werden, da keine entsprechenden Posten im [!INCLUDE[prod_short](includes/prod_short.md)] vorhanden sind. In diesem Fall müssen Sie eine Buch.-Blattzeile für jede Transaktion buchen, um einen entsprechenden Posten zu erstellen, mit dem abgeglichen werden kann.

1. Wählen Sie auf der Seite **Bankkontoabstimmung** die Aktion **Übertragung an Fibu Buch.-Blatt** aus.  
2. Geben Sie auf der Seite **Bankkto. Ausgl. Fibu Buch.-Bl.** an, welches Fibu Buch.-Blatt verwendet werden soll, und klicken Sie dann auf die Schaltfläche **OK** .

    Die Seite **Fibu Buch.-Blatt** wird geöffnet und enthält neue Buch.-Blattzeilen für sämtliche Bankauszugspositionen mit fehlende Posten.
3. Vervollständigen Sie die Buch.-Blattzeile mit entsprechenden Informationen, wie z. B. dem Gegenkonto ab. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  
4. Um das Ergebnis der Buchung erneut durchzuführen bevor Sie buchen, wählen Sie die **Bericht testen** Aktion. Der Bericht **Bankkontoauszug** wird geöffnet und zeigt die gleichen Felder wie der Kopf der Seite **Bankkonto Abstimmen** anzeigt.
5. Wählen Sie die Aktion **Buchen**.

    Nachdem der Posten gebucht ist, können Sie ihn mit der Bankauszugszeile abgleichen.
6. Aktualisieren oder öffnen Sie erneut die Seite **Bankkontoabstimmung**. Der neue Posten erscheint im Bereich **Bankposten**.
7. Vergleichen Sie die Bankkontoauszugszeile mit dem Bankposten, entweder manuell oder automatisch.

## <a name="undo-a-bank-account-reconciliation"></a>Bankkontoabstimmung rückgängig machen
Wenn Sie bei einer gebuchten Bankabstimmung einen Fehler entdecken, können Sie die Aktion **Rückgängig machen** auf der Seite **Bankkonto-Bericht** auswählen, um den Fehler zu korrigieren. Wenn Sie eine gebuchte Bankabstimmung rückgängig machen, werden die Einträge auf die Seite **Bankabstimmung** verschoben und als **offen** markiert, was bedeutet, dass sie nicht abgestimmt sind. Sie können dann die Bankabstimmung korrigieren und erneut buchen.

> [!NOTE]
> In der nordamerikanischen Version müssen Sie die Funktion gebuchte Bankabstimmungen und Kontoauszüge rückgängig machen auf der Seite **Bankabstimmung mit automatischem Abgleich** auf der Seite **Finanzbuchhaltung Einrichtung** umschalten. Die Funktion Rückgängig ist nicht verfügbar für Kontoauszüge, die aus Arbeitsblättern zur Bankabstimmung gebucht wurden.

### <a name="reusing-the-bank-statement-number"></a>Wiederverwendung der Kontoauszugsnummer
Die für die neue Bankabstimmung verwendete Kontoauszugsnummer wird ebenso wie der letzte Kontoauszug vom Bankkonto abgebucht. Sie können diese Werte ändern, bevor Sie eine neue Bankabstimmung starten. Wenn Sie jedoch eine neue Bankabstimmung erstellen, prüft [!INCLUDE[d365fin](includes/d365fin_md.md)], ob die Kontoauszugsnummer bereits einem gebuchten Kontoauszug zugeordnet ist. Wenn die Nummer verwendet wird, Sie aber möchten, dass der neue Kontoauszug diese stattdessen verwendet, können Sie die **Auszugsnummer ändern** Aktion auf der Seite **Bankkontoabstimmung** verwenden.

### <a name="examples"></a>Beispiele
Im Folgenden finden Sie einige Beispiele für die Behebung eines Fehlers bei einer gebuchten Bankabstimmung mit oder ohne Verwendung derselben Kontoauszugsnummer.

#### <a name="example-1"></a>Beispiel 1
Sie haben Bankabstimmungen für Januar, Februar und März durchgeführt. Die Bankauszugsnummer war für März 100. Später stellen Sie fest, dass der März nur Einträge bis zum 30. März enthielt, was bedeutet, dass Einträge für den 31. März fehlen. Sie müssen also die Bankabstimmung für März wiederholen. In diesem Fall öffnen wir die Seite **Bankkonto-Auszug**, wählen den Auszug für März, und wählen dann **Rückgängig machen**. 

Die neue Bankabstimmung erhält die Kontoauszugsnummer 101. Um die Nummer 100 neu zuzuweisen, wählen Sie **Auszugsnummer ändern** und geben **100** ein. 

> [!TIP]
> Denken Sie daran, das entsprechende Enddatum des Auszugs festzulegen (in diesem Beispiel den 31. März) und das Feld **Letzten Auszug ausgleichen** zu bearbeiten. 

#### <a name="example-2"></a>Beispiel 2
Sie haben Bankabstimmungen für Januar, Februar, Juni und Juli durchgeführt. Sie stellen fest, dass der Februar falsch war. Nehmen wir an, er hatte die Auszugsnnummer 100. Wie in Beispiel 1 verwenden Sie die Funktion Rückgängig machen und Auszugsnummer ändern. zum Ändern der Kontoauszugsnummer wie in Beispiel 1 oben. Sie können jetzt die Bankabstimmung für den Februar wiederholen.  

Nachdem Sie die korrigierte Bankabstimmung für Februar auf der entsprechenden Bankkontokarte gebucht haben, zeigt das Feld **Letzte Auszugsnummer** **100** an, und das Feld **Letzter Saldoauszug** zeigt den Endsaldo für den Februar-Auszug an. 

Wenn die nächste Bankabstimmung für März erfolgt, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] 101 als Auszugsnummer zuweisen und ihm den richtigen **Saldo letzte Bankauszug** geben.

Wenn Sie die nächste Bankabstimmung für August durchführen, sollten Sie die Werte in der Tabelle **Letzte Auszugsnummer** und das Feld **Saldo letzter Bankauszug** auf der Karte **Bankkonto** ändern, bevor Sie die nächste Bankabstimmung erstellen, oder die Aktion Auszugsnummer ändern verwenden und auch den Wert im Feld Saldo letzter Kontoauszug auf der Seite Bankabstimmung ändern.

> [!NOTE]
> Die Kontoauszugsnummer ist wichtig, wenn Sie Bankabstimmungen mit importierten CAMT-Dateien durchführen, die Kontoauszugsnummern enthalten, oder wenn Sie anhand gedruckter Bankauszügen abgleichen. Wenn Sie nur eine Reihe von Banktransaktionen von Ihrer Online-Bank herunterladen, ist die Kontoauszugsnummer normalerweise nicht wichtig. 
>
>Der letzte Saldokontoauszug wird auf dem Bankkonto gespeichert, um Fehler bei Bankabstimmungen zu minimieren. Er kann jedoch auch bearbeitet werden, sodass Sie Ihre Bankabstimmungen in beliebiger Reihenfolge durchführen können. Dies bedeutet auch, dass beim Rückgängigmachen eines Bankauszugs der neue Endsaldo möglicherweise nicht der letzte Saldoauszug auf dem nächsten Bankauszug ist. Es gibt keine Funktion, mit der Sie einen Saldo auf alle nachfolgenden Bankauszüge übertragen können. Beachten Sie dies, wenn Sie Rückgängig verwenden. 

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Einrichten von Regeln für die automatische Anwendung von Zahlungen](receivables-how-set-up-payment-application-rules.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]