---
title: 'Vorgehensweise: Umlagern von Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen | Microsoft Docs'
description: "Wenn die Arbeitsgänge, die den Artikel verarbeiten, an Ihrem Lagerort stattfinden, müssen Sie möglicherweise Artikel zwischen internen Lagerplätzen umlagern, um auf interne Herkunftsbelege, wie Produktions-, Montage- oder Serviceaufträge am Lagerort zu reagieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 146e113931384e8bc9ba01d5ae7ddb626d18050f
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>Vorgehensweise: Umlagern von Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen
Wenn die Arbeitsgänge, die den Artikel verarbeiten, an Ihrem Lagerort stattfinden, müssen Sie möglicherweise Artikel zwischen internen Lagerplätzen umlagern, um auf interne Herkunftsbelege, wie Produktions-, Montage- oder Serviceaufträge am Lagerort zu reagieren.  

> [!NOTE]  
>  Weitere Informationen zum Umlagern von Artikeln ohne Herkunftsbelege finden Sie unter Interne Umlagerung.  

In erweiterten Lagerkonfigurationen, in denen Lagerplätze das Einrichtungsfeld **Gesteuerte Einlag. u. Kommiss.** verwenden, können Sie das Fenster **Lagerplatzumlagerungsvorschlag** verwenden, um die Artikel zwischen Lagerplätzen umzulagern. Weitere Informationen finden Sie unter [Vorgehensweise: Umlagerung von Artikeln in erweiterten Lagerkonfigurationen](warehouse-how-to-move-items-in-advanced-warehousing.md).  

In den Basislagerkonfigurationen, in denen Lagerplätze das Einrichtungsfeld **Lagerplatz notwendig** und das Einrichtungsfeld **Kommissionierung erforderlich** verwenden , können Umlagerungen von Artikeln an interne Vorgangsbereiche basierend auf internen Herkunftsbelegen auf die folgenden Arten gebucht werden:  

-   Im Fenster **Lagerbestandsumlagerung**.  
-   Mit dem Fenster **Lagerkommissionierung**.  

> [!NOTE]  
>  Lagerkommissionierungen buchen auch negative Artikelposten als Verbrauch und werden nur für Produktionskomponenten unterstützt. Weitere Informationen finden Sie im Fenster Arbeitsblatt Auslieferung.  

Ausführliche Informationen zu Lagerbestandsumlagerungen finden Sie im Fenster Lagerbestandsumlagerung  

Zwei verschiedene Rollen können die erste Lagerbestandsumlagerung erstellen. Ein Montagearbeiter kann diese beispielsweise aus einem freigegebenen Montageauftrag erstellen, sodass diese in der Liste der offenen Arbeiten des Lagermitarbeiters angezeigt wird. Um eine Lagerbestandsumlagerung für Montageauftragszeilen zu erstellen, die bereit sind, dass Komponenten in ihre festgelegten Lagerplätze umgelagert werden, verwendet der Montagearbeiter die Funktion **Lagerbestandsumlagerung erstellen**.  

Alternativ kann ein Lagermitarbeiter diese erstellen, indem er auf den freigegebenen Montageauftrag verweist. Dies wird im folgender Verfahren beschrieben.  

> [!NOTE]  
>  Wenn die Umlagerung für einen Montageauftrag erfolgt, in dem der Artikel für einen Auftrag montiert wird, dann können Sie festlegen, dass der Lagerbestandsumlagerungsbeleg automatische erstellt wird, wenn Sie den Lagerkommissionierungsbeleg für den fertigen Montageartikel erstellen, der die Lieferung bucht. Um dies einzurichten, wählen Sie das Feld **Umlagerungen automatisch erstellen** im Fenster **Montageeinrichtung** aus  
>   
>  Weitere Informationen zu Montageaufträgen und Basis-Lagerkonfigurationen, finden Sie unter [Vorgehensweise: Verarbeiten von Auftragsmontageartikeln Lagerkommissionierungen](warehouse-how-to-pick-for-production.md).  

Im folgenden Verfahren wird beschrieben, wie eine Lagerbestandsumlagerung aus dem Fenster **Lagerbestandsumlagerung** durch das Verweisen auf einen freigegebenen Montageauftrag als Herkunftsbeleg erstellt wird. Dieser Vorgang ist derselbe, wenn Sie Komponenten für Fertigungsaufträge und Serviceaufträge umlagern.  

