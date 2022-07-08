---
title: So finden Sie gebuchte Belege ohne eingehende Belege
description: Sie können nach Hauptbuchhaltungsposten für gebuchte Einkaufs- und Verkaufsrechnungen suchen, für die es keine elektronischen Belege gibt, wie z.B. importierte Rechnungen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/14/2022
ms.author: edupont
ms.openlocfilehash: ad50260df068d38cb8266e04434eb4faf4d052f3
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076045"
---
# <a name="find-posted-documents-without-incoming-document-records"></a>So finden Sie gebuchte Belege ohne zugehörige eingehende Belege

Auf den Seiten **Kontenplan** und **Hauptbucheinträge** können Sie eine Suchfunktion verwenden, um Hauptbucheinträge für gebuchte Kauf- und Verkaufsbelege zu finden, die keine eingehenden Datensätze haben, und diese dann zentral mit bestehenden Datensätzen verknüpfen oder neue mit angehängten Belegdateien erstellen.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>So finden Sie gebuchte Belege ohne zugehörige eingehende Belege

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie eine Zeile für ein Sachkonto aus, für dessen Sachposten Sie gebuchte Einkaufs- und Verkaufsbelege abrufen möchten, zu denen keine eingehenden Belege vorhanden sind, und wählen Sie dann die Aktion **Gebuchte Belege ohne eingehenden Beleg**.
3. Wählen Sie die Aktion **Posten** aus.
4. Wählen Sie auf der Seite **Sachposten** die Aktion **Gebuchte Belege ohne eingehende Belege** aus.

Daraufhin wird die Seite **Gebuchte Belege ohne eingehenden Beleg** geöffnet, das die gebuchten Einkaufs- und Verkaufsbelege ohne zugehörige eingehende Belege enthält, die von Sachposten auf dem Sachkonto dargestellt werden, für das Sie das Fenster geöffnet haben. Die Seite kann maximal 1000 Zeilen anzeigen. Standardmäßig enthält das Feld **Datumsfilter** daher einen Filter, der die Anzeige auf Einträge beschränkt, deren Buchungsdatum zwischen dem Beginn der Buchhaltungsperiode und dem Arbeitsdatum liegt.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>So verknüpfen Sie gefundene Dokumente mit vorhandenen eingehenden Belegen

1. Wählen Sie auf der Seite **Gebuchte Belege ohne eingehenden Beleg** die Zeile für einen gebuchten Beleg aus, den Sie mit einem vorhandenen eingehenden Beleg verknüpfen möchten, und wählen Sie dann die Aktion **Eingehenden Beleg auswählen** aus.
2. Wählen Sie auf der Seite **Eingehende Belege** den eingehenden Beleg aus, den Sie der gefundenen Buchung zuordnen möchten, und klicken Sie anschließend auf die Schaltfläche **OK**.
3. Auf der Seite **Gebuchte Belege ohne eingehenden Beleg** wird der gewählte eingehende Beleg nun mit dem gebuchten Beleg verknüpft und in der Infobox **Eingehender Beleg** angezeigt.

Wenn auf der Seite **Eingehende Belege** kein entsprechender Datensatz vorhanden ist, können Sie ihn erstellen. Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).

## <a name="see-related-training-at-microsoft-learn"></a>Siehe zugehörige Schulung unter [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Siehe auch

[Erstellen von Datensätzen für eingehende Belege](across-how-create-income-document-records.md)
[Verwenden Sie OCR, um PDF- und Bilddateien in elektronische Belege zu verwandeln](across-how-use-ocr-pdf-images-files.md)
[Erstellen Sie Datensätze für eingehende Belege direkt aus Dokumenten und Einträgen](across-how-connect-disconnect-income-document-records.md)
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]