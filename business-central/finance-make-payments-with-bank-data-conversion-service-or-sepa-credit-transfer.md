---
title: Zahlungen mit AMC Banking (USA) oder per SEPA-Überweisung (EU) vornehmen
description: Verwalten Sie Zahlungen an Ihre Kreditoren, indem Sie eine Datei zusammen mit den Zahlungsinformationen von den Buch.-Blattzeilen exportieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 210dbfd3450d4cc703f73fc2cd078b0155c599da
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391849"
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder per SEPA-Überweisung vornehmen

Auf der Seite **Zahlungsjournal** können Sie Zahlungen an Ihre Kreditoren verarbeiten, indem Sie eine Datei zusammen mit den Zahlungsinformationen von den Buch.-Blattzeilen exportieren. Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten. [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt das Abbuchungsformat SEPA, aber in Ihrem Land/die Region, sind möglicherweise andere Formate für den elektronischen Zahlungsverkehr verfügbar.

> [!NOTE]
> In der generischen Version von [!INCLUDE[prod_short](includes/prod_short.md)]  wird ein globaler Diensteanbieter eingerichtet und verbunden, der Bankdaten in das Dateiformat konvertiert, das Ihre Bank verlangt. In den nordamerikanischen Versionen kann derselbe Service verwendet werden, um Zahlungsdateien als elektronischer Geldtransfer (EFT) zu buchen, mit einem leicht anderen Prozess. Siehe Schritt 6 unter [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Um SEPA-Banküberweisungen zu aktivieren, müssen Sie zunächst ein Bankkonto, einen Kreditor und das Fibu Buch.-Blatt anlegen, auf dem das Zahlungsausgangs Buch.-Blatt basiert. Sie bereiten dann Zahlungen an Kreditoren vor, indem Sie die Seite **Zahlungsjournal** automatisch mit fälligen Zahlungen mit angegebenen Buchungsdaten ausfüllen.  

> [!NOTE]  
> Wenn Sie geprüft haben, ob die Zahlungen erfolgreich von der Bank verarbeitet wurden, können Sie mit der Buchung der Zahlungsausgangs Buch.-Blattzeilen fortfahren.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>Einrichten der AMC Banking 365 Fundamentals-Erweiterung

Aktivieren Sie die AMC Banking 365 Fundamentals-Erweiterung, um jede Bankauszugsdatei in ein Format zu konvertieren, das Sie importieren können, oder um Ihre exportierten Zahlungsdateien in das Format zu konvertieren, das Ihre Bank benötigt. Weitere Informationen finden Sie [Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>Einrichten von SEPA-Kreditübertragung

Auf der Seites dem Fenster **Zahlungsjournal** können Sie Zahlungen in eine Datei zum Upload zu Ihrer elektronischen Bank für die Verarbeitung der zugehörigen Geldüberweisungen exportieren. [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt das Abbuchungsformat SEPA, aber in Ihrem Land/die Region, sind möglicherweise andere Formate für den elektronischen Zahlungsverkehr verfügbar.  

Um das Exportieren von Bankdateiformaten zu aktivieren, die nicht durch die allgemeine oder lokale Version von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt werden, können Sie eine Datenaustauschdefinition einrichten, indem Sie das Datenaustauschframework verwenden. Für weitere Informationen, siehe [Einrichten der Datenaustauschdefinition](across-how-to-set-up-data-exchange-definitions.md).  

Bevor Sie Zahlungen elektronisch durch den Export von Zahlungszeilen im SEPA-Banküberweisungsformat verarbeiten können, müssen Sie die folgenden Einrichtungsschritte ausführen:  

* Richten Sie das Bankkonto ein, um mit dem SEPA-Banküberweisungsformat umzugehen  
* Einrichten von Lieferantenkarten, um Zahlungen zu verarbeiten, indem Dateien im SEPA-Banküberweisungsformat exportiert werden.  
* Richten Sie das zugehörige Fibu Buch.-Blatt ein, um den Zahlungsexport auf der **Zahlungsjournal**-Seite zu aktivieren.  
* Verbindung der Datenaustauschdefinition für eine oder mehrere Zahlungsarten mit den relevanten Zahlungsverfahren  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Ein Bankkonto für SEPA-Banküberweisung einrichten

1. Geben Sie im Feld **Suchen** **Bankkonten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die Karte des Bankkontos, von dem Sie Zahlungsdateien im SEPA-Banküberweisungsformat exportieren.  
3. Wählen Sie im Inforegister **Umlagerung** im Feld **Format Zahlungsexport** die Option **SEPACT** aus.  
4. Wählen Sie auf dem Inforegister **Allgemein** im Feld **Kreditübertragung Nachr.-IDs** eine Nummernserie aus, aus der den SEPA-Banküberweisungsposten Nummern zugewiesen werden.  
5. Vergewissern Sie sich, dass das Feld **IBAN** ausgefüllt ist.  

    > [!NOTE]  
    > Das Feld **Währungscode** muss auf **EUR** festgelegt werden, da SEPA-Banküberweisungen nur in der EURO-Währung gebucht werden können.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Eine Kreditorenkarte für SEPA-Banküberweisung einrichten

1. Geben Sie im Feld **Suchen** **Kreditoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie die Karte des Debitors, den Sie elektronisch bezahlen, indem Sie Zahlungsdateien im SEPA-Banküberweisungsformat exportieren.  
3. Wählen Sie im Inforegister **Zahlung** im Feld **Zahlungsformencode** die Funktion **BANK** aus.  
4. Wählen Sie im **Bevorzugtes Bankkonto**-Feld die Bank aus, an die das Geld übertragen wird, wenn es durch Ihre elektronische Bank verarbeitet wird.  

     Der Wert im Feld **Bevorzugtes Bankkonto** wird aus dem Feld **Bankkonto Empfänger** auf der Seite **Zahlungsausgangs Buch.-Blatt** kopiert.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Das Zahlungsausgangs Buch.-Blatt für den Export von Zahlungsdateien festlegen

1. Geben Sie im Feld **Suchen** einen Wert für **Zahlungsausgangs Buch.-Blatt** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie das Zahlungsausgangs Buch.-Blatt, das Sie verwenden möchten, um Zahlungen zu verarbeiten, indem Sie Dateien im SEPA-Banküberweisungsformat zu exportieren.  
3. Wählen Sie im Feld **Stapelname** die\-Dropdownschaltfläche aus.  
4. Wählen Sie auf der Seite **Buch.-Blattnamen** die Aktion **Liste bearbeiten**.  
5. In der Zeile für das Zahlungsausgangs Buch.-Blatt, das Sie verwenden möchten, um Zahlungen zu exportieren, wählen Sie das Kontrollkästchen **Zahlungsexport zulassen** aus.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Verbindung der Datenaustauschdefinition für eine oder mehrere Zahlungsarten mit den relevanten Zahlungsverfahren

1. Geben Sie im Feld **Suchen** einen Wert für **Zahlungsformen** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Auf der **Zahlungsformen**-Seite wählen Sie die Zahlungsform, die verwendet wird, um Zahlungen zu exportieren, und wählen Sie dann das Feld **Definition der Zahlungsexportzeile** aus.  
3. Auf der Seite **Pmt. Export-Zeilen-Definitionen** wählen Sie den Code, den Sie im Feld **Code** im Inforegister **Zeilendefinitionen** in Schritt 4 im Bereich „Formatierung aus Zeilen und Spalten von in der Datei beschreiben“ im Vorgang [Atenaustauschdefinition einrichten](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="preparing-the-payment-journal"></a>Zahlungsausgangs Buch.-Blatt vorbereiten.

Füllen Sie das Zahlungsausgangs Buch.-Blatt mit Zeilen für fällige Zahlungen an Kreditoren, mit der Option, Buchungsdaten basierend auf dem Fälligkeitsdatum der zugehörigen Einkaufsbelege einzufügen. Weitere Informationen finden Sie unter [Kreditoren verwalten](payables-manage-payables.md).

## <a name="exporting-payments-to-a-bank-file"></a>Zahlungen in eine Bankdatei exportieren

Wenn Sie bereit sind, Zahlungen oder Rückvergütungen an Ihre Mitarbeiter zu machen, können Sie dies auf der Seite **Zahlung Buch.-Blatt** vorzunehmen. Sie können eine Datei mit den Zahlungsinformationen auf den Buch.-Blattzeilen exportieren. Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten.

In der generischen Version von [!INCLUDE[prod_short](includes/prod_short.md)] ist die AMC Banking 365 Fundamentals-Erweiterung verfügbar. In den nordamerikanischen Versionen kann die gleiche Erweiterung verwendet werden, um Zahlungsdateien wie beim elektronischen Zahlungsverkehr (EFT) zu versenden, allerdings mit einem etwas anderen Prozess. Siehe Schritt 6 unter [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Bevor Sie Zahlungsdateien aus dem Zahlungsausgangs Buch.-Blatt exportieren können, müssen Sie das elektronische Format für das betreffende Bankkonto angeben und die AMC Banking 365 Fundamentals-Erweiterung aktivieren. Weitere Informationen finden Sie unter [Bankkonten einrichten](bank-how-setup-bank-accounts.md) und [Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md). Darüber hinaus müssen Sie das Kontrollkästchen **Zahlungsexport erlauben** auf der Seite **Fibu Buch.-Blattnamen** auswählen. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  

Sie verwenden die Seite **Kreditübertragungsjournale**, um die Zahlungsdateien anzuzeigen, die aus dem Zahlungsausgangs Buch.-Blatt exportiert wurden. Von dieser Seite aus können Sie Zahlungsdateien auch erneut exportieren (im Fall von technischen Fehlern oder Dateiänderungen). Beachten Sie, dass die exportierten EFT-Dateien nicht auf dieser Seite angezeigt werden und nicht wieder exportiert werden können.  

### <a name="to-export-payments-to-a-bank-file"></a>Zahlungen in eine Bankdatei exportieren

Nachfolgend wird erläutert, wie Sie einen Kreditor mit Schecks bezahlen. Die Schritte sind ähnlich, wie wenn sie Ihren Debitoren Scheck zurückerstatten.

1. Wählen Sie die ![Glühbirne, die das Symbol Tell Me öffnet](media/ui-search/search_small.png "Was möchten Sie tun?"), geben Sie **Zahlungsjournale** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Zalungszeilen ein. Weitere Informationen finden Sie unter [Zahlungen und Rückerstattungen aufzeichnen](payables-how-post-payments-refunds.md)

    > [!NOTE]
    > Wenn Sie EFT verwenden, müssen Sie entweder **Elektronische Zahlung** oder **Elektronische Zahlung-IAT** im Feld **Bankkontozahlungsart** auswählen. Verschiedene Dateiexportdienste und deren Formaten benötigen verschiedene Einrichtungswerte auf den Seiten **Bankkontokarte** und **Kreditor-Bankkontokarte**. Sie werden über die falschen oder fehlende Einrichtungswerte informiert, wenn Sie versuchen, die Datei zu exportieren.
    >
    > Die EFT-Funktion kann nur für Bankkonten in der Mandantenwährung verwendet werden. Es kann nicht mit einer Fremdwährung verwendet werden, die durch einen Wert im Feld **Währungscode** angezeigt ist. (Leerer Feldwert bedeutet Mandantenwährung.)

3. Wenn Sie alle Zahlungsausgangs Buch.-Blattzeilen abgeschlossen haben, wählen Sie die Aktion **Export** aus.
4. Füllen Sie auf der Seite **Elektronische Zahlungen exportieren** die Felder nach Bedarf aus.

    Vorhandene Fehlermeldungen werden in der **Fehler Zahlungsdatei**-Infobox angezeigt, in der Sie eine Fehlermeldung festlegen können, um ausführliche Informationen anzuzeigen. Sie müssen alle Fehler lösen, bevor die Zahlungsdatei exportiert werden kann.

    > [!TIP]  
    > Wenn Sie die AMC Banking 365 Fundamentals-Erweiterung verwenden, wird in einer häufigen Fehlermeldung angezeigt, dass der Bankkontoauszug nicht die Länge hat, die Ihre Bank benötigt. Um den Fehler zu vermeiden oder zu beheben, müssen Sie den Wert im **IBAN**-Feld auf der Seite **Bank** entfernen, und dann im **Kontokarten**-Feld eine Bankkontonummer in dem Format eingeben, das Ihre Bank erfordert.

5. Geben Sie auf der Seite **Speichern unter** den Speicherort an, zu dem die Datei exportiert werden soll, und wählen Sie dann **Speichern**.

    > [!NOTE]  
    > Wenn Sie EFT verwenden, speichern Sie die resultierenden Kreditorenüberweisungsformulare als Word-Dokument ab oder wählen Sie aus, diese direkt per E-Mail an den Kreditor zu senden. Die Zahlungen werden jetzt auf die Seite **EFT-Datei generieren** hinzugefügt, aus der Sie mehrere Zahlungsaufträge erstellen können, um Übertragungskosten zu sparen. Weitere Informationen finden Sie unter den folgenden Themen:
6. Auf der Seite **Zahlungsausgangs Buch.-Blatt** wählen Sie die Aktion **EFT-Datei generieren** aus.

    Auf der Seite **EFT-Datei generieren** werden alle Zahlungen, die für EFT eingerichtet werden, die Sie aus dem Zahlungsausgangs Buch.-Blatt für ein angegebenes Bankkonto exportiert aber noch nicht erstellt haben, im Inforegister **Zeilen** angezeigt.
7. Wählen Sie die **EFT-Datei generieren** Aktion aus, um eine Datei für alle EFT-Zahlungen zu exportieren.
8. Geben Sie auf der Seite **Speichern unter** den Speicherort an, zu dem die Datei exportiert werden soll, und wählen Sie dann **Speichern**.

Die Bankzahlungsdatei wird in den Speicherort exportiert, den Sie festlegen, und Sie können fortfahren, sie in das elektronische Bankkonto hochzuladen und die tatsächlichen Zahlungen zu leisten. Dann können Sie die Buch.-Blattzeilen der exportierten Zahlung buchen.

### <a name="to-plan-when-to-post-exported-payments"></a>Um die Buchung von exportierten Zahlungen zu planen

Wenn Sie keine Buch.-Blattzeile für eine exportierte Zahlung buchen möchten, weil Sie beispielsweise eine Bestätigung erwarten, dass die Transaktion von der Bank verarbeitet wurde, können Sie die Buch.-Blattzeile einfach löschen. Falls Sie später eine Buch.-Blattzeile, um den Restbetrag der gebuchten Rechnung zu bezahlen, zeigt das **Exportierter Betrag gesamt**-Feld, wie viel des Zahlungsbetrags bereits exportiert wurde. Detaillierte Informationen über die exportierte Summe können Sie auch finden, indem Sie die Schaltfläche **Posten im Kreditübertragungsjournal** auswählen, um Einzelheiten zu Dateien der exportierten Zahlung anzuzeigen.

Wenn Sie ein Vorgang folgen, bei dem Sie keine Zahlungen buchen bis Sie die Bestätigung haben, dass sie in der Bank verarbeitet wurden, können Sie dieses auf zwei Arten steuern.

* In einem Zahlungsausgangs-Buch.-Blatt mit vorgeschlagenen Zahlungszeilen, können Sie entweder nach der **In Zahlungsdatei exportiert**-Spalte oder nach **Exportierter Betrag gesamt** sortieren, und dann Zahlungsvorschläge für offene Rechnungen, für die bereits Zahlungen geleistet wurden und für die Sie keine Zahlungen leisten möchten, löschen.
* Auf der Seite **Zahlungsvorschläge für Kreditoren**, in dem Sie festlegen, welche Zahlungen in das Zahlungsausgangs Buch.-Blatt einzufügen sind, können Sie das Kontrollkästchen **Exportierte Zahlungen überspringen** aktivieren, wenn Sie keine Buch.-Blattzeilen für Zahlungen einfügen möchten, die bereits exportiert wurden.

Um Informationen über exportierte Zahlungen anzuzeigen, wählen Sie die Aktion **Zahlungs-Export-Verlauf**.

### <a name="to-re-export-payments-to-a-bank-file"></a>Um Zahlungen erneut in eine Bankdatei zu exportieren

Sie können Zahlungsdateien aus der **Kreditübertragungsjournale**-Seite exportieren. Bevor Sie Zahlungsausgangs Buch.-Blattzeilen löschen oder buchen, können Sie die Zahlungsdatei aus der **Zahlung Buch.-Blatt**-Seite auch erneut exportieren, indem Sie es einfach wieder exportieren. Wenn Sie ein Zahlungsausgangs-Buch.-Blatt gelöscht oder gebucht haben, nachdem Sie es exportiert haben, können Sie dieselbe Zahlungsdatei nur aus der **Kreditübertragungsjournale**-Seite erneut exportieren. Wählen Sie die Zeile für den Stapelauftrag für Gutschriftübertragungen aus, die Sie erneut exportieren möchten, und verwenden Sie dann die Aktion **Zahlungen erneut in Datei exportieren**.

> [!NOTE]  
> Beachten Sie, dass die exportierten EFT-Dateien nicht auf der Seite **Kreditübertragungsjournale** angezeigt werden und nicht wieder exportiert werden können.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Überweisungsjournale** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie einen Zahlungsexport, den Sie erneut exportieren möchten, und wählen die Aktion **Erneuter Zahlungsexport in Datei** aus.

## <a name="posting-the-payments"></a>Die Zahlungen buchen

Wenn die elektronische Zahlung erfolgreich von der Bank verarbeitet wird, buchen Sie die Zahlungen. Weitere Informationen finden Sie unter [Zahlungen durchführen](payables-make-payments.md).

## <a name="see-also"></a>Siehe auch

[Verwenden der AMC Banking 365 Fundamentals-Erweiterung](ui-extensions-amc-banking.md)  
[Verwalten von Verbindlichkeiten](payables-manage-payables.md)  
[Arbeiten mit allgemeinen Buch.-Blättern](ui-work-general-journals.md)  
[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]