---
title: Mithilfe von Fibu Buch.-Blätern direkt in die Finanzbuchhaltung buchen
description: 'Mehr über die Nutzung von Buchungsblättern erfahren, um auf Sachkonten sowie auf andere Konten wie Bank-, Debitoren-, Kreditoren- oder Anlagekonten zu buchen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 08/29/2023
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# <a name="work-with-general-journals"></a>Mit Fibu Buch.-Blättern arbeiten

Die meisten finanziellen Transaktionen werden über Belege wie Einkaufsrechnungen und Verkaufsaufträge im Hauptbuch verbucht. Sie können jedoch auch geschäftliche Aktivitäten verarbeiten, wie z.B.:

* Einkauf
* Zahlungen
* Verwendung wiederkehrender Erfassungen zum Buchen von Abgrenzungen
* Rückerstattung von Mitarbeiterausgaben durch Buchung von Buchungsblattzeilen in Journalen  

Die meisten Erfassungen basieren auf dem Allgemeinen Buch.-Blatt, und Sie können alle Transaktionen auf der Seite **Allgemeines Buch.-Blatt** verarbeiten. Mehr dazu erfahren Sie unter [Transaktionen direkt im Hauptbuch buchen](finance-how-post-transactions-directly.md).  

Sie können zum Beispiel Spesen von Mitarbeitern zur Erstattung buchen. Erfahren Sie mehr unter [Datensätze für die Erstattung von Ausgaben der Mitarbeiter erfassen](finance-how-record-reimburse-employee-expenses.md).

[!INCLUDE [prod_short](includes/prod_short.md)] bietet jedoch auch Erfassungen, die für bestimmte Arten von Transaktionen optimiert sind, wie z.B. das **Zahlungsausgangs Buch.-Blatt** zum Erfassen von Zahlungen. Weitere Informationen finden Sie unter [Zahlungsbelege und Erstattungen im Zahlungsausgangs Buch.-Blatt](payables-how-post-payments-refunds.md).  

Mit den allgemeinen Erfassungen buchen Sie finanzielle Transaktionen auf Hauptbuch-Sachkonten und verschiedene andere Konten. Zu den anderen Konten gehören Bank-, Debitor-, Kreditor- und Mitarbeiterkonten. Die Buchung mit einem Allgemeinen Journal erstellt Erfassungen auf Hauptbuchkonten, auch wenn Sie beispielsweise eine Journalzeile auf ein Debitorenkonto buchen. Die Buchung wird über eine Buchungsgruppe auf ein Hauptbuch-Forderungskonto gebucht.

