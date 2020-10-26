---
title: Verwalten von Speicher durch das Löschen von Dokumenten oder Datenkomprimierung
description: Erfahren Sie, wie Sie Ihre historischen Daten durch Komprimieren oder Löschen von Posten beibehalten können.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 05e5078253d63fac61039d26cc0d700e96c7d21a
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911280"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Verwalten von Speicher durch das Löschen von Dokumenten oder Datenkomprimierung

Ein Benutzer mit einer zentralen Rolle, z. B. der Anwendungsadministrator, muss sich regelmäßig um die angesammelten historischen Belege kümmern, indem er diese löscht oder komprimiert.  

## <a name="delete-documents"></a>Belege löschen

Es kann gelegentlich erforderlich sein, erledigte Einkaufsbestellungen zu löschen, die noch nicht gelöscht wurden. [!INCLUDE[d365fin](includes/d365fin_md.md)] überprüft, ob Sie die gelöschten Bestellungen vollständig fakturiert haben. Sie können keine Bestellungen löschen, die noch nicht vollständig geliefert und fakturiert wurden.  

Reklamationen werden üblicherweise gelöscht, nachdem sie fakturiert wurden. Wenn Sie eine Rechnung buchen, wird sie auf die Seite **Geb. Einkaufsgutschrift** übertragen. Ist das Kontrollkästchen **Rücklieferung bei Gutschrift** im Fenster **Kreditoren & Einkauf Einr.** aktiviert, wird sie auch auf die Seite **Gebuchte Rücklieferung** übertragen. Sie können die Belege mithilfe der Stapelverarbeitung **Erledigte Eink.-Rekl. löschen** löschen. Vor dem Löschen prüft die Stapelverarbeitung, ob die Einkaufsreklamationen vollständig geliefert und fakturiert wurden.  

Rahmenbestellungen werden nicht gelöscht, nachdem Sie alle zugehörigen Bestellungen verarbeitet und fakturiert haben. Sie können erledigte Rahmenbestellungen mit Hilfe der Stapelverarbeitung **Erledigte Rahmenbestellungen löschen** löschen.  

Verrechnete Serviceaufträge werden automatisch gelöscht, nachdem diese vollständig fakturiert wurden. Beim Buchen einer Rechnung wird ein entsprechender Posten auf der Seite **Gebuchte Servicerechnungen** erstellt. Der gebuchte Beleg kann auf der Seite **Gebuchte Servicerechnung** angezeigt werden.  

Serviceaufträge werden aber nicht automatisch gelöscht, wenn die Gesamtmenge des Auftrags nicht aus dem eigentlichen Serviceauftrag, sondern von der Seite **Servicerechnung** gebucht wurde. In diesem Fall müssen Sie fakturierte Aufträge, die nicht gelöscht wurden, manuell löschen. Dazu führen Sie die Stapelverarbeitung **Fakturierte Serviceaufträge löschen** aus.  

## <a name="compress-data-with-date-compression"></a>Daten komprimieren mit der Datumskomprimierung

Sie können Daten in [!INCLUDE [prodshort](includes/prodshort.md)] komprimieren, um Platz in der Datenbank zu sparen. In [!INCLUDE [prodshort](includes/prodshort.md)] Online können Sie damit sogar Geld sparen. Die Komprimierung basiert auf Daten und fasst mehrere alte Posten in einem neuen Posten zusammen. Sie können ausschließlich Posten von abgeschlossenen Geschäftsjahren und außerdem nur solche Kreditorenposten komprimieren, bei denen im Feld **Offen** die Option *Nein* steht.  

Beispielsweise können die Kreditorenposten von zurückliegenden Geschäftsjahren so komprimiert werden, dass nur noch ein Soll- und ein Habenposten pro Konto und Monat vorhanden ist. Der Betrag des neuen Postens ist die Summe aller komprimierten Posten. Das Datum, das zugewiesen wird, ist das Startdatum der Periode, die komprimiert wird, wie z. B. der erste Tag des Monats (wenn die Posten pro Monat komprimiert werden). Nach der Komprimierung können Sie immer noch die Bewegung auf jedem Konto im vergangenen Geschäftsjahr sehen.

Die Anzahl der Posten, die im Zuge der Datumskomprimierung erstellt werden, hängt von der Anzahl der festgelegten Filter, den kombinierten Feldern und der ausgewählten Periodenlänge ab. Es gibt immer mindestens einen Posten. Wenn die Stapelverarbeitung abgeschlossen ist, sehen Sie die Ergebnisse auf der Seite **Datumskompr.-Journal** .

Sie können die folgenden Datentypen in [!INCLUDE [prodshort](includes/prodshort.md)] mithilfe von Stapelverarbeitungsaufträgen komprimieren.

* Bankposten

  Nach der Komprimierung mit der Funktion **Feldinhalt behalten** können Sie die Inhalte der Felder **Belegnr., Unser Kontaktcode** , **Globaler Dimensionscode 1** und **Globaler Dimensionscode 2** beibehalten.
* Kreditorenposten

  Nach der Komprimierung werden die Inhalte der folgenden Felder in jedem Fall beibehalten: **Buchungsdatum** , **Kreditorennr.** , **Belegart** , **Währungscode** , **Buchungsgruppe** , **Betrag** , **Restbetrag** , **Ursprungsbetrag (MW)** , **Restbetrag (MW)** , **Betrag (MW)** , **Einkauf (MW)** , **Rechnungsrabatt (MW)** , **Skonto gewährt (MW)** und **Skonto möglich** .

  Mit der Funktion **Feldinhalt behalten** können Sie auch den Inhalt folgender zusätzlicher Felder erhalten: **Belegnr.** , **Eink. von Kred.-Nr.** , **Einkäufercode** , **Globaler Dimensionscode 1** und **Globaler Dimensionscode 2** .

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
|Periodenlänge |Wählen Sie die Länge der Periode, innerhalb der Posten zusammengefasst werden sollen. Wählen Sie das Feld, um die Optionen anzuzeigen. Wenn Sie die Periodenlänge *Quartal* , *Monat* oder *Woche* ausgewählt haben, werden nur Posten mit einer gemeinsamen Buchhaltungsperiode komprimiert.|
|Feldinhalt behalten     |Setzen Sie Häkchen in die Felder, wenn Sie die Inhalte bestimmter Felder behalten möchten, obwohl die Posten komprimiert werden. Je mehr Felder Sie auswählen, desto detaillierter werden die komprimierten Posten. Wenn Sie keines dieser Felder auswählen, erzeugt die Stapelverarbeitung einen Posten pro Tag, Woche oder anderer Periode, abhängig von der Periode, die Sie im Feld **Periodenlänge** ausgewählt haben. |

## <a name="see-also"></a>Siehe auch

[Verwaltung](admin-setup-and-administration.md)  
