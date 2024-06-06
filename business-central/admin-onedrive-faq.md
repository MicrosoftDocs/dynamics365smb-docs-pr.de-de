---
title: OneDrive für Business FAQ
description: Erhalten Sie Antworten auf einige typische Fragen zur Arbeit mit OneDrive for Business und Business Central.
author: brentholtorf
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'OneDrive, integration, share, browser'
ms.date: 09/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="onedrive-for-business-faq"></a>OneDrive für Business FAQ

[!INCLUDE [online_only](includes/online_only.md)]

Dieser Artikel beantwortet einige der Fragen, die Sie zur Arbeit mit OneDrive und [!INCLUDE [prod_short](includes/prod_short.md)] haben könnten.

## <a name="does-this-work-with-all--clients"></a>Funktioniert dies mit allen [!INCLUDE[prod_short](includes/prod_short.md)]-Clients?

Ja. Sie können Dateien in OneDrive von den [!INCLUDE[prod_short](includes/prod_short.md)] Mobile-Apps aus öffnen, wenn Sie Kartendetails in Microsoft Teams ansehen, oder sogar vom Outlook Add-in aus.  

## <a name="is-onedrive-the-same-as-sharepoint-for-storing-files"></a>Ist OneDrive zum Speichern von Dateien dasselbe wie SharePoint?

Als Teil Ihres Microsoft 365-Abonnements stellt Ihnen Ihr Unternehmen OneDrive zur Verfügung, Ihren Dateispeicher in der Cloud. OneDrive ist standardmäßig ein privater Speicher, in dem Sie Ihre Inhalte organisieren und auswählen, welche Dateien oder Ordner Sie mit wem teilen möchten. SharePoint hingegen bietet einen Dateispeicher in der Cloud, der mit anderen in Ihrem Unternehmen geteilt wird.  

## <a name="does--support-consumer-onedrive"></a>Unterstützt [!INCLUDE[prod_short](includes/prod_short.md)] den Verbraucher OneDrive?

Anzahl Diese Integration ist ausschließlich für OneDrive for Business gedacht und unterstützt nur Ihr Arbeitskonto. 

## <a name="are-all-onedrive-for-business-plans-supported"></a>Werden alle OneDrive for Business-Pakete unterstützt?

[!INCLUDE[prod_short](includes/prod_short.md)] unterstützt keine eigenständigen Pläne für OneDrive for Business. OneDrive muss als Teil eines Microsoft 365 Business- oder Enterprise-Plans gekauft werden. Weitere Informationen finden Sie unter [Vergleich der Preise und Pläne für OneDrive Cloud-Speicher](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).  

## <a name="where-can-i-see-onedrive-service-health"></a>Wo kann ich den Dienststatus von OneDrive einsehen?

