---
title: Benutzerberechtigungen zuweisen oder bearbeiten | Microsoft Docs
description: "Beschreibt, wie Office 365 Benutzern Business Centrals hinzugefügt wird und vergibt dann Berechtigungen, Zugriffsrechte und Sicherheitseinstellungen."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 58077ae917d7943e6dd2da06847dfbb0eef5defd
ms.contentlocale: de-de
ms.lasthandoff: 09/28/2018

---
# <a name="managing-users-and-permissions"></a>Benutzer und ihre Berechtigungen verwalten
Um Benutzer in [!INCLUDE[d365fin](includes/d365fin_md.md)] hinzuzufügen, muss der Office 365-Administrator Ihres Unternehmens zuerst einen Benutzer im Office 365-Admin Center erstellen. Weitere Informationen sind hier verfügbar [Benutzer zu Office 365 for Business hinzufügen](https://aka.ms/CreateOffice365Users).

Sobald Benutzer in Office 365 erstellt sind, können diese in das **Benutzer**-Fenster in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert werden. Benutzer werden Berechtigungssätze abhängig vom Plan, der dem Benutzer in Office 365 zugewiesen. Ausführliche Informationen über Lizenzierung finden Sie unter [Microsoft Dynamics 365 Business Central Lizenzierungshandbuch](https://aka.ms/BusinessCentralLicensing).

Sie können dann fortfahren, um den Benutzern Berechtigungssätze zuzuordnen, um festzulegen, in welchen Datenbankobjekten und auf welche Benutzeroberflächenelemente, sie Zugriff haben und auf welche Unternehmen. Sie können Benutzer Benutzergruppen hinzufügen. Damit ist es leichter, dieselben Berechtigungssätze mehreren Benutzern zuzuordnen.

Ein Zugriffsrechtsatz ist eine Sammlung von Berechtigungen für bestimmte Objekte in der Datenbank. Allen Benutzern muss mindestens ein Berechtigungssatz zugeordnet werden, bevor sie auf [!INCLUDE[d365fin](includes/d365fin_md.md)] zugreifen können.

Im Fenster **Benutzerkarte** können Sie das Fenster **Effektive Berechtigungen** öffnen, um festzustellen, welche Berechtigungen der Benutzer hat und mit welchen Berechtigungssätzen sie gewährt werden. Hier können Sie zudem die Berechtigungsdetails für Berechtigungssätze des Typs **Benutzerdefiniert** ändern. Weitere Informationen finden Sie im Abschnitt "Anzeigen und Bearbeiten von Berechtigungen".

Administratoren nutzen das Fenster **Benutzer einrichten**, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind.

Ein anderes System, das definiert, welche Benutzer zugreifen können, ist das Festlegen von Erfahrungen. Weitere Informationen finden Sie unter [Ändern, welche Funktionen angezeigt werden](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Hinzufügen eines Benutzers in Business Central
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Benutzer von Office 365 abrufen** aus.

Jeder neue Benutzer, der für Ihr Office 365-Abonnement erstellt wurde, wird im Fenster **Benutzer** hinzugefügt.

## <a name="to-group-users-in-a-user-group"></a>Gruppieren von Benutzern in einer Benutzergruppe
Sie können Benutzergruppen einrichten, um Ihnen zu helfen, Berechtigungssätze für Benutzergruppen in Ihrem Unternehmen zu verwalten.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzergruppen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Benutzer** die Aktion **Benutzergruppen** aus.
3. Wählen Sie im Fenster **Benutzergruppen** die Aktion **Benutzergruppenmitglieder** aus.
4. Wählen Sie im Fenster **Benutzergruppenmitglieder** die Aktion **Benutzer hinzufügen** aus.

Wenn Benutzer oder Benutzergruppen erstellt werden, müssen Sie jedem davon Berechtigungssätze zuweisen, um festzulegen, auf welches Objekt ein Benutzer zugreifen kann. Zuerst müssen Sie die entsprechenden Berechtigungen im den Berechtigungssätzen organisieren. Weitere Informationen finden Sie im Abschnitt "Erstellen und Bearbeiten von Berechtigungssätzen".

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>So kopieren Sie eine Benutzergruppe und all seine Zugriffsrechtsätze
Zur schnellen Definition einer neuen Benutzergruppe können Sie eine Funktion verwenden, um alle Berechtigungssätze einer vorhandenen Benutzergruppe zur neuen Benutzergruppe zu kopieren.

Die Mitglieder der Benutzergruppe werden nicht in die neue Benutzergruppe kopiert. Sie müssen sie hinterher manuell hinzufügen.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzergruppen** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Benutzergruppe aus, die Sie kopieren möchten, und wählen Sie **Benutzergruppe kopieren** aus.
3. Im Feld **Neuer Benutzergruppencode** geben Sie einen Namen für die Gruppe an. Wählen Sie dann die Schaltfläche **OK** aus.

Die neue Benutzergruppe wird dem Fenster **Benutzergruppen** hinzugefügt. Fahren Sie fort, um Benutzer hinzuzufügen. Weitere Informationen finden Sie im Abschnitt „So ordnen Sie Benutzer in Benutzergruppen“.  

## <a name="to-set-up-user-time-constraints"></a>So richten Sie Zeiteinschränkungen ein
Administratoren nutzen das Fenster Benutzer einrichten, um Zeiträume zu definieren, in denen die angegebenen Benutzer Buchungen durchführen können. Außerdem können sie angeben, ob die Zeitdauer erfasst, während der angegebene Benutzer angemeldet sind. Administratoren können Benutzern Zuständigkeitseinheiten zuordnen. Weitere Informationen finden Sie unter [Arbeiten mit Zuständigkeitseinheiten](inventory-responsibility-centers.md).

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Benutzer einrichten** die Aktion **Neu** aus.
3. In dem Feld **Benutzer-ID** geben Sie die ID eines Benutzers ein, oder wählen Sie das Feld aus, um alle Nutzer der aktiven Fenster im System anzuzeigen.
4. Füllen Sie die Felder je nach Bedarf aus.

## <a name="to-create-or-edit-a-permission-set"></a>Erstellen und Bearbeiten von Berechtigungssätzen
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

1. Im Fenster **Berechtigungssätze** wählen Sie die Zeile für einen Zugriffsrechtsatz, den Sie kopieren möchten, und wählen die **Berechtigungssatz kopieren**-Aktion aus.
2. In Feld **Berechtigungssatz kopieren** geben Sie den Namen des neuen Berechtigungssatzes an, und wählen Sie dann die Schaltfläche **OK** aus.
3. Wählen Sie das Kontrollkästchen **Bei geändertem Berechtigungssatz benachrichtigen** aus, wenn Sie eine Verknüpfung zwischen den ursprünglichen und dem kopierten Berechtigungssätzen beibehalten möchten. Der Link wird verwendet, um Sie zu benachrichtigen, wenn der Name oder der Inhalt des ursprünglichen Berechtigungssatzes in einer zukünftigen Version geändert wird, auf die die Lösung später aktualisiert wird.

Der neue Berechtigungssatz mit allen Berechtigungen des kopierten Berechtigungssatzes wird als neue Zeile im Fenster **Berechtigungssätze** hinzugefügt. Beachten Sie, dass die Zeilen innerhalb jedes Typs alphabetisch geordnet sind.

## <a name="to-create-or-edit-permissions"></a>Erstellen und Bearbeiten von Berechtigungen
1. Im Fenster **Berechtigungssätze** wählen Sie die Zeile für einen Zugriffsrechtsatz, und wählen die **Berechtigungen**-Aktion aus.
2. Im Fenster **Berechtigungen** erstellen Sie eine neue Zeile oder bearbeiten Sie die Felder einer vorhandenen Zeile.

In jedem der fünf Zugriffstypfelder **Leseberechtigung**, **Einfügeberechtigung**, **Bearbeitungsberechtigung**, **Löschberechtigung** und **Ausführungsberechtigung** können Sie eine der folgenden drei Berechtigungsoptionen auswählen:

|Option|Description|Priorität|
|------|-----------|
|**Ja**|Der Benutzer kann die Aktion an dem fraglichen Objekt ausführen.|Am höchsten|
|**Indirekt**|Der Benutzer kann die Aktion an dem fraglichen Objekt nur über ein anderes zugehöriges Objekt ausführen, auf das der Benutzer vollständig zugreifen kann.|Zweithöchste|
|**"Leer"**|Der Benutzer kann die Aktion an dem fraglichen Objekt nicht ausführen.|Am niedrigsten|

> [!NOTE]  
> Wenn Sie eine Berechtigung und dadurch den zugehörigen Berechtigungssatz bearbeiten, gelten die Änderungen auch für andere Benutzer, denen der Berechtigungssatz zugewiesen wurde.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Zuweisen von Berechtigungssätzen zu Benutzern der Benutzergruppen
Sie können Berechtigungen Benutzern auf in zwei Arten zuweisen:
- Definieren Sie Zugriffsrechtsätze in der Benutzerkarte eines Benutzers.
- Aktivieren Sie das Kontrollkästchen für einen Benutzer, in einer Spalte, für einen verknüpften Berechtigungssatz, in einer Zeile, im Fenster **Benutzerberechtigungssatz nach Benutzer**.
    Auf diese Wiese können Sie auch Berechtigungssätze Benutzergruppen zuweisen.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Zuweisen eines Berechtigungssatzes in einer Benutzerkarte
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie den Benutzer aus, den Sie dem Debitor zuordnen möchten.
Zugriffsrechtsätze, die dem Benutzer bereits zugewiesen sind, werden im Bereich **Benutzerzugriffsrechtsätze** angezeigt.
3. Wählen Sie im Fenster **Eingehende Dokumente** das Fenster **Benutzerkarten** aus.
4. Füllen Sie im Inforegister **Benutzer-Berechtigungssatz** die Felder nach Bedarf aus. Weitere Informationen finden Sie im Abschnitt "Erstellen und Bearbeiten von Berechtigungssätzen".

### <a name="to-assign-a-permission-set-in-the-permission-set-by-user-window"></a>Zuweisen eines Berechtigungssatzes im Fenster **Benutzerberechtigungssatz nach Benutzer**  
Der nachfolgende Vorgang erklärt, wie einem Benutzer im Fenster **Benutzerberechtigungssatz nach Benutzer** Zugriffsrechtsätze zugewiesen werden. Die Schritte im Fenster **Berechtigungssatz nach Benutzergruppe** sind ähnlich.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Benutzer** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Benutzer** den gewünschten Benutzer aus, und wählen Sie die Aktion **Benutzerberechtigungssatz nach Benutzer** aus.
3. Im Fenster **Benutzerberechtigungssatz nach Benutzer** wählen Sie das Kontrollkästchen **[Benutzername]** in einer Zeile für den relevanten Berechtigungssatz aus, um den Satz einem Benutzer zuzuweisen.
4. Wählen Sie das Kontrollkästchen **Alle Benutzer** aus, um dem Berechtigungssatz allen Anwender zuzuweisen.

## <a name="to-view-or-edit-a-users-permissions"></a>Anzeigen und Bearbeiten der Berechtigungen eines Benutzers
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

5. Um einzelne Berechtigungen innerhalb des Berechtigungssatzes zu bearbeiten, wählen Sie den Wert im Feld **Berechtigungssatz** aus, um das Fenster **Berechtigungen** zu öffnen. Befolgen Sie die Schritte, die im Abschnitt "Erstellen und Bearbeiten von Berechtigungen" beschrieben werden.  

> [!NOTE]  
> Wenn Sie einen Berechtigungssatz bearbeiten, gelten die Änderungen auch für andere Benutzer, denen der Berechtigungssatz zugewiesen wurde.

## <a name="see-also"></a>Siehe auch
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Sie können auswählen, welche Funktionen angezeigt werden.](ui-experiences.md)   
[Verwaltung](admin-setup-and-administration.md)  
[Hinzufügen von Benutzern zu Office 365 for Business](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central – Lizenzierungshandbuch](https://aka.ms/BusinessCentralLicensing)

