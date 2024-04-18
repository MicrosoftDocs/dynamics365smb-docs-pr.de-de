---
title: Kontrollieren Sie den Zugriff mithilfe von Sicherheitsgruppen
description: 'In diesem Artikel wird beschrieben, wie Sicherheitsgruppen zum Definieren von Benutzerberechtigungen verwendet werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 11/29/2023
ms.service: dynamics-365-business-central
---

# Kontrollieren Sie den Zugriff auf Business Central mithilfe von Sicherheitsgruppen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Sicherheitsgruppen erleichtern Administrierenden die Verwaltung von Benutzerberechtigungen. Beispielsweise sind sie für [!INCLUDE [prod_short](includes/prod_short.md)] online in allen Dynamics 365-Anwendungen wie SharePoint Online, CRM Online und [!INCLUDE [prod_short](includes/prod_short.md)] wiederverwendbar. Administrierende fügen ihren [!INCLUDE [prod_short](includes/prod_short.md)] Sicherheitsgruppen Berechtigungen hinzu, und wenn sie der Gruppe Benutzende hinzufügen, gelten die Berechtigungen für alle Mitglieder. Beispielsweise können Administrierende eine [!INCLUDE [prod_short](includes/prod_short.md)] Sicherheitsgruppe erstellen, die Verkaufsmitarbeitenden die Möglichkeit gibt, Verkaufsaufträge zu erstellen und zu buchen. Oder lassen Sie Käufer dasselbe für Bestellungen tun.

## Business Central Online und lokal

Sie können Sicherheitsgruppen für die Online- und lokalen Versionen von [!INCLUDE [prod_short](includes/prod_short.md)] verwenden. Erstellen Sie je nach Ihrer Version auf eine der folgenden Arten Gruppen:

