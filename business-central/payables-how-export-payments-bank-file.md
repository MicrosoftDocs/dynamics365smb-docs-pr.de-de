---
title: Zahlungen in eine elektronische Zahlungsdatei exportieren| Microsoft Docs
description: Um Kreditorenzahlungen zu leisten, aktivieren Sie einen Bankdaten-Konvertierungsdienst, exportieren eine Bankdatei und laden die Datei elektronischen an Ihre Bank hoch.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.openlocfilehash: 539aac89d2da6b2eb81da7f6df729cdb5bc15cb1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "926558"
---
# <a name="export-payments-to-a-bank-file"></a>Zahlungen in eine Bankdatei exportieren
Wenn Sie bereit sind, Zahlungen oder Rückvergütungen an Ihre Mitarbeiter zu machen, können Sie dies  auf der Seite **Zahlung Buch.-Blatt** vorzunehmen. Sie können eine Datei mit den Zahlungsinformationen auf den Buch.-Blattzeilen exportieren. Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten.

In der generischen Version von [!INCLUDE[d365fin](includes/d365fin_md.md)]  wird ein globaler Diensteanbieter eingerichtet und verbunden, der Bankdaten in das Dateiformat konvertiert, das Ihre Bank verlangt. In den nordamerikanischen Versionen kann derselbe Service verwendet werden, um Zahlungsdateien als elektronischer Geldtransfer (EFT) zu buchen, mit einem leicht anderen Prozess. Siehe Schritt 6 unter [Zahlungen in eine Bankdatei exportieren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).    

> [!NOTE]  
>   Bevor Sie Zahlungsdateien aus dem Zahlungsausgangs Buch.-Blatt exportieren können, müssen Sie das elektronische Format für das beteiligte Bankkonto angeben, und den Bankdaten-Konvertierungsdienst ausführen. Weitere Informationen finden Sie unter [Einrichten von Bankkonten](bank-how-setup-bank-accounts.md) und [Einrichten des Bankdaten-Konvertierungsdiensts](bank-how-setup-bank-data-conversion-service.md). Darüber hinaus müssen Sie das Kontrollkästchen **Zahlungsexport erlauben** auf der Seite **Fibu Buch.-Blattnamen** auswählen. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  

Sie verwenden die Seite **Kreditübertragungsjournale**, um die Zahlungsdateien anzuzeigen, die aus dem Zahlungsausgangs Buch.-Blatt exportiert wurden. Von dieser Seite aus können Sie Zahlungsdateien auch erneut exportieren (im Fall von technischen Fehlern oder Dateiänderungen). Beachten Sie, dass die exportierten EFT-Dateien nicht auf dieser Seite angezeigt werden und nicht wieder exportiert werden können.  

## <a name="to-export-payments-to-a-bank-file"></a>Zahlungen in eine Bankdatei exportieren
Nachfolgend wird erläutert, wie Sie einen Kreditor mit Schecks bezahlen. Die Schritte sind ähnlich, wie wenn sie Ihren Debitoren Scheck zurückerstatten.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Zahlungs-Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die Zalungszeilen ein. Weitere Informationen finden Sie unter [Zahlungen und Rückerstattungen aufzeichnen](payables-how-post-payments-refunds.md)

> [!NOTE]  
>   Wenn Sie EFT verwenden, müssen Sie entweder **Elektronische Zahlung** oder **Elektronische Zahlung-IAT** im Feld **Bankkontozahlungsart** auswählen. Verschiedene Dateiexportdienstleistungen und deren Formaten benötigen verschiedene Einrichtungswerte auf der Seite **Bankkontokarte** und **Kreditor-Bankkontokarte**. Sie werden über die falschen oder fehlende Einrichtungswerte informiert, wenn Sie versuchen, die Datei zu exportieren.

3. Wenn Sie alle Zahlungsausgangs Buch.-Blattzeilen abgeschlossen haben, wählen Sie die Aktion **Export** aus.
4. Füllen Sie auf der Seite **Elektronische Zahlungen exportieren** die Felder nach Bedarf aus.

    Vorhandene Fehlermeldungen werden in der **Fehler Zahlungsdatei**-Infobox angezeigt, in der Sie eine Fehlermeldung festlegen können, um ausführliche Informationen anzuzeigen. Sie müssen alle Fehler lösen, bevor die Zahlungsdatei exportiert werden kann.

    > [!TIP]  
    >   Wenn Sie den Bankdaten-Konvertierungsdienst verwenden, meldet eine häufige Fehlermeldung, dass die Bankkontonummer nicht die Länge hat, die Ihre Bank benötigt. Um den Fehler zu vermeiden oder zu beheben, müssen Sie den Wert im **IBAN**-Feld auf der Seite **Bank** entfernen, und dann im **Kontokarten**-Feld eine Bankkontonummer in dem Format eingeben, das Ihre Bank erfordert.