## <a name="to-move-components-to-an-operation-area-in-basic-warehouse-configurations"></a>So lagern Sie Komponenten in einen Arbeitsgangbereich in Basis-Lagerkonfigurationen um  
1.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerbestandsumlagerung** ein. Wählen Sie dann den relevanten Link aus.  
2.  Füllen Sie auf dem Inforegister **Allgemein** das Feld **Nr.** aus. Feld Sie können die EINGABETASTE betätigen, um in den Nummernserien eine Auswahl zu treffen.  
3.  Geben Sie im Feld **Lagerortcode** den Lagerort ein, an dem die Umlagerung stattfindet.  
4.  Wählen Sie die **Herkunftsbelege holen** Aktion aus. Füllen Sie alternativ das Feld **Herkunftsbeleg** aus, und klicken Sie anschließend auf die Schaltfläche **AssistEdit** im Feld **Herkunftsnr.**.  
5.  Wählen Sie im Fenster **Herkunftsbelege** den Montageauftrag aus, für den Sie Komponenten umlagern möchten, und klicken Sie anschließend auf die Schaltfläche **OK**.  

    Für alle erforderlichen Komponenten, die umgelagert werden können, werden im Fenster **Lagerbestandsumlagerungen** eine Entnahme- und eine Einlagerungszeile generiert. Alle Felder mit Ausnahme des Felds **Bewegungsmenge** werden entsprechend den Herkunftsbelegzeilen vorbelegt. Das Feld **Bewegungsmenge** weist Null aus, bis Sie die Menge angeben, die Sie tatsächlich umgelagert haben.  

    Sie können den Lagerplatzcode in einer Entnahmezeile aber nur entsprechend der Verfügbarkeit ändern. Wenn Sie in einer Entnahmezeile die Schaltfläche **AssistEdit** im Feld **Lagerplatzcode** auswählen, wird das Fenster **Lagerplatzinhalt** geöffnet und zeigt nur Lagerplätze an, an denen die Komponente verfügbar ist.  

    Sie können den Lagerplatzcode in einer Einlagerungszeile nicht ändern. Nur der Lagerplatzcode, der in der Komponentenzeile des Herkunftsbelegs definiert ist, wird angenommen. Dies unterstützt das Prinzip, dass die Rolle, die eine Komponente anfordert, hier ein Montagearbeiter, weiß, wo die Komponente platziert werden muss. Wenn Sie die Komponenten an einem anderen Lagerplatz einlagern möchten, müssen Sie zuerst den Lagerplatzcode in der Komponentenzeile ändern und die Lagerbestandsumlagerungszeilen dann neu erstellen.  
6.  Geben Sie im Feld **Bewegungsmenge** die vollständige oder einen Teil der Menge ein, die Sie tatsächlich umgelagert haben. Die Werte in den Zeilen "Entnahme" und "Einlagerung" müssen gleich sein. Andernfalls kann die Lagerplatzumlagerung nicht gebucht werden.  

    > [!NOTE]  
    >  Wie bei anderen Lageraktivitäten, können Sie die Einlagerungszeile aufteilen, indem Sie die Aktion **Aktionen** und dann die Aktion **Zeile aufteilen** auswählen. In diesem Fall muss die Summe der beiden geteilten Einlagerungszeilen der Menge in der Zeile für die Entnahme entsprechen.  

7.  Wenn Sie bereit sind, die Umlagerungen zu erfassen, die Sie durchgeführt haben, wählen Sie die Aktion **Lagerbestandsumlagerung registrieren**.  

    Die Lagerplatzposten werden erstellt und zeigen an, dass die Komponenten jetzt an den Lagerplätzen vorhanden sind, die in den Montageauftragszeilen angegeben sind.  

    > [!NOTE]  
    >  Anders als beim Umlagern von Komponenten mit einer Lagerkommissionierung, wird Verbrauch nicht gebucht, wenn Sie eine Lagerbestandsumlagerung erfassen. Dieser Schritt muss separat ausgeführt werden, indem Istmeldung und Verbrauch des Montageauftrags gebucht werden. Weitere Informationen finden Sie unter Montageauftrag.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbest](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

