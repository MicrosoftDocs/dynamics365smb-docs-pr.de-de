---
title: Änderungen prüfen | Microsoft Docs
description: Sie können ein Benutzerprotokoll aktivieren, sodass Sie Aufzeichnungen über sämtliche Änderungen haben, die an den Daten in verfolgten Tabellen vorgenommen werden. Sie können Aktivitäten auch mit bestimmten Arten von Aktivitätsprotokollen verfolgen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c4891cb047cb16f4051b6f468115e2b6bad9f24c
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470362"
---
# <a name="auditing-changes-in-business-central"></a>Protokollieren von Änderungen in Business Central
Eine häufige Herausforderung in vielen Anwendungen zur Unternehmensverwaltung ist die Vermeidung unerwünschter Datenänderungen. Es könnte alles sein – von einer falschen Debitorentelefonnummer bis hin zu einer falschen Buchung in der Finanzbuchhaltung. In diesem Thema werden die Funktionen beschrieben, mit denen Sie herausfinden können, was geändert wurde, wer es geändert hat und wann die Änderung vorgenommen wurde.

## <a name="about-the-change-log"></a>Informationen zum Änderungsprotokoll 
Die Änderungsprotokollfunktion ermöglicht die Verfolgung aller direkten Änderungen, die von einem Benutzer an den Daten in der Datenbank vorgenommen werden. Sie müssen jede Tabelle und jedes Feld festlegen, die/das die Anwendung protokollieren soll, und dann das Änderungsprotokoll aktivieren.  

Das Nachverfolgen von Änderungen kann sich auf die Leistung auswirken, was Sie Zeit kosten kann. Möglicherweise wird auch die Datenbankgröße erhöht, was Sie Geld kosten kann. Um diese Kosten zu senken, sollten Sie Folgendes berücksichtigen:
- Gehen Sie bei der Auswahl der Tabellen und Arbeitsgänge vorsichtig vor.
- Fügen Sie keine Posten und gebuchten Dokumente hinzu. Priorisieren Sie stattdessen Systemfelder wie „Erstellt von“ und „Erstellungsdatum“.
- Verwenden Sie nicht den Tracking-Typ „Alle Felder“. Wählen Sie stattdessen „Einige Felder“ und verfolgen Sie nur die wichtigsten Felder.

Das Änderungsprotokoll basiert auf Änderungen, die an den Daten in den von Ihnen verfolgten Tabellen vorgenommen werden. Auf der Seite **Änderungsprotokollposten** werden Posten chronologisch aufgeführt und alle Änderungen angezeigt, die an den Werten in den Feldern der von Ihnen angegebenen Tabellen vorgenommen wurden.

> [!Important]
> Änderungen werden in **Änderungsprotokollposten** erst angezeigt, nachdem die Sitzung des Benutzers neu gestartet wurde, was folgendermaßen geschieht:
<br />
> * Die Sitzung war abgelaufen und wurde aktualisiert.
> * Der Benutzer hat ein anderes Unternehmen oder Rollencenter ausgewählt.
> * Der Benutzer hat sich an- und wieder angemeldet.

### <a name="working-with-the-change-log"></a>Arbeiten mit dem Änderungsprotokoll
Sie verwenden die Seite **Änderungsprotokoll einrichten** zum Aktivieren bzw. Deaktivieren des Änderungsprotokolls. Wenn Sie das Änderungsprotokoll aktivieren bzw. deaktivieren, wird diese Aktivität protokolliert, sodass Sie immer sehen, welcher Anwender die Protokollierung an- bzw. abgeschaltet hat.

Wenn Sie auf der Seite **Änderungsprotokoll Einrichtung** die Aktion **Tabellen** wählen, können Sie angeben, welche Tabellen auf Änderungen verfolgt werden sollen, und welche Änderungen verfolgt werden sollen. [!INCLUDE[prod_short](includes/prod_short.md)] verfolgt auch mehrere Systemtabellen.

