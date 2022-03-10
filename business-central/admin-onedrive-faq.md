---
title: OneDrive für Business FAQ
description: Erhalten Sie Antworten auf einige typische Fragen zur Arbeit mit OneDrive for Business und Business Central.
author: bholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, integration, share, browser
ms.date: 05/19/2021
ms.author: bholtorf
ms.openlocfilehash: f54e8b6290e9dd653180b3ea05246255b84dc2ae
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144050"
---
# <a name="onedrive-for-business-faq"></a>OneDrive für Business FAQ

[!INCLUDE [online_only](includes/online_only.md)]

Dieser Artikel beantwortet einige der Fragen, die Sie zur Arbeit mit OneDrive und [!INCLUDE [prod_short](includes/prod_short.md)] haben könnten.

## <a name="does-this-work-with-all-prod_short-clients"></a>Funktioniert dies mit allen [!INCLUDE[prod_short](includes/prod_short.md)]-Clients?

Ja. Sie können Dateien in OneDrive von den [!INCLUDE[prod_short](includes/prod_short.md)] Mobile-Apps aus öffnen, wenn Sie Kartendetails in Microsoft Teams ansehen, oder sogar vom Outlook Add-in aus.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>Ist OneDrive zum Speichern von Dateien dasselbe wie SharePoint?

Als Teil Ihres Microsoft 365-Abonnements stellt Ihnen Ihr Unternehmen OneDrive zur Verfügung, Ihren Dateispeicher in der Cloud. OneDrive ist standardmäßig ein privater Speicher, in dem Sie Ihre Inhalte organisieren und auswählen, welche Dateien oder Ordner Sie mit wem teilen möchten. SharePoint hingegen bietet einen Dateispeicher in der Cloud, der mit anderen in Ihrem Unternehmen geteilt wird.  

## <a name="does-prod_short-support-consumer-onedrive"></a>Unterstützt [!INCLUDE[prod_short](includes/prod_short.md)] den Verbraucher OneDrive?

