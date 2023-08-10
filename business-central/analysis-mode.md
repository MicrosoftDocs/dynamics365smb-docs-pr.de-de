---
title: Analysieren Sie Daten auf Listenseiten im Datenanalysemodus
description: 'Erfahren Sie, wie Sie den Datenanalysemodus in Business Central verwenden, um Daten zu analysieren.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/30/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-data-using-data-analysis-mode"></a>Analysieren Sie Daten auf Listenseiten im Datenanalysemodus

In diesem Artikel erfahren Sie, wie Sie Daten von Listenseiten mit dem *Datenanalysemodus* analysieren. Der Datenanalysemodus ermöglicht es Ihnen, Daten direkt von der Seite aus zu analysieren, ohne einen Bericht ausführen oder zu einer anderen Anwendung wie Excel wechseln zu müssen. Es bietet eine interaktive und vielseitige Möglichkeit, Daten zu berechnen, zusammenzufassen und zu untersuchen. Anstatt Berichte mit unterschiedlichen Optionen und Filtern auszuführen, können Sie mehrere Registerkarten hinzufügen, die unterschiedliche Aufgaben oder Ansichten der Daten darstellen. Beispiele könnten „Meine Kunden“, „Artikel verfolgen“, „Kürzlich hinzugefügte Lieferanten“, „Verkaufsstatistiken“ oder jede andere Ansicht sein, die Sie sich vorstellen können.

> [!TIP]
> Eine gute Sache am Datenanalysemodus ist, dass er keine der zugrunde liegenden Daten der Listenseite oder das Layout der Seite ändert, wenn er sich nicht im Datenanalysemodus befindet. Der beste Weg, um zu erfahren, was Sie im Datenanalysemodus tun können, ist, Dinge auszuprobieren.

## <a name="prerequisite"></a>Voraussetzung

