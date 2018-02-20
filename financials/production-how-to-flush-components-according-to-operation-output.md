---
title: "Vorgehensweise: Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren | Microsoft Docs"
description: "Für Artikel, die mit der Rückwärtsbuchungsmethode erstellt wurden, ist das Standardverhalten, Komponentenverbrauch zu berechnen und zu buchen, wenn Sie den Status eines freigegebenen Fertigungsauftrags in **Erledigt** ändern. Weitere Informationen finden Sie unter Entnahmemethoden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f61e3150f1978795a20d4ad68656d6d1e72402a0
ms.contentlocale: de-de
ms.lasthandoff: 01/30/2018

---
# <a name="flush-components-according-to-operation-output"></a>Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren
Für Artikel, die mit der Rückwärtsbuchungsmethode erstellt wurden, ist das Standardverhalten, Komponentenverbrauch zu berechnen und zu buchen, wenn Sie den Status eines freigegebenen Fertigungsauftrags in **Erledigt** ändern.  

Wenn Sie auch Verbindungscodes definieren, dann erfolgt die Berechnung und Buchung, wenn jeder Arbeitsgang beendet ist, und die Menge, die tatsächlich im Arbeitsgang verbraucht wurde, wird gebucht. Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).  

Wenn beispielsweise ein Fertigungsauftrag, 800 Meter zu produzieren, 8 Kilogramm einer Komponente benötigt, dann werden, wenn Sie 200 Meter buchen, wie ausgegeben, 2 Kilogramm automatisch als Verbrauch gebucht.  

Diese Funktionalität ist aus folgenden Ursachen nützlich:  

-   **Bestandsbewertung** - Wertposten für Istmeldungen und Verbräuche werden beim Fortschritt des Fertigungsauftrags erstellt. Ohne Verbindungscodes erhöht sich der Lagerwert, wenn Ausstoß registriert wird, und vermindert sich später, wenn der Wert des Komponentenverbrauchs zusammen mit dem beendeten FA gebucht wird.  
-   **Bestandsverfügbarkeit** - mit allmählicher Verbrauchsbuchung, wird die Verfügbarkeit von Komponenten aktueller, was wichtig ist, um die interne Balance zwischen Bedarf und Vorrat aufrechtzuerhalten. Ohne Verbindungscodenummern glauben möglicherweise andere, die Bedarf für die Komponente haben, dass sie verfügbar ist, solange eine verzögerte Verbrauchsbuchung dafür aussteht.  
-   **Just-In-Time** - mit der Möglichkeit, Produkte an Debitorenanfragen anzupassen, können Sie Abfall minimieren, indem Sie sicherstellen, dass Arbeits- und Systemänderungen nur eintreten, wenn es erforderlich ist.  

Im folgenden Verfahren wird gezeigt, wie Rückwärtsbuchen und die Verbindungscodes kombiniert werden, sodass die Menge, die je Arbeitsgang geleert wird, zur aktuellen Isteffektivität des abgeschlossenen Arbeitsgangs proportional ist.  

## <a name="to-flush-components-according-to-operation-output"></a>Komponenten entsprechend dem Arbeitsgangs-Ausstoß leeren  
1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") aus und geben Sie **Artikel** ein. Wählen Sie dann den zugehörigen Link aus.  
2.  Wählen Sie die Aktion **Bearbeiten** aus.  
3.  Wählen Sie im Inforegister **Beschaffung** im Feld **Buchungsmethode** die Option **Vorwärts** aus.  

    > [!NOTE]  
    >  Wählen Sie **Kommiss. + Vorwärts** aus, wenn die Komponente in einem Lagerplatz verwendet wird, der für die gesteuerte Einlagerung und Kommissionierung eingerichtet ist.  

4.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Arbeitspläne** ein. Wählen Sie dann den zugehörigen Link aus.  
5.  Definieren Sie Verbindungscodes für jeden Arbeitsgang, der die Komponente verbraucht. Weitere Informationen finden Sie unter [Arbeitspläne erstellen](production-how-to-create-routings.md).  
6.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Fertigungsstücklisten** ein. Wählen Sie dann den zugehörigen Link aus.  
7.  Definieren Sie Verbindungscodes von jeder Instanz der Komponente zu dem Arbeitsgang, in dem sie verbraucht wird.

    > [!IMPORTANT]  
    >  Die Komponente muss eine Verbindung zum letzten Arbeitsgang im Arbeitsplan haben.  

## <a name="see-also"></a>Siehe auch  
[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planung](production-planning.md)   
[Lagerbest](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

