---
title: Einrichten und Berichten von Intrastat
description: 'Erfahren Sie, wie Intrastat-Berichtsfunktinen eingerichtet werden, und wie der Handel mit Unternehmen in anderen EU-Ländern gemeldet wird.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 8451, 12202, 31077'
ms.date: 05/23/2022
ms.author: bholtorf
---
# <a name="set-up-and-report-intrastat"></a><a name="set-up-and-report-intrastat"></a>Einrichten und Berichten von Intrastat

Alle Unternehmen innerhalb der EU sind verpflichtet, Auskunft über ihre Handelsaktivitäten mit anderen EU-Ländern/-Regionen zu geben. Warenbewegungen müssen jeden Monat dem Statistischen Amt Ihres Landes/Ihrer Region mitgeteilt und die Berichte müssen an die Steuerbehörden übermittelt werden. Dies wird als Intrastat-Berichterstattung bezeichnet. Auf der Seite **Intrastat Buch.-Blatt** können Sie regelmäßige Intrastat-Berichte ausfüllen.

[!INCLUDE[intrastat-2022w2](includes/intrastat-2022w2.md)]

## <a name="required-and-optional-setups"></a><a name="required-and-optional-setups"></a>Erforderliche und optionale Einrichtung

> [!IMPORTANT]
> Debitorenkarten und Kreditorenkarten enthalten das Feld **Intrastat-Partnertyp**, das dieselben Optionswerte wie das Feld **Partnertyp** aufweist: *"" (leer)*, *Unternehmen* und *Person*. Das Feld **Partnertyp** wurde in der Intrastat-Meldung durch das Feld **Intrastat-Partnertyp** ersetzt. **Partnertyp** wird in SEPA verwendet, um das SEPA-Lastschriftverfahren (Core oder B2B) zu definieren. **Intrastat-Partnertyp** wird nur für Intrastat-Berichte verwendet. Auf diese Weise können Sie bei Bedarf unterschiedliche Werte für die beiden Felder angeben.
>
> Beachten Sie jedoch, dass der Wert aus dem Feld **Partnertyp** für Intrastat-Berichte verwendet wird, wenn das Feld **Intrastat-Partnertyp** leer gelassen wird.

Bevor Sie das Intrastat Buch.-Blatt verwenden können, um Intrastat-Informationen zu berichten, müssen Sie mehrere Dinge einrichten:  

* **Intrastat einrichten**: Intrastat-Einrichtungsseite wird verwendet, um Intrastat-Berichts- und Satzstandards zu aktivieren. Sie können festlegen, ob Sie die Intrastatmeldung von Lieferungen (Dispatches), Eingängen (Wareneingang) oder beiden abhängig von den Schwellenwerten melden müssen, die von Ihren lokalen Vorschriften festgelegt werden. Sie können auch die Transaktionstypen für reguläre Dokumente und Reklamationsbelege festlegen, die für die Transaktionsberichterstellung verwendet werden.
* **Intrastat Buch.-Blattvorlagen**: Sie müssen die Intrastat-Buch.-Blattvorlagen und Intrastat-Buch.-Blattnamen einrichten, die Sie verwenden. Da Intrastat-Daten monatlich erfasst werden, müssen Sie 12 Intrastat-Buchungsblätter basierend auf derselben Vorlage erstellen.  
* **Warencodes**: Zoll- und Steuerbehörde haben numerische Codes eingerichtet, die Artikel und Dienstleistungen klassifizieren. Sie geben diese Codes der Artikel an.
* **Transaktionstypencodes**: Länder und Regionen haben unterschiedliche Codes für Intrastat-Transaktionstypen, wie beispielsweise gewöhnlichen Einkauf und Verkauf, den Austausch zurückgegebener Waren und den Austausch nicht zurückgegebener Waren. Einrichtung aller Codes, die sich auf Ihr Land/Ihre Region beziehen. Sie verwenden diese Codes auf dem Inforegister **Außenhandel** und wenn Sie Rückgaben verarbeiten.

    > [!NOTE]
    > Ab Januar 2022 verlangt Intrastat unterschiedliche Transaktions-Natur-Codes für Versendungen an Privatpersonen oder nicht mehrwertsteuerlich registrierte Unternehmen und an mehrwertsteuerlich registrierte Unternehmen. Um diese Anforderung zu erfüllen, empfehlen wir Ihnen, die Transaktionsnatur-Codes auf der Seite **Transaktionsarten** entsprechend den Anforderungen in Ihrem Land zu überprüfen und/oder neue hinzuzufügen. Außerdem sollten Sie das Feld **Intrastat-Partnertyp** überprüfen und auf der entsprechenden **Debitoren**-Seite auf *Person* für Privatpersonen oder Debitoren nicht mehrwertsteuerlich registrierter Unternehmen aktualisieren. Wenn Sie sich nicht sicher sind, welcher Intrastat-Partnertyp oder welche Transaktionsart zu verwenden ist, empfehlen wir Ihnen, einen Experten in Ihrem Land oder Ihrer Region zu fragen.