* Verwenden Sie für die Onlineversion Microsoft Entra Sicherheitsgruppen. Weitere Informationen zum Erstellen der Gruppe finden Sie unter [Eine Sicherheitsgruppe im Microsoft 365 Admin Center erstellen, bearbeiten und löschen](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* Bei lokalen Umgebungen werden Sicherheitsgruppen nur unterstützt, wenn die Bereitstellung die Windows-Authentifizierung verwendet. Verwenden Sie Windows Active Directory-Gruppen, um Sicherheitsgruppen für lokale Umgebungen zu erstellen. Weitere Informationen finden Sie unter [Gruppenkonto in Windows Active Directory erstellen](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory). 

Erstellen Sie danach in [!INCLUDE [prod_short](includes/prod_short.md)] eine entsprechende Sicherheitsgruppe und verknüpfen Sie sie dann mit der Sicherheitsgruppe, die Sie erstellt haben. Um mehr zu erfahren, gehen Sie zu [Eine Sicherheitsgruppe in Business Central hinzufügen](#add-a-security-group-in-business-central).

> [!NOTE]
> Wenn Sie einen speziellen Benutzertyp mit einem Windows-Gruppenlizenztyp in einer lokalen Version von [!INCLUDE [prod_short](includes/prod_short.md)] eingerichtet haben, die vor den 1. Veröffentlichungszyklus 2023 liegt, konvertiert [!INCLUDE [prod_short](includes/prod_short.md)] beim Upgrade Benutzende zu einer Sicherheitsgruppe. Die neue Sicherheitsgruppe hat denselben Namen wie der Windows-Gruppenname. Die Sicherheitsgruppe gibt Ihnen einen besseren Überblick über die Gruppenmitglieder und deren wirksame Berechtigungen.

## Eine Sicherheitsgruppe in Business Central hinzufügen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion 1.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") öffnet. Symbol, geben Sie **Sicherheitsgruppen** ein und wählen Sie dann die zugehörige Verknüpfung.
1. Wählen Sie **Neu**, um eine Gruppe zu erstellen.
1. Erstellen Sie den Link zu Ihrer Gruppe wie folgt:

    * Wählen Sie für [!INCLUDE [prod_short](includes/prod_short.md)] online die Gruppe im Feld **Microsoft Entra-Sicherheitsgruppenname** aus.
    * Wählen Sie für lokale [!INCLUDE [prod_short](includes/prod_short.md)] Umgebungen die Gruppe im Feld **Windows-Gruppenname** aus.

> [!NOTE]
> Die Benutzenden werden auf der Karte **Mitglieder** in der Infobox oder auf der Seite **Mitglieder der Sicherheitsgruppe** nur angezeigt, wenn sie als Benutzende in [!INCLUDE [prod_short](includes/prod_short.md)] hinzugefügt wurden. Mehr über das hinzufügen von Benutzern erfahren unter [Um Benutzer hinzuzufügen oder Benutzerinformationen und Lizenzzuweisungen in Business Central zu aktualisieren](ui-how-users-permissions.md#adduser).  

### Einer Sicherheitsgruppe Berechtigungen zuweisen

1. Wählen Sie auf der Seite **Sicherheitsgruppe** die Gruppe aus und wählen Sie die Aktion **Berechtigungen**.
1. Weisen Sie Berechtigungen folgendermaßen zu:

    * Um Berechtigungssätze einzeln zuzuweisen, wählen Sie im Feld **Berechtigungssatz** die zuzuweisenden Berechtigungen aus.
    * Um mehrere Berechtigungssätze zuzuweisen, wählen Sie die Aktion **Berechtigungssätze auswählen** und dann die zuzuweisenden Sätze aus.

## Berechtigungen in der Sicherheitsgruppe prüfen

Auf der Seite **Sicherheitsgruppen** zeigt der Infobox-Bereich die **Berechtigungssätze** an, die der Gruppe zugewiesen sind. Jeder Benutzer, der auf der Karte **Mitglieder** aufgeführt ist, verfügt über diese Berechtigungen. Die Aktion **Berechtigung von Sicherheitsgruppe festgelegt** bietet eine detailliertere Ansicht. Dort können Sie auch die einzelnen Berechtigungen in jeder Sicherheitsgruppe erkunden.

Berechtigungen sind auch auf der Seite **Benutzer** verfügbar. Der Infoboxbereich zeigt die **Berechtigungssätze aus Sicherheitsgruppen** und **Sicherheitsgruppenmitgliedschaften** für den ausgewählten Benutzer.

## Sicherheitsgruppen und Benutzergruppen

> [!NOTE]
> Benutzergruppen werden in einer zukünftigen Version nicht mehr verfügbar sein.

Sicherheitsgruppen ähneln sehr den derzeit verfügbaren Benutzergruppen. Benutzergruppen sind jedoch nur für [!INCLUDE [prod_short](includes/prod_short.md)] relevant. Sicherheitsgruppen basieren auf Gruppen in Microsoft Entra-ID oder Windows Active Directory, je nachdem, ob Sie [!INCLUDE [prod_short](includes/prod_short.md)] online oder lokal verwenden. Administrierende profitieren von Gruppen, da sie sie mit anderen Dynamics 365-Apps verwenden können. Wenn Vertriebsmitarbeiter beispielsweise [!INCLUDE [prod_short](includes/prod_short.md)] und SharePoint verwenden, müssen Administratoren die Gruppe und ihre Mitglieder nicht neu erstellen.

### Optional: Benutzergruppen in Berechtigungssätze konvertieren

Im 1. Veröffentlichungszyklus 2023 und höher können Sie Benutzergruppen in Berechtigungssätze in Ihrem Mandanten konvertieren. Die Berechtigungssätze bieten die gleiche Funktionalität wie Benutzergruppen. Beispiele:

* Sie können die Infobox **Benutzende** zum Verwalten von Berechtigungen für Benutzende verwenden.
* Sie können einen Drilldown zum Namen des Berechtigungssatzes durchführen, um dem Satz, an dem Sie arbeiten, weitere Berechtigungssätze hinzuzufügen. Um mehr zu erfahren, gehen Sie zu [Weitere Berechtigungssätze hinzufügen](ui-define-granular-permissions.md#to-add-other-permission-sets).

Benutzen Sie die Anleitung zur unterstützten Einrichtung der **Benutzergruppenmigration**, um ihre Gruppen zu konvertieren. Um die Anleitung zu starten, suchen Sie auf der Seite **Funktionsverwaltung** **Funktion: Benutzergruppenberechtigungen konvertieren** und wählen Sie dann aus **Alle Benutzer** im Feld **Aktiviert für** aus. Die unterstützte Einrichtungsanleitung bietet die folgenden Optionen für die Konvertierung.

|Option  |Beschreibung  |
|---------|---------|
|Benutzer zuweisen     | Weisen Sie die Berechtigungen in Benutzergruppen direkt den Benutzern zu, die der Gruppe zugewiesen wurden und entfernen Sie die Zuweisung zur Benutzergruppe.        |
|In einen Berechtigungssatz konvertieren     | Erstellen Sie eine neue Berechtigung für die Berechtigungen in jeder Benutzergruppe. Der neue Berechtigungssatz wird allen Mitgliedern jeder Benutzergruppe zugewiesen.          |

### Lizenzkonfigurationen gelten weiterhin

Sie können Berechtigungen in [!INCLUDE [prod_short](includes/prod_short.md)] basierend auf Lizenzen konfigurieren. Diese Berechtigungen werden neuen Benutzenden direkt zugewiesen. Diese Konfigurationen gelten weiterhin, auch wenn Sie beginnen, Sicherheitsgruppen zu verwenden.

Um ausschließlich Sicherheitsgruppen zu verwenden, sollten Sie die Lizenzkonfigurationen entfernen. Weitere Informationen zu Lizenzkonfigurationen finden Sie unter [Benutzende gemäß Lizenzen erstellen](ui-how-users-permissions.md).

Sie können Lizenzkonfigurationen auf der Seite **Lizenzkonfiguration** entfernen. Wählen Sie eine Lizenz aus und löschen Sie dann alle ihr zugewiesenen Berechtigungssätze.

## Siehe auch

[Benutzende gemäß Lizenzen erstellen](ui-how-users-permissions.md)  
[Zugriff auf Business Central in Teams mit Microsoft 365-Lizenzen festlegen](admin-access-with-m365-license-setup.md)  
[Erfahren Sie mehr über Gruppen und Zugriffsrechte in Microsoft Entra-ID](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Microsoft Entra Sicherheitsgruppen](/windows-server/identity/ad-ds/manage/understand-security-groups)  
