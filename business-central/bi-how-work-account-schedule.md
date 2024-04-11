---
title: Erstellen von Finanzberichten mit Finanzdaten und Kontokategorien
description: 'Beschreibt, wie Sie mit Finanzberichten verschiedene Ansichten und Berichte zur Analyse von Finanzdaten erstellen können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---
# Finanzberichte mit Finanzdaten und Kontokategorien erstellen

Das Feature **Finanzberichte** gibt Ihnen Einblick in die in Ihrem Kontenplan (COA) enthaltenen Finanzdaten. Sie können Finanzberichte einrichten, um die Zahlen in den Finanzbuchhaltungskonten zu analysieren und Sachposten mit Budgetposten zu vergleichen. Die Ergebnisse werden in Diagrammen und Berichten in Ihrem Rollencenter angezeigt, darunter der Cashflowplan sowie die GuV- und Bilanzberichte. Auf diese beiden Berichte greifen Sie z. B. mit der Aktion **Finanzauswertungen** in den Homepages für Geschäftsleiter und Buchhalter zu.  

[!INCLUDE[prod_short](includes/prod_short.md)] bietet Ihnen Beispielfinanzberichte, die Sie sofort als Vorlagen verwenden können. Sie können auch Ihre eigenen Berichte einrichten, um die zu vergleichenden Zahlen anzugeben. Sie können zum Beispiel Finanzberichte erstellen, um Gewinnspannen anhand von Dimensionen wie Abteilungen oder Kundengruppen zu berechnen. Die Anzahl der Finanzberichte, die vie erstellen können, ist unbegrenzt, und Sie brauchen keine Unterstützung von der Entwicklung.  

## Voraussetzungen für Finanzberichte

Das Einrichten von Finanzberichten erfordert ein Verständnis der Struktur Ihres Kontenplans. Es gibt drei Schlüsselkonzepte, auf die Sie wahrscheinlich achten müssen, bevor Sie Ihre Finanzberichte entwerfen:

- Ordnen Sie Sachbuchungen den Finanzbuchkontokategorien zu.
- Legen Sie fest, wie Sie Dimensionen verwenden wollen.
- Legen Sie Finanzbuchhaltungsbudgets fest.

