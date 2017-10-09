---
title: "Mithilfe von Fibu Buch.-Blätern direkt in die Finanzbuchhaltung buchen| Microsoft Docs"
description: "Mehr über die Nutzung von Fibu Buch.-Blätter erfahren, um auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten zu buchen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b573bb55c29de329e5d9a804b49a91687dc369ff
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-general-journals"></a>Arbeiten mit Fibu Buch.-Blättern
Die meisten Finanztransaktionen werden in der Finanzbuchhaltung von Geschäftsbelegen wie Einkaufsrechnungen und Verkaufsaufträge gebucht. Für Geschäftsaktivitäten, die nicht in einem Beleg in[!INCLUDE[d365fin](includes/d365fin_md.md)] festgehlaten sind, wie kleinere Aufwendungen oder Zahlungseingänge, können Sie die entsprechenden Transaktionen erstellen, indem Sie die Buch.-Blattzeilen im **Fibu Buch.-Blatt** buchen. Weitere Informationen finden Sie unter [So gehts: Transaktionen direkt in der Finanzbuchhaltung buchen.](finance-how-post-transactions-directly.md).

Beispielsweise können Sie die Kosten der Mitarbeiter, die sie selber bezahlt haben buchen, um später zurückzuahlen. Weitere Informationen finden Sie unter [Vorgehensweise: Erstatten Sie die Ausgaben der Mitarbeiter zurück](finance-how-record-reimburse-employee-expenses.md).

Fibu Buch.-Blätter dienen zum Buchen auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Debitoren- oder Mitarbeiterkonten. Bei der Buchung mit einem Fibu Buch.-Blatt werden immer Posten für Sachkonten erstellt. Dies gilt auch, wenn beispielsweise eine Buch.-Blattzeile auf ein Debitorenkonto gebucht wird, da ein Posten im Rahmen einer Buchungsgruppe auf ein Fibu-Debitorenkonto gebucht wird.

