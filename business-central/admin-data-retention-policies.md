---
title: Daten mit Aufbewahrungsrichtlinien bereinigen
description: Sie können angeben, wie häufig Sie bestimmte Datentypen löschen möchten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delete, data, retention, policy, policies
ms.search.form: 3903, 3901
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: a6fee7aedd8fca20e032bc3ac67e5f9e26d1fb22
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517082"
---
# <a name="define-retention-policies"></a>Aufbewahrungsrichtlinien definieren
Administratoren können Aufbewahrungsrichtlinien definieren, um festzulegen, wie häufig [!INCLUDE[prod_short](includes/prod_short.md)] veraltete Daten in Tabellen löschen soll, die Protokolleinträge und archivierte Datensätze enthalten. Das Bereinigen von Protokolleinträgen kann beispielsweise das Arbeiten mit tatsächlich relevanten Daten erleichtern. Richtlinien können alle Daten in den Tabellen beinhalten, die nach dem Ablaufdatum liegen, oder Sie können Filterkriterien hinzufügen, die nur bestimmte abgelaufene Daten in die Richtlinie aufnehmen. 

## <a name="required-setups-and-permissions"></a>Erforderliche Einrichtungen und Berechtigungen
Bevor Sie Aufbewahrungsrichtlinien erstellen können, müssen Sie Folgendes einrichten:

