---
title: "Arbeiten mit Kontenplänen | Microsoft Docs"
description: "Beschreibt, wie Filter verwendet werden, um unterschiedliche Ansichten und Berichte zum Analysieren von Finanzverhältnisleistungsdaten zu erstellen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0284e419280be2d1faba4ac2bf40dac6f78823ed
ms.contentlocale: de-de
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-account-schedules"></a>Vorgehensweise: Arbeiten mit Kontenschemata
Verwenden von Kontenplan, um die Einblicke in die Finanzdaten zu kommen, die in Ihrem Kontenplan gespeichert werden. Verwenden von Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten. Die Ergebnisanzeige in den Diagrammen auf Ihrer Homepage, wie beispielsweise der Cashflowplan.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] enthält mehrere Beispielkontenschemata, die Sie verwenden können , oder Sie können eigene Zeilen und Spalten einrichten, um die Werte anzugeben und zu vergleichen. So können beispielsweise Kontenschemata zur Berechnung von Gewinnmargen für Dimensionen wie beispielsweise Abteilungen oder Debitorengruppen erstellen. Das bedeutet, dass Sie so viele maßgeschneiderte Finanzaufstellungen erstellen können, wie Sie möchten.  

Das Einrichten von Kontenschemata erfordert ein Verständnis für die Finanzdaten im Kontenplan. Sie können beispielsweise die Sachposten als prozentualen Anteil der Budgetposten sehen. Dazu ist es erforderlich, dass Budgets erstellt werden. Weitere Informationen finden Sie unter [Gewusst wie: Budgets erstellen](finance-how-create-budgets.md).

> [!NOTE]  
>   Diese Funktionen erfordert, dass die Benutzeroberfläche in **Suite** festgelegt wird. Weitere Informationen finden Sie unter [Anpassen Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)Experience.

## <a name="account-categories-and-account-schedules"></a>Kontengruppen und Kontenschemata
Sie können Kontengruppen dazu verwenden, das Layout Ihrer Finanzberichte zu ändern. Wenn Sie Ihre Kontengruppen im Fenster **Sachkontokategorien** eingerichtet haben und die Aktion **Kontenschemata generieren** auswählen, werden die zugrunde liegenden Kontenschemata für die Kernfinanzberichte aktualisiert. Wenn Sie das nächste Mal einen dieser Berichte wie die Saldoabrechnung ausführen, werden neue Summen und Untereinträge basierend auf Ihren Änderungen hinzugefügt. Weitere Informationen finden Sie unter [Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Neue Kontenschemata erstellen:  
 Sie benutzen Kontenschemata zum Analysieren der Werte auf Sachkonten oder zum Vergleichen von Sachposten mit Finanzbudgetposten. Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten sehen.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kontenplämne** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie im Fenster **Kontoschemaname** auf der Registerkarte **Neu** die Option Neu aus, um einen neuen Kontenschemanamen zu erstellen.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.
5. Füllen Sie die Felder im Fenster **Kontenschema** aus.  

    Nachdem Sie ein neues  Kontenschema erstellt haben und  neue Zeilen in Ihrem Kontenschema eingerichtet haben, müssen Sie die Spalten einrichten. Sie können diese entweder manuell einrichten oder Ihrem Kontenschema ein vordefiniertes Spaltenlayout zuweisen.
6. Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.
7. Füllen Sie die Felder im Fenster **Spaltenlayout** aus.

> [!NOTE]  
>   Wurde dem Kontenschema kein Standardspaltenlayout zugeordnet, müssen Sie die  Spalten manuell einrichten.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Eine Spalte zur Berechnung von Prozentsätzen erstellen:  
Manchmal möchten Sie möglicherweise eine Spalte in ein Kontenschema einfügen, in der Prozentsätze einer Summe berechnet werden. Wenn beispielsweise mehrere Zeilen vorhanden sind, in denen die Verkäufe nach Dimension aufgeschlüsselt sind, empfiehlt sich die Einrichtung einer Spalte, in der für jede Zeile der prozentuale Anteil an den Gesamtverkäufen angegeben ist.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kontenplämne** ein und wählen den zugehörenden Link aus.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Klicken Sie auf der Registerkarte **Kontoschema bearbeiten**in der Gruppe Prozess auf Kontenschema bearbeiten, um eine Kontenschemazeile einzurichten, um die Gesamtsumme zu berechnen, auf denen die Prozentsätze basieren.  
4. Fügen Sie eine Zeile unmittelbar über der ersten Zeile ein, für die Sie einen Prozentsatz anzeigen möchten.  
5. Füllen Sie die Felder in der Zeile wie folgt aus: In dem Feld **Zusammenzählungsart** geben Sie **Festgelegte Basis für Prozent** ein. Geben Sie im Feld **Zusammenzählung** eine Formel für die Summe ein, auf die der Prozentsatz basiert. Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.  
6. Wählen Sie die **Spaltenlayouteinrichtung bearbeiten** Aktion aus.  
7. Füllen Sie die Felder in der Zeile wie folgt aus: Wählen Sie im Feld **Spaltenart** **Formel** aus. Geben Sie im Feld **Formel** eine Formel für den Betrag ein, für den ein Prozentsatz berechnet werden soll, gefolgt von %. Wenn beispielsweise Spalte N die Bewegung enthält, geben Sie **N%** ein.  
8. Wiederholen Sie Schritt 4 bis 7 für jede Zeilengruppe, die nach Prozentsätzen aufgeschlüsselt werden soll.

## <a name="to-set-up-account-schedules-with-overviews"></a>Kontenschemata mit Matrizen einrichten:  
Sie können eine Kontenschema zum Erstellen eines Vergleichs der in der Finanzbuchhaltung gebuchten Werte mit den Finanzbudgetwerten benutzen.

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kontenplämne** ein und wählen den zugehörenden Link aus.
2. Wählen Sie im Fenster **Kontenschemanamen** ein Kontenschema aus.  
3. Wählen Sie die **Kontenschema bearbeiten** Aktion aus.  
4. Wählen Sie im Fenster **Kontenplan** den gewünschten Kontenschemanamen im Feld **Name** aus.
5. Wählen Sie die **Konten einfügen** Aktion aus.  
6. Wählen Sie die Konten, die Sie in Ihrer Aufstellung berücksichtigen möchten, und wählen Sie dann **OK**.

    Die Konten sind damit in Ihr Kontenschema eingefügt. Wenn Sie möchten, können Sie auch das Spaltenlayout ändern.  
7. Wählen Sie die Aktion **Übersicht** aus.  
8. Im Inforegister **Dimensionsfilter** legen Sie den gewünschten Budgetfilter fest.  
9. Wählen Sie die Schaltfläche **OK** aus.  

Die Budgetaufstellung kann nun kopiert und in ein Arbeitsblatt eingefügt werden.

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