* **Transportmethoden**: Es gibt sieben einstellige Codes für Intrastat-Transportmethoden. **1** für See, **2** für Schiene, **3** für Straße, **4** für Luft, **5** für Post, **7** für feste Installationen und **9** für eigenen Antrieb (z. B. Tranportieren eines Autos, indem dieses gefahren wird). [!INCLUDE[prod_short](includes/prod_short.md)] erfordert diese Codes nicht, wir empfehlen jedoch, dass die Beschreibungen eine ähnliche Bedeutung bereitstellen.  
* **Transaktionsspezifikationen**: Dienen der Ergänzung der Beschreibungen aus den Buchungsarten.  
* **Ursprungsland**: Verwenden Sie die aus zwei Buchstaben bestehenden ISO-Alphacodes für das Land, in dem die Ware erworben oder hergestellt wurde. Wenn die Ware in mehr als einem Land hergestellt wurde, ist das Ursprungsland das letzte Land, in dem sie in nennenswertem Umfang verarbeitet wurde.
* **Umsatzsteuer-Identifikationsnummer des Handelspartners im Einfuhrmitgliedstaat**: Dies ist die Umsatzsteuer-Identifikationsnummer des Handelspartners im Einfuhrmitgliedstaat. Die Umsatzsteuer-ID wird auch beim Austausch von Intra-EU-Ausfuhrdaten zwischen den Mitgliedstaaten verwendet und ermöglicht es den Mitgliedstaaten, die erhaltenen Daten dem einführenden Unternehmen in ihrem eigenen Land zuzuordnen. Meldestellen müssen die Umsatzsteuer-ID des Unternehmens melden, das den innergemeinschaftlichen Erwerb von Gegenständen im Einfuhrmitgliedstaat angemeldet hat.

> [!NOTE]
> Die zu verwendende Umsatzsteuer-Identifikationsnummer des Handelspartners kann je nach Geschäftssituation unterschiedlich sein. Die zu verwendende Kennung unterscheidet sich zum Beispiel für Szenarien wie Vertriebsketten, bei denen ein Lieferant ein Produkt in ein anderes Land verkauft und dieses Unternehmen den Artikel dann an ein anderes Unternehmen im selben Land weiterverkauft, Dreiecksgeschäft usw. Wenn Sie sich nicht sicher sind, welche Umsatzsteuer-ID Sie verwenden sollen, empfehlen wir Ihnen, einen Experten in Ihrem Land oder Ihrer Region zu fragen.

Optional können Sie auch Folgendes angeben:

* **Bereiche**: Dienen dazu, Informationen über Länder und Regionen zu ergänzen.  
* **Häfen**: Dienen dazu, die Positionen anzugeben, wo Sie Artikel in andere Länder versenden oder aus anderen Ländern empfangen. Heathrow Airport ist ein Beispiel für einen Hafen. Sie geben Häfen auf Verkaufs- und Einkaufsbelegen des Inforegisters **Außenhandel** ein. Diese Daten werden auch aus den Artikelposten kopiert, wenn Sie das Intrastat-Buch.-Blatt erstellen.  

### <a name="to-set-up-intrastat-templates-and-batches"></a><a name="to-set-up-intrastat-templates-and-batches"></a>So richten Sie Intrastat-Buch.-Blattvorlagen und -stapel ein

Die Intrastat-Stapelverarbeitungsaufträge enthalten nur Artikelposten, keine Sachposten. Sind Sachkonten vorhanden, die in die Intrastat-Berichte einbezogen werden müssen, müssen diese manuell eingegeben werden. Wenn Sie also beispielsweise aus einem anderen Land/einer anderen Region innerhalb der EU einen Computer erwerben, geht der Computer zwar nicht in den Lagerbestand ein, er wird jedoch auf ein Sachkonto gebucht. Diese Postenart muss manuell in das Intrastat Buch.-Blatt eingegeben werden.  

