---
title: Erstellen von Finanzberichten mit Finanzdaten und Kontokategorien
description: 'Beschreibt, wie Sie mit Finanzberichten verschiedene Ansichten und Berichte zur Analyse von Finanzdaten erstellen können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Financial Reporting mit Finanzdaten und Kontokategorien vorbereiten

Finanzberichte geben Ihnen Einblick in die in Ihrem Kontenplan (COA) gespeicherten Finanzdaten. Finanzberichte analysieren die Zahlen in den Hauptbüchern (Sachkonten) und vergleichen die Sachbuch-Einträge mit den Budget-Einträgen. Die Ergebnisse werden in Diagrammen und Berichten in Ihrem Rollencenter angezeigt, z. B. im Cashflow-Diagramm und in den Berichten zur Gewinn- und Verlustrechnung und zur Bilanz.

Auf diese beiden Berichte greifen Sie z.B. mit der Aktion **Finanzberichte** in den Rollencentern für Manager und Buchhalter zu.  

[!INCLUDE[prod_short](includes/prod_short.md)] Finanzberichte bietet Ihnen Beispielfinanzberichte, die Sie sofort verwenden können. Sie können auch Ihre eigenen Zeilen und Spalten einrichten, um die zu vergleichenden Zahlen anzugeben. Sie können zum Beispiel Finanzberichte erstellen, um Gewinnspannen anhand von Dimensionen wie Abteilungen oder Kundengruppen zu berechnen. Die Anzahl der benutzerdefinierten Finanzaufstellungen, die Sie erstellen können, ist unbegrenzt.  

Das Einrichten von Finanzberichten erfordert ein Verständnis der Finanzdaten im Kontenplan. Sie können zum Beispiel Hauptbuchhaltungsposten als Prozentsätze von Budgeteinträgen anzeigen, aber dazu müssen Sie Budgets erstellt haben. Erfahren Sie mehr unter [Sachkontenbudgets erstellen](finance-how-create-budgets.md).

## <a name="financial-reports"></a>Finanzielle Berichte

In Finanzberichten werden die Konten aus Ihrem Kontenplan so angeordnet, dass die Daten einfacher dargestellt werden können. Sie können verschiedene Layouts festlegen, um die Informationen zu definieren, die Sie aus dem Kontenplan extrahieren möchten. Finanzberichte bieten einen Platz für Berechnungen, die nicht direkt im Kontenplan vorgenommen werden können. Sie können beispielsweise Zwischensummen für Gruppen von Konten erstellen und diese Summe dann in andere Summen aufnehmen. Ein weiteres Beispiel ist die Berechnung von Gewinnmargen für Dimensionen wie Abteilungen oder Debitorengruppen. Außerdem können Sie Hauptbuch- und Budgetbuchungen filtern, z.B. nach Nettoänderung oder Sollbetrag.

Sie können auch zwei oder mehr Finanzberichte und Spaltendefinitionen mit Hilfe von Formeln vergleichen:

* Erstellen benutzerdefinierter Finanzberichte
* Erstellen Sie so viele Finanzberichte wie Sie benötigen, jeder mit einem eindeutigen Namen.
* Einrichten unterschiedlicher Berichtslayouts und Drucken der Berichte mit den aktuellen Werten

## <a name="gl-account-categories"></a>Sachkonto-Kategorien

Sie können Sachkontokategorien dazu verwenden, das Layout Ihrer Finanzberichte zu ändern. Wenn Sie beispielsweise Ihre Sachkonto-Kategorien auf der Seite **Sachkonto-Kategorien** festgelegt haben, können Sie die Aktion **Finanzberichte generieren** wählen und die zugrundeliegenden Finanzberichte für die Kernfinanzberichte aktualisieren. Wenn Sie dann das nächste Mal einen dieser Berichte ausführen, z.B. den Bericht **Bilanz**, werden neue Summen und Untereinträge hinzugefügt.

> [!NOTE]
> Die Kontenkategorien der obersten Ebene, wie z.B. der Knoten **Verbindlichkeiten**, sind fest vorgegeben und Sie können keine eigenen hinzufügen. Sie können jedoch Kontenkategorien auf niedrigeren Ebenen löschen und hinzufügen und festlegen, wie der zugehörige Finanzbericht in Berichten erscheint.
>
> Sie sollten Ihre eigenen Sachkonto-Kategorien auf unterer Ebene von Grund auf erstellen und strukturieren, ggf. in einer Hierarchie, anstatt zu versuchen, die vorhandenen Kategorien neu anzuordnen. Sie können beispielsweise den Knoten **Verbindlichkeiten** neu strukturieren, sodass er den neuen Knoten **Eigenkapital** gefolgt von den Knoten **Kurzfristige Verbindlichkeiten** und **Langfristige Verbindlichkeiten** enthalten.

