---
title: Verwalten der OneDrive Integration mit Business Central
description: Erfahren Sie, wie Sie eine Integration zwischen Business Central und OneDrive for Business verwalten können.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 05/12/2021
ms.author: bholtorf
ms.openlocfilehash: 5debd01f9d26e5e1dc1abc1a0123073d0f7ee234
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8382871"
---
# <a name="managing-onedrive-integration-with-business-central"></a>Verwalten der OneDrive Integration mit Business Central 
Dieser Artikel gibt einen Überblick darüber, was ein Administrator tun kann, um die OneDrive for Business Integration mit [!INCLUDE[prod_short](includes/prod_short.md)] zu steuern. [!INCLUDE[prod_short](includes/prod_short.md)]-Online-Kunden profitieren von der automatischen Integration, ohne dass eine zusätzliche Einrichtung erforderlich ist, um diese Funktionen zu nutzen. 

## <a name="minimum-requirements"></a>Mindestanforderungen

* Jeder Benutzer muss über eine Lizenz für [!INCLUDE[prod_short](includes/prod_short.md)] und OneDrive als Teil eines Microsoft 365-Plans verfügen.
* OneDrive muss für jeden Benutzer festgelegt werden.

## <a name="governance"></a>Governance
Das Admin Center von SharePoint bietet umfassende Steuerelemente für Richtlinien, die die Nutzung von OneDrive im gesamten Unternehmen regeln. Globale Admins oder Benutzer mit der Admin-Rolle SharePoint können Richtlinien festlegen, die bestimmen, wer auf OneDrive zugreifen darf, wo sich die Daten befinden, den Lebenszyklus der Inhalte und vieles mehr. Unter den folgenden Links finden Sie Informationen zu häufig verwendeten Funktionen und Einstellungen, die Ihre Integration mit [!INCLUDE[prod_short](includes/prod_short.md)] verbessern können. 

