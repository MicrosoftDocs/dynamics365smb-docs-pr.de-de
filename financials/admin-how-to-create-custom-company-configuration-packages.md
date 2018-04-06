---
title: 'Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete | Microsoft Docs'
description: "Während Ihr Unternehmen wächst, werden Sie sich wahrscheinlich mit der Zeit auf einen Satz von Mandantentypen festlegen, den Sie auf die meisten Ihrer Debitoren anwenden können. Sie können Ihren Implementierungsprozess rationalisieren, indem Sie diese Arten zu Konfigurationspaketen verarbeiten, die für die Wiederverwendung verfügbar sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 37fe7a482b88626adff1ef16496a785399d19a8d
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

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

Um eine vollständige Liste der Einrichtungstabellen zu sehen, wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Einrichten** ein. Wählen Sie dann den betreffenden Link aus.  

## <a name="to-create-a-custom-company-configuration-package"></a>Vorgehensweise: Erstellen benutzerdefinierter Unternehmenskonfigurationspakete  
1.  Erstellen Sie in der Liste eine neue [!INCLUDE[d365fin](includes/d365fin_md.md)] ***NICHT MÖGLICHER Link, um für das Erstellen eines neuen Tenants" zu helfen***.   
2.  Erstellen Sie einen neuen Mandanten für die Branchen- oder die Lösungsvorlage. Weitere Informationen zum Erstellen einer Vorlage finden Sie unter [Vorgehensweise: Ein neues Unternehmen  erstellen](admin-how-to-create-a-new-company.md).  
3.  Richten Sie den neuen Mandanten so ein, wie Sie ihn benötigen. Füllen Sie alle erforderlichen Einrichtungstabellen aus.  
4.  Öffnen des neuen Mandanten
5. Öffnen Sie das Fenster **Konfigurationsvorschlag**.  
6.  Fügen Sie die Tabellen hinzu, die Sie zu einem anderen Mandanten auf dem Arbeitsblatt übertragen möchten. Weisen Sie die Arbeitsblattzeilen dem Paket zu.  
7.  Erstellen Sie einen Fragebogen für die am häufigsten verwendeten Einrichtungstabellen.  
8.  Erstellen Sie Konfigurationsvorlagen, um es zu erleichtern, Stammdaten, beispielsweise Debitoren oder Artikel, zu erstellen.  
9.  Exportieren Sie Ihr Paket als eine .rapidstart-Datei.  

## <a name="see-also"></a>Siehe auch  
[Einrichten von Mandanten mit RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Verwaltung](admin-setup-and-administration.md)