## <a name="create-a-new-financial-report"></a>Erstellen Sie einen neuen Finanzbericht

Sie verwenden Finanzberichte, um Hauptbuchkonten zu analysieren oder Hauptbucheinträge mit Budgeteinträgen zu vergleichen. Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten sehen.

Die Finanzberichte in der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] entsprechen möglicherweise nicht den Anforderungen Ihres Unternehmens. Um schnell eigene Finanzberichte zu erstellen, beginnen Sie mit dem Kopieren eines bestehenden Berichts, wie in Schritt drei unten beschrieben.

> [!TIP]
> Nachdem Sie einen Finanzbericht erstellt haben, können Sie die Seite **Finanzbericht** verwenden, um Ihren neu definierten Finanzbericht in der Vorschau anzuzeigen und zu validieren. Um die Seite zu öffnen, wählen Sie die Aktion **Finanzbericht bearbeiten**.  

> [!NOTE]
> Wenn Sie einen Finanzbericht im Ansichts- oder Bearbeitungsmodus öffnen, ist der Bereich Filter verfügbar. Verwenden Sie den Bereich jedoch nicht, um Filter für die Daten in Ihrem Bericht festzulegen. Die Filter können Fehler verursachen oder die Daten nicht wirklich filtern. Verwenden Sie stattdessen die Filterfelder auf den Inforegistern **Optionen** und **Dimensionen** .

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.  
2. Auf der Seite **Finanzberichte** wählen Sie die Aktion **Neu**, um einen neuen Finanzbericht zu erstellen.
3. Wenn Sie die Einstellungen eines bestehenden Finanzberichts wiederverwenden möchten, wählen Sie alternativ die Aktion **Finanzbericht kopieren**.
4. Füllen Sie die Felder nach Bedarf aus. Wählen Sie im Feld **Spaltendefinition** eine vorhandene Definition aus, die Sie später bei Bedarf bearbeiten können.

    Spaltendefinitionen geben die Parameter an, nach denen die Finanzdaten in den Zeilen angezeigt werden. Eine Spaltendefinition könnte zum Beispiel vier Spalten enthalten, mit denen Sie die Nettoveränderung und den Saldo für denselben Zeitraum in diesem und im letzten Jahr vergleichen können. Mehr dazu erfahren Sie im Abschnitt [Bearbeiten einer Spaltendefinition](bi-how-work-account-schedule.md#edit-a-column-definition).

5. Wählen Sie die Aktion **Zeilendefinition bearbeiten**.
6. Wählen Sie die Aktionen **Sachkonten einfügen**, **KF-Konten einfügen** und **Kostenarten einfügen**, um eine Zeile für jedes Finanzelement zu erstellen, das Sie analysieren möchten. Beispielsweise könnten Sie eine Zeile für Umlaufvermögen und eine andere für Anlagevermögen haben. Lassen Sie sich von den Finanzberichten in der Firma CRONUS inspirieren.

    > [!NOTE]
    > Im Feld **Zeilennr.** Das Feld Kostenarten zeigt die ersten 10 Zeichen eines Bezeichners, z.B. einer Kontonummer. Wenn Sie Bezeichner hinzufügen, die mit denselben 10 Zeichen beginnen, enthält das Feld **Zeilennr.** Duplikate Feld Bei Bedarf können Sie die Bezeichner manuell bearbeiten, nachdem Sie die Elemente eingefügt haben. Die vollständigen Bezeichner werden im Feld **Zusammenzählung** angezeigt.

7. Wählen Sie auf der Seite **Finanzberichte** die Aktion **Finanzbericht bearbeiten**, um auf den resultierenden Finanzbericht zuzugreifen.
8. Wählen Sie auf der Seite **Finanzbericht** im Feld **Spaltendefinition** eine andere Spaltendefinition, um die Finanzdaten nach anderen Parametern zu untersuchen.
9. Wählen Sie **OK** aus.

Sie haben jetzt die Basis des folgenden Finanzberichts definiert, die Zeilen mit den anzuzeigenden Finanzdaten und ein vorhandenes Layout von Spalten, um die Daten in den Zeilen mit angepassten Parametern anzuzeigen. Wenn die Standard-Spaltendefinition, die Sie in Schritt 4 ausgewählt haben, nicht für Ihre Zwecke geeignet ist, folgen Sie den Schritten in [Eine Spaltendefinition bearbeiten](#edit-a-column-definition).

### <a name="edit-a-column-definition"></a>Bearbeiten Sie eine Spaltendefinition

Verwenden Sie Spaltendefinitionen, um die Spalten anzugeben, die in den Bericht aufgenommen werden sollen. Zum Beispiel können Sie ein Layout gestalten, das Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres vergleicht. Sie können bis zu 15 Spalten verwenden, was z.B. nützlich ist, wenn Sie Budgets für 12 Monate mit einer Spalte für die Gesamtsumme anzeigen möchten.

> [!NOTE]
> Eine gedruckte/vorgezeigte/gespeicherte Version eines Finanzberichts zeigt maximal fünf Spalten an. Wenn ein Finanzbericht dagegen nur für die Analyse auf der Seite **Finanzbericht** gedacht ist, können Sie so viele Spalten erstellen, wie Sie möchten.

1. Wählen Sie auf der Seite **Finanzberichte** den entsprechenden Finanzbericht aus und wählen Sie dann die Aktion **Spaltendefinition bearbeiten**.
2. Erstellen Sie auf der Seite **Spaltendefinition** eine Zeile für jede Spalte mit Finanzdaten, die im Finanzbericht angezeigt wird. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Wählen Sie **OK** aus.
4. Öffnen Sie die Seite **Finanzbericht** von Zeit zu Zeit, um zu überprüfen, ob die neue Spalte wie gewünscht funktioniert.

> [!NOTE]
> Die Spalten, die Sie in jeder Zeile definieren, entsprechen den Spalten drei und höher auf der Seite **Finanzbericht**. Die ersten beiden Spalten, **Zeilennr.** und **Beschreibung**, sind fest.  

### <a name="create-a-column-that-calculates-percentages"></a>Erstellen Sie eine Spalte zur Berechnung von Prozentsätzen

Manchmal möchten Sie vielleicht eine Spalte in einen Finanzbericht einfügen, um Prozentsätze einer Summe zu berechnen. Wenn beispielsweise Zeilen vorhanden sind, die den Umsatz nach Dimensionen aufschlüsseln, empfiehlt sich die Einrichtung einer Spalte, die den prozentualen Anteil an den Gesamtverkäufen in jeder Zeile angibt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 2.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Finanzberichte** einen Finanzbericht aus.  
3. Wählen Sie die Aktion **Finanzbericht bearbeiten**, um eine Finanzberichtszeile festzulegen, um die Summe zu berechnen, auf der die Prozentsätze basieren sollen.  
4. Fügen Sie eine Zeile unmittelbar über der ersten Zeile ein, für die Sie einen Prozentsatz anzeigen möchten.  
5. Füllen Sie die Felder in der Zeile wie folgt aus: In dem Feld **Zusammenzählungsart** geben Sie **Festgelegte Basis für Prozent** ein. Geben Sie in das Feld **Summenbildung** eine Formel für die Summe ein, auf der der Prozentsatz basieren soll. Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.  
6. Wählen Sie die Aktion **Spaltendefinition bearbeiten**, um eine Spalte festzulegen.  
7. Füllen Sie die Felder in der Zeile wie folgt aus: Wählen Sie im Feld **Spaltenart** **Formel** aus. Geben Sie in das Feld **Formel** eine Formel für den Betrag ein, für den Sie einen Prozentsatz berechnen möchten, gefolgt von dem Prozentzeichen (%). Wenn also die Spalte Nummer N die Nettoveränderung enthält, geben Sie **N%** ein.  
8. Wiederholen Sie die Schritte 4 bis 7 für jede Gruppe von Zeilen, die Sie nach Prozentsätzen aufschlüsseln möchten.

## <a name="set-up-financial-reports-with-overviews"></a>Einrichten von Finanzberichten mit Übersichten

Mit einem Finanzbericht können Sie eine Übersicht erstellen, in der Sie die Zahlen des Hauptbuchs mit den Budgetzahlen vergleichen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Finanzberichte** einen Finanzbericht aus.  
3. Wählen Sie die Aktion **Zeilendefinition bearbeiten**  
4. Wählen Sie auf der Seite **Zeilendefinition** im Feld **Name** den Standardnamen des Finanzberichts.
5. Wählen Sie die Aktion **Sachkonten einfügen** aus.  
6. Wählen Sie die Konten aus, die Sie in Ihren Auszug aufnehmen möchten, und wählen Sie dann **OK**.

    Die Konten werden nun in Ihren Finanzbericht eingefügt. Wenn Sie möchten, können Sie auch die Definition der Spalte ändern.  
7. Wählen Sie die Aktion **Finanzbericht bearbeiten**.  
8. Legen Sie auf der Seite **Finanzbericht** auf dem Inforegister **Dimensionen** den Budgetfilter auf den Namen des Filters fest, den Sie verwenden möchten.  
9. Wählen Sie **OK** aus.  

Die Budgetaufstellung kann nun kopiert und in ein Arbeitsblatt eingefügt werden.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Vergleich von Buchhaltungsperioden mit Hilfe von Periodenformeln

Ihr Finanzbericht kann die Ergebnisse verschiedener Buchhaltungsperioden vergleichen, z.B. den vergangenen Monat mit dem gleichen Monat des Vorjahres. Öffnen Sie dazu die Seite **Spaltendefinition** und personalisieren Sie sie, indem Sie das Feld **Vergleich Periodenformel** als Spalte hinzufügen. Erfahren Sie mehr unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md). Sie können dieses Feld dann auf eine Periodenformel setzen.  

Ein Buchhaltungszeitraum muss nicht mit dem Kalender übereinstimmen. Jedes Geschäftsjahr muss jedoch dieselbe Anzahl von Buchhaltungsperioden aufweisen, selbst wenn jede Periode eine andere Länge haben kann.  

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet die Periodenformel, um die Dauer der Vergleichsperiode im Verhältnis zu der Periode zu berechnen, die durch den Datumsfilter im Bericht dargestellt wird. Die Vergleichsperiode basiert auf der Periode des Startdatums des Datumsfilters. Für Periodenspezifikationen stehen folgende Abkürzungen zur Verfügung:

| Abkürzung | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode.                                                                                |
| EP           | Endperiode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.                                   |
| CP           | Laufende Periode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres. Verwenden Sie CP in Formeln, um den Zeitraum festzulegen, in dem die Formel beginnt oder endet. Zum Beispiel FY \[1..CP\] bezeichnet die Zeit vom Beginn des laufenden Geschäftsjahres bis zur laufenden Periode.|
| GJ           | Geschäftsjahr. Zum Beispiel bezeichnet FY\[1..3\] das erste Quartal des aktuellen Geschäftsjahres. |

Beispiele für Formeln:

| Formel         | Description                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Aktueller Zeitraum.                                                                                  |
| \-1P            | Vorherige Periode.                                                                                 |
| \-1GJ\[1..EP\]  | Gesamtes vorheriges Geschäftsjahr.                                                                     |
| \-1GJ           | Aktuelle Periode im vorherigen Geschäftsjahr.                                                          |
| \-1GJ\[1..3\]   | Erstes Quartal des vorangegangenen Geschäftsjahres.                                                           |
| \-1GJ\[1..LP\]  | Vom Beginn des vorherigen Geschäftsjahres bis zur aktuellen Periode im vorherigen Geschäftsjahr, einschließlich beider Perioden. |
| \-1GJ\[LP..EP\] | Von der aktuellen Periode im vorigen Geschäftsjahr bis zur letzten Periode des vorigen Geschäftsjahres, einschließlich beider Perioden.   |

Wenn die Berechnung gemäß regulärer Zeitperioden erfolgen soll, muss eine Formel in das Feld **Vergleichsdatumsformel** eingegeben werden. Wenn das Feld z.B. auf -1Y festgelegt ist, bezieht sich [!INCLUDE [prod_short](includes/prod_short.md)] auf die gleiche Periode ein Jahr zuvor.

> [!NOTE]
> Es ist nicht immer transparent, welche Perioden Sie vergleichen, denn Sie können in einem Bericht einen Datumsfilter festlegen, der sich auf andere Daten erstreckt als die Buchhaltungsperioden, die im Kontenplan angegeben sind. Wenn Sie also einen Finanzbericht erstellen, in dem Sie diese Periode mit der gleichen Periode im Vorjahr vergleichen möchten, legen Sie das Feld **Vergleichsdatum Formel** auf *-1FY* fest. Dann führen Sie den Bericht am 28. Februar aus und legen die Datumsfilter des Januar und Februar fest. Infolgedessen vergleicht der Finanzbericht den Januar und Februar dieses Jahres mit dem Januar des letzten Jahres, der die einzige abgeschlossene Buchhaltungsperiode des letzten Jahres ist.  

Erfahren Sie mehr unter [Arbeiten mit Kalenderdaten und -zeiten](ui-enter-date-ranges.md).

## <a name="print-and-save-financial-reports"></a>Finanzberichte drucken und speichern

Sie können Finanzberichte über die Druckdienste Ihres Geräts ausdrucken. [!INCLUDE[prod_short](includes/prod_short.md)] bietet außerdem die Möglichkeit Berichte als Microsoft Excel Arbeitsmappen, Microsoft Word Dokumente, PDF- und XML-Dateien zu speichern.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
2. Auf der Seite **Finanzberichte** wählen Sie den zu druckenden Bericht aus und wählen dann die Aktion **Drucken**.
3. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie im Feld **Drucker** das Gerät, an das der Bericht gesendet werden soll.
    1. Die Option **(Vom Browser verwaltet)** zeigt an, dass es keinen bestimmten Drucker für den Bericht gibt. In diesem Fall übernimmt der Browser den Ausdruck und zeigt die Standard-Druckschritte an, bei denen Sie einen lokalen Drucker auswählen können, der mit Ihrem Gerät verbunden ist. **(Vom Browser gehandhabt)** ist nicht verfügbar in der mobilen App von [!INCLUDE[prod_short](includes/prod_short.md)] oder der App für Microsoft Teams.
5. Wählen Sie die Aktion **Drucken** aus.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Planen Sie einen Finanzbericht oder speichern Sie ihn als PDF-, Word- oder Excel-Dokument

Ein Finanzbericht kann als Datei in verschiedenen Formaten gespeichert werden, z. B. als PDF, XML, Word oder Excel. Alternativ können Sie [!INCLUDE[prod_short](includes/prod_short.md)] festlegen, um wiederkehrende Finanzberichte zu erstellen:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Finanzberichte** die Aktion **Drucken**.
3. Legen Sie den Bericht entsprechend fest und wählen Sie dann die Aktion **Senden an**.
4. Wählen Sie das Dateiformat oder die Aktion **Zeitplan** und wählen Sie **OK**.
5. Um einen geplanten oder wiederkehrenden Finanzbericht zu erstellen, füllen Sie die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * Für wiederkehrende Finanzberichte legen Sie in den Feldern **Frühestes Startdatum/Uhrzeit** und **Ablaufdatum/Uhrzeit** das erste bzw. letzte Datum für die Erstellung des Finanzberichts fest. Legen Sie außerdem fest, an welchen Tagen der Bericht erstellt werden soll, indem Sie das Feld **Nächstes Ausführungsdatum Formel** entsprechend dem im Abschnitt [Verwendung von Datumsformeln](ui-enter-date-ranges.md#use-date-formulas) erläuterten Format festlegen.

## <a name="importing-or-exporting-financial-reports"></a>Importieren oder Exportieren von Finanzberichten

Sie können Finanzberichte als RapidStart-Konfigurationspakete importieren und exportieren, die z.B. für die gemeinsame Nutzung der Informationen mit anderen Firmen nützlich sind. Das Paket wird in einer .rapidstart-Datei erstellt, die den Inhalt komprimiert.

### <a name="import-and-export-financial-reports"></a>Finanzberichte importieren und exportieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 4.](media/ui-search/search_small.png "Was möchten Sie tun?") öffnet. Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Finanzbericht und wählen Sie dann die Aktion **Finanzbericht importieren** oder **Finanzbericht exportieren**, je nachdem, was Sie tun möchten.

> [!NOTE]
> Wenn Sie Finanzberichte importieren, werden bestehende Datensätze mit dem gleichen Namen wie die zu importierenden gelöscht.

## <a name="see-also"></a>Siehe auch

[Berichte ausführen und drucken](ui-work-report.md)  
[Financial Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Das Hauptbuch und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