Finanzbuchkontokategorien vereinfachen Ihre Finanzberichtsdefinitionen und machen sie widerstandsfähiger gegenüber Änderungen in der Kontenplanstruktur. Weitere Informationen finden Sie unter [Finanzbuchkontokategorien zum Ändern des Layouts Ihrer Finanzberichte verwenden](#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

Durch das Einrichten von Dimensionen können Sie Ihre Finanzdaten auf eine für Ihr Unternehmen sinnvolle Weise aufteilen. Erfahren Sie mehr unter [Arbeiten mit Dimensionen](finance-dimensions.md). 

Wenn Sie Sachposten als Prozentsätze von Budgetposten anzeigen möchten, müssen Sie Finanzbuchhaltungsbudgets erstellen. Erfahren Sie mehr unter [Sachkontenbudgets erstellen](finance-how-create-budgets.md).

## Finanzberichte

In Finanzberichten werden die Konten aus Ihrem Kontenplan so angeordnet, dass die Daten einfacher dargestellt werden können. Sie können verschiedene Layouts festlegen, um die Informationen zu definieren, die Sie aus dem Kontenplan extrahieren möchten. Finanzberichte bieten darüber hinaus einen Platz für Berechnungen, die nicht direkt im Kontenplan vorgenommen werden können. Sie können beispielsweise Zwischensummen für Gruppen von Konten erstellen und diese Summe dann in andere Summen aufnehmen. Ein weiteres Beispiel ist die Berechnung von Gewinnmargen für Dimensionen wie Abteilungen oder Debitorengruppen. Außerdem können Sie Hauptbuch- und Budgetbuchungen filtern, z.B. nach Nettoänderung oder Sollbetrag.

> [!NOTE] 
> Stellen Sie sich einen Finanzbericht in mathematischer Hinsicht so vor, dass er durch zwei Dinge definiert wird:
>
> - Ein Vektor aus Zeilendefinitionen, die festlegen, was berechnet werden muss.
> - Ein Vektor aus Spaltendefinitionen, der die Daten für die Berechnung festlegt.
>
> Der Finanzbericht ist dann das äußere Produkt dieser beiden Vektoren, wobei jeder Zellenwert gemäß der Formel in der Zeile berechnet wird, die auf die Datendefinition aus der Spalte angewendet wird.

:::image type="content" source="media/financial-report-definition.svg" alt-text="Zeigt, wie ein Finanzbericht aus einer Zeilendefinition und einer Spaltendefinition erstellt wird." lightbox="media/financial-report-definition.svg":::

Die Seite **Finanzberichte** zeigt, dass alle Finanzberichte einem Muster folgen, das aus den folgenden Attributen besteht:

* Name (Code)
* Description
* Zeilendefinition
* Spaltendefinition

:::image type="content" source="media/financial-reports.png" alt-text="Zeigt, dass alle Finanzberichte aus einer Zeilendefinition und einer Spaltendefinition erstellt werden." lightbox="media/financial-reports.png":::

> [!NOTE]
> Die Beispielfinanzberichte in [!INCLUDE[prod_short](includes/prod_short.md)] sind nicht sofort einsatzbereit. Je nachdem, wie Sie Ihre Finanzbuchhaltungskonten, Dimensionen, Finanzbuchhaltungskontokategorien und Budgets einrichten, müssen Sie die Beispielzeilen- und -spaltendefinitionen sowie die Finanzberichte, in denen sie verwendet werden, an Ihre Einrichtung anpassen.

Sie können auch Formeln verwenden, um zwei oder mehr Finanzberichte und Spaltendefinitionen zu vergleichen. Mit Vergleichen können Sie Folgendes tun:

* Erstellen benutzerdefinierter Finanzberichte
* Erstellen Sie so viele Finanzberichte wie Sie benötigen, jeder mit einem eindeutigen Namen.
* Einrichten unterschiedlicher Berichtslayouts und Drucken der Berichte mit den aktuellen Werten

## Lernpfad: Erstellen von Finanzberichten in Microsoft Dynamics 365 Business Central

Möchten Sie lernen, wie Sie Budgets erstellen und dann Finanzberichte, Dimensionen sowie Zeilen- und Spaltendefinitionen verwenden, um die Finanzberichte zu erstellen, welche die meisten Unternehmen normalerweise benötigen?

Fangen Sie mit dem Lernpfad [Erstellen von Finanzberichten in Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central) an

## Erstellen Sie einen neuen Finanzbericht

Sie verwenden Finanzberichte, um Hauptbuchkonten zu analysieren oder Hauptbucheinträge mit Budgeteinträgen zu vergleichen. Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten sehen.

Die Finanzberichte in der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] entsprechen möglicherweise nicht den Anforderungen Ihres Unternehmens. Um schnell eigene Finanzberichte zu erstellen, beginnen Sie mit dem Kopieren eines bestehenden Berichts, wie in Schritt drei unten beschrieben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.  
1. Auf der Seite **Finanzberichte** wählen Sie die Aktion **Neu**, um einen neuen Finanzbericht zu erstellen. Alternativ können Sie die Einstellungen eines bestehenden Finanzberichts wiederverwenden, indem Sie die Aktion **Finanzbericht kopieren** auswählen.
1. Geben Sie den Kurznamen des Berichts (dieser kann nicht geändert werden) und die Beschreibung ein.
1. Wählen Sie eine Zeilendefinition und eine Spaltendefinition aus.
1. Wählen Sie für die Zeilen- und Spaltendefinitionen optional Analyseansichten aus.
1. Wählen Sie die Aktion **Finanzbericht bearbeiten** aus, um im Finanzbericht auf mehr Eigenschaften zuzugreifen.
1. Auf dem Inforegister **Optionen** können Sie die Berichtsbeschreibung bearbeiten, die Zeilen- und Spaltendefinitionen ändern und festlegen, wie Datumsangaben angezeigt werden. Datumsangaben können in der Hierarchie Tag/Woche/Monat/Quartal/Jahr angegeben sein oder Sie können Buchhaltungsperiode verwenden. Mehr erfahren Sie unter [Vergleich von Buchhaltungsperioden mit Hilfe von Periodenformeln](#comparing-accounting-periods-using-period-formulas)
1. Auf dem Inforegister **Dimensionen** können Sie Dimensionsfilter für den Bericht festlegen.
1. Sie können eine Vorschau des Berichts im Bereich unterhalb des Inforegisters **Dimensionen** anzeigen lassen.

> [!TIP]
> Nachdem Sie einen Finanzbericht erstellt haben, können Sie die Seite **Finanzbericht** verwenden, um sich eine Vorschau anzeigen zu lassen und ihn zu überprüfen. Um die Seite zu öffnen, wählen Sie die Aktion **Finanzbericht anzeigen**.  

> [!NOTE]
> Wenn Sie einen Finanzbericht im Ansichts- oder Bearbeitungsmodus öffnen, ist der Bereich Filter verfügbar. Verwenden Sie nicht den Filterbereich, um Filter für die Daten in Ihrem Bericht festzulegen. Solche Filter können Fehler verursachen oder filtern die Daten eventuell nicht wirklich. Verwenden Sie stattdessen die Felder in den Inforegistern **Optionen** und **Dimensionen**, um Filter für den Bericht einzurichten.

### Eine Zeilendefinition erstellen oder bearbeiten

Zeilendefinitionen in Finanzberichten bieten einen Platz für Berechnungen, die nicht direkt im Kontenplan vorgenommen werden können. Sie können beispielsweise Zwischensummen für Gruppen von Konten erstellen und diese Summe dann in andere Summen aufnehmen. Dabei können auch Zwischenschritte berechnet werden, die im abschließenden Bericht nicht erscheinen.

1. Wählen Sie auf der Seite **Finanzberichte** den entsprechenden Finanzbericht und dann die Aktion **Zeilendefinition bearbeiten** aus.
1. Wählen Sie die Aktionen **Sachkonten einfügen**, **KF-Konten einfügen** und **Kostenarten einfügen**, um eine Zeile für jedes Finanzelement zu erstellen, das Sie analysieren möchten. Beispielsweise könnten Sie eine Zeile für Umlaufvermögen und eine andere für Anlagevermögen haben. Lassen Sie sich von den Finanzberichten im Demounternehmen CRONUS inspirieren.

    > [!NOTE]
    > Im Feld **Zeilennr.** Das Feld Kostenarten zeigt die ersten 10 Zeichen eines Bezeichners, z.B. einer Kontonummer. Wenn Sie Bezeichner hinzufügen, die mit denselben 10 Zeichen beginnen, enthält das Feld **Zeilennr.** Duplikate. Feld Bei Bedarf können Sie die Bezeichner manuell bearbeiten, nachdem Sie die Elemente eingefügt haben. Die vollständigen Bezeichner werden im Feld **Zusammenzählung** angezeigt.

> [!NOTE]
> Die Spalten, die Sie in jeder Zeile der Zeilendefinition festlegen, entsprechen den Spalten drei und höher auf der Seite **Finanzbericht**. Die ersten beiden Spalten, **Zeilennr.** und **Beschreibung**, sind fest.  

### Eine Spaltendefinition erstellen oder bearbeiten

Verwenden Sie Spaltendefinitionen, um die Spalten anzugeben, die in den Bericht aufgenommen werden sollen. Zum Beispiel können Sie ein Berichtslayout gestalten, das Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres vergleicht. Eine Spaltendefinition kann bis zu 15 Spalten umfassen. Zum Beispiel sind mehrere Spalten sinnvoll, wenn Sie Budgets für zwölf Monate mit einer Spalte für die Gesamtsumme anzeigen möchten.

> [!NOTE]
> Eine gedruckte/vorgezeigte/gespeicherte Version eines Finanzberichts zeigt maximal fünf Spalten an. Wenn ein Finanzbericht dagegen nur für die Analyse auf der Seite **Finanzbericht** gedacht ist, können Sie so viele Spalten erstellen, wie Sie möchten.

1. Wählen Sie auf der Seite **Finanzberichte** den entsprechenden Finanzbericht aus und wählen Sie dann die Aktion **Spaltendefinition bearbeiten**.
1. Erstellen Sie auf der Seite **Spaltendefinition** eine Zeile für jede Spalte mit Finanzdaten, die im Finanzbericht angezeigt wird. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Wählen Sie **OK** aus.
1. Öffnen Sie die Seite **Finanzbericht** von Zeit zu Zeit, um zu überprüfen, ob die neue Spalte wie gewünscht funktioniert.

### Eine Spaltendefinition zur Berechnung von Prozentsätzen erstellen

Vielleicht möchten Sie eine Spalte in einen Finanzbericht einfügen, um Prozentsätze einer Summe zu berechnen. Wenn beispielsweise Zeilen vorhanden sind, die den Umsatz nach Dimensionen aufschlüsseln, empfiehlt sich die Einrichtung einer Spalte, die den prozentualen Anteil an den Gesamtverkäufen in jeder Zeile angibt.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 2.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie auf der Seite **Finanzberichte** einen Finanzbericht aus.  
1. Wählen Sie die Aktion **Finanzbericht bearbeiten**, um eine Finanzberichtszeile festzulegen, um die Summe zu berechnen, auf der die Prozentsätze basieren.  
1. Fügen Sie eine Zeile unmittelbar über der ersten Zeile hinzu, für die Sie einen Prozentsatz anzeigen möchten.  
1. Füllen Sie die Felder in der Zeile wie folgt aus: In dem Feld **Zusammenzählungsart** geben Sie **Festgelegte Basis für Prozent** ein. Geben Sie in das Feld **Summenbildung** eine Formel für die Summe ein, auf der der Prozentsatz basieren soll. Wenn beispielsweise Zeile 11 die gesamten Verkäufe enthält, geben Sie **11** ein.  
1. Wählen Sie die Aktion **Spaltendefinition bearbeiten**, um eine Spalte festzulegen.  
1. Füllen Sie die Felder in der Zeile wie folgt aus. Wählen Sie im Feld **Spaltenart** den Eintrag **Formel** aus. Geben Sie in das Feld **Formel** eine Formel für den Betrag ein, für den Sie einen Prozentsatz berechnen möchten, gefolgt von dem Prozentzeichen (%). Wenn also die Spalte Nummer N die Nettoveränderung enthält, geben Sie **N%** ein.  
1. Wiederholen Sie die Schritte 4 bis 7 für jede Gruppe von Zeilen, die Sie nach Prozentsätzen aufschlüsseln möchten.

## Mithilfe von Finanzbuchhaltungskontokategorien das Layout Ihrer Finanzaufstellungen ändern

Sie können Sachkontokategorien dazu verwenden, das Layout Ihrer Finanzberichte zu ändern. Nachdem Sie beispielsweise Ihre Kontokategorien auf der Seite **Finanzbuchhaltungskontokategorien** festgelegt haben, können Sie die Aktion **Finanzberichte generieren** wählen und die zugrundeliegenden Finanzberichte für die Kernfinanzberichte aktualisieren. Wenn Sie dann das nächste Mal einen dieser Berichte ausführen, z. B. den Bericht **Bilanz**, werden neue Summen und Untereinträge hinzugefügt.

Ein weiterer Vorteil der Verwendung von Finanzbuchhaltungskontokategorien anstatt reiner Finanzbuchhaltungskonten in Ihren Zeilendefinitionen besteht darin, dass sich eine Änderung der Struktur Ihres Kontenplans nicht auf Ihre Finanzberichte auswirkt.

> [!NOTE]
> Die Kontokategorien der obersten Ebene, wie z. B. der Knoten **Verbindlichkeiten**, sind fest vorgegeben, und Sie können keine eigenen hinzufügen. Sie können jedoch Kontenkategorien auf niedrigeren Ebenen löschen und hinzufügen und festlegen, wie der zugehörige Finanzbericht in Berichten erscheint.
>
> Sie sollten Ihre eigenen Sachkonto-Kategorien auf unterer Ebene von Grund auf erstellen und strukturieren, ggf. in einer Hierarchie, anstatt zu versuchen, die vorhandenen Kategorien neu anzuordnen. Sie können beispielsweise den Knoten **Verbindlichkeiten** neu strukturieren, sodass er den neuen Knoten **Eigenkapital** gefolgt von den Knoten **Kurzfristige Verbindlichkeiten** und **Langfristige Verbindlichkeiten** enthalten. Weitere Informationen finden Sie unter [Finanzbuchhaltungskonten Kontokategorien zuordnen](finance-general-ledger.md#account-categories).

## Dimensionen in Finanzberichten verwenden

In der Finanzanalyse sind Dimensionen Daten, die Sie einem Eintrag als eine Art Markierung hinzufügen. Diese Daten dienen zum Gruppieren von Posten mit ähnlichen Merkmalen – beispielsweise Debitoren, Regionen, Produkte oder Verkäufer – sowie zum einfachen Abrufen dieser Gruppen zur Analyse. Sie können Dimensionen für Posten in Buch.-Blättern, Belegen und Budgets verwenden.

Jede Dimension beschreibt den Schwerpunkt der Analyse. Eine zweidimensionale Analyse wäre z.B. der Umsatz pro Bereich. Wenn Sie beim Erstellen eines Postens mehr als zwei Dimensionen verwenden, können Sie eine komplexere Analyse durchführen. Ein Beispiel für eine komplexe Analyse ist die Untersuchung der Verkäufe pro Verkaufskampagne, Debitorengruppe und Region. So erhalten Sie einen besseren Einblick in Ihr Unternehmen, z. B. wie gut Ihr Geschäft läuft, wo es floriert und wo nicht und wo Sie mehr Ressourcen zuweisen sollten. Mithilfe dieser Einblicke können Sie fundiertere Geschäftsentscheidungen treffen. Unter [Arbeiten mit Dimensionen](finance-dimensions.md) erfahren Sie mehr.

## Einrichten von Finanzberichten mit Übersichten

Mit einem Finanzbericht können Sie eine Übersicht erstellen, in der Sie die Zahlen der Finanzbuchhaltung mit denen des Budgets vergleichen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie auf der Seite **Finanzberichte** einen Finanzbericht aus.  
1. Wählen Sie die Aktion **Zeilendefinition bearbeiten**  
1. Wählen Sie auf der Seite **Zeilendefinition** im Feld **Name** den Standardnamen des Finanzberichts.
1. Wählen Sie die Aktion **Sachkonten einfügen** aus.  
1. Wählen Sie die Konten aus, die Sie in Ihren Auszug aufnehmen möchten, und wählen Sie dann **OK**.

    Die Konten werden in Ihrem Finanzbericht eingefügt. Wenn Sie möchten, können Sie auch die Definition der Spalte ändern.  
1. Wählen Sie die Aktion **Finanzbericht bearbeiten**.  
1. Legen Sie auf der Seite **Finanzbericht** auf dem Inforegister **Dimensionen** den Budgetfilter auf den Namen des Filters fest, den Sie verwenden möchten.  
1. Wählen Sie **OK** aus.  

Die Budgetaufstellung kann nun kopiert und in ein Arbeitsblatt eingefügt werden.  

## Vergleich von Buchhaltungsperioden mit Hilfe von Periodenformeln

Ihr Finanzbericht kann die Ergebnisse verschiedener Buchhaltungsperioden vergleichen, z.B. den vergangenen Monat mit dem gleichen Monat des Vorjahres. Öffnen Sie dazu die Seite **Spaltendefinition** und personalisieren Sie sie, indem Sie das Feld **Vergleich Periodenformel** als Spalte hinzufügen. Erfahren Sie mehr unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md). Sie können dieses Feld dann auf eine Periodenformel setzen.  

Ein Buchhaltungszeitraum muss nicht mit dem Kalender übereinstimmen. Jedes Geschäftsjahr muss jedoch dieselbe Anzahl von Buchhaltungsperioden aufweisen, selbst wenn jede Periode eine andere Länge haben kann.  

[!INCLUDE[prod_short](includes/prod_short.md)] verwendet die Periodenformel, um die Dauer der Vergleichsperiode im Verhältnis zu der Periode zu berechnen, die durch den Datumsfilter im Bericht dargestellt wird. Die Vergleichsperiode basiert auf der Periode des Startdatums des Datumsfilters. Für Periodenspezifikationen stehen folgende Abkürzungen zur Verfügung:

| Abkürzung | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode.                                                                                |
| EP           | Endperiode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres.                                   |
| CP           | Laufende Periode eines Geschäftsjahres, eines Halbjahres oder eines Vierteljahres. Verwenden Sie CP in Formeln, um den Zeitraum festzulegen, in dem die Formel beginnt oder endet. Zum Beispiel FY\[1..CP\] bezeichnet die Zeit vom Beginn des laufenden Geschäftsjahres bis zur laufenden Periode.|
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

## Finanzberichte drucken und speichern

Sie können Finanzberichte über die Druckdienste Ihres Geräts ausdrucken. [!INCLUDE[prod_short](includes/prod_short.md)] bietet außerdem die Möglichkeit, Berichte als Excel-Arbeitsmappen, Word-Dokumente, PDF- und XML-Dateien zu speichern.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Auf der Seite **Finanzberichte** wählen Sie den zu druckenden Bericht aus und wählen dann die Aktion **Drucken**.
1. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Wählen Sie im Feld **Drucker** das Gerät, an das der Bericht gesendet werden soll.
    1. Die Option **(Vom Browser verwaltet)** zeigt an, dass es keinen bestimmten Drucker für den Bericht gibt. In diesem Fall übernimmt der Browser den Ausdruck und zeigt die Standard-Druckschritte an, bei denen Sie einen lokalen Drucker auswählen können, der mit Ihrem Gerät verbunden ist. **(Vom Browser gehandhabt)** ist in der mobilen [!INCLUDE[prod_short](includes/prod_short.md)] App oder der App für Teams nicht verfügbar.
1. Wählen Sie die Aktion **Drucken** aus.

### Planen Sie einen Finanzbericht oder speichern Sie ihn als PDF-, Word- oder Excel-Dokument

Ein Finanzbericht kann als Datei in verschiedenen Formaten gespeichert werden, z. B. als PDF, XML, Word oder Excel. Alternativ kann [!INCLUDE[prod_short](includes/prod_short.md)] wiederkehrende Finanzberichte generieren:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie auf der Seite **Finanzberichte** die Aktion **Drucken**.
1. Legen Sie den Bericht entsprechend fest und wählen Sie dann die Aktion **Senden an**.
1. Wählen Sie das Dateiformat oder die Aktion **Zeitplan** und wählen Sie **OK**.
1. Um einen geplanten oder wiederkehrenden Finanzbericht zu erstellen, füllen Sie die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Für wiederkehrende Finanzberichte legen Sie in den Feldern **Frühestes Startdatum/Uhrzeit** und **Ablaufdatum/Uhrzeit** das erste bzw. letzte Datum für die Erstellung des Finanzberichts fest. Legen Sie außerdem fest, an welchen Tagen der Bericht erstellt werden soll, indem Sie das Feld **Nächstes Ausführungsdatum Formel** entsprechend dem im Abschnitt [Verwendung von Datumsformeln](ui-enter-date-ranges.md#use-date-formulas) erläuterten Format festlegen.

## Finanzberichtsdimensionen importieren oder exportieren

Sie können Finanzberichts- bzw. Zeilendefinitionen als RapidStart-Konfigurationspakete importieren und exportieren, die z. B. nützlich sind, wenn die Informationen an andere Unternehmen weitergegeben werden sollen. Das Paket wird in einer .rapidstart-Datei erstellt, die den Inhalt komprimiert.

> [!NOTE]
> Wenn Sie Finanzberichts- bzw. Zeilendefinitionen importieren, werden bestehende Datensätze mit dem gleichen Namen wie die zu importierenden durch die neuen Definitionen ersetzt. Beachten Sie, dass das Konfigurationspaket für eine Berichtsdefinition keine vorhandenen Zeilen- oder Spaltendefinitionen überschreibt, die in der Berichtsdefinition verwendet werden.

Um Finanzberichtsdefinitionen zu importieren oder zu exportieren, gehen Sie wie folgt vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 4 öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie den Finanzbericht und wählen Sie dann die Aktion **Finanzbericht importieren** oder **Finanzbericht exportieren**, je nachdem, was Sie tun möchten.

Um Finanzberichtszeilendefinitionen zu importieren oder zu exportieren, gehen Sie wie folgt vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Zeilendefinitionen** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie die Zeilendefinition und dann die Aktion **Zeilendefinition importieren** oder **Zeilendefinition exportieren** aus, je nachdem, was Sie tun möchten.

## Siehe auch

[Berichte ausführen und drucken](ui-work-report.md)  
[Financial Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Das Hauptbuch und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