Sie können die Positionen in eine Datei exportieren, die Sie an Ihre Intrastat-Behörden senden. Sie können auch einen Bericht ausdrucken, die Informationen manuell in die Formulare Ihrer Behörden eingeben und dann die Informationen übertragen.

> [!NOTE]
> Es empfiehlt sich, für jeden Monat einen Intrastat Buch.-Blattnamen zu erstellen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Intrastat Buch.-Blattvorlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Erstellen Sie eine Vorlage für jedes verwendete Intrastat-Formular.  
3. Um Chargen zu erstellen, wählen Sie die Aktion **Stapel**.  
4. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Erstellen Sie eine Vorlage für jedes verwendete Intrastat-Formular.

> [!NOTE]
> Geben Sie im Feld **Statistikperiode** die Statistikperiode als vierstellige Zahl ein, wobei die ersten beiden Ziffern das Jahr und die nächsten beiden Ziffern den Monat darstellen. Für Juni 2017 beispielsweise geben Sie 1706 ein.

### <a name="to-set-up-transport-methods"></a><a name="to-set-up-transport-methods"></a>Einrichten von Transportmethoden

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Verkehrszweige** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a><a name="to-set-up-which-intrastat-report-fields-are-mandatory"></a>Um einzurichten die Intrastat-Berichte erforderlich sein sollte Sie unter

In einigen Ländern wie Spanien und dem Vereinigten Königreich, verlangen die Behörden, dass Intrastat-Berichte, beispielsweise, die Lieferbedingung für Einkäufe oder einige andere Werte enthalten, wenn die Verkäufe über einem bestimmten Schwellenwert sind. Auf der Seite **Intrastat einrichten** können Sie auswählen, um **Intrastat-Prüflisten-Einrichtung** Pflichtfelder auf der Seite **Intrastat Buch.-Blatt** festlegen soll.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intrastat-Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Intrastat-Prüflisten-Einrichtung** aus.
3. Auf der Seite **Intrastat-Prüflisten-Einrichtung** in **Feldname**, um den Intrastat-Berichtsfelds auszuwählen, das Sie zwar erforderlich machen möchten.

### <a name="czechia"></a><a name="czechia"></a>Tschechien

Speziell für tschechische Unternehmen müssen Sie auch Warencodes und Transaktionscodes einrichten.  

#### <a name="to-set-up-commodity-codes"></a><a name="to-set-up-commodity-codes"></a>Um Warencodes einzurichten:

Alle Artikel, die Sie kaufen oder verkaufen, benötigen einen Warencode.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Warencodes** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Um einem Artikel einem Warencode zuzuordnen, erweitern Sie auf der Seite **Artikelkarte** das Inforegister **Kosten und Buchen** und geben dann den Code in das Feld **Warencode** ein.

### <a name="italy"></a><a name="italy"></a>Italien

Speziell für italienische Unternehmen müssen Sie auch Warencodes und Transaktionscodes einrichten.  

#### <a name="to-set-up-transaction-nature-codes"></a><a name="to-set-up-transaction-nature-codes"></a>Einrichten von Transaktionsartencodes

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Transaktionsnatur-Codes** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Wenn Sie häufiger einen bestimmten Transaktionsartencode verwenden, können Sie sich den Standard erstellen. Dazu gehen Sie zur Seite **Intrastat einrichten**, und wählen den Code aus.

## <a name="to-report-intrastat"></a><a name="to-report-intrastat"></a>Intrastat-Berichte erstellen

Nachdem Sie das Intrastat-Buch.-Blatt ausgefüllt haben, können Sie den Bericht **Checklistenbericht** ausführen, um zu überprüfen, ob alle Daten in dem Buch.-Blatt korrekt sind. Pflichtfelder, die Sie auf der Seite **Intrastat-Prüflisten-Einrichtung**, die Werte fehlende sind, werden angezeigt in Problemen und in warnendem Infobox auf der Seite **Intrastat Buch.-Blatt** festgelegt haben. Anschließend können Sie einen Intrastat-Bericht als Formular drucken, oder Sie erstellen eine Datei, um diese an die Steuerbehörden in Ihrem Land/Region zu senden.  

