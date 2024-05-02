---
title: Verwalten von Speicher durch Löschen von Belegen oder Komprimieren von Daten
description: 'Erfahren Sie, wie Sie mit sich ansammelnden historischen Belegen umgehen (und die Menge der in einer Datenbank gespeicherten Daten reduzieren), indem Sie sie löschen oder komprimieren.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 09/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Verwalten von Speicher durch Löschen von Belegen oder Komprimieren von Daten

Ein Benutzer mit einer zentralen Rolle, z. B. der Anwendungsadministrator, muss sich regelmäßig um die angesammelten historischen Belege kümmern, indem er diese löscht oder komprimiert.  

> [!TIP]
> Erfahren Sie mehr über andere Möglichkeiten, um die Menge der in einer Datenbank gespeicherten Daten zu reduzieren. Lesen Sie dazu [Reduzierung der in Business Central-Datenbanken gespeicherten Daten](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) in unserer Dokumentation für Entwickler und IT-Profis.

## Löschen von Belegen

In bestimmten Situationen kann es erforderlich sein, dass Sie fakturierte Bestellungen löschen müssen. Sie können sie jedoch erst löschen, wenn Sie die Artikel in den Bestellungen vollständig in Rechnung gestellt und erhalten haben. [!INCLUDE[prod_short](includes/prod_short.md)] hilft Ihnen, dies zu überprüfen.

Retouren werden normalerweise gelöscht, nachdem sie in Rechnung gestellt wurden. Wenn Sie eine Rechnung buchen, wird sie auf die Seite **Gebuchte Einkaufsgutschrift** übertragen. Wenn Sie das Kontrollkästchen **Rücklieferung bei Gutschrift** auf der Seite **Kreditoren & Einkauf Einr.** aktiviert haben, wird die Rechnung auf die Seite **Gebuchte Rücklieferung** übertragen. Sie können die Belege mithilfe der Stapelverarbeitung **Erledigte Eink.-Rekl. löschen** löschen. Vor dem Löschen prüft die Stapelverarbeitung, ob die Einkaufsreklamationen vollständig geliefert und fakturiert wurden.  

Rahmenbestellungen werden nicht automatisch gelöscht, nachdem Sie alle zugehörigen Bestellungen verarbeitet und fakturiert haben. Stattdessen können Sie sie mit der Stapelverarbeitung **Erledigte Rahmenbestellungen löschen** löschen.  

Fakturierte Serviceaufträge werden in der Regel automatisch gelöscht, nachdem sie vollständig fakturiert wurden. Wenn eine Rechnung gebucht wird, wird ein entsprechender Posten erstellt, der dann auf der Seite **Gebuchte Servicerechnungen** eingesehen werden kann.  

Serviceaufträge werden jedoch nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags von der Seite **Servicerechnung** und nicht vom Serviceauftrag selbst gebucht wurde. Sie müssen solche fakturierten Aufträge möglicherweise manuell löschen, indem Sie die Stapelverarbeitung **Fakturierte Serviceaufträge löschen** ausführen.  

## Daten mit Datumskomprimierung komprimieren

Sie können Daten in [!INCLUDE [prod_short](includes/prod_short.md)] komprimieren, um Platz in der Datenbank zu sparen, wodurch Sie in [!INCLUDE [prod_short](includes/prod_short.md)] online sogar Geld sparen können. Die Komprimierung, die auf Daten und Funktionen basiert, fasst mehrere alte Posten zu einem neuen Posten zusammen.

Sie können Posten komprimieren, die alle der folgenden Bedingungen erfüllen:

* Sie stammen aus abgeschlossenen Geschäftsjahren.
* Das Feld **Öffnen** ist auf **Nein** festgelegt.
* Sie sind mindestens fünf Jahre alt. Wenn Sie Daten komprimieren möchten, die weniger als fünf Jahre alt sind, wenden Sie sich an Ihren Microsoft-Partner.

So können z. B. Kreditorenposten aus früheren Geschäftsjahren komprimiert werden, sodass pro Konto und Monat nur ein Haben- und ein Sollposten vorhanden ist. Der Betrag des neuen Postens ergibt sich aus der Summe aller komprimierten Posten. Das zugewiesene Datum ist das Startdatum für den komprimierten Zeitraum, z. B. der erste Tag des Monats (wenn die Posten nach Monaten komprimiert sind). Nach der Komprimierung können Sie immer noch die Nettoveränderung für jedes Konto im vorherigen Geschäftsjahr sehen.

Die Anzahl der Posten, die im Zuge der Datumskomprimierung erstellt werden, hängt von der Anzahl der festgelegten Filter, den kombinierten Feldern und der ausgewählten Periodenlänge ab. Es gibt immer mindestens einen Posten. Wenn die Stapelverarbeitung beendet ist, können Sie das Ergebnis auf der Seite **Datumskomprimierungsjournal** sehen.

