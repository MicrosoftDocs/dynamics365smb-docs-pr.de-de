---
title: Erstellen Sie Analyseberichte| Microsoft Docs
description: "Beschreibt, wie neue Analyseberichte für Verkauf, Einkauf und Lager erstellt und Analysevorlagen eingerichtet werden."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: f127cef1af857b5f50f5e14c7376941151b57e91
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
#  <a name="create-analysis-reports"></a>Analyseberichte erstellen
Verkaufsleiter müssen regelmäßig Umsatz, Bruttogewinn sowie andere Verkaufsleistungsschlüsselindikatoren analysieren. Einkäufer sind eher an der Entwicklung des Einkaufsvolumens, der Leistung des Verkäufers und den Einkaufspreisen interessiert. Demgegenüber benötigen Logistik- und Lagerbestandsmanager Informationen zu Lagerumsatz, eine Analyse der Lagerbestandsumlagerung und Statistiken zum Lagerwert.  

Sie können Analyseberichte verwenden, um spezifische Berichte basierend auf den Datensätzen der gebuchten Transaktionen (z. B. Verkäufe, Einkäufe, Umlagerungen und Lagerregulierungen) zu erzeugen. In einem spezifischen Bericht können die Quelldaten, die aus den Artikelposten (mit den dazu gehörenden Wertposten) abgeleitet werden, kombiniert, verglichen und auf eine sinnvolle, benutzerdefinierte Weise dargestellt werden. In diesem Sinne ist der Analysebericht einem PivotTable-Bericht in Microsoft Excel sehr ähnlich.  

Sie können Ihren personalisierten Bericht erstellen, der sich auf Ihre Hauptkonten hinsichtlich des Gesamtumsatzes konzentriert, und zwar sowohl bei Beträgen als auch bei verkauften Mengen, Bruttogewinn sowie dem Prozentsatz des Bruttogewinns bezogen auf den aktuellen Monat. Sie können diese Zahlen mit den Ergebnissen vergangener Monate oder dem gleichen Vorjahresmonat vergleichen und Abweichungen berechnen. All dies können Sie in einer einzigen Ansicht vornehmen, und Sie haben die Möglichkeit, zur Ursache eines identifizierten Problemfeldes zu navigieren, indem Sie auf den AssistButton klicken, um auf Details auf der Ebene der individuellen Transaktionen zuzugreifen.  

Der Analysebericht besteht aus den Objekten, die Sie analysieren möchten (beispielsweise Kunden, Kundengruppen, Verkäufer usw.), die als Zeilen dargestellt werden, und den Analyseparametern, d. h. die Art und Weise, in der Sie das Objekt analysieren möchten. Diese Parameter werden als Spalten dargestellt (z. B. Gewinnberechnungen, periodische Vergleiche von Verkaufsbeträgen und -volumen bzw. periodische Vergleiche von tatsächlichen und budgetierten Zahlen).

