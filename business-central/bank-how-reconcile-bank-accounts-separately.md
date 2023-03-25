---
title: Bankkonten abstimmen
description: 'Erfahren Sie, wie Sie Transaktionen in Business Central mit Transaktionen in Kontoauszügen Ihrer Bank abstimmen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/13/2022
ms.custom: bap-template
---
# Bankkonten abstimmen

Mit dem Bankabgleich können Sie sicherstellen, dass die Angaben in Ihren Büchern mit den Auszügen übereinstimmen, die Sie von Ihrer Bank erhalten. Die Bankkontoabstimmung vergleicht und gleicht die Buchungen auf den Bankkonten, die Sie unter [!INCLUDE[prod_short](includes/prod_short.md)] festgelegt haben, mit den Transaktionen bei Ihrer Bank ab. Der Abgleich kann dann die Salden auf Ihre Bankkonten in [!INCLUDE[prod_short](includes/prod_short.md)] buchen, um sie den Finanzmanagern zur Verfügung zu stellen. Der Bankabgleich ist auch eine praktische Methode, um fehlende Zahlungen und Buchhaltungsfehler zu ermitteln und zu beheben.

In diesem Artikel wird beschrieben, wie Sie Bankkonten von der Seite **Bankkonten. Reconciliation** abgleicht.

