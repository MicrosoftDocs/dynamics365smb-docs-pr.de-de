---
title: Änderungen protokollieren
description: 'Sie können ein Benutzerprotokoll aktivieren, sodass Sie Aufzeichnungen über sämtliche Änderungen haben, die an den Daten in verfolgten Tabellen vorgenommen werden. Sie können Aktivitäten auch mit bestimmten Arten von Aktivitätsprotokollen verfolgen.'
author: edupont04
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 03/24/2022
ms.author: edupont
---
# Protokollieren von Änderungen in Business Central

Eine häufige Herausforderung in vielen Anwendungen zur Unternehmensverwaltung ist die Vermeidung unerwünschter Datenänderungen. Es könnte alles sein – von einer falschen Debitorentelefonnummer bis hin zu einer falschen Buchung in der Finanzbuchhaltung. In diesem Thema werden die Funktionen beschrieben, mit denen Sie herausfinden können, was geändert wurde, wer es geändert hat und wann die Änderung vorgenommen wurde.

## Informationen zum Änderungsprotokoll

Die Änderungsprotokollfunktion ermöglicht die Verfolgung aller direkten Änderungen, die von einem Benutzer an den Daten in der Datenbank vorgenommen werden. Sie geben jede Tabelle und jedes Feld an, die das System protokollieren soll, und aktivieren dann das Änderungsprotokoll. Das Änderungsprotokoll basiert auf Änderungen, die an den Daten in den von Ihnen verfolgten Tabellen vorgenommen werden. Auf der Seite **Änderungsprotokollposten** werden Posten chronologisch aufgeführt und alle Änderungen angezeigt, die an den Werten in den Feldern der von Ihnen angegebenen Tabellen vorgenommen wurden. 

Das Nachverfolgen von Änderungen kann sich auf die Leistung auswirken, was Sie Zeit kosten kann. Möglicherweise wird auch die Datenbankgröße erhöht, was Sie Geld kosten kann. Um diese Kalkulationen zu reduzieren, sollten Sie Folgendes beachten:

- Gehen Sie bei der Auswahl der Tabellen und Arbeitsgänge vorsichtig vor.
- Fügen Sie keine Posten und gebuchten Dokumente hinzu. Priorisieren Sie stattdessen Systemfelder wie „Erstellt von“ und „Erstellungsdatum“.
- Verwenden Sie nicht den Tracking-Typ „Alle Felder“. Wählen Sie stattdessen „Einige Felder“ und verfolgen Sie nur die wichtigsten Felder.

Das Änderungsprotokoll wird auch aus Performance-Gründen während des Upgrades von [!INCLUDE [prod_short](includes/prod_short.md)] auf die nächste Version deaktiviert. Dies beschleunigt nicht nur den Upgrade-Prozess, sondern trägt auch dazu bei, Datenmüll im Zufallsprotokoll zu verringern. Sobald das Upgrade abgeschlossen ist, beginnt das Protokoll wieder mit der Verfolgung von Änderungen.

> [!Important]
> Änderungen werden in **Änderungsprotokollposten** erst angezeigt, nachdem die Sitzung des Benutzers neu gestartet wurde, was folgendermaßen geschieht:
>
> * Die Sitzung war abgelaufen und wurde aktualisiert.
> * Der Benutzer hat ein anderes Unternehmen oder Rollencenter ausgewählt.
> * Der Benutzer hat sich abgemeldet und erneut angemeldet.

### Mit dem Änderungsprotokoll arbeiten
Sie verwenden die Seite **Änderungsprotokoll einrichten** zum Aktivieren bzw. Deaktivieren des Änderungsprotokolls. Wenn Sie das Änderungsprotokoll aktivieren bzw. deaktivieren, wird diese Aktivität protokolliert, sodass Sie immer sehen, welcher Anwender die Protokollierung an- bzw. abgeschaltet hat.

Wenn Sie auf der Seite **Einrichtung des Änderungsprotokolls** die Aktion **Tabellen** wählen, können Sie angeben, für welche Tabellen Sie Änderungen verfolgen wollen und welche Änderungen verfolgt werden sollen. Mit [!INCLUDE[prod_short](includes/prod_short.md)] werden auch mehrere Systemtabellen verfolgt.

