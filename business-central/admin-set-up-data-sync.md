---
title: 'Richten Sie Unternehmen ein, um Stammdaten zu synchronisieren'
description: 'Erfahren Sie, wie Sie ein oder mehrere Unternehmen einrichten, um Stammdaten zu synchronisieren.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# <a name="get-ready-to-synchronize-master-data"></a>Vorbereitung der Synchronisierung der Masterdaten

Wenn zwei oder mehr Unternehmen teilweise dieselben Stammdaten verwenden, können Sie die Daten synchronisieren, anstatt sie manuell in jedem Unternehmen hinzuzufügen. Die Synchronisierung der Daten ist zum Beispiel besonders nützlich, wenn Sie neue Tochterunternehmen gründen.

Stammdaten umfassen Einstellungen und nicht transaktionale Informationen über Geschäftseinheiten. Zum Beispiel Debitoren, Kreditoren, Artikel und Mitarbeitende. Die Daten bieten Kontext für Geschäftstransaktionen. Nachfolgend einige Beispiele für Stammdaten eines Kunden:

* Name
* Identifikationsnummer
* Adresse
* Zahlungsbedingungen
* Kreditgrenze

In diesem Fenster richten Sie die Synchronisierung untergeordneter Unternehmen ein. Unter Verwendung eines Pull-Modells ziehen Tochtergesellschaften die Daten aus dem Quellunternehmen, die sie für die Geschäftsabwicklung benötigen. Nachdem Sie die Synchronisierung eingerichtet und zum ersten Mal Daten synchronisiert haben, sind Sie fertig. Auftragswarteschlangeneinträge aktualisiert gekoppelte Datensätze in den Tochtergesellschaften, wenn jemand Daten im Quellunternehmen ändert.

## <a name="uni-directional-synchronization-only"></a>Nur eindirektionale Synchronisierung

Sie können Daten nur vom Quellunternehmen mit den Tochterunternehmen im Pullverfahren synchronisieren. Tochterunternehmen können keine Daten an das Quellunternehmen übertragen.

> [!NOTE]
> Obwohl es möglich ist, empfehlen wir nicht, die bidirektionale Synchronisierung einzurichten. Das heißt, das Synchronisieren von Daten vom Quellunternehmen mit den Tochterunternehmen und von den Tochterunternehmen mit dem Quellunternehmen. Das Synchronisieren von Daten in beide Richtungen kann zu Konflikten oder unerwünschten Überschreibungen führen.

## <a name="before-you-start"></a>Bevor Sie beginnen

Im Folgenden finden Sie Voraussetzungen für die Einrichtung der Synchronisierung.

* Alle Unternehmen müssen in der selben Umgebung sein.
* Der Benutzende, der die Tochtergesellschaft einrichtet, muss über die Lizenz **Essential**, **Premium** oder **Basic ISV** verfügen.

> [!NOTE]
> Mit den Lizenzen für Teammitglieder und interne Administrierende können man auf Datensätze zugreifen, sie jedoch nicht ändern, sodass sie nicht zum Einrichten der Synchronisierung verwendet werden können. Mit der Lizenz für delegierte Administrierende können Sie keine Hintergrundaufgaben planen, sodass Sie die Einrichtung nicht abschließen können.

## <a name="specify-the-source-company"></a>Quellunternehmen definieren

Die ersten Schritte bestehen darin, das Unternehmen anzugeben, das die Datenquelle sein soll, und die Synchronisierung zu aktivieren. Tochterunternehmen beziehen Daten aus dem Quellunternehmen.

