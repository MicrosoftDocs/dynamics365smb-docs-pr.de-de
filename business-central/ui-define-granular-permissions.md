---
title: Granulare Berechtigungen definieren
description: 'In diesem Artikel wird beschrieben, wie Sie granulare Berechtigungen definieren und jedem Benutzer die Berechtigungssätze zuweisen, die er für seine Aufgaben benötigt.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# <a name="assign-permissions-to-users-and-groups"></a><a name="assign-permissions-to-users-and-groups"></a><a name="assign-permissions-to-users-and-groups"></a>Zuweisen von Berechtigungen zu Benutzern und Gruppen

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Das [!INCLUDE[prod_short](includes/prod_short.md)]-Sicherheitssystem steuert, auf welche Objekte ein Benutzer in jeder Datenbank oder Umgebung in Kombination mit den Lizenzen des Benutzers zugreifen kann. Sie können für jeden Benutzer festlegen, ob er Daten in den Datenbankobjekten lesen, ändern oder eingeben darf. Weitere Informationen finden Sie unter [Datensicherheit](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) in der Hilfe für Entwickler und Verwaltungsinhalt für [!INCLUDE[prod_short](includes/prod_short.md)].

Bevor Sie Benutzern und Benutzergruppen Berechtigungen zuweisen, müssen Sie festlegen, wer sich anmelden kann, indem Sie Benutzer entsprechend ihrer Lizenz erstellen. Weitere Informationen finden Sie unter [Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md).

In [!INCLUDE[prod_short](includes/prod_short.md)] gibt es zwei Ebenen von Berechtigungen für Datenbankobjekte:

- Gesamt-Berechtigungen gemäß der Lizenz, auch als Berechtigung bezeichnet.

  Die Lizenzen enthalten Standardberechtigungssätze. Ab dem 1. Veröffentlichungszyklus 2022 können Administratoren diese Standardberechtigungen für die relevanten Lizenztypen anpassen. Weitere Informationen finden Sie unter [Berechtigungen basierend auf Lizenzen konfigurieren](ui-how-users-permissions.md#licensespermissions).  

- Detaillierte Berechtigungen, die Sie in [!INCLUDE[prod_short](includes/prod_short.md)] zuweisen.

Dieser Artikel beschreibt, wie Sie in [!INCLUDE [prod_short](includes/prod_short.md)] Berechtigungen definieren, verwenden und anwenden können, um die Standardkonfiguration zu ändern.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Weitere Informationen finden Sie unter [Delegierter Administratorzugriff auf Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)]-Online enthält Standardbenutzergruppen, die Benutzern automatisch basierend auf ihrer Lizenz zugewiesen werden. Sie können die Standardkonfiguration ändern, indem Sie Sicherheitsgruppen, Berechtigungssätze und Berechtigungen ändern oder hinzufügen. In der folgenden Tabelle sind wichtige Szenarien zum Ändern der Standardberechtigungen aufgeführt.  

