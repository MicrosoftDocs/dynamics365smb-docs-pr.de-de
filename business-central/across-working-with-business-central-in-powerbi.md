---
title: Von der lokalen Business Central-Version aus eine Verbindung mit Power BI herstellen | Microsoft-Dokumentation
description: 'Abrufen von Erkenntnissen, Business Intelligence und KPIs aus Ihren Business Central-Daten mithilfe von Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="connect-to-power-bi-from-business-central-on-premises"></a>Von der lokalen Business Central-Version eine Verbindung mit Power BI herstellen

<!--In this article, you learn some of the basics about working with reports and dashboards in Power BI that use [!INCLUDE [prod_short](includes/prod_short.md)] as a data source. The article discusses some aspects that will help you get started as a [!INCLUDE[prod_short](includes/prod_short.md)] user. For general guidelines and instructions about using Power BI, see [Power BI documentation for consumers](/power-bi/consumer).

## <a name="get-ready"></a>Get ready

Sign up for the Power BI service. If you haven't already signed up, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). When you sign up, use a work email address and password.-->

## <a name="get-started"></a>Erste Schritte

Wenn Sie die lokale [!INCLUDE [prod_short](includes/prod_short.md)]-Version verwenden, muss es für die Power BI-Integration aktiviert sein. Diese Aufgabe wird normalerweise von einem Administrator ausgeführt. Weitere Informationen zum Aktivieren der Power BI-Integration mit Business Central Online finden Sie unter [Die lokale Business Central-Version für die Power BI-Integration einrichten](admin-powerbi-setup.md).