Zusätzlich zu Analyseberichten können Sie ähnliche Informationen in den Analyseansichten erstellen und anzeigen, die auf Dimensionen basieren. Weitere Informationen finden Sie unter [Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Beispiel  
Sie können beispielsweise folgende Zeilen einrichten:  
- Computer  
- Bildschirme  
- Ersatzteile  

Dann können Sie beispielsweise folgende Spalten erstellen:  

- Verkäufe aktueller Monat  
- Verkäufe letzter Monat  
- Verkäufe in Prozent zum letzten Monat  

## <a name="setting-up-line-and-column-layouts"></a>Einrichten von Zeilen- und Spaltenlayouts  
 Im Fenster **Analysebericht** können Sie unterschiedliche Zeilen- und Spaltenlayouts entsprechend Ihren Einrichtungsparametern anzeigen. Sie erstellen die Zeilen bzw. Zeilenvorlagen im Fenster **Analysezeilenvorlagen**. Sie können in diesem Fenster den Namen des Berichts und die Objekte festlegen, die Sie in den Zeilen des Berichts anzeigen möchten. Sie erstellen die Spalten im Fenster **Analysespaltenvorlagen**. In diesem Fenster können Sie den Namen der Spaltenvorlage und die Analyseparameter, die Sie in dem Bericht als Spalten darstellen möchten, festlegen. Jede Zeile im Fenster **Analysespaltenvorlagen** stellt eine Spalte im Bericht dar. Beachten Sie, dass Analysezeilen und -spalten voneinander unabhängig sind.  

Das Programm fasst, basierend auf den eingerichteten Zeilen und Spalten, die Ergebnisse des Berichts im Fenster **Analysebericht** zusammen. Es verwendet dazu in etwa folgende Matrix:  

| |Verkäufe aktueller Monat|Verkäufe letzter Monat|Verkäufe letzter Monat %|  
|-|-|-|-|  
|Computer| | | |  
|Bildschirme| | | |  
|Ersatzteile| | | |  
|Gesamt| | | |  

 Sie können beispielsweise eine Gruppe von Zeilen und verschiedene Gruppen von Spaltenlayouts einrichten, um monatliche bzw. Jahresberichte anzuzeigen.

 ## <a name="to-set-up-analysis-column-templates"></a>Analysespaltenvorlagen einrichten
Das folgende Verfahren basiert auf einer Analyseansicht für Aufträge. Die Schritte sind gleich für Einkaufs- und Bestandsanalyseansichten.

In einem Analysebericht werden die Analyseparameter als Spalten angezeigt. Sie können durch das Einrichten von Analysespaltenvorlagen die Spalten definieren, die der Analysebericht enthalten soll.  

Eine Vorlage enthält eine Gruppe von Zeilen, wobei jede Zeile eine Analysespalte darstellt, die Sie im Analysebericht sehen. Um eine Spalte zu definieren, müssen Sie einer Zeile einen Analysetypcode zuweisen. Dieser Analysetypcode bestimmt den Quelldatentyp in den Artikelposten, auf denen die Analyse basiert. Quelldaten enthalten Kosten, Verkaufsbetrag oder Menge sowie die dazugehörigen Wertposten. Sie können beliebig viele Spaltenvorlagen einrichten und zur Erstellung neuer Analyseberichte verwenden.    

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsspaltenvorlage** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die erste leere Linie und füllen Sie die notwendigen Felder aus.
3. Wählen Sie die Aktion **Spalten** aus.  
4. Füllen Sie die Felder im Fenster **Analysespalten** aus, um die Spalten zu bestimmen, die der Analysebericht enthalten soll.  

    > [!NOTE]  
    >   Um eine Spalte zu definieren, müssen Sie das Feld **Analysenartcode** für alle Spaltentypen außer **Formel** ausfüllen. Sie richten die Analysetypcodes im Fenster **Analysearten** ein.  
    Wenn Sie zudem im Feld **Postenart** die Option **Artikelposten** auswählen, werden die aktuellen Zahlen aus dem Artikelposten kopiert. Wenn Sie **Artikelbudgetposten** auswählen, werden die budgetierten Zahlen aus dem Budget kopiert.  
5.  Klicken Sie auf die Schaltfläche **OK**, um die Änderungen zu speichern.  

## <a name="to-set-up-analysis-line-templates"></a>Analysenzeilenvorlagen einrichten:  
Das folgende Verfahren basiert auf Analyseberichten für Aufträge. Die Schritte sind gleich für Einkaufs- und Bestandsanalyseansichten.

In einem Analysebericht werden die Analyseobjekte in den Zeilen angezeigt. Sie können durch das Einrichten von Analysezeilenvorlagen die Zeilen definieren, die der Analysebericht enthalten soll.  

Eine Vorlage enthält eine Gruppe von Zeilen, die die im Bericht angezeigten Analysezeilen darstellen. Eine Zeile kann für einen oder mehrere Artikel, Debitoren, Kreditoren oder Gruppen stehen. Sie können in einer Zeile auch eine Formel erzeugen, mit der die anderen Zeilen zusammengezählt werden. Sie können beliebig viele Zeilenvorlagen erstellen und diese dann zur Generierung neuer Analyseberichte verwenden.    

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsspaltenvorlage** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die erste leere Linie und füllen Sie die notwendigen Felder aus.
3. Wählen Sie die Aktion **Zeilen** aus.  
4. Erstellen Sie im Fenster **Analysezeilen** Zeilen für die Artikel, Debitoren, Kreditioren oder Verkäufer, für die Sie Zahlen im Analysebericht anzeigen möchten. Sie müssen das Feld **Art**, das Feld **Bereich** und das Feld **Beschreibung** ausfüllen.  

> [!NOTE]  
>   Möchten Sie alternativ mehrere individuelle Zeilen für jeden Artikel, Debitor usw. erzeugen, wählen Sie die geeignete Einfügeoption aus. Wenn es erforderlich ist, können Sie dann die Zeilen manuell bearbeiten. Um Zeilen einzufügen, wählen Sie auf der Registerkarte Aktionen in der Gruppe Funktionen die Option **Artikel einfügen** oder **Artikelgruppen** einfügen aus.  

## <a name="to-create-a-new-sales-analysis-report"></a>So erstellen Sie einen neuen Vertriebsanalysebericht:
Das folgende Verfahren basiert auf Analyseberichten für Aufträge. Die Schritte sind gleich für Einkaufs- und Bestandsanalyseansichten.

Verwenden Sie Analyseberichte, um die Entwicklung der Verkäufe anhand der ausgewählten Schlüsselindikatoren für die Verkaufsperformance zu analysieren, beispielsweise den Verkaufsumsatz in Beträgen und Mengen, die Beitragsspanne oder den Status der aktuellen Verkäufe gegenüber dem Budget. Sie können den Bericht auch verwenden, um durchschnittliche VK-Preise zu analysieren und die Verkaufsperformance der Verkaufsabteilung zu bewerten.  

1. Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Verkaufsanalysebericht** ein und wählen den zugehörenden Link aus.  
2. Wählen Sie im Fenster **Analyseberichtsverkauf** die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die **Analysebericht bearbeiten** Aktion aus.
5. Wählen Sie im Fenster **Analyseansichtsliste** die Aktion **Matrix anzeigen** aus.  

> [!NOTE]  
>   Das Einrichten von Kombinationen aus Zeilen- und Spaltenvorlagen für das Erstellen von Berichten und das Zuweisen von eindeutigen Namen zu diesen sind nicht erforderlich. Falls Sie dieses Verfahren verwenden, müssen Sie lediglich einen Berichtsnamen auswählen, so dass Sie im Fenster **Vertriebsanalysebericht** keine Zeilen- und Spaltenvorlagen auswählen müssen. Nach dem Auswählen eines Berichtsnamens können Sie die Zeilen- und Spaltenvorlagen unabhängig voneinander ändern und später den Berichtsnamen erneut auswählen, um die ursprüngliche Kombination wiederherzustellen.

## <a name="see-also"></a>Siehe auch
[Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

