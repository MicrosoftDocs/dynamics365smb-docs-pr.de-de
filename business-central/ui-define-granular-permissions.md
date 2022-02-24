---
title: Granulare Berechtigungen definieren | Microsoft Docs
description: Beschreibt, wie Sie Benutzern Zugriff auf Objekte gewähren, indem Sie ihnen Berechtigungen zuweisen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 04/22/2020
ms.author: sgroespe
ms.openlocfilehash: d6fe5cff52d3ed8c2404e12b3e37703c8e8db8bb
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324030"
---
# <a name="assign-permissions-to-users-and-groups"></a>Zuweisen von Berechtigungen zu Benutzern und Gruppen
Mit dem Sicherheitssystem [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie steuern, auf welche Objekte ein Benutzer innerhalb jeder Datenbank oder Umgebung zugreifen darf. Sie können für jeden Benutzer festlegen, ob er Daten in den ausgewählten Datenbankobjekten lesen, ändern oder eingeben darf. Detaillierte Informationen finden Sie unter [Datensicherheit](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) in der Hilfe für Entwickler und ITPro für [!INCLUDE[d365fin](includes/d365fin_md.md)].

Bevor Sie Benutzern und Benutzergruppen Berechtigungen zuweisen, müssen Sie festlegen, wer sich anmelden kann, indem Sie Benutzer gemäß der Lizenz erstellen, wie im Microsoft 365 Admin Center definiert. Weitere Informationen finden Sie unter [Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md).

In [!INCLUDE[d365fin](includes/d365fin_md.md)] gibt es zwei Ebenen von Berechtigungen für Datenbankobjekte:
- Gesamt-Berechtigungen gemäß der Lizenz, auch als Berechtigung bezeichnet.
- Detailliertere Berechtigungen, wie sie innerhalb von [!INCLUDE[d365fin](includes/d365fin_md.md)] vergeben werden.

Um die Verwaltung von Berechtigungen für mehrere Benutzer zu erleichtern, können Sie diese in Benutzergruppen organisieren und so ein Berechtigungsset für mehrere Benutzer in einer Aktion zuordnen oder ändern. Weitere Informationen finden Sie unter [Berechtigungen über Benutzergruppen verwalten](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Eine weitere Methode, um zu definieren, auf welche Funktionen ein Benutzer Zugriff hat, ist das Setzen des Feldes **Erfahrung** auf der Seite **Unternehmensinformationen**. Weitere Informationen finden Sie unter [Ändern Sie, welche Funktionen angezeigt werden](ui-experiences.md).
>
> Sie können auch definieren, was Benutzer auf der Benutzeroberfläche sehen und wie sie mit ihrer zulässigen Funktionalität über Seiten interagieren. Dies geschieht über Profile, die Sie verschiedenen Arten von Benutzern entsprechend ihrer Jobrolle oder Abteilung zuordnen. Weitere Informationen finden Sie unter [Verwalten von Profilen](admin-users-profiles-roles.md) und [[!INCLUDE[d365fin](includes/d365fin_md.md)] anpassen](ui-customizing-overview.md).

## <a name="to-assign-permission-sets-to-users"></a>So weisen Sie Benutzern Berechtigungen zu
Ein Berechtigungssatz ist eine Sammlung von Berechtigungen für bestimmte Datenbankobjekte. Allen Benutzern muss mindestens ein Berechtigungssatz zugeordnet werden, bevor sie auf [!INCLUDE[d365fin](includes/d365fin_md.md)] zugreifen können.

Eine [!INCLUDE[d365fin](includes/d365fin_md.md)]-Lösung enthält eine Reihe von vordefinierten Berechtigungen, die von Microsoft oder Ihrem Lösungsanbieter hinzugefügt werden. Sie können auch neue Berechtigungen hinzufügen, die auf die Bedürfnisse Ihres Unternehmens zugeschnitten sind. Weitere Informationen finden Sie unter [Erstellen und Bearbeiten von Berechtigungssätzen](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

> [!NOTE]
> Wenn Sie den Zugriff eines Benutzers nicht mehr einschränken möchten, als in der Lizenz bereits definiert ist, können Sie dem Benutzer eine spezielle Berechtigung namens SUPER zuweisen. Diese Berechtigung stellt sicher, dass der Benutzer auf alle in der Lizenz angegebenen Objekte zugreifen kann.<br /><br />
> Ein Benutzer mit der Essential-Lizenz und dem SUPER-Berechtigungssatz hat Zugriff auf mehr Funktionen als Benutzer mit der Team Member-Lizenz und dem SUPER-Berechtigungssatz.

Sie können den Benutzern Berechtigungsgruppen auf zwei Arten zuweisen:
- Auf der Seite **Benutzerkarte** durch Auswahl von Berechtigungssätzen, die dem Benutzer zugewiesen werden sollen.
- Auf der Seite **Berechtigung vom Benutzer festgelegt** durch Auswählen von Benutzern, denen ein Berechtigungssatz zugeordnet ist.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Zuweisen eines Berechtigungssatzes in einer Benutzerkarte
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie den Benutzer aus, den Sie dem Debitor zuordnen möchten.
Zugriffsrechtsätze, die dem Benutzer bereits zugewiesen sind, werden im Bereich **Benutzerzugriffsrechtsätze** angezeigt.
3. Wählen Sie auf der Seite **Benutzerkarte** die Aktion **Bearbeiten** aus.
4. Füllen Sie im Inforegister **Benutzer-Berechtigungssatz** die Felder nach Bedarf aus. Weitere Informationen finden Sie unter [Erstellen und Bearbeiten von Berechtigungssätzen](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Zuweisen eines Berechtigungssatzes auf der Seite **Benutzerberechtigungssatz nach Benutzer**  
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Benutzer** den gewünschten Benutzer aus, und wählen Sie die Aktion **Benutzerberechtigungssatz nach Benutzer** aus.
3. Auf der Seite **Benutzerberechtigungssatz nach Benutzer** wählen Sie das Kontrollkästchen **[Benutzername]** in einer Zeile für den relevanten Berechtigungssatz aus, um den Satz einem Benutzer zuzuweisen.
4. Wählen Sie das Kontrollkästchen **Alle Benutzer** aus, um dem Berechtigungssatz allen Anwender zuzuweisen.

## <a name="to-get-an-overview-of-a-users-permissions"></a>So erhalten Sie eine Übersicht der Benutzerberechtigungen
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie die karte des relevanten Benutzers.
3. Wählen Sie die Aktion **Effektive Berechtigungen** aus.

    Der Teil **Berechtigungen** führt alle Datenbankobjekte auf, auf die der Benutzer Zugriff hat. Sie können diesen Abschnitt nicht bearbeiten.

    Der Teil **Nach Berechtigungssatz** zeigt die zugewiesenen Zugriffsrechtsätze, über die dem Benutzer die Berechtigungen gewährt werden, die Herkunft und die Art des Berechtigungssatzes und wie weit die verschiedenen Berechtigungssätze zulässig sind.

    Für jede Zeile, die Sie im Abschnitt **Berechtigungen** auswählen, zeigt der Abschnitt **Nach Berechtigungssatz**, über welchen Berechtigungssatz oder welche Berechtigungssätze die Berechtigung gewährt wird. In diesem Abschnitt können Sie den Wert in jedem der fünf Zugriffstypfelder **Leseberechtigung**, **Einfügeberechtigung**, **Bearbeitungsberechtigung**, **Löschberechtigung** und **Ausführungsberechtigung** ändern.

    > [!NOTE]  
    > Nur Berechtigungssätze vom Typ **Benutzerdefiniert** können bearbeitet werden.<br /><br />
    > Die Zeilen des Quellanspruchs stammen aus der Abonnementlizenz. Die Berechtigungswerte des Anspruchs setzen Werte in anderen Berechtigungssätzen außer Kraft, wenn Ihre Priorität höher ist. Ein Wert in einem Berechtigungssatz ohne Anspruch mit einer höheren Priorität als der zugehörige Wert im Anspruch, wird in Klammern gesetzt, um anzugeben, dass er nicht wirksam ist, da er durch den Anspruch außer Kraft gesetzt wurde.<br /><br />
    > Eine Erklärung der Priorität finden Sie unter [So erstellen oder bearbeiten Sie Berechtigungen manuell](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Wenn Sie einen Berechtigungssatz bearbeiten möchten, wählen Sie im Teil **Nach Berechtigungssatz** in der Zeile für einen entsprechenden Berechtigungssatz vom Typ **Benutzerdefiniert** eins der fünf Zugriffstypfelder und einen anderen Wert aus.

5. Um einzelne Berechtigungen innerhalb des Berechtigungssatzes zu bearbeiten, wählen Sie den Wert im Feld **Berechtigungssatz** aus, um die Seite **Berechtigungen** zu öffnen. Befolgen Sie die Schritte, die unter [So erstellen oder bearbeiten Sie Berechtigungen](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually) beschrieben werden.  

> [!NOTE]  
> Wenn Sie einen Berechtigungssatz bearbeiten, gelten die Änderungen auch für andere Benutzer, denen der Berechtigungssatz zugewiesen wurde.

## <a name="to-create-or-modify-a-permission-set"></a>Um ein Berechtigungssatz zu erstellen oder zu ändern
Berechtigungssatz funktionieren als Container von Berechtigungen, sodass Sie mehrere Berechtigungen einfach in einem Datensatz verwalten können.

> [!NOTE]  
> Eine [!INCLUDE[d365fin](includes/d365fin_md.md)]-Lösung enthält normalerweise mehrere vordefinierte Berechtigungssätze, die von Microsoft oder von Ihrem Software-Anbieter hinzugefügt werden. Diese Berechtigungssätze sind vom Typ **System** oder **Erweiterung**. Sie können diese Art der Berechtigungssätze oder die Berechtigungen darin nicht erstellen oder bearbeiten. Jedoch können Sie sie kopieren, um eigene Berechtigungssätze und Berechtigungen zu definieren. <br /><br />
Berechtigungssätze, die Benutzer neu oder als Kopien erstellen, sind vom Typ **Benutzerdefiniert** und können bearbeitet werden.

### <a name="to-create-new-permission-set-from-scratch"></a>So erstellen Sie neue Berechtigungen von Grund auf neu
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Berechtigungssätze** ein und wählen Sie dann den entsprechenden Link.
2. Wenn Sie einen neuen Berechtigungssatz erstellen, wählen Sie die Aktion **Neu** aus.
3. Auf der neuen Zeile füllen Sie die Felder wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Wenn Sie ein Berechtigungssat erstellt haben, müssen Sie die tatsächlichen Berechtigungen hinzufügen. Weitere Informationen finden Sie unter [Berechtigungen manuell erstellen oder ändern](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Kopieren eines Berechtigungssatzes
Sie können auch eine Kopierfunktion verwenden, um schnell alle Berechtigungen eines anderen Berechtigungssatzes auf einen neuen Berechtigungssatz zu übertragen.

> [!NOTE]  
> Wenn ein Systemberechtigungssatz, den Sie kopiert haben, geändert wird, werden Sie (abhängig von Ihrer Auswahl) benachrichtigt, sodass Sie entscheiden können, ob die Änderungen in Ihren benutzerdefinierten Berechtigungssatz kopiert oder geschrieben werden müssen.

1. Auf der Seite **Berechtigungssätze** wählen Sie die Zeile für einen Zugriffsrechtsatz, den Sie kopieren möchten, und wählen die **Berechtigungssatz kopieren**-Aktion aus.
2. Auf der Seite **Berechtigungssatz kopieren** geben Sie den Namen des neuen Berechtigungssatzes an, und wählen Sie dann die Schaltfläche **OK** aus.
3. Wählen Sie das Kontrollkästchen **Bei geändertem Berechtigungssatz benachrichtigen** aus, wenn Sie eine Verknüpfung zwischen den ursprünglichen und dem kopierten Berechtigungssätzen beibehalten möchten. Der Link wird verwendet, um Sie zu benachrichtigen, wenn der Name oder der Inhalt des ursprünglichen Berechtigungssatzes in einer zukünftigen Version geändert wird, auf die die Lösung später aktualisiert wird.

Der neue Berechtigungssatz mit allen Berechtigungen des kopierten Berechtigungssatzes wird als neue Zeile auf der Seite **Berechtigungssätze** hinzugefügt. Jetzt können Sie die Berechtigung im neuen Berechtigungssatz ändern. Beachten Sie, dass die Zeilen innerhalb jedes Typs alphabetisch geordnet sind.

### <a name="to-export-and-import-a-permission-set"></a>So exportieren und importieren Sie einen Berechtigungssatz
Um Berechtigungen schnell einzurichten, können Sie Berechtigungssätze importieren, die Sie aus einem anderen [!INCLUDE[d365fin](includes/d365fin_md.md)]Mandanten exportiert haben.

In Umgebungen mit mehreren Mandanten wird ein Berechtigungssatz in einen bestimmten Mandanten importiert, d. h. der Umfang des Imports ist „Mandant“.

1. Wählen Sie auf der Seite **Berechtigungssätze** unter „Mandant 1“ die zu importierende(n) Zeile bzw. Zeilen für die Berechtigungssätze und dann die Aktion **Berechtigungssätze exportieren** aus.

    Eine XML-Datei wird im Download-Ordner auf Ihrem Computer erstellt. Diese hat standardmäßig den Namen „Export Permission Sets.xml“.

2. Wählen Sie auf der Seite **Berechtigungssätze** unter „Mandant 2“ die Aktion **Berechtigungssätze importieren** aus.
3. Berücksichtigen Sie auf der Seite **Berechtigungssätze importieren**, ob Sie vorhandene Berechtigungssätze mit neuen Berechtigungssätzen in der XML-Datei zusammenführen möchten.

    Wenn Sie das Kontrollkästchen **Vorhandene Berechtigungen aktualisieren** aktivieren, werden vorhandene Berechtigungssätze, deren Namen mit den in der XML-Datei vorhandenen Berechtigungssätzen identisch sind, mit den importierten Berechtigungssätzen zusammengeführt.

    Wenn Sie das Kontrollkästchen **Vorhandene Berechtigungen aktualisieren** nicht aktivieren, werden Berechtigungssätze, deren Namen mit den in der XML-Datei vorhandenen Berechtigungssätzen identisch sind, während des Imprts übersprungen. In diesem Fall werden Sie über übersprungene Berechtigungssätze informiert.

4. Suchen Sie auf der Dialogfeldseite **Importieren** die zu importierende XML-Datei, und wählen Sie sie aus. Wählen Sie anschließend die Aktion **Öffnen** aus.

Die Berechtigungssätze werden importiert.

## <a name="to-create-or-modify-permissions-manually"></a>Um Berechtigungen manuell zu erstellen oder zu ändern
In diesem Verfahren wird beschrieben, wie manuell Berechtigungen addiert oder bearbeitet werden. Sie können auch automatisch Berechtigungen aus Ihren Aktionen in der Benutzeroberfläche generieren lassen. Weitere Informationen finden Sie unter [Erstellen oder Ändern von Berechtigungen durch Aufzeichnen Ihrer Aktionen](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Wenn Sie eine Berechtigung und dadurch den zugehörigen Berechtigungssatz bearbeiten, gelten die Änderungen auch für andere Benutzer, denen der Berechtigungssatz zugewiesen wurde.

1. Auf der Seite **Berechtigungssätze** wählen Sie die Zeile für einen Zugriffsrechtsatz, und wählen die **Berechtigungen**-Aktion aus.
2. Auf der Seite **Berechtigungen** erstellen Sie eine neue Zeile oder bearbeiten Sie die Felder einer vorhandenen Zeile.

In jedem der fünf Zugriffstypfelder **Leseberechtigung**, **Einfügeberechtigung**, **Bearbeitungsberechtigung**, **Löschberechtigung** und **Ausführungsberechtigung** können Sie eine der folgenden drei Berechtigungsoptionen auswählen:

|Option|Description|Priorität|
|------|-----------|
|**Ja**|Der Benutzer kann die Aktion an dem fraglichen Objekt ausführen.|Am höchsten|
|**Indirekt**|Der Benutzer kann die Aktion an dem fraglichen Objekt nur über ein anderes zugehöriges Objekt ausführen, auf das der Benutzer vollständig zugreifen kann. Weitere Informationen zu indirekten Berechtigungen finden Sie unter [Berechtigungseigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) in der Entwickler- und IT-Pro-Hilfe|Zweithöchste|
|**"Leer"**|Der Benutzer kann die Aktion an dem fraglichen Objekt nicht ausführen.|Am niedrigsten|

### <a name="example---indirect-permission"></a>Beispiel - Indirekte Berechtigungen
Sie können indirekte Berechtigungen zuweisen, um ein Objekt nur über ein anderes Objekt zu verwenden.
Beispielsweise kann ein Benutzer die Berechtigung haben, Codeunit 80, Vertrieb-Beitrag, auszuführen. Die Verkaufsbuchung Codeunit führt viele Aufgaben aus, einschließlich der Bearbeitung von Tabelle 37 Verkaufsposition aus. Wenn der Benutzer ein Verkaufsbeleg bucht, überprüft die Codeunit "Vertrieb-Beitrag" [!INCLUDE[d365fin](includes/d365fin_md.md)], ob der Benutzer über die Berechtigung zum Bearbeiten der Tabelle "Verkaufszeile" verfügt. Wenn nicht, kann die Codeunit ihre Aufgaben nicht ausführen und der Benutzer erhält eine Fehlermeldung. In diesem Fall wird die Codeunit erfolgreich ausgeführt.

Jedoch muss der Anwender keinen vollen Zugriff auf die Tabelle Verkaufszeile haben, um Codeunit auszuführen. Wenn der Benutzer über indirekte Berechtigungen für die Tabelle "Verkaufszeile" verfügt, wird die Codeunit "Verkaufseinheit" erfolgreich ausgeführt. Wenn ein Benutzer über indirekte Berechtigungen verfügt, kann dieser Benutzer die Tabelle Verkaufszeile nur ändern, indem die Verkaufsbuchung Codeunit oder ein anderes Objekt ausgeführt wird, das die Berechtigung zum ändern der Tabelle Verkaufsposition hat. Der Benutzer kann die Tabelle Verkaufsposition nur von unterstützten Anwendungsbereichen aus ändern. Der Benutzer kann die Funktion mit anderen Methoden nicht unbeabsichtigt oder böswillig ausführen.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>So erstellen oder ändern Sie Berechtigungen, indem Sie Ihre Aktionen aufzeichnen
1.    Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Berechtigungssätze** ein und wählen Sie dann den entsprechenden Link.
2.    Wählen Sie alternativ auf der Seite **Benutzer** die Aktion **Berechtigungssätze** aus.
3.    Wählen Sie auf der Seite **Benutzer** die Aktion **Neu** aus.
4.    Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.
5.    Wählen Sie die Aktion **Berechtigungen** aus.
6.    Auf der Seite **Berechtigungen** wählen Sie die Aktion **Berechtigungen aufzeichnen** aus, und wählen Sie dann die Aktion **Starten** aus.

    Damit wird ein Aufnahmeprozesses gestartet, der alle Ihre Aktionen in der Benutzeroberfläche erfasst.
7.    Wechseln Sie zu den verschiedenen Seiten und Aktivitäten in [!INCLUDE[d365fin](includes/d365fin_md.md)] für die Benutzer mit diesem Berechtigungssatz, die darauf zugreifen sollen. Sie müssen die Aufgaben ausführen, für die Sie Berechtigungen erfassen möchten.
8.    Wenn Sie die Erfassung abschließen möchten, kehren Sie zur Seite **Berechtigungen** zurück, und wählen Sie die **Beenden** Aktion aus.
9.    Wählen Sie die Schaltfläche **Ja**, um die erfassten Berechtigungen dem neuen Berechtigungssatz zuzuordnen.
10.    Für jedes Objekt in der erfassten Liste geben Sie an, ob Benutzer in der Lage sind, Datensätze in den erfassen Tabellen einzufügen, zu ändern oder zu löschen.

## <a name="security-filters---to-limit-a-users-access-to-specific-records-in-a-table"></a>Sicherheitsfilter - So beschränken Sie den Zugriff eines Benutzers auf bestimmte Datensätze in einer Tabelle
Verwenden Sie für Sicherheit auf Datensatzebene in [!INCLUDE[d365fin](includes/d365fin_md.md)] Sicherheitsfilter, um den Benutzerzugriff auf Daten in einer Tabelle einzuschränken. Sie erstellen Sicherheitsfilter für Tabellendaten. Ein Sicherheitsfilter beschreibt einen Satz Datensätze in einer Tabelle, worauf ein Benutzer zugreifen darf. Sie können z. B. angeben, dass ein Benutzer nur die Daten lesen kann, die Informationen über einen bestimmten Debitor enthalten. Das bedeutet, dass der Benutzer nicht auf die Daten zugreifen kann, die Informationen zu anderen Debitoren enthalten. Weitere Informationen finden Sie unter [Verwenden von Sicherheitsfiltern](/dynamics365/business-central/dev-itpro/security/security-filters) in der Hilfe für Entwickler und IT-Spezialisten.

## <a name="to-manage-permissions-through-user-groups"></a>So verwalten Sie Berechtigungen über Benutzergruppen
Sie können Benutzergruppen einrichten, die Ihnen bei der Verwaltung von Berechtigungen für Benutzergruppen in Ihrem Unternehmen helfen.

Sie beginnen mit der Erstellung einer Benutzergruppe. Anschließend ordnen Sie der Gruppe Berechtigungen zu, um festzulegen, auf welche Objekte die Benutzer der Gruppe zugreifen können. Wenn Sie einen Benutzer zur Gruppe hinzufügen, gelten die für die Gruppe definierten Berechtigungssätze für den Benutzer.

Berechtigungssätze, die einem Benutzer über eine Benutzergruppe zugewiesen wurden, bleiben synchronisiert, so dass eine Änderung der Berechtigungen der Benutzergruppe automatisch an den Benutzer weitergegeben wird. Wenn Sie einen Benutzer aus einer Benutzergruppe entfernen, werden die entsprechenden Berechtigungen automatisch entzogen.

### <a name="to-group-users-in-user-groups"></a>Um Benutzer in Benutzergruppen zu ordnen
Die folgende Vorgehensweise erläutert, wie Sie Benutzergruppen manuell anlegen. Um Benutzergruppen automatisch zu erstellen, siehe [Eine Benutzergruppe und alle ihre Berechtigungen kopieren](ui-define-granular-permissions.md#to-copy-a-user-group-and-all-its-permission-sets).

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzergruppen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie alternativ auf der Seite **Benutzer** die Aktion **Benutzergruppen** aus.
3. Wählen Sie auf der Seite **Benutzergruppen** die Aktion **Benutzergruppenmitglieder** aus.
4. Wählen Sie auf der Seite **Benutzergruppenmitglieder** die Aktion **Benutzer hinzufügen** aus.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>So kopieren Sie eine Benutzergruppe und all seine Zugriffsrechtsätze
Zur schnellen Definition einer neuen Benutzergruppe können Sie eine Funktion verwenden, um alle Berechtigungssätze einer vorhandenen Benutzergruppe zur neuen Benutzergruppe zu kopieren.

> [!NOTE]
> Die Mitglieder der Benutzergruppe werden nicht in die neue Benutzergruppe kopiert. Sie müssen sie hinterher manuell hinzufügen. Weitere Informationen finden Sie unter [So ordnen Sie Benutzer in Benutzergruppen](ui-define-granular-permissions.md#to-group-users-in-user-groups).

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzergruppen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Benutzergruppe aus, die Sie kopieren möchten, und wählen Sie **Benutzergruppe kopieren** aus.
3. Im Feld **Neuer Benutzergruppencode** geben Sie einen Namen für die Gruppe an. Wählen Sie dann die Schaltfläche **OK** aus.

Die neue Benutzergruppe wird die Seite **Benutzergruppen** hinzugefügt. Fahren Sie fort, um Benutzer hinzuzufügen. Weitere Informationen finden Sie unter [Zu Gruppenbenutzern in Benutzergruppen](ui-define-granular-permissions.md#to-group-users-in-user-groups).  

### <a name="to-assign-permission-sets-to-user-groups"></a>So weisen Sie Berechtigungssätze Benutzergruppen zu
1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzergruppen** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie die Benutzergruppe aus, der Sie die Berechtigung zuweisen möchten.
Zugriffsrechtsätze, die dem Benutzer bereits zugewiesen sind, werden im Bereich **Benutzerzugriffsrechtsätze** angezeigt.
3. Wählen Sie die Aktion **Benutzerrechtesätze**, um die Seite **Benutzerrechtesätze** zu öffnen.
4. Füllen Sie auf der Seite **Benutzerberechtigungen** in einer neuen Zeile die Felder nach Bedarf aus.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>So weisen Sie ein Berechtigungsset auf der Seite **Berechtigung festgelegt nach Benutzergruppe** zu  
Die folgende Vorgehensweise erläutert, wie Sie Berechtigungssätze einer Benutzergruppe auf der Seite **Berechtigungen nach Benutzergruppe** zuordnen.

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzer** ein und wählen Sie dann den entsprechenden Link.
2. Wählen Sie auf der Seite **Benutzer** den entsprechenden Benutzer aus und wählen Sie dann die Aktion **Berechtigung festgelegt durch Benutzergruppe**.
3. Aktivieren Sie auf der Seite **Berechtigung festgelegt durch Benutzergruppe** das Kontrollkästchen **[Name der Benutzergruppe]** in einer Zeile für die entsprechende Berechtigung, um die Gruppe der Benutzergruppe zuzuordnen.
4. Aktivieren Sie das Kontrollkästchen **Alle Benutzergruppen**, um die Berechtigung allen Benutzergruppen zuzuordnen.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>So entfernen Sie veraltete Berechtigungen aus allen Berechtigungssätzen
1. Wählen Sie auf der Seite **Berechtigungssätze** die Aktion **Veraltete Berechtigungssätze entfernen** aus.

## <a name="to-set-up-user-time-constraints"></a>So richten Sie Zeiteinschränkungen ein
Administratoren nutzen das Fenster Benutzer einrichten, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind. Administratoren können Benutzern Zuständigkeitseinheiten zuordnen. Weitere Informationen finden Sie unter [Arbeiten mit Zuständigkeitseinheiten](inventory-responsibility-centers.md).

1. Wählen Sie die ![Glühbirne, die das Tell Me Feature](media/ui-search/search_small.png "Tell Me-Funktion") Symbol öffnet, geben Sie **Benutzereinrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie auf der Seite **Benutzereinrichtung** die Aktion **Neu** aus.
3. In dem Feld **Benutzer-ID** geben Sie die ID eines Benutzers ein, oder wählen Sie das Feld aus, um alle Nutzer der aktiven Fenster im System anzuzeigen.
4. Füllen Sie die Felder bei Bedarf aus.

## <a name="see-also"></a>Siehe auch
[Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md)  
[Profile verwalten](admin-users-profiles-roles.md)  
[Funktionen, die angezeigt werden ändern](ui-experiences.md)  
[Anpassen von [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Vorbereitung für die Geschäftstätigkeit](ui-get-ready-business.md)  
[Verwaltung](admin-setup-and-administration.md)  
[Benutzer zu Office 365 für Unternehmen hinzufügen](https://aka.ms/CreateOffice365Users)  
[Sicherheit und Schutz in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) in der Hilfe für Entwickler und IT-Profis