Der Datenanalysemodus befindet sich derzeit in der Vorschauphase, was bedeutet, dass ein Administrator ihn aktivieren muss, bevor Sie ihn verwenden können. Wenn Sie Administrator sind und den Datenanalysemodus aktivieren möchten, gehen Sie zur Seite **Funktionsverwaltung** und aktivieren Sie **Funktionsaktualisierung: Analysemodus, analysieren Sie schnell Daten direkt in Business Central**. Weitere Informationen zum Ein- und Ausschalten von Funktionen finden Sie unter[Funktionsverwaltung](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="get-started"></a>Erste Schritte

1. Öffnen Sie die Listenseite.

   Um beispielsweise mit **Kundenbucheinträgen** zu arbeiten, wählen Sie die ![Lupe aus, die die Tell Me-Funktion öffnet.](media/ui-search/search_small.png) Symbol (<kbd>Alt</kbd>+<kbd>Q</kbd>) geben Sie *Hauptbuchhaltungsposten* ein und wählen Sie dann den zugehörigen Link aus.  
2. Aktivieren Sie in der Aktionsleiste oben auf der Seite den Umschalter **Analysieren**.

    Der Datenanalysemodus öffnet die Daten in einer Erfahrung, die für die Datenanalyse optimiert ist.  Im Datenanalysemodus wird die normale Aktionsleiste durch eine spezielle Datenanalysemodusleiste ersetzt. Die folgende Abbildung veranschaulicht die verschiedenen Bereiche einer Seite im Datenanalysemodus.

   [![Zeigt eine Übersicht einer Seite zum Datenanalysemodus](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Jeder Bereich wird in den folgenden Abschnitten erläutert.

3. Verwenden Sie die verschiedenen Bereiche, um Daten zu manipulieren, zusammenzufassen und zu analysieren. Details finden Sie in den folgenden Abschnitten.

4. Wenn Sie den Analysemodus verlassen möchten, schalten Sie den Umschalter **Analysieren** aus.

   Die hinzugefügten Analyseregisterkarten bleiben erhalten, bis Sie sie löschen. Wenn Sie also wieder in den Datenanalysemodus zurückkehren, sehen Sie sie genau so, wie Sie sie verlassen haben.

> [!NOTE]
> Die im Analysemodus angezeigten Daten werden durch die auf der Listenseite eingestellten Filter oder Ansichten gesteuert. Auf diese Weise können Sie Daten vor dem Aufrufen des Analysemodus vorfiltern.

## <a name="work-with-data-analysis-mode"></a>Arbeiten Sie mit dem Datenanalysemodus

Im Datenanalysemodus ist die Seite in zwei Bereiche unterteilt:

- Der Hauptbereich, bestehend aus dem Datenbereich (1), der Übersichtsleiste (2) und der Registerkartenleiste (5)
- Der Datenbearbeitungsbereich, der aus zwei Bereichen besteht: Spalten (3) und Analysefilter (4).

### <a name="data-area-1"></a>Datenbereich (1)

Im Datenbereich werden die Zeilen und Spalten der Listenseite angezeigt und die Daten zusammengefasst. Der Datenbereich bietet eine vielseitige Möglichkeit, das Layout der Spalten zu steuern und eine schnelle Möglichkeit, eine Zusammenfassung der Daten zu erhalten. Bei Spalten, die numerische Werte enthalten, wird die Summe aller Werte in der Spalte in einer letzten Zeile angezeigt, es sei denn, Sie haben Zeilengruppen definiert. In diesem Fall erscheinen die Summen als Zwischensumme für die Gruppen.  

![Zeigt eine Übersicht eines Datenbereichs auf einer Seite im Datenanalysemodus an](media/analysis-mode-data-area.png)

- Um eine Spalte zu verschieben, wählen Sie sie aus und ziehen Sie sie an die Stelle, an der sie in Ihrer Analyse am sinnvollsten ist.
- Klicken Sie mit der rechten Maustaste auf die Spalte oder bewegen Sie den Mauszeiger darüber und wählen Sie das Menüsymbol aus ![Zeigt das Symbol in einer Spalte im Datenanalysemodus an, das ein Menü mit Aktionen öffnet](media/analysis-mode-column-menu-icon.png) um auf mehrere Aktionen zuzugreifen, die Sie für Spalten ausführen können. Beispiel:

  - Um eine Spalte links oder rechts vom Datenbereich anzuheften, damit sie beim Scrollen nicht vom Bildschirm verschwindet, wählen Sie ![Zeigt das Symbol in einer Spalte im Datenanalysemodus an, das ein Menü mit Aktionen im Spaltenteil ](media/analysis-mode-column-menu-icon.png) > **Spalte anheften** > **Link anheften** öffnet.
  - Definieren Sie Datenfilter direkt in der Spaltendefinition, anstatt zum Bereich **Analysefilter** zu gehen. Sie können immer noch Details zu verwandten Daten und für jede Zeile einsehen und die Karte öffnen, um mehr über eine bestimmte Entität zu erfahren.
- Verwenden Sie den Datenbereich, um mit den Daten zu interagieren. Für Spalten, die numerische, summierbare Werte enthalten, können Sie deskriptive Statistiken zu einer Gruppe von Feldern erhalten, indem Sie sie markieren. Die Statistiken erscheinen in der Statusleiste (2) unten auf der Seite.
- Exportieren Sie Daten im Excel- oder CSV-Format. Klicken Sie einfach mit der rechten Maustaste auf den Datenbereich oder eine Auswahl von Zellen, um sie zu exportieren.

### <a name="summary-bar-2"></a>Zusammenfassungsleiste (2)

Die Zusammenfassungsleiste befindet sich unten auf der Seite und zeigt Statistiken zu den Daten in der Liste an. Wenn Sie mit Spalten interagieren, deren Werte summiert werden können, z. B. mehrere Zeilen in einer Spalte auswählen, die Beträge anzeigt, werden die Daten aktualisiert.

![Zeigt eine Übersicht einer Zusammefassungsleiste im Datenanalysemodus an](media/analysis-mode-totals-row.png)

Die folgende Tabelle beschreibt die verschiedenen Zahlen, die im Summenbereich angezeigt werden:

|Anzahl|Beschreibung|
|-|-|
|Zeilen|Die Anzahl der ausgewählten Zeilen als Teil der Gesamtzahl der verfügbaren Zeilen. |
|Zeilen gesamt|Die Anzahl der Zeilen in der ungefilterten Liste.|
|Gefiltert|Die Anzahl der Zeilen, die als Ergebnis der auf die Liste angewendeten Filter angezeigt werden.|
|Durchschnitt|Der Durchschnittswert in allen ausgewählten summierbaren Feldern.|
|Anzahl|Die Anzahl der ausgewählten Zeilen.|
|Min.|Der minimale Wert in allen ausgewählten summierbaren Feldern.|
|Max.|Der maximale Wert in allen ausgewählten summierbaren Feldern.|
|Summe|Die Gesamtsumme aller Werte in den ausgewählten summierbaren Feldern.|

### <a name="columns-3"></a>Spalten (3)

Die **Spalten** sind einen von zwei Bereichen, die zusammenarbeiten, um Ihre Analyse zu definieren. Der andere Bereich ist der **Analysefilter**. Der **Spalten**-Bereich wird verwendet, um die Daten zusammenzufassen. Verwenden Sie den Bereich **Spalten**, um festzulegen, welche Spalten in die Analyse einbezogen werden sollen.

![Zeigt eine Übersicht des Spaltenbereichs im Datenanalysemodus an](media/analysis-mode-columns-2.png)

|Bereiche|Beschreibung|
|-|-|
|Suchen/aktivieren oder deaktivieren Sie alle Kästchen|Suche nach Spalten. Aktivieren Sie das Kontrollkästchen, um alle Spalten auszuwählen/abzuwählen.|
|Kontrollkästchen|Dieser Bereich enthält ein Kontrollkästchen für jedes Feld in der Quelltabelle der Liste. Verwenden Sie diesen Bereich, um zu ändern, welche Spalten in der Liste angezeigt werden. Aktivieren Sie ein Kontrollkästchen, um die Spalte für das Feld auf der Seite anzuzeigen; Deaktivieren Sie das Kontrollkästchen, um die Spalte auszublenden. |
|Zeilengruppen|Verwenden Sie diesen Bereich, um Daten nach einem oder mehreren Feldern zu gruppieren und zu summieren. Sie können nur nicht numerische Felder wie Text-, Datums- und Zeitfelder einschließen. Zeilengruppen werden häufig im Pivot-Modus verwendet.|
|Werte|Verwenden Sie diesen Bereich, um Felder anzugeben, für die Sie eine Gesamtsumme wünschen. Sie können nur Felder einschließen, die Zahlen enthalten, die addiert werden können; wie beispielsweise keine Text-, Datums- oder Zeitfelder.|

Um ein Feld von einem Bereich in einen anderen zu verschieben, wählen Sie das Greifsymbol ![Zeigt eine Übersicht einer Seite zum Datenanalysemodus](media/column-grab-icon.png) neben der Spalte in der obigen Liste an; ziehen Sie sie in den Zielbereich. Sie werden daran gehindert, ein Feld in einen Bereich zu verschieben, in dem es nicht erlaubt ist.

### <a name="analysis-filters-4"></a>Analysefilter (4)

Im Bereich **Analysefilter** können Sie weitere Datenfilter für Spalten festlegen, um die Einträge in der Liste einzuschränken. Legen Sie Filter für Spalten fest, um die Einträge in der Liste und die nachfolgenden Summen basierend auf einem von Ihnen definierten Kriterium auf nur die Einträge zu beschränken, an denen Sie interessiert sind. Angenommen, Sie sind nur an Daten für einen bestimmten Kunden oder Verkaufsaufträge interessiert, die einen bestimmten Betrag überschreiten. Um einen Filter festzulegen, wählen Sie die Spalte aus und wählen Sie die Vergleichsoperation aus der Liste aus (z. B. **Gleich** oder **Beginnt mit**), geben Sie dann den Wert ein.

![Zeigt eine Übersicht des Filterbereichs im Datenanalysemodus an](media/analysis-mode-filters.png)

> [!NOTE]
> Die zusätzlichen Filter gelten nur für die aktuelle Analyse-Registerkarte. Auf diese Weise können Sie genau die zusätzlichen Datenfilter definieren, die für eine bestimmte Analyse benötigt werden.

### <a name="tabs-5"></a>Registerkarten (5)

Im Registerkartenbereich oben können Sie verschiedene Konfigurationen (Spalten und Analysefilter) auf separaten Registerkarten erstellen, wobei Sie Daten auf den Registerkarten unabhängig voneinander bearbeiten können. Es gibt immer mindestens eine Registerkarte, die standardmäßig **Analyse 1** heißt. Das Hinzufügen weiterer Registerkarten ist vorteilhaft, um häufig verwendete Analysekonfigurationen für einen Datensatz zu speichern. Sie haben beispielsweise Registerkarten zum Analysieren von Daten im Pivot-Modus und andere Registerkarten, die nach einer Teilmenge von Zeilen filtern. Einige Registerkarten zeigen möglicherweise eine detaillierte Ansicht mit vielen Spalten an, und andere zeigen nur einige Schlüsselspalten an.

Hier sind einige Hinweise zum Arbeiten mit mehreren Analyseregisterkarten:

- Um eine neue Registerkarte hinzuzufügen, wählen Sie das große **+** Zeichen neben der letzten Analyseregisterkarte aus.
- Wählen Sie auf einer Registerkarte den Abwärtspfeil aus, um auf eine Liste mit Aktionen zuzugreifen, die Sie auf einer Registerkarte ausführen können, z. B. umbenennen, duplizieren, löschen und verschieben.

   - **Löschen** löscht die aktuell geöffnete Registerkarte. **Alle löschen** löscht alle Registerkarten, die Sie hinzugefügt haben, mit Ausnahme der Standardregisterkarte **Analyse 1**.
- Sie können die **Analyse 1** nicht vollständig entfernen, aber Sie können sie umbenennen, indem Sie die Aktion **Umbenennen** und löschen verwenden und die Änderungen, die Sie vorgenommen haben mithilfe von **Löschen** oder **Alle löschen** löschen.  

- Die hinzugefügten und konfigurierten Analyseregisterkarten bleiben erhalten, bis Sie sie löschen. Wenn Sie also wieder in den Datenanalysemodus zurückkehren, sehen Sie sie genau so, wie Sie sie verlassen haben.

   > [!TIP]
   > Die von Ihnen eingerichteten Registerkarten sind nur für Sie sichtbar. Andere Benutzer sehen nur die Registerkarten, die sie eingerichtet haben.
- Sie können Analyseregisterkarten kopieren. Das Kopieren kann nützlich sein, wenn Sie mit dem Ändern einer Registerkarte experimentieren möchten, ohne das Original zu ändern, oder wenn Sie verschiedene Variationen derselben Analyse erstellen möchten.

## <a name="pivot-mode"></a>Pivot-Modus

Sie können den Pivot-Modus verwenden, um große Mengen numerischer Daten zu analysieren und Daten nach Kategorien und Unterkategorien zu subsummieren. Der Pivot-Modus ist wie [Pivot-Tabellen in Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Um den Pivot-Modus ein- und auszuschalten, verschieben Sie den **Pivot-Modus** im Bereich **Spalten** (3). Wenn Sie den Pivot-Modus aktivieren, wird der Bereich **Spaltenbeschriftungen** im Bereich angezeigt. Verwenden Sie den Bereich **Spaltenbeschriftungen**, um Gesamtsummen für Zeilen in Kategorien zu gruppieren. Felder, die Sie dem Bereich **Spaltenbeschriftungen** hinzufügen, werden als Spalten im Datenbereich (1) angezeigt.

Der Aufbau der Datenanalyse im Pivot-Modus umfasst das Verschieben von Feldern in die drei Bereiche: **Zeilengruppen**, **Spaltenbeschriftungen**, und **Werte**. Die folgende Abbildung zeigt, wo die Felder dem Datenbereich (1) zugeordnet sind, wobei `sum` die berechneten Daten und optional **Werte** sind.

<table>
<tr><th></th><th>Spaltenbeschriftung</th><th></th><th>Spaltenbeschriftung</th><th></th></tr>
<tr><th>Zeilengruppe</th><th>Wert</th><th>Wert</th><th>Wert</th><th>Wert</th></tr>
<tr><td>Zeile</td><td>Summe</td><td>Summe</td><td>Summe</td><td>Summe</td></tr>
<tr><td>Zeile</td><td>Summe</td><td>Summe</td><td>Summe</td><td>Summe</td></tr>
<tr><td>Zeile</td><td>Summe</td><td>Summe</td><td>Summe</td><td>Summe</td></tr>
<tr><td>Zeile</td><td>Summe</td><td>Summe</td><td>Summe</td><td>Summe</td></tr>
</table>

> [!TIP]
> Spalten mit nur wenigen möglichen Werten sind die besten Kandidaten für die Verwendung in Spalte **Werte**.

## <a name="limitations"></a>Einschränkungen

Die Analyseansicht hat derzeit ein Limit von 100.000 Zeilen. Wenn Sie diese Grenze überschreiten, erhalten Sie eine entsprechende Nachricht. Um diese Einschränkung zu umgehen, setzen Sie die Filter auf der Seite, bevor Sie in den Datenanalysemodus wechseln, sofern dies möglich ist.  Vielleicht möchten Sie eine bestimmte Kundengruppe analysieren oder nur Daten aus dem laufenden Jahr. Sie können auch eine vordefinierte Ansicht auswählen, wenn diese für Ihre Analyse geeignet ist.

## <a name="see-also"></a>Siehe auch

[Ad-hoc-Datenanalyse](reports-adhoc-analysis.md)  
[Anzeigen und Bearbeiten in Excel](across-work-with-excel.md)  