Die in ein Buch.-Blatt eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Buch.-Blatt befinden. Durch Buchen des Buch.-Blatts werden die Informationen in Posten auf Konten übertragen und können nicht mehr geändert werden. Der Ausgleich gebuchter Posten kann jedoch aufgehoben werden, und Sie haben die Möglichkeit zum Buchen von Storno- oder Korrekturposten. Weitere Informationen finden Sie unter [Gewusst wie: Buchungen rückgängig machen](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Buch-Blattvorlagen und Stapel nutzen
Es gibt mehrere Fibu Buch.-Blattvorlagen. Jede Buch.-Blattvorlage wird durch ein spezifisches Fenster mit bestimmten Funktionen und den Feldern dargestellt, die benötigt werden, um diese Funktionen zu unterstützen, wie das Fenster **Zahlungs-Abstimmungs-Buch.-Blatt**, um Bankzahlungen und das Fenster **Zahlungsausgangs Buch.-Blatt** zu verarbeiten, um Ihre Mitarbeiter zu bezahlen. Weitere Informationen finden Sie unter [Anwenden von Zahlungen](payables-make-payments.md) und [Vorgehensweise: Ausgleichen Debitoren-Zahlungen manuell aus](receivables-how-apply-sales-transactions-manually.md).

Sie können zu jeder Buch.-Blattvorlage mehrere Buch.-Blattnamen als Buch-Stapel erstellen. Beispielsweise können Sie Ihre eigenen Buch-Stapel für das Zahlungsausgangsbuch erstellen, das Ihr persönliches Layout und Ihre Einstellungen hat. Der nächste Tipp ist ein Beispiel, wie Sie ein Buch.-Blatt anpassen.

> [!TIP]  
> Wenn Sie das Kontrollkästchen **Ausgleichsbetrag vorschlagen** in der Zeile für Ihren Stapel im **Fibu Buch.-Blattnamen** auswählen, dann werden das Feld **Betrag**, beispielsweise Fibu Buch.-Blattzeilen für dieselbe Belegnummer automatisch mit dem Wert, der zum Ausgleichen des Belegs erforderlich ist, ausgefüllt. Weitere Informationen finden Sie unter[[!INCLUDE[d365fin](includes/d365fin_md.md)]Werte Vorschlagen](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hauptkonten und Gegenkonten und Saldokonten verstehen
Wurden auf der Seite **Fibu Buch.-Blätter** Standardgegenkonten für die Buch.-Blattnamen eingerichtet, wird das Gegenkonto beim Ausfüllen des Felds **Kontonr.** automatisch ausgefüllt. Andernfalls müssen die Felder **Kontonr.** und **Gegenkontonr.** manuell ausgefüllt werden. Bei einem positiven Betrag im Feld **Betrag** wird das Hauptkonto belastet, und auf dem Gegenkonto erfolgt eine Gutschrift. Bei einem negativen Betrag erfolgt eine Gutschrift auf dem Hauptkonto, und das Gegenkonto wird entsprechend belastet.

> [!NOTE]  
>   Die MwSt. für Haupt- und Gegenkonto wird getrennt berechnet, damit für die Konten unterschiedliche MwSt.-Prozentsätze verwendet werden können.

## <a name="working-with-recurring-journals"></a>Arbeiten mit wiederkehrenden Buchblättern
Bei einem wiederkehrenden Buch.-Blatt handelt es sich um ein Fibu Buch.-Blatt mit speziellen Feldern für die Verwaltung von Transaktionen, die häufig mit geringen oder keinen Änderungen gebucht werden. Mithilfe dieser speziellen Felder für wiederkehrende Transaktionen können Sie feste und variable Beträge buchen. Sie können auch ein automatisches Storno für den Tag nach dem Buchungsdatum festlegen und wiederkehrende Posten zusammen mit Verteilungsschlüsseln verwenden.

## <a name="working-with-standard-journals"></a>Arbeiten mit Standard-Buchblättern
Wenn Sie Buch.-Blattzeilen erstellt haben, die Sie wahrscheinlich zu einem späteren Zeitpunkt erneut erstellen werden, können Sie sich entscheiden, diese als Standard Buch.-Blatt zu speichern, bevor Sie das Buch.-Blatt buchen. Diese Funktionalität wird in Artikel Buch.-Blätter und Buch.-Blätter angewendet.

> [!NOTE]  
>   Das folgende Verfahren bezieht sich auf das Artikel Buch.-Blatt, die Informationen betreffen jedoch auch das Standard Buch.-Blatt.

### <a name="to-save-a-standard-journal"></a>Ein Standard-Buch.-Blatt speichern:
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buchblatt** ein und wählen den zugehörenden Link aus.
2. Geben Sie in mindestens eine Buch.-Blattzeile ein.
3. Wählen Sie die Buch.-Blattzeilen aus, die Sie wieder verwenden möchten.
4. Wählen Sie die **Als Standard Buch.-Blatt speichern** Aktion aus.
5. Im Anforderungsfenster **Als Standard Artikel Buch.-Blatt speichern** müssen Sie ein neues oder vorhandenes Standard Buch.-Blatt eingeben, in dem die Zeilen gespeichert werden sollen:

    Wenn Sie bereits mindestens ein Standard-Artikel Buch.-Blatt erstellt haben und es durch eine neue Zusammenstellung von Artikel Buch.-Blattzeilen ersetzen möchten, können Sie Feld Code den gewünschten Code auszuwählen.
6. Wählen Sie die Schaltfläche **OK**, um zu bestätigen, dass Sie das vorhandene Standard-Artikel-Buch.-Blatt überschreiben und seinen gesamten Inhalt ersetzen möchten.
7. Wählen Sie das Feld **Stückpreis speichern** aus, wenn Sie die Werte im Feld **Stückpreis** im Standard Artikel Buch.-Blatt speichern möchten.
8. Wählen Sie das Feld **Menge speichern** aus, wenn die Anwendung die Werte im Feld **Menge** speichern soll.
9. Wählen Sie **OK** aus, um das Standard Artikel Buch.-Blatt zu speichern.

Wenn Sie das Standard-Artikel-Buch.-Blatt gespeichert haben, wird das Fenster Artikel Buch.-Blatt angezeigt, so dass Sie mit der Buchung fortfahren können. Diesen Vorgang können Sie beim Buchen dieser oder einer ähnlichen Zeile einfach wiederholen.

### <a name="to-reuse-a-standard-journal"></a>Standard-Protokolle wieder nutzen
1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buchblatt** ein und wählen den zugehörenden Link aus.
2. Wählen Sie die **Standard Buch.-Blatt abrufen** Aktion aus.

    Das Fenster Standard-Artikelprotokolle wird geöffnet und zeigt Codes und Beschreibungen für alle vorhandenen Standard-Artikelprotokolle an.
3. Zum Überprüfen eines Standard Artikel Buch.-Blatts vor dem Auswählen für die Wiederverwendung klicken Sie auf **Buch.-Blatt anzeigen**.

    Alle Änderungen, die an einem Standard Artikel Buch.-Blatt vorgenommen werden, werden sofort implementiert. Sie sind beim nächsten Mal, wenn Sie das betreffenden Standard Artikel Buch.-Blatt öffnen oder verwenden. Daher sollten Sie sicher sein, dass die Änderung gewichtig genug ist, um sie allgemein zu übernehmen. Nehmen Sie andernfalls die spezifische Änderung am Artikel Buch.-Blatt vor, nachdem die Zeilen im Standard Artikel Buch.-Blatt eingefügt wurden. Siehe dazu auch Schritt 4 unten.
4. Im Fenster **Standard Artikel Buch.-Blätter** wählen Sie das Standard Artikel Buch.-Blatt aus, das Sie erneut verwenden möchten, und klicken Sie auf **OK**.

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

Die folgende Prozedur basiert auf dem Fenster **Fibu Buch.-Blatt**, gilt aber für alle anderen Buch.-Blätter, die auf dem Hauptbuch basieren, wie etwa das Fenster **Zahlungs Buch.-Blatt**.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Fibu Buch.-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wenn Sie zum Buchen des Buchs bereit sind, wählen Sie auf der Registerkarte Aktionen, in der Gruppe Funktionen, die Option **Belegnummern neu nummerieren**.

Werte im Feld **Dokumentennr.** werden geändert, wo erforderlich, sodass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen in sequenzieller Reihenfolge stehen. Nach der Neunummerierung der Dokumente können Sie mit der Buchung des Buch.-Blatts fortfahren.

## <a name="see-also"></a>Siehe auch
[Vorgehensweise: Buchen von Transaktionen direkt in der Finanzbuchhaltung](finance-how-post-transactions-directly.md)  
[So geht's: Buchungen stornieren](finance-how-reverse-journal-posting.md)  
[Erklärt, wie Kosten und Einnahmen zugewiesen werden.](year-allocate-costs-income.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