> [!NOTE]
> Wenn Sie die Synchronisierung aktivieren, erstellt und plant [!INCLUDE [prod_short](includes/prod_short.md)] die Aufgabenwarteschlangeneinträge, die die Daten synchronisieren. Es könnte so aussehen, als ob die Einträge die Daten sofort synchronisieren, aber das ist nicht der Fall. Die erstellten Jobwarteschlangeneinträge synchronisieren nur gekoppelte Datensätze, und Sie haben dies zu diesem Zeitpunkt noch nicht eingerichtet. Die Synchronisierung beginnt, nachdem Sie [Tabellen und Felder aktivieren oder deaktivieren](#enable-or-disable-tables-and-fields) und [zum ersten Mal synchronisieren](#synchronize-for-the-first-time).

1. Wählen Sie in einem untergeordneten Unternehmen die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Masterdaten-Verwaltungseinrichtung** ein, und wählen Sie dann den entsprechenden Link.
1. Geben Sie im Feld **Quellunternehmen** das Unternehmen an, von dem Sie die Änderungen abrufen.
1. Aktivieren Sie den Umschalter **Synchronisierung aktivieren**.
1. Wählen Sie in der Bestätigungsmeldung **OK** aus. [!INCLUDE [prod_short](includes/prod_short.md)] findet die Tabellen und Felder, die von der Quellfirma verfügbar sind.

Der nächste Schritt besteht darin, Tabellen und Felder für die Synchronisierung zu aktivieren.

## <a name="enable-or-disable-tables-and-fields"></a>Aktivieren oder deaktivieren Sie Tabellen und Felder

Um Zeit zu sparen, stellt [!INCLUDE [prod_short](includes/prod_short.md)] eine Liste von Tabellen bereit, die Unternehmen häufig synchronisieren. Diese Tabellen sind standardmäßig für die Synchronisierung aktiviert. Sie können sie nach Belieben ändern, deaktivieren oder löschen. Zur zusätzlichen Zeitersparnis sind einige Felder in den Tabellen bereits deaktiviert, da sie für die Tochtergesellschaft wahrscheinlich nicht relevant sind.

> [!NOTE]
> Wenn im Quellunternehmen eine oder mehrere Erweiterungen installiert sind und eine Tochtergesellschaft die Synchronisierung einrichtet, enthält die Seite **Synchronisierungstabellen** Tabellen aus den Erweiterungen, und Sie können auf deren Felder zugreifen. Wenn das Quellunternehmen jedoch eine Erweiterung hinzufügt, nachdem die Synchronisierung eingerichtet wurde, muss jede Tochtergesellschaft die Tabellen manuell hinzufügen. Weitere Informationen zum Hinzufügen von Tabellen finden Sie unter [Tabellen zur Synchronisierungstabellenliste hinzufügen oder löschen](#add-or-delete-tables-from-the-synchronization-tables-list). Weitere Informationen zum Erweitern von [!INCLUDE [prod_short](includes/prod_short.md)] finden Sie unter [Entwicklung von Erweiterungen in Visual Studio Code](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Masterdaten-Verwaltungseinrichtung** ein, und wählen Sie dann den entsprechenden Link.
1. Wählen Sie die **Tabellen synchronisieren**-Aktion aus.
1. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Das Feld **Tabellenfilter** ist hilfreich, um zu steuern, was für eine Tabelle synchronisiert werden soll. Sie können Filter so einrichten, dass sie nur dann synchronisiert werden, wenn bestimmte Bedingungen erfüllt sind. Beispielsweise können Sie Filter hinzufügen, die angeben, dass Sie nur Anbieter in einer bestimmten Region synchronisieren. Oder Kunden, die eine bestimmte Währung verwenden.
>
> Wenn die Tochtergesellschaft bereits Daten in ihren Tabellen hat, besteht eine weitere gute Möglichkeit zum Festlegen von Kriterien für die Synchronisierung darin, eine trefferbasierte Kopplung einzurichten. Weitere Informationen zum Abgleich finden Sie unter [Kopplung basierend auf Übereinstimmung verwenden](#use-match-based-coupling).

1. Um Felder für eine Tabelle zu aktivieren, wählen Sie die Tabelle und dann die Aktion **Felder**.
1. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Eine schnelle Möglichkeit, mehrere Felder gleichzeitig zu aktivieren oder zu deaktivieren, besteht darin, sie in der Liste auszuwählen und dann die Aktionen **Aktivieren** oder **Deaktivieren** zu verwenden.

### <a name="use-match-based-coupling"></a>Kopplung basierend auf Übereinstimmung verwenden

Sie können die für eine Tabelle zu synchronisierenden Daten angeben, indem Sie Datensätze basierend auf Kriterien abgleichen. Wählen Sie auf der SEite **Masterdaten-Verwaltung einrichten** **Kopplung basierend auf Übereinstimmung** und öffnen Sie die Seite **Kopplungskriterien** auswählen. Folgende Kriterien können Sie für Ihre Zuordnung definieren:

* Geben Sie an, ob nach dem Koppeln von Datensätzen eine Synchronisierung erfolgen soll.
* Legen Sie fest, ob ein neuer Datensatz im untergeordneten Unternehmen erstellt werden soll, falls anhand der Abgleichskriterien keine eindeutige, ungekoppelte Übereinstimmung gefunden werden kann. Um diese Funktionalität zu aktivieren, wählen Sie die Aktion **Neu erstellen, wenn keine Übereinstimmung gefunden werden kann**.
* Die Felder, die zum Abgleichen von Datensätzen verwendet werden sollen, und ob bei der Übereinstimmung zwischen Groß- und Kleinschreibung unterschieden wird.
* Legen Sie die Reihenfolge fest, in der die Datensätze durchsucht werden, indem Sie eine Übereinstimmungspriorität für die entsprechenden Zuordnungsfelder angeben. [!INCLUDE [prod_short](includes/prod_short.md)] sucht basierend auf dem Wert im Feld Übereinstimmungspriorität in aufsteigender Reihenfolge nach einer Übereinstimmung. Ein leerer Wert im Feld Übereinstimmungspriorität ist gleich der Priorität 0, bei der es sich um die höchste Priorität handelt. Felder mit der Priorität 0 werden zuerst berücksichtigt.

## <a name="synchronize-for-the-first-time"></a>Zum ersten Mal synchronisieren

Wenn Sie fertig sind, wählen Sie auf der Seite **Masterdaten-Verwaltung einrichten** die Aktion **Erste Synchronisierung starten** aus. Wählen Sie auf der Seite **Erste Synchronisierung der Masterdaten** den Synchronisierungstyp aus, den Sie für jede Tabelle verwenden möchten.

* Wenn Sie bereits Datensätze sowohl in der Quell- als auch in den Tochterunternehmen haben und vorhandene Datensätze abgleichen möchten, wählen Sie die Aktion **Übereinstimmungsbasierte Kopplung verwenden** aus. [!INCLUDE [prod_short](includes/prod_short.md)] gleicht Datensätze in der Tochtergesellschaft mit Datensätzen im Quellunternehmen ab. Die Übereinstimmungen basieren auf von Ihnen festgelegten Übereinstimmungskriterien. Für mehrere Standardtabellen hat [!INCLUDE [prod_short](includes/prod_short.md)] bereits vorhandene Datensätze anhand ihres Primärschlüssels abgeglichen, aber Sie können dies ändern, wenn Sie möchten. Sie können die Synchronisierung auch neue Datensätze in der Tochtergesellschaft für Datensätze in der Quellfirma erstellen lassen, die die Tochtergesellschaft nicht hat. Weitere Informationen zum Abgleich finden Sie unter [Kopplung basierend auf Übereinstimmung verwenden](#use-match-based-coupling).
* Wenn Sie **Vollständige Synchronisierung ausführen** auswählen, erstellt die Synchronisierung neue Datensätze für alle Datensätze im Quellunternehmen, die noch nicht gekoppelt sind. Diese Option ist beispielsweise in den folgenden Szenarien hilfreich:

    * Die Tochtergesellschaft verfügt über keine Daten in der Tabelle.
    * Sie möchten Datensätze des Quellunternehmens hinzufügen, ohne sie abzugleichen.  

Nachdem Sie die zu verwendende Option ausgewählt haben, wählen Sie die Aktion **Alle starten**, um die Synchronisierung zu starten.

Während die Synchronisierung ausgeführt wird, zeigt die Spalte **Auftragsstatus** auf der Seite **Erste vollständige Synchronisierung der Stammdaten** den jeweiligen Status jeder Auftragswarteschlange an. Drücken Sie **F5** auf Ihrer Tastatur, um den Status zu aktualisieren.

> [!TIP]
> Tabellen werden in einer vordefinierten Reihenfolge synchronisiert. Wenn die Synchronisierung bei einer Tabelle hängen bleibt, wählen Sie die Tabelle aus und wählen Sie dann die Aktion **Neu starten**, um sie wieder in Gang zu bringen.

Um auf Details wie die Anzahl der eingefügten oder geänderten Datensätze zuzugreifen, wählen Sie den Wert in der Spalte **Auftragsstatus** aus, um die **Ansicht – Integrationssynchronisierungsjobs** zu öffnen. Bei eingefügten Datensätzen können Sie die Nummer in der Spalte **Eingefügt** auswählen, um auf weitere Details der neuen Datensätzen zuzugreifen.

## <a name="add-or-delete-tables-from-the-synchronization-tables-list"></a>Hinzufügen oder Löschen von Tabellen aus der Synchronisierungstabellenliste

### <a name="add-a-table"></a>Eine Tabelle hinzufügen

> [!IMPORTANT]
> Obwohl Tabellen mit Transaktionsdaten in der Liste verfügbar sind, wie z. B. Tabellen mit Hauptbucheinträgen, sollten Sie sie nicht auswählen. Die Synchronisierung funktioniert nur für Tabellen, die keine Transaktionsdaten enthalten.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Synchronisierungs-Tabellen** ein, und wählen Sie dann die zugehörige Verknüpfung aus.
1. Wählen Sie **Neu** aus und wählen Sie dann die hinzuzufügende Tabelle aus.
1. Füllen Sie die Felder nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### <a name="delete-a-table"></a>Tabelle löschen

> [!NOTE]
> Wenn Sie einen Datensatz in der Quellunternehmung löschen, wird er nicht auch in der Tochtergesellschaft gelöscht. Dadurch wird ein unerwünschter Datenverlust verhindert. Die Tochtergesellschaft kann entscheiden, die Tabelle zu löschen, wenn sie dies wünscht.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol, geben Sie **Synchronisierungs-Tabellen** ein, und wählen Sie dann die zugehörige Verknüpfung aus.
1. Wählen Sie die Aktion **Löschen** aus.

## <a name="use-export-and-import-to-share-a-synchronization-setup"></a>Verwenden Sie Export und Import, um ein Synchronisierungseinrichtung gemeinsam zu nutzen

Wenn Sie mehrere Tochtergesellschaften einrichten, die dieselben oder ähnliche Synchronisierungseinstellungen verwenden, können Sie Zeit sparen. Richten Sie eine Tochtergesellschaft ein und exportieren Sie deren Einstellungen dann in eine XML-Datei. Die Datei enthält die gesamte Einrichtung, einschließlich Tabellen- und Feldzuordnungen und Filterkriterien. Anschließend können Sie die Datei in die nächste Tochtergesellschaft importieren. Um eine Einrichtung zu importieren oder zu exportieren, verwenden Sie auf der Seite **Stammdatenverwaltungseinrichtung** die Schaltfläche **Importieren** oder **Export** Aktionen.

## <a name="see-also"></a>Weitere Informationen

[Masterdatensynchronisierung verwalten](admin-sync-master-data.md)
