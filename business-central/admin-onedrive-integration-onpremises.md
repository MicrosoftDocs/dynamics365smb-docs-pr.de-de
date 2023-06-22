---
title: Konfigurieren von OneDrive Integration mit Business Central Lokal
description: 'Erfahren Sie, wie Sie Business Central Lokal für die Integration mit OneDrive for Business festlegen.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 09/06/2022
ms.author: jswymer
---
# <a name="configuring-onedrive-integration-with-business-central-on-premises" />Konfigurieren von OneDrive Integration mit Business Central Lokal

Dieser Artikel erklärt, wie Sie die OneDrive-Integration mit Business Central vor Ort konfigurieren. Anders als bei [!INCLUDE[prod_short](includes/prod_short.md)] online, wird die Verbindung zwischen Business Central und OneDrive for Business nicht automatisch festgelegt. Wenn die Verbindung nicht konfiguriert ist, können die Benutzer die Funktionen für OneDrive nicht nutzen.

Für die Konfiguration der OneDrive-Integration sind zwei Aufgaben zu erledigen.

- Die erste Aufgabe besteht darin, eine Anwendung (App) auf Ihrem Azure Active Directory-Mandanten Ihres Microsoft 365 Plans zu registrieren. Die registrierte App wird für die Authentifizierung verwendet. Diese Aufgabe wird normalerweise im Azure-Portal und im Business Central Web Client erledigt.
- Die zweite Aufgabe besteht darin, die Verbindung mit der OneDrive-URL festzulegen und die OneDrive-Funktionen in Business Central zu aktivieren. Diese Aufgabe wird im Business Central Web Client erledigt. In Version 21 wird sie anders durchgeführt als in den Versionen 19 und 20. Version 21 führt eine neue **OneDrive Einrichtung** ein, die die **SharePoint Verbindungen Einrichtung** ersetzt.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] on-premises kann nur mit OneDrive verbunden werden, das von Microsoft in der Cloud gehostet wird. Die Verbindung von [!INCLUDE[prod_short](includes/prod_short.md)] vor Ort mit dem Meine Sites Repository von Server SharePoint wird nicht unterstützt.

## <a name="a-nameregisterapparegister-an-app-in-azure-ad-for-onedrive-integration" /><a name="registerapp"></a>Registrieren Sie eine App in Azure AD für die OneDrive Integration

In dieser Aufgabe fügen Sie eine registrierte App für Business Central im Mandant Azure AD Ihres Plans Microsoft 365 hinzu. Wie andere Azure-Dienste, die mit Business Central zusammenarbeiten, erfordert auch OneDrive eine registrierte App in Azure Active Directory (Azure AD). Die registrierte App stellt Authentifizierungs- und Autorisierungsdienste zwischen Business Central und SharePoint zur Verfügung, die von OneDrive genutzt werden.

Detaillierte Schritte für diesen Schritt finden Sie unter [Registrieren einer Anwendung in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) in der Hilfe für Entwickler und IT-Profis.

Beachten Sie bei der Registrierung der Anwendung die folgenden Punkte:

- Wenn Sie eine Anwendung bereits als Teil einer Integration mit einem anderen Microsoft-Produkt registriert haben, wie z.B. in Power BI, dann verwenden Sie diese registrierte App wieder. In diesem Fall müssen Sie nur die Berechtigungen für SharePoint für die bereits registrierte App festlegen.

- Stellen Sie sicher, dass Sie die registrierte App mit den folgenden delegierten Berechtigungen für die SharePoint API konfigurieren:

    - AllSites.FullControl
    - User.ReadWrite.All
    
    Legen Sie für Business Central 2021 Veröffentlichungszyklus 2 (Version 19) stattdessen diese Berechtigungen fest:
    
    - AllSites.Write
    - MyFiles.Write
    - User.Read.All 

- Wenn Sie Business Central Version 19 oder 20 verwenden, kopieren Sie die **Anwendungs-(Client-)ID** und **Client-Geheimnis**, die von der registrierten App verwendet werden. Sie benötigen diese Informationen in der nächsten Aufgabe.

## <a name="a-nameurlaget-your-onedrive-url" /><a name="url"></a>Ihre OneDrive URL abrufen

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## <a name="set-up-the-onedrive-connection-in-version--and-later" />Legen Sie die OneDrive-Verbindung in Version 21 und höher fest

