---
title: Änderungen protokollieren
description: 'Sie können ein Benutzerprotokoll aktivieren, sodass Sie Aufzeichnungen über sämtliche Änderungen haben, die an den Daten in verfolgten Tabellen vorgenommen werden. Sie können Aktivitäten auch mit bestimmten Arten von Aktivitätsprotokollen verfolgen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="auditing-changes"></a>Änderungen protokollieren

Eine häufige Herausforderung in vielen Anwendungen zur Unternehmensverwaltung ist die Vermeidung unerwünschter Datenänderungen. Es könnte alles sein – von einer falschen Debitorentelefonnummer bis hin zu einer falschen Buchung in der Finanzbuchhaltung. In diesem Artikel werden die Funktionen beschrieben, mit denen Sie herausfinden können, was geändert wurde, wer es geändert hat und wann die Änderung vorgenommen wurde.

## <a name="about-the-change-log"></a>Informationen zum Änderungsprotokoll

Die Änderungsprotokollfunktion ermöglicht die Verfolgung aller direkten Änderungen, die von einem Benutzer an den Daten in der Datenbank vorgenommen werden. Sie geben jede Tabelle und jedes Feld an, die das System protokollieren soll, und aktivieren dann das Änderungsprotokoll. Das Änderungsprotokoll basiert auf Änderungen, die an den Daten in den von Ihnen verfolgten Tabellen vorgenommen werden. Auf der Seite **Änderungsprotokollposten** werden Posten chronologisch aufgeführt und alle Änderungen angezeigt, die an den Werten in den Feldern der von Ihnen angegebenen Tabellen vorgenommen wurden.

Das Nachverfolgen von Änderungen kann sich auf die Leistung auswirken, was Sie Zeit kosten kann. Möglicherweise steigt auch die Datenbankgröße, was Sie Geld kosten kann. Um diese Kosten zu reduzieren, sollten Sie Folgendes beachten:

- Gehen Sie bei der Auswahl der Tabellen und Arbeitsgänge vorsichtig vor.
- Fügen Sie keine Posten und gebuchten Belege hinzu. Priorisieren Sie stattdessen Systemfelder wie „Erstellt von“ und „Erstellungsdatum“.
- Verwenden Sie nicht den Nachverfolgungstyp **Alle Felder**. Wählen Sie stattdessen **Einige Felder** und verfolgen Sie nur die wichtigsten Felder.

> [!NOTE]
> Das Änderungsprotokoll verfolgt keine Änderungen für Felder, welche die `autoIncrement property` verwenden. Ein Beispiel für ein Feld, das die Eigenschaft verwendet, ist das Feld „Ganzzahl“ in den Tabellen „Fehlermeldungen“ und „MwSt.-Berichtszeile“.

Das Änderungsprotokoll wird auch aus Performance-Gründen während des Upgrades von [!INCLUDE [prod_short](includes/prod_short.md)] auf die nächste Version deaktiviert. Die Abschaltung der Protokollierung beschleunigt nicht nur den Upgrade-Prozess, sondern trägt auch dazu bei, Datenmüll im Änderungsprotokoll zu verringern. Sobald das Upgrade abgeschlossen ist, beginnt das Protokoll wieder mit der Verfolgung von Änderungen.

> [!Important]
> Änderungen werden in **Änderungsprotokollposten** erst angezeigt, nachdem die Sitzung des Benutzers neu gestartet wurde, was folgendermaßen geschieht:
>
> - Die Sitzung war abgelaufen und wurde aktualisiert.
> - Der Benutzer hat ein anderes Unternehmen oder Rollencenter ausgewählt.
> - Der Benutzer hat sich abgemeldet und erneut angemeldet.

## <a name="setting-up-the-change-log"></a>Einrichten des Änderungsprotokolls