|Aktion  |Siehe  |
|---------|---------|
|Um die Verwaltung von Berechtigungen für mehrere Benutzer zu erleichtern, können Sie diese in Sicherheitsgruppen organisieren und dann ein Berechtigungsset für mehrere Benutzer in einer Aktion zuordnen oder ändern.| [So verwalten Sie Berechtigungen über Benutzergruppen](#to-manage-permissions-through-user-groups) |
|So verwalten Sie Berechtigungssätze für bestimmte Benutzer | [So weisen Sie Benutzern Berechtigungen zu](#to-assign-permission-sets-to-users) |
|Erfahren Sie, wie Sie einen Berechtigungssatz definieren|[Erstellen eines Berechtigungssatzes](#to-create-a-permission-set)|
|So zeigen Sie Berechtigungen eines Benutzers an oder bearbeiten sie|[So erhalten Sie eine Übersicht der Benutzerberechtigungen](#to-get-an-overview-of-a-users-permissions)|
|So erfahren Sie mehr über Sicherheit auf Rekordniveau|[Sicherheitsfilter beschränken den Zugriff eines Benutzers auf bestimmte Datensätze in einer Tabelle](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Eine breitere Methode, um zu definieren, auf welche Funktionen Benutzer Zugriff haben, ist das Setzen des Feldes **Erfahrung** auf der Seite **Unternehmensinformationen**. Weitere Informationen finden Sie unter [Ändern, welche Funktionen angezeigt werden](ui-experiences.md).
>
> Sie können auch Funktionen definieren, die für Benutzer auf der Benutzeroberfläche verfügbar sind und wie sie mit ihnen über Seiten interagieren. Dies geschieht über Profile, die Sie verschiedenen Arten von Benutzern entsprechend ihrer Jobrolle oder Abteilung zuordnen. Weitere Informationen finden Sie unter [Verwalten von Profilen](admin-users-profiles-roles.md) und [[!INCLUDE[prod_short](includes/prod_short.md)] anpassen](ui-customizing-overview.md).

## <a name="to-create-a-permission-set"></a><a name="to-create-a-permission-set"></a><a name="to-create-a-permission-set"></a>Erstellen eines Berechtigungssatzes

> [!NOTE]
> Im Veröffentlichungszyklus 2, 2022 haben wir das Hinzufügen von Berechtigungen zu Berechtigungssätzen vereinfacht. Anstatt Berechtigungen einzeln hinzuzufügen, können Sie ganze Berechtigungssätze hinzufügen. Bei Bedarf können Sie dann einzelne Berechtigungen darin ausschließen. Weitere Informationen finden Sie unter [WeitereBerechtigungssätze hinzufügen](#to-add-other-permission-sets). Um dies zu ermöglichen, haben wir die Seite „Berechtigungssatz“ durch eine neue ersetzt. Die wichtigsten Unterschiede sind die neuen Bereiche **Berechtigungssätze** und **Ergebnisse** und die Infobox **Enthaltene Berechtigungen**. Um die ersetzte Seite „Berechtigungen“ weiterhin zu verwenden, klicken Sie auf der Seite **Berechtigungssätze** auf **Berechtigungen (alt)**.

Die Wartung ist auch einfacher. Wenn Sie eine Systemberechtigungen hinzufügen, wird Ihr benutzerdefinierter Berechtigungssatz automatisch mit allen Änderungen aktualisiert, die Microsoft an diesen Berechtigungen vornimmt.

1. Wählen Sie das Symbol ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Befugnissätze** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Aktion **Neu**.
3. Auf der neuen Zeile füllen Sie die Felder wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die Aktion **Berechtigungen** aus.
5. Auf der Seite **Berechtigungssatz** im Feld **Typ** können Sie Berechtigungen für das Objekt wie folgt einschließen oder ausschließen:

  Um die Berechtigung einzuschließen, wählen Sie **Einschließen** und dann die Zugriffstufe für die Felder **Leseberechtigung**, **Einfügeberechtigung**, **Bearbeitungsberechtigung**, **Löschberechtigung** und **Ausführungsberechtigung**. Die Optionen werden in der folgenden Tabelle beschrieben.

  |Option|Description|Lagerplatzpriorität|
  |------|-----------|-------|
  |**"Leer"**|Der Benutzer kann die Aktion an dem Objekt ausführen.|Am niedrigsten|  
  |**Ja**|Der Benutzer kann die Aktion an dem Objekt ausführen.|Am höchsten|
  |**Indirekt**|Der Benutzer kann die Aktion an dem Objekt nur über ein anderes zugehöriges Objekt ausführen, auf das der Benutzer vollständig zugreifen kann. Weitere Informationen finden Sie unter [Beispiel - Indirekte Berechtigung](#example---indirect-permission) in diesem Artikel und [Berechtigungseigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission) in der Entwickler- und IT-Pro-Hilfe.|Zweithöchste|
  
  Um die Berechtigung oder eine oder mehrere Zugriffsebenen auszuschließen, wählen Sie **Ausschließen** und dann die zu gewährende Zugriffsebene aus. Die Optionen werden in der folgenden Tabelle beschrieben.

  |Option|Description|
  |------|-----------|-------|
  |**"Leer"**|Verwenden Sie die Zugriffsebene basierend auf der Hierarchie der Berechtigungen im Satz.  |
  |**Ausschließen**|Entfernen Sie die spezifische Zugriffsebene für das Objekt.|
  |**Auf indirekt reduzieren**|Ändern Sie die Zugriffsebene in Indirekt, wenn Berechtigungssätze direkten Zugriff auf das Objekt gewähren. Wählen Sie diese Option beispielsweise aus, wenn der Berechtigungssatz direkten Zugriff auf Sachkonteneinträge gewährt, Sie aber nicht möchten, dass Benutzer vollen Zugriff auf die Einträge haben.|
  
  > [!NOTE]
  > Wenn eine Berechtigung sowohl eingeschlossen als auch ausgeschlossen ist, wird die Berechtigung ausgeschlossen.

6. Verwenden Sie die Felder **Objekttyp** und **Objekt-ID**, um das Objekt anzugeben, auf das Sie Zugriff gewähren.

  > [!TIP]
  > Neue Zeilen zeigen Standardwerte an. Zum Beispiel enthält das Feld **Objekttyp** **Tabellendaten**, und das Feld **Objekt-ID** enthält **0**. Die Standardwerte sind nur Platzhalter und werden nicht verwendet. Sie müssen einen Objekttyp und ein Objekt im Feld **Objekt-ID** auswählen, bevor Sie eine weitere neue Zeile erstellen können.

7. Optional: Wenn Sie Berechtigungen für einen Tabellendaten-Objekttyp definieren, können Sie im Feld **Sicherheitsfilter** die Daten filtern, auf die ein Benutzer in Feldern in der ausgewählten Tabelle zugreifen kann. Sie können z. B. angeben, dass ein Benutzer nur auf die Datensätze zugreifen kann, die Informationen über einen bestimmten Debitor enthalten. Weitere Informationen finden Sie unter [Sicherheitsfilter beschränken den Zugriff eines Benutzers auf bestimmte Datensätze in einer Tabelle](#security-filters-limit-a-users-access-to-specific-records-in-a-table) und [Verwenden von Sicherheitsfiltern](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Optional: Fügen Sie im Bereich **Berechtigungssätze** einen oder mehrere andere Berechtigungssätze hinzu. Weitere Informationen finden Sie unter [WeitereBerechtigungssätze hinzufügen](#to-add-other-permission-sets).

> [!IMPORTANT]
> Seien Sie vorsichtig, wenn Sie **Berechtigung einfügen** oder **Berechtigung ändern** auf die Tabelle **9001Benutzergruppenmitglied** oder **9003Benutzergruppenberechtigungssatz** festlegen. Alle Benutzer, die dem Berechtigungssatz zugeordnet sind, könnten sich möglicherweise selbst anderen Benutzergruppen zuordnen, wodurch sie wiederum unbeabsichtigte Berechtigungen erhalten könnten.

### <a name="example---indirect-permission"></a><a name="example---indirect-permission"></a><a name="example---indirect-permission"></a>Beispiel - Indirekte Berechtigungen

Sie können Benutzern indirekte Berechtigungen zuweisen, um ein Objekt nur über ein anderes Objekt zu verwenden. Beispielsweise hat ein Benutzer die Berechtigung, Codeunit 80, Vertrieb-Beitrag, auszuführen. Die Verkaufsbuchung Codeunit führt viele Aufgaben aus, einschließlich der Bearbeitung von Tabelle 37 Verkaufsposition aus. Wenn der Benutzer ein Verkaufsbeleg bucht, überprüft die Codeunit "Vertrieb-Beitrag" [!INCLUDE[prod_short](includes/prod_short.md)], ob der Benutzer über die Berechtigung zum Bearbeiten der Tabelle "Verkaufszeile" verfügt. Wenn nicht, kann die Codeunit ihre Aufgaben nicht ausführen und der Benutzer erhält eine Fehlermeldung. In diesem Fall wird die Codeunit erfolgreich ausgeführt.

Jedoch muss der Anwender keinen vollen Zugriff auf die Tabelle Verkaufszeile haben, um Codeunit auszuführen. Wenn der Benutzer über indirekte Berechtigungen für die Tabelle "Verkaufszeile" verfügt, wird die Codeunit "Verkaufseinheit" erfolgreich ausgeführt. Wenn ein Benutzer über indirekte Berechtigungen verfügt, kann dieser Benutzer die Tabelle Verkaufszeile nur ändern, indem die Verkaufsbuchung Codeunit oder ein anderes Objekt ausgeführt wird, das die Berechtigung zum ändern der Tabelle Verkaufsposition hat. Der Benutzer kann die Tabelle Verkaufsposition nur von unterstützten Anwendungsbereichen aus ändern. Der Benutzer kann die Funktion mit anderen Methoden nicht unbeabsichtigt oder böswillig ausführen.

### <a name="to-add-other-permission-sets"></a><a name="to-add-other-permission-sets"></a><a name="to-add-other-permission-sets"></a>Weitere Berechtigungssätze hinzufügen

Erweitern Sie einen Berechtigungssatz, indem Sie ihm andere Berechtigungssätze hinzufügen. Anschließend können Sie in jedem hinzugefügten Satz bestimmte Berechtigungen oder ganze Berechtigungssätze ein- oder ausschließen. Dies schließt Berechtigungen in den Berechtigungssätzen des Typs „Erweiterung“ und „System“ ein, die andernfalls nicht zulässig sind. Ausschlüsse gelten nur für den Berechtigungssatz, den Sie erweitern. Das ursprügnliche Set wird nicht verändert.

Fügen Sie auf der Seite **Berechtigungssatz** einen Berechtigungssatz im Bereich **Berechtigungssätze** hinzu. Im Bereich **Ergebnis** werden alle hinzugefügten Berechtigungssätze aufgelistet. Um die Berechtigungen zu untersuchen, die in einem von Ihnen hinzugefügten Satz enthalten sind, wählen Sie den Satz im Ergebnisbereich aus und die Infobox **Enthaltene Berechtigungen** zeigt die Berechtigungen an.

Verwenden Sie im Bereich **Ergebnis** das Feld **Inklusionsstatus**, um die Berechtigungssätze zu identifizieren, in denen Sie Berechtigungen oder Berechtigungssätze ausgeschlossen haben. Wenn etwas ausgeschlossen wurde, lautet der Status **Teilweise**.

Wählen Sie für eine Gesamtansicht der Berechtigungen im Berechtigungssatz die Aktion **Alle Berechtigungen anzeigen** aus. Die Seite **Erweiterte Berechtigungen** zeigt alle Berechtigungen, die dem Berechtigungssatz bereits zugewiesen wurden, und die Berechtigungen in den hinzugefügten Berechtigungssätzen.

Um einen Berechtigungssatz vollständig auszuschließen, wählen Sie im Bereich **Ergebnis** die Option **Weitere Optionen anzeigen**, und wählen Sie dann **Ausschließen**. Wenn Sie einen Berechtigungssatz ausschließen, wird eine Zeile im Bereich **Berechtigungssätze** vom Typ Ausgeschlossen erstellt. Wenn Sie einen Berechtigungssatz ausgeschlossen haben, ihn aber wieder einschließen möchten, löschen Sie die Zeile im Feld **Berechtigungssätze**.

Um eine bestimmte Berechtigung in einem von Ihnen hinzugefügten Satz vollständig oder teilweise auszuschließen, erstellen Sie eine Zeile für das Objekt unter **Berechtigungen**. Die Felder für die Zugriffsebene, Berechtigung einfügen, Berechtigung ändern usw. enthalten alle **Ausschließen**. Wählen Sie die entsprechende Option, um eine bestimmte Zugriffsebene zuzulassen.

> [!NOTE]
> Durch das Ausschließen eines Berechtigungssatzes werden alle Berechtigungen im Satz ausgeschlossen. [!INCLUDE [prod_short](includes/prod_short.md)] berechnet Berechtigungen wie folgt:

> 1. Berechnen Sie die vollständige Liste der enthaltenen Berechtigungen
> 2. Berechnen Sie die vollständige Liste der ausgeschlossenen Berechtigungen
> 3. Ausgeschlossene Berechtigungen aus der Liste der enthaltenen Berechtigungen entfernen (das Entfernen einer indirekten Berechtigung entspricht dem Reduzieren auf indirekt)

## <a name="to-copy-a-permission-set"></a><a name="to-copy-a-permission-set"></a><a name="to-copy-a-permission-set"></a>Kopieren eines Berechtigungssatzes

Erstellen Sie einen neuen Berechtigungssatz, indem Sie einen anderen kopieren. Der neue Satz enthält alle Berechtigungen und Berechtigungssätze aus dem kopierten Satz. Wie die Berechtigungen und Berechtigungssätze im neuen Berechtigungssatz angeordnet sind, hängt von Ihrer Auswahl im Feld **Kopiervorgang** ab. Die Optionen werden in der folgenden Tabelle beschrieben.

|Option  |Description  |
|---------|---------|
|**Nach Referenz kopieren**     | Der ursprüngliche Berechtigungssatz und alle ihm hinzugefügten Berechtigungssätze werden in **Ergebnisse** aufgelistet.       |
|**Kopie für flache Berechtigung**  | Alle Berechtigungen aus allen Berechtigungssätzen sind in einer flachen Liste im **Bereich „Berechtigungen“** enthalten. Berechtigungen werden nicht nach Berechtigungssatz organisiert.        |
|**Klonen**     | Erstellen Sie eine exakte Kopie des ursprünglichen Berechtigungssatzes.        |

1. Auf der Seite **Berechtigungssätze** wählen Sie die Zeile für einen Zugriffsrechtsatz, den Sie kopieren möchten, und wählen die **Berechtigungssatz kopieren**-Aktion aus.
2. Auf der Seite **Berechtigungssatz kopieren** geben Sie den Namen des neuen Berechtigungssatzes an.
3. Geben Sie im Feld **Kopiervorgang** an, wie die Berechtigung im neuen Berechtigungssatz angeordnet werden soll.
4. Optional: Wenn Sie einen Systemberechtigungssatz hinzufügen, möchten Sie möglicherweise benachrichtigt werden, wenn sich der Name oder Inhalt des ursprünglichen Berechtigungssatzes in einer zukünftigen Version ändert. Auf diese Weise können Sie überlegen, ob Sie Ihren benutzerdefinierten Berechtigungssatz aktualisieren möchten. Um eine Benachrichtigung zu erhalten, schalten Sie den Schalter **Bei geändertem Berechtigungssatz benachrichtigen** um.

> [!NOTE]
> Die Benachrichtigung setzt voraus, dass die Benachrichtigung **Ursprünglicher Systemberechtigungssatz geändert** auf der Seite **Meine Benachrichtigungen** aktiviert ist.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a><a name="to-create-or-modify-permissions-by-recording-your-actions"></a><a name="to-create-or-modify-permissions-by-recording-your-actions"></a>So erstellen oder ändern Sie Berechtigungen, indem Sie Ihre Aktionen aufzeichnen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Befugnissätze** ein und wählen Sie dann den entsprechenden Link.

    Wählen Sie alternativ auf der Seite **Benutzer** die Aktion **Berechtigungssätze** aus.
2. Wählen Sie auf der Seite **Benutzer** die Aktion **Neu** aus.
3. Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.
4. Wählen Sie die Aktion **Berechtigungen** aus.
5. Auf der Seite **Berechtigungen** wählen Sie die Aktion **Berechtigungen aufzeichnen** aus, und wählen Sie dann die Aktion **Starten** aus.  
    Die Aufzeichnung muss entweder über die Funktion **Diese Seite in einem neuen Fenster öffnen** (Pop-Out) erfolgen, um das Aufzeichnungsfenster **Berechtigungen** nebeneinander zu haben, oder Sie arbeiten innerhalb derselben Registerkarte.  
    Jetzt wird ein Aufzeichnungsprozess gestartet, der alle Ihre Aktionen auf der Benutzeroberfläche erfasst.
6. Wechseln Sie zu den verschiedenen Seiten und Aktivitäten in [!INCLUDE[prod_short](includes/prod_short.md)] für die Benutzer mit diesem Berechtigungssatz, die darauf zugreifen sollen. Sie müssen die Aufgaben ausführen, für die Sie Berechtigungen erfassen möchten.
7. Wenn Sie die Erfassung abschließen möchten, kehren Sie zur Seite **Berechtigungen** zurück, und wählen Sie die **Beenden** Aktion aus.
8. Wählen Sie die Schaltfläche **Ja**, um die erfassten Berechtigungen dem neuen Berechtigungssatz zuzuordnen.
9. Für jedes Objekt in der erfassten Liste geben Sie an, ob Benutzer in der Lage sind, Datensätze in den erfassen Tabellen einzufügen, zu ändern oder zu löschen.

### <a name="to-export-and-import-a-permission-set"></a><a name="to-export-and-import-a-permission-set"></a><a name="to-export-and-import-a-permission-set"></a>So exportieren und importieren Sie einen Berechtigungssatz

Um Berechtigungen schnell einzurichten, können Sie Berechtigungssätze importieren, die Sie aus einem anderen [!INCLUDE[prod_short](includes/prod_short.md)]-Mandanten exportiert haben.

In Umgebungen mit mehreren Mandanten wird ein Berechtigungssatz in einen bestimmten Mandanten importiert. D. h. der Umfang des Imports ist *Mandant*.

1. Wählen Sie auf der Seite **Berechtigungssätze** unter „Mandant 1“ die zu importierende(n) Zeile bzw. Zeilen für die Berechtigungssätze und dann die Aktion **Berechtigungssätze exportieren** aus.

    Eine XML-Datei wird im Download-Ordner auf Ihrem Computer erstellt. Der Name lautet standardmäßig *Export Permission Sets.xml*.

2. Wählen Sie auf der Seite **Berechtigungssätze** unter „Mandant 2“ die Aktion **Berechtigungssätze importieren** aus.
3. Berücksichtigen Sie auf der Seite **Berechtigungssätze importieren**, ob Sie vorhandene Berechtigungssätze mit neuen Berechtigungssätzen in der XML-Datei zusammenführen möchten.

    Wenn Sie das Kontrollkästchen **Vorhandene Berechtigungen aktualisieren** aktivieren, werden vorhandene Berechtigungssätze, deren Namen mit den in der XML-Datei vorhandenen Berechtigungssätzen übereinstimmen, mit den importierten Berechtigungssätzen zusammengeführt.

    Wenn Sie das Kontrollkästchen **Vorhandene Berechtigungen aktualisieren** nicht aktivieren, werden Berechtigungssätze, deren Namen mit den in der XML-Datei vorhandenen Berechtigungssätzen übereinstimmen, während des Imprts übersprungen. In diesem Fall werden Sie über übersprungene Berechtigungssätze informiert.

4. Suchen Sie auf der Dialogfeldseite **Importieren** die zu importierende XML-Datei, und wählen Sie sie aus. Wählen Sie anschließend die Aktion **Öffnen** aus.

Die Berechtigungssätze werden importiert.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a><a name="to-remove-obsolete-permissions-from-all-permission-sets"></a><a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>So entfernen Sie veraltete Berechtigungen aus allen Berechtigungssätzen

Wählen Sie auf der Seite **Berechtigungssätze** die Aktion **Veraltete Berechtigungssätze entfernen** aus.

## <a name="to-set-up-time-constraints-for-users"></a><a name="to-set-up-time-constraints-for-users"></a><a name="to-set-up-time-constraints-for-users"></a>So richten Sie Zeiteinschränkungen für Benutzer ein

Administratoren können Zeiträume definieren, in denen bestimmte Benutzer Beiträge veröffentlichen können. Administratoren können auch angeben, ob das System protokolliert, wie lange Benutzer angemeldet sind. Entsprechend können Administratoren Benutzern Zuständigkeitseinheiten zuordnen. Weitere Informationen finden Sie unter [Arbeiten mit Zuständigkeitseinheiten](inventory-responsibility-centers.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol. Geben Sie **Benutzereinrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie auf der Seite **Benutzereinrichtung** die Aktion **Neu** aus.
3. In dem Feld **Benutzer-ID** geben Sie die ID eines Benutzers ein, oder wählen Sie das Feld aus, um alle Nutzer der aktiven Fenster im System anzuzeigen.
4. Füllen Sie die Felder nach Bedarf aus.

## <a name="to-manage-permissions-through-user-groups"></a><a name="to-manage-permissions-through-user-groups"></a><a name="to-manage-permissions-through-user-groups"></a>So verwalten Sie Berechtigungen über Benutzergruppen

Benutzergruppen helfen Ihnen bei der Verwaltung von Berechtigungssätzen im gesamten Unternehmen. [!INCLUDE [prod_short](includes/prod_short.md)]-Online enthält Standardbenutzergruppen, die Benutzern automatisch basierend auf ihrer Lizenz zugewiesen werden. Sie können Benutzer manuell zu einer Benutzergruppe hinzufügen und neue Benutzergruppen als Kopien vorhandener Gruppen erstellen.  

Sie beginnen mit der Erstellung einer Benutzergruppe. Anschließend ordnen Sie der Gruppe Berechtigungen zu, um festzulegen, auf welche Objekte die Benutzer der Gruppe zugreifen können. Wenn Sie einen Benutzer zur Gruppe hinzufügen, gelten die für die Gruppe definierten Berechtigungssätze für den Benutzer.

Berechtigungssätze, die einem Benutzer über eine Benutzergruppe zugewiesen wurden, bleiben synchronisiert. Eine Änderung der Benutzergruppenberechtigungen wird automatisch an die Benutzer weitergegeben. Wenn Sie einen Benutzer aus einer Benutzergruppe entfernen, werden die entsprechenden Berechtigungen automatisch entzogen.

### <a name="to-add-users-to-a-user-group"></a><a name="to-add-users-to-a-user-group"></a><a name="to-add-users-to-a-user-group"></a>So fügen Sie einer Benutzergruppe Benutzer hinzu

Die folgende Vorgehensweise erläutert, wie Sie Benutzergruppen manuell anlegen. Informationen zum automatischen Erstellen von Benutzergruppen finden Sie unter [Eine Benutzergruppe und alle ihre Berechtigungen kopieren](#to-copy-a-user-group-and-all-its-permission-sets).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Benutzergruppen** ein und wählen Sie dann den zugehörigen Link.

    1. Wählen Sie alternativ auf der Seite **Benutzer** die Aktion **Benutzergruppen** aus.
2. Wählen Sie auf der Seite **Benutzergruppen** die Aktion **Benutzergruppenmitglieder** aus.
3. Wählen Sie auf der Seite **Benutzergruppenmitglieder** die Aktion **Benutzer hinzufügen** aus.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a><a name="to-copy-a-user-group-and-all-its-permission-sets"></a><a name="to-copy-a-user-group-and-all-its-permission-sets"></a>So kopieren Sie eine Benutzergruppe und all seine Zugriffsrechtsätze

Zur schnellen Definition einer neuen Benutzergruppe können Sie eine Funktion verwenden, um alle Berechtigungssätze einer vorhandenen Benutzergruppe zur neuen Benutzergruppe zu kopieren.

> [!NOTE]
> Die Mitglieder der Benutzergruppe werden nicht in die neue Benutzergruppe kopiert. Sie müssen sie hinterher manuell hinzufügen. Weitere Informationen finden Sie im Abschnitt [So fügen Sie Benutzer einer Benutzergruppe hinzu](#to-add-users-to-a-user-group).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Benutzergruppen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Benutzergruppe aus, die Sie kopieren möchten, und wählen Sie **Benutzergruppe kopieren** aus.
3. Im Feld **Neuer Benutzergruppencode** geben Sie einen Namen für die Gruppe an. Wählen Sie dann die Schaltfläche **OK** aus.

Die neue Benutzergruppe wird die Seite **Benutzergruppen** hinzugefügt. Fahren Sie fort, um Benutzer hinzuzufügen. Weitere Informationen finden Sie im Abschnitt [So fügen Sie Benutzer einer Benutzergruppe hinzu](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Sie erhalten einen Validierungsfehler, wenn Sie versuchen, dem Benutzer eine Benutzergruppe zuzuweisen, die sich auf einen Berechtigungssatz bezieht, der in einer nicht installierten Erweiterung definiert wurde. Dies liegt daran, dass die App-ID der Erweiterung überprüft wird, wenn darauf verwiesen wird. Um diese Benutzergruppe einem Benutzer zuzuweisen, können Sie entweder die Erweiterung neu installieren, die Referenz der deinstallierten Erweiterung aus dem Berechtigungssatz entfernen oder diesen Berechtigungssatz aus der Benutzergruppe entfernen.

### <a name="to-assign-permission-sets-to-user-groups"></a><a name="to-assign-permission-sets-to-user-groups"></a><a name="to-assign-permission-sets-to-user-groups"></a>So weisen Sie Berechtigungssätze Benutzergruppen zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Benutzergruppen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Benutzergruppe aus, der Sie die Berechtigung zuweisen möchten.  

    Zugriffsrechtsätze, die dem Benutzer bereits zugewiesen sind, werden im Bereich **Benutzerzugriffsrechtsätze** angezeigt.
3. Wählen Sie die Aktion **Benutzerrechtesätze**, um die Seite **Benutzerrechtesätze** zu öffnen.
4. Füllen Sie auf der Seite **Benutzerberechtigungen** in einer neuen Zeile die Felder nach Bedarf aus.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a><a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a><a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>So weisen Sie ein Berechtigungsset auf der Seite **Berechtigung festgelegt nach Benutzergruppe** zu

Die folgende Vorgehensweise erläutert, wie Sie Berechtigungssätze einer Benutzergruppe auf der Seite **Berechtigungen nach Benutzergruppe** zuordnen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Benutzer** den entsprechenden Benutzer aus und wählen Sie dann die Aktion **Berechtigung festgelegt durch Benutzergruppe**.
3. Aktivieren Sie auf der Seite **Berechtigung festgelegt durch Benutzergruppe** das Feld **[Name der Benutzergruppe]** in einer Zeile für die entsprechende Berechtigung, um die Gruppe der Benutzergruppe zuzuordnen.
4. Aktivieren Sie das Kontrollkästchen **Alle Benutzergruppen**, um die Berechtigung allen Benutzergruppen zuzuordnen.

Sie können einem Benutzer Berechtigungsgruppen zudem direkt zuweisen.

## <a name="to-assign-permission-sets-to-users"></a><a name="to-assign-permission-sets-to-users"></a><a name="to-assign-permission-sets-to-users"></a>So weisen Sie Benutzern Berechtigungen zu

Ein Berechtigungssatz ist eine Sammlung von Berechtigungen für bestimmte Datenbankobjekte. Allen Benutzern muss mindestens ein Berechtigungssatz zugeordnet werden, bevor sie auf [!INCLUDE[prod_short](includes/prod_short.md)] zugreifen können.  

Eine [!INCLUDE[prod_short](includes/prod_short.md)]-Lösung enthält vordefinierte Berechtigungen, die von Microsoft oder Ihrem Lösungsanbieter hinzugefügt werden. Sie können auch neue Berechtigungen hinzufügen, die auf die Bedürfnisse Ihres Unternehmens zugeschnitten sind. Weitere Informationen finden Sie im Abschnitt [So erstellen Sie Berechtigungssätze](#to-create-a-permission-set).

> [!NOTE]
> Wenn Sie den Zugriff eines Benutzers nicht mehr einschränken möchten, als in der Lizenz bereits definiert ist, können Sie dem Benutzer eine spezielle Berechtigung namens SUPER zuweisen. Diese Berechtigung stellt sicher, dass der Benutzer auf alle in der Lizenz angegebenen Objekte zugreifen kann.
>
> Ein Benutzer mit der Essential-Lizenz und dem SUPER-Berechtigungssatz hat Zugriff auf mehr Funktionen als Benutzer mit der Team Member-Lizenz und dem SUPER-Berechtigungssatz.

Sie können den Benutzern Berechtigungsgruppen auf zwei Arten zuweisen:

- Auf der Seite **Benutzerkarte** durch Auswahl von Berechtigungssätzen, die dem Benutzer zugewiesen werden sollen.
- Auf der Seite **Berechtigung vom Benutzer festgelegt** durch Auswählen von Benutzern, denen ein Berechtigungssatz zugeordnet ist.

### <a name="to-assign-a-permission-set-on-a-user-card"></a><a name="to-assign-a-permission-set-on-a-user-card"></a><a name="to-assign-a-permission-set-on-a-user-card"></a>Zuweisen eines Berechtigungssatzes in einer Benutzerkarte

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Benutzer aus, den Sie dem Debitor zuordnen möchten.
Zugriffsrechtsätze, die dem Benutzer bereits zugewiesen sind, werden im Bereich **Benutzerzugriffsrechtsätze** angezeigt.
3. Wählen Sie auf der Seite **Benutzerkarte** die Aktion **Bearbeiten** aus.
4. Füllen Sie im Inforegister **Benutzer-Berechtigungssatz** die Felder nach Bedarf aus. Weitere Informationen finden Sie unter [Erstellen und Bearbeiten von Berechtigungssätzen](ui-define-granular-permissions.md#to-create-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a><a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a><a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Zuweisen eines Berechtigungssatzes auf der Seite Benutzerberechtigungssatz nach Benutzer

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Benutzer** die Aktion **Berechtigungssatz nach Benutzer** aus.
3. Auf der Seite **Benutzerberechtigungssatz nach Benutzer** wählen Sie das Kontrollkästchen **[Benutzername]** in einer Zeile für den relevanten Berechtigungssatz aus, um den Satz einem Benutzer zuzuweisen.

    Wählen Sie das Kontrollkästchen **Alle Benutzer** aus, um dem Berechtigungssatz allen Anwender zuzuweisen.

## <a name="to-get-an-overview-of-a-users-permissions"></a><a name="to-get-an-overview-of-a-users-permissions"></a><a name="to-get-an-overview-of-a-users-permissions"></a>So erhalten Sie eine Übersicht der Benutzerberechtigungen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Was möchten Sie tun?") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die karte des relevanten Benutzers.
3. Wählen Sie die Aktion **Effektive Berechtigungen** aus.

    Der Teil **Berechtigungen** führt alle Datenbankobjekte auf, auf die der Benutzer Zugriff hat. Sie können diesen Abschnitt nicht bearbeiten.

    Der Teil **Nach Berechtigungssatz** zeigt die zugewiesenen Berechtigungssätze, über die dem Benutzer die Berechtigungen gewährt werden, die Quelle und den Typ des Berechtigungssatzes und in welchem Umfang die verschiedenen Zugriffsarten erlaubt sind.

    Für jede Zeile, die Sie im Abschnitt **Berechtigungen** auswählen, zeigt der Abschnitt **Nach Berechtigungssatz**, über welchen Berechtigungssatz oder welche Berechtigungssätze die Berechtigung gewährt wird. In diesem Abschnitt können Sie den Wert in jedem der fünf Zugriffstypfelder **Leseberechtigung**, **Einfügeberechtigung**, **Bearbeitungsberechtigung**, **Löschberechtigung** und **Ausführungsberechtigung** ändern.

    > [!NOTE]  
    > Nur Berechtigungssätze vom Typ **Benutzerdefiniert** können bearbeitet werden.
    >
    > Die Zeilen des Quellanspruchs stammen aus der Abonnementlizenz. Die Berechtigungswerte des Anspruchs setzen Werte in anderen Berechtigungssätzen außer Kraft, wenn Ihre Priorität höher ist. Ein Wert in einem Berechtigungssatz ohne Anspruch mit einer höheren Priorität als der zugehörige Wert im Anspruch, wird in Klammern gesetzt, um anzugeben, dass er nicht wirksam ist, da er durch den Anspruch außer Kraft gesetzt wurde.
    >
    > Eine Erklärung der Priorität finden Sie unter [So erstellen Sie Berechtigungssätze](ui-define-granular-permissions.md#to-create-a-permission-set).  

4. Wenn Sie einen Berechtigungssatz bearbeiten möchten, wählen Sie im Teil **Nach Berechtigungssatz** in der Zeile für einen entsprechenden Berechtigungssatz vom Typ **Benutzerdefiniert** eins der fünf Zugriffstypfelder und einen anderen Wert aus.

5. Um einzelne Berechtigungen innerhalb des Berechtigungssatzes zu bearbeiten, wählen Sie den Wert im Feld **Berechtigungssatz** aus, um die Seite **Berechtigungen** zu öffnen.

> [!NOTE]  
> Wenn Sie einen Berechtigungssatz bearbeiten, gelten die Änderungen auch für andere Benutzer, denen der Berechtigungssatz zugewiesen wurde.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a><a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a><a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Sicherheitsfilter beschränken den Zugriff eines Benutzers auf bestimmte Datensätze in einer Tabelle

Verwenden Sie für Sicherheit auf Datensatzebene in [!INCLUDE[prod_short](includes/prod_short.md)] Sicherheitsfilter, um den Benutzerzugriff auf Daten in einer Tabelle einzuschränken. Sie erstellen Sicherheitsfilter für Tabellendaten. Ein Sicherheitsfilter beschreibt einen Satz Datensätze in einer Tabelle, worauf ein Benutzer zugreifen darf. Sie können z. B. angeben, dass ein Benutzer nur die Daten lesen kann, die Informationen über einen bestimmten Debitor enthalten. Auf diese Weise kann der Benutzer nicht auf die Daten zugreifen, die Informationen zu anderen Debitoren enthalten. Weitere Informationen finden Sie unter [Verwenden von Sicherheitsfiltern](/dynamics365/business-central/dev-itpro/security/security-filters) im Verwaltungsinhalt.

## <a name="viewing-permission-changes-telemetry"></a><a name="viewing-permission-changes-telemetry"></a><a name="viewing-permission-changes-telemetry"></a>Durch das Anzeigen der Berechtigung wird die Telemetrie geändert

Sie können [!INCLUDE[prod_short](includes/prod_short.md)] einrichten, um Änderungen, die an der Berechtigung vorgenommen wurden, an eine Application Insights Ressource in Microsoft Azure zu senden. Anschließend erstellen Sie mit Azure Monitor Berichte und richten Warnungen für die erfassten Daten ein. Weitere Informationen finden Sie in den folgenden Artikeln in der [!INCLUDE[prod_short](includes/prod_short.md)]-Hilfe für Entwickler und die Verwaltung:

- [Überwachung und Analyse der Telemetrie – Aktivieren Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Ananlysieren der Feldüberwachungstelemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="delegated-admin-users"></a><a name="delegated-admin-users"></a><a name="delegated-admin-users"></a>Delegierte Administratorbenutzer

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Siehe auch

[Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md)  
[Profile verwalten](admin-users-profiles-roles.md)  
[Funktionen, die angezeigt werden ändern](ui-experiences.md)  
[Anpassen von [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Verwaltung](admin-setup-and-administration.md)  
[Benutzer zu Microsoft 365 für Unternehmen hinzufügen](/microsoft-365/admin/add-users/add-users)  
[Sicherheit und Schutz in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) in der Hilfe für Entwickler und IT-Profis  
[Benutzern eine Telemetriekennung zuweisen](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
