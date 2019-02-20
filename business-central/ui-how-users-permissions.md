---
title: Benutzerberechtigungen zuweisen oder bearbeiten | Microsoft Docs
description: "Beschreibt, wie Office 365-Benutzern Business Central hinzugefügt wird und vergibt dann Berechtigungen, Zugriffsrechte und Sicherheitseinstellungen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 11/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 78e83ee0740531935bd30a5988a72d1421a1fd89
ms.contentlocale: de-de
ms.lasthandoff: 11/29/2018

---
# <a name="managing-users-and-permissions"></a>Benutzer und ihre Berechtigungen verwalten
Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen. Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://aka.ms/CreateOffice365Users).

Sobald Benutzer in Office 365 erstellt sind, können diese auf die **Benutzer**-Seite in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert werden. Benutzer werden Berechtigungssätze abhängig vom Plan, der dem Benutzer in Office 365 zugewiesen. Ausführliche Informationen über Lizenzierung finden Sie unter [Microsoft Dynamics 365 Business Central Lizenzierungshandbuch](https://aka.ms/BusinessCentralLicensing).

Sie können dann fortfahren, um den Benutzern Berechtigungssätze zuzuordnen, um festzulegen, in welchen Datenbankobjekten und auf welche Benutzeroberflächenelemente, sie Zugriff haben und auf welche Unternehmen. Sie können Benutzer Benutzergruppen hinzufügen. Damit ist es leichter, dieselben Berechtigungssätze mehreren Benutzern zuzuordnen.

Ein Zugriffsrechtsatz ist eine Sammlung von Berechtigungen für bestimmte Objekte in der Datenbank. Allen Benutzern muss mindestens ein Berechtigungssatz zugeordnet werden, bevor sie auf [!INCLUDE[d365fin](includes/d365fin_md.md)] zugreifen können.

Auf der Seite **Benutzerkarte** können Sie das Fenster **Effektive Berechtigungen** öffnen, um festzustellen, welche Berechtigungen der Benutzer hat und mit welchen Berechtigungssätzen sie gewährt werden. Hier können Sie zudem die Berechtigungsdetails für Berechtigungssätze des Typs **Benutzerdefiniert** ändern. Weitere Informationen finden Sie im Abschnitt "Anzeigen und Bearbeiten von Berechtigungen".

Administratoren nutzen die Seite **Benutzer einrichten**, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind.

Ein anderes System, das definiert, welche Benutzer zugreifen können, ist das Festlegen von Erfahrungen. Weitere Informationen finden Sie unter [Ändern, welche Funktionen angezeigt werden](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Hinzufügen eines Benutzers in Business Central
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Benutzer von Office 365 abrufen** aus.

Jeder neue Benutzer, der für Ihr Office 365-Abonnement erstellt wurde, wird auf der Seite **Benutzer** hinzugefügt.

## <a name="to-group-users-in-a-user-group"></a>Gruppieren von Benutzern in einer Benutzergruppe
Sie können Benutzergruppen einrichten, um Ihnen zu helfen, Berechtigungssätze für Benutzergruppen in Ihrem Unternehmen zu verwalten.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzergruppen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie alternativ auf der Seite **Benutzer** die Aktion **Benutzergruppen** aus.
3. Wählen Sie auf der Seite **Benutzergruppen** die Aktion **Benutzergruppenmitglieder** aus.
4. Wählen Sie auf der Seite **Benutzergruppenmitglieder** die Aktion **Benutzer hinzufügen** aus.

Wenn Benutzer oder Benutzergruppen erstellt werden, müssen Sie jedem davon Berechtigungssätze zuweisen, um festzulegen, auf welches Objekt ein Benutzer zugreifen kann. Zuerst müssen Sie die entsprechenden Berechtigungen im den Berechtigungssätzen organisieren. Weitere Informationen finden Sie im Abschnitt "Erstellen und Bearbeiten von Berechtigungssätzen".

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>So kopieren Sie eine Benutzergruppe und all seine Zugriffsrechtsätze
Zur schnellen Definition einer neuen Benutzergruppe können Sie eine Funktion verwenden, um alle Berechtigungssätze einer vorhandenen Benutzergruppe zur neuen Benutzergruppe zu kopieren.

Die Mitglieder der Benutzergruppe werden nicht in die neue Benutzergruppe kopiert. Sie müssen sie hinterher manuell hinzufügen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzergruppen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Benutzergruppe aus, die Sie kopieren möchten, und wählen Sie **Benutzergruppe kopieren** aus.
3. Im Feld **Neuer Benutzergruppencode** geben Sie einen Namen für die Gruppe an. Wählen Sie dann die Schaltfläche **OK** aus.

Die neue Benutzergruppe wird die Seite **Benutzergruppen** hinzugefügt. Fahren Sie fort, um Benutzer hinzuzufügen. Weitere Informationen finden Sie im Abschnitt „So ordnen Sie Benutzer in Benutzergruppen“.  

## <a name="to-set-up-user-time-constraints"></a>So richten Sie Zeiteinschränkungen ein
Administratoren nutzen das Fenster Benutzer einrichten, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind. Administratoren können Benutzern Zuständigkeitseinheiten zuordnen. Weitere Informationen finden Sie unter [Arbeiten mit Zuständigkeitseinheiten](inventory-responsibility-centers.md).

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie auf der Seite **Benutzereinrichtung** die Aktion **Neu** aus.
3. In dem Feld **Benutzer-ID** geben Sie die ID eines Benutzers ein, oder wählen Sie das Feld aus, um alle Nutzer der aktiven Fenster im System anzuzeigen.
4. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-create-or-modify-a-permission-set"></a>Um ein Berechtigungssatz zu erstellen oder zu ändern
Berechtigungssatz funktionieren als Container von Berechtigungen, sodass Sie mehrere Berechtigungen einfach in einem Datensatz verwalten können. Wenn Sie einen Berechtigungssatz erstellt haben, müssen Sie die tatsächlichen Berechtigungen hinzufügen. Weitere Informationen finden Sie im Abschnitt "Erstellen und Bearbeiten von Berechtigungen".

> [!NOTE]  
> Eine [!INCLUDE[d365fin](includes/d365fin_md.md)]-Lösung enthält normalerweise mehrere vordefinierte Berechtigungssätze, die von Microsoft oder von Ihrem Software-Anbieter hinzugefügt werden. Diese Berechtigungssätze sind vom Typ **System** oder **Erweiterung**. Sie können diese Art der Berechtigungssätze oder die Berechtigungen darin nicht erstellen oder bearbeiten. Jedoch können Sie sie kopieren, um eigene Berechtigungssätze und Berechtigungen zu definieren. <br /><br />
Berechtigungssätze, die Benutzer neu oder als Kopien erstellen, sind vom Typ **Benutzerdefiniert** und können bearbeitet werden.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Berechtigungssätze** ein, und wählen dann den zugehörigen Link aus.
2. Wenn Sie einen neuen Berechtigungssatz erstellen, wählen Sie die Aktion **Neu** aus.
3. Auf der neuen Zeile füllen Sie die Felder wie erforderlich aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Kopieren eines Berechtigungssatzes
Wenn Sie neue Berechtigungssätze erstellen, können Sie eine Kopierfunktion verwenden, um schnell alle Berechtigungen eines anderen Berechtigungssätzen in einen neuen Berechtigungssatz zu übertragen.

> [!NOTE]  
> Wenn ein Systemberechtigungssatz, den Sie kopiert haben, geändert wird, werden Sie (abhängig von Ihrer Auswahl) benachrichtigt, sodass Sie entscheiden können, ob die Änderungen in Ihren benutzerdefinierten Berechtigungssatz kopiert oder geschrieben werden müssen.

1. Auf der Seite **Berechtigungssätze** wählen Sie die Zeile für einen Zugriffsrechtsatz, den Sie kopieren möchten, und wählen die **Berechtigungssatz kopieren**-Aktion aus.
2. Auf der Seite **Berechtigungssatz kopieren** geben Sie den Namen des neuen Berechtigungssatzes an, und wählen Sie dann die Schaltfläche **OK** aus.
3. Wählen Sie das Kontrollkästchen **Bei geändertem Berechtigungssatz benachrichtigen** aus, wenn Sie eine Verknüpfung zwischen den ursprünglichen und dem kopierten Berechtigungssätzen beibehalten möchten. Der Link wird verwendet, um Sie zu benachrichtigen, wenn der Name oder der Inhalt des ursprünglichen Berechtigungssatzes in einer zukünftigen Version geändert wird, auf die die Lösung später aktualisiert wird.

Der neue Berechtigungssatz mit allen Berechtigungen des kopierten Berechtigungssatzes wird als neue Zeile auf der Seite **Berechtigungssätze** hinzugefügt. Beachten Sie, dass die Zeilen innerhalb jedes Typs alphabetisch geordnet sind.

## <a name="to-create-or-modify-permissions-manually"></a>Um Berechtigungen manuell zu erstellen oder zu ändern
In diesem Verfahren wird beschrieben, wie manuell Berechtigungen addiert oder bearbeitet werden. Sie können einen Berechtigungssatz auch automatisch aus Ihren Aktionen in der Benutzeroberfläche generieren lassen. Weitere Informationen finden Sie im Abschnitt "So erstellen oder ändern Sie Berechtigungssätze durch Aufnehmen Ihrer Aktionen".

1. Auf der Seite **Berechtigungssätze** wählen Sie die Zeile für einen Zugriffsrechtsatz, und wählen die **Berechtigungen**-Aktion aus.
2. Auf der Seite **Berechtigungen** erstellen Sie eine neue Zeile oder bearbeiten Sie die Felder einer vorhandenen Zeile.

In jedem der fünf Zugriffstypfelder **Leseberechtigung**, **Einfügeberechtigung**, **Bearbeitungsberechtigung**, **Löschberechtigung** und **Ausführungsberechtigung** können Sie eine der folgenden drei Berechtigungsoptionen auswählen:

|Option|Description|Priorität|
|------|-----------|
|**Ja**|Der Benutzer kann die Aktion an dem fraglichen Objekt ausführen.|Am höchsten|
|**Indirekt**|Der Benutzer kann die Aktion an dem fraglichen Objekt nur über ein anderes zugehöriges Objekt ausführen, auf das der Benutzer vollständig zugreifen kann.|Zweithöchste|
|**"Leer"**|Der Benutzer kann die Aktion an dem fraglichen Objekt nicht ausführen.|Am niedrigsten|

### <a name="example---indirect-permission"></a>Beispiel - Indirekte Berechtigungen
Sie können indirekte Berechtigungen zuweisen, um ein Objekt nur über ein anderes Objekt zu verwenden.
Beispielsweise kann ein Benutzer die Berechtigung haben, Codeunit 80, Vertrieb-Beitrag, auszuführen. Die Verkaufsbuchung Codeunit führt viele Aufgaben aus, einschließlich der Bearbeitung von Tabelle 37 Verkaufsposition aus. Wenn der Benutzer ein Verkaufsbeleg bucht, überprüft die Codeunit "Vertrieb-Beitrag" [!INCLUDE[d365fin](includes/d365fin_md.md)], ob der Benutzer über die Berechtigung zum Bearbeiten der Tabelle "Verkaufszeile" verfügt. Wenn nicht, kann die Codeunit ihre Aufgaben nicht ausführen und der Benutzer erhält eine Fehlermeldung. In diesem Fall wird die Codeunit erfolgreich ausgeführt.

Jedoch muss der Anwender keinen vollen Zugriff auf die Tabelle Verkaufszeile haben, um Codeunit auszuführen. Wenn der Benutzer über indirekte Berechtigungen für die Tabelle "Verkaufszeile" verfügt, wird die Codeunit "Verkaufseinheit" erfolgreich ausgeführt. Wenn ein Benutzer über indirekte Berechtigungen verfügt, kann dieser Benutzer die Tabelle Verkaufszeile nur ändern, indem die Verkaufsbuchung Codeunit oder ein anderes Objekt ausgeführt wird, das die Berechtigung zum ändern der Tabelle Verkaufsposition hat. Der Benutzer kann die Tabelle Verkaufsposition nur von unterstützten Anwendungsbereichen aus ändern. Der Benutzer kann die Funktion mit anderen Methoden nicht unbeabsichtigt oder böswillig ausführen.

## <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Um Berechtigungssätze durch die Erfassung Ihrer Aktionen zu erstellen oder zu ändern
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Berechtigungssätze** ein, und wählen dann den zugehörigen Link aus.
2.  Wählen Sie alternativ auf der Seite **Benutzer** die Aktion **Berechtigungssätze** aus.
3.  Wählen Sie auf der Seite **Benutzer** die Aktion **Neu** aus.
4.  Füllen Sie die Felder in einer neuen Zeile wie erforderlich aus.
5.  Wählen Sie die Aktion **Berechtigungen** aus.
6.  Auf der Seite **Berechtigungen** wählen Sie die Aktion **Berechtigungen aufzeichnen** aus, und wählen Sie dann die Aktion **Starten** aus.

    Damit wird ein Aufnahmeprozesses gestartet, der alle Ihre Aktionen in der Benutzeroberfläche erfasst.
7.  Wechseln Sie zu den verschiedenen Seiten und Aktivitäten in [!INCLUDE[d365fin](includes/d365fin_md.md)] für die Benutzer mit diesem Berechtigungssatz, die darauf zugreifen sollen. Sie müssen die Aufgaben ausführen, für die Sie Berechtigungen erfassen möchten.
8.  Wenn Sie die Erfassung abschließen möchten, kehren Sie zur Seite **Berechtigungen** zurück, und wählen Sie die **Beenden** Aktion aus.
9.  Wählen Sie die Schaltfläche **Ja**, um die erfassten Berechtigungen dem neuen Berechtigungssatz zuzuordnen.
10. Für jedes Objekt in der erfassten Liste geben Sie an, ob Benutzer in der Lage sind, Datensätze in den erfassen Tabellen einzufügen, zu ändern oder zu löschen.

> [!NOTE]  
> Wenn Sie eine Berechtigung und dadurch den zugehörigen Berechtigungssatz bearbeiten, gelten die Änderungen auch für andere Benutzer, denen der Berechtigungssatz zugewiesen wurde.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Zuweisen von Berechtigungssätzen zu Benutzern der Benutzergruppen
Sie können Berechtigungen Benutzern auf in zwei Arten zuweisen:
- Definieren Sie Zugriffsrechtsätze in der Benutzerkarte eines Benutzers.
- Aktivieren Sie das Kontrollkästchen für einen Benutzer, in einer Spalte, für einen verknüpften Berechtigungssatz, in einer Zeile, auf der Seite **Benutzerberechtigungssatz nach Benutzer**.
    Auf diese Wiese können Sie auch Berechtigungssätze Benutzergruppen zuweisen.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Zuweisen eines Berechtigungssatzes in einer Benutzerkarte
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie den Benutzer aus, den Sie dem Debitor zuordnen möchten.
Zugriffsrechtsätze, die dem Benutzer bereits zugewiesen sind, werden im Bereich **Benutzerzugriffsrechtsätze** angezeigt.
3. Wählen Sie auf der Seite **Benutzerkarte** die Aktion **Bearbeiten** aus.
4. Füllen Sie im Inforegister **Benutzer-Berechtigungssatz** die Felder nach Bedarf aus. Weitere Informationen finden Sie im Abschnitt "Erstellen und Bearbeiten von Berechtigungssätzen".

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Zuweisen eines Berechtigungssatzes auf der Seite **Benutzerberechtigungssatz nach Benutzer**  
Der nachfolgende Vorgang erklärt, wie einem Benutzer auf der Seite **Benutzerberechtigungssatz nach Benutzer** Zugriffsrechtsätze zugewiesen werden. Die Schritte auf der Seite **Berechtigungssatz nach Benutzergruppe** sind ähnlich.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie auf der Seite **Benutzer** den gewünschten Benutzer aus, und wählen Sie die Aktion **Benutzerberechtigungssatz nach Benutzer** aus.
3. Auf der Seite **Benutzerberechtigungssatz nach Benutzer** wählen Sie das Kontrollkästchen **[Benutzername]** in einer Zeile für den relevanten Berechtigungssatz aus, um den Satz einem Benutzer zuzuweisen.
4. Wählen Sie das Kontrollkästchen **Alle Benutzer** aus, um dem Berechtigungssatz allen Anwender zuzuweisen.

## <a name="to-get-an-overview-of-a-users-permissions"></a>So erhalten Sie eine Übersicht der Benutzerberechtigungen
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie die karte des relevanten Benutzers.
3. Wählen Sie die Aktion **Effektive Berechtigungen** aus.

    Der Teil **Berechtigungen** führt alle Datenbankobjekte auf, auf die der Benutzer Zugriff hat. Sie können diesen Abschnitt nicht bearbeiten.

    Der Teil **Nach Berechtigungssatz** zeigt die zugewiesenen Zugriffsrechtsätze, über die dem Benutzer die Berechtigungen gewährt werden, die Herkunft und die Art des Berechtigungssatzes und wie weit die verschiedenen Berechtigungssätze zulässig sind.

    Für jede Zeile, die Sie im Abschnitt **Berechtigungen** auswählen, zeigt der Abschnitt **Nach Berechtigungssatz**, welchen Berechtigungssatz oder welche -sätze an, über die die Berechtigung gewährt wird. In diesem Abschnitt können Sie den Wert in jedem der fünf Zugriffstypfelder **Leseberechtigung**, **Einfügeberechtigung**, **Bearbeitungsberechtigung**, **Löschberechtigung** und **Ausführungsberechtigung** ändern.   

    > [!NOTE]  
    > Nur Berechtigungssätze vom Typ **Benutzerdefiniert** können bearbeitet werden.<br /><br />
    > Zeilen des Quellrechtsanspruchs stammen aus dem Abonnementplan. Die Berechtigungswerte des Anspruchs setzen Werte in anderen Berechtigungssätzen außer Kraft, wenn Ihre Priorität höher ist. Ein Wert in einem Berechtigungssatz ohne Anspruch mit einer höheren Priorität als der zugehörige Wert im Anspruch, wird in Klammern gesetzt, um anzugeben, dass er nicht wirksam ist, da er durch den Anspruch außer Kraft gesetzt wurde. Eine Erklärung der Priorität finden Sie im Abschnitt "Erstellen und Bearbeiten von Berechtigungen".  

4. Wenn Sie einen Berechtigungssatz bearbeiten möchten, wählen Sie im Teil **Nach Berechtigungssatz** in der Zeile für einen entsprechenden Berechtigungssatz vom Typ **Benutzerdefiniert** eins der fünf Zugriffstypfelder und einen anderen Wert aus.

5. Um einzelne Berechtigungen innerhalb des Berechtigungssatzes zu bearbeiten, wählen Sie den Wert im Feld **Berechtigungssatz** aus, um die Seite **Berechtigungen** zu öffnen. Befolgen Sie die Schritte, die im Abschnitt "Erstellen und Bearbeiten von Berechtigungen" beschrieben werden.  

> [!NOTE]  
> Wenn Sie einen Berechtigungssatz bearbeiten, gelten die Änderungen auch für andere Benutzer, denen der Berechtigungssatz zugewiesen wurde.

## <a name="see-also"></a>Siehe auch
[Benutzer, Profile und Rollencenter verstehen](admin-users-profiles-roles.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  
[Verwaltung](admin-setup-and-administration.md)  
[Hinzufügen von Benutzern zu Office 365 for Business](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central – Lizenzierungshandbuch](https://aka.ms/BusinessCentralLicensing)

