---
title: Suche nach Belegen ohne Dateianhänge| Microsoft Docs
Description: Sie können nach Sachposten für gebuchte Einkaufs- und Verkaufsbelege suchen, die keine eingehenden elektronische Belege haben, wie importierte Rechnungen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 79504010d6bb4f2afb0f09f866991dd76f6e35b5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "923694"
---
# <a name="find-posted-documents-without-incoming-document-records"></a>So finden Sie gebuchte Belege ohne zugehörige Eingangsbelege
Auf der Seiten **Kontenplan** und **Sachposten** können Sie eine Suchfunktion verwenden, um Sachposten für gebuchte Einkaufs- und Verkaufsbelege zu finden, für die keine eingehende Belegdatensätze vorhanden sind, und dann zentral eine Verknüpfung zu vorhandenen Datensätzen herstellen oder neue mit angefügten Belegdateien erstellen.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>So finden Sie gebuchte Belege ohne zugehörige Eingangsbelege
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontenplan** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie eine Zeile für ein Sachkonto aus, für dessen Sachposten Sie gebuchte Einkaufs- und Verkaufsbelege abrufen möchten, zu denen keine Eingangsbelege vorhanden sind, und wählen Sie dann die Aktion **Gebuchte Belege ohne Eingangsbeleg**.
3. Wählen Sie die Aktion **Posten** aus.
4. Wählen Sie auf der Seite **Sachposten** die Aktion **Gebuchte Belege ohne Eingangsbelege** aus.

Daraufhin wird die Seite **Gebuchte Belege ohne Eingangsbeleg** geöffnet, das die gebuchten Einkaufs- und Verkaufsbelege ohne zugehörige Eingangsbelege enthält, die von Sachposten auf dem Sachkonto dargestellt werden, für das Sie das Fenster geöffnet haben. Die Seite kann maximal 1000 Zeilen anzeigen. Standardmäßig enthält das Feld **Datumsfilter** daher einen Filter, der die Anzeige auf Einträge beschränkt, deren Buchungsdatum zwischen dem Beginn der Buchhaltungsperiode und dem Arbeitsdatum liegt.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>So verknüpfen Sie gefundene Dokumente mit vorhandenen Eingangsbelegen
1. Wählen Sie auf der Seite **Gebuchte Belege ohne Eingangsbeleg** die Zeile für einen gebuchten Beleg aus, den Sie mit einem vorhandenen Eingangsbeleg verknüpfen möchten, und wählen Sie dann die Aktion **Eingehenden Beleg auswählen** aus.
2. Wählen Sie auf der Seite **Eingehende Belege** den Eingangsbeleg aus, den Sie der gefundenen Buchung zuordnen möchten, und klicken Sie anschließend auf die Schaltfläche **OK**.
3. Auf der Seite **Gebuchte Belege ohne Eingangsbeleg** wird der gewählte Eingangsbeleg nun mit dem gebuchten Beleg verknüpft und in der Infobox **Eingehende Belegdateien** angezeigt.

Wenn die Seite **Eingehende Belege** keinen relevanten Eingangsbeleg-Datensatz enthält, können Sie einen erstellen. Weitere Informationen finden Sie unter [So geht's: Eingehende Belege erstellen](across-how-create-income-document-records.md).

## <a name="see-also"></a>Siehe auch
[Eingehende Belege verarbeiten](across-process-income-documents.md)  
[Eingehende Belege](across-income-documents.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