Die in ein Buch.-Blatt eingegebenen Informationen sind temporär und können geändert werden, solange sie sich im Buch.-Blatt befinden. Wenn Sie das Journal buchen, werden die Informationen in Erfassungen auf einzelnen Konten übertragen, wo sie nicht geändert werden können. Der Ausgleich gebuchter Posten kann jedoch aufgehoben werden, und Sie haben die Möglichkeit zum Buchen von Storno- oder Korrekturposten. Erfahren Sie mehr unter [Buch.-Blatt-Buchungen stornieren und Rückgängigmachung von Eingängen/Versendungen](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="add-context-to-general-journal-transactions"></a>Fibu Buch.-Blatt-Transaktionen Kontext hinzufügen

Wenn Sie ein Buchungsblatt erstellen, können Sie Links mit Kontext zu seinen Transaktionen hinzufügen. Wenn Sie das Buchungsblatt buchen, kopiert [!INCLUDE [prod_short](includes/prod_short.md)] die Links zu dem gebuchten Buchungsblatt und den Posten, die das Buchungsblatt erstellt. Die Bereitstellung von Links kann beispielsweise Ihrem Wirtschaftsprüfer das Leben erleichtern. Wenn Sie Bilder Ihrer Ausgabenbelege auf der Sharepoint-Website Ihres Unternehmens speichern, können Sie Links zu den Dateien hinzufügen. Wenn Sie das Buchungsblatt veröffentlichen, um Ihre Ausgaben einzureichen, kann Ihr Wirtschaftsprüfer schnell auf die Belegdateien zugreifen.

## <a name="use-journal-templates-and-batches"></a>Buch-Blattvorlagen und -namen verwenden

Es gibt mehrere Fibu Buch.-Blattvorlagen. Jede Buch.-Blattvorlage wird durch eine spezifisches Seite mit bestimmten Funktionen und den Feldern dargestellt, die benötigt werden, um diese Funktionen zu unterstützen, wie die Seite **Zahlungs-Abstimmungs-Buch.-Blatt**, um Bankzahlungen zu verarbeiten, und die Seite **Zahlungsausgangs Buch.-Blatt**, um Ihre Mitarbeiter zu bezahlen. Weitere Informationen finden Sie unter [Zahlungen vornehmen](payables-make-payments.md) und [Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Buch.-Blatt oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md).

Sie können zu jeder Buch.-Blattvorlage mehrere Buch.-Blattnamen als Buch-Stapel erstellen. Beispielsweise können Sie Ihre eigenen Buch-Stapel für das Zahlungsausgangsbuch erstellen, das Ihr persönliches Layout und Ihre Einstellungen hat. Der nächste Tipp ist ein Beispiel, wie Sie ein Buch.-Blatt anpassen.

> [!TIP]  
> Wenn Sie auf der Seite **Fibu Buch.-Blätter** in der Zeile für Ihren Batch das Kontrollkästchen **Ausgleichsbetrag vorschlagen** aktivieren, wird das Feld **Betrag** z.B. in den Buchungsblattzeilen für dieselbe Belegnummer automatisch mit dem Wert vorausgefüllt, der zum Ausgleich des Belegs erforderlich ist. Weitere Informationen finden Sie unter [[!INCLUDE[prod_short](includes/prod_short.md)] Werte vorschlagen lassen](ui-let-system-suggest-values.md).

> [!TIP]
> Sie können Felder in Buchungsblättern hinzufügen oder entfernen, indem Sie sie personalisieren. Erfahren Sie mehr unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Fibu Buch.-Blatt-Stapelverarbeitungen überprüfen

Sie können eine Hintergrundprüfung einschalten, um Verzögerungen beim Buchen zu vermeiden. Die Prüfung benachrichtigt Sie, wenn ein Fehler in dem Finanzjournal, an dem Sie gerade arbeiten, das Buchen des Journals verhindert. Auf der Seite **Fibu Buch.-Blatt** können Sie **Hintergrundfehlerprüfung** wählen, damit [!INCLUDE[prod_short](includes/prod_short.md)] Finanzbuch.-Blätter überprüft, wie z. B. Fibu Buch.Blätter oder Zahlungsausgangs Buch.-Blätter, während Sie an ihnen arbeiten.

Wenn Sie die Prüfung aktivieren, werden in der FactBox **Journalprüfung** Ausgaben in der aktuellen Zeile und im gesamten Batch angezeigt. Die Überprüfung erfolgt, wenn Sie einen Finanz-Buch.-Blattname laden und eine andere Buch.-Blattzeile auswählen. Die Kachel **Probleme insgesamt** in der Infobox zeigt die Gesamtanzahl von Problemen, die [!INCLUDE[prod_short](includes/prod_short.md)] gefunden hat, und Sie können sie auswählen, um eine Übersicht über die Probleme zu öffnen.

Mit den Aktionen **Zeilen mit Erfassungen anzeigen** und **Alle Zeilen anzeigen** können Sie zwischen Buchungsblattzeilen mit und ohne Erfassungen hin- und herschalten. Die FactBox **Details der Buchungsblattzeilen** bietet einen schnellen Überblick und Zugriff auf die Daten der Buchungsblattzeilen, wie z.B. das Sachkonto, den Debitor oder Kreditor und die Buchungseinrichtung für bestimmte Konten.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hauptkonten und Gegenkonten und Saldokonten verstehen

Wurden auf der Seite **Fibu Buch.-Blätter** Standardgegenkonten für die Buch.-Blattnamen eingerichtet, wird das Gegenkonto beim Ausfüllen des Felds **Kontonr.** automatisch ausgefüllt. Andernfalls müssen die Felder **Kontonr.** und **Gegenkontonr.** manuell ausgefüllt werden. Bei einem positiven Betrag im Feld **Betrag** wird das Hauptkonto belastet, und auf dem Gegenkonto erfolgt eine Gutschrift. Bei einem negativen Betrag erfolgt eine Gutschrift auf dem Hauptkonto, und das Gegenkonto wird entsprechend belastet.

> [!NOTE]  
> Die MwSt. für Haupt- und Gegenkonto wird getrennt berechnet, damit für die Konten unterschiedliche MwSt.-Prozentsätze verwendet werden können.

## <a name="work-with-recurring-journals"></a>Mit wiederkehrenden Buchblättern arbeiten

Ein Wiederk. Fibu Buch.-Blatt ist ein allgemeines Journal mit spezifischen Feldern zur Verwaltung von Transaktionen, die Sie häufig mit wenigen oder gar keinen Änderungen buchen. Zum Beispiel Transaktionen für Ausgaben wie Miete, Abonnements, Strom und Heizung. Mit wiederkehrenden Erfassungen können Sie feste und variable Beträge buchen und automatische Stornobuchungen für den Tag nach dem Buchungsdatum festlegen. Mit Zuweisungsschlüsseln können Sie die wiederkehrenden Buchungen auf verschiedene Konten aufteilen. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Buch.-Blatts auf mehrere Konten](#allocating-recurring-journal-amounts-to-several-accounts).

Mit einem wiederkehrenden Journal erstellen Sie die Erfassungen, die regelmäßig nur einmal gebucht werden sollen. So bleiben beispielsweise die Konten, Dimensionen, Dimensionswerte usw. nach der Buchung im Journal erhalten. Falls Änderungen erforderlich sind, können Sie diese bei jeder Buchung vornehmen.

### <a name="recurring-method-field"></a>Feld Wiederholungsmethode

Das Feld **Wiederkehrende Methode** ist wichtig. Es bestimmt, wie der Betrag in der Buchungsblattzeile nach der Buchung behandelt werden soll. Wenn Sie z.B. bei jeder Buchung der Zeile den gleichen Betrag verwenden, können Sie den Betrag beibehalten. Wenn Sie dieselben Konten und denselben Text in der Zeile verwenden, der Betrag aber bei jeder Buchung variiert, können Sie den Betrag nach der Buchung löschen.

| Aktion | Siehe |
| --- | --- |
|F Fest|Der Betrag in der Buch.-Blattzeile wird nach der Buchung nicht geändert.|
|V Variabel|Der Betrag wird nach dem Buchen aus der Buch.-Blattzeile gelöscht.|
|B Saldo|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile in der Tabelle Gen angegeben werden. Fibu Buch.-Blatt Tabelle. Der Saldo des Kontos wird auf Null festgelegt. Denken Sie daran, das Feld **Verteilung %** auf der Seite **Verteilungsübersicht** auszufüllen. Weitere Informationen finden Sie unter [Zuordnung von Beträgen des wiederkehrenden Buch.-Blatts auf mehrere Konten](#allocating-recurring-journal-amounts-to-several-accounts).|
|RF Umgekehrt fix|Der Betrag in der Buch.-Blattzeile bleibt nach der Buchung erhalten und für den folgenden Tag wird ein Gegenposten gebucht.|
|RV Umgekehrt variabel|Der Betrag in der Buch.-Blattzeile wird nach der Buchung gelöscht und für den folgenden Tag wird ein Gegenposten gebucht.|
|RB Umgekehrt Ausgleich|Der gebuchte Betrag des Kontos in der Zeile wird Konten zugewiesen, die für die Zeile auf der Seite **Zuweisungen** angegeben werden. Der Saldo auf dem Konto wird auf Null gesetzt, und ein Gegenposten wird am folgenden Tag gebucht.|
|Saldo nach Dimension|Die Journalzeile ordnet die Kosten basierend auf dem Saldo eines Sachkontos nach Dimensionen zu. Sie werden aufgefordert, die Dimensionsfilter festzulegen, die zur Berechnung des Kontostands des Sachkontos nach Dimension verwendet werden sollen, aus der Sie die Kosten zuordnen möchten. Alternativ können Sie später die Aktion **Dimensionsfilter festlegen** wählen.|
|Rückbuchungssaldo nach Dimension|Die Journalzeile ordnet die Kosten basierend auf den umgekehrten Ausgleich eines Sachkontos nach Dimensionen zu. Sie werden aufgefordert, die Dimensionsfilter festzulegen, die zur Berechnung des Kontostands des Sachkontos nach Dimension verwendet werden sollen, aus der Sie die Kosten zuordnen möchten. Sie können auch die Aktion **Dimensionsfilter festlegen** später wählen.|

> [!NOTE]  
> Die MwSt.-Felder können entweder in der Wiederk. Buch.-Blattzeile oder in der Verteilungs Buch.-Blattzeile ausgefüllt werden, aber nicht in beiden. Das heißt, sie können auf der Seite **Zuweisungen** nur passende Zeilen eintragen, wenn die entsprechenden Zeilen nicht im wiederkehrenden Buch.-Blatt eingetragen werden.

### <a name="recurring-frequency-field"></a>Feld Wiederholungsrate

Dieses Feld für die Datumsformel bestimmt, wie oft der Eintrag in der Buchungsblattzeile gebucht werden soll, und muss ausgefüllt werden. Mehr dazu erfahren Sie unter [Verwenden von Datumsformeln](ui-enter-date-ranges.md#use-date-formulas).

#### <a name="examples"></a>Beispiele

Wenn das Buch.-Blatt z. B. monatlich gebucht werden soll, geben Sie "1M" ein. Nach jeder Buchung wird dann das Datum im Feld **Buchungsdatum** auf dasselbe Datum im nächsten Monat aktualisiert.

Wenn Sie immer am Letzten des Monats buchen möchten, können Sie nach einem der folgenden Beispiele vorgehen:

* Sie können die erste Buchung am letzten Tag eines Monats buchen und die Wiederholungsrate 1T + 1M – 1T (1 Tag + 1 Monat –1 Tag) eingeben. Mit dieser Formel wird immer das richtige Datum berechnet, unabhängig davon, wie viele Tage der Monat hat.

* Buchen Sie den ersten Eintrag an einem beliebigen Tag des Monats, indem Sie 1M+CM eingeben. Diese Formel addiert einen ganzen Monat plus die verbleibenden Tage bis zum Letzten des Monats.

### <a name="expiration-date-field"></a>Ablaufdatumsfeld

Das Feld bestimmt das Datum, an dem die Zeile letztmalig gebucht werden soll. Die Zeile wird nach diesem Datum nicht mehr gebucht.

Die Verwendung des Feldes Verfallsdatum hat den Vorteil, dass die Zeile nicht sofort aus der Erfassung gelöscht wird. Sie können ein späteres Datum eingeben, so dass Sie die Zeile auch in der Zukunft verwenden können.

Wenn das Feld leer ist, wird die Zeile jedes Mal gebucht, bis sie aus dem Journal gelöscht wird.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Zuordnung von Beträgen des wiederkehrenden Buch.-Blatts auf mehrere Konten

Auf der Seite **Wiederk. Fibu Buch.-Blatt** können Sie die **Verteilungen** Aktion auswählen und bestimmen, wie Beträge der Zeile des wiederkehrenden Buch.-Blatts auf mehrere Konten und Dimensionen zugeordnet werden. Die Zuordnung dient als Ausgleichskontozeile für die Buchungsblattzeile.

Wie bei einem wiederkehrenden Journal geben Sie eine Zuweisung einmalig ein und sie bleibt nach der Buchung im Zuweisungsjournal erhalten. Sie müssen nicht jedes Mal Beträge und Zuweisungen eingeben, wenn Sie die Buchungsblattzeile buchen.

Wenn die wiederkehrende Methode im Erfassungsjournal auf **Saldo** oder **Saldo umkehren** festgelegt ist, werden die Wertcodes der Dimensionen im Erfassungsjournal nicht berücksichtigt, wenn das Konto auf Null festgelegt ist. Wenn Sie eine wiederkehrende Zeile auf der Seite **Zuordnungen** den Dimensionenwerten zuordnen, wird nur ein Storno erstellt.

> [!NOTE]
> Wenn Sie eine wiederkehrende Buchungsblattzeile zuweisen, die einen Code für Dimensionswerte enthält, geben Sie denselben Code nicht auf der Seite **Zuordnungen** ein. Andernfalls sind die Zahlen für die Dimensionswerte falsch.  

Um wiederkehrende Journalbeträge basierend auf Dimensionen zuzuweisen, legen Sie das Feld **Wiederkehrende Methode** auf **Saldo nach Dimension** oder **Umkehren des Gleichgewichts nach Dimension** fest. Wenn die wiederkehrende Methode im Dauerjournal auf **Saldo nach Dimension** oder **Saldo nach Dimension umkehren** festgelegt ist, werden Dimensionswertcodes im Dauerjournal berücksichtigt, wenn das Konto auf Null gesetzt wird. Wenn Sie eine wiederkehrende Zeile auf der Seite **Zuordnungen** den Dimensionswerten zuordnen, werden Stornobuchungen erstellt, die der Anzahl der Dimensionswertkombinationen entsprechen, aus denen sich der Saldo zusammensetzt. Wenn Sie einen Kontosaldo über eine wiederkehrende Erfassung zuweisen, die einen Dimensionswertcode enthält, denken Sie daran, **Saldo nach Dimension** oder **Saldo nach Dimension stornieren** zu verwenden, um sicherzustellen, dass die Dimensionswerte korrekt aus dem Quellkonto ausgeglichen oder storniert werden.  

Ihr Unternehmen verfügt beispielsweise über einige Geschäftsbereiche und eine Handvoll Abteilungen, die Ihre Controller als Dimensionen eingerichtet haben. Um den Prozess der Buchungserfassung zu beschleunigen, müssen die Sachbearbeiter nur die Dimensionen der Geschäftsbereiche eingeben. Da jede Unternehmenseinheit über spezifische Zuordnungsschlüssel für die Dimension Abteilung verfügt, z.B. basierend auf der Anzahl der Mitarbeiter, können Sie die wiederkehrenden Methoden **BD Ausgleich nach Dimension** oder **RBD Umkehrung des Ausgleichs nach Dimension** verwenden, um die Ausgaben für jede Unternehmenseinheit auf der Grundlage der Zuordnungsschlüssel den richtigen Abteilungen zuzuordnen.  

> [!NOTE]
> Bemaßungen, die Sie in Zuordnungszeilen festlegen, werden nicht automatisch berechnet, und Sie müssen angeben, welche Bemaßungswerte in den Zuordnungskonten festgelegt werden müssen. Wenn Sie die Verknüpfung zwischen der Quellkontodimension und der Zuordnungskontodimension beibehalten möchten, empfehlen wir die Verwendung der Funktionen [Kostenrechnung](finance-about-cost-accounting.md).

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Beispiel: Zuordnen von Mietzahlungen auf verschiedene Abteilungen

Sie zahlen monatlich Miete, also haben Sie den Betrag auf dem Kassenkonto in einer wiederkehrenden Buchungsblattzeile erfasst. Auf der Seite **Zuweisungen** können Sie die Dimension Abteilung verwenden, um die Ausgaben auf mehrere Abteilungen aufzuteilen. Zum Beispiel nach der Anzahl der Quadratmeter, die jede Abteilung belegt. Die Berechnung erfolgt aufgrund der Verteilungsprozente für jede Verteilungs-Buch.-Blattzeile. Sie können die Aufteilung auf verschiedene Arten vornehmen:

* Geben Sie verschiedene Konten in verschiedenen Zuordnungszeilen ein, um die Mietkosten auf mehrere Konten aufzuteilen.
* Geben Sie dasselbe Konto ein, verwenden Sie aber in jeder Zeile unterschiedliche Dimensionswertcodes für die Dimension Abteilung.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### <a name="calculate-the-reversal-date"></a>Stornierungsdatum berechnen

Wenn Sie wiederkehrende Fibu Buch.-Blätter verwenden, um Abgrenzungen am Ende einer Periode zu buchen, ist es wichtig, die volle Kontrolle über Stornierungsposten zu haben. Auf der Seite **Wiederkehrende Fibu Buch.-Blätter** können Sie mithilfe des Felds **Stornierungsdatumsberechnung** das Datum steuern, an dem Stornierungsposten gebucht werden, wenn wiederkehrende Stornierungsmethoden verwendet werden.

#### <a name="example"></a>Beispiel

Abgrenzungen werden in der Regel mit den wiederkehrenden Methoden **Fest**, **Variabel** oder **Saldo** in der Buchungsblattzeile gebucht. Das Buchungsdatum des gebuchten Betrags auf dem Konto in der Buch.-Blattzeile wird anhand der wiederkehrenden Häufigkeit berechnet. Das Buchungsdatum für die Gegenposten wird mithilfe des Felds **Stornierungsdatumsberechnung** wie folgt berechnet:

* Wenn das Feld leer ist, wird der Gegenposten am nächsten Tag gebucht.
* Wenn das Feld eine Datumsformel enthält (z. B. **5D** für fünf Tage) wird der Gegenposten mit einem Buchungsdatum gebucht, das anhand der Stornierungsdatumberechnung berechnet wird.

> [!NOTE]
> Standardmäßig ist das Feld **Stornierungsdatumsberchnung** auf der Seite **Wiederkehrende Fibu Buch.-Blätter** nicht verfügbar. Um das Feld zu verwenden, müssen Sie es hinzufügen, indem Sie die Seite personalisieren. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

## <a name="work-with-standard-journals"></a>Mit Standard-Buchblättern arbeiten

Wenn Sie Buchungsblattzeilen erstellt haben, von denen Sie wissen, dass Sie sie wahrscheinlich später noch einmal erstellen werden, können Sie sie als Standardjournal speichern, bevor Sie das Journal buchen. Dasselbe gilt für Artikel Buch.-Blätter und Allgemeine Journale.

> [!NOTE]
> Standard-Buchblätter enthalten möglicherweise nicht alle Felder, die Sie in die resultierenden Sachkontoeinträge aufnehmen möchten. Wenn Sie z. B. eine allgemeine Standard Fibu Buch.-Blatt zum Erfassen einer Zahlung verwenden, enthalten die Sachkontoeinträge das Feld „Zahlungsformencode“ nicht.

> [!NOTE]  
> Das folgende Verfahren bezieht sich auf das Artikel Buch.-Blatt, die Informationen betreffen jedoch auch das Standard Buch.-Blatt.

### <a name="to-save-a-standard-journal"></a>Ein Standard-Buch.-Blatt speichern:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Geben Sie in mindestens eine Buch.-Blattzeile ein.
3. Wählen Sie die Buch.-Blattzeilen aus, die Sie wieder verwenden möchten.
4. Wählen Sie die **Als Standard Buch.-Blatt speichern** Aktion aus.
5. Auf der Anforderungsseite **Als Standard Artikel Buch.-Blatt speichern** müssen Sie ein neues oder vorhandenes Standard Buch.-Blatt eingeben, in dem die Zeilen gespeichert werden sollen:

    Wenn Sie bereits ein oder mehrere Artikel Buch.-Blätter erstellt haben und eines davon durch die neuen Artikel Buchungsblattzeilen ersetzen möchten, wählen Sie im Feld **Code** das Artikel Buch.-Blatt aus.
6. Wählen Sie **OK**, um zu bestätigen, dass Sie den Inhalt des vorhandenen Artikel Buch.-Blattes ersetzen möchten.
7. Um die Werte im Feld **Einheitsbetrag** des Standard-Artikel-Journals zu speichern, wählen Sie das Feld **Einheitsbetrag speichern**.
8. Um die Werte im Feld **Menge** zu speichern, wählen Sie das Feld **Menge speichern**.
9. Wählen Sie **OK**, um das Standard-Artikel-Journal zu speichern.

Wenn Sie das Standard-Artikel Buch.-Blatt speichern, wird die Seite Artikel Buch.-Blatt angezeigt, auf der Sie die Erfassung vornehmen können.

### <a name="to-reuse-a-standard-journal"></a>Standard-Protokolle wieder nutzen

> [!NOTE]
> Standardbuchblätter haben nicht immer die gleichen Felder wie allgemeine Buchblätter. Wenn Sie die Aktion „Standardbuchblätter abrufen“ verwenden, um die Felder in das allgemeine Buchblatt zu kopieren, enthält das allgemeine Buchblatt möglicherweise weniger Informationen, als bei der manuellen Erstellung. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Element Buch.-Blätter** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die **Standard Buch.-Blatt abrufen** Aktion aus.
3. Zum Überprüfen eines Standard Artikel Buch.-Blatts vor dem Auswählen für die Wiederverwendung klicken Sie auf **Buch.-Blatt anzeigen**.

    Änderungen, die Sie in einem Artikel Buch.-Blatt vornehmen, werden sofort implementiert und sind beim nächsten Öffnen oder Wiederverwenden des Artikel Buch.-Blattes wieder vorhanden. Vergewissern Sie sich, dass die Änderung wichtig genug ist, um sie allgemein anzuwenden. Andernfalls nehmen Sie die spezifische Änderung im Artikel Buch.-Blatt vor, nachdem die Zeilen des Standard Artikel Buchungsblattes hinzugefügt wurden. Siehe dazu auch Schritt 4.
4. Wählen Sie auf der Seite **Standard Artikel Buch.-Blätter** das Standard Artikel Buch.-Blatt aus, das Sie wiederverwenden möchten, und wählen Sie dann **OK**.

    Das Artikel Buch.-Blatt enthält die von Ihnen gespeicherten Zeilen. Wenn das Artikel Buch.-Blatt bereits Zeilen enthält, erscheinen die neuen Zeilen nach diesen.

    Wenn Sie den Schalter **Betrag pro Einheit speichern** beim Speichern des Buchblattes nicht aktivieren, enthält das Feld **Betrag pro Einheit** in den Zeilen, die aus dem Standardjournal hinzugefügt werden, den Wert aus dem Feld **Kosten pro Einheit** auf der Artikelkarte.

    > [!NOTE]  
    > Wenn Sie die Schalter **Einheit speichern** oder **Menge speichern** beim Speichern des Buchblattes aktiviert haben, stellen Sie sicher, dass die neuen Werte korrekt sind, bevor Sie das Artikel Buch.-Blatt buchen.
    >
    > Wenn die eingefügten Artikel Buchungsblattzeilen gespeicherte Einheitsbeträge enthalten, die Sie nicht buchen möchten, können Sie sie an den aktuellen Wert des Artikels anpassen.

5. Wählen Sie den Artikel, für den Sie den Lagerbestand anpassen möchten, und wählen Sie dann die Aktion **Einheitsbetrag neu berechnen** aus. Durch diese Aktion wird das Feld Betrag pro Einheit mit den aktuellen Kosten pro Einheit des Artikels aktualisiert.
6. Wählen Sie die Aktion **Buchen**.

## <a name="to-renumber-document-numbers-in-journals"></a>Belegnummern in Buch.-Blättern neu nummerieren

Um durch die Belegnummer verursachte Buchungsfehler zu vermeiden, können Sie die Aktion **Belegnummern neu nummerieren** verwenden, bevor Sie ein Journal buchen.

In allen Buch.-Blättern, die auf dem Fibu Buch.-Blatt basieren, kann das Feld **Dokumentennr.** bearbeitet werden, so dass Sie unterschiedliche Belegnummern für verschiedene Buch.-Blattzeilen oder die gleiche Belegnummer für die zugehörigen Buch.-Blattzeilen angeben können.

Wenn das Feld **Serien-Nr.** auf dem Buch.-Blatt ausgefüllt ist, erfordert die Buchungsfunktion in Fibu Buch.-Blättern, dass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen sequenziell angeordnet sind. Wählen Sie einfach die Aktion **Belegnummern neu nummerieren** aus, und relevante **Belegnr.**-Felder werden anschließend aktualisiert. Wenn zusammengehörige Buchungsblattzeilen nach Belegnummern gruppiert waren, bevor Sie die Funktion verwendet haben, bleiben sie gruppiert, erhalten aber möglicherweise eine andere Belegnummer.  

Diese Funktion funktioniert auch bei gefilterten Ansichten.

Bei einer Neunummerierung der Belegnummern werden zusammenhängende Anwendungen berücksichtigt, z.B. ein Zahlungsantrag, der von dem Beleg in der Buchungsblattzeile auf ein Kreditorenkonto gestellt wurde. Dementsprechend werden die Felder **Antrags-ID** und **Antrags-Dok. Nr.** in den Sachkontoeinträgen aktualisiert werden.

### <a name="to-renumber-documents-in-journals"></a>Belege in Buch.-Blättern neu nummerieren

Die folgende Prozedur basiert auf der Seite **Fibu Buch.-Blatt**, gilt aber für alle anderen Buch.-Blätter, die auf dem Hauptbuch basieren, wie etwa die Seite **Zahlungs Buch.-Blatt**.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Allgemeine Erfassungen** ein, und wählen Sie dann den entsprechenden Link.
2. Wenn Sie bereit sind, das Journal zu buchen, wählen Sie die Aktion **Belegnummern neu nummerieren**.

Werte im Feld **Dokumentennr.** werden geändert, wo erforderlich, sodass die Belegnummern auf einzelnen oder gruppierten Buch.-Blattzeilen in sequenzieller Reihenfolge stehen. Nachdem die Belege neu nummeriert wurden, können Sie das Journal buchen.

## <a name="see-also"></a>Siehe auch

[Transaktionen direkt in der Finanzbuchhaltung buchen](finance-how-post-transactions-directly.md)  
[Buch.-Blatt-Buchungen stornieren und Eingänge/Lieferungen rückgängig machen](finance-how-reverse-journal-posting.md)  
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
