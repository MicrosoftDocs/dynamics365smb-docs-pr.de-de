---
title: 'Vorgehensweise: Erstellen von Serviceartikeln | Microsoft Docs'
description: Wenn Sie einen Serviceartikel für Servicearbeiten empfangen, der nicht erfasst ist, kann dieser als Serviceartikel angelegt werden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 265b1e916894b588f296f3737cda04c685734d47
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194907"
---
# <a name="create-service-items"></a>Serviceartikel erstellen
In [!INCLUDE[d365fin](includes/d365fin_md.md)], berücksichtigt der Begriff "Serviceartikel" Lagerhilfsmittel oder Artikel, die Service benötigen. Wenn Sie einen Serviceauftrag erstellen, geben Sie den Artikeln die Anforderungsdienst an. Im Verkaufsauftrag können Sie einen Serviceartikel für einen Artikel im Lagerbestand oder in einer Serviceartikelgruppe verknüpfen.    

Wenn Sie einen Serviceartikel für Servicearbeiten empfangen, der nicht erfasst ist, kann dieser als Serviceartikel angelegt werden. Es gibt mehrere Möglichkeiten dazu: Beispielsweise können Sie einen Serviceartikel unter **Serviceartikel** oder als Teil eines anderen Prozesses erstellen, etwa bei der Arbeit mit einem Serviceauftrag.   

## <a name="to-create-a-service-item"></a>So erstellen Sie einen Serviceartikel  
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceartikel** ein und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>So erstellen Sie Serviceartikel in Serviceaufträgen  
Wenn Sie Artikel für Servicearbeiten erhalten, können Sie diese als Serviceartikel auf der Seite **Serviceauftrag** oder **Serviceangebot** anlegen.  

1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Serviceaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie die Aktion **Serviceartikel erstellen**.  

    Eine Nummer wird dem Serviceartikel zugeordnet und eine Serviceartikelkarte wird erstellt. Das Feld **Serviceartikelnr.** wird mit der Nummer des neuen Serviceartikels ausgefüllt.

## <a name="to-create-a-service-item-when-shipping-items"></a>So erstellen Sie Serviceartikel bei Artikellieferungen  
Wenn Sie Artikel liefern, indem Sie entweder Verkaufsaufträge oder Verkaufsrechnungen buchen, werden die gelieferten Artikel unter folgender Bedingung automatisch als Serviceartikel erfasst. Die Artikel müssen zu einer Serviceartikelgruppe mit aktiviertem Kontrollkästchen **Serviceartikel erstellen** gehören. Wenn die Artikel über auf der Seite "Artikelverfolgungszeilen" erfasste Seriennummern verfügen, werden diese Informationen beim Erstellen der Serviceartikel automatisch in das Feld **Seriennr.** der Serviceartikelkarte kopiert.  

Im folgenden Verfahren wird gezeigt, wie bei Artikellieferungen in Verkaufsaufträgen Serviceartikel erstellt werden.  

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol öffnet, geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den entsprechenden Verkaufsauftrag.  
3. Wählen Sie die Aktion **Buchen** oder **Buchen und drucken** aus.  
4. Wählen Sie **Warenausgang** oder die **Liefern und fakturieren** Aktion aus.  
5. Es werden automatisch Serviceartikel für die Artikel im Auftrag erstellt, sofern diese einer Serviceartikelgruppe angehören, die zum Erstellen von Serviceartikeln eingerichtet wurde. Wenn auf der Seite **Artikelverfolgungszeilen** spezielle Seriennummern erfasst wurden, werden diese den Serviceartikeln zugeordnet.  

> [!NOTE]  
>  Wenn es sich bei dem Artikel um eine Stückliste handelt und die Stückliste entfaltet wurde, werden die entfalteten Stücklistenartikel wie normale Artikel behandelt. Serviceartikel werden gemäß der Bedingung für Serviceartikelgruppen und optional gemäß der Bedingung für Seriennummern erstellt. Weiterhin werden diese Artikel, wenn ein Serviceartikel für einen entfalteten Stücklistenartikel erstellt wird, der aus anderen Stücklistenkomponenten besteht, als Serviceartikelkomponenten für den entfalteten Stücklistenserviceartikel erstellt.  
>   
>  Wenn es sich bei dem Artikel um eine nicht entfaltete Stückliste handelt, wird ein Serviceartikel gemäß der Bedingung für Serviceartikelgruppen und optional gemäß der Bedingung für Seriennummern erstellt.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>So fügen Sie die Grundgebühr für einen Serviceartikel ein
1. Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Serviceaufgaben** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Artikel-Arbeitsblatt** aus.
3. Wählen Sie auf dem Inforegister Zeilen die relevante **Aktion** aus, und wählen Sie dann **Funktinone**und dann **Grundgebühr** einfügen.  

    Eine Servicezeile der Art **Kosten** wird mit der Grundgebühr eingefügt. Die Grundgebühr bezieht sich auf den ausgewählten Serviceartikel.

## <a name="see-also"></a>Siehe auch  
[Richten Sie Serviceartikel und Serviceartikelkomponenten ein.](service-how-setup-service-items.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Service](service-service.md)  
