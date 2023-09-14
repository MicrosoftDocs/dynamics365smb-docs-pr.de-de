---
title: Analyseberichte erstellen
description: 'Beschreibt, wie neue Analyseberichte für Verkauf, Einkauf und Lager erstellt und Analysevorlagen eingerichtet werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: bholtorf
---
# <a name="create-analysis-reports"></a>Analyseberichte erstellen

Vertriebsmanager müssen regelmäßig den Umsatz, den Bruttogewinn und andere wichtige Vertriebskennzahlen analysieren. Einkäufer interessieren sich eher für die Dynamik des Kaufvolumens, die Leistung der Lieferanten und die Einkaufspreise. Demgegenüber benötigen Logistik- und Lagerbestandsmanager Informationen zu Lagerumsatz, eine Analyse der Lagerbestandsumlagerung und Statistiken zum Lagerwert. Es gibt also keinen Analysebericht, der für alle passt.

Sie können Analyseberichte auf der Grundlage von Datensätzen Ihrer gebuchten Transaktionen anpassen, z.B. Verkäufe, Einkäufe, Transfers und Bestandsanpassungen. In einem anpassbaren Bericht können die Quelldaten, die aus dem Sachkonto (mit den zugehörigen Werteinträgen) stammen, auf sinnvolle, benutzerdefinierte Weise kombiniert, verglichen und dargestellt werden. In diesem Sinne ist der Analysebericht einem PivotTable-Bericht in Microsoft Excel sehr ähnlich.  

So können Sie z.B. einen personalisierten Bericht erstellen, der sich auf Ihre Großkunden in Bezug auf den Gesamtproduktumsatz in Mengen und verkauften Mengen, den Bruttogewinn und den prozentualen Bruttogewinn im laufenden Monat konzentriert. Dann können Sie diese Zahlen mit den Ergebnissen der Vormonate oder des gleichen Monats im letzten Jahr vergleichen und Abweichungen berechnen lassen. All dies kann in ein und derselben Ansicht erfolgen, die es Ihnen ermöglicht, zu den Ursachen der identifizierten Problembereiche zu navigieren und sogar das Dropdown-Menü zu wählen, um Details bis hinunter auf die Ebene der einzelnen Transaktionen zu betrachten.  

Der Analysebericht besteht aus den Objekten, die Sie analysieren möchten (z.B. Kunden, Kundengruppen, Verkäufer usw., dargestellt als Zeilen) und den Analyseparametern, d.h. der Art und Weise, wie Sie das Objekt analysieren möchten (z.B. Gewinnberechnungen, periodische Vergleiche von Verkaufsbeträgen und -volumen oder periodische Vergleiche von Ist- und Planzahlen, dargestellt als Spalten). 