### <a name="to-fill-in-intrastat-journals"></a><a name="to-fill-in-intrastat-journals"></a>Intrastat-Buch.-Blätter ausfüllen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intrastat Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Intrastat-Buch.-Blatt** den betreffenden Buch.-Blattnamen im Feld **Buch.-Blattname** aus und dann **OK**.  
3. Wählen Sie die Aktion **Mahnungszeile vorschlagen**. Die Felder **Startdatum** und **Enddatum** enthalten bereits die Daten, die Sie im Buch.-Blattnamen für die Statistikperiode angegeben haben.  
4. Im Feld **Kosten Zu-/Abschlag %** können Sie einen Prozentsatz (zur Deckung der Transport- und Versicherungskosten) eingeben. Wenn Sie einen Prozentsatz eingeben, ist der Inhalt des Feldes **Statistischer Wert** dementsprechend höher.  
5. Klicken Sie zum Starten des Batchauftrags auf **OK**.  

Der Batchauftrag holt alle Posten innerhalb der Statistikperiode und fügt Sie als Zeilen im Intrastat Buch.-Blatt ein. Sie können diese Positionen bei Bedarf bearbeiten.  

> [!IMPORTANT]  
> Durch die Stapelverarbeitung werden nur die Posten abgerufen, die einen Länder-/Regionscode enthalten, für den auf der Seite **Länder/Regionen** ein Intrastatcode angegeben wurde. Daher ist es wichtig, dass Sie Intrastatcodes für die Länder-/Regionscodes eingeben, für die Sie die Stapelverarbeitung ausführen möchten. Der Batchauftrag legt das Feld **Partner-Umsatzsteuer-ID** auf *QV999999999999* für Privatpersonen oder nicht mehrwertsteuerpflichtige Unternehmen fest (Debitoren, bei denen das Feld **Intrastat** auf *Person* festgelegt ist), und er verwendet den Wert des Feldes **Buchungstyp** auf dem gebuchten Artikel- oder Auftragsbucheintrag.