Sie können mit Stapelverarbeitungen die folgenden Datentypen komprimieren.

* Finanzposten – Sachposten, Mehrwertsteuerposten, Bankposten, Finanzbudgetposten, Debitorenposten und Kreditorenposten
* Lagerplatzposten
* Ressourcenposten
* Artikelbudgetposten
* Anlagenposten (FA), FA-Wartungsposten und FA-Versicherungsposten

Wenn Sie Kriterien für die Komprimierung festlegen, können Sie den Inhalt bestimmter Felder mit den Optionen unter **Feldinhalt beibehalten** beibehalten. Die verfügbaren Felder hängen von den Daten ab, die Sie komprimieren.

> [!NOTE]
> Bevor Sie die Datumskomprimierung ausführen können, müssen Ihre Analyseansichten aktuell sein. Mehr dazu erfahren Sie im Abschnitt [Aktualisieren einer Analyseansicht](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Nach der Komprimierung werden die Inhalte der folgenden Felder in jedem Fall beibehalten: **Buchungsdatum**, **Kreditorennr.**, **Belegart**, **Währungscode**, **Buchungsgruppe**, **Betrag**, **Restbetrag**, **Ursprungsbetrag (MW)**, **Restbetrag (MW)**, **Betrag (MW)**, **Einkauf (MW)**, **Rechnungsrabatt (MW)**, **Skonto gewährt (MW)** und **Skonto möglich**.

## Komprimierte Posten buchen

Komprimierte Posten werden etwas anders gebucht als Standardbuchungen. Dies dient dazu, die Anzahl der durch die Datumskomprimierung erstellten neuen Sachposten zu verringern. Dies ist besonders wichtig, wenn Sie Informationen wie Dimensionen und Belegnummern aufbewahren. Durch die Datumskomprimierung werden neue Posten wie folgt erstellt:

* Auf der Seite **Sachposten** werden neue Posten für die komprimierten Posten erstellt. Das Feld **Beschreibung** enthält den Begriff **Datumskomprimiert**, damit die komprimierten Posten leicht zu identifizieren sind. 
* Auf Sachkontoseiten, wie z. B. der Seite **Debitorenposten**, werden ein oder mehrere neue Posten erstellt. 

Der Buchungsprozess erzeugt Lücken in der Nummernreihe für Posten auf der Seite **Sachposten**. Diese Nummern werden nur den Posten auf den Sachkontoseiten zugewiesen. Der den Posten zugeordnete Nummernkreis ist auf der Seite **Fibujournal** in den Feldern **Von Lfd. Nr.** und **Bis Lfd. Nr.** verfügbar. 

> [!NOTE]
> Nachdem Sie die Datumskomprimierung ausgeführt haben, werden alle Konten im Sachkonto gesperrt. Das bedeutet, dass Sie z. B. keine Kreditoren- oder Bankposten für die von der Komprimierung betroffenen Konten stornieren können.

Die Anzahl der Posten, die sich aus einer Datumskomprimierung ergeben, hängt davon ab, wie viele Filter Sie festlegen, welche Felder kombiniert werden und wie lang der von Ihnen gewählte Zeitraum ist. Es gibt immer mindestens einen Posten.

> [!WARNING]
> Die Datumskomprimierung löscht Posten. Daher sollten Sie immer eine Datensicherung der Datenbank durchführen, bevor Sie die Stapelverarbeitung ausführen.

### So führen Sie eine Datumskomprimierung aus

1. Wählen Sie das Symbol ![Suche nach Seite oder Bericht](media/ui-search/search_small.png "Symbol für „Suche nach Seite oder Bericht“") aus, geben Sie **Datenverwaltung** ein und wählen Sie dann den entsprechenden Link aus.
2. Führen Sie einen der folgenden Schritte aus:
    * Um eine Anleitung zum Festlegen der Datumskomprimierung für eine oder mehrere Arten von Daten zu verwenden, wählen Sie **Datenverwaltungsanleitung** aus.
    * Um die Komprimierung für einen einzelnen Datentyp festzulegen, wählen Sie **Datenkomprimierung**, **Posten komprimieren** und dann die zu komprimierenden Daten aus.

   > [!NOTE]
   > Sie können nur Daten komprimieren, die älter als fünf Jahre sind. Wenn Sie Daten komprimieren möchten, die weniger als fünf Jahre alt sind, wenden Sie sich an Ihren Microsoft-Partner. Sie müssen das `OnSetMinimumNumberOfYearsToKeep`-Ereignis in der „Datumskomprimierung“-codeunit verwenden, um den Schwellenwert festzulegen.


## Siehe auch

[Verwaltung](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