Zusätzlich zu den Analyseberichten können Sie ähnliche Informationen in Analyseansichten (auf der Grundlage von Dimensionen) erstellen und anzeigen. Erfahren Sie mehr unter [Daten nach Dimensionen analysieren](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Beispiel

Sie können diese Zeilen festlegen (Objekte, die Sie analysieren möchten):  

- Computer  
- Bildschirme  
- Ersatzteile  

Dann können Sie diese Spalten festlegen (wie Sie die Objekte analysiert haben möchten):  

- Verkäufe aktueller Monat  
- Verkäufe letzter Monat  
- Verkäufe in Prozent zum letzten Monat  

## <a name="setting-up-line-and-column-layouts"></a>Festlegen von Zeilen- und Spaltenlayouts

Auf der Seite **Analysebericht** können Sie verschiedene Zeilen- und Spalten-Layouts sehen, die Sie auf der Seite festgelegt haben:

* **Vorlagen für Analysezeilen**, auf der Sie den Namen des Berichts und die Objekte, die Sie in den Zeilen Ihres Berichts anzeigen möchten, festlegen, und auf der Seite
* **Analyse Spaltenvorlagen** Seite, auf der Sie den Namen der Spaltenvorlage und die Analyseparameter festlegen, die im Bericht als Spalten angezeigt werden. Jede Zeile auf dieser Seite steht für eine Spalte in Ihrem Bericht. 

Beachten Sie, dass Analysezeilen und -spalten voneinander unabhängig sind.  

Basierend auf den Zeilen und Spalten, die Sie festgelegt haben, fasst [!INCLUDE[prod_short](includes/prod_short.md)] das Ergebnis Ihres Berichts auf der Seite **Analysebericht** zusammen, wie in der folgenden Tabelle dargestellt.  

|- |Verkäufe aktueller Monat|Verkäufe letzter Monat|Verkäufe letzter Monat %|  
|-|-|-|-|  
|Computer| | | |  
|Bildschirme| | | |  
|Ersatzteile| | | |  
|Summe| | | |  

Sie können z.B. eine Gruppe von Zeilen und mehrere Gruppen von Spaltenlayouts festlegen, um Monats- bzw. Jahresberichte anzuzeigen.

## <a name="set-up-analysis-column-templates"></a>Analysespaltenvorlagen festlegen

Das folgende Verfahren basiert auf den Verkaufsanalyse-Ansichten. Die Schritte sind gleich für Einkaufs- und Bestandsanalyseansichten.

Eine Analysespaltenvorlage enthält eine Reihe von Zeilen, die jeweils eine Analysespalte darstellen, die Sie im Analysebericht haben möchten. Um eine Spalte zu definieren, müssen Sie einer Zeile einen Analysetypcode zuweisen. Dieser Analysetypcode bestimmt den Quelldatentyp in den Artikelposten, auf denen die Analyse basiert. Zu den Quelldaten können Kosten, Verkaufsbeträge oder Mengen und die dazugehörigen Werteinträge gehören. Sie können so viele Spaltenvorlagen festlegen, wie Sie möchten, und diese dann zum Erstellen neuer Analyseberichte verwenden.    

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Vertriebsspaltenvorlagen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die erste leere Zeile aus und füllen Sie die Felder nach Bedarf aus.
3. Wählen Sie die Aktion **Spalten** aus.  
4. Füllen Sie auf der Seite **Analysespalten** die Felder aus, um die Spalten anzugeben, die Sie in Ihrem Analysebericht haben möchten.  

    > [!NOTE]  
    > Um eine Spalte zu definieren, müssen Sie das Feld **Analysenartcode** für alle Spaltentypen außer **Formel** ausfüllen. Sie richten die Analysetypcodes auf der Seite **Analysearten** ein.  
    
    Wenn Sie zudem im Feld **Postenart** die Option **Artikelposten** auswählen, werden die aktuellen Zahlen aus dem Artikelposten kopiert. Wenn Sie **Artikelbudgetposten** auswählen, werden die budgetierten Zahlen aus dem Budget kopiert.  
5. Wählen Sie **OK**, um Ihre Änderungen zu speichern.  

## <a name="set-up-analysis-line-templates"></a>Vorlagen für Analysezeilen festlegen

Das folgende Verfahren basiert auf Analyseberichten für Aufträge. Die Schritte sind gleich für Einkaufs- und Bestandsanalyseansichten.

Eine Analysezeilenvorlage enthält eine Reihe von Zeilen, die jeweils eine von Ihnen gewünschte Analysezeile im Analysebericht darstellen. Eine Zeile kann für einen oder mehrere Artikel, Debitoren, Kreditoren oder Gruppen stehen. Sie können in einer Zeile auch eine Formel erzeugen, mit der die anderen Zeilen zusammengezählt werden. Sie können so viele Zeilenvorlagen festlegen, wie Sie möchten, und diese dann zum Erstellen neuer Analyseberichte verwenden.   

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Vertriebszeilen-Vorlagen** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die erste leere Zeile aus, und füllen Sie dann die Felder nach Bedarf aus.
3. Wählen Sie die Aktion **Zeilen** aus.  
4. Erstellen Sie auf der Seite **Analysezeilen** Zeilen für die Artikel, Debitoren, Kreditioren oder Verkäufer, für die Sie Zahlen im Analysebericht anzeigen möchten. Sie müssen das Feld **Art**, das Feld **Bereich** und das Feld **Beschreibung** ausfüllen.  

> [!NOTE]  
> Wenn Sie viele einzelne Zeilen für jeden Artikel, Kunden usw. erstellen möchten, können Sie alternativ die entsprechende Einfügeoption wählen, um alle relevanten Felder in der Zeile auszufüllen. Wenn es erforderlich ist, können Sie dann die Zeilen manuell bearbeiten. Um Zeilen einzufügen, wählen Sie die Aktion **Elemente einfügen** oder **Elementgruppen einfügen**.  

## <a name="create-a-new-sales-analysis-report"></a>Einen neuen Verkaufsanalysebericht erstellen

Die folgende Vorgehensweise bezieht sich auf Analyseberichte für den Verkauf. Die Schritte sind für Kauf- und Bestandsanalyseberichte ähnlich.

Mit Analyseberichten können Sie die Dynamik Ihrer Verkäufe anhand von wichtigen Verkaufsleistungsindikatoren analysieren, z.B. Umsatz in Beträgen und Mengen, Deckungsbeitrag oder Fortschritt der tatsächlichen Verkäufe gegenüber dem Budget. Mit Analyseberichten können Sie auch Ihre durchschnittlichen Verkaufspreise analysieren und die Verkaufsleistung Ihres Außendienstes bewerten.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Verkaufsanalyseberichte** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Analyseberichtsverkauf** die Aktion **Neu** aus.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die **Analysebericht bearbeiten** Aktion aus.
5. Wählen Sie auf der Seite **Analyseansichtsliste** die Aktion **Matrix anzeigen** aus.  

> [!NOTE]  
> Das Einrichten von Kombinationen aus Zeilen- und Spaltenvorlagen für das Erstellen von Berichten und das Zuweisen von eindeutigen Namen zu diesen sind nicht erforderlich. Wenn Sie dies tun, müssen Sie auf der Seite **Verkaufsanalyseberichte** keine Zeilen- und Spaltenvorlagen auswählen. Nach dem Auswählen eines Berichtsnamens können Sie die Zeilen- und Spaltenvorlagen unabhängig voneinander ändern und später den Berichtsnamen erneut auswählen, um die ursprüngliche Kombination wiederherzustellen.

## <a name="see-also"></a>Siehe auch

[Financial Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Das Hauptbuch und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
