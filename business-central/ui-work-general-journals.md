---
title: Mithilfe von Fibu Buch.-Blätern direkt in die Finanzbuchhaltung buchen
description: Mehr über die Nutzung von Buchungsblättern erfahren, um auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten zu buchen. Verwenden Sie wiederkehrende Journale, um Rückstellungen zu buchen und Salden nach Dimensionswerten zuzuordnen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: journals, recurring, accrual, renumber, bulk-post
ms.search.form: 39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 92535c17570f8204214018377b738cd15f05d9c8
ms.sourcegitcommit: f4b32ba1f926a2a712400c36305616f320757723
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2022
ms.locfileid: "8100864"
---
# <a name="working-with-general-journals"></a>Arbeiten mit Fibu Buch.-Blättern

Die meisten Finanztransaktionen werden in der Finanzbuchhaltung von Geschäftsbelegen wie Einkaufsrechnungen und Verkaufsaufträge gebucht. Sie können auch Geschäftsaktivitäten wie Einkauf, Zahlung, die Verwendung wiederkehrender Buch.-Blätter, um Abgrenzungen zu buchen, oder Rückerstattung von Mitarbeiterausgaben verarbeiten, indem Sie Buch.-Blattzeilen in den verschiedenen Buch.-Blättern in [!INCLUDE[prod_short](includes/prod_short.md)] buchen.  

Die meisten Buchungsblätter basieren auf dem *Fibu Buch.-Blatt*, und Sie können alle Transaktionen auf der Seite **Fibu Buch.-Blatt** bearbeiten. Weitere Informationen finden Sie unter [Transaktionen direkt in der Finanzbuchhaltung buchen](finance-how-post-transactions-directly.md).  

Beispielsweise können Sie die Kosten der Mitarbeiter, die sie selber bezahlt haben, verwenden, um später zurückzuahlen. Weitere Informationen finden Sie unter [Erstatten Sie die Ausgaben der Mitarbeiter zurück](finance-how-record-reimburse-employee-expenses.md).

Aber in vielen Fällen sollten Sie Buchungsblätter verwenden, die für bestimmte Arten von Transaktionen optimiert sind, wie **Zahlungsausgangs Buch.-Blatt** zum Erfassen von Zahlungen. Weitere Informationen finden Sie unter [Zahlungsbelege und Erstattungen im Zahlungsausgangs Buch.-Blatt](payables-how-post-payments-refunds.md).  

Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Debitoren- oder Mitarbeiterkonten. Bei der Buchung mit einem Fibu Buch.-Blatt werden immer Posten für Sachkonten erstellt. Dies gilt auch, wenn beispielsweise eine Buch.-Blattzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird.

