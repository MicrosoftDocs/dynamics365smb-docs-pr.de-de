---
title: 'So gehts: Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln| Microsoft Docs'
description: Beschreibt, wie OCR verwendet wird, um PDF und Bilddateien in elektronische Belege umzuwandeln
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 03/22/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7be94659e8f00021446314acf6558ae01b158971
ms.contentlocale: de-de
ms.lasthandoff: 06/26/2017


---
# Gewusst wie: Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln
<a id="how-to-use-ocr-to-turn-pdf-and-image-files-into-electronic-documents" class="xliff"></a>
Mithilfe eines externen OCR-Dienstes (optische Zeichenerkennung) können Sie aus PDF- oder Bilddateien, die Sie von Ihren Handelspartnern erhalten, elektronische Belege erstellen, die Sie in [!INCLUDE[d365fin](includes/d365fin_md.md)] in Belegdatensätze konvertieren können. Wenn Sie beispielsweise eine Rechnung in PDF-Format von Ihrem Kreditor erhalten, können Sie diese über das Fenster **Eingehende Belege** zum OCR-Dienst senden. Dies wird im ersten Verfahren beschrieben.

Als Alternative zum Versenden der Datei über das Fenster **Eingehende Belege** können Sie die Datei per E-Mail zum OCR-Dienst senden. Wenn Sie dann den elektronischen Beleg zurückerhalten, wird automatisch ein damit zusammenhängener Datensatz zum eingehenden Beleg erstellt. Dies wird im zweiten Verfahren beschrieben.

Nach einigen Sekunden erhalten Sie die Datei vom OCR-Dienst als elektronische Rechnung zurück, die zu einer Einkaufsrechnung für den Kreditor umgewandelt werden kann. Dies wird im dritten Verfahren beschrieben.

Da OCR mit einer optischen Zeichenerkennung arbeitet, ist es wahrscheinlich, dass der OCR-Dienst Zeichen in Ihrem PDF oder in Bilddateien (beispielsweise bei der ersten Verarbeitung der Dokumente eines bestimmten Kreditor) falsch erkennt. Er interpretiert möglicherweise nicht das Firmenlogo als Name des Kreditors oder interpretiert den Gesamtbetrag auf einer Quittung aufgrund des Layouts falsch. Um zu vermeiden, dass diese Fehler fortgeführt werden, können Sie die Fehler in einem separaten Fenster **Eingehender Beleg** korrigieren. Anschließend senden Sie die Korrekturen zum OCR-Dienst zurück, um ihn zu schulen, die bestimmten Zeichen richtig zu interpretieren, wenn er das nächste Mal eine PDF- oder Bilddatei für denselben Kreditor verarbeitet. Weitere Informationen finden Sie im Abschnitt "So trainieren Sie den OCR-Dienst, um Fehler zu vermeiden".

Der Dateiverkehr zum und vom OCR-Dienst wird von einen dedizierten Projektwarteschlangeneintrag verarbeitet, der automatisch erstellt wird, wenn Sie die damit zusammenhängende Dienstverbindung aktivieren. Weitere Informationen finden Sie unter [So gehts: Einrichten von eingehenden Belegen](across-how-setup-income-documents.md).

## So senden Sie eine PDF- oder eine Bilddatei vom Fenster **Eingehende Belege** an den OCR-Dienst
<a id="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-window" class="xliff"></a>
1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Eingehende Dokumente** ein und wählen Sie dann den entsprechenden Link aus.
2. Erstellen Sie einen neuen Datensatz für den Eingangsbeleg und fügen Sie die Datei an. Weitere Informationen finden Sie unter [So gehts: Eingehende Dokumente erstellen](across-how-create-income-document-records.md).  
3. Wählen Sie im Fenster **Eingehende Belege** eine oder mehrere Zeilen aus, und wählen Sie dann die Aktion **An Aufgabenwarteschlange senden**.

    Der Wert im Feld **OCR-Status** wird in **Bereit** geändert. Die angefügte PDF- oder Bilddatei wird von der Projektwarteschlange gemäß dem Zeitplan zum OCR-Dienst gesendet, sofern keine Fehler vorliegen.
4. Wählen Sie im Fenster **Eingehende Belege** eine oder mehrere Zeilen aus, und wählen Sie dann die Aktion **An OCR-Dienst senden**.

Der Wert im Feld **OCR-Status** ändert sich zu **Gesendet**, sofern keine Fehler vorliegen.