* [Verwaltung der Freigabeeinstellungen](/sharepoint/turn-external-sharing-on-or-off)
* [Nutzen Sie Informationsbarrieren mit SharePoint](/sharepoint/information-barriers)
* [Erfahren Sie mehr über die Verhinderung von Datenverlust](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Festlegen des Standardspeicherplatzes für OneDrive-Benutzer](/onedrive/set-default-storage-space)
* [Admins für OneDrive-Benutzer hinzufügen und entfernen](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Deaktivieren Sie die Erstellung von OneDrive für einige Benutzer](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Multi-Geo Funktionalitäten in OneDrive und SharePoint Online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Einige Funktionen können nur für bestimmte Pläne verfügbar sein.

## <a name="managing-privacy"></a>Datenschutz verwalten
Administratoren und Endbenutzer haben das Steuerelement für die in OneDrive gespeicherten Inhalte, und diese Daten sind das alleinige Eigentum Ihrer Organisation. Weitere Informationen finden Sie unter [Wie SharePoint und OneDrive Ihre Daten in der Cloud schützen](/sharepoint/safeguarding-your-data). Sie können auch unsere [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/en-us/privacystatement) besuchen, in der erklärt wird, welche Daten Microsoft verarbeitet, wie Microsoft sie verarbeitet und zu welchem Zweck.

## <a name="restoring-onedrive-and-prod_short"></a>Wiederherstellung von OneDrive und [!INCLUDE[prod_short](includes/prod_short.md)]
Im Rahmen einer Disaster Recovery-Übung müssen Administratoren möglicherweise eine [!INCLUDE[prod_short](includes/prod_short.md)]-Umgebung auf ein Backup aus der Vergangenheit wiederherstellen und den OneDrive-Speicher mit demselben Zeitpunkt synchronisieren. OneDrive bietet hierfür verschiedene Tools, wie z.B. die Wiederherstellung der OneDrive eines Benutzers zu einem früheren Zeitpunkt, die Wiederherstellung einer früheren Version einer einzelnen Datei oder die Wiederherstellung gelöschter Dateien. Weitere Informationen finden Sie in den folgenden Artikeln:

* Zu [!INCLUDE[prod_short](includes/prod_short.md)], siehe [Wiederherstellen einer Umgebung im Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Für OneDrive, siehe [Wiederherstellen Ihrer OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Konfigurieren von Business Central On-Premises

Ein Administrator muss die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] on-premises und OneDrive festlegen. Anders als bei [!INCLUDE[prod_short](includes/prod_short.md)] online, ist die Verbindung nicht automatisch. Wenn die Verbindung nicht konfiguriert ist, können die Benutzer die Funktionen für OneDrive nicht nutzen. 

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises kann nur mit OneDrive verbunden werden, das von Microsoft in der Cloud gehostet wird. Die Verbindung von [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort mit dem Meine Sites Repository von Server SharePoint wird nicht unterstützt.

> [!IMPORTANT]
> Wenn Sie diese Funktion konfigurieren, aktivieren Sie auch veraltete Funktionen, die Dateien an OneDrive senden.  
>
>* Die Funktion In Excel öffnen kopiert die Excel-Datei automatisch auf OneDrive und öffnet sie dann in Excel Online. 
>* Wenn Sie einen Bericht in eine Datei exportieren, wird die Datei automatisch nach OneDrive kopiert und anschließend in Excel Online, Word Online oder OneDrive geöffnet. 
>* Andere Funktionen können ebenfalls automatisch in OneDrive geöffnet werden.

### <a name="to-prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>So bereiten Sie [!INCLUDE[prod_short](includes/prod_short.md)] on-premises für die Verbindung mit OneDrive vor

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Fügen Sie eine registrierte Anwendung für Business Central in Ihrem Azure AD-Mandanten Ihres Microsoft 365-Plans hinzu. Wie andere Azure-Dienste, die mit Business Central arbeiten, erfordert auch OneDrive eine App-Registrierung in Azure Active Directory (Azure AD). Die App-Registrierung stellt Authentifizierungs- und Autorisierungsdienste zwischen Business Central und SharePoint bereit, die von OneDrive genutzt werden.

Konfigurieren Sie die registrierte Anwendung mit den folgenden delegierten Berechtigungen für die API von SharePoint:

- AllSites.Write
- MyFiles.Write
- User.Read.All 

Diese Arbeit führen Sie im Azure-Portal aus. Achten Sie darauf, die Anwendungs-(Client-)ID und das Client-Geheimnis zu kopieren, die von der registrierten Anwendung verwendet werden. Sie benötigen diese Informationen in der nächsten Aufgabe.

Weitere Informationen über die Registrierung einer Anwendung und die Konfiguration von Berechtigungen finden Sie unter [Registrieren einer Anwendung in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) in der Hilfe für Entwickler und IT-Profis.

> [!TIP]
> Wenn Sie bereits eine Anwendung als Teil einer Integration mit einem anderen Microsoft-Produkt registriert haben, wie z.B. in Power BI, dann können Sie diese App-Registrierung wiederverwenden. In diesem Fall müssen Sie nur die Berechtigungen für SharePoint festlegen.

### <a name="to-set-up-the-connection-in-prod_short-on-premises"></a>Um die Verbindung in [!INCLUDE[prod_short](includes/prod_short.md)] on-premises festzulegen

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Microsoft SharePoint Verbindungseinrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Geben Sie in das Feld **Beschreibung** eine Beschreibung für die Verbindung ein, z.B. **OneDrive**.
3. Geben Sie in das Feld **Ordner** **Business Central** ein.
4. Geben Sie in das Feld **Lagerort** die URL für Ihre OneDrive ein.

    Die URL für eine OneDrive hat normalerweise das folgende Format: `https://<tenant name>-my.sharepoint.com`. Weitere Informationen finden Sie unter [OneDrive-URLs für Benutzer in Ihrer Organisation](/onedrive/list-onedrive-urls) in der OneDrive-Dokumentation.
5. Geben Sie in das Feld **Client ID** die Client ID aus Ihrer Anwendungsregistrierung ein.
6. In das Feld **Geheimnis des Clients** geben Sie das Geheimnis aus Ihrer Anwendungsregistrierung ein. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> Die Seite SharePoint-Verbindungseinrichtung dient der Konfiguration mehrerer veralteter Funktionen. Der Abschnitt **Allgemein** konfiguriert die Verbindung zu OneDrive, und der Abschnitt **Gemeinsame Dokumente** leitet die Dateien stattdessen zu SharePoint um. Die veraltete Funktion SharePoint wird in naher Zukunft veraltet sein. Wir empfehlen Ihnen, den Bereich **Gemeinsame Belege** nicht zu konfigurieren.

## <a name="see-also"></a>Weitere Informationen
[Business Central und OneDrive für Business Integration](across-onedrive-overview.md)  
[Öffnen von Business Central Dateien in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)