Sie können das Änderungsprotokoll auf der Seite **Änderungsprotokoll einrichten** aktivieren bzw. deaktivieren. Wenn Sie dies tun, wird die Aktivität protokolliert, sodass Sie immer sehen können, wer die Änderung vorgenommen hat.

Wenn Sie auf der Seite **Einrichtung des Änderungsprotokolls** die Aktion **Tabellen** wählen, können Sie angeben, für welche Tabellen Sie Änderungen verfolgen wollen und welche Änderungen verfolgt werden sollen. Mit [!INCLUDE[prod_short](includes/prod_short.md)] werden auch mehrere Systemtabellen verfolgt.

> [!NOTE]
> Sie können bestimmte Felder auf Änderungen überwachen, z. B. Felder, die sensible Daten enthalten, indem Sie die Feldüberwachung einrichten. Wenn Sie dies tun, ist die Tabelle, die das Feld enthält, zur Vermeidung von Redundanz nicht für die Einrichtung des Änderungsprotokolls verfügbar. Weitere Informationen finden Sie unter [Sensible Felder überwachen](across-log-changes.md#monitor-sensitive-fields).

Wenn Sie das Änderungsprotokoll einrichten und aktivieren und jemand Daten verändert, protokolliert die Anwendung die Änderung in einem **Änderungsprotokollposten**. Wenn Sie Einträge löschen möchten, richten Sie eine Aufbewahrungsrichtlinie ein, in der Sie Filter basierend auf Datum und Uhrzeit festlegen können. Weitere Informationen zu Aufbewahrungsrichtlinien finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).  

## <a name="analyze-data-in-the-change-log"></a>Daten im Änderungsprotokoll analysieren

