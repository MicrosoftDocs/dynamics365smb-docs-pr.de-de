---
title: Mithilfe von Fibu Buch.-Blätern direkt in die Finanzbuchhaltung buchen| Microsoft Docs
description: Mehr über die Nutzung von Buchungsblättern erfahren, um auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten zu buchen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/10/2020
ms.author: edupont
ms.openlocfilehash: 669985f08dd497ecec925eef126fff262067b947
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785246"
---
# <a name="working-with-general-journals"></a>Arbeiten mit Fibu Buch.-Blättern

Die meisten Finanztransaktionen werden in der Finanzbuchhaltung von Geschäftsbelegen wie Einkaufsrechnungen und Verkaufsaufträge gebucht. Sie können auch Geschäftsaktivitäten wie Einkauf, Zahlung oder Rückerstattung von Mitarbeiterausgaben verarbeiten, indem Sie Buch.-Blattzeilen in den verschiedenen Buch.-Blättern in [!INCLUDE[d365fin](includes/d365fin_md.md)] buchen.  

Die meisten Buchungsblätter basieren auf dem *Fibu Buch.-Blatt*, und Sie können alle Transaktionen auf der Seite **Fibu Buch.-Blatt** bearbeiten. Weitere Informationen finden Sie unter [Transaktionen direkt in der Finanzbuchhaltung buchen.](finance-how-post-transactions-directly.md).  

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
> Wenn Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel auf der Seite **Fibu Buch.-Blattnamen**-Seite auswählen, dann werden das Feld **Betrag**, beispielsweise Fibu Buch.-Blattzeilen für dieselbe Belegnummer automatisch mit dem Wert, der zum Ausgleichen des Belegs erforderlich ist, ausgefüllt. Weitere Informationen finden Sie unter[[!INCLUDE[d365fin](includes/d365fin_md.md)] Werte vorschlagen](ui-let-system-suggest-values.md).

> [!TIP]
> Verwenden Sie zum Hinzufügen oder Entfernen von Feldern in Buchungsblättern das Banner **Personalisieren**. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hauptkonten und Gegenkonten und Saldokonten verstehen
Wurden auf der Seite **Fibu Buch.-Blätter** Standardgegenkonten für die Buch.-Blattnamen eingerichtet, wird das Gegenkonto beim Ausfüllen des Felds **Kontonr.** automatisch ausgefüllt. Andernfalls müssen die Felder **Kontonr.** und **Gegenkontonr.** manuell ausgefüllt werden. Bei einem positiven Betrag im Feld **Betrag** wird das Hauptkonto belastet, und auf dem Gegenkonto erfolgt eine Gutschrift. Bei einem negativen Betrag erfolgt eine Gutschrift auf dem Hauptkonto, und das Gegenkonto wird entsprechend belastet.

> [!NOTE]  
>   Die MwSt. für Haupt- und Gegenkonto wird getrennt berechnet, damit für die Konten unterschiedliche MwSt.-Prozentsätze verwendet werden können.

## <a name="working-with-recurring-journals"></a>Arbeiten mit wiederkehrenden Buchblättern
Bei einem wiederkehrenden Buch.-Blatt handelt es sich um ein Fibu Buch.-Blatt mit speziellen Feldern für die Verwaltung von Transaktionen, die häufig und ohne oder und mit geringen Änderungen gebucht werden. Mithilfe dieser speziellen Felder für wiederkehrende Transaktionen können Sie feste und variable Beträge buchen. Sie können auch ein automatisches Storno für den Tag nach dem Buchungsdatum festlegen und wiederkehrende Posten zusammen mit Verteilungsschlüsseln verwenden. Sie können auch Verteilungsschlüssel verwenden, um wiederkehrende Posten mit einem einzigen Vorgang zwischen verschiedenen Konten aufteilen zu können. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Buch.-Blatts auf mehrere Konten](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).

Mit einem wiederkehrenden Buchungsblatt müssen Posten, die regelmäßig gebucht werden, nur einmal eingetippt werden. Das bedeutet, dass Einträge wie Konten, Dimensionen oder Dimensionswerte nach der Buchung im Buchungsblatt verbleiben. Werden Anpassungen notwendig, können Sie diese mit jeder Buchung durchführen.

### <a name="recurring-method-field"></a>Feld Wiederholungsmethode
Dieses Feld legt fest, wie der in der Buch.-Blattzeile angegebene Betrag nach der Buchung bearbeitet werden soll. Wenn Sie z. B. bei jeder Buchung der Zeile den gleichen Betrag verwenden, können Sie den Betrag unverändert lassen. Wenn Sie dagegen immer den Betrag ändern, jedoch Konto und Text unverändert lassen, können Sie den Betrag nach der Buchung löschen lassen.

