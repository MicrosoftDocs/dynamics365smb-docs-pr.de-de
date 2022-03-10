---
title: Verwalten von Speicher durch das Löschen von Dokumenten oder Datenkomprimierung
description: Erfahren Sie, wie Sie mit sich ansammelnden historischen Belegen umgehen (und die Menge der in einer Datenbank gespeicherten Daten reduzieren), indem Sie sie löschen oder komprimieren.
author: edupont04
ms.topic: conceptual
ms.search.form: 107, 9040
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: a5c79da88ec49f6d9ff763b6712b0777158d2805
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147908"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Verwalten von Speicher durch das Löschen von Dokumenten oder Datenkomprimierung

Ein Benutzer mit einer zentralen Rolle, z. B. der Anwendungsadministrator, muss sich regelmäßig um die angesammelten historischen Belege kümmern, indem er diese löscht oder komprimiert.  

> [!TIP]
> Informationen zu anderen Möglichkeiten zum Reduzieren der in einer Datenbank gespeicherten Datenmenge finden Sie unter [Reduzieren von in Business Central-Datenbanken gespeicherten Daten](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) in unserer Entwickler- und IT-Pro-Dokumentation.

## <a name="delete-documents"></a>Belege löschen

Es kann gelegentlich erforderlich sein, erledigte Einkaufsbestellungen zu löschen, die noch nicht gelöscht wurden. [!INCLUDE[prod_short](includes/prod_short.md)] überprüft, ob Sie die gelöschten Bestellungen vollständig fakturiert haben. Sie können keine Bestellungen löschen, die noch nicht vollständig geliefert und fakturiert wurden.  

Reklamationen werden üblicherweise gelöscht, nachdem sie fakturiert wurden. Wenn Sie eine Rechnung buchen, wird sie auf die Seite **Geb. Einkaufsgutschrift** übertragen. Ist das Kontrollkästchen **Rücklieferung bei Gutschrift** im Fenster **Kreditoren & Einkauf Einr.** aktiviert, wird sie auch auf die Seite **Gebuchte Rücklieferung** übertragen. Sie können die Belege mithilfe der Stapelverarbeitung **Erledigte Eink.-Rekl. löschen** löschen. Vor dem Löschen prüft die Stapelverarbeitung, ob die Einkaufsreklamationen vollständig geliefert und fakturiert wurden.  

Rahmenbestellungen werden nicht gelöscht, nachdem Sie alle zugehörigen Bestellungen verarbeitet und fakturiert haben. Sie können erledigte Rahmenbestellungen mit Hilfe der Stapelverarbeitung **Erledigte Rahmenbestellungen löschen** löschen.  

Verrechnete Serviceaufträge werden automatisch gelöscht, nachdem diese vollständig fakturiert wurden. Beim Buchen einer Rechnung wird ein entsprechender Posten auf der Seite **Gebuchte Servicerechnungen** erstellt. Der gebuchte Beleg kann auf der Seite **Gebuchte Servicerechnung** angezeigt werden.  

Serviceaufträge werden aber nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags nicht aus dem eigentlichen Serviceauftrag, sondern von der Seite **Servicerechnung** gebucht wurde. In diesem Fall müssen Sie fakturierte Aufträge, die nicht gelöscht wurden, manuell löschen. Dazu führen Sie die Stapelverarbeitung **Fakturierte Serviceaufträge löschen** aus.  

## <a name="compress-data-with-date-compression"></a>Daten komprimieren mit der Datumskomprimierung

Sie können Daten in [!INCLUDE [prod_short](includes/prod_short.md)] komprimieren, um Platz in der Datenbank zu sparen. In [!INCLUDE [prod_short](includes/prod_short.md)] Online können Sie damit sogar Geld sparen. Die Komprimierung basiert auf Daten und fasst mehrere alte Posten in einem neuen Posten zusammen. 

Sie können Einträge unter folgenden Bedingungen komprimieren:

* Sie stammen aus abgeschlossenen Geschäftsjahren
* Das Feld **Offen** ist auf **Nein** festgelegt. 
* Sie sind mindestens fünf Jahre alt. Wenn Sie Daten komprimieren möchten, die weniger als fünf Jahre alt sind, wenden Sie sich an Ihren Microsoft-Partner.

Beispielsweise können die Kreditorenposten von zurückliegenden Geschäftsjahren so komprimiert werden, dass nur noch ein Soll- und ein Habenposten pro Konto und Monat vorhanden ist. Der Betrag des neuen Postens ist die Summe aller komprimierten Posten. Das Datum, das zugewiesen wird, ist das Startdatum der Periode, die komprimiert wird, wie z. B. der erste Tag des Monats (wenn die Posten pro Monat komprimiert werden). Nach der Komprimierung können Sie immer noch die Bewegung auf jedem Konto im vergangenen Geschäftsjahr sehen.

Die Anzahl der Posten, die im Zuge der Datumskomprimierung erstellt werden, hängt von der Anzahl der festgelegten Filter, den kombinierten Feldern und der ausgewählten Periodenlänge ab. Es gibt immer mindestens einen Posten. Wenn die Stapelverarbeitung abgeschlossen ist, sehen Sie die Ergebnisse auf der Seite **Datumskompr.-Journal**.