Mit dem Feature **Datenanalyse** können Sie Daten im Änderungsprotokoll von der Seite [Änderungsprotokollposten](https://businesscentral.dynamics.com/?page=595) aus analysieren. Sie müssen keinen Bericht ausführen und keine andere Anwendung wie beispielsweise Excel öffnen. Das Feature bietet eine interaktive und vielseitige Möglichkeit, Daten zu berechnen, zusammenzufassen und zu untersuchen. Anstatt Berichte mit Optionen und Filtern auszuführen, können Sie mehrere Registerkarten hinzufügen, die unterschiedliche Aufgaben oder Ansichten der Daten darstellen. Einige Beispiele sind „Wer hat wann welche Daten geändert?“ oder „Datenänderungen nach Tabelle/Feld“ oder jede andere Ansicht, die Sie sich vorstellen können. Weitere Informationen zur Verwendung des Features **Datenanalyse** finden Sie unter [Listen- und Abfragedaten mit dem Analysemodus analysieren](analysis-mode.md).

### <a name="change-log-ad-hoc-analysis-scenarios"></a>Ad-hoc-Analyseszenarien für das Änderungsprotokoll

Die folgenden Abschnitte enthalten Beispiele für Szenarios, in denen Ihnen die Analyse des Änderungsprotokolls dabei helfen kann, wichtige Änderungen zu überwachen und zu überprüfen.

| Region | An... | Öffnen Sie diese Seite im Analysemodus | Diese Felder verwenden |
| ---- | ----- | ------------------------------- |------------------- |
| [Wer hat wann welche Daten geändert?](#example-who-changed-what-data-and-when) | Sehen Sie sich an, wer welche Daten geändert hat. | [Änderungsprotokolleinträge](https://businesscentral.dynamics.com/?page=595) | **Benutzer-ID**, **Datum und Uhrzeit**, **Tabellenbeschriftung**, **Feldbeschriftung**, **Primärschlüsselwert 2**, **Primärschlüsselwert 3**, **Änderungsart**, **Alter Wert** und **Neuer Wert**. |
| [Datenänderungen nach Tabelle/Feld](#example-data-changes-by-tablefield) | Sehen Sie sich Datenänderungen nach Tabelle/Feld und wer die Änderung vorgenommen hat an. | [Änderungsprotokolleinträge](https://businesscentral.dynamics.com/?page=595) | **Tabellenbeschriftung**, **Feldbeschriftung**, **Benutzer-ID**, **Datum und Uhrzeit**, **Primärschlüsselwert 2**, **Primärschlüsselwert 3**, **Änderungsart**, **Alter Wert** und **Neuer Wert**. |

### <a name="example-who-changed-what-data-and-when"></a>Beispiel: Wer hat wann welche Daten geändert?

Um zu analysieren, wer wann welche Daten geändert hat, gehen Sie folgendermaßen vor:

1. Öffnen Sie die Liste [Änderungsprotokollposten](https://businesscentral.dynamics.com/?page=595) und wählen Sie das Symbol :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben"::: aus, um den Analysemodus zu aktivieren.
1. Entfernen Sie auf dem Menü **Spalten** alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** auf der rechten Seite aus).
1. Ziehen Sie das Feld **Benutzer-ID** (wer hat es getan) in den Bereich **Zeilengruppen** .
1. Wählen Sie jetzt die folgenden Felder aus:
   - Um anzuzeigen, wann es passiert ist, wählen Sie **Datum und Uhrzeit**.
   - Um die Tabelle anzuzeigen, in der es passiert ist, wählen Sie **Tabellenbeschriftung**. 
   - Um anzuzeigen, um welches Feld es geht, wählen Sie **Feldbeschriftung**.
   - Um den Feldcode anzuzeigen, wählen Sie **Primärschlüsselwert 2**. 
   - Um den Unternehmensnamen anzuzeigen, wählen Sie **Primärschlüsselwert 3**.
   - Um anzuzeigen, ob es sich bei der Änderung um eine Einfüge-, Aktualisierungs- oder Löschaktion handelt, wählen Sie **Änderungsart**.
   - Um die Änderung anzuzeigen, wählen Sie **Alter Wert** und **Neuer Wert**.
1. Benennen Sie Ihre Analyseregisterkarte in **Wer hat wann welche Daten geändert?** oder in etwas anderes um, das diese Analyse beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source=" media/data-analysis-change-log-entries-Who-changed-What-data-When.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Änderungsprotokollposten“ (Wer hat wann welche Daten geändert?)." lightbox="media/data-analysis-change-log-entries-Who-changed-What-data-When.png":::

### <a name="example-data-changes-by-tablefield"></a>Beispiel: Datenänderungen nach Tabelle/Feld

Um Datenänderungen nach Tabelle/Feld zu analysieren, gehen Sie wie folgt vor:

1. Öffnen Sie die Liste [Änderungsprotokollposten](https://businesscentral.dynamics.com/?page=595) und wählen Sie das Symbol :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus eingeben"::: aus, um den Analysemodus zu aktivieren.
1. Entfernen Sie auf dem Menü **Spalten** alle Spalten (wählen Sie das Kästchen neben dem Feld **Suchen** auf der rechten Seite aus).
1. Ziehen Sie die Felder **Tabellenbeschriftung** (in welcher Tabelle) und **Feldbeschriftung** (in welchem Feld) in den Bereich **Zeilengruppen**.
1. Wählen Sie jetzt die folgenden Felder aus:
   - Um anzuzeigen, wann es passiert ist, wählen Sie **Datum und Uhrzeit**
   - Um anzuzeigen, wer die Änderung vorgenommen hat, wählen Sie **Benutzer-ID**.
   - Um den Code für das Feld anzuzeigen, wählen Sie **Primärschlüsselwert 2**.
   - Um den Unternehmensnamen anzuzeigen, wählen Sie **Primärschlüsselwert 3** (normalerweise der Unternehmensname). 
   - Um anzuzeigen, ob es sich bei der Änderung um eine Einfüge-, Aktualisierungs- oder Löschaktion handelt, wählen Sie **Änderungsart**.
   - Um die Änderung anzuzeigen, wählen Sie **Alter Wert** und **Neuer Wert**.
1. Benennen Sie Ihre Analyseregisterkarte in **Datenänderungen in Tabelle + Feld** oder in etwas anderes um, das diese Analyse beschreibt.

Das folgende Bild zeigt das Ergebnis dieser Schritte.

:::image type="content" source=" media/data-analysis-change-log-entries-data-changes-by-table-field.png" alt-text="Beispiel für die Durchführung einer Datenanalyse auf der Seite „Änderungsprotokollposten“ (Datenänderungen nach Tabelle/Feld)." lightbox="media/data-analysis-change-log-entries-data-changes-by-table-field.png":::

## <a name="about-activity-logs"></a>Informationen zu Aktivitätsprotokollen

Von einigen Seiten in [!INCLUDE [prod_short](includes/prod_short.md)] können Sie ein Aktivitätsprotokoll anzeigen, in dem der Status und alle Fehler von Dateien angezeigt werden, aus denen Sie exportieren oder in die Sie importieren [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="work-with-activity-logs"></a>Mit Aktivitätsprotokollen arbeiten

Die Informationen werden auf der Seite **Aktivitätsprotokoll** angezeigt, entsprechend dem Kontext, aus dem Sie sie geöffnet haben. Sie können die Seite beispielsweise über die Seiten **Belegaustauschdienst – Einrichtung**, **Eingehender Beleg**, **Gebuchte Verkaufsrechnung** und **Geb. Verkaufsgutschrift** öffnen. Sie können die Liste der Protokolleinträge leeren oder die Liste der Einträge löschen, die älter als sieben Tage sind.  

## <a name="monitor-sensitive-fields"></a>Sensible Felder überwachen

Der Schutz sensibler Daten ist für die meisten Unternehmen ein zentrales Anliegen. Um eine Sicherheitsebene hinzuzufügen, können Sie wichtige Felder überwachen und eine E-Mail erhalten, wenn jemand einen Wert ändert. Sie können sich beispielsweise benachrichtigen lassen, wenn jemand die IBAN Ihres Unternehmens ändert.

> [!NOTE]
> Um den Versand von Benachrichtigungen per E-Mail zu ermöglichen, müssen Sie die E-Mail-Funktion in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

### <a name="set-up-field-monitoring"></a>Feldüberwachung einrichten

Sie können die Anleitung zum unterstützten Setup **Einrichtung der Überwachung von Feldänderungen** verwenden, um die Felder anzugeben, die Sie anhand von Filterkriterien überwachen möchten, z. B. die Klassifizierung der Datensensibilität für die Felder. Weitere Informationen finden Sie unter [Datensensitivität klassieren](admin-classifying-data-sensitivity.md). Mit dieser Anleitung können Sie auch die Person, die bei einer Änderung eine E-Mail-Benachrichtigung erhält, sowie das E-Mail-Konto angeben, das die Benachrichtigungs-E-Mail sendet. Geben Sie sowohl den zu benachrichtigenden Benutzer als auch das Konto an, von dem aus die Benachrichtigung gesendet werden soll. Wenn Sie die Anleitung abgeschlossen haben, können Sie die Einstellungen für die Feldüberwachung auf der Seite **Feldüberwachungseinrichtung** verwalten.

> [!NOTE]
> Wenn Sie das E-Mail-Konto angeben, von dem die Benachrichtigungen gesendet werden sollen, müssen Sie entweder die Kontotypen **Microsoft 365** oder **SMTP** hinzufügen. Benachrichtigungen sollten von einem Konto aus gesendet werden, das nicht mit einem tatsächlichen Benutzer verbunden ist. Daher können Sie nicht den Kontotyp **Aktueller Benutzer** wählen. Wenn Sie dies tun, werden keine Benachrichtigungen gesendet.

Im Laufe der Zeit nimmt die Liste der Einträge auf der Seite **Protokolleinträge für überwachte Felder** zu. Um die Anzahl der Einträge zu reduzieren, können Sie eine Aufbewahrungsrichtlinie erstellen, die Einträge nach einer bestimmten Zeitspanne löscht. Weitere Informationen finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).

Wenn Sie die Feldüberwachung einrichten oder etwas im Setup ändern, werden Einträge für Ihre Änderungen erstellt. Sie können festlegen, ob Einträge im Zusammenhang mit der Überwachungseinrichtung angezeigt werden sollen, indem Sie sie ein- oder ausblenden.

Sie können Einstellungen für die Feldüberwachung (z. B. ob eine E-Mail-Benachrichtigung gesendet oder nur die Änderung protokolliert wird) für jedes Feld auf der Seite **Arbeitsblatt „Überwachte Felder“** verwalten. Auf dieser Seite können Sie ebenfalls zu überwachende Felder hinzufügen oder entfernen.

> [!NOTE]
> Nachdem Sie ein oder mehrere Felder hinzugefügt und mit der Überwachung begonnen haben, müssen Sie sich bei [!INCLUDE[prod_short](includes/prod_short.md)] abmelden und erneut anmelden, damit Ihre Einstellungen übernommen werden.

### <a name="work-with-field-monitoring"></a>Mit der Feldüberwachung arbeiten

Einträge für alle geänderten Werte für überwachte Felder sind auf der Seite **Protokolleinträge für überwachte Felder** verfügbar. Die Einträge enthalten zum Beispiel die folgenden Informationen:

- Das Feld, in dem der Wert geändert wurde.
- Die ursprünglichen und neuen Werte.
- Wer die Änderung vorgenommen hat und wann er sie vorgenommen hat.

Um eine Änderung genauer zu untersuchen, wählen Sie einen Wert aus, um die Seite zu öffnen, auf der die Änderung vorgenommen wurde. Um eine Liste aller Einträge anzuzeigen, wählen Sie **Feldänderungseinträge** aus.

### <a name="view-field-monitoring-telemetry"></a>Feldüberwachungstelemetrie anzeigen

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, um eine Feldüberwachungsaktivität an eine Application Insights Ressource in Microsoft Azure zu senden. Anschließend erstellen Sie mit Azure Monitor Berichte und richten Warnungen für die erfassten Daten ein. Weitere Informationen finden Sie in den folgenden Artikeln in [!INCLUDE[prod_short](includes/prod_short.md)] Entwickler- und IT-Pro-Hilfe:

- [Überwachung und Analyse der Telemetrie – Aktivieren Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview?toc=/dynamics365/business-central/toc.json#enable)
- [Ananlysieren der Feldüberwachungstelemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)

## <a name="define-retention-policies"></a>Aufbewahrungsrichtlinien definieren

Sie können Aufbewahrungsrichtlinien erstellen, um nicht benötigte Daten in Protokollen nach einem von Ihnen angegebenen Zeitraum zu löschen. Beispielsweise kann die Anzahl der Einträge in einem Protokoll im Laufe der Zeit stark zunehmen. Durch das Bereinigen alter Einträge können Sie sich leichter auf neuere und wahrscheinlich relevantere Einträge konzentrieren. Weitere Informationen zu Aufbewahrungsrichtlinien finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).

## <a name="see-also"></a>Siehe auch

[Sensible Felder überwachen](across-log-changes.md#monitor-sensitive-fields)  
[Ananlysieren der Feldüberwachungstelemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)  
[Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md)  
[Grundlegende Einstellungen ändern](ui-change-basic-settings.md)  
[Sortieren, Suchen und Filtern](ui-enter-criteria-filters.md)  
[Suche nach Seiten und Informationen mit „Sie wünschen...“](ui-search.md)  
[Benutzenden und Gruppen Berechtigungen zuweisen](ui-define-granular-permissions.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
