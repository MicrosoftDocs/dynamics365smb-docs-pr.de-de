---
title: Daten mit Aufbewahrungsrichtlinien bereinigen
description: 'Sie können angeben, wie häufig Sie bestimmte Datentypen löschen möchten.'
author: brentholtorf
ms.topic: conceptual
ms.author: bholtorf
ms.search.keywords: 'delete, data, retention, policy, policies'
ms.search.form: '3903, 3901'
ms.date: 12/15/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="define-retention-policies"></a>Aufbewahrungsrichtlinien definieren

Dieser Artikel beschreibt, wie Administrierende Aufbewahrungsrichtlinien definieren können, um festzulegen, wie oft veraltete Daten in Tabellen gelöscht werden sollen, die Protokolleinträge und archivierte Datensätze enthalten. Das Bereinigen von Protokolleinträgen kann beispielsweise das Arbeiten mit relevanteren Daten erleichtern. Richtlinien können Daten basierend auf einem Ablaufdatum löschen, oder Sie können Filter hinzufügen, um nur bestimmte abgelaufene Daten einzubeziehen.

## <a name="required-setups-and-permissions"></a>Erforderliche Einrichtungen und Berechtigungen

Bevor Sie Aufbewahrungsrichtlinien erstellen können, müssen Sie die einzubeziehenden Tabellen und die Zeiträume für die Aufbewahrung der Daten festlegen.

|Einrichten  |Beschreibung  |
|---------|---------|
|**Zulässige Tabellen**     |Wir stellen eine Liste der Tabellen bereit, die Sie in Aufbewahrungsrichtlinien berücksichtigen können. Wenn Sie Tabellen aus einer Erweiterung zu einer Aufbewahrungsrichtlinie hinzufügen möchten, muss die Entwicklung ihre Tabellen zur Liste hinzufügen. Um mehr zu erfahren, gehen Sie zu [Ihre Erweiterung in eine Aufbewahrungsrichtlinie einbeziehen](admin-data-retention-policies.md#include-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Aufbewahrungsfristen**     |Geben Sie Zeiträume für die Aufbewahrung von Daten in den Tabellen in einer Richtlinie an. Die Zeiträume bestimmen, wie häufig Daten gelöscht werden.         |

Darüber hinaus müssen Sie über die **SUPERUSER**-Berechtigungen oder den Berechtigungssatz zum **Einrichten von Aufbewahrungsrichtlinien** verfügen. Benutzende mit der Berechtigung „Einrichten von Aufbewahrungsrichtlinien“ können Aufbewahrungsrichtlinien für Tabellen festlegen. Das gilt auch dann, wenn sie keine Lese- und Löschberechtigungen für die Tabellen haben. Der Aufgabewarteschlangenposten muss als Benutzer mit Berechtigungen zum Lesen und Löschen der Daten ausgeführt werden. Erteilen Sie den Berechtigungssatz zum Einrichten von Aufbewahrungsrichtlinien nicht an Benutzende, die zum Löschen von Daten berechtigt sein sollen.

> [!NOTE]
> Wenn Sie die lokale Version von [!INCLUDE[prod_short](includes/prod_short.md)] verwenden und Aufbewahrungsrichtlinien in der Cronus-Demodatenbank ausprobieren möchten, müssen Sie einige Vorbereitungen treffen. Das Demounternehmen enthält keine Tabellen, die Sie mit Aufbewahrungsrichtlinien verwenden können. Sie müssen diese daher hinzufügen. Erstellen Sie hierzu ein neues, leeres Unternehmen in der Demodatenbank. Importieren Sie im neuen Unternehmen das RapidStart-Konfigurationspaket für Ihr Land/Ihre Region, das dem standardmäßigen NAV17.0.W1.ENU.STANDARD.rapidstart-Paket entspricht. Die Einrichtungsdaten für Aufbewahrungsrichtlinien sind im neuen Unternehmen verfügbar.

### <a name="create-retention-periods"></a>Aufbewahrungszeiträume erstellen

Die Aufbewahrungszeiträume können beliebig lang oder kurz sein. Um Aufbewahrungszeiträume zu erstellen, verwenden Sie auf der Seite **Aufbewahrungsrichtlinien** die Aktion **Aufbewahrungszeitraum**. Die von Ihnen festgelegten Zeiträume sind für alle Richtlinien verfügbar.

> [!NOTE]
> Aus Kompatibilitätsgründen haben wir für einige Tabellen einen Mindestaufbewahrungszeitraum festgelegt. Wenn Sie einen Aufbewahrungszeitraum festlegen, der die Mindestdauer unterschreitet, wird in einer Meldung der obligatorische Mindestaufbewahrungszeitraum angezeigt.

### <a name="set-up-a-retention-policy"></a>Aufbewahrungsrichtlinie einrichten

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Aufbewahrungsrichtlinien** ein und wählen Sie den zugehörigen Link.
2. Geben Sie im Feld **Tabellen-ID** die Tabelle ein, die in der Richtlinie berücksichtigt werden soll.
3. Geben Sie im Feld **Aufbewahrungszeitraum** an, wie lange die Daten in der Tabelle verbleiben sollen.
4. Optional: Sie können die Richtlinie auf bestimmte Daten in einer Tabelle statt auf alle Datensätze anwenden, indem Sie die Daten für jede Zeile filtern. Die Richtlinie gilt nur für die Datensätze, die die Filter zurückgeben. Um die Filterkriterien anzugeben, deaktivieren Sie den Umschalter **Auf alle Datensätze anwenden**. Das Inforegister **Datensatzaufbewahrungsrichtlinie** wird angezeigt, wo Sie Filterkriterien festlegen können. Weitere Informationen zur Funktionsweise von Filtern finden Sie unter [Filtern](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Jede Zeile hat ihren eigenen Aufbewahrungszeitraum. Wenn Sie für dieselben Daten unterschiedliche Aufbewahrungszeiträume angeben, wird der längste Zeitraum verwendet. Einige Tabellen enthalten auch Filter, die Sie nicht ändern oder entfernen können. Um Ihnen die Identifizierung dieser Filter zu erleichtern, werden sie in einer helleren Schrift angezeigt.

#### <a name="video-guidance"></a>Videoanleitung

Dieses Video zeigt ein Beispiel für die Einrichtung einer Aufbewahrungsrichtlinie.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1fLeJ]

## <a name="apply-retention-policies"></a>Aufbewahrungsrichtlinien anwenden

Sie können einen Aufgabenwarteschlangenposten zum Anwenden von Aufbewahrungsrichtlinien verwenden, um Daten automatisch zu löschen, oder Sie können Richtlinien manuell anwenden.

Um eine Aufbewahrungsrichtlinie automatisch anzuwenden, erstellen und aktivieren Sie einfach eine Richtlinie. Wenn Sie eine Richtlinie aktivieren, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] einen Aufgabenwarteschlangenposten, der je nach dem angegebenen Aufbewahrungszeitraum angewendet wird. Alle Aufbewahrungsrichtlinien verwenden denselben Aufgabenwarteschlangenposten. Standardmäßig wendet der Aufgabenwarteschlangenposten die Richtlinie jeden Tag um 02:00 Uhr an. Sie können die Standardeinstellung ändern. Wir empfehlen Ihnen jedoch, die Ausführung außerhalb der Geschäftszeiten zu legen. Mehr erfahren Sie unter [Aufgabenwarteschlangen zum Planen von Aufgaben verwenden](admin-job-queues-schedule-tasks.md). 