Sie können die folgenden Arten von Daten mit Batchaufträgen komprimieren. Für jede Art von Daten gibt es einen Batchauftrag.

* Finance-Einträge – Sachkonto-Einträge, MwSt.-Posten, Sachkonto-Einträge, Sachkontenbudgets, Kreditor-Ledger-Einträge.
* Lager-Einträge 
* Ressourcen-Buchungen
* Element-Budgetbuchungen
* Sachkonto – Sachkonto-Ledger-Einträge, FA-Wartungs-Ledger-Einträge, FA-Versicherungs-Ledger-Einträge.

Wenn Sie Kriterien für die Komprimierung definieren, können Sie die Optionen unter **Feldinhalte beibehalten** verwenden, um den Inhalt bestimmter Felder beizubehalten. Welche Felder zur Verfügung stehen, hängt von den Daten ab, die Sie komprimieren.

> [!NOTE]
> Bevor Sie die Datenkomprimierung ausführen können, müssen Ihre Analyseansichten auf dem neuesten Stand sein. Weitere Informationen finden Sie unter [So aktualisieren Sie eine Analyseansicht](bi-how-analyze-data-dimension.md#to-update-an-analysis-view).

Nach der Komprimierung werden die Inhalte der folgenden Felder in jedem Fall beibehalten: **Buchungsdatum**, **Kreditorennr.**, **Belegart**, **Währungscode**, **Buchungsgruppe**, **Betrag**, **Restbetrag**, **Ursprungsbetrag (MW)**, **Restbetrag (MW)**, **Betrag (MW)**, **Einkauf (MW)**, **Rechnungsrabatt (MW)**, **Skonto gewährt (MW)** und **Skonto möglich**.

## <a name="posting-compressed-entries"></a>Veröffentlichen komprimierter Einträge
Komprimierte Einträge werden etwas anders gebucht als Standardbuchungen. Dies dient dazu, die Anzahl der durch die Datumskomprimierung erstellten neuen Sachposten zu verringern. Dies ist besonders wichtig, wenn Sie Informationen wie Abmessungen und Belegnummern aufbewahren. Durch die Datumskomprimierung werden neue Einträge wie folgt erstellt:
* Auf der Seite **Sachposten** werden neue Einträge mit neuen Eintragsnummern für die komprimierten Einträge erstellt. Das Feld **Beschreibung** enthält **Datum komprimiert**, damit die komprimierten Einträge leicht zu identifizieren sind. 
* Auf Hauptbuchseiten wie der Seite **Debitorenposten** werden ein oder mehrere Einträge mit neuen Eintragsnummern erstellt. 

Der Buchungsprozess erzeugt Lücken in der Nummernreihe für Einträge auf der Seite **Sachposten**. Diese Nummern werden nur den Einträgen auf den Hauptbuchseiten zugewiesen. Der den Einträgen zugewiesene Nummernkreis ist auf der **Sachkontenregisterseite** in den Feldern **Von Lfd. Nr.** und **Bis Lfd. Nr.** Felder. 

> [!NOTE]
> Nachdem Sie die Datumskomprimierung ausgeführt haben, werden alle Konten im Hauptbuch gesperrt. Beispielsweise können Sie während des Zeitraums, für den Daten komprimiert werden, keine Lieferanten- oder Bankbucheinträge für Konten aufheben.

Die Anzahl der Posten, die im Zuge der Datumskomprimierung erstellt werden, hängt von der Anzahl der festgelegten Filter, den kombinierten Feldern und der ausgewählten Periodenlänge ab. Es gibt immer mindestens einen Posten. 

> [!WARNING]
> Die Datumskomprimierung löscht Posten. Daher sollten Sie immer eine Datensicherung der Datenbank durchführen, bevor Sie die Stapelverarbeitung ausführen.

### <a name="to-run-a-date-compression"></a>So führen Sie eine Datumskomprimierung aus
1. Wählen Sie das Symbol ![Suche nach Seite oder Bericht](media/ui-search/search_small.png "Nach dem Symbol für „Seite“ oder „Bericht“ suchen"). Geben Sie **Datenverwaltung** ein, und wählen Sie dann den entsprechenden Link.
2. Führen Sie einen der folgenden Schritte aus:
    * Um eine Anleitung zur unterstützten Einrichtung zu verwenden, um die Datumskomprimierung für einen oder mehrere Datentypen festzulegen, wählen Sie **Datenverwaltung Anleitung**.
    * Um die Komprimierung für einen einzelnen Datentyp festzulegen, wählen Sie **Datenkomprimierung**, **Einträge komprimieren** und wählen dann die zu komprimierenden Daten.

   > [!NOTE]
   > Sie können nur Daten komprimieren, die älter als fünf Jahre sind. Wenn Sie Daten komprimieren möchten, die weniger als fünf Jahre alt sind, wenden Sie sich an Ihren Microsoft-Partner.

## <a name="see-also"></a>Weitere Informationen

[Verwaltung](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]