|Einrichtung  |Beschreibung  |
|---------|---------|
|**Zulässige Tabellen**     |Wir stellen eine Liste der Tabellen bereit, die in Aufbewahrungsrichtlinien berücksichtigt werden können. Wenn Sie jedoch Tabellen aus einer Erweiterung zu einer Aufbewahrungsrichtlinie hinzufügen möchten, muss ein Entwickler seine Tabellen zur Liste hinzufügen. Weitere Informationen finden Sie unter [Ihre Erweiterung in eine Aufbewahrungsrichtlinie einbeziehen](admin-data-retention-policies.md#including-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Aufbewahrungszeiträume**     |Geben Sie Zeiträume für die Aufbewahrung von Daten in den Tabellen in einer Richtlinie an. Die Zeiträume bestimmen, wie häufig Daten gelöscht werden.         |

Darüber hinaus müssen Sie über die SUPERUSER-Berechtigungen oder den Berechtigungssatz zum Einrichten von Aufbewahrungsrichtlinien verfügen. Benutzer, denen der Berechtigungssatz zum Einrichten von Aufbewahrungsrichtlinien erteilt wurde, können Aufbewahrungsrichtlinien für Tabellen definieren, auch wenn sie keine Lese- und Löschberechtigungen für diese Tabellen haben. Der Aufgabewarteschlangenposten muss als Benutzer mit Berechtigungen zum Lesen und Löschen der Daten ausgeführt werden. Wir empfehlen, den Berechtigungssatz zum Einrichten von Aufbewahrungsrichtlinien nur den Benutzern zu erteilen, die zum Löschen von Daten berechtigt sein sollen.

> [!NOTE]
> Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises verwenden und Aufbewahrungsrichtlinien in der Cronus-Demodatenbank ausprobieren möchten, müssen Sie einige Vorbereitungen treffen. Das Demounternehmen enthält keine Tabellen, die Sie mit Aufbewahrungsrichtlinien verwenden können. Sie müssen diese daher hinzufügen. Erstellen Sie hierzu ein neues, leeres Unternehmen in der Demodatenbank. Importieren Sie im neuen Unternehmen das RapidStart-Konfigurationspaket für Ihr Land, das dem standardmäßigen NAV17.0.W1.ENU.STANDARD.rapidstart-Paket entspricht. Die Einrichtungsdaten für Aufbewahrungsrichtlinien sind im neuen Unternehmen verfügbar.

### <a name="to-create-retention-periods"></a>So erstellen Sie Aufbewahrungszeiträume
Die Aufbewahrungszeiträume können beliebig lang oder kurz sein. Um Aufbewahrungszeiträume zu erstellen, verwenden Sie auf der Seite **Aufbewahrungsrichtlinien** die Aktion **Aufbewahrungszeitraum**. Die von Ihnen definierten Zeiträume sind für alle Richtlinien verfügbar.

> [!NOTE]
> Aus Kompatibilitätsgründen haben wir für einige Tabellen einen Mindestaufbewahrungszeitraum festgelegt. Wenn Sie einen Aufbewahrungszeitraum festlegen, der die Mindestdauer unterschreitet, wird in einer Meldung der obligatorische Mindestaufbewahrungszeitraum angezeigt.

### <a name="set-up-a-retention-policy"></a>Aufbewahrungsrichtlinie einrichten
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufbewahrungsrichtlinien** ein und wählen Sie den zugehörigen Link.
2. Geben Sie im Feld **Tabellen-ID** die Tabelle ein, die in der Richtlinie berücksichtigt werden soll.
3. Geben Sie im Feld **Aufbewahrungszeitraum** an, wie lange die Daten in der Tabelle verbleiben sollen.
4. Optional: Um die Richtlinie auf bestimmte Daten in einer Tabelle anzuwenden, deaktivieren Sie die Option „Auf alle Datensätze anwenden“. Das Inforegister „Datensatzaufbewahrungsrichtlinie“ wird angezeigt, in dem Sie Filter festlegen können, um Teilmengen von Daten für jede Zeile zu erstellen. Weitere Informationen finden Sie unter [Filterung](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Jede Zeile hat ihren eigenen Aufbewahrungszeitraum. Wenn Sie für dieselben Daten unterschiedliche Aufbewahrungszeiträume angeben, wird der längste Zeitraum verwendet. Einige Tabellen enthalten auch Filter, die Sie nicht ändern oder entfernen können. Um Ihnen die Identifizierung dieser Filter zu erleichtern, werden sie in einer helleren Schrift angezeigt.

## <a name="applying-retention-policies"></a>Anwenden von Aufbewahrungsrichtlinien
Sie können einen Aufgabenwarteschlangenposten zum Anwenden von Aufbewahrungsrichtlinien verwenden, um Daten automatisch zu löschen, oder Sie können Richtlinien manuell anwenden.

Um eine Aufbewahrungsrichtlinie automatisch anzuwenden, erstellen und aktivieren Sie einfach eine Richtlinie. Wenn Sie eine Richtlinie aktivieren, erstellen wir einen Aufgabenwarteschlangenposten, der Aufbewahrungsrichtlinien entsprechend dem von Ihnen angegebenen Aufbewahrungszeitraum anwendet. Alle Aufbewahrungsrichtlinien verwenden denselben Aufgabenwarteschlangenposten. Standardmäßig wendet der Aufgabenwarteschlangenposten die Richtlinie jeden Tag um 02:00 Uhr an. Sie können die Standardeinstellung ändern. Wir empfehlen Ihnen jedoch, die Ausführung außerhalb der Geschäftszeiten zu legen. Weitere Informationen finden Sie unter [Job-Warteschlangen zur Einplanung von Aufgaben verwenden](admin-job-queues-schedule-tasks.md). 

Sie können eine Richtlinie manuell anwenden, indem Sie die Aktion **Manuell anwenden** auf der Seite **Aufbewahrungsrichtlinien** verwenden. Wenn Sie eine Richtlinie immer manuell anwenden möchten, aktivieren Sie die Option **Manuell**. Der Aufgabenwarteschlangenposten ignoriert die Richtlinie, wenn er ausgeführt wird.

## <a name="viewing-retention-policy-log-entries"></a>Anzeigen von Protokolleinträgen für Aufbewahrungsrichtlinien
Sie können Aktivitäten im Zusammenhang mit Aufbewahrungsrichtlinien auf der Seite **Aufbewahrungsrichtlinienprotokoll** anzeigen. Beispielsweise werden Einträge erstellt, wenn eine Richtlinie angewendet wird oder wenn dabei Fehler aufgetreten sind. 

## <a name="including-your-extension-in-a-retention-policy-requires-help-from-a-developer"></a>Ihre Erweiterung in eine Aufbewahrungsrichtlinie einbeziehen (erfordert die Unterstützung eines Entwicklers)
Standardmäßig decken Aufbewahrungsrichtlinien nur Tabellen ab, die in der Liste der von uns bereitgestellten [!INCLUDE[prod_short](includes/prod_short.md)]-Tabellen enthalten sind. Sie können Standardtabellen aus der Liste entfernen und eigene Tabellen hinzufügen. Das heißt, Sie können keine Tabelle hinzufügen, die Sie nicht selbst erstellt haben. Sie können beispielsweise keine anderen Tabellen von [!INCLUDE[prod_short](includes/prod_short.md)] oder von einer Erweiterung, die Sie gekauft haben, hinzufügen.

Um Ihre Tabellen zur Liste der zulässigen Tabellen hinzuzufügen, muss ein Entwickler Code hinzufügen, z. B. zur Installer-Codeunit für die Erweiterung (eine Codeunit mit dem Untertyp *install*). 

Wenn ein Entwickler eine Tabelle hinzufügt, kann er obligatorische Filter und Standardfilter angeben. Obligatorische Filter können später nicht entfernt oder geändert werden, wenn Sie Tabellen hinzufügen, um eine Aufbewahrungsrichtlinie zu definieren. Standardfilter sind lediglich Vorschläge.

Im Folgenden finden Sie Beispiele zum Hinzufügen einer Tabelle zur Liste der zulässigen Tabellen mit und ohne obligatorische Filter oder Standardfilter. Ein komplexeres Beispiel finden Sie in der Codeunit 3999 „Aufb. -Richtl.  install. – Basis-App“. 

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

Das folgende Beispiel enthält einen obligatorischen Filter.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Nachdem ein Entwickler der Liste Tabellen hinzugefügt hat, kann ein Administrator diese in eine Aufbewahrungsrichtlinie aufnehmen. 

## <a name="see-also"></a>Siehe auch

[Analysieren der Trace-Telemetrie von Aufbewahrungsrichtlinien](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Protokollieren von Änderungen in Business Central](across-log-changes.md)  
[Filterung](ui-enter-criteria-filters.md#filtering)  
[Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung](admin-job-queues-schedule-tasks.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]