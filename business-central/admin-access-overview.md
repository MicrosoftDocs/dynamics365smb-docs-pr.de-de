---
title: Zugriff auf Business Central verwalten
description: Administrierende steuern den Zugriff auf Business Central und seine Funktionen mit einem mehrstufigen Ansatz.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Zugriff auf Business Central verwalten

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Dieser Artikel gibt Administrierenden und Anwendungsentwickelnden einen allgemeinen Überblick darüber, wie sie den Zugriff auf [!INCLUDE [prod_short](includes/prod_short.md)] und seine Funktionen steuern können. Verwenden Sie die Links, um zu anderen Artikeln mit weiteren Einzelheiten zu den Themen zu gelangen.

## Mehrstufigen Zugriff

[!INCLUDE [prod_short](includes/prod_short.md)] verwendet einen mehrstufigen Ansatz für die Anwendungssicherheit, wie im folgenden Diagramm dargestellt. Um mehr über die einzelnen Stufen zu erfahren, gehen Sie zu [Anwendungssicherheit in Business Central](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Mehrstufige Anwendungssicherheit in Business Central.":::

## Lizenzen

Weisen Sie [!INCLUDE [prod_short](includes/prod_short.md)]-Benutzenden eine **Dynamics 365 Business Central**-Lizenz zu, sodass sie ihre Geschäftsdaten von jeder Benutzeroberfläche aus anzeigen, ändern und bearbeiten können. Weitere Informationen zu Lizenzen finden Sie unter [Lizenzierung in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).

Personen, die gelegentlich Lesezugriff auf Informationen in [!INCLUDE [prod_short](includes/prod_short.md)] benötigen, können jedoch eine **Microsoft 365**-Lizenz verwenden. Um mehr über die Erteilung eines eingeschränkten Zugriffs zu erfahren, gehen Sie zu [Business Central-Zugriff mit Microsoft 365-Lizenzen](admin-access-with-m365-license.md).

Um umfassendere Informationen zu den verschiedenen Lizenztypen und zur Funktionsweise der Lizenzierung in [!INCLUDE[prod_short](includes/prod_short.md)] zu erhalten, [laden Sie das Dynamics 365-Lizenzierungshandbuch](https://go.microsoft.com/fwlink/?LinkId=866544) herunter.

## Administratorenaufgaben in Business Central

In der folgenden Tabelle ist aufgeführt, wie Administrierende den Zugriff auf [!INCLUDE [prod_short](includes/prod_short.md)] steuern können und welche Funktionen die Benutzenden verwenden werden. Einige der Aufgaben helfen auch dabei, die Zugriffseinstellungen auf dem neuesten Stand zu halten.

|Aufgabe| Weitere Informationen |
|--|--|--|
|Jede Person muss über ein Benutzerkonto verfügen, bevor sie sich bei [!INCLUDE [prod_short](includes/prod_short.md)] anmelden kann. Am einfachsten richten Sie Benutzende ein, indem Sie sie einzeln im [Microsoft 365 Admin Center](https://go.microsoft.com/fwlink/p/?linkid=2024339) hinzufügen. |[Benutzende hinzufügen und gleichzeitig Lizenzen zuweisen](/microsoft-365/admin/add-users/add-users)|
|Verwalten Sie den Zugriff für alle Benutzenden auf Umgebungsebene. Erstellen Sie eine Microsoft Entra-Sicherheitsgruppe und weisen Sie sie der Umgebung zu.<br><br> Sie können Sicherheitsgruppen auch verwenden, um den Zugriff für bestimmte Benutzergruppen zu verwalten. | [Zugriff auf Umgebungen verwalten](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Kontrollieren Sie den Zugriff auf Business Central mithilfe von Sicherheitsgruppen](ui-security-groups.md) |
|Erstellen Sie Benutzende in [!INCLUDE [prod_short](includes/prod_short.md)] und legen Sie fest, wer sich anmelden kann. | [Benutzende gemäß Lizenzen erstellen](ui-how-users-permissions.md) |
|Berechtigungen legen in Verbindung mit Benutzerlizenzen fest, auf welche Objekte ein Benutzender in jeder Datenbank oder Umgebung zugreifen kann. Legen Sie fest, ob Daten in den Datenbankobjekten gelesen, geändert oder eingegeben werden können. |[Benutzenden und Gruppen Berechtigungen zuweisen](ui-define-granular-permissions.md)|
|Wenn ein externer Buchhaltungsdienst Ihre Bücher und Finanzberichte verwaltet, laden Sie ihn zu Ihrem [!INCLUDE [prod_short](includes/prod_short.md)] ein. Er kann bei Ihren Steuerdaten enger mit Ihnen zusammenarbeiten.|[Buchhalter-Erfahrung in [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Wenn Sie ein [!INCLUDE [prod_short](includes/prod_short.md)] Verkaufspartner sind, können Sie eine E-Mail an einen Kunden senden, um eine Verkaufsbeziehung anzufordern. Sie können delegierte Administrationsrechte für Microsoft Entra-ID und Microsoft 365 in die E-Mail aufnehmen.| [Delegierter Administratorzugriff auf Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|Ein Azure-Diensttag stellt eine Gruppe von IP-Adressen dar, von denen Datenverkehr für einen Dienst kommen oder an die er gehen kann. Verwenden Sie Diensttags, um Firewalls so einzurichten, dass Datenverkehr nur von bestimmten Diensten zugelassen wird. Mit dem **Dynamics365BusinessCentral**-Tag können Sie Firewall- und Netzwerksicherheitsgruppenregeln verwenden, um den Datenverkehr zu und von [!INCLUDE [prod_short](includes/prod_short.md)] einzuschränken.| [Azure-Sicherheitsdiensttags](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Bei Verwendung der Microsoft Entra-Authentifizierung mit [!INCLUDE [prod_short](includes/prod_short.md)] empfehlen wir Ihnen, die [Microsoft Entra-ID Multi-Factor Authentication (MFA)](/azure/active-directory/authentication/concept-mfa-howitworks) zu nutzen. MFA schützt außerdem den Zugriff auf die Anwendung und Daten.|[Multi-Factor Authentication für Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## Entwickleraufgaben in Business Central

Es gibt auch einen Entwicklerablauf zum Verwalten des Zugriffs auf [!INCLUDE [prod_short](includes/prod_short.md)]. Beispielsweise können Entwickelnde und Administrierende Anwendungen, die dem Unternehmen zugute kommen, erstellen und mit [!INCLUDE [prod_short](includes/prod_short.md)] verbinden:  

* Geschäftsprozesse optimieren
* Kundeninteraktionen verbessern
* Schneller bessere Entscheidungen treffen

Die folgende Tabelle enthält Links zu Informationen darüber, wie Sie Apps und Erweiterungen Zugriff auf [!INCLUDE [prod_short](includes/prod_short.md)] Daten gewähren.

| Aufgabe | Weitere Informationen |
|--|--|
|Die beiden Hauptkonzepte zum Definieren des Zugriffs auf Funktionen sind Berechtigungen und Rechte. Berechtigungen geben entsprechend der Lizenzen oder Microsoft Entra-Rollen umfassenden Zugriff auf Objekte. Mit Rechten und Berechtigungssätzen können Sie die Feinabstimmung für den Zugriff auf Objekte durchführen. |[Übersicht über Berechtigungen und Berechtigungssätze](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## Siehe auch

[Sicherheit in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)
