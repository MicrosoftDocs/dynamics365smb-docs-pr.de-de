---
title: 'Gewusst wie: Einrichten von Intrastat-Berichten| Microsoft Docs'
description: Erfahren Sie, wie Intrastat-Berichtsfunktinen eingerichtet werden, und wie der Handel mit Unternehmen in anderen EU-Ländern gemeldet wird.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 23759b874f7a92bf9ff91cd0822ac8f9bb716ab1
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183524"
---
# <a name="set-up-and-report-intrastat"></a>Einrichten und Berichten von Intrastat
Alle Unternehmen innerhalb der EU sind verpflichtet, Auskunft über ihre Handelsaktivitäten mit anderen EU-Ländern/-Regionen zu geben. Warenbewegungen müssen jeden Monat dem Statistischen Amt Ihres Landes/Ihrer Region mitgeteilt und die Berichte müssen an die Steuerbehörden übermittelt werden. Dies wird als Intrastat-Berichterstattung bezeichnet. Auf der Seite **Intrastat Buch.-Blatt** können Sie regelmäßige Intrastat-Berichte ausfüllen.  

## <a name="required-and-optional-setups"></a>Erforderliche und optionale Einrichtung
Bevor Sie das Intrastat Buch.-Blatt verwenden können, um Intrastat-Informationen zu berichten, müssen Sie mehrere Dinge einrichten:  

* **Intrastat einrichten**: Intrastat-Einrichtungsseite wird verwendet, um Intrastat-Berichts- und Satzstandards zu aktivieren. Sie können festlegen, ob Sie die Intrastatmeldung von Lieferungen (Dispatches), Eingängen (Wareneingang) oder beiden abhängig von den Schwellenwerten melden müssen, die von Ihren lokalen Vorschriften festgelegt werden. Sie können auch die Transaktionstypen für reguläre Dokumente und Reklamationsbelege festlegen, die für die Transaktionsberichterstellung verwendet werden.
* **Intrastat Buch.-Blattvorlagen**: Sie müssen die Intrastat-Buch.-Blattvorlagen und Intrastat-Buch.-Blattnamen einrichten, die Sie verwenden. Da Intrastat-Daten monatlich erfasst werden, müssen Sie 12 Intrastat-Buchungsblätter basierend auf derselben Vorlage erstellen.  
* **Warencodes**: Zoll- und Steuerbehörde haben numerische Codes eingerichtet, die Artikel und Dienstleistungen klassifizieren. Sie geben diese Codes der Artikel an.
* **Transaktionstypencodes**: Länder und Regionen haben unterschiedliche Codes für Intrastat-Transaktionstypen, wie beispielsweise gewöhnlichen Einkauf und Verkauf, den Austausch zurückgegebener Waren und den Austausch nicht zurückgegebener Waren. Einrichtung aller Codes, die sich auf Ihr Land/Ihre Region beziehen. Sie verwenden diese Codes in Einkaufs- und Verkaufsbelegen und wenn Sie Rückgaben verarbeiten.  
* **Transportmethoden**: Es gibt sieben einstellige Codes für Intrastat-Transportmethoden. **1** für See, **2** für Schiene, **3** für Straße, **4** für Luft, **5** für Post, **7** für feste Installationen und **9** für eigenen Antrieb (z. B. Tranportieren eines Autos, indem dieses gefahren wird). [!INCLUDE[d365fin](includes/d365fin_md.md)] erfordert diese Codes nicht, wir empfehlen jedoch, dass die Beschreibungen eine ähnliche Bedeutung bereitstellen.  

Optional können Sie auch Folgendes angeben:

* **Transaktionsspezifikationen**: Dienen der Ergänzung der Beschreibungen aus den Buchungsarten.  
* **Bereiche**: Dienen dazu, Informationen über Länder und Regionen zu ergänzen.  
* **Häfen**: Dienen dazu, die Positionen anzugeben, wo Sie Artikel in andere Länder versenden oder aus anderen Ländern empfangen. Heathrow Airport ist ein Beispiel für einen Hafen. Sie geben Häfen auf Verkaufs- und Einkaufsbelegen des Inforegisters **Außenhandel** ein. Diese Daten werden auch aus den Artikelposten kopiert, wenn Sie das Intrastat-Buch.-Blatt erstellen.  

