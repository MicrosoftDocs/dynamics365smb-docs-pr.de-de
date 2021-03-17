---
title: Verwalten von Speicher durch das Löschen von Dokumenten oder Datenkomprimierung
description: Erfahren Sie, wie Sie Ihre historischen Daten durch Komprimieren oder Löschen von Posten beibehalten können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b17e4df039ef713bf5c0048d258aefd175157ba4
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493047"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Verwalten von Speicher durch das Löschen von Dokumenten oder Datenkomprimierung

Ein Benutzer mit einer zentralen Rolle, z. B. der Anwendungsadministrator, muss sich regelmäßig um die angesammelten historischen Belege kümmern, indem er diese löscht oder komprimiert.  

> [!TIP]
> Informationen zu anderen Möglichkeiten zum Reduzieren der in einer Datenbank gespeicherten Datenmenge finden Sie unter [Reduzieren von in Business Central-Datenbanken gespeicherten Daten](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) in der Entwickler- und IT-Pro-Hilfe.

## <a name="delete-documents"></a>Belege löschen

Es kann gelegentlich erforderlich sein, erledigte Einkaufsbestellungen zu löschen, die noch nicht gelöscht wurden. [!INCLUDE[prod_short](includes/prod_short.md)] überprüft, ob Sie die gelöschten Bestellungen vollständig fakturiert haben. Sie können keine Bestellungen löschen, die noch nicht vollständig geliefert und fakturiert wurden.  

Reklamationen werden üblicherweise gelöscht, nachdem sie fakturiert wurden. Wenn Sie eine Rechnung buchen, wird sie auf die Seite **Geb. Einkaufsgutschrift** übertragen. Ist das Kontrollkästchen **Rücklieferung bei Gutschrift** im Fenster **Kreditoren & Einkauf Einr.** aktiviert, wird sie auch auf die Seite **Gebuchte Rücklieferung** übertragen. Sie können die Belege mithilfe der Stapelverarbeitung **Erledigte Eink.-Rekl. löschen** löschen. Vor dem Löschen prüft die Stapelverarbeitung, ob die Einkaufsreklamationen vollständig geliefert und fakturiert wurden.  

Rahmenbestellungen werden nicht gelöscht, nachdem Sie alle zugehörigen Bestellungen verarbeitet und fakturiert haben. Sie können erledigte Rahmenbestellungen mit Hilfe der Stapelverarbeitung **Erledigte Rahmenbestellungen löschen** löschen.  

Verrechnete Serviceaufträge werden automatisch gelöscht, nachdem diese vollständig fakturiert wurden. Beim Buchen einer Rechnung wird ein entsprechender Posten auf der Seite **Gebuchte Servicerechnungen** erstellt. Der gebuchte Beleg kann auf der Seite **Gebuchte Servicerechnung** angezeigt werden.  

Serviceaufträge werden aber nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags nicht aus dem eigentlichen Serviceauftrag, sondern von der Seite **Servicerechnung** gebucht wurde. In diesem Fall müssen Sie fakturierte Aufträge, die nicht gelöscht wurden, manuell löschen. Dazu führen Sie die Stapelverarbeitung **Fakturierte Serviceaufträge löschen** aus.  

## <a name="compress-data-with-date-compression"></a>Daten komprimieren mit der Datumskomprimierung

Sie können Daten in [!INCLUDE [prod_short](includes/prod_short.md)] komprimieren, um Platz in der Datenbank zu sparen. In [!INCLUDE [prod_short](includes/prod_short.md)] Online können Sie damit sogar Geld sparen. Die Komprimierung basiert auf Daten und fasst mehrere alte Posten in einem neuen Posten zusammen. Sie können ausschließlich Posten von abgeschlossenen Geschäftsjahren und außerdem nur solche Kreditorenposten komprimieren, bei denen im Feld **Offen** die Option *Nein* steht.  

Beispielsweise können die Kreditorenposten von zurückliegenden Geschäftsjahren so komprimiert werden, dass nur noch ein Soll- und ein Habenposten pro Konto und Monat vorhanden ist. Der Betrag des neuen Postens ist die Summe aller komprimierten Posten. Das Datum, das zugewiesen wird, ist das Startdatum der Periode, die komprimiert wird, wie z. B. der erste Tag des Monats (wenn die Posten pro Monat komprimiert werden). Nach der Komprimierung können Sie immer noch die Bewegung auf jedem Konto im vergangenen Geschäftsjahr sehen.

Die Anzahl der Posten, die im Zuge der Datumskomprimierung erstellt werden, hängt von der Anzahl der festgelegten Filter, den kombinierten Feldern und der ausgewählten Periodenlänge ab. Es gibt immer mindestens einen Posten. Wenn die Stapelverarbeitung abgeschlossen ist, sehen Sie die Ergebnisse auf der Seite **Datumskompr.-Journal**.

Sie können die folgenden Datentypen in [!INCLUDE [prod_short](includes/prod_short.md)] mithilfe von Stapelverarbeitungsaufträgen komprimieren.