Verwenden Sie dieses Verfahren, wenn Sie Business Central 2022 Veröffentlichungswelle 2 (Version 21) oder höher verwenden.

### <a name="prerequisites" />Voraussetzungen

- Berechtigung zum Einfügen, Bearbeiten und Löschen (imd) in der Tabelle **Dokumentenservice-Szenario** als Minimum

### <a name="run-onedrive-setup" />Einrichtung OneDrive ausführen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **OneDrive Einrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Wenn Sie die Unterstützte Einrichtung zum ersten Mal ausführen, sehen Sie die Seite **Ihre Privatsphäre**. Lesen Sie die Informationen auf der Seite, und wenn Sie mit den Bedingungen einverstanden sind, wählen Sie **Zustimmen**, um fortzufahren.
3. Auf der Seite **Dateiverarbeitung konfigurieren** haben Sie folgende Optionen zur Auswahl:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. Geben Sie auf der Seite **Business Central konfigurieren** die URL von OneDrive in das Feld **OneDrive URL** ein.

   [Wie finde ich meine OneDrive URL?](#url)
5. Wählen Sie **Verbindung testen** und warten Sie die Ergebnisse ab.
   - Wenn der Test erfolgreich ist, wählen Sie **Erledigt**, dann sind Sie bereit.
   - Schlägt der Test fehl, erhalten Sie eine Nachricht, in der das Problem beschrieben wird. In der Regel hat das Problem mit der URL zu tun, die Sie angegeben haben. Wählen Sie **OK**, um zur Seite **Business Central konfigurieren** zurückzukehren, überprüfen Sie die URL und versuchen Sie es erneut.
   - Wenn Sie die Azure AD registrierte App noch nicht festgelegt haben, öffnet sich die Anleitung **Einrichten Azure Active Directory**.
6. Nach Fertigstellung wird der Datenschutzhinweis für die OneDrive-Integration für alle Benutzer vereinbart. Wenn Sie es so ändern möchten, dass die Benutzer selbst zustimmen oder ablehnen müssen, gehen Sie auf die Seite **Status der Datenschutzhinweise** und wählen Sie **Benutzer entscheiden lassen** für die OneDrive-Integration. Die Benutzer werden dann aufgefordert, den Datenschutzhinweisen zuzustimmen oder sie abzulehnen, wenn sie die OneDrive-Funktionen zum ersten Mal verwenden. Weitere Informationen finden Sie unter [Datenschutzerklärungen](privacy-notices-status.md).

## <a name="set-up-the-connection-in-includeprodshortincludesprodshortmd-version--and-" />Einrichten der Verbindung in [!INCLUDE[prod_short](includes/prod_short.md)] Version 19 und 20

Verwenden Sie dieses Verfahren, wenn Sie Business Central 2022 Veröffentlichungswelle 1 (Version 20) oder 2021 Veröffentlichungswelle 2 (Version 19) verwenden.
> [!IMPORTANT]
> Wenn Sie diese Funktion konfigurieren, aktivieren Sie auch veraltete Funktionen, die Dateien an OneDrive senden.  
>
>* Die Funktion In Excel öffnen kopiert die Excel-Datei automatisch auf OneDrive und öffnet sie dann in Excel Online. 
>* Wenn Sie einen Bericht in eine Datei exportieren, wird die Datei automatisch nach OneDrive kopiert und anschließend in Excel Online, Word Online oder OneDrive geöffnet. 
>* Andere Funktionen können ebenfalls automatisch in OneDrive geöffnet werden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Microsoft SharePoint Verbindungseinrichtung** ein und wählen Sie dann den entsprechenden Link.
2. Geben Sie in das Feld **Beschreibung** eine Beschreibung für die Verbindung ein, z.B. **OneDrive**.
3. Geben Sie in das Feld **Ordner** **Business Central** ein.
4. Geben Sie in das Feld **Lagerort** die URL für Ihre OneDrive ein.

   [Wie finde ich meine OneDrive URL?](#url)
5. Geben Sie in das Feld **Client ID** die Client ID aus Ihrer registrierten App ein.
6. In das Feld **Client Secret** geben Sie das Geheimnis Ihrer registrierten App ein. 

> [!IMPORTANT]
> Die Seite **SharePoint Einrichtung der Verbindung** wird verwendet, um mehrere veraltete Funktionen zu konfigurieren. Der Abschnitt **Allgemein** konfiguriert die Verbindung zu OneDrive, und der Abschnitt **Gemeinsame Dokumente** leitet die Dateien stattdessen zu SharePoint um. Die **SharePoint Einrichtung von Verbindungen** wurde außer Betrieb genommen und wird in der nächsten Version entfernt. Wir empfehlen Ihnen, den Bereich **Gemeinsame Belege** nicht zu konfigurieren. Weitere Informationen finden Sie unter [Veraltete Funktionen in der Base App](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup).

## <a name="after-upgrade-to-version-" />Nach dem Upgrade auf Version 21

Wenn Sie ein Upgrade auf Version 21 oder höher durchführen, funktioniert die bestehende Verbindung zu OneDrive, die auf der Seite **SharePoint Verbindungseinrichtung** konfiguriert wurde, weiterhin. Da aber die Seite **SharePoint Einrichtung** in Version 23 entfernt wird, empfehlen wir Ihnen, auf die neue OneDrive Integration umzusteigen, wie im nächsten Abschnitt beschrieben. Wenn Sie diese Umstellung jetzt vornehmen, wird es einfacher, wenn die **SharePoint Einrichtung** irgendwann entfernt wird. Außerdem können Sie dann die Anleitung zur unterstützten Einrichtung der **OneDrive Einrichtung** verwenden, um die OneDrive Funktionen zu verwalten, auf die die Benutzer Zugriff haben.

## <a name="switching-from-legacy-sharepoint-to-new-onedrive-integration" />Wechsel von der veralteten SharePoint- zur neuen OneDrive-Integration

Um zur neuen OneDrive-Integration zu wechseln, führen Sie die Anleitung zur unterstützten Einrichtung **OneDrive Einrichtung** aus, die Sie direkt oder über die veraltete Seite **SharePoint Verbindungseinrichtung** öffnen können. Die **OneDrive Einrichtung** führt Sie durch die Umstellung und informiert Sie über die Änderungen, die auf dem Weg dorthin vorgenommen werden.

Bevor Sie mit der Umstellung beginnen oder während Sie sie durchführen, lesen Sie den nächsten Abschnitt, um sich über einige Aspekte und Überlegungen zu diesem Prozess zu informieren. 

### <a name="a-nameonedrivesetupmigrationaabout-switching-to-the-new-onedrive-integration" /><a name="onedrivesetupmigration"></a>Über die Umstellung auf die neue OneDrive-Integration

Neben der OneDrive-Integration kann Business Central auch mit anderen Diensten, wie Power BI und Universal Print, integriert werden. Die Integration mit diesen anderen Diensten erfordert ebenfalls eine registrierte Azure AD-App zur Authentifizierung. Die von diesen anderen Diensten verwendete Azure AD App wird in der **Einrichtung Ihrer Azure Active Directory Konten** unterstützten Einrichtung festgelegt. Wenn Sie von der veralteten SharePoint-Verbindungseinrichtung wechseln, ändert die neue **OneDrive-Einrichtung** unterstützte Einrichtung Ihre OneDrive-Integration so, dass sie auch die **Einrichtung Ihrer Azure Active Directory-Konten** unterstützte Einrichtung &mdash;verwendet, so dass alle Integrationen dieselbe Azure AD-App verwenden.

Diese Änderung hat Auswirkungen auf den Wechsel zur neuen OneDrive-Integration, je nachdem, ob in der unterstützten Einrichtung **Einrichten Ihrer Azure Active Directory-Konten** bereits eine Azure AD-App konfiguriert ist. 

> [!IMPORTANT]
> Nach dem Wechsel zur neuen OneDrive-Einrichtung können Sie die Seite **SharePoint-Verbindungseinrichtung** nicht mehr verwenden, um die OneDrive-Integration zu konfigurieren.

#### <a name="how-the-changes-affect-the-integration" />Wie sich die Änderungen auf die Integration auswirken

Die unterstützte Einrichtung **OneDrive Einrichtung** verwendet immer die App, die in der unterstützten Einrichtung **Einrichten Ihrer Azure Active Directory Konten** festgelegt ist, sofern es eine gibt. Wenn Sie die unterstützte Einrichtung **OneDrive Einrichtung** ausführen, vergleicht sie die in **Einrichten Ihrer Azure Active Directory Konten** festgelegte App mit Ihrer aktuellen App, die in **SharePoint Verbindungseinrichtung** festgelegt wurde.

> [!TIP]
> Auf der Seite **SharePoint Verbindung einrichten** und **Ihre Azure Active Directory Konten einrichten** wird die App Azure AD durch die **Client ID** identifiziert.

- Wenn die App in **Einrichten Ihrer Azure Active Directory Konten** eine andere ist als die App in **SharePoint Verbindungseinrichtung**, ändert sich die OneDrive Integration, um die App in **Einrichten Ihrer Azure Active Directory Konten** zu verwenden.

   In **OneDrive Einrichtung** erhalten Sie während der Umstellung eine Nachricht ähnlich dem folgenden Text: 

  `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` steht für die Client ID der App in **Einrichten Ihrer Azure Active Directory Konten**, auf die die OneDrive Integration umgestellt wurde. 

  > [!IMPORTANT]
  > Damit die neue OneDrive Integration nach der Umstellung funktioniert, müssen Sie der App die Berechtigung für die SharePoint API im Azure-Portal erteilen. Sie können diesen Schritt vor oder nach der Umstellung auf die neue OneDrive-Einrichtung durchführen. Weitere Informationen finden Sie im Abschnitt [Registrieren einer App in Azure AD für die OneDrive Integration](#registerapp).

- Wenn die App in **Einrichten Ihrer Azure Active Directory-Konten** dieselbe ist wie die App in **SharePoint-Verbindungseinrichtung**, verwendet die OneDrive-Integration dieselbe App wie zuvor, abgesehen von der Konfiguration in der Einrichtung **Einrichten Ihrer Azure Active Directory-Konten**.

   In **OneDrive Einrichtung** erhalten Sie bei der Umstellung eine Nachricht ähnlich dem folgenden Text:

    `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Wenn in der **Einrichtung Ihrer Azure Active Directory Konten** keine App festgelegt ist, wird für die OneDrive Integration die gleiche App wie zuvor verwendet.

   Die unterstützte Einrichtung **OneDrive Einrichtung** kopiert die App-Konfiguration in die **Einrichten Ihrer Azure Active Directory Konten** Einrichtung, so dass sie für andere Integrationen, die später festgelegt werden, verwendet wird.

   In **OneDrive Einrichtung** erhalten Sie während der Umstellung eine Nachricht ähnlich dem folgenden Text:

   `The Azure Active Directory Application used for authentication will be configured for all Business Central integrations`.

### <a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration" />Führen Sie die Einrichtung OneDrive aus, um zur neuen Integration OneDrive zu wechseln

1. Öffnen Sie entweder die Seite **OneDrive Einrichtung** oder die Seite **SharePoint Verbindung Einrichtung**.
2. Wenn Sie die Seite **SharePoint Einrichtung** verwenden, wählen Sie **Zur neuen OneDrive Einrichtung wechseln** in der Benachrichtigung am oberen Rand der Seite.
3. Folgen Sie der Anleitung zur **OneDrive Einrichtung** für die unterstützte Einrichtung.
4. Wenn Sie zur Seite **Dateiverarbeitung konfigurieren** gelangen, wählen Sie eine der folgenden Optionen, um Funktionen zu aktivieren:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. Die Seite **Business Central konfigurieren** zeigt dieselbe URL an, die von der bestehenden OneDrive Integration verwendet wird. Sie können die URL nach Bedarf ändern.
6. Wählen Sie **Verbindung testen** und folgen Sie den Anweisungen.

   Wenn der Test erfolgreich war, wählen Sie **Erledigt**, und Sie sind bereit, loszulegen. Andernfalls nutzen Sie die Nachrichten auf der Seite, um das Problem zu beheben.

## <a name="see-also" />Siehe auch
[Business Central und OneDrive für Business Integration](across-onedrive-overview.md)  
[Öffnen von Business Central Dateien in OneDrive](across-share-onedrive.md)  
[OneDrive FAQ](admin-onedrive-faq.md)

