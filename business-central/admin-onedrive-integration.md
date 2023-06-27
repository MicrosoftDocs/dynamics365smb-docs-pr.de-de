---
title: Verwalten der OneDrive Integration mit Business Central
description: 'Erfahren Sie, wie Sie eine Integration zwischen Business Central und OneDrive for Business verwalten können.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 02/28/2022
ms.author: jswymer
---
# <a name="managing-onedrive-integration-with-business-central"></a>Verwalten der OneDrive Integration mit Business Central

Dieser Artikel gibt einen Überblick darüber, was ein Administrator tun kann, um die OneDrive for Business Integration mit [!INCLUDE[prod_short](includes/prod_short.md)] zu steuern. [!INCLUDE[prod_short](includes/prod_short.md)] Online-Kunden profitieren von der automatischen Integration ohne zusätzliche Einrichtung, um die Funktionen Öffnen und Freigeben in OneDrive zu nutzen. Mit der Anleitung zur unterstützten Einrichtung von **OneDrive** können Sie den Benutzern Zugriff auf noch mehr Funktionen von OneDrive geben, z.B. das Öffnen von Excel-Dateien in OneDrive&mdash;oder sogar alle Funktionen ausschalten.  

## <a name="configure-onedrive-for-integration-with-business-central"></a>Konfigurieren Sie OneDrive für die Integration mit Business Central

In diesem Abschnitt werden die Anforderungen erläutert, die in OneDrive for Business erfüllt sein müssen, um die Integration mit Business Central zu konfigurieren, sowie die Aufgaben, die Sie zur Verwaltung der Integration durchführen können.

### <a name="minimum-requirements"></a>Mindestanforderungen

* Jeder Benutzer muss über eine Lizenz für [!INCLUDE[prod_short](includes/prod_short.md)] und OneDrive als Teil eines Microsoft 365-Plans verfügen.
* OneDrive muss für jeden Benutzer festgelegt werden.

### <a name="managing-privacy"></a>Datenschutz verwalten

> [!IMPORTANT]
> Wenn Sie sich dafür entschieden haben, Business Central und OneDrive in verschiedenen Ländern oder Regionen bereitzustellen, können die von Business Central erzeugten und in OneDrive abgelegten Dateien die Grenzen der Datenresidenz überschreiten. Vergewissern Sie sich, dass die Richtlinien Ihres Unternehmens und die gesetzlichen Anforderungen an die Datenaufbewahrung erfüllt sind, bevor Sie die Verbindung zu OneDrive aktivieren.

Administratoren und Endbenutzer haben das Steuerelement für die in OneDrive gespeicherten Inhalte, und diese Daten sind das alleinige Eigentum Ihrer Organisation. Weitere Informationen finden Sie unter [Wie SharePoint und OneDrive Ihre Daten in der Cloud schützen](/sharepoint/safeguarding-your-data). Sie können auch unsere [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/en-us/privacystatement) besuchen, in der erklärt wird, welche Daten Microsoft verarbeitet, wie Microsoft sie verarbeitet und zu welchem Zweck.

Mit der Aktivierung dieser Service-Verbindung erklären Sie sich einverstanden:

(a) der Weitergabe von Daten aus Dynamics 365 Business Central an den Dienstanbieter, der diese gemäß seinen Bedingungen und Richtlinien zum Schutz der Privatsphäre verwenden wird; (b) die Compliance-Stufen des Dienstanbieters können sich von Dynamics 365 Business Central unterscheiden; und (c) Microsoft kann Ihre Kontaktinformationen an diesen Dienstanbieter weitergeben, wenn dies für den Vorgang und die Problembehandlung des Dienstes erforderlich ist.

## <a name="configure-business-central"></a>Business Central konfigurieren

Wenn Business Central online ist, wird die Verbindung zwischen Business Central und OneDrive automatisch für Sie konfiguriert, und die Funktionen von OneDrive stehen den Benutzern standardmäßig zur Verfügung. Wenn Sie einige oder alle Funktionen deaktivieren möchten, können Sie die Anleitung zur **OneDrive Einrichtung** im Business Central Client verwenden.

