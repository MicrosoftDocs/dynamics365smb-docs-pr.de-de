---
title: Kontrollieren Sie den Zugriff mithilfe von Sicherheitsgruppen
description: 'In diesem Artikel wird beschrieben, wie Sicherheitsgruppen zum Definieren von Benutzerberechtigungen verwendet werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Kontrollieren Sie den Zugriff auf Business Central mithilfe von Sicherheitsgruppen

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Sicherheitsgruppen erleichtern Administratoren die Verwaltung von Benutzerberechtigungen in ihren Dynamics 365-Anwendungen, wie SharePoint Online, CRM Online und die Online-Version von [!INCLUDE [prod_short](includes/prod_short.md)]. Administratoren fügen ihren Sicherheitsgruppen Berechtigungen hinzu, und wenn sie der Gruppe Benutzer hinzufügen, gelten die Berechtigungen für alle Mitglieder. Beispielsweise kann ein Administrator eine Sicherheitsgruppe erstellen, die Verkäufern die Möglichkeit gibt, Verkaufsaufträge zu erstellen und zu buchen. Oder lassen Sie Käufer dasselbe für Bestellungen tun.

Erstellen Sie Ihre Sicherheitsgruppen in Ihrem Microsoft 365 Admin Center oder Azure Active Directory. Dieser Artikel beschreibt die Schritte im Microsoft 365 Admin Center, aber die Schritte sind in beiden ähnlich.

## Fügen Sie im Microsoft 365 Admin Center eine Sicherheitsgruppe hinzu

1. Wechseln Sie im Microsoft 365 Admin Center zur Seite **Aktive Teams & Gruppen**.
2. Wählen Sie **Eine Gruppe hinzufügen**.
3. Wählen Sie den Gruppentyp **Sicherheit** und wählen sie **Weiter**.
4. Legen Sie die Grundlagen für Ihre Gruppe fest.
5. Optional: Machen Sie die Mitglieder der Gruppe für die Rollenzuweisung verfügbar. Um mehr über die Zuweisungen zu erfahren, gehen Sie zu [Azure AD Gruppen zum Verwalten von Rollenzuweisungen verwenden](/azure/active-directory/roles/groups-concept).
6. Öffnen Sie die Gruppe und verwenden Sie dann die Registerkarte **Mitglieder hinzufügen**, um Personen in die Gruppe aufzunehmen.

## Eine Sicherheitsgruppe in Business Central hinzufügen

Erstellen Sie in [!INCLUDE [prod_short](includes/prod_short.md)] eine Sicherheitsgruppe und verknüpfen Sie sie dann mit der Sicherheitsgruppe im Microsoft 365 Admin Center. Ihre neue Gruppe enthält die Mitglieder, die Sie im Microsoft 365 Admin Center hinzugefügt haben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Sicherheitsgruppen** ein und wählen Sie dann die zugehörige Verknüpfung.
2. Wählen Sie **Neu**, um eine Gruppe zu erstellen.
3. Geben Sie im Feld **Namen** einen Namen für die Gruppe ein.
4. Geben Sie im Feld **Name der AAD-Sicherheitsgruppe** den Namen der Sicherheitsgruppe genau so ein, wie er im Microsoft 365 Admin Center angezeigt wird. [!INCLUDE [prod_short](includes/prod_short.md)] findet diese Gruppe und verknüpft sie mit dieser Gruppe.

> [!NOTE]
> Die Benutzer, die auf der Karte **Mitglieder** in der Infobox oder auf der Seite **Mitglieder der Sicherheitsgruppe** nur angezeigt werden, wenn sie als Benutzer in [!INCLUDE [prod_short](includes/prod_short.md)] hinzugefügt wurden. Mehr über das hinzufügen von Benutzern erfahren unter [Um Benutzer hinzuzufügen oder Benutzerinformationen und Lizenzzuweisungen in Business Central zu aktualisieren](ui-how-users-permissions.md#adduser).  

### Der Gruppe Berechtigungen zuweisen

1. Wählen Sie auf der Seite **Sicherheitsgruppe** die Gruppe aus und wählen Sie die Aktion **Berechtigungen**.
1. Weisen Sie Berechtigungen folgendermaßen zu:
    * Um Berechtigungssätze einzeln zuzuweisen, wählen Sie im Feld **Berechtigungssatz** die zuzuweisenden Berechtigungen aus.
    * Um mehrere Berechtigungssätze zuzuweisen, wählen Sie die Aktion **Berechtigungssätze auswählen** und dann die zuzuweisenden Sätze aus.

## Berechtigungen in der Sicherheitsgruppe prüfen

Auf der Seite **Sicherheitsgruppen** zeigt der Infobox-Bereich die **Berechtigungssätze** an, die der Gruppe zugewiesen sind. Jeder Benutzer, der auf der Karte **Mitglieder** aufgeführt ist, verfügt über diese Berechtigungen. Die Aktion **Berechtigung von Sicherheitsgruppe festgelegt** bietet eine detailliertere Ansicht. Dort können Sie auch die einzelnen Berechtigungen in jeder Sicherheitsgruppe erkunden.

Berechtigungen sind auch auf der Seite **Benutzer** verfügbar. Der Infoboxbereich zeigt die **Berechtigungssätze aus Sicherheitsgruppen** und **Sicherheitsgruppenmitgliedschaften** für den ausgewählten Benutzer.

## Sicherheitsgruppen und Benutzergruppen

Wenn Sie Benutzergruppen haben, können Sie die Gruppen in Berechtigungssätze in Ihrem Mandanten umwandeln, indem Sie die Anleitung zur unterstützten Einrichtung **Benutzergruppenmigration** verwenden. Um die Anleitung zu starten, suchen Sie auf der Seite **Funktionsverwaltung** **Funktion: Benutzergruppenberechtigungen konvertieren** und wählen Sie dann aus **Alle Benutzer** im Feld **Aktiviert für** aus. Die unterstützte Einrichtungsanleitung bietet die folgenden Optionen für die Konvertierung.

|Option  |Beschreibung  |
|---------|---------|
|Benutzer zuweisen     | Weisen Sie die Berechtigungen in Benutzergruppen direkt den Benutzern zu, die der Gruppe zugewiesen wurden und entfernen Sie die Zuweisung zur Benutzergruppe.        |
|In einen Berechtigungssatz konvertieren     | Erstellen Sie eine neue Berechtigung für die Berechtigungen in jeder Benutzergruppe. Der neue Berechtigungssatz wird allen Mitgliedern jeder Benutzergruppe zugewiesen.          |

## Weitere Informationen

[Benutzer nach Lizenzen anlegen](ui-how-users-permissions.md)  
[Zugriff auf Business Central in Teams mit Microsoft 365-Lizenzen festlegen](admin-access-with-m365-license-setup.md)  
[Erfahren Sie mehr über Gruppen und Zugriffsrechte in Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Active Directory-Sicherheitsgruppen](/windows-server/identity/ad-ds/manage/understand-security-groups)  