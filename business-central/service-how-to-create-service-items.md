---
title: 'Vorgehensweise: Erstellen von Serviceartikeln | Microsoft Docs'
description: "Wenn Sie einen Serviceartikel für Servicearbeiten empfangen, der nicht erfasst ist, kann dieser als Serviceartikel angelegt werden."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0e251cd1aa071484cbf235feee6f0e891f27020e
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="create-service-items"></a>Serviceartikel erstellen
In [!INCLUDE[d365fin](includes/d365fin_md.md)], berücksichtigt der Begriff "Serviceartikel" Lagerhilfsmittel oder Artikel, die Service benötigen. Wenn Sie einen Serviceauftrag erstellen, geben Sie den Artikeln die Anforderungsdienst an. Im Verkaufsauftrag können Sie einen Serviceartikel für einen Artikel im Lagerbestand oder in einer Serviceartikelgruppe verknüpfen.    

Wenn Sie einen Serviceartikel für Servicearbeiten empfangen, der nicht erfasst ist, kann dieser als Serviceartikel angelegt werden. Es gibt mehrere Möglichkeiten dazu: Beispielsweise können Sie einen Serviceartikel unter **Serviceartikel** oder als Teil eines anderen Prozesses erstellen, etwa bei der Arbeit mit einem Serviceauftrag.   

## <a name="to-create-a-service-item"></a>So erstellen Sie einen Serviceartikel  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceartikel** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>So erstellen Sie Serviceartikel in Serviceaufträgen  
Wenn Sie Artikel für Servicearbeiten erhalten, können Sie diese als Serviceartikel im Fenster **Serviceauftrag** oder **Serviceangebot** anlegen.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Aktion **Serviceartikel erstellen**.  

    Eine Nummer wird dem Serviceartikel zugeordnet und eine Serviceartikelkarte wird erstellt. Das Feld **Serviceartikelnr.** wird mit der Nummer des neuen Serviceartikels ausgefüllt.

## <a name="to-create-a-service-item-when-shipping-items"></a>So erstellen Sie Serviceartikel bei Artikellieferungen  
Wenn Sie Artikel liefern, indem Sie entweder Serviceaufträge oder Servicerechnungen buchen, werden die gelieferten Artikel unter folgender Bedingung automatisch als Serviceartikel erfasst. Die Artikel müssen zu einer Serviceartikelgruppe mit aktiviertem Kontrollkästchen **Serviceartikel erstellen** gehören. Wenn die Artikel über im Fenster "Artikelverfolgungszeilen" erfasste Seriennummern verfügen, werden diese Informationen beim Erstellen der Serviceartikel automatisch in das Feld **Seriennr.** der Serviceartikelkarte kopiert.  

Im folgenden Verfahren wird gezeigt, wie bei Artikellieferungen Serviceartikel in Serviceaufträgen erstellt werden.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Öffnen Sie den relevanten Serviceauftrag.  
3. Wählen Sie die Aktion **Buchen** oder **Buchen und drucken** aus.  
4. Wählen Sie **Warenausgang** oder die **Liefern und fakturieren** Aktion aus.  
5. Es werden automatisch Serviceartikel für die Artikel im Auftrag erstellt, sofern diese einer Serviceartikelgruppe angehören, die zum Erstellen von Serviceartikeln eingerichtet wurde. Wenn im Fenster **Artikelverfolgungszeilen** spezielle Seriennummern erfasst wurden, werden diese den Serviceartikeln entsprechend zugeordnet.  

> [!NOTE]  
>  Wenn es sich bei dem Artikel um eine Stückliste handelt und die Stückliste entfaltet wurde, werden die entfalteten Stücklistenartikel wie normale Artikel behandelt. Serviceartikel werden gemäß der Bedingung für Serviceartikelgruppen und optional gemäß der Bedingung für Seriennummern erstellt. Weiterhin werden diese Artikel, wenn ein Serviceartikel für einen entfalteten Stücklistenartikel erstellt wird, der aus anderen Stücklistenkomponenten besteht, als Serviceartikelkomponenten für den entfalteten Stücklistenserviceartikel erstellt.  
>   
>  Wenn es sich bei dem Artikel um eine nicht entfaltete Stückliste handelt, wird ein Serviceartikel gemäß der Bedingung für Serviceartikelgruppen und optional gemäß der Bedingung für Seriennummern erstellt.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>So fügen Sie die Grundgebühr für einen Serviceartikel ein
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceaufgaben** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Artikel-Arbeitsblatt** aus.
3. Wählen Sie auf dem Inforegister Zeilen die relevante **Aktion** aus, und wählen Sie dann **Funktinone**und dann **Grundgebühr** einfügen.  

    Eine Servicezeile der Art **Kosten** wird mit der Grundgebühr eingefügt. Die Grundgebühr bezieht sich auf den ausgewählten Serviceartikel.

## <a name="see-also"></a>Siehe auch  
[Richten Sie Serviceartikel und Serviceartikelkomponenten ein.](service-how-setup-service-items.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Service](service-service.md)  

