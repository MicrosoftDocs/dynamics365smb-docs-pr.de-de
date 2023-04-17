---
title: Kontaktsynchronisierung mit Outlook für Business Central lokal einrichten
description: 'Erfahren Sie, wie Sie eine lokale Business Central-Umgebung, um Kontakte in Business Central und Outlook zu synchronisieren.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/04/2023
ms.custom: bap-template
---

# Kontaktsynchronisierung mit Outlook für Business Central lokal einrichten

In diesem Artikel erfahren Sie, wie Sie [!INCLUDE[prod_short](includes/prod_short.md)] lokal einrichten, um Kontakte in [!INCLUDE[prod_short](includes/prod_short.md)] mit Kontakten in Outlook zu synchronisieren. Weitere Informationen zu diesem Feature finden Sie unter [Synchronisieren Sie Kontakte in Business Central mit Kontakten in Microsoft Outlook](admin-synchronize-outlook-contacts.md).

## Einführung

Die Kontaktsynchronisierung erfordert die Verwendung des OAuth-2.0-Protokolls für die Authentifizierung mit Exchange Online. Bisher wurde auch die Standardauthentifizierung unterstützt, sie ist jedoch veraltet und wird im Rahmen von Exchange Online nicht mehr unterstützt. Weitere Informationen zur Einstellung finden Sie unter [Einstellung der Standardauthentifizierung in Exchange Online](/exchange/clients-and-mobile-in-exchange-online/deprecation-of-basic-authentication-exchange-online). Diese Änderung bedeutet, dass die Kontaktsynchronisierung in Business Central in Ihrer lokalen Umgebung möglicherweise nicht mehr funktioniert. In diesem Artikel wird erklärt, wie Sie sie wieder zum Laufen bringen.

## Voraussetzungen

- Exchange Online, entweder als eigenständige Version oder über den Microsoft 365 Plan  
- Zugriff auf den Azure Active Directory-Mandanten (Azure AD), der von Exchange Online verwendet wird
- [!INCLUDE[prod_short](includes/prod_short.md)] Benutzende haben ein Microsoft 365- oder Exchange Online-E-Mail-Konto, das ihren Konten in [!INCLUDE[prod_short](includes/prod_short.md)] zugewiesen ist. Sie können diese Einstellung im Abschnitt **Microsoft 365-Authentifizierung** des Benutzerprofils in der Liste **Benutzende** überprüfen. 

## Die Kontaktsynchronisierung einrichten

Führen Sie die folgenden Schritte aus, um die Kontaktsynchronisierung einzurichten. Wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] Frühling 2019 (v.14) ausführen, müssen Sie einen zusätzlichen Schritt ausführen, der entweder den Anwendungscode ändert oder eine Verbindung zu Power BI herstellt.

1. <a name="registerapp"></a>Registrieren Sie eine App für die Exchange Online-API in Ihrem Azure AD-Mandanten.

   In diesem Schritt fügen Sie eine registrierte App im Azure AD-Mandanten Ihres Microsoft 365- oder Exchange Online-Plans ein. Wie andere Azure-Dienste, die mit Business Central zusammenarbeiten, erfordert auch Exchange Online eine registrierte App in Azure AD. Die registrierte App stellt Authentifizierungs- und Autorisierungsdienste zwischen Business Central und Exchange Online zur Verfügung.

   Befolgen Sie die detaillierten Anweisungen in der Entwickler- und IT-Profihilfe unter [Registrieren Sie eine Anwendung in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). Beachten Sie, während Sie die Anweisungen durcharbeiten, die folgenden Punkte:

   - Wenn Sie eine Anwendung bereits als Teil einer Integration mit einem anderen Microsoft-Produkt registriert haben, wie z. B. in Power BI, dann verwenden Sie diese registrierte App wieder. In diesem Fall müssen Sie einfach nur die App mit den im nächsten Punkt beschriebenen Office 365 Exchange Online-Berechtigungen einrichten.

   - Konfigurieren Sie die registrierte App mit den folgenden delegierten Berechtigungen für die Office 365 Exchange Online-API:

     - Contacts.ReadWrite
     - EWS.AccessAsUser.All

2. Führen Sie für [!INCLUDE[prod_short](includes/prod_short.md)] Version 14 eine der folgenden Aufgaben aus:

   - Ändern Sie Seite 6700, indem Sie in der folgenden Codezeile im `OnPageOpen` Trigger `FALSE` auf `TRUE` ändern:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Erstellen Sie eine neue Seite mit dem folgenden Code für den OnPageOpen-Trigger:

     ```
     PasswordRequired := AzureADMgt.GetAccessToken(AzureADMgt.GetO365Resource,AzureADMgt.GetO365ResourceName,TRUE) = '';
     ```

   - Richten Sie Power BI ein, indem Sie die Anweisungen unter [Business Central lokal für die Power BI-Integration einrichten](admin-powerbi-setup.md#setup)befolgen.

   Nachdem die von Ihnen gewählte Lösung vorhanden ist, bitten Sie die Benutzende, entweder die neue/geänderte Seite auszuführen oder [eine Verbindung zu Power BI](across-working-with-powerbi.md#connect) herzustellen. Sie müssen diesen Schritt nur einmal ausführen.

## Nächste Schritte

[Synchronisieren Sie Kontakte in Business Central mit Kontakten in Microsoft Outlook](admin-synchronize-outlook-contacts.md)  