Die in ein Buch.-Blatt eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Buch.-Blatt befinden. Durch Buchen des Buch.-Blatts werden die Informationen in Posten auf Konten übertragen und können nicht mehr geändert werden. Der Ausgleich gebuchter Posten kann jedoch aufgehoben werden, und Sie haben die Möglichkeit zum Buchen von Storno- oder Korrekturposten. Weitere Informationen finden Sie unter [Buchungen stornieren und Belege/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Buch-Blattvorlagen und Stapel nutzen

Es gibt mehrere Fibu Buch.-Blattvorlagen. Jede Buch.-Blattvorlage wird durch eine spezifisches Seite mit bestimmten Funktionen und den Feldern dargestellt, die benötigt werden, um diese Funktionen zu unterstützen, wie die Seite **Zahlungs-Abstimmungs-Buch.-Blatt**, um Bankzahlungen zu verarbeiten, und die Seite **Zahlungsausgangs Buch.-Blatt**, um Ihre Mitarbeiter zu bezahlen. Weitere Informationen finden Sie unter [Zahlungen vornehmen](payables-make-payments.md) und [Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Buch.-Blatt oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md).

Sie können zu jeder Buch.-Blattvorlage mehrere Buch.-Blattnamen als Buch-Stapel erstellen. Beispielsweise können Sie Ihre eigenen Buch-Stapel für das Zahlungsausgangsbuch erstellen, das Ihr persönliches Layout und Ihre Einstellungen hat. Der nächste Tipp ist ein Beispiel, wie Sie ein Buch.-Blatt anpassen.

> [!TIP]  
> Wenn Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel auf der Seite **Fibu Buch.-Blattnamen**-Seite auswählen, dann werden das Feld **Betrag**, beispielsweise Fibu Buch.-Blattzeilen für dieselbe Belegnummer automatisch mit dem Wert, der zum Ausgleichen des Belegs erforderlich ist, ausgefüllt. Weitere Informationen finden Sie unter [[!INCLUDE[prod_short](includes/prod_short.md)] Werte vorschlagen lassen](ui-let-system-suggest-values.md).

> [!TIP]
> Verwenden Sie zum Hinzufügen oder Entfernen von Feldern in Buchungsblättern das Banner **Personalisieren**. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Fibu Buch.-Blatt-Stapelverarbeitungen überprüfen
Um Verzögerungen beim Buchen zu vermeiden, können Sie eine Hintergrundüberprüfung aktivieren, die Sie benachrichtigt, wenn in dem Finanzbuch.-Blatt, an dem Sie arbeiten, ein Fehler vorliegt, der Sie daran hindert, das Buch.-Blatt zu veröffentlichen. Auf der Seite **Fibu Buch.-Blatt** können Sie **Hintergrundfehlerprüfung** wählen, damit [!INCLUDE[prod_short](includes/prod_short.md)] Finanzbuch.-Blätter überprüft, wie z. B. Fibu Buch.Blätter oder Zahlungsausgangs Buch.-Blätter, während Sie an ihnen arbeiten. 

Wenn Sie die Überprüfung aktivieren, wird die Infobox **Buch.-Blatt-Prüfung** neben den Buch.-Blattzeilen angezeigt und zeigt Probleme in der aktuellen Zeile und im gesamten Stapel an. Die Überprüfung erfolgt, wenn Sie einen Finanz-Buch.-Blattname laden und eine andere Buch.-Blattzeile auswählen. Die Kachel **Probleme insgesamt** in der Infobox zeigt die Gesamtanzahl von Problemen, die [!INCLUDE[prod_short](includes/prod_short.md)] gefunden hat, und Sie können sie auswählen, um eine Übersicht über die Probleme zu öffnen. 

Sie können die Aktionen **Zeilen mit Problemen anzeigen** und **Alle Zeilen anzeigen** anzeigen, um zwischen Buch.-Blattzeilen umzuschalten, die Probleme haben oder keine. Die neue Infobox **Buch.-Blattzeilendetails** bietet einen schnellen Überblick und Zugriff auf Daten aus Buch.-Blattzeilen, wie z. B. Sachkonto, Debitor oder Kreditor sowie zur Buchungseinrichtung für bestimmte Konten.     

### <a name="reversing-journals-to-correct-mistakes"></a>Umkehren von Buch.-Blättern, um Fehler zu korrigieren
Wenn Sie mit Buch.-Blättern arbeiten, die viele Zeilen haben und etwas schief geht, ist es wichtig, dass sich Fehler leicht korrigieren lassen. Die Seite **Gebuchtes Fibu Buch.-Blatt** bietet eine Reihe von Aktionen, die helfen können.

* **Ausgewählte Zeilen in Buch.-Blatt kopieren** – Kopieren Sie nur die von Ihnen ausgewählten Zeilen.
* **Kopieren Sie das Finanzbuchhaltungsjournal in das Buch.-Blatt** – Kopieren Sie alle Zeilen, die zum gleichen Finanzbuchhaltungsjournal gehören.

Mit diesen Aktionen können Sie eine Kopie einer Fibu Buch.-Blattzeile oder eines Stapels erstellen und dann Folgendes angeben:

* Das Buch.-Blatt, in das die Zeilen kopiert werden sollen
* Ob mit entgegengesetzten Zeichen (ein Stornierungs-Buch.-Blatt)
* Ein anderes Buchungsdatum oder eine andere Belegnummer

Damit Buch.-Blätter in gebuchte Fibu Buch.-Blätter kopiert werden können, wählen Sie auf der Seite **Fibu Buch.-Blatt-Vorlagen** das Kontrollkästchen **In gebuchte Buch.-Blattzeilen kopieren**. Nachdem Sie Personen das Kopieren gebuchter Fibu Buch.-Blätter erlauben, können Sie, falls notwendig, das Kopieren für bestimmte Stapel deaktivieren.

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hauptkonten und Gegenkonten und Saldokonten verstehen
Wurden auf der Seite **Fibu Buch.-Blätter** Standardgegenkonten für die Buch.-Blattnamen eingerichtet, wird das Gegenkonto beim Ausfüllen des Felds **Kontonr.** automatisch ausgefüllt. Andernfalls müssen die Felder **Kontonr.** und **Gegenkontonr.** manuell ausgefüllt werden. Bei einem positiven Betrag im Feld **Betrag** wird das Hauptkonto belastet, und auf dem Gegenkonto erfolgt eine Gutschrift. Bei einem negativen Betrag erfolgt eine Gutschrift auf dem Hauptkonto, und das Gegenkonto wird entsprechend belastet.

> [!NOTE]  
> Die MwSt. für Haupt- und Gegenkonto wird getrennt berechnet, damit für die Konten unterschiedliche MwSt.-Prozentsätze verwendet werden können.

## <a name="working-with-recurring-journals"></a>Arbeiten mit wiederkehrenden Buchblättern
Bei einem wiederkehrenden Buch.-Blatt handelt es sich um ein Fibu Buch.-Blatt mit speziellen Feldern für die Verwaltung von Transaktionen, die häufig und ohne oder und mit geringen Änderungen gebucht werden. Mithilfe dieser speziellen Felder für wiederkehrende Transaktionen können Sie feste und variable Beträge buchen. Sie können auch ein automatisches Storno für den Tag nach dem Buchungsdatum festlegen und wiederkehrende Posten zusammen mit Verteilungsschlüsseln verwenden. Sie können auch Verteilungsschlüssel verwenden, um wiederkehrende Posten mit einem einzigen Vorgang zwischen verschiedenen Konten aufteilen zu können. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Buch.-Blatts auf mehrere Konten](#allocating-recurring-journal-amounts-to-several-accounts).

Mit einem wiederkehrenden Buchungsblatt müssen Posten, die regelmäßig gebucht werden, nur einmal eingetippt werden. Das bedeutet, dass Einträge wie Konten, Dimensionen oder Dimensionswerte nach der Buchung im Buchungsblatt verbleiben. Werden Anpassungen notwendig, können Sie diese mit jeder Buchung durchführen.

### <a name="recurring-method-field"></a>Feld Wiederholungsmethode

Dieses Feld legt fest, wie der in der Buch.-Blattzeile angegebene Betrag nach der Buchung bearbeitet werden soll. Wenn Sie z. B. bei jeder Buchung der Zeile den gleichen Betrag verwenden, können Sie den Betrag unverändert lassen. Wenn Sie dagegen immer den Betrag ändern, jedoch Konto und Text unverändert lassen, können Sie den Betrag nach der Buchung löschen lassen.

| Aktion | Siehe |
| --- | --- |
|F Fest|Der Betrag in der Buch.-Blattzeile wird nach der Buchung nicht geändert.|
|V Variabel|Der Betrag wird nach dem Buchen aus der Buch.-Blattzeile gelöscht.|
|B Saldo|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile in der Tabelle Gen angegeben werden. Fibu Buch.-Blatt Tabelle. Der Saldo auf dem Konto wird daher auf Null festgelegt. Denken Sie daran, das Feld **Verteilung %** auf der Seite **Verteilungsübersicht** auszufüllen. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Buch.-Blatts auf mehrere Konten](#allocating-recurring-journal-amounts-to-several-accounts).|
|RF Umgekehrt fix|Der Betrag in der Buch.-Blattzeile bleibt nach der Buchung erhalten und für den folgenden Tag wird ein Gegenposten gebucht.|
|RV Umgekehrt variabel|Der Betrag in der Buch.-Blattzeile wird nach der Buchung gelöscht und für den folgenden Tag wird ein Gegenposten gebucht.|
|RB Umgekehrt Ausgleich|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile auf der Seite **Zuweisungen** angegeben werden. Der Saldo auf dem Konto wird auf Null gesetzt, und ein Gegenposten wird am folgenden Tag gebucht.|
|Saldo nach Dimension|Die Journalzeile ordnet die Kosten basierend auf dem Saldo eines Sachkontos nach Dimensionen zu. Sie werden aufgefordert, die Dimensionsfilter festzulegen, die zur Berechnung des Kontostands des Sachkontos nach Dimension verwendet werden sollen, aus der Sie die Kosten zuordnen möchten. Alternativ wählen Sie die **Bemaßungsfilter einstellen** Aktion später.|
|Rückbuchungssaldo nach Dimension|Die Journalzeile ordnet die Kosten basierend auf den umgekehrten Ausgleich eines Sachkontos nach Dimensionen zu. Sie werden aufgefordert, die Dimensionsfilter festzulegen, die zur Berechnung des Kontostands des Sachkontos nach Dimension verwendet werden sollen, aus der Sie die Kosten zuordnen möchten. Alternativ wählen Sie die **Bemaßungsfilter einstellen** Aktion später.|

> [!NOTE]  
> Die MwSt.-Felder können entweder in der Wiederk. Buch.-Blattzeile oder in der Verteilungs Buch.-Blattzeile ausgefüllt werden, aber nicht in beiden. Das heißt, sie können auf der Seite **Zuweisungen** nur passende Zeilen eintragen, wenn die entsprechenden Zeilen nicht im wiederkehrenden Buch.-Blatt eingetragen werden.

### <a name="recurring-frequency-field"></a>Feld Wiederholungsrate
Das Feld legt fest, wie oft der Posten in der Buch.-Blattzeile gebucht wird. Das ist ein Datumsformelfeld, und es muss für andere Zeilen des wiederkehrenden Buch.-Blatts ausgefüllt werden. Weitere Informationen zu finden Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Beispiele
Wenn das Buch.-Blatt z. B. monatlich gebucht werden soll, geben Sie "1M" ein. Nach jeder Buchung wird dann das Datum im Feld **Buchungsdatum** auf dasselbe Datum im nächsten Monat aktualisiert.

Wenn Sie immer am Letzten des Monats buchen möchten, können Sie nach einem der folgenden Beispiele vorgehen:

- Sie können die erste Buchung am letzten Tag eines Monats buchen und die Wiederholungsrate 1T + 1M – 1T (1 Tag + 1 Monat –1 Tag) eingeben. Mit dieser Formel wird immer das richtige Datum berechnet, unabhängig davon, wie viele Tage der Monat hat.

- Sie können die erste Buchung an einem beliebigen Tag eines Monats buchen und dann die Formel eingeben: 1M+CM. Diese Formel addiert einen ganzen Monat plus die verbleibenden Tage bis zum Letzten des Monats.

### <a name="expiration-date-field"></a>Ablaufdatumsfeld
Das Feld bestimmt das Datum, an dem die Zeile letztmalig gebucht werden soll. Nach dem im Feld angegebenen Datum wird die Zeile nicht mehr gebucht.

Dieses Feld bietet den Vorteil, dass die Zeile nicht sofort aus dem Buch.-Blatt gelöscht wird und Sie jederzeit das Ablaufdatum durch ein späteres Datum ersetzen können, so dass Sie die Zeile noch länger verwenden können.

Wenn das Feld leer ist, wird die Zeile bei jeder Buchung mitgebucht, bis sie aus dem Buch.-Blatt gelöscht wird.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Zuordnung von Beträgen des wiederkehrenden Buch.-Blatts auf mehrere Konten

Auf der Seite **Wiederk. Fibu Buch.-Blatt** können Sie die **Verteilungen** Aktion auswählen, anzeigen oder verwalten und bestimmen, wie Beträge der Zeile des wiederkehrenden Buch.-Blatts auf mehrere Konten und Dimensionen zugeordnet werden. Das heißt, die Verteilung ist eine Gegenkontozeile für die Zeile des wiederkehrenden Buch.-Blattes.

Genau wie in einem wiederkehrenden Buch.-Blatt müssen Sie eine Verteilung nur einmal eingeben. Die Verteilung bleibt nach dem Buchen im Verteilungsbuch, sodass Sie nicht jedes Mal, wenn Sie die Zeile des wiederkehrenden Buch.-Blattes buchen, Beträge und Verteilungen eingeben müssen.

Wenn die *Wiederholungsart* im Wiederk. Buch.-Blatt auf **Ausgleich** oder **Umgekehrt Ausgleich** gesetzt ist, werden keine Dimensionswertcodes im Wiederk. Buch.-Blatt berücksichtigt, wenn das Konto auf Null gesetzt ist. Anders ausgedrückt, wenn Sie auf der Seite **Zuordnungen** eine wiederkehrende Zeile auf die verschiedenen Dimensionswerte verteilen, wird nur eine Umkehrbuchung erstellt. Wenn Sie also im Verteilungsbuch eine Zeile des wiederkehrenden Buch.-Blattes zuordnen, die einen Wertcode der Dimension enthält, dürfen Sie denselben Code nicht auf der Seite **Zuordnungen** eingeben. Andernfalls sind die Zahlen für die Dimensionswerte falsch.  

Um wiederkehrende Journalbeträge basierend auf Dimensionen zuzuweisen, legen Sie das Feld **Wiederkehrende Methode** auf **Saldo nach Dimension** oder **Umkehren des Gleichgewichts nach Dimension** stattdessen. Wenn die Wiederholungsart im Wiederk. Buch.-Blatt auf **Ausgleich nach Dimension** oder **Umgekehrt Ausgleich nach Dimension** gesetzt ist, werden Dimensionswertcodes im Wiederk. Buch.-Blatt berücksichtigt, wenn das Konto auf Null gesetzt ist. Wenn Sie also verschiedenen Dimensionswerten eine wiederkehrende Zeile auf der Seite **Zuweisungen** zuweisen, wird dann eine Anzahl von Umkehreinträgen erstellt, die mit der Anzahl der Dimensionswertkombinationen übereinstimmen, aus denen der Saldo besteht. Wenn Sie den Kontostand über das wiederkehrende Journal zuordnen, das einen Dimensionswertcode enthält, denken Sie daran, **Saldo nach Dimension** oder **Umkehren des Saldos nach Dimension** zu verwenden, um sicherzustellen, dass die Dimensionswerte vom Quellkonto korrekt ausgeglichen oder umgekehrt werden.  

Ihr Unternehmen verfügt beispielsweise über einige Geschäftsbereiche und eine Handvoll Abteilungen, die Ihre Controller als Dimensionen eingerichtet haben. Um den Prozess der Buchungserfassung zu beschleunigen, müssen die Sachbearbeiter nur die Dimensionen der Geschäftsbereiche eingeben. Da jeder Geschäftsbereich über spezifische Zuordnungsschlüssel für die Abteilungsdimension verfügt, z. B. basierend auf der Anzahl der Mitarbeiter, können Sie die wiederkehrenden Methoden **BD Balance nach Dimension** oder **RBD-Umkehrung des Gleichgewichts nach Dimension** zur Neuzuordnung von Ausgaben für jeden Geschäftsbereich zu den richtigen Abteilungen basierend auf den Zuordnungsschlüsseln verwenden.  

> [!NOTE]
> Bemaßungen, die Sie in Zuordnungszeilen festlegen, werden nicht automatisch berechnet, und Sie müssen angeben, welche Bemaßungswerte in den Zuordnungskonten festgelegt werden müssen. Wenn Sie die Verknüpfung zwischen der Quellkontodimension und der Zuordnungskontodimension beibehalten möchten, empfehlen wir die Verwendung der Funktionen [Kostenrechnung](finance-about-cost-accounting.md).

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Beispiel: Zuordnen von Mietzahlungen auf verschiedene Abteilungen
Sie zahlen jeden Monat Miete, daher haben Sie den Vertragsrabattbetrag auf das Kassenkonto in einer Zeile des wiederkehrenden Buch.-Blattes eingegeben. Auf der Seite **Zuordnungen** können Sie die Kosten auf die Kostenstellen entsprechend der jeweils belegten Quadratmeterzahlen aufteilen. Die Berechnung erfolgt aufgrund der Verteilungsprozente für jede Verteilungs-Buch.-Blattzeile. Sie können verschiedene Konten für jede Zeile des Buch.-Blattes Verteilungen eingeben (wenn die Miete auch auf verschiedene Konten aufgeteilt werden soll) oder Sie können dasselbe Konto mit verschiedenen Dimensionswertcodes für die Dimension "Kostenstelle" auf jeder Zeile eingeben.

### <a name="reversal-date-calculation"></a>Stornierungsdatumsberechnung
Wenn Sie wiederkehrende Fibu Buch.-Blätter verwenden, um Abgrenzungen am Ende einer Periode zu buchen, ist es wichtig, die volle Kontrolle über Stornierungsposten zu haben. Auf der Seite **Wiederkehrende Fibu Buch.-Blätter** können Sie mithilfe des Felds **Stornierungsdatumsberechnung** das Datum steuern, an dem Stornierungsposten gebucht werden, wenn wiederkehrende Stornierungsmethoden verwendet werden.

#### <a name="example"></a>Beispiel
Abgrenzungen werden normalerweise mit wiederkehrenden Methoden Fest, Variabel oder Saldo in der Buch.-Blattzeile gebucht. Das Buchungsdatum des gebuchten Betrags auf dem Konto in der Buch.-Blattzeile wird anhand der wiederkehrenden Häufigkeit berechnet. Das Buchungsdatum für die Gegenposten wird mithilfe des Felds **Stornierungsdatumsberechnung** wie folgt berechnet:

* Wenn das Feld leer ist, wird der Gegenposten am nächsten Tag gebucht.
* Wenn das Feld eine Datumsformel enthält (z. B. **5D** für fünf Tage) wird der Gegenposten mit einem Buchungsdatum gebucht, das anhand der Stornierungsdatumberechnung berechnet wird.

> [!NOTE]
> Standardmäßig ist das Feld **Stornierungsdatumsberchnung** auf der Seite **Wiederkehrende Fibu Buch.-Blätter** nicht verfügbar. Um das Feld zu verwenden, müssen Sie es hinzufügen, indem Sie die Seite personalisieren. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="working-with-standard-journals"></a>Arbeiten mit Standard-Buchblättern
Wenn Sie Buch.-Blattzeilen erstellt haben, die Sie wahrscheinlich zu einem späteren Zeitpunkt erneut erstellen werden, können Sie sich entscheiden, diese als Standard Buch.-Blatt zu speichern, bevor Sie das Buch.-Blatt buchen. Diese Funktionalität wird in Artikel Buch.-Blätter und Buch.-Blätter angewendet.

> [!NOTE]  
>   Das folgende Verfahren bezieht sich auf das Artikel Buch.-Blatt, die Informationen betreffen jedoch auch das Standard Buch.-Blatt.

### <a name="to-save-a-standard-journal"></a>Ein Standard-Buch.-Blatt speichern:
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Geben Sie in mindestens eine Buch.-Blattzeile ein.
3. Wählen Sie die Buch.-Blattzeilen aus, die Sie wieder verwenden möchten.
4. Wählen Sie die **Als Standard Buch.-Blatt speichern** Aktion aus.
5. Auf der Anforderungsseite **Als Standard Artikel Buch.-Blatt speichern** müssen Sie ein neues oder vorhandenes Standard Buch.-Blatt eingeben, in dem die Zeilen gespeichert werden sollen:

    Wenn Sie bereits mindestens ein Standard-Artikel Buch.-Blatt erstellt haben und es durch eine neue Zusammenstellung von Artikel Buch.-Blattzeilen ersetzen möchten, können Sie Feld Code den gewünschten Code auszuwählen.
6. Wählen Sie die Schaltfläche **OK**, um zu bestätigen, dass Sie das vorhandene Standard-Artikel-Buch.-Blatt überschreiben und seinen gesamten Inhalt ersetzen möchten.
7. Wählen Sie das Feld **Stückpreis speichern** aus, wenn Sie die Werte im Feld **Stückpreis** im Standard Artikel Buch.-Blatt speichern möchten.
8. Wählen Sie das Feld **Menge speichern** aus, wenn die Anwendung die Werte im Feld **Menge** speichern muss.
9. Wählen Sie **OK** aus, um das Standard Artikel Buch.-Blatt zu speichern.

Wenn Sie das Standard-Artikel-Buch.-Blatt gespeichert haben, wird die Seite "Artikel Buch.-Blatt" angezeigt, so dass Sie mit der Buchung fortfahren können. Diesen Vorgang können Sie beim Buchen dieser oder einer ähnlichen Zeile einfach wiederholen.

### <a name="to-reuse-a-standard-journal"></a>Standard-Protokolle wieder nutzen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die **Standard Buch.-Blatt abrufen** Aktion aus.

    Die Seite "Standard Artikel Buch.-Blätter" wird geöffnet und zeigt Codes und Beschreibungen für alle vorhandenen Standard Artikel Buch.-Blätter an.
3. Zum Überprüfen eines Standard Artikel Buch.-Blatts vor dem Auswählen für die Wiederverwendung klicken Sie auf **Buch.-Blatt anzeigen**.

    Alle Änderungen, die an einem Standard Artikel Buch.-Blatt vorgenommen werden, werden sofort implementiert. Sie sind beim nächsten Mal, wenn Sie das betreffenden Standard Artikel Buch.-Blatt öffnen oder verwenden. Daher sollten Sie sicher sein, dass die Änderung gewichtig genug ist, um sie allgemein zu übernehmen. Nehmen Sie andernfalls die spezifische Änderung am Artikel Buch.-Blatt vor, nachdem die Zeilen im Standard Artikel Buch.-Blatt eingefügt wurden. Siehe dazu auch Schritt 4 unten.
4. Auf der Seite **Standard Artikel Buch.-Blätter** wählen Sie das Standard Artikel Buch.-Blatt aus, das Sie erneut verwenden möchten, und klicken Sie auf **OK**.

    Jetzt wird das Artikel Buch.-Blatt mit den Zeilen aufgefüllt, die Sie als Standard Artikel Buch.-Blatt gespeichert haben. Wenn Buch.-Blattzeilen bereits im Artikel Buch.-Blatt vorhanden sind, werden die eingefügten Zeilen unterhalb der vorhandenen Buch.-Blattzeilen eingefügt.

    Normalerweise, d.h., wenn das Feld **Stückpreis speichern** während der Funktion **Als Standard Buch.-Blatt speichern** nicht markiert war, wird das Feld **Stückpreis** in den eingefügten Zeilen automatisch mit dem aktuellen Wert des Artikels gefüllt (der aus dem Feld **Einstandspreis** auf der Artikelkarte kopiert wird).

    > [!NOTE]  
    > Wenn Sie eines der Felder **Stückzahl speichern** oder **Menge speichern** ausgewählt haben, sollten Sie jetzt überprüfen, ob die eingefügten Werte für diese bestimmte Lagerregulierung richtig sind, bevor Sie das Artikelprotokoll speichern.

    Wenn die eingefügten Artikel Buch.-Blattzeilen gespeicherte Stückpreise enthalten, die Sie nicht buchen möchten, können Sie sie schnell an den aktuellen Artikelwert anpassen:

5. Wählen Sie den Artikel, für den Sie den Lagerbestand anpassen möchten, und wählen Sie dann die Aktion **Einheitsbetrag neu berechnen** aus. Dadurch wird das Feld Stückpreis mit dem aktuellen Einstandspreis des Artikels aktualisiert.
6. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-renumber-document-numbers-in-journals"></a>Belegnummern in Buch.-Blättern neu nummerieren

Um sicherzustellen, dass Sie keine Buchungsfehler aufgrund der Reihenfolge der Belegnummern erhalten, können Sie die Funktion **Belegnummern neu nummerieren** verwenden, bevor Sie ein Buch.-Blatt buchen.

In allen Buch.-Blättern, die auf dem Fibu Buch.-Blatt basieren, kann das Feld **Dokumentennr.** bearbeitet werden, so dass Sie unterschiedliche Belegnummern für verschiedene Buch.-Blattzeilen oder die gleiche Belegnummer für die zugehörigen Buch.-Blattzeilen angeben können.

Wenn das Feld **Serien-Nr.** auf dem Buch.-Blatt ausgefüllt ist, erfordert die Buchungsfunktion in Fibu Buch.-Blättern, dass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen sequenziell angeordnet sind. Wählen Sie einfach die Aktion **Belegnummern neu nummerieren** aus, und relevante **Belegnr.**-Felder werden anschließend aktualisiert. Wenn verwandte Buch.-Blattzeilen nach Belegnummern gruppiert wurden, bevor Sie die Funktion verwendet haben, bleiben sie gruppiert, können aber eine andere Belegnummer erhalten.  

Diese Funktion funktioniert auch bei gefilterten Ansichten.

Jede Neunummerierung der Belegnummern berücksichtigt verwandte Anwendungen, wie etwa eine Zahlungsanwendung, die von dem Dokument auf der Buch.-Blattzeile an ein Kreditorenkonto durchgeführt wurde. Entsprechend werden die Felder **Ausgleichs-ID** und **Ausgleich mit Belegnr.** in den betroffenen Posten aktualisiert.

### <a name="to-renumber-documents-in-journals"></a>Belege in Buch.-Blättern neu nummerieren

Die folgende Prozedur basiert auf der Seite **Fibu Buch.-Blatt**, gilt aber für alle anderen Buch.-Blätter, die auf dem Hauptbuch basieren, wie etwa die Seite **Zahlungs Buch.-Blatt**.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Allgemeine Erfassungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wenn Sie zum Buchen des Buchs bereit sind, wählen Sie auf der Registerkarte Aktionen, in der Gruppe Funktionen, die Option **Belegnummern neu nummerieren**.

Werte im Feld **Dokumentennr.** werden geändert, wo erforderlich, sodass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen in sequenzieller Reihenfolge stehen. Nach der Neunummerierung der Dokumente können Sie mit der Buchung des Buch.-Blatts fortfahren.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Buchen von Transaktionen direkt in der Finanzbuchhaltung](finance-how-post-transactions-directly.md)  
[Buch.-Blatt-Buchungen stornieren und Rückgängigmachung von Eingängen/Versendungen](finance-how-reverse-journal-posting.md)  
[Kosten und Einkünfte zuteilen](year-allocate-costs-income.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Schließen von offenen Artikelposten aus einem festen Ausgleich im Artikel Buch.-Blatt](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Lager im Neubewertungs-Blatt neu bewerten](inventory-how-revalue-inventory.md)  
[Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md)  
[Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Buch.-Blatt oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md)  
[Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md)  
[Arbeiten mit Intercompany-Belegen und Buch.-Blättern](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]