* Bankposten

  Nach der Komprimierung mit der Funktion **Feldinhalt behalten** können Sie die Inhalte der Felder **Belegnr., Unser Kontaktcode**, **Globaler Dimensionscode 1** und **Globaler Dimensionscode 2** beibehalten.
* Kreditorenposten

> [!NOTE]
> Komprimierte Einträge für untergeordnete Kunden-, Lieferanten-, Bank- und FA-Konten werden geringfügig anders als die Standardbuchung gebucht. Dies dient dazu, die Anzahl der durch die Datumskomprimierung erstellten neuen Sachposten zu verringern. Dies ist besonders wichtig, wenn Sie Informationen wie Abmessungen und Belegnummern aufbewahren. Durch die Datumskomprimierung werden neue Einträge wie folgt erstellt:
>* Auf der Seite **Sachposten** werden neue Einträge mit neuen Eintragsnummern für die komprimierten Einträge erstellt. Das Feld **Beschreibung** enthält **Datum komprimiert**, damit die komprimierten Einträge leicht zu identifizieren sind. 
>* Auf Hauptbuchseiten wie der Seite **Debitorenposten** werden ein oder mehrere Einträge mit neuen Eintragsnummern erstellt. 
> Der Buchungsprozess erzeugt Lücken in der Nummernreihe für Einträge auf der Seite **Sachposten**. Diese Nummern werden nur den Einträgen auf den Hauptbuchseiten zugewiesen. Der den Einträgen zugewiesene Nummernkreis ist auf der **Sachkontenregisterseite** in den Feldern **Von Lfd. Nr.** und **Bis Lfd. Nr.** Felder. 

Nach der Komprimierung werden die Inhalte der folgenden Felder in jedem Fall beibehalten: **Buchungsdatum**, **Kreditorennr.**, **Belegart**, **Währungscode**, **Buchungsgruppe**, **Betrag**, **Restbetrag**, **Ursprungsbetrag (MW)**, **Restbetrag (MW)**, **Betrag (MW)**, **Einkauf (MW)**, **Rechnungsrabatt (MW)**, **Skonto gewährt (MW)** und **Skonto möglich**.

  Mit der Funktion **Feldinhalt behalten** können Sie auch den Inhalt folgender zusätzlicher Felder erhalten: **Belegnr.**, **Eink. von Kred.-Nr.**, **Einkäufercode**, **Globaler Dimensionscode 1** und **Globaler Dimensionscode 2**.

> [!NOTE]
> Nachdem Sie die Datumskomprimierung ausgeführt haben, werden alle Konten im Hauptbuch gesperrt. Beispielsweise können Sie während des Zeitraums, für den Daten komprimiert werden, keine Lieferanten- oder Bankbucheinträge für Konten aufheben.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

Die Anzahl der Posten, die von der Stapelverarbeitung zur Datumskomprimierung erstellt werden, hängt von der Anzahl der festgelegten Filter, den kombinierten Feldern und der ausgewählten Periodenlänge ab. Es gibt immer mindestens einen Posten. 

> [!WARNING]
> Die Datumskomprimierung löscht Posten. Daher sollten Sie immer eine Datensicherung der Datenbank durchführen, bevor Sie die Stapelverarbeitung ausführen.

In der folgenden Tabelle sind die Felder im Inforegister **Optionen** aufgeführt, die in allen Stapelverarbeitungsaufträgen zur Verfügung stehen. Der Bereich **Feldinhalt behalten** enthält zusätzliche Felder, die oben beschrieben werden.

|Feld  |Beschreibung  |
|-------|-------------|
|Startdatum     |Geben Sie das erste Datum ein, das in der Datumskomprimierung berücksichtigt werden soll. Die Komprimierung erfasst alle Posten ab diesem Datum bis zum Enddatum.|
|Enddatum     |Geben Sie das letzte Datum ein, das in der Datumskomprimierung enthalten sein soll. Die Komprimierung erfasst alle Posten vom Startdatum bis zu diesem Datum.|
|Periodenlänge |Wählen Sie die Länge der Periode, innerhalb der Posten zusammengefasst werden sollen. Wählen Sie das Feld, um die Optionen anzuzeigen. Wenn Sie die Periodenlänge *Quartal*, *Monat* oder *Woche* ausgewählt haben, werden nur Posten mit einer gemeinsamen Buchhaltungsperiode komprimiert.|
|Feldinhalt behalten     |Setzen Sie Häkchen in die Felder, wenn Sie die Inhalte bestimmter Felder behalten möchten, obwohl die Posten komprimiert werden. Je mehr Felder Sie auswählen, desto detaillierter werden die komprimierten Posten. Wenn Sie keines dieser Felder auswählen, erzeugt die Stapelverarbeitung einen Posten pro Tag, Woche oder anderer Periode, abhängig von der Periode, die Sie im Feld **Periodenlänge** ausgewählt haben. |

## <a name="see-also"></a>Siehe auch

[Verwaltung](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]