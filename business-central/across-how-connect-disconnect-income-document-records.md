---
title: Erstellen von Datensätzen für eingehende Belege aus Docs
description: 'Sie können externe Geschäftsdokumente speichern, indem Sie die Dokumentdateien an die zugehörigen Datensätze für eingehende Dokumente anhängen.'
author: jswymer
ms.topic: how-to
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 02/23/2023
ms.author: jswymer
ms.reviewer: jswymer
ms-service: dynamics-365-business-central
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Datensätze für eingehende Belege aus Belegen und Posten direkt erstellen

Sie können externe Geschäftsdokumente in [!INCLUDE[prod_short](includes/prod_short.md)] speichern, indem Sie die Dokumentdateien mit den entsprechenden eingehenden Belegen verknüpfen. Wenn das Dokument, z.B. eine Einkaufsrechnung, nicht als Datensatz für ein eingehendes Dokument erstellt wurde, können Sie auch später noch einen Datensatz für ein eingehendes Dokument erstellen und mit diesem verbinden. Sie können eingehende Belege auch an gebuchte Einkaufs- und Verkaufsbelege und an Kreditor-, Debitor- und Sachposten anfügen, indem Sie die Infobox **eingehende Belege** verwenden, zum Beispiel auf der Seite **Geb. Einkaufsrechnungen** und **Kreditorenposten**.

Auf den Seiten **Kontenplan** und **Hauptbucheinträge** können Sie eine Suchfunktion verwenden, um Hauptbucheinträge für gebuchte Kauf- und Verkaufsbelege zu finden, die keine eingehenden Datensätze haben, und diese dann zentral mit bestehenden Datensätzen verknüpfen oder neue mit angehängten Belegdateien erstellen. Weitere Informationen finden Sie unter [Gebuchte Belege ohne eingehende Belege finden](across-how-find-posted-documents-without-income-document-records.md).

Die folgenden Prozeduren zeigen, wie Sie eine Datei an ein Kreditorenposten-Sachkonto oder eine bestehende Einkaufsrechnung anhängen, die nicht aus einem Datensatz für eingehende Dokumente erstellt wurde. Das Anfügen einer Datei an gebuchte Einkaufs- oder Verkaufsdokumenten erfolgt auf ähnliche Weise.

## <a name="create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>Einen Datensatz für einen eingehenden Beleg anhand einer Einkaufsrechnung erstellen und verknüpfen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Datei anhängen**.
4. Auf der Seite **Datei einfügen** führen Sie einen der folgenden Schritte aus, um eine Datei anzufügen, die den jeweiligen eingehenden Beleg darstellt:

   [!INCLUDE[file-upload](includes/file-upload.md)]


## <a name="create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>Einen Datensatz für einen eingehenden Beleg aus einem Kreditorenposten erstellen und verknüpfen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kreditorenposten** ein, und wählen Sie dann den zugehörigen Link.
2. Markieren Sie eine Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten und wählen dann die Aktion **Datei anhängen**.
4. Auf der Seite **Datei einfügen** führen Sie einen der folgenden Schritte aus, um eine Datei anzufügen, die den jeweiligen eingehenden Beleg darstellt:

   [!INCLUDE[file-upload](includes/file-upload.md)]


## <a name="remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>Eine Verknüpfung von einem Datensatz für einen eingehenden Beleg zu einem gebuchten Beleg entfernen

Sie können Dateianhänge von nicht-gebuchten Belegen jederzeit entfernen, indem Sie den entsprechenden eingehenden Beleg löschen. Wenn der Beleg gebucht ist, müssen Sie zuerst die Verknüpfung vom eingehenden Beleg entfernen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Posten für einen, mit einem gebuchten Beleg verknüpften, eingehenden Belegdatensatz aus, den Sie entfernen möchten, und wählen Sie die Aktion **Verweis auf Datensatz entfernen** aus.

Die Verbindung zum gebuchten Beleg wird entfernt. Sie können nun damit fortfahren, einen weiteren Datensatz für eingehende Dokumente mit dem gebuchten Dokument zu verbinden, wie in diesem Artikel beschrieben.

## <a name="see-also"></a>Siehe auch

[Erstellen von Datensätzen für Eingehende Belege](across-how-create-income-document-records.md)
[Verwenden Sie OCR, um PDF- und Bilddateien in elektronische Belege zu verwandeln](across-how-use-ocr-pdf-images-files.md)
[Finden Sie gebuchte Belege ohne Datensätze für Eingehende Belege](across-how-find-posted-documents-without-income-document-records.md)
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