### <a name="to-set-up-intrastat-templates-and-batches"></a>So richten Sie Intrastat-Buch.-Blattvorlagen und -stapel ein
Die Intrastat-Stapelverarbeitungsaufträge enthalten nur Artikelposten, keine Sachposten. Sind Sachkonten vorhanden, die in die Intrastat-Berichte einbezogen werden müssen, müssen diese manuell eingegeben werden. Wenn Sie also beispielsweise aus einem anderen Land/einer anderen Region innerhalb der EU einen Computer erwerben, geht der Computer zwar nicht in den Lagerbestand ein, er wird jedoch auf ein Sachkonto gebucht. Diese Postenart muss manuell in das Intrastat Buch.-Blatt eingegeben werden.  

Sie können die Positionen in eine Datei exportieren, die Sie an Ihre Intrastat-Behörden senden. Sie können auch einen Bericht ausdrucken, die Informationen manuell in die Formulare Ihrer Behörden eingeben und dann die Informationen übertragen.

>  [!Note]
> Es empfiehlt sich, für jeden Monat einen Intrastat Buch.-Blattnamen zu erstellen.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Intrastat Buch.-Blattvorlagen** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Erstellen Sie eine Vorlage für jedes verwendete Intrastat-Formular.  
3. Um Chargen zu erstellen, wählen Sie die Aktion **Stapel**.  
4. Füllen Sie die Felder bei Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Erstellen Sie eine Vorlage für jedes verwendete Intrastat-Formular.  

> [!Note]
> Geben Sie im Feld **Statistikperiode** die Statistikperiode als vierstellige Zahl ein, wobei die ersten beiden Ziffern das Jahr und die nächsten beiden Ziffern den Monat darstellen. Für Juni 2017 beispielsweise geben Sie 1706 ein.

### <a name="to-set-up-commodity-codes"></a>Um Warencodes einzurichten:
Alle Artikel, die Sie kaufen oder verkaufen, benötigen einen Warencode.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Warencodes** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Um einem Artikel einem Warencode zuzuordnen, erweitern Sie auf der Seite **Artikelkarte** das Inforegister **Kosten und Buchen** und geben dann den Code in das Feld **Warencode** ein.   

### <a name="to-set-up-transaction-nature-codes"></a>Einrichten von Transaktionsartencodes
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Transaktionsartencodes** ein, und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!Tip]
> Wenn Sie häufiger einen bestimmten Transaktionsartencode verwenden, können Sie sich den Standard erstellen. Dazu gehen Sie zur Seite **Intrastat einrichten**, und wählen den Code aus.

### <a name="to-set-up-transport-methods"></a>Einrichten von Transportmethoden
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Verkehrszweige** ein, und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Um einzurichten die Intrastat-Berichte erforderlich sein sollte Sie unter
In einigen Ländern wie Spanien und Großbritannien, verlangen die Behörden, dass Intrastat-Berichte, beispielsweise, die Lieferbedingung für Einkäufe oder einige andere Werte enthalten, wenn Verkaufs- über einem bestimmten Schwellenwert ist. Auf der Seite **Intrastat einrichten** können Sie auswählen, um **Einrichtung Checkist Intrastat** Pflichtfelder auf der Seite **Intrastat Buch.-Blatt** festlegen soll.

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Intrastat einrichten** ein und wählen Sie dann den entsprechenden Link.
2. Wählt die **Intrastat-Prüflisten-Einrichtung** Aktion aus.
3. Auf der Seite **Intrastat-Prüflisten-Einrichtung** in **Feldname**, um den Intrastat-Berichtsfelds auszuwählen, das Sie zwar erforderlich machen möchten.

## <a name="to-report-intrastat"></a>Erstellen Sie Intrastat-Berichte
Nachdem Sie das Intrastat-Buch.-Blatt ausgefüllt haben, können Sie den Bericht **Checklistenbericht** ausführen, um zu überprüfen, ob alle Daten in dem Buch.-Blatt korrekt sind. Pflichtfelder, die Sie auf der Seite **Intrastat-Prüflisten-Einrichtung**, die Werte fehlende sind, werden angezeigt in Problemen und in warnendem Infobox im Fenster **Intrastat Buch.-Blatt** festgelegt haben. Anschließend können Sie einen Intrastat-Bericht als Formular drucken, oder Sie erstellen eine Datei, um diese an die Steuerbehörden in Ihrem Land/Region zu senden.  

### <a name="to-fill-in-intrastat-journals"></a>Intrastat-Buch.-Blätter ausfüllen:  
1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Intrastat Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Intrastat-Buch.-Blatt** den betreffenden Buch.-Blattnamen im Feld **Buch.-Blattname** aus und dann **OK**.  
3. Wählen Sie die Aktion **Mahnungszeile vorschlagen**. Die Felder **Startdatum** und **Enddatum** enthalten bereits die Daten, die Sie im Buch.-Blattnamen für die Statistikperiode angegeben haben.  
4. Im Feld **Kosten Zu-/Abschlag %** können Sie einen Prozentsatz (zur Deckung der Transport- und Versicherungskosten) eingeben. Wenn Sie einen Prozentsatz eingeben, ist der Inhalt des Feldes **Statistischer Wert** dementsprechend höher.  
5. Klicken Sie zum Starten des Batchauftrags auf **OK**.  