| An | Siehe |
| --- | --- |
|Fixiert|Der Betrag in der Buch.-Blattzeile wird nach der Buchung nicht geändert.|
|Variabel|Der Betrag wird nach dem Buchen aus der Buch.-Blattzeile gelöscht.|
|Saldo|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile in der Tabelle Gen angegeben werden. Fibu Buch.-Blatt Tabelle. Der Saldo auf dem Konto wird daher auf Null festgelegt. Denken Sie daran, das Feld **Verteilung %** auf der Seite **Verteilungsübersicht** auszufüllen. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Buch.-Blatts auf mehrere Konten](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).|
|Umgekehrt fix|Der Betrag in der Buch.-Blattzeile bleibt nach der Buchung erhalten und für den folgenden Tag wird ein Gegenposten gebucht.|
|Umgekehrt variabel|Der Betrag in der Buch.-Blattzeile wird nach der Buchung gelöscht und für den folgenden Tag wird ein Gegenposten gebucht.|
|Umgekehrt Ausgleich|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile auf der Seite **Zuweisungen** angegeben werden. Der Saldo auf dem Konto wird auf Null gesetzt, und ein Gegenposten wird am folgenden Tag gebucht.|

> [!NOTE]  
>  Die MwSt.-Felder können entweder in der Wiederk. Buch.-Blattzeile oder in der Verteilungs Buch.-Blattzeile ausgefüllt werden, aber nicht in beiden. Das heißt, sie können auf der Seite **Zuweisungen** nur passende Zeilen eintragen, wenn die entsprechenden Zeilen nicht im wiederkehrenden Buch.-Blatt eingetragen werden.

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

Wenn die Wiederholungsart im Wiederk. Buch.-Blatt auf **Ausgleich** oder **Umgekehrt Ausgleich** gesetzt ist, werden keine Dimensionswertcodes im Wiederk. Buch.-Blatt berücksichtigt, wenn das Konto auf Null gesetzt ist. Anders ausgedrückt, wenn Sie auf der Seite **Zuordnungen** eine wiederkehrende Zeile auf die verschiedenen Dimensionswerte verteilen, wird nur eine Umkehrbuchung erstellt. Wenn Sie also im Verteilungsbuch eine Zeile des wiederkehrenden Buch.-Blattes zuordnen, die einen Wertcode der Dimension enthält, dürfen Sie denselben Code nicht auf der Seite **Zuordnungen** eingeben. Andernfalls sind die Zahlen für die Dimensionswerte falsch.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Beispiel: Zuordnen von Mietzahlungen auf verschiedene Abteilungen
Sie zahlen jeden Monat Miete, daher haben Sie den Vertragsrabattbetrag auf das Kassenkonto in einer Zeile des wiederkehrenden Buch.-Blattes eingegeben. Auf der Seite **Zuordnungen** können Sie die Kosten auf die Kostenstellen entsprechend der jeweils belegten Quadratmeterzahlen aufteilen. Die Berechnung erfolgt aufgrund der Verteilungsprozente für jede Verteilungs-Buch.-Blattzeile. Sie können verschiedene Konten für jede Zeile des Buch.-Blattes Verteilungen eingeben (wenn die Miete auch auf verschiedene Konten aufgeteilt werden soll) oder Sie können dasselbe Konto mit verschiedenen Dimensionswertcodes für die Dimension "Kostenstelle" auf jeder Zeile eingeben.

## <a name="working-with-standard-journals"></a>Arbeiten mit Standard-Buchblättern
Wenn Sie Buch.-Blattzeilen erstellt haben, die Sie wahrscheinlich zu einem späteren Zeitpunkt erneut erstellen werden, können Sie sich entscheiden, diese als Standard Buch.-Blatt zu speichern, bevor Sie das Buch.-Blatt buchen. Diese Funktionalität wird in Artikel Buch.-Blätter und Buch.-Blätter angewendet.

> [!NOTE]  
>   Das folgende Verfahren bezieht sich auf das Artikel Buch.-Blatt, die Informationen betreffen jedoch auch das Standard Buch.-Blatt.

### <a name="to-save-a-standard-journal"></a>Ein Standard-Buch.-Blatt speichern:
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Artikel Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.
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
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Artikel Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die **Standard Buch.-Blatt abrufen** Aktion aus.

    Die Seite "Standard Artikel Buch.-Blätter" wird geöffnet und zeigt Codes und Beschreibungen für alle vorhandenen Standard Artikel Buch.-Blätter an.
3. Zum Überprüfen eines Standard Artikel Buch.-Blatts vor dem Auswählen für die Wiederverwendung klicken Sie auf **Buch.-Blatt anzeigen**.

    Alle Änderungen, die an einem Standard Artikel Buch.-Blatt vorgenommen werden, werden sofort implementiert. Sie sind beim nächsten Mal, wenn Sie das betreffenden Standard Artikel Buch.-Blatt öffnen oder verwenden. Daher sollten Sie sicher sein, dass die Änderung gewichtig genug ist, um sie allgemein zu übernehmen. Nehmen Sie andernfalls die spezifische Änderung am Artikel Buch.-Blatt vor, nachdem die Zeilen im Standard Artikel Buch.-Blatt eingefügt wurden. Siehe dazu auch Schritt 4 unten.