> [!NOTE]
> Sie können bestimmte Felder auf Änderungen überwachen, z. B. Felder, die sensible Daten enthalten, indem Sie die Feldüberwachung einrichten. Wenn Sie dies tun, ist die Tabelle, die das Feld enthält, zur Vermeidung von Redundanz nicht für die Einrichtung des Änderungsprotokolls verfügbar. Weitere Informationen finden Sie unter [Überwachen sensibler Felder](across-log-changes.md#monitoring-sensitive-fields).

Wenn Sie das Änderungsprotokoll eingerichtet und aktiviert haben und jemand Daten verändert hat, protokolliert die Anwendung die Änderung in einem **Änderungsprotokollposten**. Wenn Sie Posten löschen möchten, können Sie dies auf der Seite **Änderungsprotokollposten löschen** tun, an dem Sie Filter auf Basis Datum und Zeit festlegen können.  

## <a name="about-activity-logs"></a>Informationen zu Aktivitätsprotokollen
Von einigen Seiten in [!INCLUDE [prod_short](includes/prod_short.md)] können Sie ein Aktivitätsprotokoll anzeigen, in dem der Status und alle Fehler von Dateien angezeigt werden, aus denen Sie exportieren oder in die Sie importieren [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="working-with-activity-logs"></a>Arbeiten mit Aktivitätsprotokollen
Die Informationen werden auf der Seite **Aktivitätsprotokoll** angezeigt, entsprechend dem Kontext, aus dem sie geöffnet wurden. Sie können die Seite beispielsweise über die Seiten **Belegaustauschdienst – Einrichtung**, **Eingehender Beleg**, **Gebuchte Verkaufsrechnung** und **Geb. Verkaufsgutschrift** öffnen. Sie können die Liste der Protokolleinträge leeren oder die Liste der Einträge löschen, die älter als sieben Tage sind.  

## <a name="monitoring-sensitive-fields"></a>Überwachen sensibler Felder
Der Schutz sensibler Daten ist für die meisten Unternehmen ein zentrales Anliegen. Um eine Sicherheitsebene hinzuzufügen, können Sie wichtige Felder überwachen und sich per E-Mail benachrichtigen lassen, wenn jemand einen Wert ändert. Sie können sich beispielsweise benachrichtigen lassen, wenn jemand die IBAN Ihres Unternehmens ändert.

> [!NOTE]
> Um den Versand von Benachrichtigungen per E-Mail zu ermöglichen, müssen Sie die E-Mail-Funktion in [!INCLUDE[prod_short](includes/prod_short.md)] einrichten. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).

### <a name="setting-up-field-monitoring"></a>Einrichten der Feldüberwachung
Sie können die Anleitung zum unterstützten Setup **Einrichtung der Überwachung von Feldänderungen** verwenden, um die Felder anzugeben, die Sie anhand von Filterkriterien überwachen möchten, z. B. die Klassifizierung der Datensensibilität für die Felder. Weitere Informationen finden Sie unter [Datensensitivität klassieren](admin-classifying-data-sensitivity.md). Mit dieser Anleitung können Sie auch die Person angeben, die bei einer Änderung eine E-Mail-Benachrichtigung erhalten soll, sowie das E-Mail-Konto, das die Benachrichtigungs-E-Mail sendet. Sie müssen sowohl die Benutzerbenachrichtigung als auch das Konto angeben, von dem aus die Benachrichtigung gesendet werden soll. Wenn Sie die Anleitung abgeschlossen haben, können Sie die Einstellungen für die Feldüberwachung auf der Seite **Feldüberwachungseinrichtung** verwalten. 

Im Laufe der Zeit nimmt die Liste der Einträge auf der Seite **Protokolleinträge für überwachte Felder** zu. Um die Anzahl der Einträge zu verringern, können Sie eine Aufbewahrungsrichtlinie erstellen, mit der Einträge nach einem bestimmten Zeitraum gelöscht werden. Weitere Informationen finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).

Wenn Sie die Feldüberwachung einrichten oder etwas im Setup ändern, werden Einträge für Ihre Änderungen erstellt. Sie können festlegen, ob Einträge im Zusammenhang mit der Überwachungseinrichtung angezeigt werden sollen, indem Sie sie ein- oder ausblenden. 

Sie können Einstellungen für die Feldüberwachung (z. B. ob eine E-Mail-Benachrichtigung gesendet oder nur die Änderung protokolliert wird) für jedes Feld auf der Seite **Arbeitsblatt „Überwachte Felder“** verwalten. Auf dieser Seite können Sie ebenfalls zu überwachende Felder hinzufügen oder entfernen.

> [!NOTE]
> Nachdem Sie ein oder mehrere Felder hinzugefügt und mit der Überwachung begonnen haben, müssen Sie sich bei [!INCLUDE[prod_short](includes/prod_short.md)] abmelden und erneut anmelden, damit Ihre Einstellungen übernommen werden.

### <a name="working-with-field-monitoring"></a>Arbeiten mit der Feldüberwachung

Einträge für alle geänderten Werte für überwachte Felder sind auf der Seite **Protokolleinträge für überwachte Felder** verfügbar. Einträge enthalten beispielsweise Informationen wie das Feld, für das der Wert geändert wurde, die ursprünglichen und neuen Werte sowie die Person, die die Änderung vorgenommen hat und der Zeitpunkt der Änderung. Um eine Änderung genauer zu untersuchen, wählen Sie einen Wert aus, um die Seite zu öffnen, auf der die Änderung vorgenommen wurde. Um eine Liste aller Einträge anzuzeigen, wählen Sie **Feldänderungseinträge** aus.

### <a name="viewing-field-monitoring-telemetry"></a>Anzeigen der Feldüberwachungstelemetrie 

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, um eine Feldüberwachungsaktivität an eine Application Insights Ressource in Microsoft Azure zu senden. Anschließend erstellen Sie mit Azure Monitor Berichte und richten Warnungen für die erfassten Daten ein. Weitere Informationen finden Sie in den folgenden Artikeln in [!INCLUDE[prod_short](includes/prod_short.md)] Entwickler- und IT-Pro-Hilfe:

- [Überwachung und Analyse der Telemetrie – Aktivieren Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Ananlysieren der Feldüberwachungstelemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="defining-retention-policies"></a>Definieren von Aufbewahrungsrichtlinien

Sie können Aufbewahrungsrichtlinien erstellen, um nicht benötigte Daten in Protokollen nach einem von Ihnen angegebenen Zeitraum zu löschen. Beispielsweise kann die Anzahl der Einträge in einem Protokoll im Laufe der Zeit stark zunehmen. Durch das Bereinigen alter Einträge können Sie sich leichter auf neuere und wahrscheinlich relevantere Einträge konzentrieren. Weitere Informationen finden Sie unter [Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md).

## <a name="see-also"></a>Siehe auch
[Ändern von grundlegenden Einstellungen](ui-change-basic-settings.md)  
[Sortieren, Suchen und Filtern](ui-enter-criteria-filters.md)  
[Suche nach Seiten und Informationen mit Tell Me](ui-search.md)  
[Berechtigungen an Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md)    
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Aufbewahrungsrichtlinien definieren](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
