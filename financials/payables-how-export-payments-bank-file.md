---
title: 'Vorgehensweise: Zahlungen in eine Bankdatei exportieren | Microsoft Docs'
description: 'Vorgehensweise: Zahlungen in eine Bankdatei exportieren'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 04/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a7f388db2d00b9916160d19edead92714f6eacc1
ms.contentlocale: de-de
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-export-payments-to-a-bank-file"></a>Vorgehensweise: Zahlungen in eine Bankdatei exportieren
Wenn Sie bereit sind, Zahlungen an Ihre Kreditoren mit dem Fenster **Zahlung Buch.-Blatt** vorzunehmen, können Sie eine Datei mit den Zahlungsinformationen auf den Buch.-Blattzeilen exportieren. Sie können die Datei dann zu Ihrer elektronischen Bank hochladen, um die entsprechenden Geldüberweisungen zu verarbeiten.

In der generischen Version von [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]  wird ein globaler Diensteanbieter eingerichtet und verbunden, der Bankdaten in das Dateiformat konvertiert, das Ihre Bank verlangt. In den nordamerikanischen Versionen kann derselbe Service verwendet werden, um Zahlungsdateien als elektronischer Geldtransfer (EFT) zu buchen, mit einem leicht anderen Prozess. Siehe Schritt 6 im Bereich "Zahlungen in eine Bankdatei exportieren".    

**Hinweis**: Bevor Sie Zahlungsdateien aus dem Zahlungsausgangs Buch.-Blatt exportieren können, müssen Sie das elektronische Format für das beteiligte Bankkonto angeben, und den Bankdaten-Konvertierungsdienst ausführen. Weitere Informationen finden Sie unter [So gehts: Einrichten von Bankkonten](bank-how-setup-bank-accounts.md) und [So gehts: Einrichten des Bankdaten-Konvertierungsdiensts](bank-how-setup-bank-data-conversion-service.md). Darüber hinaus müssen Sie das Kontrollkästchen **Zahlungsexport erlauben** im Fenster **Fibu Buch.-Blattnamen** auswählen. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)  

Sie verwenden das Fenster **Kreditübertragungsjournale**, um die Zahlungsdateien anzuzeigen, die aus dem Zahlungsausgangs Buch.-Blatt exportiert wurden. Von diesem Fenster aus können Sie Zahlungsdateien auch erneut exportieren (im Fall von technischen Fehlern oder Dateiänderungen). Beachten Sie, dass die exportierten EFT-Dateien nicht in diesem Fenster angezeigt werden und nicht wieder exportiert werden können.  

## <a name="to-export-payments-to-a-bank-file"></a>Zahlungen in eine Bankdatei exportieren
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen aus**![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen.") Geben Sie **Zahlungsjournal** ein und wählen Sie dann den entsprechenden Link aus.
2. Füllen Sie die Buch.-Blattzeilen z. B. mit der Funktion **Zahlungsvorschlag** aus. Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).
3. Füllen Sie die Felder in den Buch.-Blattzeilen wie notwendig aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    **Hinweis**: Wenn Sie EFT verwenden, müssen Sie entweder **Elektronische Zahlung** oder **Elektronische Zahlung-IAT** im Feld **Bankkontozahlungsart** auswählen.

    Verschiedene Dateiexportdienstleistungen und deren Formaten benötigen verschiedene Einrichtungswerte im Fenster **Bankkontokarte** und **Kreditor-Bankkontokarte**. Sie werden über die falschen oder fehlende Einrichtungswerte informiert, wenn Sie versuchen, die Datei zu exportieren.
        
4. Wenn Sie alle Zahlungsausgangs Buch.-Blattzeilen abgeschlossen haben, wählen Sie die Aktion **Export** aus.
5. Füllen Sie im Fenster **Elektronische Zahlungen exportieren** die Felder nach Bedarf aus.

    Vorhandene Fehlermeldungen werden in der **Fehler Zahlungsdatei**-Infobox angezeigt, in der Sie eine Fehlermeldung festlegen können, um ausführliche Informationen anzuzeigen. Sie müssen alle Fehler lösen, bevor die Zahlungsdatei exportiert werden kann.

    **Tipp**: Wenn Sie den Bankdaten-Konvertierungsdienst verwenden, meldet eine häufige Fehlermeldung, dass die Bankkontonummer nicht die Länge hat, die Ihre Bank benötigt. Um den Fehler zu vermeiden oder zu beheben, müssen Sie den Wert im **IBAN**-Feld im **Bankkontokarte**-Fenster entfernen, und dann im Feld **Bankkontonummer** eine Bankkontonummer im Format eingeben, das die Bank benötigt.

6. Geben Sie im Fenster **Speichern unter** den Speicherort an, zu dem die Datei exportiert werden soll, und wählen Sie dann **Speichern**.

    **Hinweis**: Wenn Sie EFT verwenden, speichern Sie die resultierenden Kreditorenüberweisungsformulare als Word-Dokument ab oder wählen Sie aus, diese direkt per E-Mail an den Kreditor zu senden. Die Zahlungen werden jetzt in das Fenster **EFT-Datei generieren** hinzugefügt, aus der Sie mehrere Zahlungsaufträge erstellen können, um Übertragungskosten zu sparen. Weitere Informationen finden Sie unter den folgenden Themen:
