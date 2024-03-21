---
title: Verwalten von Speicher durch das Löschen von Dokumenten oder Datenkomprimierung
description: 'Erfahren Sie, wie Sie mit sich ansammelnden historischen Belegen umgehen (und die Menge der in einer Datenbank gespeicherten Daten reduzieren), indem Sie sie löschen oder komprimieren.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 09/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Verwalten von Speicher durch das Löschen von Dokumenten oder Datenkomprimierung

Ein Benutzer mit einer zentralen Rolle, z. B. der Anwendungsadministrator, muss sich regelmäßig um die angesammelten historischen Belege kümmern, indem er diese löscht oder komprimiert.  

> [!TIP]
> Erfahren Sie mehr über andere Möglichkeiten, die Menge der in einer Datenbank gespeicherten Daten zu reduzieren. Lesen Sie dazu [Reduzierung der in Business Central Datenbanken gespeicherten Daten](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) in unserer Dokumentation für Entwickler und IT-Profis.

## Löschen von Belegen

In bestimmten Situationen kann es erforderlich sein, dass Sie fakturierte Bestellungen löschen müssen. Sie können sie jedoch erst löschen, wenn Sie die Artikel in den Bestellungen vollständig in Rechnung gestellt und erhalten haben. [!INCLUDE[prod_short](includes/prod_short.md)] hilft Ihnen, dies zu überprüfen.

Rücklieferungen werden normalerweise gelöscht, nachdem sie in Rechnung gestellt wurden. Wenn Sie eine Rechnung buchen, wird sie auf die Seite **Gebuchte Einkaufsgutschrift** übertragen. Wenn Sie das Kontrollkästchen **Gebuchte Rücklieferung bei Gutschrift** auf der Seite **Einkäufe & Einkauf Einr.** aktiviert haben, wird die Rechnung auf die Seite **Gebuchte Rücklieferung** übertragen. Sie können die Belege mithilfe der Stapelverarbeitung **Erledigte Eink.-Rekl. löschen** löschen. Vor dem Löschen prüft die Stapelverarbeitung, ob die Einkaufsreklamationen vollständig geliefert und fakturiert wurden.  

Erledigte Rahmenbestellungen werden nicht automatisch gelöscht, nachdem Sie alle zugehörigen Bestellungen verarbeitet und in Rechnung gestellt haben. Stattdessen können Sie sie mit dem Batchauftrag **Erledigte Rahmenbestellungen löschen** löschen.  

Fakturierte Serviceaufträge werden in der Regel automatisch gelöscht, nachdem sie vollständig in Rechnung gestellt wurden. Wenn eine Rechnung gebucht wird, wird ein entsprechender Eintrag erstellt, der dann auf der Seite **Gebuchte Servicerechnungen** eingesehen werden kann.  

Serviceaufträge werden jedoch nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags von der Seite **Gebuchte Servicerechnungen** und nicht vom Serviceauftrag selbst gebucht wurde. Sie müssen solche fakturierten Aufträge möglicherweise manuell löschen, indem Sie den Batchauftrag **Fakturierte Serviceaufträge löschen** ausführen.  

## Daten mit Datumskomprimierung komprimieren

Sie können Daten in [!INCLUDE [prod_short](includes/prod_short.md)] komprimieren, um Platz in der Datenbank zu sparen, was Ihnen in [!INCLUDE [prod_short](includes/prod_short.md)] online sogar Geld sparen kann. Die Komprimierung, die auf Daten und Funktionen basiert, fasst mehrere alte Einträge zu einem neuen Eintrag zusammen.

Sie können Einträge komprimieren, die alle der folgenden Bedingungen erfüllen:

* Sie stammen aus abgeschlossenen Geschäftsjahren.
* Das Feld **Öffnen** ist auf **Nein** festgelegt.
* Sie sind mindestens fünf Jahre alt. Wenn Sie Daten komprimieren möchten, die weniger als fünf Jahre alt sind, wenden Sie sich an Ihren Microsoft-Partner.

So können z.B. Kreditorenposten aus früheren Geschäftsjahren komprimiert werden, so dass es nur eine Gutschrift und eine Lastschrift pro Konto und Monat gibt. Der Betrag des neuen Postens ergibt sich aus der Summe aller komprimierten Posten. Das zugewiesene Datum ist das Startdatum für den komprimierten Zeitraum, z.B. der erste Tag des Monats (wenn die Buchungen nach Monaten komprimiert sind). Nach der Komprimierung können Sie immer noch die Nettoveränderung für jedes Konto im vorherigen Geschäftsjahr sehen.

Die Anzahl der Posten, die im Zuge der Datumskomprimierung erstellt werden, hängt von der Anzahl der festgelegten Filter, den kombinierten Feldern und der ausgewählten Periodenlänge ab. Es gibt immer mindestens einen Eintrag. Wenn der Batchauftrag beendet ist, sehen Sie das Ergebnis auf der Seite **Date Compr. Register** sehen.

