---
title: Eingehende Dokumente von Dokumenten erstellen| Microsoft Docs
description: "Sie finden hier Datensätze aus eingehenden Belege, wie Erechnungen erstellen und verwalten OCRaufgaben, elektronische Geschäftsverkehr und Belegaustausch."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 44105a8bf043795d60ecab135c6a8b61712b4f60
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-incoming-document-records-directly-from-documents-and-entries"></a>So wird's gemacht: Erstellen und Verknüpfen von Eingangsbelegen aus Dokumenten und Posten
Sie können externe Geschäftsdokumente in [!INCLUDE[d365fin](includes/d365fin_md.md)] speichern, indem Sie die Dokumentdateien mit den entsprechenden Eingangsbelegen verknüpfen. Auch wenn das Dokument, beispielsweise eine Einkaufsrechnung, ursprünglich nicht als Eingangsbeleg erfasst wurde, können Sie trotzdem später einen Eingangsbeleg erstellen und diesen zuordnen. Sie können Eingangsbelegdateien auch an gebuchte Einkaufs- und Verkaufsbelege und an Kreditor-, Debitor- und Sachposten anfügen, indem Sie die Infobox **Eingangsbelegdateien** verwenden, zum Beispiel in den Fenstern **Geb. Einkaufsrechnungen** und **Kreditorenposten**.

In den Fenstern **Kontenplan** und **Sachposten** können Sie eine Suchfunktion verwenden, um Sachposten für gebuchte Einkaufs- und Verkaufsbelege zu finden, für die keine eingehende Belegdatensätze vorhanden sind, und dann zentral eine Verknüpfung zu vorhandenen Datensätzen herstellen oder neue mit angefügten Belegdateien erstellen. Weitere Informationen finden Sie unter [So gehts: Gebuchte Belege ohne Eingangsbelege finden](across-how-find-posted-documents-without-income-document-records.md).

Das folgende Verfahren zeigt, wie eine Datei einer vorhandenen Einkaufsrechnung beifügt wird, die nicht aus einem Eingangsbeleg erstellt wurde, und wie eine Datei einem Kreditorposten angefügt wird. Das Anfügen einer Datei an gebuchte Einkaufs- oder Verkaufsdokumenten erfolgt auf ähnliche Weise.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>So erstellen und verknüpfen Sie einen Eingangsbeleg anhand einer Einkaufsrechnung
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Datei anhängen**.
4. Im **Datei einfügen**-Fenster wählen Sie die Datei, die den jeweiligen Eingangsbeleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>So erstellen und verknüpfen Sie einen Eingangsbeleg aus einem Hauptbucheintrag
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Finanzbuchhaltung einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Markieren Sie eine Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten und wählen dann die Aktion **Datei anhängen**.
4. Im **Datei einfügen**-Fenster wählen Sie die Datei, die den jeweiligen Eingangsbeleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>So entfernen Sie die Verknüpfung des Eingangsbeleges zu einem gebuchten Beleg
Sie können Dateianhänge von nicht-gebuchten Belegen jederzeit entfernen, indem Sie den entsprechenden Eingangsbeleg löschen. Wenn der Beleg gebucht ist, müssen Sie zuerst die Verknüpfung vom Eingangsbeleg entfernen.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Gebuchte Einkaufsrechnungen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie den Posten für einen, mit einem gebuchten Beleg verknüpften, eingehenden Belegdatensatz aus, den Sie entfernen möchten, und wählen Sie die Aktion **Verweis auf Datensatz entfernen** aus.

Die Verbindung zum gebuchten Beleg wird entfernt. Sie können nun einen anderen Eingangsbeleg mit dem gebuchten Beleg verknüpfen, wie in diesem Thema beschrieben.

## <a name="see-also"></a>Siehe auch
[Eingehende Dokumente verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

