---
title: Verwenden Sie OCR, um PDF-Dateien zu E-Rechnungen umzuwandeln| Microsoft Docs
description: Beschreibt, wie Sie einen OCR-Dienst verwenden können, um PDF-Dateien oder Bilddateien zu elektronischen Belegen umzuwandeln.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c35ccb10ca67e66697002add56d518f3a7bacc0d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305164"
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln
Mithilfe eines externen OCR-Dienstes (optische Zeichenerkennung) können Sie aus PDF- oder Bilddateien, die Sie von Ihren Handelspartnern erhalten, elektronische Belege erstellen, die Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Belegdatensätze konvertieren können. Wenn Sie beispielsweise eine Rechnung in PDF-Format von Ihrem Kreditor erhalten, können Sie diese über die Seiter **Eingehende Belege** zum OCR-Dienst senden. Dies wird im ersten Verfahren beschrieben.

Als Alternative zum Versenden der Datei über die Seite **Eingehende Belege** können Sie die Datei per E-Mail zum OCR-Dienst senden. Wenn Sie dann den elektronischen Beleg zurückerhalten, wird automatisch ein damit zusammenhängener Datensatz zum eingehenden Beleg erstellt. Dies wird im zweiten Verfahren beschrieben.

Nach einigen SeDebitoren erhalten Sie die Datei vom OCR-Dienst als elektronische Rechnung zurück, die zu einer Einkaufsrechnung für den Kreditor umgewandelt werden kann. Dies wird im dritten Verfahren beschrieben.

Da OCR mit einer optischen Zeichenerkennung arbeitet, ist es wahrscheinlich, dass der OCR-Dienst Zeichen in Ihrem PDF oder in Bilddateien (beispielsweise bei der ersten Verarbeitung der Dokumente eines bestimmten Kreditor) falsch erkennt. Er interpretiert möglicherweise nicht das Firmenlogo als Name des Kreditors oder interpretiert den Gesamtbetrag auf einer Quittung aufgrund des Layouts falsch. Um zu vermeiden, dass diese Fehler fortgeführt werden, können Sie die Fehler auf einer separaten Seite **Eingehender Beleg** korrigieren. Anschließend senden Sie die Korrekturen zum OCR-Dienst zurück, um ihn zu schulen, die bestimmten Zeichen richtig zu interpretieren, wenn er das nächste Mal eine PDF- oder Bilddatei für denselben Kreditor verarbeitet. Weitere Informationen finden Sie im Abschnitt [So trainieren Sie den OCR-Dienst, um Fehler zu vermeiden](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Der Dateiverkehr zum und vom OCR-Dienst wird von einen dedizierten Projektwarteschlangeneintrag verarbeitet, der automatisch erstellt wird, wenn Sie die damit zusammenhängende Dienstverbindung aktivieren. Weitere Informationen finden Sie unter [Eingehende Belege einrichten](across-how-setup-income-documents.md).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>So senden Sie eine PDF- oder eine Bilddatei von der Seite **Eingehende Belege** an den OCR-Dienst
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren?“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Eingehende Belege** ein, und wählen dann den zugehörigen Link aus.
2. Erstellen Sie einen neuen Datensatz für den eingehenden Beleg und fügen Sie die Datei an. Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).  
3. Wählen auf der Seite **Eingehende Belege** eine oder mehrere Zeilen aus, und wählen Sie dann die Aktion **An Aufgabenwarteschlange senden**.

    Der Wert im Feld **OCR-Status** wird in **Bereit** geändert. Die angefügte PDF- oder Bilddatei wird von der Projektwarteschlange gemäß dem Zeitplan zum OCR-Dienst gesendet, sofern keine Fehler vorliegen.
4. Wählen Sie auf der Seite **Eingehende Belege** eine oder mehrere Zeilen aus, und wählen Sie dann die Aktion **An OCR-Dienst senden**.

Der Wert im Feld **OCR-Status** ändert sich zu **Gesendet**, sofern keine Fehler vorliegen.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>So senden Sie eine PDF- oder Bilddatei per E-Mail zum OCR-Dienst
Senden Sie eine E-Mail mit der PDF oder Bilddatei als Anhang aus Ihrer E-Mail-Anwendung an den OCR-Dienstanbieter. Weitere Informationen zur gewünschte E-Mail-Adresse zum Senden finden Sie auf der Website des OCR-Dienstanbieters.