## So senden Sie eine PDF- oder Bilddatei per E-Mail zum OCR-Dienst
<a id="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email" class="xliff"></a>
Senden Sie eine E-Mail mit der PDF oder Bilddatei als Anhang aus Ihrer E-Mail-Anwendung an den OCR-Dienstanbieter. Weitere Informationen zur gewünschte E-Mail-Adresse zum Senden finden Sie auf der Website des OCR-Dienstanbieters.

Da kein Eingangsbeleg-Datensatz für die Datei vorhanden ist, wird automatisch ein neuer Datensatz im Fenster **Eingehende Belege** erstellt, wenn Sie den resultierenden elektronischen Beleg vom OCR-Dienst erhalten. Weitere Informationen finden Sie unter [So gehts: Eingehende Dokumente erstellen](across-how-create-income-document-records.md).

**Hinweis**: Wenn Sie mit einem Tablet oder einem Telefon arbeiten, können Sie die Datei zum OCR-Dienst senden, sobald Sie ein Foto des Dokuments aufgenommen haben, oder Sie können einen Eingangsbeleg direkt erstellen. Weitere Informationen finden Sie im Abschnitt "So erstellen Sie Eingangsbelegdatensätze indem Sie ein Foto machen" entnehmen [So gehts: Erstellen von Eingangsbelegen](across-how-create-income-document-records.md).

## So erhalten Sie ein fertiges elektronisches Dokument vom OCR-Service
<a id="to-receive-the-resulting-electronic-document-from-the-ocr-service" class="xliff"></a>
Das elektronische Dokument, das vom OCR-Dienst aus PDF-Dateien oder der Bilddatei erstellt wird, wird automatisch in das **Eingehende Belege**-Fenster mit dem Aufgabenwarteschlangenposten erhalten, der eingerichtet wurde, wenn Sie den OCR-Dienst aktivieren.

Wenn Sie keine Aufgabenwarteschlange verwenden oder Sie einen fertigen OCR-Beleg früher als für den Aufgabenwarteschlangenplan geplant erhalten möchten, können Sie die **Von OCR-Dienst abrufen**-Schaltfläche verwenden. So rufen Sie alle Dokumente ab, die vom OCR-Dienst abgeschlossen wurden.

**Hinweis**
: Wenn der OCR-Dienst für die manuelle Überprüfung der verarbeiteten Belegen eingerichtet wird, dann enthält das **OCR-Status**-Feld den Wert **Wartet auf Verifizierung**. In diesem Fall führen Sie die folgenden Schritte aus, um sich an der OCR-Dienst-Website anzumelden, um einen OCR-Beleg manuell zu überprüfen.

1. Im Feld **OCR-Status**-Feld wählen Sie den Link **Wartet auf Verifizierung** aus. Alternativ wählen Sie die **Wartet auf Verifizierung**-Kachel auf der Homepage aus.
2. Melden Sie sich auf der OCR-Dienst-Website mit den Anmeldeinformationen des OCR-Service-Kontos an. Das sind die Anmeldeinformationen, die Sie beim Einrichten des Dienstes verwendet haben. Weitere Informationen finden Sie im Abschnitt"So richten Sie einen OCR-Service ein"in [Gewusst wie: Eingehende Dokumente einrichten](across-how-setup-income-documents.md).

    Wenn Sie auf die Website über das Feld **OCR Status** zugreifen, wird der entsprechende Beleg sofort nach Ihrem Anmelden gezeigt. Wenn Sie auf die Website zugreifen, indem Sie die Kachel auf der Startseite auswählen, müssen Sie auf der ersten OCR-Dienst-Seite die **Start**-Schaltfläche auf der Registerkarte **Prüfen** auswählen, oder in den Beleg, den Sie prüfen möchten doppelklicken.

    Die Daten für den OCR-Beleg werden angezeigt und zeigen den Quellinhalt der PDF-Datei oder der Bilddatei und der resultierenden OCR-Feldwerte an.
3. Prüfen Sie die verschiedenen Feldwerte und bearbeiten Sie sie manuell geben Sie Werte in die Felder ein, die der OCR-Dienst als unsicher markiert hat.
4. Wählen Sie die Schaltfläche **OK** aus. Der OCR-Vorgang ist abgeschlossen und das resultierende elektronische Dokument wird an das **Eingehender Belege**-Fenster in [!INCLUDE[d365fin](includes/d365fin_md.md)] entsprechend dem Aufgabenwarteschlangenplan gesendet.

    Wenn Sie auf die Website zugreifen, indem Sie die Kachel der Startseite auswählen, wird jeder andere zu überprüfende OCR-Beleg automatisch auf der Website angezeigt.