Einige Features sind nur mit Business Central Online und nicht mit der lokalen Version verfügbar. Weitere Informationen finden Sie unter [Einführung in Business Central und Power BI](admin-powerbi.md#what-you-can-do-with-power-bi-and-business-central)

## <a name="set-up--on-premises-for-power-bi-integration"></a><a name="setup"></a>[!INCLUDE[prod_short](includes/prod_short.md)] on-premises für die Power BI-Integration einrichten

In diesem Abschnitt werden die Anforderungen für eine Bereitstellung von [!INCLUDE[prod_short](includes/prod_short.md)] on-premises zur Integration mit Power BI erläutert.

1. Konfigurieren Sie die Authentifizierungsmethode für die Bereitstellung entweder mit [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) oder [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview).  
    
    > [!NOTE]
    > Die Power BI Integration unterstützt keine Windows-Authentifizierung und wird auf dem Windows-Client nicht unterstützt.

2. OData-Webdienste und ODataV4-Endpunkt aktivieren.

    Der OData-Webdienst muss auf dem [!INCLUDE[server](includes/server.md)] aktiviert sein und der OData-Port in der Firewall muss offen sein. Weitere Informationen finden Sie unter [Konfigurieren von Business Central Server – OData-Webdienste](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Der lokale Server muss über das Internet erreichbar sein.

3. [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzerkonten erhalten einen Webdienst-Zugriffsschlüssel.

    Zur Anzeige von [!INCLUDE[prod_short](includes/prod_short.md)]-Daten in Power BI wird nur ein Webdienst-Zugriffsschlüssel benötigt. Sie können jedem Benutzerkonto einen Webdienst-Zugriffsschlüssel zuweisen. Oder erstellen Sie stattdessen ein bestimmtes Konto mit einem Webdienst-Zugriffsschlüssel, der von allen Benutzern verwendet werden kann. Weitere Informationen finden Sie unter [Webdienst-Authentifizierung](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Erstellen Sie eine Anwendungsregistrierung für [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    Um Power BI-Berichte anzuzeigen, die in [!INCLUDE[prod_short](includes/prod_short.md)]-Seiten eingebettet sind, muss für [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure eine Anwendung registriert werden. Die registrierte Anwendung benötigt Berechtigungen für Power BI-Dienste. Für die App ist mindestens die Berechtigung **User.ReadWrite.All** erforderlich. Damit Benutzer Berichte von freigegebenen Power BI-Arbeitsbereichen anzeigen können, erfordert die App die Berechtigung **Workspace.Read.All**. Weitere Informationen finden Sie unter [Die lokale [!INCLUDE[prod_short](includes/prod_short.md)]-Version in Microsoft Entra-ID zur Integration mit anderen Diensten registrieren](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Wenn Ihre Bereitstellung die NavUserPassword-Authentifizierung verwendet, stellt [!INCLUDE[prod_short](includes/prod_short.md)] für alle Benutzer eine Verbindung mit demselben Power BI-Dienst her. Sie geben dieses Dienstkonto bei der Registrierung der Anwendung an. Wenn Sie die Microsoft Entra-Authentifizierung verwenden, verbindet sich [!INCLUDE[prod_short](includes/prod_short.md)] mit dem Power BI-Dienst, der den einzelnen Benutzerkonten zugeordnet ist.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Stellen Sie die erste Verbindung von Business Central zu Power BI her.

    Bevor Endbenutzer Power BI in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden können, muss ein Azure-Anwendungsadministrator dem Power BI-Service zustimmen.

    Um die erste Verbindung herzustellen, öffnen Sie [!INCLUDE[prod_short](includes/prod_short.md)], und führen Sie **Erste Schritte mit Power BI** über die Startseite aus. Diese Aktion führt Sie durch den Einwilligungsprozess und überprüft Ihre Power BI-Lizenz. Wenn Sie dazu aufgefordert werden, melden Sie sich mit einem Microsoft Entra-Administratorkonto an. Weitere Informationen finden Sie unter [Mit Power BI verbinden – nur ein Mal](across-working-with-powerbi.md#connect).

## <a name="build-power-bi-reports-to-display--data"></a>Power BI-Berichte zur Anzeige von [!INCLUDE [prod_long](includes/prod_long.md)]-Daten erstellen

Sie können Ihre Dynamics 365 Business Central-Daten zur Verfügung stellen als Datenquelle in Power BI Desktop und leistungsstarke Berichte über den Zustand Ihres Geschäftes erstellen.

Verwenden Sie Power BI Desktop, um Berichte zu erstellen, die Dynamics 365 Business Central-Daten anzeigen. Nach dem Erstellen können Sie die Berichte in Ihrem Power BI-Dienst veröffentlichen oder sie mit allen Benutzern in Ihrer Organisation teilen. Sobald sich diese Berichte im Power BI-Dienst befinden, können Sie von Benutzern, die dafür eingerichtet sind, in Dynamics 365 Business Central angezeigt werden.

- Für [!INCLUDE[prod_short](includes/prod_short.md)] on-premises benötigen Sie folgende Informationen:

  - Die OData-URL für [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Diese URL hat in der Regel das Format `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, z. B. `https://localhost:7048/BC190/ODataV4`. Bei einer Bereitstellung mit mehreren Mandanten sollte der Mandant in der URL enthalten sein, z. B. `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Einen Benutzernamen und einen Webdienst-Zugriffsschlüssel für ein [!INCLUDE[prod_short](includes/prod_short.md)]-Konto.

    Für das Abrufen von Daten aus [!INCLUDE[prod_short](includes/prod_short.md)] verwendet Power BI die Standardauthentifizierung. Sie benötigen also einen Benutzernamen und einen Webdienst-Zugriffsschlüssel, um eine Verbindung herzustellen. Hierbei kann es sich um Ihr eigenen Benutzerkonto oder um ein Konto Ihrer Organisation handeln, das speziell für diesen Zweck angelegt wurde.

## <a name="add--as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>[!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power BI Desktop hinzufügen

Die erste Aufgabe beim Erstellen von Berichten ist das Hinzufügen von [!INCLUDE[prod_short](includes/prod_short.md)] als Datenquelle in Power BI Desktop. Sobald die Verbindung hergestellt ist, können Sie mit der Erstellung des Berichts beginnen.

1. Starten Sie Power BI Desktop.
2. Wählen Sie **Daten abrufen** aus.

    Wenn Sie die Option **Daten abrufen** nicht sehen können, wählen Sie das Menü **Datei** und dann den Menüpunkt **Daten abrufen** aus.
3. Wählen Sie auf der Seite **Daten abrufen** die Option **Onlinedienste** aus.
4. Stellen Sie im Bereich **Onlinedienste** eine Verbindung mit der lokalen [!INCLUDE [prod_short](includes/prod_short.md)]-Version her, wählen Sie **Dynamics 365 Business Central (lokal)** und dann **Verbinden** aus.
5. Melden Sie sich bei [!INCLUDE [prod_short](includes/prod_short.md)] an (nur einmalig).

    Wenn Sie sich noch nicht bei [!INCLUDE [prod_short](includes/prod_short.md)] von Power BI Desktop aus angemeldet haben, werden Sie aufgefordert, sich anzumelden.

   - Für [!INCLUDE [prod_short](includes/prod_short.md)] lokal geben Sie zuerst die OData-URL für [!INCLUDE[prod_short](includes/prod_short.md)] ein und wählen dann **OK**. Wenn Sie dazu aufgefordert werden, geben Sie den Benutzernamen und das Kennwort des Kontos ein, das für die Verbindung mit [!INCLUDE[prod_short](includes/prod_short.md)] verwendet werden soll. Geben Sie in das Feld **Kennwort** den Webdienst-Zugriffsschlüssel ein. Wenn Sie fertig sind, wählen Sie **Verbinden**.
   
    > [!NOTE]  
    > Sobald Sie sich erfolgreich mit [!INCLUDE[prod_short](includes/prod_short.md)] verbunden haben, werden Sie nicht mehr aufgefordert, sich anzumelden. [Wie ändere oder lösche ich das Konto, das ich derzeit für die Verbindung mit Business Central von Power BI Desktop verwende?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Sobald die Verbindung hergestellt ist, stellt Power BI Kontakte zum Business Central-Dienst her. Das Fenster **Navigator** erscheint und zeigt die verfügbaren Datenquellen für die Erstellung von Berichten an. Wählen Sie einen Ordner, um ihn zu erweitern und die verfügbaren Datenquellen zu sehen. 

   Diese Datenquellen stellen alle Webdienste und API-Seiten dar, die für [!INCLUDE [prod_short](includes/prod_short.md)] veröffentlicht sind. Die Datenquellen sind nach den Business Central Umgebungen und Firmen gruppiert.

   > [!NOTE]
    > Die Struktur für Business Central lokal ist anders, weil es keine API-Seiten unterstützt.

7. Wählen Sie die Datenquelle(n) aus, die Sie zu Ihrem Datenmodell hinzufügen möchten, und wählen Sie dann die Schaltfläche **Laden**.
8. Wenn Sie später weitere Business Central-Daten hinzufügen möchten, können Sie die vorherigen Schritte wiederholen.

Sobald die Daten geladen sind, können Sie sie in der rechten Navigation auf der Seite sehen. Zu diesem Zeitpunkt haben Sie sich erfolgreich mit Ihren [!INCLUDE[prod_short](includes/prod_short.md)]-Daten verbunden und können mit dem Erstellen Ihres Power BI-Berichts beginnen.  

> [!TIP]
> Weitere Informationen zur Verwendung von Power BI Desktop finden Sie unter [Erste Schritte mit Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="manage-and-modify-reports"></a>Berichte verwalten und ändern

> [!NOTE]
> Sie können keine Berichte verwalten und ändern. 

## <a name="upload-reports"></a>Berichte hochladen

Für die lokale [!INCLUDE [prod_short](includes/prod_short.md)]-Version stehen keine Demoberichte zur Verfügung. Sie müssen daher bei Null beginnen und Power BI Desktop verwenden. Optional können Power BI-Berichte als Dateien verteilt werden, die Sie direkt von Power BI-Onlinediensten aus hochladen können. Weitere Informationen finden Sie unter [Hochladen des Berichts in den Dienst](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have SUPER user permissions in [!INCLUDE[prod_short](includes/prod_short.md)]. Also, you can't upload reports with [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. With on-premises, you upload reports directly to your Power BI workspace. For more information, see [Connect to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md).

<!--Once you have a Power BI account, you can sign in at [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

The Power BI service hosts all the reports available to you. To see the report, select **My Workspace** > **Reports**. Then just select the report that you want to view.

With [!INCLUDE[prod_short](includes/prod_short.md)] online, you'll automatically have a set of default reports on your workspace. If you want to create your own reports, you can use Power BI Desktop to create reports, and then publish them to your workspace. For more information, see [Getting Started Building Reports in Power BI Desktop to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, you'll have to start from scratch by using Power BI Desktop. Optionally, Power BI reports can be distributed as files, that you can upload.

<!--## Get the latest data

Each Power BI report is based on a dataset that gets data from the [!INCLUDE[prod_short](includes/prod_short.md)] sources. You want to make sure that the data in your Power BI reports is up to date with the data in [!INCLUDE[prod_short](includes/prod_short.md)]. This concept is referred to as *refreshing*.  Depending on how your organization has set up Power BI, refreshing might not happen automatically. There are two ways to refresh data: manually or by scheduling a refresh. Manual refreshing is done on-demand, as needed. Scheduled refreshing lets you refresh automatically at defined time intervals.

### <a name="refresh-manually"></a>Refresh manually

In the navigation pane, under **Datasets**, select **More options (...)** next to the dataset, then select **Refresh now**.

### <a name="schedule-a-refresh"></a>Schedule a refresh

In the navigation pane, under Datasets, select More options (...) next to the dataset, then select **Schedule refresh**. Fill in the information under the **Schedule refresh** section, and select **Apply**.

For more information, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh)-->

<!--## <a name="upload"></a>Upload reports from files

Power BI Reports can be distributed among users as .pbix files. If you have a .pbix file, you can upload the file to a workspace. To upload a report, do the following steps:

1. In your new workspace, select **Get Data**.

2. In the Files box, select **Get**.

3. Select **Local File**, navigate to where you saved the file, and select **Open**.

For more information, see [Upload the report to the service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> If you're using [!INCLUDE[prod_short](includes/prod_short.md)] online, you can also upload a report from within [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Work with Power BI Reports in [!INCLUDE [prod_short](includes/prod_short.md)] - Upload Reports](across-working-with-powerbi.md#upload).

## <a name="share-reports-with-others"></a><a name="share"></a>Share reports with others

Once a report is in your workspace, you can share it with others in your organization.

To share a report, in a list reports, or in an open report, select **Share**. In the **Share report** pane, enter the full email addresses for individuals or distribution groups you want to share with. Follow the instructions on screen to complete the sharing. For more information, see [Share a dashboard or report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> You must have  [Power BI Pro license](/power-bi/service-features-license-type), and the people you share with do too. The content must be in a workspace in a [Premium capacity](/power-bi/service-premium-what-is). For more information, see [Ways to share your work in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).-->

## <a name="see-also"></a>Siehe auch

[Business Central und Power BI](admin-powerbi.md)  
[Einen Bericht aus Dateien hochladen](across-working-with-powerbi.md#upload-reports)  
 
[!INCLUDE[footer-include](includes/footer-banner.md)]
