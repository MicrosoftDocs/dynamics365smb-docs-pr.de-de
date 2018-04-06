---
title: Analysieren von Actuals vs. Budget | Microsoft Docs
description: "Beschreibt, wie die tatsächlichen Beträge mit den budgetierten Beträgen analysiert werden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1da2e94fa64d1daa3304b5266d54152563cfa283
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Tatsächlichen Beträge mit den budgetierten Beträgen analysieren
Als Teil des Zusammentragen, Analysieren und Teilen der Firmendaten sehen Sie aktuelle Beträge verglichen mit den budgetierten Beträgen für alle Konten sowie für mehrere Perioden.

Um budgetierte Beträge zu analysieren, müssen Sie zunächst Sachkonto-Budgets erstellen. Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).

## <a name="to-view-a-gl-budget"></a>Einsehen eines Sachkonto-Budgets
In einem Budget mit Dimensionen können Sie die Posten filtern und somit bestimmte Budgets einsehen.

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **G/L-Blatt Budgets** ein. Wählen Sie dann den zugehörigen Link aus.
2. Öffnen Sie im Fenster **G/L Budgets** das Budget, das Sie anzeigen möchten.  
3. Im Fenster oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Wenn Sie **Periode** entweder im Feld **Als Zeile anzeigen** oder im Feld **Als Spalte anzeigen** ausgewählt haben, müssen Sie das Feld **Anzeigen nach** ausfüllen. Wenn Sie **Periode** weder im Feld **Zeilenansicht** noch im Feld **Spaltenansicht** ausgewählt haben, dann geben Sie die entsprechende Periode im Feld **Datenfilter** ein.  

> [!NOTE]  
>   In der Berechnung werden nur Finnanzbudgetposten mit den Filtercodes berücksichtigt, die Sie im Inforegister **Filter** eingeben. Budgetposten mit anderen Filtercodes oder ohne Filtercodes werden nicht berücksichtigt. Solange der Filter im Fenster verbleibt, zeigt das Budget nur die Budgetposten mit diesen Filtercodes an.  

> [!TIP]  
>   Ist eine Änderung des Budgets erforderlich, können Sie die einzelnen Budgetposten bearbeiten. Wählen Sie einen Betrag aus, um die zugrunde liegenden Finanzbudgetposten anzuzeigen.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Aktuelle und budgetierte Beträge für alle Konten anzeigen:  
Sie können Finanzbudgets anzeigen und sie mit tatsächlichen Werten in verschiedenen Bereichen von [!INCLUDE[d365fin](includes/d365fin_md.md)] vergleichen.

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben **Kontenplan** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Im Fenster **Kontenplan** wählen Sie die **Saldo/Budget** Aktion aus.
3. Im Fenster oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.  
4. Um die Spezifikation eines angezeigten Betrags anzuzeigen, aktivieren Sie das Feld.  

> [!NOTE]  
>   Die Filter, die Sie im Kopf des Fensters setzen, werden sowohl auf die Sachposten als auch auf die Budgetposten angewendet.

Die Spalten auf der linken Seite enthalten den Kontenplan. Von den fünf Spalten auf der rechten Seite enthalten die ersten vier aktuelle und budgetierte Soll- und Habenbeträge für jedes Konto. Die fünfte Spalte zeigt die Relation zwischen den aktuellen und den budgetierten Beträgen des Sachkontos.  

> [!TIP]  
>   Wählen Sie im Fenster **Saldo/Budget** mithilfe des Felds **Anzeigen nach** die gewünschte Periodenlänge aus. Wählen Sie mithilfe des Felds **Anzeigen als** aus, wie die Beträge berechnet werden sollen (**Bewegung** oder **Saldo bis Datum**). Klicken Sie auf der Registerkarte Aktionen auf **Vorperiode** oder F **olgeperiode**, um die Periode zu ändern.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Aktuelle und budgetierte Beträge für mehrere Perioden anzeigen:  
Anstatt die aktuellen und budgetierten Beträge für alle Konten für eine einzige Periode einzusehen, können Sie eine Anzahl von Perioden für ein einziges Konto einsehen.  

1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben **Kontenplan** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Im Fenster **Kontenplan** wählen Sie das entsprechende Sachkonto aus, und wählen Sie die **Sachkontensaldo/Budget** Aktion aus.  
3. Im Fenster oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.   
4. Um die Spezifikation eines angezeigten Betrags anzuzeigen, aktivieren Sie das Feld.  

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Arbeiten mit Kontenschemata](bi-how-work-account-schedule.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

