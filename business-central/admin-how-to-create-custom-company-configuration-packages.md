---
title: 'Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete | Microsoft Docs'
description: Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 511281b5f4d8c7437324ed123a5a5a62bd4cc51d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783652"
---
# <a name="create-custom-company-configuration-packages"></a>Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete
Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.  

Im Allgemeinen erstellen Sie ein Konfigurationspaket pro Funktionsbereich, zum Beispiel ein Paket für Ihre Fertigungsfunktionen. Dadurch können Sie nach Bedarf neue Bereiche in einem Mandanten anwenden und einrichten.  

Ein anderer Ansatz wäre die Erstellung eines Pakets, das die Tabellen enthält, die die Einrichtung definieren, etwa wie folgt:  

-   Anlagen Einrichtung  
-   Finanzbuchhaltungs-Einrichtung:  
-   Lager Einrichtung  
-   Produktion Einrichtung  
-   Kreditoren und Einkauf Einr.  
-   Marketing & Vertrieb Einr.  
-   Service Einrichtung  
-   Debitoren und Verkauf Einr.  
-   Logistik Einrichtung  
-   Buchungsmatrix Einrichtung  
-   MwSt.-Buchungsmatrix  
-   Lagerbuchungseinrichtung  

Um eine vollständige Liste von Einrichtungstabellen zu sehen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Sie wünschen“ geöffnet wird](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Manuelle Einrichtung** ein und wählen Sie dann den zugehörigen Link aus.  

> [!IMPORTANT]
> Seien Sie vorsichtig, wenn Sie Tabellen oder Felder auswählen, die denselben zeitlichen Namen haben, sich jedoch durch Sonderzeichen wie %, &, <,>, (, und) unterscheiden. Beispielsweise kann die Tabelle „XYZ“ die Felder „Feld 1“ und „Feld 1%“ enthalten.
>
> Der XML-Prozessor akzeptiert nur einige Sonderzeichen und entfernt diejenigen, die er nicht akzeptiert. Wenn das Entfernen eines Sonderzeichens, wie z. B. des %-Zeichens in „Feld 1 %“, zu zwei oder mehr Tabellen oder Feldern mit demselben Namen führt, tritt beim Exportieren oder Importieren eines Konfigurationspakets ein Fehler auf.

## <a name="to-create-a-custom-company-configuration-package"></a>Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete  
1.  Erstellen eines neuen Mandanten. Weitere Informationen finden Sie unter [Neue Mandanten erstellen in Business Central](about-new-company.md).  
3.  Richten Sie den neuen Mandanten so ein, wie Sie ihn benötigen. Füllen Sie alle erforderlichen Einrichtungstabellen aus.  
4.  Öffnen des neuen Mandanten
5. Öffnen Sie das Fenster **Konfigurationsvorschlag**.  
6.  Fügen Sie die Tabellen hinzu, die Sie zu einem anderen Mandanten auf dem Arbeitsblatt übertragen möchten. Weisen Sie die Arbeitsblattzeilen dem Paket zu.  
7.  Erstellen Sie einen Fragebogen für die am häufigsten verwendeten Einrichtungstabellen.  
8.  Erstellen Sie Konfigurationsvorlagen, um es zu erleichtern, Stammdaten, beispielsweise Debitoren oder Artikel, zu erstellen.  
9.  Exportieren Sie Ihr Paket als eine .rapidstart-Datei.  

## <a name="see-also"></a>Siehe auch  
[Einrichten eines Unternehmens mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