Sie können mit Batchaufträgen die folgenden Datentypen komprimieren.

* Finance-Einträge - Hauptbuch-Einträge, Mehrwertsteuer-Einträge, Sachkonto-Einträge, Sachkontenbudgets, Debitorenbuch-Einträge und Kreditorenbuch-Einträge.
* Lager-Einträge
* Ressourcen-Buchungen
* Element-Budgetbuchungen
* Sachkonto-Buchungen für Anlagen (FA), FA-Wartungsbuch-Buchungen und FA-Versicherungsbuch-Buchungen.

Wenn Sie Kriterien für die Komprimierung festlegen, können Sie den Inhalt bestimmter Felder mit den Optionen unter **Feldinhalte beibehalten** beibehalten. Die verfügbaren Felder hängen von den Daten ab, die Sie komprimieren.

> [!NOTE]
> Bevor Sie die Datenkomprimierung ausführen können, müssen Ihre Analyseansichten aktuell sein. Mehr dazu erfahren Sie im Abschnitt [Aktualisieren einer Analyseansicht](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Nach der Komprimierung werden die Inhalte der folgenden Felder in jedem Fall beibehalten: **Buchungsdatum**, **Kreditorennr.**, **Belegart**, **Währungscode**, **Buchungsgruppe**, **Betrag**, **Restbetrag**, **Ursprungsbetrag (MW)**, **Restbetrag (MW)**, **Betrag (MW)**, **Einkauf (MW)**, **Rechnungsrabatt (MW)**, **Skonto gewährt (MW)** und **Skonto möglich**.

## Komprimierte Buchungen buchen

Komprimierte Einträge werden etwas anders gebucht als Standardbuchungen. Dies dient dazu, die Anzahl der durch die Datumskomprimierung erstellten neuen Sachposten zu verringern. Dies ist besonders wichtig, wenn Sie Informationen wie Abmessungen und Belegnummern aufbewahren. Durch die Datumskomprimierung werden neue Einträge wie folgt erstellt:

* Auf der Seite **Hauptbuchhaltungsposten** werden neue Einträge für die komprimierten Buchungen erstellt. Das Feld **Beschreibung** enthält **Datum komprimiert**, damit die komprimierten Einträge leicht zu identifizieren sind. 
* Auf Sachkonto-Seiten, wie z.B. der Seite **Kunden-Sachkonto-Einträge**, werden ein oder mehrere neue Einträge erstellt. 

Der Buchungsprozess erzeugt Lücken in der Nummernreihe für Einträge auf der Seite **Sachposten**. Diese Nummern werden nur den Einträgen auf den Hauptbuchseiten zugewiesen. Der den Einträgen zugeordnete Nummernkreis ist auf der Seite **Fibujournal** in den Feldern **Von Lfd. Nr.** und **Bis Lfd. Nr.** verfügbar. 

> [!NOTE]
> Nachdem Sie die Datumskomprimierung ausgeführt haben, werden alle Konten im Hauptbuch gesperrt. Das bedeutet, dass Sie z.B. keine Kreditoren- oder Bank-Sachkonto-Einträge für die von der Komprimierung betroffenen Konten stornieren können.

Die Anzahl der Einträge, die sich aus einer Datumsverdichtung ergeben, hängt davon ab, wie viele Filter Sie festlegen, welche Felder kombiniert werden und wie lang der von Ihnen gewählte Zeitraum ist. Es gibt immer mindestens einen Posten.

> [!WARNING]
> Die Datumskomprimierung löscht Posten. Daher sollten Sie immer eine Datensicherung der Datenbank durchführen, bevor Sie die Stapelverarbeitung ausführen.

### So führen Sie eine Datumskomprimierung aus

1. Wählen Sie das Symbol ![Suche nach Seite oder Bericht](media/ui-search/search_small.png "Suche nach dem Symbol für Seite oder Bericht"), geben Sie **Datenverwaltung** ein und wählen Sie dann den entsprechenden Link.
2. Führen Sie einen der folgenden Schritte aus:
    * Um eine Anleitung zum Festlegen der Datenkompression für eine oder mehrere Arten von Daten zu verwenden, wählen Sie **Datenverwaltungsanleitung**.
    * Um die Komprimierung für einen einzelnen Datentyp festzulegen, wählen Sie **Datenkomprimierung**, **Einträge komprimieren**, und wählen Sie dann die zu komprimierenden Daten.

   > [!NOTE]
   > Sie können nur Daten komprimieren, die älter als fünf Jahre sind. Wenn Sie Daten komprimieren möchten, die weniger als fünf Jahre alt sind, wenden Sie sich an Ihren Microsoft-Partner. Sie müssen das `OnSetMinimumNumberOfYearsToKeep`-Ereignis in der „Datumskomprimierung“-codeunit verwenden, um den Schwellenwert festzulegen.


## Siehe auch

[Verwaltung](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
