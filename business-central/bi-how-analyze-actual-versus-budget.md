---
title: Analysieren von Actuals vs. Budget | Microsoft Docs
description: Beschreibt, wie die tatsächlichen Beträge mit den budgetierten Beträgen analysiert werden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 32680efab7168ade5c8feca4cb69a37687da708b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186116"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Tatsächlichen Beträge mit den budgetierten Beträgen analysieren
Als Teil des Zusammentragen, Analysieren und Teilen der Firmendaten sehen Sie aktuelle Beträge verglichen mit den budgetierten Beträgen für alle Konten sowie für mehrere Perioden.

Um budgetierte Beträge zu analysieren, müssen Sie zunächst Sachkonto-Budgets erstellen. Weitere Informationen finden Sie unter [Sachkonto-Budgets erstellen](finance-how-create-budgets.md).

## <a name="to-view-a-gl-budget"></a>Einsehen eines Sachkonto-Budgets
In einem Budget mit Dimensionen können Sie die Posten filtern und somit bestimmte Budgets einsehen.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Sachkontenbudgets** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie auf der Seite **G/L Budgets** das Budget, das Sie anzeigen möchten.  
3. Auf der Seite oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Wenn Sie **Periode** entweder im Feld **Als Zeile anzeigen** oder im Feld **Als Spalte anzeigen** ausgewählt haben, müssen Sie das Feld **Anzeigen nach** ausfüllen. Wenn Sie **Periode** weder im Feld **Zeilenansicht** noch im Feld **Spaltenansicht** ausgewählt haben, dann geben Sie die entsprechende Periode im Feld **Datenfilter** ein.  

> [!NOTE]  
>   In der Berechnung werden nur Finnanzbudgetposten mit den Filtercodes berücksichtigt, die Sie im Inforegister **Filter** eingeben. Budgetposten mit anderen Filtercodes oder ohne Filtercodes werden nicht berücksichtigt. Solange der Filter auf der Seite verbleibt, zeigt das Budget nur die Budgetposten mit diesen Filtercodes an.  

> [!TIP]  
>   Ist eine Änderung des Budgets erforderlich, können Sie die einzelnen Budgetposten bearbeiten. Wählen Sie einen Betrag aus, um die zugrunde liegenden Finanzbudgetposten anzuzeigen.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Aktuelle und budgetierte Beträge für alle Konten anzeigen:  
Sie können Finanzbudgets anzeigen und sie mit tatsächlichen Werten in verschiedenen Bereichen von [!INCLUDE[d365fin](includes/d365fin_md.md)] vergleichen.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Kontenplan** wählen Sie die **Saldo/Budget** Aktion aus.
3. Auf der Seite oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.  
4. Um die Spezifikation eines angezeigten Betrags anzuzeigen, aktivieren Sie das Feld.  

> [!NOTE]  
>   Die Filter, die Sie im Kopf auf der Seite setzen, werden sowohl auf die Sachposten als auch auf die Budgetposten angewendet.

Die Spalten auf der linken Seite enthalten den Kontenplan. Von den fünf Spalten auf der rechten Seite enthalten die ersten vier aktuelle und budgetierte Soll- und Habenbeträge für jedes Konto. Die fünfte Spalte zeigt die Relation zwischen den aktuellen und den budgetierten Beträgen des Sachkontos.  

> [!TIP]  
>   Wählen Sie auf der Seite **Saldo/Budget** mithilfe des Felds **Anzeigen nach** die gewünschte Periodenlänge aus. Wählen Sie mithilfe des Felds **Anzeigen als** aus, wie die Beträge berechnet werden sollen (**Bewegung** oder **Saldo bis Datum**). Klicken Sie auf der Registerkarte Aktionen auf **Vorperiode** oder F **olgeperiode**, um die Periode zu ändern.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Aktuelle und budgetierte Beträge für mehrere Perioden anzeigen:  
Anstatt die aktuellen und budgetierten Beträge für alle Konten für eine einzige Periode einzusehen, können Sie eine Anzahl von Perioden für ein einziges Konto einsehen.  

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Kontenplan** wählen Sie das entsprechende Sachkonto aus, und wählen Sie die **Sachkontensaldo/Budget** Aktion aus.  
3. Auf der Seite oben füllen Sie die Felder aus, um anzuzeigen, was gezeigt werden soll.   
4. Um die Spezifikation eines angezeigten Betrags anzuzeigen, aktivieren Sie das Feld.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Arbeiten mit Kontenschemata](bi-how-work-account-schedule.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
