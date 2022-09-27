---
title: Verwenden Sie OCR, um PDF in elektronische Rechnungen umzuwandeln
description: Beschreibt, wie Sie einen OCR-Dienst verwenden können, um PDF-Dateien oder Bilddateien zu elektronischen Belegen umzuwandeln.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/14/2022
ms.author: edupont
ms.openlocfilehash: 74263e606c11b0491a1f84277d75493c26cf8efe
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534345"
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents"></a>Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln

Mithilfe eines externen OCR-Dienstes (optische Zeichenerkennung) können Sie aus PDF- oder Bilddateien, die Sie von Ihren Handelspartnern erhalten, elektronische Belege erstellen, die Sie in [!INCLUDE[prod_short](includes/prod_short.md)] in Belegdatensätze konvertieren können. Wenn Sie zum Beispiel eine Rechnung im PDF-Format von Ihrem Lieferanten erhalten, können Sie diese [von der Seite **Eingehende Belege** aus an den OCR-Dienst senden](#to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page).

Als Alternative zum Senden der Datei von der Seite **Eingehende Belege** kann der OCR-Dienst die Option anbieten, [Dateien zu verarbeiten, die an eine spezielle E-Mail-Adresse weitergeleitet werden](#to-send-a-pdf-or-image-file-to-the-ocr-service-by-email). Wenn Sie dann den elektronischen Beleg zurückerhalten, wird automatisch ein zugehöriger Datensatz für eingehende Dokumente in [!INCLUDE[prod_short](includes/prod_short.md)] erstellt.

Nach einigen Sekunden sendet der OCR-Dienst die verarbeitete Datei an die Seite **Eingehende Belege** als einen elektronischen Datensatz, der [in eine Einkaufsrechnung für den Verkäufer](#to-receive-the-resulting-electronic-document-from-the-ocr-service), eine Verkaufsrechnung, eine Gutschrift oder einen Journaleintrag umgewandelt werden kann.

Da OCR auf optischer Erkennung basiert, ist es wahrscheinlich, dass der OCR-Dienst die Zeichen in Ihren PDF- oder Bilddateien falsch interpretiert, wenn er z.B. die Dokumente eines bestimmten Anbieters zum ersten Mal verarbeitet. Es kann sein, dass das Logo der Firma nicht als Name des Verkäufers interpretiert wird oder dass der Gesamtbetrag auf einem Bon aufgrund seines Layouts falsch interpretiert wird. Um zu vermeiden, dass diese Fehler fortgeführt werden, können Sie die Fehler auf einer separaten Seite **Eingehender Beleg** korrigieren. Dann senden Sie die Korrekturen an den OCR-Dienst zurück, um ihn zu trainieren, die spezifischen Zeichen und Felder bei der nächsten Verarbeitung eines PDF- oder Bilddokuments für denselben Verkäufer richtig zu interpretieren. Weitere Informationen finden Sie unter [Trainieren Sie den OCR-Dienst, um Fehler zu vermeiden](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Der Dateiverkehr zum und vom OCR-Dienst wird über einen speziellen Eintrag in der Auftragswarteschlange verarbeitet. Diese Auftragswarteschlange wird automatisch erstellt, wenn Sie die externe OCR-Dienst-Verbindung aktivieren. Weitere Informationen finden Sie unter [Eingehende Belege festlegen](across-how-setup-income-documents.md).

> [!NOTE]
> Die OCR Funktion wird von externen Anbietern bereitgestellt. Wählen Sie ein Servicepaket, das für Ihr Unternehmen und/oder Ihr Land/Ihre Region geeignet ist. Dienste, die mit [!INCLUDE[prod_short](includes/prod_short.md)] kompatibel sind, und Details zu den verfügbaren Funktionen finden Sie unter [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page"></a>So senden Sie eine PDF- oder Bilddatei über die Seite Eingehende Belege an den OCR-Dienst

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
2. Erstellen Sie einen neuen Datensatz für den eingehenden Beleg und fügen Sie die Datei an. Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).  
3. Wählen auf der Seite **Eingehende Belege** eine oder mehrere Zeilen aus, und wählen Sie dann die Aktion **An Aufgabenwarteschlange senden**.

   Der Wert im Feld **OCR-Status** wird in **Bereit** geändert. Die angehängte PDF- oder Bilddatei wird von der Auftragswarteschlange gemäß dem Zeitplan an den OCR-Dienst gesendet, sofern keine Fehler vorliegen.
4. Alternativ können Sie auf der Seite **Eingehende Belege** eine oder mehrere Zeilen auswählen und dann die Aktion **An OCR-Dienst senden** wählen, um die Dateien sofort zur Verarbeitung zu senden.

   Der Wert im Feld **OCR Status** ändert sich in **Gesendet**, wenn keine Fehler vorliegen.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email"></a>So senden Sie eine PDF- oder Bilddatei per E-Mail zum OCR-Dienst

Von Ihrer E-Mail-Anwendung aus können Sie eine E-Mail mit der angehängten PDF- oder Bilddatei an den OCR-Dienstleister weiterleiten. Informationen über die E-Mail-Adresse, an die die Rechnung zu senden ist, finden Sie auf der Website des OCR-Dienstes.

Da für die Datei kein Datensatz für Eingehende Belege existiert, wird auf der Seite **Eingehende Belege** automatisch ein neuer Datensatz erstellt, wenn der OCR-Dienst das resultierende elektronische Dokument sendet. Weitere Informationen finden Sie unter [Erstellen von Datensätzen für eingehende Dokumente](across-how-create-income-document-records.md).

> [!NOTE]  
> Wenn Sie an einem Tablet oder einem Telefon arbeiten, können Sie die Datei zum OCR-Dienst senden, sobald Sie ein Foto des Dokuments aufgenommen haben, oder Sie können einen eingehenden Beleg direkt erstellen. Weitere Informationen finden Sie unter [Erstellen eines Datensatzes für ein eingehendes Dokument durch Aufnahme eines Fotos](across-how-create-income-document-records.md#to-create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service"></a>So erhalten Sie den resultierenden elektronischen Beleg vom OCR-Dienst

Das elektronische Dokument, das vom OCR-Dienst aus PDF-Dateien oder der Bilddatei erstellt wird, wird automatisch in das **Eingehende Belege**-Fenster mit dem Aufgabenwarteschlangenposten erhalten, der eingerichtet wurde, wenn Sie den OCR-Dienst aktivieren.

Wenn Sie keine Auftragswarteschlange verwenden oder ein fertiges OCR-Dokument früher als nach dem Zeitplan der Auftragswarteschlange erhalten möchten, können Sie die Aktion **Vom OCR-Dienst empfangen** wählen. Mit dieser Option erhalten Sie alle Dokumente, die durch den OCR-Dienst vervollständigt wurden.

> [!NOTE]  
> Wenn der OCR-Dienst für die manuelle Überprüfung der verarbeiteten Belegen eingerichtet wird, dann enthält das **OCR-Status**-Feld den Wert **Wartet auf Verifizierung**. Führen Sie in diesem Fall die folgenden Schritte aus, um sich auf der Website des OCR-Dienstes anzumelden und ein OCR-Dokument manuell zu überprüfen.

1. Im Feld **OCR-Status**-Feld wählen Sie den Link **Wartet auf Verifizierung** aus.
2. Melden Sie sich auf der Website des OCR-Dienstes mit den Anmeldeinformationen für Ihr OCR-Dienst-Konto an. Weitere Informationen finden Sie unter [Einrichten eines OCR-Dienstes](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   Die Daten für den OCR-Beleg werden angezeigt und zeigen den Quellinhalt der PDF-Datei oder der Bilddatei und der resultierenden OCR-Feldwerte an.
3. Überprüfen Sie die Feldwerte und bearbeiten Sie manuell oder geben Sie Werte in Felder ein, die der OCR-Dienst als unsicher gekennzeichnet hat.
4. Wählen Sie die Schaltfläche **OK** aus. Der OCR-Prozess ist abgeschlossen und der daraus resultierende elektronische Beleg wird gemäß dem Zeitplan der Auftragswarteschlange an die Seite **Eingehende Belege** in [!INCLUDE[prod_short](includes/prod_short.md)] gesendet.
5. Wiederholen Sie die Schritte 2 bis 4 für jedes weitere zu überprüfende OCR-Dokument.

Jetzt können Sie fortfahren, manuelle oder automatisch Belegdatensätze für die eingegangenen elektronische Belege in [!INCLUDE[prod_short](includes/prod_short.md)] zu erstellen. Weitere Informationen finden Sie im nächsten Verfahren. Sie können den Datensatz des neuen eingehenden Dokuments auch [mit bereits gebuchten oder nicht gebuchten Dokumenten verknüpfen](across-how-connect-disconnect-income-document-records.md), sodas die Quelldatei von [!INCLUDE[prod_short](includes/prod_short.md)] aus leicht zugänglich ist.

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service"></a>Eine Einkaufsrechnung aus einem vom OCR-Dienst erhaltenen elektronischen Beleg erstellen.

Nachfolgend wird beschrieben, wie ein Einkaufsrechnungsdatensatz von Rechnungsrabatten des Kreditors erstellt, die als elektronischer Beleg vom OCR-Dienst erhalten. Dieser Vorgang ist derselbe, wenn Sie beispielsweise eine Fibu Buch.-Blattzeile von einem Ausgabenenwareneingang oder eine Verkaufsreklamation von einem Debitoren erstellen.

> [!NOTE]  
> Die Felder **Beschreibung** und **Nummer** Felder in den erstellten Belegzeilen werden nur ausgefüllt, wenn Sie zuerst den Text aus dem OCR-Beleg zu den zwei Felder in [!INCLUDE[prod_short](includes/prod_short.md)] zugeordnet haben. Sie können diese Zuordnung als Artikelreferenzen für Belegzeilen vom Typ Artikel vornehmen. Weitere Informationen finden Sie unter [Verwendung von Element-Referenzen](inventory-how-use-item-cross-refs.md). Sie können auch die Funktion **Text-zu-Konto Zuordnung** verwenden. Weitere Informationen finden Sie unter [Text auf einem eingehenden Dokument einem bestimmten Lieferanten, Sachkonto oder Bankkonto zuordnen](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Wählen Sie die Zeile für den eingehenden Beleg aus, und wählen Sie die **Beleg erstellen**-Aktion aus.

In [!INCLUDE[prod_short](includes/prod_short.md)] wird auf der Basis der Informationen im elektronischen Kreditorenbeleg, den Sie vom OCR-Dienst erhalten haben, die Einkaufsrechnung erstellt. Die Informationen werden in der neuen Einkaufsrechnung auf der Grundlage der Zuordnung eingefügt, die Sie als Referenz oder als Text-zu-Konto-Zuordnung definiert haben.

Alle Validierungsfehler, die in der Regel mit falschen oder fehlenden Daten in [!INCLUDE[prod_short](includes/prod_short.md)] zusammenhängen, werden auf der Registerkarte **Fehler und Warnungen** angezeigt. Weitere Informationen finden Sie unter [Behandlung von Fehlern beim Empfang elektronischer Belege](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account"></a>So ordnen Sie Text auf einem eingehenden Beleg einem bestimmten Kreditorkonto zu

Für eingehende Belege verwenden **Sie üblicherweise die Aktion**, um zu definieren, das ein gegebener Text in einer Kreditorenrechnung vom OCR-Dienst zu einem bestimmten Kreditorkonto verknüpft ist. In Zukunft bedeutet jeder Teil der Beschreibung des eingehenden Dokuments, der als Zuordnungstext existiert, dass das Feld **Kreditorennummer** auf dem resultierenden Dokument oder den Buchungsblattzeilen des Typs *Sachkonto* mit dem betreffenden Lieferanten gefüllt wird.

Neben der Zuordnung zu einem Kreditorenkonto oder Sachkonto können Sie den Text auch einem Bankkonto zuordnen. Diese Option ist z.B. für elektronische Belege für bereits bezahlte Ausgaben nützlich, für die Sie eine allgemeine Buchungsblattzeile erstellen möchten, die bereit ist, auf ein Bankkonto zu buchen.

1. Wählen Sie die entsprechende Zeile des eingehenden Belegs aus, und wählen die **Text zu Konto zuordnen** Aktion aus. Die Seite **Text zu Konto zuordnen** öffnet sich.
2. In dem Feld **Abbildungstext** geben Sie beliebigen Text auf Kreditorenrechnungen ein, für die Sie Einkaufsbelege oder Buch.-Blattzeilen erstellen möchten. Sie können bis zu 50 Zeichen eingeben.
3. In dem Feld **Kreditorennr.** geben Sie den Kreditor ein, für den der sich daraus ergebende Verkaufsbeleg oder die Buch.-Blattzeile erstellt wird.
4. Geben Sie im Feld **Sollkontonr.** das Sachkonto vom Solltyp ein, das auf dem sich daraus ergebenden Verkaufsbeleg oder der Buch.-Blattzeile vom Typ "Sachkonto" eingefügt wird.
5. Geben Sie im Feld **Habenkontonr.** das Kostenart-Sachkonto ein, das auf dem sich daraus ergebenden Verkaufsbeleg oder der Buch.-Blattzeile vom Typ "Sachkonto" eingefügt wird.

   > [!NOTE]
   > Verwenden Sie die Felder **Herkunftsart Saldo** und **Herkunftsnr. Saldo** nicht in Verbindung mit eingehenden Belegen. Sie werden nur für die automatische Zahlungsabstimmung verwendet. Weitere Informationen finden Sie unter [Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
6. Wiederholen Sie die Schritte 2 bis 5 für alle Texte auf eingehenden Belegen, für die Sie automatisch Belege erstellen möchten.

## <a name="to-handle-errors-when-receiving-electronic-documents"></a>Behandeln von Fehlern beim Erhalt von elektronischen Belegen

1. Wählen Sie auf der Seite **Eingehende Belege** die Zeile für einen elektronischen Beleg aus, der vom OCR-Dienst mit Fehlern empfangen wurde, angezeigt durch den Wert *Fehler* im Feld **OCR-Status**.
2. Wählen Sie auf der Seite **Eingehende Belege** die Aktion **Bearbeiten** aus.
3. Im **Fehler und Warnungen**-Inforegister wählen Sie die Meldung aus, und wählen Sie dann die **Entsprechenden Datensatz öffnen**-Aktion aus.
4. Die Seite, die die falschen oder fehlenden Daten enthält (zum Beispiel eine Kreditorenkarte mit einem fehlenden Feldwert), wird geöffnet.
5. Beheben Sie die Fehler wie in den einzelnen Fehlermeldungen beschrieben.
6. Verarbeiten Sie den elektronischen eingehenden Beleg weiter, indem Sie die Aktion **Manuell erstellen** erneut auswählen.
7. Wiederholen Sie Schritt 5 und 6 für alle Fehler, bis der elektronische Beleg erfolgreich empfangen werden kann.

## <a name="to-train-the-ocr-service-to-avoid-errors"></a>So schulen Sie den OCR-Dienst, um Fehler zu vermeiden

Da OCR auf optischer Erkennung basiert, kann der OCR-Dienst Zeichen in Ihren PDF- oder Bilddateien falsch interpretieren, wenn er zum Beispiel zum ersten Mal Dokumente eines bestimmten Anbieters verarbeitet. Es kann sein, dass das Logo der Firma nicht als Name des Lieferanten interpretiert wird oder dass der Gesamtbetrag auf einem Spesenbeleg aufgrund des Layouts falsch interpretiert wird. Um solche Fehler zukünftigt zu vermeiden, können Sie die vom OCR-Servier erhalten Daten korrigieren und ein Feedback an den Service senden.

Die Seite **OCR-Datenkorrektur**, die Sie über das Fenster **Eingehender Beleg** öffnen, zeigt die Felder aus dem Inforegister **Finanzinformationen** in zwei Spalten an. Eine mit bearbeitungsfähigen OCR-Daten und eine mit den schreibgeschützten OCR-Daten. Wenn Sie auf die Schaltfläche **OCR-Feedback senden** klicken, wird der Inhalt der Seite **OCR-Datenkorrektur** an den OCR-Service gesendet. Wenn der Dienst das nächste Mal PDF- oder Bilddateien verarbeitet, die die betreffenden Daten enthalten, werden Ihre Korrekturen zur Verbesserung der Dokumenterkennung eingearbeitet.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie einen Datensatz eines eingehenden Dokuments, der vom OCR-Dienst empfangene Daten enthält, die Sie korrigieren möchten.
3. Wählen Sie auf der Seite **Eingehender Beleg** die Aktion **OCR-Daten korrigieren** aus.
4. Überschreiben Sie auf der Seite **OCR-Datenkorrektur** die Daten in der editierbaren Spalte für jedes Feld, das einen fehlerhaften Wert enthält.
5. Um Korrekturen rückgängig zu machen, die Sie seit dem Öffnen der Seite **OCR-Datenkorrektur** vorgenommen haben, wählen Sie die Aktion **Reset OCR Data** aus.
6. Um die Korrekturen an den OCR-Dienst zu senden, wählen Sie die Aktion **OCR-Feedback senden** aus.
7. Um die Korrekturen zu speichern, schließen Sie die Seite **OCR-Datenkorrektur**.

Die Felder auf dem Inforegister **Finanzinformationen** auf der Seite **Eingehender Beleg** werden mit allen neuen Werten aktualisiert, die Sie in Schritt 4 eingegeben haben.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Erstellen von Datensätzen für Eingehende Belege](across-how-create-income-document-records.md)
[Erstellen von Datensätzen für Eingehende Belege direkt aus Dokumenten und Einträgen](across-how-connect-disconnect-income-document-records.md)
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