4. Auf der Seite **Standard Artikel Buch.-Blätter** wählen Sie das Standard Artikel Buch.-Blatt aus, das Sie erneut verwenden möchten, und klicken Sie auf **OK**.

    Jetzt wird das Artikel Buch.-Blatt mit den Zeilen aufgefüllt, die Sie als Standard Artikel Buch.-Blatt gespeichert haben. Wenn Buch.-Blattzeilen bereits im Artikel Buch.-Blatt vorhanden sind, werden die eingefügten Zeilen unterhalb der vorhandenen Buch.-Blattzeilen eingefügt.

    Normalerweise, d.h., wenn das Feld **Stückpreis speichern** während der Funktion **Als Standard Buch.-Blatt speichern** nicht markiert war, wird das Feld **Stückpreis** in den eingefügten Zeilen automatisch mit dem aktuellen Wert des Artikels gefüllt (der aus dem Feld **Einstandspreis** auf der Artikelkarte kopiert wird).

    > [!NOTE]  
    >   Wenn Sie eines der Felder **Stückzahl speichern** oder **Menge speichern** ausgewählt haben, sollten Sie jetzt überprüfen, ob die eingefügten Werte für diese bestimmte Lagerregulierung richtig sind, bevor Sie das Artikelprotokoll speichern.

    Wenn die eingefügten Artikel Buch.-Blattzeilen gespeicherte Stückpreise enthalten, die Sie nicht buchen möchten, können Sie sie schnell an den aktuellen Artikelwert anpassen:

6. Wählen Sie den Artikel, für den Sie den Lagerbestand anpassen möchten, und wählen Sie dann die Aktion **Einheitsbetrag neu berechnen** aus. Dadurch wird das Feld Stückpreis mit dem aktuellen Einstandspreis des Artikels aktualisiert.
7. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-renumber-document-numbers-in-journals"></a>Belegnummern in Buch.-Blättern neu nummerieren
Um sicherzustellen, dass Sie keine Buchungsfehler aufgrund der Reihenfolge der Belegnummern erhalten, können Sie die Funktion **Belegnummern neu nummerieren** verwenden, bevor Sie ein Buch.-Blatt buchen.

In allen Buch.-Blättern, die auf dem Fibu Buch.-Blatt basieren, kann das Feld **Dokumentennr.** bearbeitet werden, so dass Sie unterschiedliche Belegnummern für verschiedene Buch.-Blattzeilen oder die gleiche Belegnummer für die zugehörigen Buch.-Blattzeilen angeben können.

Wenn das Feld **Serien-Nr.** auf dem Buch.-Blatt ausgefüllt ist, erfordert die Buchungsfunktion in Fibu Buch.-Blättern, dass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen sequenziell angeordnet sind. Um sicherzustellen, dass Sie keine Buchungsfehler aufgrund der Reihenfolge der Belegnummern erhalten, können Sie die Funktion **Belegnummern neu nummerieren** verwenden. Wenn verwandte Buch.-Blattzeilen nach Belegnummern gruppiert wurden, bevor Sie die Funktion verwendet haben, bleiben sie gruppiert, können aber eine andere Belegnummer erhalten.

Diese Funktion funktioniert auch bei gefilterten Ansichten.

Jede Neunummerierung der Belegnummern berücksichtigt verwandte Anwendungen, wie etwa eine Zahlungsanwendung, die von dem Dokument auf der Buch.-Blattzeile an ein Kreditorenkonto durchgeführt wurde. Entsprechend werden die Felder**Ausgleichs-ID** und **Ausgleich mit Belegnr.** in den betroffenen Posten aktualisiert.

Die folgende Prozedur basiert auf der Seite**Fibu Buch.-Blatt**, gilt aber für alle anderen Buch.-Blätter, die auf dem Hauptbuch basieren, wie etwa die Seite **Zahlungs Buch.-Blatt**.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen"), geben Sie **Fibu Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.
2. Wenn Sie zum Buchen des Buchs bereit sind, wählen Sie auf der Registerkarte Aktionen, in der Gruppe Funktionen, die Option **Belegnummern neu nummerieren**.

Werte im Feld **Dokumentennr.** werden geändert, wo erforderlich, sodass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen in sequenzieller Reihenfolge stehen. Nach der Neunummerierung der Dokumente können Sie mit der Buchung des Buch.-Blatts fortfahren.

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Buchen von Transaktionen direkt in der Finanzbuchhaltung](finance-how-post-transactions-directly.md)  
[Buch.-Blatt-Buchungen stornieren und Rückgängigmachung von Eingängen/Versendungen](finance-how-reverse-journal-posting.md)  
[Kosten und Einkünfte zuteilen](year-allocate-costs-income.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Schließen von offenen Artikelposten aus einem festen Ausgleich im Artikel Buch.-Blatt](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Lager im Neubewertungs-Blatt neu bewerten](inventory-how-revalue-inventory.md)  
[Erfassen, Regulieren und Umbuchen von Lagerbestand mithilfe von Buch.-Blättern](inventory-how-count-adjust-reclassify.md)  
[Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Buch.-Blatt oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md)  
[Abstimmen von Kreditorenzahlungen mit dem Zahlungsjournal oder aus Kreditorenposten](payables-how-apply-purchase-transactions-manually.md)  
[Arbeiten mit Intercompany-Belegen und Buch.-Blättern](intercompany-how-work-documents-journals.md)  