5. Wiederholen Sie Schritt 4 für jeden anderen zu überprüfenden OCR-Beleg.

Jetzt können Sie fortfahren, manuelle oder automatisch Belegdatensätze für die eingegangenen elektronische Belege in [!INCLUDE[d365fin](includes/d365fin_md.md)] zu erstellen. Weitere Informationen finden Sie im nächsten Verfahren. Sie können außerdem den neuen Eingangsbelegdatensatz mit vorhandenen gebuchten oder nicht gebuchten Belegen verknüpfen, sodass aus [!INCLUDE[d365fin](includes/d365fin_md.md)] einfach auf die Quelldatei zugegriffen werden kann. Weitere Informationen finden Sie unter [Eingehende Dokumente verarbeiten](across-process-income-documents.md).

## Eine Einkaufsrechnung aus einem vom OCR-Dienst erhaltenen elektronischen Beleg erstellen.
<a id="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service" class="xliff"></a>
Nachfolgend wird beschrieben, wie ein Einkaufsrechnungsdatensatz von Rechnungsrabatten des Kreditors erstellt, die als elektronischer Beleg vom OCR-Dienst erhalten. Dieser Vorgang ist derselbe, wenn Sie beispielsweise eine Fibu Buch.-Blattzeile von einem Ausgabenenwareneingang erstellen.