Die Konfiguration von Business Central vor Ort ist anders, weil die Verbindung zwischen Business Central und OneDrive nicht für Sie konfiguriert wird. Sie müssen dies manuell tun. Weitere Informationen finden Sie unter [Konfiguration der Integration von OneDrive mit Business Central vor Ort](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a>Über mehrere Umgebungen

Die OneDrive Integration wird pro Umgebung konfiguriert, d.h. Ihre Einstellungen gelten für alle Firmen in dieser Umgebung. Wenn Ihr Unternehmen mehr als eine Umgebung hat, müssen Sie für jede Umgebung OneDrive Integration konfigurieren.

### <a name="prerequisites"></a>Voraussetzungen

- Berechtigung zum Einfügen, Bearbeiten und Löschen (imd) in der Tabelle **Dokumentenservice-Szenario** als Minimum

### <a name="configure-onedrive-using-onedrive-setup"></a>Konfigurieren Sie OneDrive über die Einrichtung OneDrive

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **OneDrive Einrichtung** ein und wählen Sie dann den entsprechenden Link. 
2. Wenn Sie die Unterstützte Einrichtung zum ersten Mal ausführen, sehen Sie die Seite **Ihre Privatsphäre**. Lesen Sie die Informationen auf der Seite, und wenn Sie mit den Bedingungen einverstanden sind, wählen Sie **Zustimmen**, um fortzufahren.
3. Auf der Seite **Dateiverarbeitung konfigurieren** haben Sie folgende Optionen zur Auswahl:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Wählen Sie **Weiter**>**Erledigt**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a>Umschalten auf die neue OneDrive Integration nach dem Upgrade

Die **OneDrive-Einrichtung** wurde mit der Veröffentlichungswelle 2, Version 21.0, im Jahr 2022 eingeführt. Zuvor verwendete die OneDrive-Integration die **SharePoint-Verbindungseinrichtung**, die außer Betrieb genommen wurde und in 2023 Veröffentlichungswelle 2, Version 23.0, entfernt wird. Nachdem Sie auf Version 21 aktualisiert haben, funktioniert OneDrive noch wie bisher. Wir empfehlen Ihnen jedoch, auf die neue OneDrive-Integration umzusteigen. Wenn Sie diese Umstellung jetzt vornehmen, wird es einfacher, wenn die **SharePoint Einrichtung** irgendwann entfernt wird. Außerdem können Sie dann die Anleitung zur unterstützten Einrichtung der **OneDrive Einrichtung** verwenden, um die OneDrive Funktionen zu verwalten, auf die die Benutzer Zugriff haben. Die **OneDrive Einrichtung** macht den Übergang von der veralteten SharePoint Einrichtung einfach und nahtlos.

Um zu wechseln, öffnen Sie einfach die **OneDrive Einrichtung** und führen Sie sie direkt aus, oder öffnen Sie die Seite **SharePoint Verbindungseinrichtung** und wählen Sie **Zur neuen OneDrive Einrichtung gehen** in der Benachrichtigung am oberen Rand der Seite. Folgen Sie der Anleitung zur Einrichtung wie im vorherigen Abschnitt beschrieben.

## <a name="restoring-onedrive-and-"></a>Wiederherstellung von OneDrive und [!INCLUDE[prod_short](includes/prod_short.md)]

Im Rahmen einer Disaster Recovery-Übung müssen Administratoren möglicherweise eine [!INCLUDE[prod_short](includes/prod_short.md)]-Online-Umgebung mit einem Backup aus der Vergangenheit wiederherstellen und den OneDrive-Speicher mit demselben Zeitpunkt synchronisieren. OneDrive bietet verschiedene Tools zur Wiederherstellung, z.B. die Wiederherstellung von OneDrive eines Benutzers zu einem früheren Zeitpunkt, die Wiederherstellung einer früheren Version einer einzelnen Datei oder die Wiederherstellung gelöschter Dateien. Weitere Informationen finden Sie in den folgenden Artikeln:

* Zu [!INCLUDE[prod_short](includes/prod_short.md)], siehe [Wiederherstellen einer Umgebung im Admin Center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Für OneDrive, siehe [Wiederherstellen Ihrer OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

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

## <a name="see-also"></a>Siehe auch

[Business Central und OneDrive für Business Integration](across-onedrive-overview.md)  
[Öffnen von Business Central Dateien in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