> [!NOTE]
> Sie können bestimmte Felder auf Änderungen überwachen, z. B. Felder, die sensible Daten enthalten, indem Sie die Feldüberwachung einrichten. Wenn Sie dies tun, ist die Tabelle, die das Feld enthält, zur Vermeidung von Redundanz nicht für die Einrichtung des Änderungsprotokolls verfügbar. Weitere Informationen finden Sie unter [Überwachen sensibler Felder](across-log-changes.md#monitoring-sensitive-fields).

Wenn Sie das Änderungsprotokoll eingerichtet und aktiviert haben und jemand Daten verändert hat, protokolliert die Anwendung die Änderung in einem **Änderungsprotokollposten**. Wenn Sie Posten löschen möchten, können Sie dies auf der Seite **Änderungsprotokollposten löschen** tun, an dem Sie Filter auf Basis Datum und Zeit festlegen können.  

## Informationen zu Aktivitätsprotokollen

Von einigen Seiten in [!INCLUDE [prod_short](includes/prod_short.md)] können Sie ein Aktivitätsprotokoll anzeigen, in dem der Status und alle Fehler von Dateien angezeigt werden, aus denen Sie exportieren oder in die Sie importieren [!INCLUDE [prod_short](includes/prod_short.md)].  

### Mit Aktivitätsprotokollen arbeiten
Die Informationen werden auf der Seite **Aktivitätsprotokoll** angezeigt, entsprechend dem Kontext, aus dem sie geöffnet wurden. Sie können die Seite beispielsweise über die Seiten **Belegaustauschdienst – Einrichtung**, **Eingehender Beleg**, **Gebuchte Verkaufsrechnung** und **Geb. Verkaufsgutschrift** öffnen. Sie können die Liste der Protokolleinträge leeren oder die Liste der Einträge löschen, die älter als sieben Tage sind.  

## Überwachen sensibler Felder

Der Schutz sensibler Daten ist für die meisten Unternehmen ein zentrales Anliegen. Um eine Sicherheitsebene hinzuzufügen, können Sie wichtige Felder überwachen und sich per E-Mail benachrichtigen lassen, wenn jemand einen Wert ändert. Sie können sich beispielsweise benachrichtigen lassen, wenn jemand die IBAN Ihres Unternehmens ändert.

> [!NOTE]
> Um den Versand von Benachrichtigungen per E-Mail zu ermöglichen, müssen Sie die E-Mail-Funktion in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

### Einrichten der Feldüberwachung

Sie können die Anleitung zum unterstützten Setup **Einrichtung der Überwachung von Feldänderungen** verwenden, um die Felder anzugeben, die Sie anhand von Filterkriterien überwachen möchten, z. B. die Klassifizierung der Datensensibilität für die Felder. Weitere Informationen finden Sie unter [Datensensitivität klassieren](admin-classifying-data-sensitivity.md). Mit dieser Anleitung können Sie auch die Person angeben, die bei einer Änderung eine E-Mail-Benachrichtigung erhalten soll, sowie das E-Mail-Konto, das die Benachrichtigungs-E-Mail sendet. Geben Sie sowohl den zu benachrichtigenden Benutzer als auch das Konto an, von dem aus die Benachrichtigung gesendet werden soll. Wenn Sie die Anleitung abgeschlossen haben, können Sie die Einstellungen für die Feldüberwachung auf der Seite **Feldüberwachungseinrichtung** verwalten. 

> [!NOTE]
> Wenn Sie das E-Mail-Konto angeben, von dem die Benachrichtigungen gesendet werden sollen, müssen Sie entweder die Kontotypen **Microsoft 365** oder **SMTP** hinzufügen. Benachrichtigungen sollten von einem Konto aus gesendet werden, das nicht mit einem tatsächlichen Benutzer verbunden ist. Daher können Sie nicht den Kontotyp **Aktueller Benutzer** wählen. Wenn Sie dies tun, werden keine Benachrichtigungen gesendet. 

Im Laufe der Zeit nimmt die Liste der Einträge auf der Seite **Protokolleinträge für überwachte Felder** zu. Um die Anzahl der Einträge zu reduzieren, können Sie eine Aufbewahrungsrichtlinie erstellen, die Einträge nach einer bestimmten Zeitspanne löscht. Weitere Informationen finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).

Wenn Sie die Feldüberwachung einrichten oder etwas im Setup ändern, werden Einträge für Ihre Änderungen erstellt. Sie können festlegen, ob Einträge im Zusammenhang mit der Überwachungseinrichtung angezeigt werden sollen, indem Sie sie ein- oder ausblenden. 

Sie können Einstellungen für die Feldüberwachung (z. B. ob eine E-Mail-Benachrichtigung gesendet oder nur die Änderung protokolliert wird) für jedes Feld auf der Seite **Arbeitsblatt „Überwachte Felder“** verwalten. Auf dieser Seite können Sie ebenfalls zu überwachende Felder hinzufügen oder entfernen.

> [!NOTE]
> Nachdem Sie ein oder mehrere Felder hinzugefügt und mit der Überwachung begonnen haben, müssen Sie sich bei [!INCLUDE[prod_short](includes/prod_short.md)] abmelden und erneut anmelden, damit Ihre Einstellungen übernommen werden.

### Mit der Feldüberwachung arbeiten

Einträge für alle geänderten Werte für überwachte Felder sind auf der Seite **Protokolleinträge für überwachte Felder** verfügbar. Die Einträge enthalten zum Beispiel die folgenden Informationen:

* Das Feld, für das der Wert geändert wurde.
* Die ursprünglichen und neuen Werte.
* Wer die Änderung vorgenommen hat und wann er sie vorgenommen hat. 

Um eine Änderung genauer zu untersuchen, wählen Sie einen Wert aus, um die Seite zu öffnen, auf der die Änderung vorgenommen wurde. Um eine Liste aller Einträge anzuzeigen, wählen Sie **Feldänderungseinträge** aus.

### Anzeigen der Feldüberwachungstelemetrie 

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, um eine Feldüberwachungsaktivität an eine Application Insights Ressource in Microsoft Azure zu senden. Anschließend erstellen Sie mit Azure Monitor Berichte und richten Warnungen für die erfassten Daten ein. Weitere Informationen finden Sie in den folgenden Artikeln in [!INCLUDE[prod_short](includes/prod_short.md)] Entwickler- und IT-Pro-Hilfe:

- [Überwachung und Analyse der Telemetrie – Aktivieren Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Ananlysieren der Feldüberwachungstelemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## Definieren von Aufbewahrungsrichtlinien

Sie können Aufbewahrungsrichtlinien erstellen, um nicht benötigte Daten in Protokollen nach einem von Ihnen angegebenen Zeitraum zu löschen. Beispielsweise kann die Anzahl der Einträge in einem Protokoll im Laufe der Zeit stark zunehmen. Durch das Bereinigen alter Einträge können Sie sich leichter auf neuere und wahrscheinlich relevantere Einträge konzentrieren. Weitere Informationen finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).

## Siehe auch

[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Sortieren, Suchen und Filtern](ui-enter-criteria-filters.md)  
[Suche nach Seiten und Informationen mit „Sie wünschen...“](ui-search.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
