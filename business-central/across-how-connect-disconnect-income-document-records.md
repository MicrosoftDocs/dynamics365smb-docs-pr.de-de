---
title: Eingehende Dokumente von Dokumenten erstellen| Microsoft Docs
description: "Sie finden hier Datensätze aus eingehenden Belege, wie Erechnungen erstellen und verwalten OCRaufgaben, elektronische Geschäftsverkehr und Belegaustausch."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d5d7e672488139dfba2d3056d1d44941594c2a12
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="create-incoming-document-records-directly-from-documents-and-entries"></a>Erstellen und Verknüpfen von Eingangsbelegen aus Dokumenten und Posten
Sie können externe Geschäftsdokumente in [!INCLUDE[d365fin](includes/d365fin_md.md)] speichern, indem Sie die Dokumentdateien mit den entsprechenden Eingangsbelegen verknüpfen. Auch wenn das Dokument, beispielsweise eine Einkaufsrechnung, ursprünglich nicht als Eingangsbeleg erfasst wurde, können Sie trotzdem später einen Eingangsbeleg erstellen und diesen zuordnen. Sie können Eingangsbelegdateien auch an gebuchte Einkaufs- und Verkaufsbelege und an Kreditor-, Debitor- und Sachposten anfügen, indem Sie die Infobox **Eingangsbelegdateien** verwenden, zum Beispiel in den Fenstern **Geb. Einkaufsrechnungen** und **Kreditorenposten**.

In den Fenstern **Kontenplan** und **Sachposten** können Sie eine Suchfunktion verwenden, um Sachposten für gebuchte Einkaufs- und Verkaufsbelege zu finden, für die keine eingehende Belegdatensätze vorhanden sind, und dann zentral eine Verknüpfung zu vorhandenen Datensätzen herstellen oder neue mit angefügten Belegdateien erstellen. Weitere Informationen finden Sie unter [Gebuchte Belege ohne Eingangsbelege finden](across-how-find-posted-documents-without-income-document-records.md).

Das folgende Verfahren zeigt, wie eine Datei einer vorhandenen Einkaufsrechnung beifügt wird, die nicht aus einem Eingangsbeleg erstellt wurde, und wie eine Datei einem Kreditorposten angefügt wird. Das Anfügen einer Datei an gebuchte Einkaufs- oder Verkaufsdokumenten erfolgt auf ähnliche Weise.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-purchase-invoice"></a>So erstellen und verknüpfen Sie einen Eingangsbeleg anhand einer Einkaufsrechnung
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kaufrechnung** ein, und wählen dann den zugehörigen Link aus.
2. Markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für eine Einkaufsrechnung, der Sie eine Datei anfügen möchten, und wählen dann die Aktion **Datei anhängen**.
4. Im **Datei einfügen**-Fenster wählen Sie die Datei, die den jeweiligen Eingangsbeleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.

## <a name="to-create-and-connect-an-incoming-document-record-from-a-vendor-ledger-entry"></a>So erstellen und verknüpfen Sie einen Eingangsbeleg aus einem Hauptbucheintrag
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Verkäufer-Buchungseinträge** ein, und wählen dann den zugehörigen Link aus.
2. Markieren Sie eine Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten, und wählen dann die Aktion **Eingehenden Beleg aus Datei erstellen**.
3. Alternativ markieren Sie die Zeile für einen Kreditorenposten, dem Sie eine Datei anfügen möchten und wählen dann die Aktion **Datei anhängen**.
4. Im **Datei einfügen**-Fenster wählen Sie die Datei, die den jeweiligen Eingangsbeleg darstellt, und wählen Sie die Schaltfläche **Öffnen**.

## <a name="to-remove-a-connection-from-an-incoming-document-record-to-a-posted-document"></a>So entfernen Sie die Verknüpfung des Eingangsbeleges zu einem gebuchten Beleg
Sie können Dateianhänge von nicht-gebuchten Belegen jederzeit entfernen, indem Sie den entsprechenden Eingangsbeleg löschen. Wenn der Beleg gebucht ist, müssen Sie zuerst die Verknüpfung vom Eingangsbeleg entfernen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Eingehende Dokumente** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie den Posten für einen, mit einem gebuchten Beleg verknüpften, eingehenden Belegdatensatz aus, den Sie entfernen möchten, und wählen Sie die Aktion **Verweis auf Datensatz entfernen** aus.

Die Verbindung zum gebuchten Beleg wird entfernt. Sie können nun einen anderen Eingangsbeleg mit dem gebuchten Beleg verknüpfen, wie in diesem Thema beschrieben.

## <a name="see-also"></a>Siehe auch
[Eingehende Dokumente verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