Administratoren können im Microsoft 365 Admin Center auf das Dashboard zum Dienststatus zugreifen. Das Dashboard zeigt die Verfügbarkeit des Dienstes OneDrive an. Gehen Sie zu [https://admin.microsoft.com/Adminportal/Home?#/servicehealth](https://admin.microsoft.com/Adminportal/Home?#/servicehealth).
 
## <a name="is-onedrive-integration-available-to--on-premises"></a>Ist die Integration von OneDrive auch für [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort verfügbar?

Ja, aber im Gegensatz zu [!INCLUDE[prod_short](includes/prod_short.md)] online, erfordert es mehr Einrichtung. Weitere Informationen finden Sie unter [Konfiguration von Business Central vor Ort](admin-onedrive-integration-onpremises.md).  

## <a name="does--on-premises-connect-with-sharepoint-server"></a>Lässt sich [!INCLUDE[prod_short](includes/prod_short.md)] on-premises mit SharePoint Server verbinden?

Anz. Diese Bereitstellungskombination wird nicht unterstützt, selbst wenn SharePoint Server Meine Sites aktiviert hat.  

## <a name="does--online-connect-with-sharepoint-server"></a>Stellt [!INCLUDE[prod_short](includes/prod_short.md)] online eine Verbindung zu SharePoint Server her?

Anz. Diese Bereitstellungskombination wird nicht unterstützt, selbst wenn SharePoint Server Meine Sites aktiviert hat.  

## <a name="how-does-this-work-in-an-organization-with-multiple-environments"></a>Wie funktioniert dies in einem Unternehmen mit mehreren Umgebungen?

Die Integration geht davon aus, dass die Namen der Firmen in den Umgebungen von [!INCLUDE[prod_short](includes/prod_short.md)] eindeutig sind. Wenn die Namen der Firmen innerhalb des Unternehmens eindeutig sind, wird beim Öffnen einer Datei in OneDrive die Datei in einen Ordner kopiert, der nach der aktuellen Firma benannt ist. Wenn Firmennamen in verschiedenen Umgebungen nicht eindeutig sind, werden Dateien mit identischen Firmennamen möglicherweise im selben Ordner abgelegt.  

## <a name="weve-changed-company-name-what-happens-to-my-previous-files"></a>Wir haben den Namen unserer Firma geändert. Was passiert mit meinen früheren Dateien?

[!INCLUDE[prod_short](includes/prod_short.md)] migriert Dateien, die Sie zuvor in OneDrive geöffnet haben, nicht automatisch in den neuen Ordner. Nach der Umbenennung Ihrer Firma kopiert die Aktion Öffnen in OneDrive die Dateien in einen Ordner, der den neuen Namen der Firma trägt.   

## <a name="when-attaching-files-to--how-do-i-pick-a-file-from-onedrive"></a>Wie kann ich beim Anhängen von Dateien an [!INCLUDE[prod_short](includes/prod_short.md)] eine Datei aus OneDrive kommissionieren?

[!INCLUDE[prod_short](includes/prod_short.md)] bietet keinen Cloud-Datei-Picker. Sie müssen die Datei von OneDrive auf Ihr Gerät herunterladen und sie dann auf [!INCLUDE[prod_short](includes/prod_short.md)] hochladen. 

## <a name="i-want-to-open-files-in-sharepoint-instead-how-do-i-do-this"></a>Ich möchte stattdessen Dateien in SharePoint öffnen. Wie kann ich das tun?

[!INCLUDE[prod_short](includes/prod_short.md)] bietet keine Funktionen zum Kopieren von Dateien in SharePoint und zum Öffnen von Dateien aus einer SharePoint-Bibliothek. Wenden Sie sich an Ihren Microsoft-Partner, um Ihre Möglichkeiten zu verstehen, oder suchen Sie nach Apps in AppSource.  

## <a name="how-do-i-turn-off-integration-to-onedrive"></a>Wie kann ich die Integration in OneDrive deaktivieren?

Führen Sie die Anleitung zur **OneDrive Einrichtung** aus und deaktivieren Sie die Schalter **Verwenden Sie OneDrive für Apps Funktionen** und **Verwenden Sie OneDrive für Systemfunktionen**. 

## <a name="should-i-use-the-sharepoint-connection-setup-page-to-connect-to-sharepoint"></a>Soll ich die Seite für die Einrichtung der Verbindung zu SharePoint verwenden, um eine Verbindung zu SharePoint herzustellen?

Dies ist eine veraltete Funktion, bei der alle [!INCLUDE[prod_short](includes/prod_short.md)]-Dateien von allen Benutzern an einen einzigen SharePoint-Ordner gesendet werden. Wir empfehlen Ihnen, das Inforegister „Gemeinsame Dokumente“ nicht auf der Seite **SharePoint Verbindungseinrichtung** zu konfigurieren, da diese Seite [veraltet](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup) ist und in der Veröffentlichungswelle 2 2023, Version 23.0, entfernt werden wird.  Wir empfehlen Ihnen, stattdessen die **OneDrive Einrichtung** zu verwenden.  

## <a name="which-version-of--supports-onedrive"></a>Welche Version von [!INCLUDE[prod_short](includes/prod_short.md)] unterstützt OneDrive?

Die Integration mit OneDrive wurde 2021 im Veröffentlichungszyklus 2 verfügbar.  

## <a name="which-features-are-affected-by-onedrive-integration"></a><a name="features"></a>Welche Funktionen sind von der OneDrive Integration betroffen?

In der Anleitung **OneDrive Einrichtung** zur Einrichtung der OneDrive-Integration können Sie Funktionen für den Umgang mit Business Central-Dateien in OneDrive ein- oder ausschalten. Die Funktionen sind in zwei Optionen unterteilt:

|Option|Description|
|------|----------|
|**OneDrive für App-Funktionen verwenden**|Wenn Sie diese Option aktivieren, stehen die Aktionen **Öffnen in OneDrive** und **Freigeben** für Dateien in Business Central zur Verfügung, z.B. für Dateien im Anhang von Dokumenten oder im Posteingang von Berichten. Mit diesen Aktionen können Benutzer Dateien in OneDrive kopieren, öffnen und freigeben. Weitere Informationen finden Sie unter [Öffnen und Freigeben von Business Central Dateien in OneDrive](across-share-onedrive.md).
|**Verwenden Sie OneDrive für Systemfunktionen**|Wenn Sie diese Option einschalten, werden die folgenden Funktionen aktiviert:<ul><li> Die Aktionen **Öffnen in Excel** und **Bearbeiten in Excel** auf Listenseiten kopieren die Excel-Datei automatisch nach OneDrive und öffnen sie dann in Excel Online. Weitere Informationen finden Sie unter [Betrachten und Bearbeiten in Excel](across-work-with-excel.md).</li><li> Wenn Sie einen Bericht an eine Excel- oder Word-Datei senden, wird die Datei automatisch nach OneDrive kopiert und dann in Excel oder Word Online geöffnet. Weitere Informationen finden Sie unter [Speichern eines Berichts in einer Datei](ui-work-report.md#saving-a-report-to-a-file).|

## <a name="will-microsoft-continue-to-improve-the-integration-to-onedrive"></a>Wird Microsoft die Integration in OneDrive weiter verbessern?

Bei Microsoft achten wir stets auf das Feedback aus unsere breitgefächerte Benutzer-Community und reagieren auf die häufigsten Vorschläge. Um zu erfahren, was als nächstes für Integrationen mit Microsoft 365-Apps geplant ist, lesen Sie den [Dynamics 365 Veröffentlichungsplan](/dynamics365-release-plan/2021wave1).  

Wenn Sie sich an der Verbesserung der OneDrive-Integration beteiligen möchten oder eine Idee haben, die die gemeinsame Nutzung von Dateien und die Zusammenarbeit in [!INCLUDE[prod_short](includes/prod_short.md)] verbessern würde, fügen Sie eine Idee hinzu oder stimmen Sie für bestehende Ideen unter [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas) ab.

## <a name="troubleshooting"></a>Problembehebung

Dieser Abschnitt enthält Informationen darüber, wie Sie Probleme, die bei der Verwendung von OneDrive mit [!INCLUDE[prod_short](includes/prod_short.md)] auftreten können, erkennen und beheben können.  

### <a name="business-central-cant-find-my-onedrive"></a>Business Central kann meine OneDrive nicht finden

Wenn diese Nachricht angezeigt wird, „Der Lagerort Ihrer OneDrive für Business konnte nicht festgelegt werden, wenden Sie sich an Ihren Partner, um dies einzurichten.“, überprüfen Sie, ob der Benutzer mindestens einmal auf seine OneDrive zugegriffen hat. Ist dies nicht der Fall, bitten Sie die Person, die Einrichtung unter portal.office.com/onedrive vorzunehmen. Das kann eine Weile dauern. Wenn die Nachricht auch nach 24 Stunden noch angezeigt wird, wenden Sie sich an den Support.  
 
### <a name="im-having-problems-sharing-from-outlook"></a>Ich habe Probleme bei der Freigabe aus Outlook

Siehe [Kann keine OneDrive-Dateien von Outlook.com freigeben](https://support.microsoft.com/en-us/office/can-t-share-onedrive-files-from-outlook-com-05d4cb21-40a2-40e3-b111-82cddb82d22f) auf Microsoft Support.

### <a name="actions-open-in-onedrive-and-share-are-missing"></a>Die Aktionen Öffnen in OneDrive und Freigeben fehlen

Es gibt ein paar Dinge, die Sie überprüfen können:

- Vergewissern Sie sich, dass die Funktionen der Anwendung OneDrive in der Anleitung zur **OneDrive Einrichtung** aktiviert sind. Siehe [Konfigurieren Sie OneDrive mit der OneDrive Einrichtung](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup).
- Vergewissern Sie sich, dass Microsoft OneDrive auf der Seite **Status der Datenschutzhinweise** auf **Zustimmen** festgelegt ist. Siehe [Status der Datenschutzhinweise](privacy-notices-status.md).

## <a name="see-also"></a>Siehe auch

[Business Central und OneDrive Integration](across-onedrive-overview.md)  
[Verwaltung der OneDrive Integration mit Business Central](admin-onedrive-integration.md)  
[Öffnen von Business Central Dateien in OneDrive](across-share-onedrive.md)  