5. Geben Sie auf der Seite **Speichern unter** den Speicherort an, zu dem die Datei exportiert werden soll, und wählen Sie dann **Speichern**.

    > [!NOTE]  
    >   Wenn Sie EFT verwenden, speichern Sie die resultierenden Kreditorenüberweisungsformulare als Word-Dokument ab oder wählen Sie aus, diese direkt per E-Mail an den Kreditor zu senden. Die Zahlungen werden jetzt auf die Seite **EFT-Datei generieren** hinzugefügt, aus der Sie mehrere Zahlungsaufträge erstellen können, um Übertragungskosten zu sparen. Weitere Informationen finden Sie unter den folgenden Themen:
6. Auf der Seite **Zahlungsausgangs Buch.-Blatt** wählen Sie die Aktion **EFT-Datei generieren** aus.

    Auf der Seite **EFT-Datei generieren** werden alle Zahlungen, die für EFT eingerichtet werden, die Sie aus dem Zahlungsausgangs Buch.-Blatt für ein angegebenes Bankkonto exportiert aber noch nicht erstellt haben, im Inforegister **Zeilen** angezeigt.
7. Wählen Sie die **EFT-Datei generieren** Aktion aus, um eine Datei für alle EFT-Zahlungen zu exportieren.
8. Geben Sie auf der Seite **Speichern unter** den Speicherort an, zu dem die Datei exportiert werden soll, und wählen Sie dann **Speichern**.

Die Bankzahlungsdatei wird in den Speicherort exportiert, den Sie festlegen, und Sie können fortfahren, sie in das elektronische Bankkonto hochzuladen und die tatsächlichen Zahlungen zu leisten. Dann können Sie die Buch.-Blattzeilen der exportierten Zahlung buchen.

## <a name="to-plan-when-to-post-exported-payments"></a>Um die Buchung von exportierten Zahlungen zu planen
Wenn Sie keine Buch.-Blattzeile für eine exportierte Zahlung buchen möchten, weil Sie beispielsweise eine Bestätigung erwarten, dass die Transaktion von der Bank verarbeitet wurde, können Sie die Buch.-Blattzeile einfach löschen. Falls Sie später eine Buch.-Blattzeile, um den Restbetrag der gebuchten Rechnung zu bezahlen, zeigt das **Exportierter Betrag gesamt**-Feld, wie viel des Zahlungsbetrags bereits exportiert wurde. Detaillierte Informationen über die exportierte Summe können Sie auch finden, indem Sie die Schaltfläche **Posten im Kreditübertragungsjournal** auswählen, um Einzelheiten zu Dateien der exportierten Zahlung anzuzeigen.

Wenn Sie ein Vorgang folgen, bei dem Sie keine Zahlungen buchen bis Sie die Bestätigung haben, dass sie in der Bank verarbeitet wurden, können Sie dieses auf zwei Arten steuern.

* In einem Zahlungsausgangs-Buch.-Blatt mit vorgeschlagenen Zahlungszeilen, können Sie entweder nach der **In Zahlungsdatei exportiert**-Spalte oder nach **Exportierter Betrag gesamt** sortieren, und dann Zahlungsvorschläge für offene Rechnungen, für die bereits Zahlungen geleistet wurden und für die Sie keine Zahlungen leisten möchten, löschen.
* Auf der Seite **Zahlungsvorschläge für Kreditoren**, in dem Sie festlegen, welche Zahlungen in das Zahlungsausgangs Buch.-Blatt einzufügen sind, können Sie das Kontrollkästchen **Exportierte Zahlungen überspringen** aktivieren, wenn Sie keine Buch.-Blattzeilen für Zahlungen einfügen möchten, die bereits exportiert wurden.

Um Informationen über exportierte Zahlungen anzuzeigen, wählen Sie die Aktion **Zahlungs-Export-Verlauf**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Um Zahlungen erneut in eine Bankdatei zu exportieren
Sie können Zahlungsdateien aus der **Kreditübertragungsjournale**-Seite exportieren. Bevor Sie Zahlungsausgangs Buch.-Blattzeilen löschen oder buchen, können Sie die Zahlungsdatei aus der **Zahlung Buch.-Blatt**-Seite auch erneut exportieren, indem Sie es einfach wieder exportieren. Wenn Sie ein Zahlungsausgangs-Buch.-Blatt gelöscht oder gebucht haben, nachdem Sie es exportiert haben, können Sie dieselbe Zahlungsdatei nur aus der **Kreditübertragungsjournale**-Seite erneut exportieren. Wählen Sie die Zeile für den Stapelauftrag für Gutschriftübertragungen aus, die Sie erneut exportieren möchten, und verwenden Sie dann die Aktion **Zahlungen erneut in Datei exportieren**.

> [!NOTE]  
>   Beachten Sie, dass die exportierten EFT-Dateien nicht auf der Seite **Kreditübertragungsjournale** angezeigt werden und nicht wieder exportiert werden können.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kredit-Transferregister** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie einen Zahlungsexport, den Sie erneut exportieren möchten, und wählen die Aktion **Erneuter Zahlungsexport in Datei** aus.

## <a name="see-also"></a>Siehe auch
[Zahlungen vornehmen](payables-make-payments.md)  
[Verbindlichkeiten](payables-manage-payables.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