Sie können jedoch Bankkonten auf der Seite **Zahlungsabstimmungsbuch.-Blatt** in Zusammenhang mit der Zahlungsverarbeitung abgleichen. Offene Sachkonto-Einträge auf Bankkonten, die mit den angewendeten Kunden- oder Lieferanten-Sachkonto-Einträgen zusammenhängen, werden geschlossen, wenn Sie die Aktion **Zahlungen buchen und Bankkonto abstimmen** wählen. Dies bedeutet, dass das Bankkonto automatisch mit Zahlungen abgestimmt wird, die Sie mit dem Buch.-Blatt buchen. Weitere Informationen finden Sie unter [Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Die nordamerikanischen Versionen bieten dies auch auf der Seite **Bank Rec. Arbeitsblatt**, das sich besser für Schecks und Einzahlungen eignet, mit dem Sie aber keine Bankauszugsdateien importieren können. Wenn Sie diese Seite anstelle der Seite **Bankkontenabstimmung** verwenden möchten, deaktivieren Sie das Feld **Bankabst. Mit Auto. Abgleich** auf der Seite **Hauptbuchhaltungs-Einrichtung**. Weitere Informationen finden Sie im Abschnitt [Abstimmen von Bankkonten](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) unter der lokalen USA-Funktionalität.

Die Zeilen auf der Seite **Bankkontoabstimmung** sind in zwei Bereiche unterteilt. Der Bereich **Bankauszugspositionen** zeigt entweder importierte Banktransaktionen oder Posten mit ausstehenden Zahlungen an. Der Bereich **Bankposten** zeigt die Posten im internen Bankkonto an.

Das Abstimmen von Transaktionen in Bankauszügen Ihrer Bank mit Bankeinträgen in [!INCLUDE[prod_short](includes/prod_short.md)] wird als *Abgleich* bezeichnet. Es gibt zwei Möglichkeiten, Transaktionen mit Bankeinträgen abzugleichen:

* Automatisch durch Verwendung der Aktion **Automatisch abgleichen**.
* Manuell durch Auswahl von Zeilen in beiden Fenstern, um jede Zeile des Bankauszugs mit einem oder mehreren zugehörigen Sachkonto-Buchungen zu verknüpfen, und dann durch Verwendung der Aktion **Manuell abgleichen**.

Das Kontrollkästchen **Ausgeglichen** ist in Zeilen ausgewählt, in denen Posten übereinstimmen. Weitere Informationen finden Sie unter [Einrichten von Regeln für die automatische Anwendung von Zahlungen](receivables-how-set-up-payment-application-rules.md). Wenn Sie ein Enddatum des Auszugs auf der Bankabstimmung eingeben, nachdem Sie seine Zeilen mit Einträgen abgeglichen haben, macht [!INCLUDE [prod_short](includes/prod_short.md)] die Übereinstimmungen für Zeilen und Einträge rückgängig, die nach diesem Datum liegen.

> [!NOTE]
> Nachdem Sie ein Datum in das Feld „Enddatum des Bankauszugs“ haben, werden die Bankposten auf der Seite „Bankkontoabstimmung“ gefiltert, um nur Einträge bis zu diesem Datum anzuzeigen. Sie können Bankabstimmungen nur mit Bankposten am oder vor dem Enddatum des Auszugs buchen. Der Filter stellt sicher, dass Ihr Bankbuch mit Ihrem Kontoauszug am Enddatum des Bankauszugs ausgeglichen ist, wobei die Differenz die ausstehenden Zahlungen und Schecks sind.

Wenn der Wert im Feld **Gesamtsaldo** im Bereich **Bankauszugszeilen** dem Gesamtwert des Feldes **Saldo abzustimmen** plus dem Feld **Saldo letzter Kontoauszug** im Bereich **Sachkonto-Sachkonto-Einträge** entspricht, können Sie die Aktion **Buchen** wählen. Nicht übereinstimmende Sachkonto-Einträge bleiben auf der Seite und weisen auf Diskrepanzen hin, die Sie zum Abstimmen des Bankkontos beheben sollten.

Um Ihre Bankkontoabstimmung vor der Buchung noch einmal zu überprüfen, verwenden Sie die Aktion **Testbericht**, um eine Vorschau der Abstimmung zu erstellen. Der Bericht ist in den folgenden Kontexten verfügbar:

* Wenn Sie eine Bankabstimmung auf der Seite **Bankkontoabstimmung** vorbereiten.
* Wenn Sie Zahlungen auf der Seite **Zahlungsabstimmungen Buch.-Blätter** abstimmen.

Alle nicht übereinstimmenden Zeilen, die durch einen Wert im Feld **Unterschied** angegeben werden, bleiben auf nach der Buchung der Seite **Bankkontoabstimmung**. Sie stellen eine Art von Diskrepanz dar, die Sie beheben müssen, bevor Sie die Bankkontenabstimmung abschließen können. Die folgende Tabelle beschreibt einige typische Geschäftssituationen, die zu Unterschieden führen können.

| Differenz | Grund | Lösung |
|------------|--------|------------|
| Eine Transaktion auf Ihrem Bankkonto in [!INCLUDE[prod_short](includes/prod_short.md)] ist nicht im Bankauszug enthalten. | Die Bank-Transaktion wurde nicht erstellt, obwohl eine Buchung in [!INCLUDE[prod_short](includes/prod_short.md)] vorgenommen wurde. | Erstellen Sie die fehlende Transaktion (oder fordern Sie einen Debitor auf, sie zu erstellen). Importieren Sie dann die Bankauszugsdatei erneut oder geben Sie die Transaktion manuell ein. |
| Eine Transaktion auf dem Bankauszug ist nicht als Beleg oder Buchungsblattzeile in [!INCLUDE[prod_short](includes/prod_short.md)] vorhanden. | Es wurde eine Banküberweisung ohne entsprechende Buchung in [!INCLUDE[prod_short](includes/prod_short.md)]getätigt, zum Beispiel eine Buch.-Blattzeilenbuchung für eine Ausgabe. | Erstellen und buchen Sie den fehlenden Eintrag. Wie Sie das schnell bewerkstelligen können, erfahren Sie unter [Fehlende Sachkontoeinträge zum Abgleich mit Bankgeschäften erstellen](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Eine Transaktion auf dem internen Bankkonto entspricht einer Banktransaktion, doch sind einige Informationen zu unterschiedlich, um eine Übereinstimmung zu erzielen. | Informationen, wie z.B. der Betrag oder der Kundenname, wurden in der Banktransaktion oder in der internen Buchung anders eingegeben. | Überprüfen Sie die Informationen und passen Sie sie dann manuell an. Korrigieren Sie optional die Abweichung. |

Sie müssen die Differenzen beheben, z. B. indem Sie die fehlenden Einträge erstellen und nicht übereinstimmende Informationen korrigieren oder indem Sie fehlende Geldtransaktionen vornehmen, bis Sie die Bankkontoabstimmung abschließen und buchen können.

Sie können den Bereich **Bankauszugspositionen** auf der Seite **Bankkontoabstimmung** auf folgende Arten ausfüllen:

* Automatisch durch Verwendung der Funktion **Bankauszug importieren**, um den Bereich **Bankauszugszeile** mit Banktransaktionen entsprechend einer importierten Datei oder eines von der Bank bereitgestellten Streams auszufüllen.
* Manuell durch Verwendung der Funktion **Zeilen vorschlagen**, um den Bereich **Bankauszugszeilen** entsprechend zu Rechnungen in [!INCLUDE[prod_short](includes/prod_short.md)] mit ausstehenden Zahlungen auszufüllen.

## So fügen Sie Bankauszugspositionen durch den Import eines Bankauszugs hinzu

Der Bereich **Kontoauszugszeilen** wird entsprechend einer importierten Datei oder eines von der Bank bereitgestellten Streams mit Banktransaktionen gefüllt.

Um Bankauszüge als Bankfeeds zu importieren, müssen Sie den Envestnet Yodlee Bank Feed Service festlegen. Die Einrichtung umfasst die Verknüpfung Ihrer Bankkonten in [!INCLUDE[prod_short](includes/prod_short.md)] mit den entsprechenden Online-Bankkonten. Weitere Informationen finden Sie unter [Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Sie können Kontoauszugsdateien auch im durch Kommas oder Semikolons getrennten Format (.CSV) importieren. Verwenden Sie die unterstützte Einrichtung **Richten Sie ein Bankauszugs-Dateiimportformat ein** zum Definieren von Importformaten für Kontoauszüge und Anhängen des Formats an ein Bankkonto. Sie können diese Formate dann verwenden, wenn Sie Kontoauszüge in die Seite **Bankkontenabgleich** importieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Bankkontoabstimmung** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Wählen Sie im Feld **Bankkontonummer** den entsprechenden Bankkontocode aus. Die Bankposten, die im Bankkonto vorhanden sind, werden im Bereich **Bankposten** angezeigt.
4. Geben Sie im Feld **Auszugsdatum** das Datum des Kontoauszuges der Bank ein.
5. Geben Sie im Feld **Auszug Schluss-Saldo** den Saldo des Bankauszuges ein.
6. Wenn Sie eine Bankauszugsdatei haben, wählen Sie die Aktion **Bankauszug importieren**.
7. Suchen Sie die Datei und wählen Sie dann **Öffnen**, um die Banktransaktionen in den Beriech **Bankauszugszeilen** auf der Seite **Bankkontoabstimmung** zu importieren.

## So füllen Sie Bankabstimmungspositionen mit der Aktion „Zeilen vorschlagen“ aus.

Der Beriech **Kontoauszugszeilen** wird entsprechend den Rechnungen in [!INCLUDE[prod_short](includes/prod_short.md)], die ausstehende Zahlungen aufweisen, gefüllt.  

1. Wählen Sie auf der Seite **Bankkontoabstimmung** die Aktion **Vorschlagszeilen** aus.
2. Geben Sie im Feld **Startdatum** das früheste Buchungsdatum für die Posten ein, die bei der Abstimmung berücksichtigt werden sollen.
3. Geben Sie im Feld **Enddatum** das späteste Buchungsdatum für die Posten ein, die bei der Abstimmung berücksichtigt werden sollen.

    > [!NOTE]
    > Normalerweise stimmt das Enddatum mit dem im Feld **Auszugsdatum** angegebenen Datum überein. Wenn Sie jedoch Transaktionen nur für einen Teil einer Periode abstimmen möchten, können Sie ein anderes Enddatum eingeben.

4. Wenn Sie nicht möchten, dass die Sachkonto-Einträge nicht zugeordnete offene Stornobuchungen enthalten, wählen Sie die Option **Stornobuchungen ausschließen**. Standardmäßig enthält die Liste der Sachkonto-Buchungen stornierte Buchungen bis zum Datum des Kontoauszugs.
5. Wählen Sie die Schaltfläche **OK**.

## So gleichen Sie Bankkontoauszugszeilen mit Bankposten automatisch ab

Die Seite **Bankkontoabstimmung** bietet automatisch Zuordnungsfunktionen auf Grundlage einer Zuordnung des Textes in einer Bankkontoauszugszeile (linker Bereich) zu Text auf einer oder mehreren offenen Posten (rechter Bereich). Sie können den vorgeschlagenen automatischen Abgleich überschreiben und Sie können den automatischen Abgleich auch ganz abschalten. Weitere Informationen finden Sie unter [So gleichen Sie manuell Bankauszugspositionen mit Bankposten ab](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Mit der Aktion **Details abgleichen** können Sie die Grundlage für den Abgleich untersuchen. Die Details enthalten zum Beispiel die Namen der Felder, die übereinstimmende Werte enthalten.  

1. Wählen Sie auf der Seite **Bankkontoabstimmung** die Aktion **Automatisch abgleichen** aus. Die Seite **Bankposten abstimmen** wird geöffnet.
2. Geben Sie im Feld **Toleranz Buchungsdaten in Tagen** die Anzahl der Tage vor und nach dem Bankpostenbuchungsdatum an, innerhalb dessen die Aktion nach entsprechenden Transaktionsdaten im Bankkontoauszug sucht.

    Wenn Sie 0 eingeben oder das Feld leer lassen, sucht die Aktion **Automatisch abgleichen** nur nach übereinstimmenden Transaktionsdaten am Buchungsdatum des Sachkontos.
3. Wählen Sie die Schaltfläche **OK**.

    Die Linien sind farblich gekennzeichnet, damit sie leichter zu verstehen sind, was mit ihnen zu tun ist. Alle Bankauszugszeilen und Sachkontoeinträge, die abgeglichen werden können, werden in grüner Schrift angezeigt und das Kontrollkästchen **Angewandt** ist aktiviert. Bankkontoeinträge, die bereits mit anderen Bankabstimmungen abgeglichen wurden, werden in blauer Schrift angezeigt.
4. Um eine Übereinstimmung zu entfernen, wählen Sie die Bankkontoauszugszeile, und dann die Aktion **Übereinstimmung entfernen**.

> [!TIP]
> Sie können eine Mischung aus manuellem und automatischem Abgleich verwenden. Wenn Sie Einträge manuell abgeglichen haben, wird der automatische Abgleich Ihre Auswahl nicht überschreiben.

## So gleichen Sie manuell Bankauszugspositionen mit Bankposten ab

> [!TIP]
> Beim manuellen Abgleich von Zeilen und Buchungen können Sie sich mit den Aktionen **Alle anzeigen**, **Stornierte Buchungen anzeigen**, **Stornierte Buchungen ausblenden** und **Nicht übereinstimmende Buchungen anzeigen** leichter einen Überblick verschaffen. Standardmäßig enthalten die Sachkonto-Einträge keine nicht übereinstimmenden stornierten Einträge. Um diese Einträge in die Liste aufzunehmen und sie manuell abzugleichen, wählen Sie die Aktion **Stornierte Einträge anzeigen**. Wenn Sie stornierte Einträge ausblenden möchten, nachdem Sie eine oder mehrere Übereinstimmungen vorgenommen haben, werden die übereinstimmenden Einträge weiterhin angezeigt.

1. Wählen Sie auf der Seite **Bankkontoabstimmung** eine nicht zugeordnete Zeile im Bereich **Bankauszugspositionen** aus.
2. Wählen Sie im Bereich **Bankposten** eine oder mehrere Bankkontoposten aus, die mit der ausgewählten Bankauszugszeile abgeglichen werden können. Um mehrere Zeilen auszuwählen, wählen Sie die <kbd>STRG</kbd>-Taste aus und wählen dann die Zeilen aus.

   > [!TIP]
   > Sie können auch mehrere Zeilen des Bankauszugs manuell mit einem Eintrag im Sachkonto abgleichen. Dies ist z.B. dann sinnvoll, wenn Ihre Bankeinzahlung mehrere Zahlungsformen enthielt, wie z.B. Kreditkarten von verschiedenen Ausstellern, und Ihre Bank diese als separate Zeilen aufführt.
3. Wählen Sie die Aktion **Manuell abgleichen** aus.

    Die ausgewählte Bankkontoauszugszeilen und die Bankposten ändern ihre Schriftart zu grün, und das Kontrollkästchen **Ausgeglichen** im rechten Fensterbereich ist aktiviert.
4. Wiederholen Sie die Schritte 1 bis 3 für alle Zeilen des Bankauszugs, die nicht abgeglichen wurden.

> [!TIP]
> Um eine Übereinstimmung zu entfernen, wählen Sie die Bankkontoauszugszeile, und dann die Aktion **Übereinstimmung entfernen**. Wenn Sie mehrere Zeilen des Bankauszugs einem Posten zugeordnet haben und eine oder mehrere der zugeordneten Zeilen entfernen müssen, werden alle manuellen Zuordnungen für den Posten entfernt, wenn Sie **Zuordnung entfernen** wählen.

## So erstellen Sie fehlende Sachkontoeinträge, die mit den Zeilen des Bankauszugs übereinstimmen

Manchmal enthält der Bankauszug Beträge für berechnete Zinsen oder Gebühren. Solche Bankauszugszeilen können nicht abgeglichen werden, weil es in [!INCLUDE[prod_short](includes/prod_short.md)] keine entsprechenden Ledgerbuchungen gibt. In diesem Fall müssen Sie eine Buch.-Blattzeile für jede Transaktion buchen, um einen entsprechenden Posten zu erstellen, mit dem abgeglichen werden kann.

1. Wählen Sie auf der Seite **Bankkontoabstimmung** die Aktion **Übertragung an Fibu Buch.-Blatt** aus.  
2. Geben Sie auf der Seite **Bankkto. Ausgl. Fibu Buch.-Bl.** an, welches Fibu Buch.-Blatt verwendet werden soll, und klicken Sie dann auf die Schaltfläche **OK** .

    Die Seite **Fibu Buch.-Blatt** wird geöffnet und enthält neue Buch.-Blattzeilen für sämtliche Bankauszugspositionen mit fehlende Posten.
3. Vervollständigen Sie die Buch.-Blattzeile mit entsprechenden Informationen, wie z. B. dem Gegenkonto ab. Weitere Informationen finden Sie unter [Arbeiten mit Allgemeinen Buch.-Blättern](ui-work-general-journals.md).  
4. Um das Ergebnis der Buchung erneut durchzuführen bevor Sie buchen, wählen Sie die **Bericht testen** Aktion. Der Bericht **Bankkontoauszug** wird geöffnet und zeigt die gleichen Felder wie der Kopf der Seite **Bankkonto Abstimmen** anzeigt.
5. Wählen Sie die Aktion **Buchen**.

    Nachdem die Buchung gebucht wurde, passen Sie die Zeile des Bankauszugs an diese an.
6. Aktualisieren oder öffnen Sie erneut die Seite **Bankkontoabstimmung**. Der neue Posten erscheint im Bereich **Bankposten**.
7. Vergleichen Sie die Bankkontoauszugszeile mit dem Bankposten, entweder manuell oder automatisch.

## Ausstehende Transaktionen in vorherigen Perioden suchen

Sie können den Bericht Bankauszug verwenden, um ausstehende Transaktionen in früheren Perioden zu finden. Ausstehende Transaktionen wurden vor dem Datum des Kontoauszugs eröffnet und noch nicht abgeschlossen oder wurden abgeschlossen, nachdem der Bankabgleich gebucht wurde.

Wenn Sie den Bericht Bankauszug von der Seite Kontoauszugsliste aus ausführen, können Sie den Umschalter **Ausstehende Posten** aktivieren, so dass der Bericht einen Abschnitt enthält, in dem ausstehende Buchungen aufgeführt sind.

**Beispiel** Wir haben die Sachkonto-Buchungen A, B und C auf unserem Bankkonto für den Monat August. Wenn wir unser Bankkonto für August abstimmen, finden wir eine Zeile im Bankauszug, die mit Buchung A übereinstimmt, aber keine für B und C. Also buchen wir die Abstimmung mit Buchung A abgestimmt und B und C als ausstehende Buchungen.

Im September erhalten wir eine Zahlung für Buchung B und beschließen, unser Bankkonto abzustimmen. Wenn wir den Bericht Bankauszug ausführen, bevor wir den Abgleich buchen, haben wir eine abgestimmte Transaktion und eine ausstehende.

Wenn wir den Bericht für August ausdrucken, haben wir ausstehende Transaktionen für unsere Buchungen B und C, obwohl wir Buchung B im September abgeschlossen haben.

## Bankkontoabstimmung rückgängig machen

Wenn Sie einen Fehler in einer gebuchten Bankabstimmung feststellen, können Sie ihn mit der Aktion **Rückgängig machen** auf der Seite **Bankkonto Auszugsübersicht** korrigieren. Wenn Sie eine gebuchte Bankabstimmung rückgängig machen, werden die Einträge auf die Seite **Bankabstimmung** verschoben und als **Offen** markiert, was bedeutet, dass sie nicht abgestimmt sind. Sie können dann die Bankabstimmung korrigieren und erneut buchen.

> [!NOTE]
> In der nordamerikanischen Version müssen Sie die Funktion gebuchte Bankabstimmungen und Kontoauszüge rückgängig machen auf der Seite **Bankabstimmung mit automatischem Abgleich** auf der Seite **Finanzbuchhaltung Einrichtung** umschalten. Die Funktion Rückgängig ist nicht verfügbar für Kontoauszüge, die aus Arbeitsblättern zur Bankabstimmung gebucht wurden.

### Wiederverwendung der Kontoauszugsnummer

Die für die neue Bankabstimmung verwendete Kontoauszugsnummer wird ebenso wie der letzte Kontoauszug vom Bankkonto abgebucht. Sie können diese Werte ändern, bevor Sie eine neue Bankabstimmung starten. Wenn Sie jedoch eine neue Bankabstimmung erstellen, prüft [!INCLUDE[d365fin](includes/d365fin_md.md)], ob die Kontoauszugsnummer bereits einem gebuchten Kontoauszug zugeordnet ist. Wenn die Nummer verwendet wird, Sie aber möchten, dass der neue Kontoauszug diese stattdessen verwendet, können Sie die **Auszugsnummer ändern** Aktion auf der Seite **Bankkontoabstimmung** verwenden.

### Beispiele

Die folgenden Beispiele zeigen, wie Sie einen Fehler in einer gebuchten Bankabstimmung korrigieren, mit oder ohne Verwendung derselben Auszugsnummer.

#### Beispiel 1

Sie haben Bankabstimmungen für Januar, Februar und März durchgeführt. Die Bankauszugsnummer war für März 100. Später stellen Sie fest, dass der März nur Einträge bis zum 30. März enthielt, was bedeutet, dass Einträge für den 31. März fehlen. Sie müssen also die Bankabstimmung für März wiederholen. In diesem Fall öffnen wir die Seite **Bankkonto-Auszug**, wählen den Auszug für März, und wählen dann **Rückgängig machen**. 

Die neue Bankabstimmung erhält die Kontoauszugsnummer 101. Um die Nummer 100 neu zuzuweisen, wählen Sie **Auszugsnummer ändern** und geben **100** ein. 

> [!TIP]
> Denken Sie daran, das entsprechende Enddatum des Auszugs festzulegen (in diesem Beispiel den 31. März) und das Feld **Letzten Auszug ausgleichen** zu bearbeiten. 

#### Beispiel 2

Sie haben Bankabstimmungen für Januar, Februar, Juni und Juli durchgeführt. Sie stellen fest, dass der Februar falsch war. Nehmen wir an, er hatte die Auszugsnnummer 100. Wie in Beispiel 1 verwenden Sie die Funktionen Rückgängig und Auszugsnummer ändern. zum Ändern der Kontoauszugsnummer wie in Beispiel 1 oben. Sie können jetzt die Bankabstimmung für den Februar wiederholen.  

Nachdem Sie die korrigierte Bankabstimmung für Februar gebucht haben, werden auf der entsprechenden Bankkontokarte die **Letzte Auszugsnummer** **100** an, und das Feld **Letzter Saldoauszug** zeigt den Endsaldo für den Februar-Auszug an. 

Wenn die nächste Bankabstimmung für März erfolgt, wird [!INCLUDE[d365fin](includes/d365fin_md.md)] 101 als Auszugsnummer zuweisen und ihm den richtigen **Saldo letzte Bankauszug** geben.

Wenn Sie die nächste Bankabstimmung für August durchführen, sollten Sie die Werte in der Tabelle **Letzte Auszugsnummer** und **Letzter Kontoauszug ausgleichen** auf der Karte **Bankkonto**, bevor Sie den nächsten Bankauszug erstellen, oder verwenden Sie die **Auszugsnummer ändern** und ändern Sie auch den Wert im Feld **Saldo letzter Auszug** auf der Seite für den Bankabgleich.

> [!NOTE]
> Die Kontoauszugsnummer ist wichtig, wenn Sie Bankabstimmungen mit importierten CAMT-Dateien durchführen, die Kontoauszugsnummern enthalten, oder wenn Sie anhand gedruckter Bankauszügen abgleichen. Wenn Sie nur eine Reihe von Banktransaktionen von Ihrer Online-Bank herunterladen, ist die Kontoauszugsnummer normalerweise nicht wichtig.  
>
> Der letzte Saldokontoauszug wird auf dem Bankkonto gespeichert, um Fehler bei Bankabstimmungen zu minimieren. Er kann jedoch auch bearbeitet werden, sodass Sie Ihre Bankabstimmungen in beliebiger Reihenfolge durchführen können. Dies bedeutet auch, dass beim Rückgängigmachen eines Bankauszugs der neue Endsaldo möglicherweise nicht der letzte Saldoauszug auf dem nächsten Bankauszug ist. Es gibt keine Funktion, mit der Sie einen Saldo auf alle nachfolgenden Bankauszüge übertragen können. Beachten Sie dies, wenn Sie Rückgängig verwenden.  

## Vermeiden Sie Direktbuchungen

Verwenden Sie in Ihrer Buchungsgruppe für Bankkonten kein Sachkonto, das direkte Buchungen zulässt. Durch die Direktbuchung wird die Verbindung zwischen der Sachkonto-Buchung und der Sachkonto-Buchung unterbrochen. Wenn Sie Ihr Bankkonto abstimmen, werden die direkt auf das Sachkonto gebuchten Buchungen nicht berücksichtigt und es wird schwierig sein, die Abstimmung abzuschließen.

Dieser Fehler passiert häufig bei der Eingabe eines Eröffnungssaldos für ein Bankkonto. Es ist wichtig, dass Sie den Eröffnungssaldo nicht direkt in das Hauptbuch buchen. Buchungen im Sachkonto, die direkt auf das Sachkonto gebucht werden, verursachen Probleme. Diese Buchungen können zum Beispiel verhindern, dass Sie Ihr Bankkonto abstimmen können. Bei Bankkonten in Fremdwährung können die Einträge dazu führen, dass sich Differenzen ansammeln, nachdem Sie weitere Bankabstimmungen aufgrund von Anpassungen der Wechselkurse gebucht haben. Häufig wird der Anfangsbestand der Bank direkt auf das Bankkonto gebucht, und der Betrag landet dann auf dem Sachkonto. Alternativ können Sie eine Stornierung für ein Sachkonto durchführen, das Sie zum Ausgleich des Anfangssaldos des Sachpostens verwenden. In beiden Fällen müssen Sie alle Direktbuchungen auf das Sachkonto ausgleichen, bevor Sie mit der ersten Bankabstimmung beginnen, vor allem, wenn das Bankkonto auf eine Fremdwährung lautet.

## Siehe verwandte [Microsoft Schulungen](/training/modules/bank-reconciliation-dynamics-365-business-central/index)

## Siehe auch
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Einrichten von Banken](bank-setup-banking.md)  
[Einrichten von Regeln für die automatische Anwendung von Zahlungen](receivables-how-set-up-payment-application-rules.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
