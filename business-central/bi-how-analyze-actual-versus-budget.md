---
title: Tatsächlichen Beträge mit den budgetierten Beträgen analysieren
description: 'In diesem Artikel wird beschrieben, wie Sie die tatsächlichen Beträge im Vergleich zu den geplanten Beträgen analysieren können, um Daten Ihrer Firma zu erfassen, zu analysieren und weiterzugeben.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '120, 121, 422'
ms.date: 09/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Tatsächlichen Beträge mit den budgetierten Beträgen analysieren

Als Teil des Zusammentragen, Analysieren und Teilen der Firmendaten sehen Sie aktuelle Beträge verglichen mit den budgetierten Beträgen für alle Konten sowie für mehrere Perioden.

Um die budgetierten Beträge zu analysieren, müssen Sie zunächst Sachkontenbudgets erstellen. Erfahren Sie mehr unter [Sachkontenbudgets erstellen](finance-how-create-budgets.md).

## <a name="view-a-gl-budget"></a>Ein Sachkontenbudget anzeigen

In einem Budget mit Dimensionen können Sie die Posten filtern und somit bestimmte Budgets einsehen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Sachkontenbudgets** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie auf der Seite **Sachkontenbudgets** das Budget, das Sie sich ansehen möchten.  
3. Füllen Sie oben auf der Seite die erforderlichen Felder aus, um festzulegen, was angezeigt werden soll. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Wenn Sie **Periode** entweder im Feld **Als Zeilen anzeigen** oder **Als Spalten anzeigen** ausgewählt haben, müssen Sie das Feld **Anzeigen nach** ausfüllen. Wenn Sie in keinem dieser Felder **Periode** ausgewählt haben, geben Sie die entsprechende Periode in das Feld **Datumsfilter** ein.  

> [!NOTE]  
> Nur Einträge aus dem Sachkonto mit den Filtercodes, die Sie auf dem Inforegister **Filter** eingeben, werden bei der Berechnung berücksichtigt. Budgetbuchungen ohne oder mit anderen Filtercodes werden nicht berücksichtigt. Solange der Filter auf der Seite bleibt, werden im Budget nur Einträge mit diesen Filtercodes angezeigt.  

> [!TIP]  
> Verwenden Sie die Aktion **Budget bearbeiten**, um das Budget zu ändern. Wählen Sie auf der Budgetseite einen Betrag aus, um die zugrundeliegenden Sachkonto-Budgeteinträge anzuzeigen.

## <a name="view-actual-and-budgeted-amounts-for-all-accounts"></a>Anzeigen der tatsächlichen und budgetierten Beträge für alle Konten

Sie können Finanzbudgets anzeigen und sie mit tatsächlichen Werten in verschiedenen Bereichen von [!INCLUDE[prod_short](includes/prod_short.md)] vergleichen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Auf der Seite **Kontenplan** wählen Sie die **Saldo/Budget** Aktion aus.
3. Füllen Sie auf dem Inforegister **Optionen** die erforderlichen Felder aus, um festzulegen, was in der Tabelle angezeigt werden soll.  
4. Bewegen Sie den Mauszeiger über ein Feld in der Tabelle, um eine kurze Beschreibung des angezeigten Betrags zu lesen.

> [!NOTE]  
> Die Filter, die Sie auf dem Seitenkopf festgelegt haben, werden sowohl auf die Hauptbuch- als auch auf die Haushaltsbucheinträge angewendet.

Die Spalten auf der linken Seite enthalten den Kontenplan. Von den fünf Spalten auf der rechten Seite enthalten die ersten vier aktuelle und budgetierte Soll- und Habenbeträge für jedes Konto. Die fünfte Spalte zeigt die Relation zwischen den aktuellen und den budgetierten Beträgen des Sachkontos.  

> [!TIP]  
> Wählen Sie auf der Seite **Saldo/Budget** mithilfe des Felds **Anzeigen nach** die gewünschte Periodenlänge aus. Verwenden Sie das Feld **Ansicht als**, um auszuwählen, wie die Beträge berechnet werden sollen, entweder **Nettoänderung** oder **Saldo zum Datum**. Klicken Sie auf der Registerkarte Aktionen auf **Vorperiode** oder F **olgeperiode**, um die Periode zu ändern.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Aktuelle und budgetierte Beträge für mehrere Perioden anzeigen:

Anstatt die aktuellen und budgetierten Beträge für alle Konten für eine einzige Periode einzusehen, können Sie eine Anzahl von Perioden für ein einziges Konto einsehen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Kontenplan** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Kontenplan** das entsprechende Sachkonto aus und wählen Sie dann die Aktion **Sachkonto Saldo/Budget**.  
3. Füllen Sie auf dem Inforegister **Optionen** die erforderlichen Felder aus, um festzulegen, was in der Tabelle angezeigt werden soll.  
4. Fahren Sie auf der Seite **Zeilen** Inforegister mit dem Mauszeiger über ein Feld in der Tabelle, um eine kurze Beschreibung des angezeigten Betrags zu lesen.  

## <a name="see-also"></a>Siehe auch

[Financial Business Intelligence](bi.md)  
[Mit Finanzberichten arbeiten](bi-how-work-account-schedule.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
