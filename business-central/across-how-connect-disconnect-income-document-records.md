---
title: Erstellen von Datensätzen für eingehende Belege aus Docs
description: 'Sie können externe Geschäftsdokumente speichern, indem Sie die Dokumentdateien an die zugehörigen Datensätze für eingehende Dokumente anhängen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Erstellen und Verknüpfen von eingehenden Belegen aus Dokumenten und Posten

Sie können externe Geschäftsdokumente in [!INCLUDE[prod_short](includes/prod_short.md)] speichern, indem Sie die Dokumentdateien mit den entsprechenden eingehenden Belegen verknüpfen. Wenn das Dokument, z.B. eine Einkaufsrechnung, nicht als Datensatz für ein eingehendes Dokument erstellt wurde, können Sie auch später noch einen Datensatz für ein eingehendes Dokument erstellen und mit diesem verbinden. Sie können eingehende Belege auch an gebuchte Einkaufs- und Verkaufsbelege und an Kreditor-, Debitor- und Sachposten anfügen, indem Sie die Infobox **eingehende Belege** verwenden, zum Beispiel auf der Seite **Geb. Einkaufsrechnungen** und **Kreditorenposten**.

Auf den Seiten **Kontenplan** und **Hauptbucheinträge** können Sie eine Suchfunktion verwenden, um Hauptbucheinträge für gebuchte Kauf- und Verkaufsbelege zu finden, die keine eingehenden Datensätze haben, und diese dann zentral mit bestehenden Datensätzen verknüpfen oder neue mit angehängten Belegdateien erstellen. Weitere Informationen finden Sie unter [Gebuchte Belege ohne eingehende Belege finden](across-how-find-posted-documents-without-income-document-records.md).

Die folgenden Prozeduren zeigen, wie Sie eine Datei an ein Kreditorenposten-Sachkonto oder eine bestehende Einkaufsrechnung anhängen, die nicht aus einem Datensatz für eingehende Dokumente erstellt wurde. Das Anfügen einer Datei an gebuchte Einkaufs- oder Verkaufsdokumenten erfolgt auf ähnliche Weise.

## <a name="create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>So erstellen und verknüpfen Sie einen eingehenden Beleg anhand einer Einkaufsrechnung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Datei anhängen**.
4. Auf der Seite **Datei einfügen** wählen Sie die Datei, die den jeweiligen eingehenden Beleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.

## <a name="create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>So erstellen und verknüpfen Sie einen eingehenden Beleg aus einem Hauptbucheintrag

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kreditorenposten** ein, und wählen Sie dann den zugehörigen Link.
2. Markieren Sie eine Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten und wählen dann die Aktion **Datei anhängen**.
4. Auf der Seite **Datei einfügen** wählen Sie die Datei, die den jeweiligen eingehenden Beleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.

## <a name="remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>So entfernen Sie die Verknüpfung des eingehenden Beleges zu einem gebuchten Beleg

Sie können Dateianhänge von nicht-gebuchten Belegen jederzeit entfernen, indem Sie den entsprechenden eingehenden Beleg löschen. Wenn der Beleg gebucht ist, müssen Sie zuerst die Verknüpfung vom eingehenden Beleg entfernen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Posten für einen, mit einem gebuchten Beleg verknüpften, eingehenden Belegdatensatz aus, den Sie entfernen möchten, und wählen Sie die Aktion **Verweis auf Datensatz entfernen** aus.

Die Verbindung zum gebuchten Beleg wird entfernt. Sie können nun damit fortfahren, einen weiteren Datensatz für eingehende Dokumente mit dem gebuchten Dokument zu verbinden, wie in diesem Artikel beschrieben.

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Erstellen von Datensätzen für Eingehende Belege](across-how-create-income-document-records.md)
[Verwenden Sie OCR, um PDF- und Bilddateien in elektronische Belege zu verwandeln](across-how-use-ocr-pdf-images-files.md)
[Finden Sie gebuchte Belege ohne Datensätze für Eingehende Belege](across-how-find-posted-documents-without-income-document-records.md)
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
