---
title: 'Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete | Microsoft Docs'
description: Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6fd35133d16056b947db6680cc9a76cfccaa6a3c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308074"
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

Um eine vollständige Liste von Tabellen-Einrichtungen zu sehen, wählen Sie das Symbol ![Glühlampe, mit der die Funktion Wie möchten Sie weiter verfahren geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren") und geben Sie **Manuelle Einrichtung** ein und wählen dann den zugehörigen Link aus.  

## <a name="to-create-a-custom-company-configuration-package"></a>Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete  
1.  Erstellen eines neuen Mandanten. Weitere Informationen finden Sie unter  [Neue Mandanten erstellen in Business Central](about-new-company.md).  
3.  Richten Sie den neuen Mandanten so ein, wie Sie ihn benötigen. Füllen Sie alle erforderlichen Einrichtungstabellen aus.  
4.  Öffnen des neuen Mandanten
5. Öffnen Sie das Fenster **Konfigurationsvorschlag**.  
6.  Fügen Sie die Tabellen hinzu, die Sie zu einem anderen Mandanten auf dem Arbeitsblatt übertragen möchten. Weisen Sie die Arbeitsblattzeilen dem Paket zu.  
7.  Erstellen Sie einen Fragebogen für die am häufigsten verwendeten Einrichtungstabellen.  
8.  Erstellen Sie Konfigurationsvorlagen, um es zu erleichtern, Stammdaten, beispielsweise Debitoren oder Artikel, zu erstellen.  
9.  Exportieren Sie Ihr Paket als eine .rapidstart-Datei.  

## <a name="see-also"></a>Siehe auch  
[Mandanten mit RapidStart Services einrichten](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)