Anzahl Diese Integration ist ausschließlich für OneDrive for Business gedacht und unterstützt nur Ihr Arbeitskonto. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Werden alle OneDrive for Business-Pakete unterstützt?

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt keine eigenständigen Pläne für OneDrive for Business. OneDrive muss als Teil eines Microsoft 365 Business- oder Enterprise-Plans gekauft werden. Weitere Informationen finden Sie unter [Vergleich der Preise und Pläne für OneDrive Cloud-Speicher](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Wo kann ich den Dienststatus von OneDrive einsehen?

Administratoren können im Microsoft 365 Admin Center auf das Dashboard zum Dienststatus zugreifen. Das Dashboard zeigt die Verfügbarkeit des Dienstes OneDrive an. 
 
## <a name="is-onedrive-integration-available-to-prod_short-on-premises"></a>Ist die Integration von OneDrive auch für [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort verfügbar?

Ja, aber im Gegensatz zu [!INCLUDE[prod_short](includes/prod_short.md)] online ist dafür eine zusätzliche Einrichtung erforderlich. Weitere Informationen finden Sie unter [Konfiguration von Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).  

## <a name="does-prod_short-on-premises-connect-with-sharepoint-server"></a>Lässt sich [!INCLUDE[prod_short](includes/prod_short.md)] on-premises mit SharePoint Server verbinden?

Anzahl Diese Bereitstellungskombination wird nicht unterstützt, auch wenn SharePoint Server Meine Sites aktiviert hat.  

## <a name="does-prod_short-online-connect-with-sharepoint-server"></a>Stellt [!INCLUDE[prod_short](includes/prod_short.md)] online eine Verbindung zu SharePoint Server her?

Anzahl Diese Bereitstellungskombination wird nicht unterstützt, auch wenn SharePoint Server Meine Sites aktiviert hat.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Wie funktioniert dies in einem Unternehmen mit mehreren Umgebungen?

Die Integration geht davon aus, dass die Namen der Firmen in den Umgebungen von [!INCLUDE[prod_short](includes/prod_short.md)] eindeutig sind. Wenn die Namen der Firmen innerhalb des Unternehmens eindeutig sind, wird beim Öffnen einer Datei in OneDrive die Datei in einen Ordner kopiert, der nach der aktuellen Firma benannt ist. Wenn Firmennamen in verschiedenen Umgebungen nicht eindeutig sind, werden Dateien mit identischen Firmennamen zusammen im selben Ordner abgelegt.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Wir haben den Namen unserer Firma geändert. Was passiert mit meinen früheren Dateien?

Mit [!INCLUDE[prod_short](includes/prod_short.md)] werden Dateien, die Sie zuvor mit OneDrive geöffnet haben, nicht automatisch in den neuen Ordner migriert. Nach der Umbenennung Ihrer Firma kopiert die Aktion Öffnen in OneDrive die Dateien in einen Ordner, der den neuen Namen der Firma trägt.   

## <a name="when-attaching-files-to-prod_short-how-do-i-pick-a-file-from-onedrive"></a>Wie kann ich beim Anhängen von Dateien an [!INCLUDE[prod_short](includes/prod_short.md)] eine Datei aus OneDrive kommissionieren? 
[!INCLUDE[prod_short](includes/prod_short.md)] verfügt nicht über eine Cloud-Dateiauswahl. Sie müssen die Datei von OneDrive auf Ihr Gerät herunterladen und sie dann auf [!INCLUDE[prod_short](includes/prod_short.md)] hochladen. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Ich möchte stattdessen Dateien in SharePoint öffnen. Wie kann ich das tun?

[!INCLUDE[prod_short](includes/prod_short.md)] bietet keine Funktionen zum Kopieren von Dateien nach SharePoint und zum Öffnen von Dateien aus einer SharePoint-Bibliothek. Wenden Sie sich an Ihren Microsoft-Partner, um Ihre Möglichkeiten zu verstehen, oder suchen Sie nach Apps in AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Wie kann ich die Integration in OneDrive deaktivieren?

[!INCLUDE[prod_short](includes/prod_short.md)] bietet online keine Möglichkeit, die Integration in OneDrive zu aktivieren oder zu deaktivieren.  

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Soll ich die Seite für die Einrichtung der Verbindung zu SharePoint verwenden, um eine Verbindung zu SharePoint herzustellen?

Dies ist eine veraltete Funktion, bei der alle [!INCLUDE[prod_short](includes/prod_short.md)]-Dateien von allen Benutzern an einen einzigen SharePoint-Ordner gesendet werden. Wir empfehlen Ihnen, das Inforegister für gemeinsame Belege nicht auf der Seite Einrichtung der Verbindung SharePoint zu konfigurieren, da wir daran arbeiten, diese Funktion außer Betrieb zu nehmen.  

## <a name="which-version-of-prod_short-supports-onedrive"></a>Welche Version von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt OneDrive?

Die Integration mit OneDrive wurde 2021 im Veröffentlichungszyklus 2 verfügbar.  

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Wird Microsoft die Integration in OneDrive weiter verbessern?

Bei Microsoft achten wir stets auf das Feedback aus unsere breitgefächerte Benutzer-Community und reagieren auf die häufigsten Vorschläge. Um zu erfahren, was als nächstes für Integrationen mit Microsoft 365-Apps geplant ist, lesen Sie den [Dynamics 365 Veröffentlichungsplan](/dynamics365-release-plan/2021wave1).  

Wenn Sie sich an der Verbesserung der OneDrive-Integration beteiligen möchten oder eine Idee haben, die die gemeinsame Nutzung von Dateien und die Zusammenarbeit in [!INCLUDE[prod_short](includes/prod_short.md)] verbessern würde, fügen Sie eine Idee hinzu oder stimmen Sie für bestehende Ideen unter [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas) ab.

## <a name="troubleshooting"></a>Problembehebung

Dieser Abschnitt enthält Informationen darüber, wie Sie Probleme, die bei der Verwendung von OneDrive mit [!INCLUDE[prod_short](includes/prod_short.md)] auftreten können, erkennen und beheben können.  

### <a name="i-have-to-sign-in-each-time-i-open-a-file"></a>Ich muss mich jedes Mal anmelden, wenn ich eine Datei öffne

Tut uns leid, das ist ein bekanntes Problem, an dem wir arbeiten. Wir gehen davon aus, dass wir in einem der nächsten Updates für ein reibungsloseres Erlebnis sorgen werden.  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central kann meine OneDrive nicht finden

Wenn diese Nachricht angezeigt wird, „Der Lagerort Ihrer OneDrive für Business konnte nicht festgelegt werden, wenden Sie sich an Ihren Partner, um dies einzurichten.“, überprüfen Sie, ob der Benutzer mindestens einmal auf seine OneDrive zugegriffen hat. Ist dies nicht der Fall, bitten Sie die Person, die Einrichtung unter portal.office.com/onedrive vorzunehmen. Das kann eine Weile dauern. Wenn die Nachricht auch nach 24 Stunden noch angezeigt wird, wenden Sie sich an den Support.  
 

## <a name="see-also"></a>Weitere Informationen
[Business Central und OneDrive Integration](across-onedrive-overview.md)  
[Verwaltung der OneDrive Integration mit Business Central](admin-onedrive-integration.md)  
[Öffnen von Business Central Dateien in OneDrive](across-share-onedrive.md)  