**Hinweis:**: Die Felder **Beschreibung** und **Nummer** Felder in den erstellten Belegzeilen werden nur ausgefüllt, wenn Sie zuerst den Text aus dem OCR-Beleg zu den zwei Felder in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet haben. Sie können dies entweder über Artikel-Referenzen, für Belegzeilen vom Typ Artikel oder als Text-zu-Konto-Zuordnungen für Beleg- oder Buch.-Blattzeilen vom Typ Sachkonto machen Weitere Informationen finden Sie in der QuickInfo für die Aktion **Referenzen** auf Artikelkarten und dem zugehörigen Verfahren [Vorgehensweise: Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Für eingehende Belege verwenden **Sie üblicherweise die Aktion**, um zu definieren, das ein gegebener Text in einer Kreditorenrechnung vom OCR-Dienst zu einem bestimmten Kreditorkonto verknüpft ist. Danach wird bei jedem Teil der Dokumentbeschreibung, derals Zuordnungstext vorhanden ist das Feld **Nr.** in Beleg- oder Buch.-Blattzeilen der Art Sachkonto werden mit dem jeweiligen Kreditor gefüllt.

Neben der Zuordnung zu einem Kreditor oder einem anderen Sachkonto können Sie auch ein Bankkonto zuordnen. Dies ist beispielsweise für elektronische Belege für Ausgaben nützlich, die bereits bezahlt wurden, für die Sie jedoch eine Fibu Buch.-Blattzeile erstellen möchten, die auf ein Bankkonto buchen kann.

1. Wählen Sie die Zeile des eingehenden Beleges für elektronischen Kreditorenbeleg aus, der vom OCR-Dienst erhalten wird.
2. Um Text in dem Beleg dem Kreditorenkonto zuzuordnen, wählen Sie die Aktion **Zu Konto zuordnen** und füllen dann das Fenster **Zuordnung Text zu Konto** mit Informationen aus, die für den Kreditor gelten. Weitere Informationen finden Sie unter [Vorgehensweise: Zuordnen von sich wiederholenden Zahlungen an Konten bei der automatischen Abstimmung](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
3. Um die Artikelnummern im Beleg Ihren Artikelbeschreibungen des Kreditors zuzuordnen, öffnen Sie die Karte eines jeden Artikels, und wählen Sie dann die **Referenzen**-Aktion aus, um Referenzen zwischen Ihren Artikelbeschreibungen und dem des Kreditors einzurichten.
4. Wählen Sie im Fenster **Einrichtung für eingehende Dokumente** die Aktion **Dokument erstellen** aus.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] wird auf der Basis der Informationen im elektronischen Kreditorenbeleg, den Sie vom OCR-Dienst erhalten haben, die Einkaufsrechnung erstellt.

Überprüfungsfehler, die üblicherweise mit falschen oder fehlenden Stammdaten in [!INCLUDE[d365fin](includes/d365fin_md.md)] zusammenhängen, werden im Inforegister **Fehler und Warnungen** angezeigt. Weitere Informationen finden Sie unter "So behandeln Sie Fehler beim Erhalt eines elektronischen Belegs im Fenster „Eingehende Dokumente".

## Behandeln von Fehlern beim Erhalt von elektronischen Belegen
<a id="to-handle-errors-when-receiving-electronic-documents" class="xliff"></a>
1. Im **Eingehende Belege** Fenster wählen Sie die Zeile für ein elektronischer Beleg aus, der vom OCR-Dienst mit Fehlern erhalten wurde. Dies wird durch den Fehlerwert im Feld **OCR Status**-Feld angegeben.
2. Wählen Sie im Fenster **Eingehende Dokumente** die Aktion **Bearbeiten** aus.
3. Im **Fehler und Warnungen**-Inforegister wählen Sie die Meldung aus, und wählen Sie dann die **Entsprechenden Datensatz öffnen**-Aktion aus.
4. Das Fenster, das die falschen oder fehlenden Daten enthält (zum Beispiel eine Kreditorenkarte mit einem fehlenden Feldwert), wird geöffnet.
5. Beheben Sie die Fehler wie in den einzelnen Fehlermeldungen beschrieben.
6. Verarbeiten Sie den elektronischen Eingangsbeleg weiter, indem Sie die Aktion **Manuell erstellen** erneut auswählen.
7. Wiederholen Sie Schritt 5 und 6 für alle Fehler, bis der elektronische Beleg erfolgreich empfangen werden kann.

## So schulen Sie den OCR-Dienst, um Fehler zu vermeiden
<a id="to-train-the-ocr-service-to-avoid-errors" class="xliff"></a>
Da OCR mit einer optischen Zeichenerkennung arbeitet, ist es wahrscheinlich, dass der OCR-Service Zeichen in Ihrem PDF oder in Bilddateien (beispielsweise bei der ersten Verarbeitung von einem bestimmten eines bestimmten Kreditor) falsch erkennt. Es interpretiert möglicherweise nicht das Firmenlogo als Name des Kreditors, oder interpretiert den Gesamtbetrag aufgrund des Layouts falsch. Um solche Fehler zukünftigt zu vermeiden, können Sie die vom OCR-Servier erhalten Daten korrigieren und ein Feedback an den Service senden.

Das Fenster **OCR-Datenkorrektur**, das Sie über das Fenster **Eingehender Beleg** öffnen, zeigt die Felder aus dem Inforegister **Finanzinformationen** in zwei Spalten an. Eine mit bearbeitungsfähigen OCR-Daten und eine mit den schreibgeschützten OCR-Daten. Wenn Sie auf die Schaltfläche **OCR-Feedback senden** klicken, wird der Inhalt des Fensters **OCR-Datenkorrektur** an den OCR-Service gesendet. Bei der nächsten Verarbeitung eines PDFs oder einer Bilddateien mit den entsprechenden Daten durch den Service werden Ihre Korrekturen dazu genutzt, die gleichen Fehler zu vermeiden.

1. In der oberen rechter Ecke wählen Sie das Symbol **Nach Seite oder Bericht suchen** aus ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen"). Geben Sie **Eingehende Dokumente** ein und wählen Sie dann den entsprechenden Link aus.
2. Öffnen Sie einen Eingangsbelegsdatensatz mit den Daten, die vom OCR-Dienst empfangen wurden und die Sie korrigieren möchten.
3. Wählen Sie im Fenster **Eingehender Beleg** die Aktion **OCR-Daten korrigieren** aus.
4. Überschreiben Sie im Fenster **OCR-Datenkorrektur** die Daten in der editierbaren Spalte für jedes Feld, das einen fehlerhaften Wert enthält.
5. Um Korrekturen rückgängig zu machen, die Sie seit dem Öffnen des Fensters **OCR-Datenkorrektur** vorgenommen haben, wählen Sie die Aktion **Reset OCR Data** aus.
6. Um die Korrekturen an den OCR-Dienst zu senden, wählen Sie die Aktion **OCR-Feedback senden** aus.
7. Um die Korrekturen zu speichern, schließen Sie das Fenster **OCR-Datenkorrektur**.

Die Felder auf dem Inforegister **Finanzinformationen** im Fenster **Eingehender Beleg** werden mit allen neuen Werten aktualisiert, die Sie in Schritt 4 eingegeben haben.

## Siehe auch
<a id="see-also" class="xliff"></a>
[Eingehende Dokumente verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

