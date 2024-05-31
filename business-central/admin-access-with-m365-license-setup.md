---
title: Zugriff mit Microsoft 365-Lizenzen einrichten
description: 'Eine Anleitung, wie Administratoren den Zugriff auf Business Central mit Microsoft 365-Lizenzen konfigurieren können.'
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/28/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
ms.search.form: '9061,'
---
# <a name="set-up-business-central-access-in-teams-with-microsoft-365-licenses"></a>Zugriff auf Business Central in Teams mit Microsoft 365-Lizenzen festlegen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Administratoren müssen mehrere Aktivitäten abschließen, bevor Benutzer auf [!INCLUDE [prod_short](includes/prod_short.md)] mit ihrer Microsoft 365-Lizenz zugreifen können. Die folgenden Schritte stellen die Mindesteinrichtung dar, die für den Einstieg erforderlich ist. Um mehr über den Zugriff mit Microsoft 365-Lizenzen zu erfahren, gehen Sie zu [Business Central Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license.md).

## <a name="guidelines"></a>Richtlinien

Das Einrichten des Zugriffs mit Microsoft 365-Lizenzen umfasst die folgenden Aufgaben:

|Schritt|Aufgabe|Erforderlich|
|-|-|-|
|0|[Konfigurieren Sie, welche Business Central-Daten die Benutzer mit Microsoft 365-Lizenz anzeigen dürfen](#configure-permissions)|![Häkchen](media/check.png "Aktivieren")|
|2|[Ermöglichen Sie den Zugriff mit Microsoft 365-Lizenzen auf die Business Central-Umgebung](#enable-access-with-microsoft-365-licenses)|![Häkchen](media/check.png "Aktivieren")|
|3|[Weisen Sie eine Sicherheitsgruppe der Umgebung zu](#choose-who-gets-access-by-using-security-group)|
|4|[Business Central-App für Teams für Benutzer bereitstellen](#deploy-the-business-central-app-for-teams)|![Häkchen](media/check.png "Aktivieren")|
|5|[Testen Sie die Einrichtung](#test-your-setup)||

> [!TIP]
> Mit Ausnahme der letzten Aufgabe können Sie die Aufgaben in beliebiger Reihenfolge erledigen. Sie können Aufgaben separat ausführen, wie in den folgenden Abschnitten beschrieben, oder die Anleitung zur unterstützten Einrichtung von **Zugriff mit Microsoft 365-Lizenzen** verwenden, um sie zu erklären.
>
> Um die unterstützte Einrichtung auszuführen, gehen Sie folgendermaßen vor:
>
> 1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol, geben Sie **Unterstützte Einrichtung** ein und wählen Sie dann den entsprechenden Link.
> 2. Gehen Sie auf der Seite **Unterstützte Einrichtung** zum Abschnitt **Mehr Möglichkeiten in Business Central** und wählen Sie **Zugriff mit Microsoft 365-Lizenzen**.
> 3. Befolgen Sie den Anweisungen.  

## <a name="configure-permissions"></a>Berechtigungen konfigurieren

[!INCLUDE [prod_short](includes/prod_short.md)] ist von Haus aus sicher und minimiert das Risiko, indem keine Berechtigungen für Microsoft 365-Benutzer standardmäßig gewährt werden. Administratoren müssen Objektberechtigungen konfigurieren, die festlegen, auf welche Tabellen, Seiten und Berichte in Teams nur mit einer Microsoft 365-Lizenz zugegriffen werden kann. Diese Berechtigungen sind die Startberechtigungen, die zugewiesen werden, wenn sich ein Benutzer zum ersten Mal mit seiner Microsoft 365-Lizenz anmeldet. 

So konfigurieren Sie Startberechtigungen:

1. Suchen Sie in [!INCLUDE [prod_short](includes/prod_short.md)] nach **Lizenzkonfiguration**.
2. Wählen Sie die Microsoft 365-Lizenz aus.
3. Wählen Sie oben auf der **Microsoft 365**-Lizenzseite das Bearbeiten-Symbol ![Bearbeiten-Symbol](media/edit-pencil.png) aus, aktivieren Sie dann **Berechtigungen anpassen**. 
4. Fügen Sie im Abschnitt **Benutzerdefinierte Berechtigungssätze** die entsprechenden Berechtigungssätze hinzu und wählen Sie aus, ob sie für ein einzelnes Unternehmen oder alle Unternehmen in der Umgebung gelten.

Bei dieser Konfiguration werden Benutzer mit nur einer Microsoft 365-Lizenz zur Liste **Benutzer** hinzugefügt, wenn sie zum ersten Mal auf [!INCLUDE [prod_short](includes/prod_short.md)] zugreifen. Weitere Informationen über Benutzer finden Sie unter [Erstellen von Benutzern nach Lizenzen](ui-how-users-permissions.md).

> [!NOTE]
> Beim Synchronisieren der Benutzerliste in [!INCLUDE [prod_short](includes/prod_short.md)] mit Benutzern in Microsoft 365 werden nur Benutzer, die über eine [!INCLUDE [prod_short](includes/prod_short.md)]-Lizenz verfügen, zur Benutzerliste von [!INCLUDE [prod_short](includes/prod_short.md)] hinzugefügt. Um mehr administrative Steuerelemente für Berechtigungen und Profile zu erhalten, können Sie der Umgebung eine Sicherheitsgruppe zuweisen. Wenn Umgebungen mit einer Sicherheitsgruppe gesichert sind und der Zugriff mit Microsoft 365-Lizenzen ermöglicht wird, schließt die Aktion **Benutzer von Microsoft 365** auf der Seite **Benutzer** auch Benutzer ein, die nur eine Microsoft 365-Lizenz haben. Informationen zur Sicherung von Umgebungen finden Sie unter [Verwalten des Zugriffs mit Microsoft Entra-Gruppen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) in der Hilfe für Entwickler und IT-Profis.

> [!TIP]
> Suchen Sie nach einer schnelleren Möglichkeit, diese Funktion in einer Sandbox oder Auswertungsfirma auszuprobieren? Weisen Sie den Berechtigungssatz **D365 Lesen** zu, der den meisten Objekten Berechtigungen erteilt.  

Beim Arbeiten mit mehreren Umgebungen muss die Lizenzkonfiguration auf jede Umgebung angewendet werden und kann in jeder Umgebung unterschiedlich sein.

Weitere Informationen finden Sie unter [Zuweisen von Berechtigungen zu Benutzern und Gruppen](ui-define-granular-permissions.md) und [Zusammenstellen von Berechtigungssätzen](/dynamics365/business-central/dev-itpro/developer/devenv-permissionset-composing).

## <a name="enable-access-with-microsoft-365-licenses"></a>Zugriff mit Microsoft 365-Lizenzen ermöglichen

Der Zugriff mit Microsoft 365-Lizenzen ist standardmäßig deaktiviert. Der Zugriff muss für jede Umgebung separat aktiviert werden, sodass Administratoren die Kontrolle erhalten und eine gestaffelte Einführung in der gesamten Organisation möglich ist. Sie aktivieren den Zugriff über das [!INCLUDE [prod_short](includes/prod_short.md)] Admin Center: 

1. Wählen Sie in der oberen rechten Ecke **Einstellungen** ![Einstellungen.](media/ui-experience/settings_icon_small.png "Einstellungssymbol für Rollenzentrum") > **Admin Center**.  
2. Wählen Sie im Admin Center  **Umgebungen** aus, und wählen Sie dann die Umgebung aus, für die Sie den Lizenzzugriff ändern möchten. 
3. Wählen Sie auf der **Umgebungsdetails**-Seite **Ändern** für die Einstellung **Zugriff mit Microsoft 365-Lizenzen**.
4. In dem Bereich **Microsoft 365-Lizenzen** schalten Sie den Schalter ein. 
5. Wählen Sie **Speichern** aus, wenn Sie fertig sind, und akzeptieren Sie die Bestätigung. Die Änderung tritt sofort in Kraft.

## <a name="choose-who-gets-access-by-using-security-group"></a>Wählen Sie mithilfe der Sicherheitsgruppe aus, wer Zugriff erhält

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Im Business Center Admin Center kann eine Umgebung einer oder mehreren Sicherheitsgruppen zugewiesen werden, um den Zugriff zu steuern. Sie können der Umgebung eine Microsoft Entra-Gruppe hinzufügen. Durch die Zuweisung einer Microsoft Entra-Gruppe zu einer Umgebung erhalten nur direkte und indirekte Mitglieder der Gruppe Zugriff auf die Umgebung. Indirekte Mitglieder sind Benutzer einer anderen Gruppe, die selbst Mitglied der der Umgebung zugeordneten Gruppe ist. Obwohl alle lizenzierten Benutzer in Microsoft Entra-ID der Umgebung hinzugefügt werden, wenn sie mit Microsoft 365 synchronisiert wird, können sich nur Gruppenmitglieder anmelden. Weitere Informationen finden Sie unter [Verwalten des Zugriffs mit Microsoft Entra-Gruppen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access#manage-access-using-azure-active-directory-groups) in der Hilfe für Entwickler und IT-Profis.

## <a name="deploy-the-business-central-app-for-teams"></a>Die Business Central-App für Teams bereitstellen

Für [!INCLUDE [prod_short](includes/prod_short.md)]-Lizenzinhaber zum Teilen von Daten in Teams und für Microsoft 365-Lizenzinhaber, um auf diese Daten zugreifen zu können, muss die [!INCLUDE [prod_short](includes/prod_short.md)]-App für Teams installiert sein. Obwohl Benutzer die App selbst installieren können, wird empfohlen, dass Administratoren die zentrale Bereitstellung verwenden. Durch die zentrale Bereitstellung können Sie die App einem breiteren Publikum in der gesamten Organisation zur Verfügung stellen und den Aufwand einzelner Benutzer minimieren. 

Informationen zum zentralen Bereitstellen der [!INCLUDE [prod_short](includes/prod_short.md)]-App für Teams finden Sie unter [Installieren der Business Central-App mit Hilfe der zentralen Bereitstellung](admin-teams-integration.md#installing-the-business-central-app-by-using-centralized-deployment).

> [!NOTE]
> Wenn Sie zuvor die zentrale Bereitstellung ausgeführt und die App nur für die Sicherheitsgruppe der lizenzierten [!INCLUDE [prod_short](includes/prod_short.md)]-Benutzer bereitgestellt haben, müssen Sie sie erneut ausführen, um sie für zusätzliche Gruppen oder die gesamte Organisation bereitzustellen, je nachdem, wie Sie den Zugriff konfigurieren.

> [!TIP]
> Suchen Sie nach einer schnelleren Möglichkeit, diese Funktion auszuprobieren? Testbenutzer können die App unter [aka.ms/BCgetTeamsApp](https://aka.ms/BCgetTeamsApp) installieren.

## <a name="test-your-setup"></a>Ihre Einrichtung testen

Um zu überprüfen, ob Ihr Setup für die Produktion bereit ist, helfen Ihnen die folgenden Schritte, das Vertrauen aufzubauen, dass alles so funktioniert, wie es sollte.

1. Erstellen oder identifizieren Sie zwei Testbenutzer (A und B).

   - Testbenutzer A muss über eine [!INCLUDE [prod_short](includes/prod_short.md)]-Lizenz und Microsoft 365-Lizenz mit Zugriff auf Teams verfügen.
   - Testbenutzer B muss nur eine Microsoft 365-Lizenz mit Zugriff auf Teams haben.

2. Melden Sie sich als Testbenutzer A beim [!INCLUDE [prod_short](includes/prod_short.md)]-Webclient an.

   1. Öffnen Sie einen Datensatz, auf den Testbenutzer B Zugriff haben soll, z. B. eine **Artikel**-Karte in der entsprechenden Firma und Umgebung.
   2. Wählen Sie **Teilen** ![!Aktion auf Seiten mit anderen Apps teilen.](media/share-icon.png) > **Für Teams freigeben**, um das Fenster „Für Teams freigeben“ aufzurufen.
   3. In dem Feld **Freigeben für** fügen Sie Testnutzer B als Empfänger hinzu.
   4. Warten Sie, bis der Link zu einer Karte erweitert wird, und wählen Sie „Teilen“ aus.

3. Melden Sie sich bei Microsoft Teams als Testbenutzer B an.

   1. Wählen Sie „Chat“ aus, und öffnen Sie die Unterhaltung mit Testbenutzer A.
   2. Wählen Sie in der von Testbenutzer A gesendeten Nachricht die Schaltfläche „Details“ auf der Karte aus. Wenn der [!INCLUDE [prod_short](includes/prod_short.md)]-Client angezeigt wird und schreibgeschützt ist, war Ihre Einrichtung erfolgreich.

> [!TIP]
> Ist ein Fehler aufgetreten? Überprüfen Sie [Fehlerbehebung beim Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license-troubleshooting.md).

## <a name="see-also"></a>Siehe auch

[Übersicht über den Business Central Access mit Microsoft 365-Lizenzen](admin-access-with-m365-license.md#minimum-requirements)  
[Fehlerbehebung beim Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license-troubleshooting.md)  
[Integration von Business Central und Microsoft Teams](across-teams-overview.md)  