Da kein eingehender Beleg für die Datei vorhanden ist, wird automatisch ein neuer Datensatz auf der Seite **Eingehende Belege** erstellt, wenn Sie den resultierenden elektronischen Beleg vom OCR-Dienst erhalten. Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).

> [!NOTE]  
>   Wenn Sie an einem Tablet oder einem Telefon arbeiten, können Sie die Datei zum OCR-Dienst senden, sobald Sie ein Foto des Dokuments aufgenommen haben, oder Sie können einen eingehenden Beleg direkt erstellen. Weitere Informationen finden Sie unter [So erstellen Sie einen Datensatz für eingehende Belege, indem Sie ein Foto machen](across-how-create-income-document-records.md#to-create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>So erhalten Sie ein fertiges elektronisches Dokument vom OCR-Service
Das elektronische Dokument, das vom OCR-Dienst aus PDF-Dateien oder der Bilddatei erstellt wird, wird automatisch in das **Eingehende Belege**-Fenster mit dem Aufgabenwarteschlangenposten erhalten, der eingerichtet wurde, wenn Sie den OCR-Dienst aktivieren.

Wenn Sie keine Aufgabenwarteschlange verwenden oder Sie einen fertigen OCR-Beleg früher als für den Aufgabenwarteschlangenplan geplant erhalten möchten, können Sie die **Von OCR-Dienst abrufen**-Schaltfläche verwenden. So rufen Sie alle Dokumente ab, die vom OCR-Dienst abgeschlossen wurden.

> [!NOTE]  
>   Wenn der OCR-Dienst für die manuelle Überprüfung der verarbeiteten Belegen eingerichtet wird, dann enthält das **OCR-Status**-Feld den Wert **Wartet auf Verifizierung**. In diesem Fall führen Sie die folgenden Schritte aus, um sich an der OCR-Dienst-Website anzumelden, um einen OCR-Beleg manuell zu überprüfen.

1. Im Feld **OCR-Status**-Feld wählen Sie den Link **Wartet auf Verifizierung** aus.
2. Melden Sie sich auf der OCR-Dienst-Website mit den Anmeldeinformationen des OCR-Service-Kontos an. Das sind die Anmeldeinformationen, die Sie beim Einrichten des Dienstes verwendet haben. Weitere Informationen finden Sie unter [So richten Sie einen OCR-Dienst ein](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

    Die Daten für den OCR-Beleg werden angezeigt und zeigen den Quellinhalt der PDF-Datei oder der Bilddatei und der resultierenden OCR-Feldwerte an.
3. Prüfen Sie die verschiedenen Feldwerte und bearbeiten Sie sie manuell geben Sie Werte in die Felder ein, die der OCR-Dienst als unsicher markiert hat.
4. Wählen Sie die Schaltfläche **OK** aus. Der OCR-Vorgang ist abgeschlossen und das resultierende elektronische Dokument wird an die **Eingehender Belege**-Seite in [!INCLUDE[d365fin](includes/d365fin_md.md)] entsprechend dem Aufgabenwarteschlangenplan gesendet.
5. Wiederholen Sie Schritt 4 für jeden anderen zu überprüfenden OCR-Beleg.

Jetzt können Sie fortfahren, manuelle oder automatisch Belegdatensätze für die eingegangenen elektronische Belege in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu erstellen. Weitere Informationen finden Sie im nächsten Verfahren. Sie können außerdem den neuen eingehenden Beleg mit vorhandenen gebuchten oder nicht gebuchten Belegen verknüpfen, sodass aus [!INCLUDE[d365fin](includes/d365fin_md.md)] einfach auf die Quelldatei zugegriffen werden kann. Weitere Informationen finden Sie unter [Eingehende Belege verarbeiten](across-process-income-documents.md).

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Eine Einkaufsrechnung aus einem vom OCR-Dienst erhaltenen elektronischen Beleg erstellen.
Nachfolgend wird beschrieben, wie ein Einkaufsrechnungsdatensatz von Rechnungsrabatten des Kreditors erstellt, die als elektronischer Beleg vom OCR-Dienst erhalten. Dieser Vorgang ist derselbe, wenn Sie beispielsweise eine Fibu Buch.-Blattzeile von einem Ausgabenenwareneingang oder eine Verkaufsreklamation von einem Debitoren erstellen.

> [!NOTE]  
>   Die Felder **Beschreibung** und **Nummer** Felder in den erstellten Belegzeilen werden nur ausgefüllt, wenn Sie zuerst den Text aus dem OCR-Beleg zu den zwei Felder in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet haben. Sie können diese Zuordnung als Artikel-Referenzen für Belegzeilen vom Typ "Artikel" durchführen. Weitere Informationen finden Sie unter [Verwenden von Artikelquerverweisen](inventory-how-use-item-cross-refs.md). Sie können auch die Text-zu-Kontozuordnungsfunktion verwenden. Weitere Informationen finden Sie im Abschnitt [So ordnen Sie Text zu einem eingehenden Beleg einem bestimmten Kreditor, Sachkonto oder Bankkonto zu](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Wählen Sie die Zeile für den eingehenden Beleg aus, und wählen Sie die **Beleg erstellen**-Aktion aus.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] wird auf der Basis der Informationen im elektronischen Kreditorenbeleg, den Sie vom OCR-Dienst erhalten haben, die Einkaufsrechnung erstellt. Informationen werden in die neue Einkaufsrechnung auf Grundlage der Zuordnung eingefügt, die Sie als Referenz oder als Text-zu-Kontozuordnung definiert haben.

Überprüfungsfehler, die üblicherweise mit falschen oder fehlenden Stammdaten in [!INCLUDE[d365fin](includes/d365fin_md.md)] zusammenhängen, werden im Inforegister **Fehler und Warnungen** angezeigt. Weitere Informationen finden Sie unter [So behandeln Sie Fehler beim Erhalt elektronischer Belege](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>So ordnen Sie Text auf einem eingehenden Beleg einem bestimmten Kreditorkonto zu
Für eingehende Belege verwenden **Sie üblicherweise die Aktion**, um zu definieren, das ein gegebener Text in einer Kreditorenrechnung vom OCR-Dienst zu einem bestimmten Kreditorkonto verknüpft ist. Danach wird bei jedem Teil der eingehende Beleg, der als Zuordnungstext vorhanden ist, das Feld **Nr.** in Beleg- oder Buch.-Blattzeilen der Art Sachkonto werden mit dem jeweiligen Kreditor gefüllt.

Neben der Zuordnung zu einem Kreditor oder einem anderen Sachkonto können Sie auch ein Bankkonto zuordnen. Dies ist beispielsweise für elektronische Belege für Ausgaben nützlich, die bereits bezahlt wurden, für die Sie jedoch eine Fibu Buch.-Blattzeile erstellen möchten, die auf ein Bankkonto buchen kann.

1. Wählen Sie die entsprechende Zeile des eingehenden Belegs aus, und wählen die **Text zu Konto zuordnen** Aktion aus. Die Seite **Text zu Konto zuordnen** öffnet sich.
3. In dem Feld **Abbildungstext** geben Sie beliebigen Text auf Kreditorenrechnungen ein, für die Sie Einkaufsbelege oder Buch.-Blattzeilen erstellen möchten. Sie können bis zu 50 Zeichen eingeben.
4. In dem Feld **Kreditorennr.** geben Sie den Kreditor ein, für den der sich daraus ergebende Verkaufsbeleg oder die Buch.-Blattzeile erstellt wird.
5. Geben Sie im Feld **Sollkontonr.** das Sachkonto vom Solltyp ein, das auf dem sich daraus ergebenden Verkaufsbeleg oder der Buch.-Blattzeile vom Typ "Sachkonto" eingefügt wird.
6. Geben Sie im Feld **Habenkontonr.** das Kostenart-Sachkonto ein, das auf dem sich daraus ergebenden Verkaufsbeleg oder der Buch.-Blattzeile vom Typ "Sachkonto" eingefügt wird.

    > [!NOTE]
    > Verwenden Sie die Felder **Herkunftsart Saldo** und **Herkunftsnr. Saldo** nicht in Verbindung mit eingehenden Belegen. Sie werden nur für die automatische Zahlungsabstimmung verwendet. Weitere Informationen finden Sie unter [Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

7. Wiederholen Sie die Schritte 2 bis 5 für alle Texte auf eingehenden Belegen, für die Sie automatisch Belege erstellen möchten.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Behandeln von Fehlern beim Erhalt von elektronischen Belegen
1. Auf der **Eingehende Belege** Seite wählen Sie die Zeile für ein elektronischer Beleg aus, der vom OCR-Dienst mit Fehlern erhalten wurde. Dies wird durch den Fehlerwert im Feld **OCR Status**-Feld angegeben.
2. Wählen Sie auf der Seite **Eingehende Belege** die Aktion **Bearbeiten** aus.
3. Im **Fehler und Warnungen**-Inforegister wählen Sie die Meldung aus, und wählen Sie dann die **Entsprechenden Datensatz öffnen**-Aktion aus.
4. Die Seite, die die falschen oder fehlenden Daten enthält (zum Beispiel eine Kreditorenkarte mit einem fehlenden Feldwert), wird geöffnet.
5. Beheben Sie die Fehler wie in den einzelnen Fehlermeldungen beschrieben.
6. Verarbeiten Sie den elektronischen eingehenden Beleg weiter, indem Sie die Aktion **Manuell erstellen** erneut auswählen.
7. Wiederholen Sie Schritt 5 und 6 für alle Fehler, bis der elektronische Beleg erfolgreich empfangen werden kann.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>So schulen Sie den OCR-Dienst, um Fehler zu vermeiden
Da OCR mit einer optischen Zeichenerkennung arbeitet, ist es wahrscheinlich, dass der OCR-Service Zeichen in Ihrem PDF oder in Bilddateien (beispielsweise bei der ersten Verarbeitung von einem bestimmten eines bestimmten Kreditor) falsch erkennt. Es interpretiert möglicherweise nicht das Firmenlogo als Name des Kreditors, oder interpretiert den Gesamtbetrag aufgrund des Layouts falsch. Um solche Fehler zukünftigt zu vermeiden, können Sie die vom OCR-Servier erhalten Daten korrigieren und ein Feedback an den Service senden.

Die Seite **OCR-Datenkorrektur**, die Sie über das Fenster **Eingehender Beleg** öffnen, zeigt die Felder aus dem Inforegister **Finanzinformationen** in zwei Spalten an. Eine mit bearbeitungsfähigen OCR-Daten und eine mit den schreibgeschützten OCR-Daten. Wenn Sie auf die Schaltfläche **OCR-Feedback senden** klicken, wird der Inhalt der Seite **OCR-Datenkorrektur** an den OCR-Service gesendet. Bei der nächsten Verarbeitung eines PDFs oder einer Bilddateien mit den entsprechenden Daten durch den Service werden Ihre Korrekturen dazu genutzt, die gleichen Fehler zu vermeiden.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Eingehende Belege** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie einen eingehenden Belegsdatensatz mit den Daten, die vom OCR-Dienst empfangen wurden und die Sie korrigieren möchten.
3. Wählen Sie auf der Seite **Eingehender Beleg** die Aktion **OCR-Daten korrigieren** aus.
4. Überschreiben Sie auf der Seite **OCR-Datenkorrektur** die Daten in der editierbaren Spalte für jedes Feld, das einen fehlerhaften Wert enthält.
5. Um Korrekturen rückgängig zu machen, die Sie seit dem Öffnen der Seite **OCR-Datenkorrektur** vorgenommen haben, wählen Sie die Aktion **Reset OCR Data** aus.
6. Um die Korrekturen an den OCR-Dienst zu senden, wählen Sie die Aktion **OCR-Feedback senden** aus.
7. Um die Korrekturen zu speichern, schließen Sie die Seite **OCR-Datenkorrektur**.

Die Felder auf dem Inforegister **Finanzinformationen** auf der Seite **Eingehender Beleg** werden mit allen neuen Werten aktualisiert, die Sie in Schritt 4 eingegeben haben.

## <a name="see-also"></a>Siehe auch
[Eingehende Belege verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