Sie können eine Richtlinie manuell anwenden, indem Sie die Aktion **Manuell anwenden** auf der Seite **Aufbewahrungsrichtlinien** verwenden. Wenn Sie eine Richtlinie immer manuell anwenden möchten, aktivieren Sie die Option **Manuell**. Der Aufgabenwarteschlangenposten ignoriert die Richtlinie, wenn er ausgeführt wird.

## <a name="view-retention-policy-log-entries"></a>Protokolleinträge für Aufbewahrungsrichtlinien anzeigen

Sie können Aktivitäten im Zusammenhang mit Aufbewahrungsrichtlinien auf der Seite **Aufbewahrungsrichtlinienprotokoll** anzeigen. Beispielsweise werden Einträge erstellt, wenn eine Richtlinie angewendet wird oder aufgetreten sind.

## <a name="include-your-extension-in-a-retention-policy-requires-help-from-a-developer"></a>Ihre Erweiterung in eine Aufbewahrungsrichtlinie einbeziehen (erfordert die Unterstützung der Entwicklung)

Standardmäßig decken die Aufbewahrungsrichtlinien nur [!INCLUDE[prod_short](includes/prod_short.md)] in der von uns bereitgestellten Liste ab. Sie können Standardtabellen aus der Liste entfernen und eigene Tabellen hinzufügen. Das heißt, Sie können keine Tabelle hinzufügen, die Sie nicht selbst erstellt haben. Sie können beispielsweise keine anderen Tabellen von [!INCLUDE[prod_short](includes/prod_short.md)] oder von einer Erweiterung, die Sie gekauft haben, hinzufügen.

Um Ihre Tabellen zur Liste der zulässigen Tabellen hinzuzufügen, muss die Entwicklung Code hinzufügen. Zum Beispiel an die Installer-Codeunit für die Erweiterung (eine Codeunit mit dem Untertyp *installieren*).

Wenn ein Entwickler eine Tabelle hinzufügt, kann er obligatorische Filter und Standardfilter angeben. Obligatorische Filter können später nicht entfernt oder geändert werden, wenn Sie Tabellen hinzufügen, um eine Aufbewahrungsrichtlinie festzulegen. Die Standardfilter sind lediglich Vorschläge.

Im Folgenden finden Sie Beispiele zum Hinzufügen einer Tabelle zur Liste der zulässigen Tabellen mit und ohne obligatorische Filter oder Standardfilter. Ein komplexeres Beispiel finden Sie in der Codeunit 3999 „Aufb. -Richtl. install. – Basis-App“.

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
