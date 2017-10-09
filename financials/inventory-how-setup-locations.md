---
title: Einrichten einer Lagerortkarte und definieren von Umlagerungsrouten| Microsoft Docs
description: "Sie stellen eine Lagerortkarte für jedes Bundesland, den von Lagerartikel speichern, beispielsweise, ein Lager oder eine Vertriebsstelle und Einrichtungsrouten, um Artikel zwischen Lagerorten umlagern erstellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7d82b1c63bb1da367736f8dd044640b583493af8
ms.contentlocale: de-de
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-locations"></a>So wird's gemacht: Standorte einrichten
Wenn Sie Artikel a mehr als einem Ort oder Lagerort kaufen, lagern oder verkaufen, müssen Sie jeden Lagerplatz mit einer Lagerortkarte einrichten und Umlagerungsrouten definieren.

Sie können dann Belegzeilen für einen bestimmten Lagerplatz erstellen, Verfügbarkeit nach Lagerplatz anzeigen und Lagerbestand zwischen Lagerplätzen umlagern. Weitere Informationen finden Sie unter [Lagerbestand verwalten](inventory-manage-inventory.md).

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.

## <a name="to-create-a-location-card"></a>So erstellen Sie eine Lagerortkarte
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplätze** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie im Fenster **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wiederholen Sie die Schritte 2 und 3 für jeden Lagerplatz, an dem Sie Lagerbestand aufbewahren möchten.

> [!NOTE]  
> Viele Felder auf der Lagerortkarte beziehen sich auf Auftragsabwicklung von Artikel in eingehenden und ausgehenden Lagerprozessen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md). 

## <a name="to-create-a-transfer-route"></a>So erstellen Sie eine Umlagerungsroute
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplätze** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie von jedem beliebigen Fenster **Standortkarten** die Aktion **Umlagerungsrouten** aus.
3. Wählen Sie die Aktion **Neu** aus.
4. Füllen Sie im Fenster **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sie können jetzt die Lagerartikel zwischen zwei Lagerplätzen umlagern. Weitere Informationen finden Sie unter [So geht's: Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Siehe auch
[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[So geht's: Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Anpassen der[!INCLUDE[d365fin](includes/d365fin_md.md)]Erfahrung](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

