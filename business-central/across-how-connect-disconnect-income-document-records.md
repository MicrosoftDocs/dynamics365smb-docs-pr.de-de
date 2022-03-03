---
title: Erstellen von Datensätzen für eingehende Belege aus Docs
description: Sie können externe Geschäftsdokumente speichern, indem Sie die Dokumentdateien an die zugehörigen Datensätze für eingehende Dokumente anhängen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 609a57cd1d87a8a3518d6eaf7bc3fe8fc142953a
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134356"
---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Erstellen und Verknüpfen von eingehenden Belegen aus Dokumenten und Posten
Sie können externe Geschäftsdokumente in [!INCLUDE[prod_short](includes/prod_short.md)] speichern, indem Sie die Dokumentdateien mit den entsprechenden eingehenden Belegen verknüpfen. Auch wenn das Dokument, beispielsweise eine Einkaufsrechnung, ursprünglich nicht als eingehenden Beleg erfasst wurde, können Sie trotzdem später einen eingehenden Beleg erstellen und diesen zuordnen. Sie können eingehende Belege auch an gebuchte Einkaufs- und Verkaufsbelege und an Kreditor-, Debitor- und Sachposten anfügen, indem Sie die Infobox **eingehende Belege** verwenden, zum Beispiel auf der Seite **Geb. Einkaufsrechnungen** und **Kreditorenposten**.

Auf der Seiten **Kontenplan** und **Sachposten** können Sie eine Suchfunktion verwenden, um Sachposten für gebuchte Einkaufs- und Verkaufsbelege zu finden, für die keine eingehende Belege vorhanden sind, und dann zentral eine Verknüpfung zu vorhandenen Datensätzen herstellen oder neue mit angefügten Belegdateien erstellen. Weitere Informationen finden Sie unter [Gebuchte Belege ohne eingehende Belege finden](across-how-find-posted-documents-without-income-document-records.md).

Das folgende Verfahren zeigt, wie eine Datei einer vorhandenen Einkaufsrechnung beifügt wird, die nicht aus einem eingehenden Beleg erstellt wurde, und wie eine Datei einem Kreditorposten angefügt wird. Das Anfügen einer Datei an gebuchte Einkaufs- oder Verkaufsdokumenten erfolgt auf ähnliche Weise.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>So erstellen und verknüpfen Sie einen eingehenden Beleg anhand einer Einkaufsrechnung
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Datei anhängen**.
4. Auf der Seite **Datei einfügen** wählen Sie die Datei, die den jeweiligen eingehenden Beleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>So erstellen und verknüpfen Sie einen eingehenden Beleg aus einem Hauptbucheintrag
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Kreditorenposten** ein, und wählen Sie dann den zugehörigen Link.
2. Markieren Sie eine Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten und wählen dann die Aktion **Datei anhängen**.
4. Auf der Seite **Datei einfügen** wählen Sie die Datei, die den jeweiligen eingehenden Beleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>So entfernen Sie die Verknüpfung des eingehenden Beleges zu einem gebuchten Beleg
Sie können Dateianhänge von nicht-gebuchten Belegen jederzeit entfernen, indem Sie den entsprechenden eingehenden Beleg löschen. Wenn der Beleg gebucht ist, müssen Sie zuerst die Verknüpfung vom eingehenden Beleg entfernen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Eingehende Belege** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Posten für einen, mit einem gebuchten Beleg verknüpften, eingehenden Belegdatensatz aus, den Sie entfernen möchten, und wählen Sie die Aktion **Verweis auf Datensatz entfernen** aus.

Die Verbindung zum gebuchten Beleg wird entfernt. Sie können nun einen anderen eingehenden Beleg mit dem gebuchten Beleg verknüpfen, wie in diesem Thema beschrieben.

## <a name="see-also"></a>Siehe auch
[Eingehende Belege verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]