### <a name="to-modify-intrastat-journals-lines"></a><a name="to-modify-intrastat-journals-lines"></a>So ändern Sie die Zeilen der Intrastat-Erfassungen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intrastat-Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Intrastat-Buch.-Blatt** den betreffenden Buch.-Blattnamen im Feld **Buch.-Blattname** aus und dann **OK**.  
3. Benutzer-Filterbereich zum Filtern von Intrastat-Jorunal-Zeilen anhand bestimmter Kriterien. Filtern Sie zum Beispiel auf **Partner-Mehrwertsteuer-ID** Felder mit dem Wert *QV999999999999*.
4. Wählen Sie das Symbol **Freigeben** ![Eine Seite in einer anderen App freigeben.](media/share-icon.png) und wählen Sie **Bearbeiten in Excel**
5. Ändern Sie in Excel die Intrastat-Buch.-Blatt-Zeilen, die Sie herausgefiltert haben. Ändern Sie zum Beispiel die Werte des Feldes **Transaktionsart**.  
6. Veröffentlichen Sie die Änderungen, die Sie in Excel vorgenommen haben, zurück auf [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> In [!INCLUDE[prod_short](includes/prod_short.md)]-Versionen, die [**In Excel bearbeiten**](across-work-with-excel.md#edit-in-excel) für Erfassungen nicht unterstützen, können Sie Konfigurationspakete erstellen, um Intrastat-Buch.-Blattzeilen nach Excel zu exportieren und in Excel zu importieren. Weitere Informationen finden Sie unter [Lokale Daten zu Business Central Online migrieren](/dynamics365/business-central/dev-itpro/administration/migrate-data) im Verwaltungsinhalt.

### <a name="report-intrastat-on-a-form-or-a-file"></a><a name="report-intrastat-on-a-form-or-a-file"></a>Melden von Intrastat auf einem Formular oder einer Datei

Um von den Statistikbehörden die für das Intrastat-Formular benötigten Daten zu erhalten, müssen Sie den Bericht **Intrastat – Formular** ausdrucken. Zuvor müssen Sie das Intrastat-Buch.-Blatt vorbereiten und ausfüllen. Wenn Sie sowohl Einkaufs- als auch Verkaufstransaktionen haben, müssen Sie für jede Art ein eigenes Formular ausfüllen und daher den Bericht zweimal drucken.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intrastat Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Intrastat-Buch.-Blatt** den betreffenden Buch.-Blattnamen im Feld **Buch.-Blattname** aus.  
3. Wenn Sie dies noch nicht getan haben, füllen Sie das Journal manuell aus oder wählen Sie die Aktion **Zeilen vorschlagen**.  
4. Wählen Sie die **Druck-Intrastat Buch.-Blatt** Aktion aus.  
5. Fügen Sie im Inforegister **Intrastat Buch.-Blattzeile** einen **Art**-Filter hinzu, und geben Sie an, ob es sich um einen **Wareneingang** oder **Warenausgang** handelt.  
6. Wählen Sie **Senden an**, um den Bericht zu drucken.  

### <a name="report-intrastat-in-a-file"></a><a name="report-intrastat-in-a-file"></a>Intrastat Berichte in einer Datei

Sie können den Intrastat-auch auf einer Datei einreichen. Bevor Sie die Datei erstellen, können Sie einen Testbericht drucken, der dieselben Daten enthält wie die Datei.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intrastat-Buch.-Blatt** ein und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie auf der Seite **Intrastat-Buch.-Blatt** den betreffenden Buch.-Blattnamen im Feld **Buch.-Blattname** aus.  
3. Wenn Sie dies noch nicht getan haben, füllen Sie das Journal manuell oder über die Aktion **Zeilen vorschlagen** aus.  
4. Wählen Sie die Aktion **Aus Datei erstellen** aus.  
5. Wählen Sie auf der Stapel-Job-Seite die Schaltfläche **OK**.  
6. Wählen Sie **Speichern** aus.  
7. Navigieren Sie zum gewünschten Speicherort für die Datei, und geben Sie den Dateinamen ein. Klicken Sie auf **Speichern**.

> [!NOTE]
> Wenn eine Zeile im Intrastat-Bericht eine zusätzliche Maßeinheit aufweist, wird das Gewicht des Artikels nicht angezeigt, da dieser Wert nicht erforderlich ist.

## <a name="reorganize-intrastat-journals"></a><a name="reorganize-intrastat-journals"></a>Reorganisieren von Intrastat Buch.-Blättern

Sie müssen für jeden Monat einen Intrastat-Bericht einreichen und für jeden Bericht einen neuen Buch.-Blattnamen erstellen. Deshalb werden Sie irgendwann über eine Vielzahl von Buch.-Blattnamen verfügen. Die Buch.-Blattzeilen werden nicht automatisch gelöscht. Sie werden vielleicht Ihre Buch.-Blattnamen periodisch reorganisieren wollen. Sie tun dies, indem Sie die Buch.-Blattnamen löschen, die Sie nicht länger benötigen. Die Buch.-Blattzeilen in diesen Buch.-Blattnamen werden ebenfalls gelöscht.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Intrastat Buch.-Blatt** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das Feld **Buch.-Blattname** aus, um die Optionen anzuzeigen.  
3. Wählen Sie die zu löschenden Journalchargen aus und wählen Sie dann die Schaltfläche **Löschen**.  

## <a name="tariff-numbers"></a><a name="tariff-numbers"></a>Zollpositionen

In vielen Ländern werden von den Zoll- und Steuerbehörden achtstellige Artikelcodse für verschiedene Artikelarten vorgeschrieben. Damit die Artikelposten die notwendigen Informationen enthalten, wenn das Programm sie in die Intrastat Buch.-Blattzeile importiert, müssen Sie die Informationen über die Zollposition auf der Seite **Zollpositionen** eingegeben haben. Ermitteln Sie die Codes der Artikel, mit denen Ihr Unternehmen handelt, und geben Sie diese auf der Seite **Zollpositionen** ein.

Auf der Seite **Zollpositionen** fügen Sie alle Codes hinzu, die Sie verwenden. Sie müssen die Codes auf der Artikelkarte eingeben, bevor Sie mit dem Buchen beginnen. Wenn Sie die Codes eingerichtet haben, geben Sie diese ein im **Zollposition** -Feld auf der Artikelkarte. Darüber hinaus müssen Sie das Feld **Nettogewicht** auf der Artikelkarte ausfüllen.

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Siehe verwandte Schulungen unter [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a>Siehe auch

[Finanzmanagement](finance.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