7. Im Fenster **Zahlungsausgangs Buch.-Blatt** wählen Sie die Aktion **EFT-Datei generieren** aus.

    Im Fenster **EFT-Datei generieren** werden alle Zahlungen, die für EFT eingerichtet werden, die Sie aus dem Zahlungsausgangs Buch.-Blatt für ein angegebenes Bankkonto exportiert aber noch nicht erstellt haben, im Inforegister **Zeilen** angezeigt.
8. Wählen Sie die **EFT-Datei generieren** Aktion aus, um eine Datei für alle EFT-Zahlungen zu exportieren.
9. Geben Sie im Fenster **Speichern unter** den Speicherort an, zu dem die Datei exportiert werden soll, und wählen Sie dann **Speichern**.

Die Bankzahlungsdatei wird in den Speicherort exportiert, den Sie festlegen, und Sie können fortfahren, sie in das elektronische Bankkonto hochzuladen und die tatsächlichen Zahlungen zu leisten. Dann können Sie die Buch.-Blattzeilen der exportierten Zahlung buchen.

## <a name="to-export-payments-that-represent-customer-refunds"></a>So exportieren Sie Zahlungen, die Debitorenerstattungen darstellen
Nachfolgend wird eine Vorgehensweise zum Exportieren von elektronischen Erstattungszahlungen erläutert.

**Vorsicht**: Die resultierenden Buch.-Blattzeilen können nicht gebucht, gelöscht oder storniert werden.
1. Kunden als Kreditor einrichten. Nennen wir ihn beispielsweise  "Debitor X für Erstattungen". Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten neuer Kreditoren](purchasing-how-register-new-vendors.md).
2. Auf der Zahlungsbuch.-Blattzeile für den Debitor setzen Sie das Feld **Kontoart** auf **Debitor** und das Feld **Belegart** auf **Erstattung** fest.
3. Führen Sie die normalen Schritte für Zahlungsexporte aus, die im Abschnitt "Zahlungen in eine Bankdatei exportieren"  erläutert sind.

## <a name="to-plan-when-to-post-exported-payments"></a>Um die Buchung von exportierten Zahlungen zu planen
Wenn Sie keine Buch.-Blattzeile für eine exportierte Zahlung buchen möchten, weil Sie beispielsweise eine Bestätigung erwarten, dass die Transaktion von der Bank verarbeitet wurde, können Sie die Buch.-Blattzeile einfach löschen. Falls Sie später eine Buch.-Blattzeile, um den Restbetrag der gebuchten Rechnung zu bezahlen, zeigt das **Exportierter Betrag gesamt**-Feld, wie viel des Zahlungsbetrags bereits exportiert wurde. Detaillierte Informationen über die exportierte Summe können Sie auch finden, indem Sie die Schaltfläche **Posten im Kreditübertragungsjournal** auswählen, um Einzelheiten zu Dateien der exportierten Zahlung anzuzeigen.

Wenn Sie ein Vorgang folgen, bei dem Sie keine Zahlungen buchen bis Sie die Bestätigung haben, dass sie in der Bank verarbeitet wurden, können Sie dieses auf zwei Arten steuern.

* In einem Zahlungsausgangs-Buch.-Blatt mit vorgeschlagenen Zahlungszeilen, können Sie entweder nach der **In Zahlungsdatei exportiert**-Spalte oder nach **Exportierter Betrag gesamt** sortieren, und dann Zahlungsvorschläge für offene Rechnungen, für die bereits Zahlungen geleistet wurden und für die Sie keine Zahlungen leisten möchten, löschen.
* Im Fenster **Zahlungsvorschläge für Kreditoren**, in dem Sie festlegen, welche Zahlungen in das Zahlungsausgangs Buch.-Blatt einzufügen sind, können Sie das Kontrollkästchen **Exportierte Zahlungen überspringen** aktivieren, wenn Sie keine Buch.-Blattzeilen für Zahlungen einfügen möchten, die bereits exportiert wurden.

Um Informationen über exportierte Zahlungen anzuzeigen, wählen Sie die Aktion **Zahlungs-Export-Verlauf**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Um Zahlungen erneut in eine Bankdatei zu exportieren
Sie können Zahlungsdateien aus dem **Kreditübertragungsjournale**-Fenster exportieren. Bevor Sie Zahlungsausgangs Buch.-Blattzeilen löschen oder buchen, können Sie die Zahlungsdatei aus dem **Zahlung Buch.-Blatt**-Fenster auch erneut exportieren, indem Sie es einfach wieder exportieren. Wenn Sie ein Zahlungsausgangs-Buch.-Blatt gelöscht oder gebucht haben, nachdem Sie es exportiert haben, können Sie dieselbe Zahlungsdatei nur aus dem **Kreditübertragungsjournale**-Fenster erneut exportieren. Wählen Sie die Zeile für den Stapelauftrag für Gutschriftübertragungen aus, die Sie erneut exportieren möchten, und verwenden Sie dann die Aktion **Zahlungen erneut in Datei exportieren**.

**Hinweis**Beachten Sie, dass die exportierten EFT-Dateien nicht im Fenster **Kreditübertragungsjournale**angezeigt werden und nicht wieder exportiert werden können.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus! ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und **Kreditübertragungsjournale** eingeben und den entsprechenden Link auswählen.„”
2. Wählen Sie einen Zahlungsexport, den Sie erneut exportieren möchten, und wählen die Aktion **Erneuter Zahlungsexport in Datei** aus.

## <a name="see-also"></a>Siehe auch
[Verbindlichkeiten](payables-manage-payables.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md]

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