Der Batchauftrag holt alle Posten innerhalb der Statistikperiode und fügt Sie als Zeilen im Intrastat Buch.-Blatt ein. Sie können diese Positionen bei Bedarf bearbeiten.  

> [!IMPORTANT]  
>  Durch die Stapelverarbeitung werden nur die Posten abgerufen, die einen Länder-/Regionscode enthalten, für den auf der Seite **Länder/Regionen** ein Intrastatcode angegeben wurde. Daher ist es wichtig, dass Sie Intrastatcodes für die Länder-/Regionscodes eingeben, für die Sie die Stapelverarbeitung ausführen möchten.  

### <a name="report-intrastat-on-a-form-or-a-file"></a>Melden von Intrastat auf einem Formular oder einer Datei
Um von den Statistikbehörden die für das Intrastat-Formular benötigten Daten zu erhalten, müssen Sie den Bericht **Intrastat – Formular** ausdrucken. Zuvor müssen Sie das Intrastat-Buch.-Blatt vorbereiten und ausfüllen. Wenn Sie sowohl Einkaufs- als auch Verkaufstransaktionen haben, müssen Sie für jede Art ein eigenes Formular ausfüllen und daher den Bericht zweimal drucken.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Intrastat Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Intrastat-Buch.-Blatt** den betreffenden Buch.-Blattnamen im Feld **Buch.-Blattname** aus.  
3. Wenn Sie dies noch nicht getan haben, füllen Sie das Journal manuell aus oder wählen Sie die Aktion **Zeilen vorschlagen**.  
4. Wählen Sie die **Druck-Intrastat Buch.-Blatt** Aktion aus.  
5. Fügen Sie im Inforegister **Intrastat Buch.-Blattzeile** einen **Art**-Filter hinzu, und geben Sie an, ob es sich um einen **Wareneingang** oder **Warenausgang** handelt.  
6. Wählen Sie **Senden an**, um den Bericht zu drucken.  

### <a name="report-intrastat-in-a-file"></a>Intrastat Berichte in einer Datei
Sie können den Intrastat-auch auf einer Datei einreichen. Bevor Sie die Datei erstellen, können Sie einen Testbericht drucken, der dieselben Daten enthält wie die Datei.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Intrastat Buch.-Blatt** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Intrastat-Buch.-Blatt** den betreffenden Buch.-Blattnamen im Feld **Buch.-Blattname** aus.  
3. Wenn Sie dies noch nicht getan haben, füllen Sie das Journal manuell oder über die Aktion **Zeilen vorschlagen** aus.  
4. Wählen Sie die Aktion **Aus Datei erstellen** aus.  
5. Wählen Sie auf der Stapel-Job-Seite die Schaltfläche **OK**.  
6. Wählen Sie **Speichern** aus.  
7. Navigieren Sie zum gewünschten Speicherort für die Datei, und geben Sie den Dateinamen ein. Klicken Sie auf **Speichern**.

## <a name="reorganize-intrastat-journals"></a>Reorganisieren von Intrastat Buch.-Blättern
Sie müssen für jeden Monat einen Intrastat-Bericht einreichen und für jeden Bericht einen neuen Buch.-Blattnamen erstellen. Deshalb werden Sie irgendwann über eine Vielzahl von Buch.-Blattnamen verfügen. Die Buch.-Blattzeilen werden nicht automatisch gelöscht. Sie werden vielleicht Ihre Buch.-Blattnamen periodisch reorganisieren wollen. Sie tun dies, indem Sie die Buch.-Blattnamen löschen, die Sie nicht länger benötigen. Die Buch.-Blattzeilen in diesen Buch.-Blattnamen werden ebenfalls gelöscht.  

1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Sie wünschen“ öffnet](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Intrastat Buch.-Blätter** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie das Feld **Buch.-Blattname** aus, um die Optionen anzuzeigen.  
3. Wählen Sie die zu löschenden Journalchargen aus und wählen Sie dann die Schaltfläche **Löschen**.  

## <a name="see-related-training-at-microsoft-learn"></a>Das dazugehörige Training finden Sie unter [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch
[Finanzmanagement](finance.md)
