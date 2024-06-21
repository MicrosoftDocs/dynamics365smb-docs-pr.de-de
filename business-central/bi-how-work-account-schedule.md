---
title: Erstellen von Finanzberichten mit Finanzdaten und Kontokategorien
description: 'Beschreibt, wie Sie mit Finanzberichten verschiedene Ansichten und Berichte zur Analyse von Finanzdaten erstellen können.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: 'Report_25, 103, 104, 108, 195, 196, 197, 198, 488, 489, 490, 764, 765, 766'
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

Finanzbuchkontokategorien vereinfachen Ihre Finanzberichtsdefinitionen und machen sie widerstandsfähiger gegenüber Änderungen in der Kontenplanstruktur. Weitere Informationen finden Sie unter [Finanzbuchkontokategorien zum Ändern des Layouts Ihrer Finanzberichte verwenden](bi-row-definitions.md#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

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

- Name (Code)
- Beschreibung
- Zeilendefinition
- Spaltendefinition

:::image type="content" source="media/financial-reports.png" alt-text="Zeigt, dass alle Finanzberichte aus einer Zeilendefinition und einer Spaltendefinition erstellt werden." lightbox="media/financial-reports.png":::

> [!NOTE]
> Die Beispielfinanzberichte in [!INCLUDE[prod_short](includes/prod_short.md)] sind nicht sofort einsatzbereit. Je nachdem, wie Sie Ihre Finanzbuchhaltungskonten, Dimensionen, Finanzbuchhaltungskontokategorien und Budgets einrichten, müssen Sie die Beispielzeilen- und -spaltendefinitionen sowie die Finanzberichte, in denen sie verwendet werden, an Ihre Einrichtung anpassen.

Sie können auch Formeln verwenden, um zwei oder mehr Finanzberichte und Spaltendefinitionen zu vergleichen. Mit Vergleichen können Sie Folgendes tun:

- Erstellen benutzerdefinierter Finanzberichte
- Erstellen Sie so viele Finanzberichte wie Sie benötigen, jeder mit einem eindeutigen Namen.
- Einrichten unterschiedlicher Berichtslayouts und Drucken der Berichte mit den aktuellen Werten

## Lernpfad: Erstellen von Finanzberichten in Microsoft Dynamics 365 Business Central

Möchten Sie lernen, wie Sie Budgets erstellen und dann Finanzberichte, Dimensionen sowie Zeilen- und Spaltendefinitionen verwenden, um die Finanzberichte zu erstellen, die Unternehmen normalerweise benötigen?

Fangen Sie mit dem folgenden Lernpfad [Erstellen von Finanzberichten in Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central) an.

## Erstellen Sie einen neuen Finanzbericht

Sie verwenden Finanzberichte, um Hauptbuchkonten zu analysieren oder Hauptbucheinträge mit Budgeteinträgen zu vergleichen. Sie können beispielsweise die Sachposten als prozentualen Anteil der Finanzbudgetposten sehen.

Die Finanzberichte in der Standardversion von [!INCLUDE[prod_short](includes/prod_short.md)] entsprechen möglicherweise nicht den Anforderungen Ihres Unternehmens. Um schnell eigene Finanzberichte zu erstellen, beginnen Sie mit dem Kopieren eines bestehenden Berichts, wie in Schritt 3 unten beschrieben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.  
1. Auf der Seite **Finanzberichte** wählen Sie die Aktion **Neu**, um einen neuen Finanzbericht zu erstellen. Alternativ können Sie die Einstellungen eines bestehenden Finanzberichts wiederverwenden, indem Sie die Aktion **Finanzbericht kopieren** auswählen.
1. Geben Sie den Kurznamen des Berichts (Sie können den Namen später nicht mehr ändern) und die Beschreibung ein.
1. Wählen Sie eine Zeilendefinition und eine Spaltendefinition aus.
1. Wählen Sie für die Zeilen- und Spaltendefinitionen optional Analyseansichten aus.
1. Wählen Sie die Aktion **Finanzbericht bearbeiten** aus, um im Finanzbericht auf mehr Eigenschaften zuzugreifen.
1. Auf dem Inforegister **Optionen** können Sie die Berichtsbeschreibung bearbeiten, die Zeilen- und Spaltendefinitionen ändern und festlegen, wie Datumsangaben angezeigt werden. Datumsangaben können in der Hierarchie Tag/Woche/Monat/Quartal/Jahr angegeben sein oder Sie können Buchhaltungsperiode verwenden. Mehr erfahren Sie unter [Vergleich von Buchhaltungsperioden mit Hilfe von Periodenformeln](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas)
1. Auf dem Inforegister **Dimensionen** können Sie Dimensionsfilter für den Bericht festlegen.
1. Sie können eine Vorschau des Berichts im Bereich unterhalb des Inforegisters **Dimensionen** anzeigen lassen.

> [!TIP]
> Nachdem Sie einen Finanzbericht erstellt haben, können Sie die Seite **Finanzbericht** verwenden, um sich eine Vorschau anzeigen zu lassen und ihn zu überprüfen. Um die Seite zu öffnen, wählen Sie die Aktion **Finanzbericht anzeigen**.  

> [!NOTE]
> Wenn Sie einen Finanzbericht im Ansichts- oder Bearbeitungsmodus öffnen, ist der Bereich Filter verfügbar. Verwenden Sie nicht den Filterbereich, um Filter für die Daten in Ihrem Bericht festzulegen. Solche Filter können Fehler verursachen oder filtern die Daten eventuell nicht wirklich. Verwenden Sie stattdessen die Felder in den Inforegistern **Optionen** und **Dimensionen**, um Filter für den Bericht einzurichten.

### Eine Zeilendefinition erstellen oder bearbeiten

Zeilendefinitionen in Finanzberichten bieten einen Platz für Berechnungen, die nicht direkt im Kontenplan vorgenommen werden können. Sie können beispielsweise Zwischensummen für Gruppen von Konten erstellen und diese Summe dann in andere Summen aufnehmen. Dabei können auch Zwischenschritte berechnet werden, die im abschließenden Bericht nicht erscheinen.

Mehr erfahren Sie unter [Zeilendefinitionen in Finanzberichten](bi-row-definitions.md).

### Eine Spaltendefinition erstellen oder bearbeiten

Verwenden Sie Spaltendefinitionen, um die Spalten anzugeben, die in den Bericht aufgenommen werden sollen. Zum Beispiel können Sie ein Berichtslayout gestalten, das Bewegung und Saldo für dieselbe Periode dieses und letzten Jahres vergleicht. Eine Spaltendefinition kann bis zu 15 Spalten umfassen. Zum Beispiel sind mehrere Spalten sinnvoll, wenn Sie Budgets für zwölf Monate mit einer Spalte für die Gesamtsumme anzeigen möchten.

Mehr erfahren Sie unter [Spaltendefinition in Finanzberichten](bi-column-definitions.md).

## Dimensionen in Finanzberichten verwenden

In der Finanzanalyse sind Dimensionen Daten, die Sie einem Eintrag als eine Art Markierung hinzufügen. Diese Daten dienen zum Gruppieren von Posten mit ähnlichen Merkmalen – beispielsweise Debitoren, Regionen, Produkte oder Verkäufer – sowie zum einfachen Abrufen dieser Gruppen zur Analyse. Sie können Dimensionen für Posten in Buch.-Blättern, Belegen und Budgets verwenden.

Jede Dimension beschreibt den Schwerpunkt der Analyse. Eine zweidimensionale Analyse wäre z.B. der Umsatz pro Bereich. Wenn Sie beim Erstellen eines Postens mehr als zwei Dimensionen verwenden, können Sie eine komplexere Analyse durchführen. Ein Beispiel für eine komplexe Analyse ist die Untersuchung der Verkäufe pro Verkaufskampagne, Debitorengruppe und Region. So erhalten Sie einen besseren Einblick in Ihr Unternehmen, z. B. wie gut Ihr Geschäft läuft, wo es floriert und wo nicht und wo Sie mehr Ressourcen zuweisen sollten. Mithilfe dieser Einblicke können Sie fundiertere Geschäftsentscheidungen treffen. Um mehr darüber zu erfahren, gehen Sie zu [Arbeiten mit Dimensionen](finance-dimensions.md).

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

## Finanzberichte in Excel integrieren

Sie können einen Finanzbericht in eine Excel-Arbeitsmappenvorlage integrieren, das Layout an Ihre Anforderungen anpassen und dann die Excel-Vorlage mit Daten aus [!INCLUDE[prod_short](includes/prod_short.md)] aktualisieren. Mithilfe dieser Integration können Sie beispielsweise Ihre monatlichen und jährlichen Finanzberichte einfacher in einem für Sie geeigneten Format erstellen.

### Excel-Integration für einen Finanzbericht einrichten (Excel-Vorlage erstellen)

Um die Excel-Integration für einen Finanzbericht einzurichten, gehen Sie wie folgt vor, um eine Excel-Vorlage für einen Bericht zu erstellen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 4.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") öffnet. Symbol. Geben Sie **Finanzberichte** ein und wählen Sie dann den zugehörigen Link.
1. Wählen Sie auf der Seite **Finanzberichte** den Finanzbericht aus, für den Sie Excel aktivieren möchten, und dann die Aktion **In Excel exportieren** aus.
1. Wählen Sie die Aktion **Neues Dokument erstellen**. Diese Aktion lädt eine Excel-Arbeitsmappenvorlage mit einem einzelnen Arbeitsblatt herunter, das nach dem Berichtsnamen benannt ist.
1. Kopieren Sie das Arbeitsblatt und benennen Sie es in **Daten** um.
1. Benennen Sie das Berichtsarbeitsblatt nach Ihren Wünschen um.
1. Markieren Sie im Berichtsarbeitsblatt alle Zellen, die Daten aus dem Finanzbericht enthalten (einschließlich Spalten- und Zeilenüberschriften). Suchen Sie im Menüband **Start** nach dem Menü **Nummer** und wählen Sie als Format **Allgemein**.
1. Wählen Sie die äußerste linke Zelle des Bereichs mit Daten aus dem Finanzbericht aus und legen Sie einen Verweis auf die entsprechende Zelle im Datenarbeitsblatt fest. Ziehen Sie die Formel nach rechts, um sie auf alle Zellen in der ersten Zeile auszuweiten, und ziehen Sie die Zeile anschließend nach unten, um alle Zeilen im Finanzbericht einzubeziehen.
1. Blenden Sie das Arbeitsblatt **Daten** aus.
1. Formatieren Sie das Berichtsarbeitsblatt nach Ihren Anforderungen.
1. Speichern Sie die Arbeitsmappe in OneDrive oder an einem ähnlichen Ort, an dem die Datei gesichert und versioniert wird.
1. Schließen Sie die Arbeitsmappe.

### Einen Finanzbericht mit einer Excel-Vorlage ausführen

Um einen Finanzbericht mit einer Excel-Vorlage auszuführen, gehen Sie folgendermaßen vor:

1. Wählen Sie das ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Finanzberichte** ein und wählen Sie dann den zugehörigen Link.
1. Wählen Sie auf der Seite **Finanzberichte** den Finanzbericht aus, für den Sie Excel aktivieren möchten, und dann die Aktion **In Excel exportieren** aus.
1. Wählen Sie die Aktion **Kopie des vorhandenen Dokuments aktualisieren** aus.
1. Laden Sie Ihre Excel-Vorlage hoch (schließen Sie die Excel-Arbeitsmappe, bevor Sie sie hochladen).
1. Wählen Sie auf der Seite **Namens-/Wertsuche** das Arbeitsblatt „Daten“ aus.
1. [!INCLUDE[prod_short](includes/prod_short.md)] führt den Finanzbericht aus und führt die sich daraus ergebenden Daten mit Ihrer Excel-Vorlage zusammen.

## Finanzberichte drucken und speichern

Sie können Finanzberichte über die Druckdienste Ihres Geräts ausdrucken. [!INCLUDE[prod_short](includes/prod_short.md)] bietet außerdem Möglichkeiten, um Berichte als Excel-Arbeitsmappen, Word-Dokumente, PDF- und XML-Dateien zu speichern.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Auf der Seite **Finanzberichte** wählen Sie den zu druckenden Bericht aus und wählen dann die Aktion **Drucken**.
1. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Wählen Sie im Feld **Drucker** das Gerät, an das der Bericht gesendet wird.
    1. Die Option **(Vom Browser verwaltet)** zeigt an, dass es keinen bestimmten Drucker für den Bericht gibt. In diesem Fall handhabt der Browser den Ausdruck und zeigt die Standarddruckschritte an, in denen Sie einen lokalen Drucker auswählen können, der mit Ihrem Gerät verbunden ist. **(Vom Browser gehandhabt)** ist in der mobilen [!INCLUDE[prod_short](includes/prod_short.md)] App oder der App für Teams nicht verfügbar.
1. Wählen Sie die Aktion **Drucken** aus.

### Planen Sie einen Finanzbericht oder speichern Sie ihn als PDF-, Word- oder Excel-Dokument

Sie können einen Finanzbericht in Dateiformaten wie PDF, XML, Word oder Excel speichern. [!INCLUDE[prod_short](includes/prod_short.md)] kann auch wiederkehrende Finanzberichte generieren.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 4 öffnet](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie auf der Seite **Finanzberichte** die Aktion **Drucken**.
1. Legen Sie den Bericht entsprechend fest und wählen Sie dann die Aktion **Senden an**.
1. Wählen Sie das Dateiformat oder die Aktion **Zeitplan** und wählen Sie **OK**.
1. Um einen geplanten oder wiederkehrenden Finanzbericht zu erstellen, füllen Sie die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Für wiederkehrende Finanzberichte legen Sie in den Feldern **Frühestes Startdatum/Uhrzeit** und **Ablaufdatum/Uhrzeit** das erste bzw. letzte Datum für die Erstellung des Finanzberichts fest. Legen Sie außerdem fest, an welchen Tagen der Bericht erstellt werden soll, indem Sie das Feld **Nächstes Ausführungsdatum Formel** entsprechend dem im Abschnitt [Verwendung von Datumsformeln](ui-enter-date-ranges.md#use-date-formulas) erläuterten Format festlegen.


## Bewährte Methoden für die Arbeit mit Finanzberichtsdefinitionen

Für die Finanzberichtsdefinitionen gibt es keine Versionsverwaltung. Wenn Sie eine Berichtsdefinition ändern, wird die alte Version ersetzt, wenn Ihre Änderung in der Datenbank gespeichert wird. Die folgende Liste enthält einige bewährte Vorgehensweisen für die Arbeit mit Finanzberichtsdefinitionen:

- Wenn Sie Berichtsdefinitionen hinzufügen, wählen Sie einen guten Code und geben Sie im Beschreibungsfeld einen aussagekräftigen Text ein, solange Sie noch wissen, wofür Sie den Bericht verwenden. Diese Informationen helfen Ihren Mitarbeitenden (und Ihnen selbst in der Zukunft) bei der Arbeit mit dem Bericht und falls notwendig beim Ändern der Berichtsdefinition.
- Bevor Sie eine Berichtsdefinition ändern, sollten Sie eine Sicherungskopie davon erstellen, für den Fall, dass die Änderung nicht wie erwartet funktioniert. Sie können die Definition entweder einfach kopieren (geben Sie ihr einen guten Namen) oder exportieren. Mehr erfahren Sie unter [Finanzberichtsdefinitionen importieren oder exportieren](#import-or-export-financial-report-definitions).
- Wenn Sie eine neue Kopie einer Definition benötigen, die [!INCLUDE[prod_short](includes/prod_short.md)] bereitstellt, erhalten Sie diese ganz einfach, indem Sie ein neues Unternehmen erstellen, das nur die Einrichtungsdaten enthält. Exportieren Sie dann die Definition und importieren Sie sie in das Unternehmen, wo die Definition aktualisiert werden muss.

## Finanzberichtsdefinitionen importieren oder exportieren

Sie können Finanzberichtsdefinitionen als RapidStart-Konfigurationspakete importieren und exportieren. Konfigurationspakete sind beispielsweise hilfreich, um Informationen für andere Unternehmen freizugeben. Das Paket wird in einer .rapidstart-Datei erstellt, die den Inhalt komprimiert.

> [!NOTE]
> Wenn Sie Finanzberichtsdefinitionen importieren, werden bestehende Datensätze mit dem gleichen Namen wie die zu importierenden durch die neuen Definitionen ersetzt. Das Konfigurationspaket für eine Berichtsdefinition überschreibt keine vorhandenen Zeilen- oder Spaltendefinitionen, die in der Berichtsdefinition verwendet werden.

Um Finanzberichtsdefinitionen zu importieren oder zu exportieren, gehen Sie wie folgt vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 4.](media/ui-search/search_small.png "Was möchten Sie tun?") aus, geben Sie **Finanzberichte** ein und wählen Sie dann den entsprechenden Link.
1. Wählen Sie den Finanzbericht und wählen Sie dann die Aktion **Finanzbericht importieren** oder **Finanzbericht exportieren**, je nachdem, was Sie tun möchten.

Weitere Informationen zum Importieren und Exportieren von Zeilen- oder Spaltendefinitionen in Finanzberichten finden Sie in den folgenden Artikeln: 

- [Finanzberichtszeilendefinitionen importieren oder exportieren](bi-row-definitions.md#import-or-export-financial-reporting-row-definitions) oder
- [Finanzberichtsspaltendefinitionen importieren oder exportieren](bi-column-definitions.md#import-or-export-financial-report-column-definitions)

## Siehe auch

[Zeilendefinitionen in Finanzberichten](bi-row-definitions.md)  
[Spaltendefinitionen in Finanzberichten](bi-column-definitions.md)  
[Berichte ausführen und drucken](ui-work-report.md)  
[Financial Business Intelligence](bi.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Das Hauptbuch und der Kontenplan](finance-general-ledger.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
