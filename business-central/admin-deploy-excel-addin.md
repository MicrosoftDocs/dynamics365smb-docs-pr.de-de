---
title: Business Central-Add-in für Excel abrufen
description: 'Erfahren Sie, wie Sie Benutzern das Business Central-Add-in für Excel zur Verfügung stellen können.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.form: 1480
ms.search.keywords: 'Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource'
ms.date: 10/07/2021
ms.author: jswymer
---
# <a name="get-the-business-central-add-in-for-excel"></a>Holen Sie sich das Business Central-Add-in für Excel

[!INCLUDE[prod_short](includes/prod_short.md)] enthält ein Add-in für Excel, mit dem Benutzer auf bestimmten Seiten eine Aktion **In Excel bearbeiten** auswählen können, um die Daten in einem Excel-Arbeitsblatt zu öffnen. Diese Aktion unterscheidet sich von der Aktion **In Excel öffnen**, denn sie ermöglicht es den Benutzern, Änderungen in Excel vorzunehmen und diese dann wieder in [!INCLUDE[prod_short](includes/prod_short.md)] zu veröffentlichen.

## <a name="overview"></a>Matrix

### <a name="about-the-add-in"></a>Über das Add-in

Das Add-in heißt **Microsoft Dynamics Office Add-in** und kann über den [Office Store (AppSource)](https://appsource.microsoft.com/) installiert werden. Wenn das Add-in installiert ist, ist die Aktion **In Excel bearbeiten** auf den meisten Listen- und Listenteilseiten über das Symbol **Freigeben** verfügbar. ![Eine Seite in einer anderen App freigeben.](media/share-icon.png). Weitere Informationen zur Verwendung des Add-Ins finden Sie unter [Anzeigen und Bearbeiten in Excel von Business Central](across-work-with-excel.md).

> [!NOTE]
> Das Add-In funktioniert nur unter Windows, nicht unter macOS.

### <a name="about-deployment-as-an-admin"></a>Über das Bereitstellen als Admin

Mit [!INCLUDE[prod_short](includes/prod_short.md)] Online gibt es einige Bereitstellungsoptionen, um das Add-In für die Benutzer bereitzustellen. Eine Option ist der *individuelle Erwerb*, bei dem Sie die Benutzer das Add-In selbst installieren lassen. Bei dieser Option müssen die Benutzer Zugriff auf das Herunterladen von Dateien aus dem Office Store haben. Eine andere Möglichkeit ist, die *Zentrale Bereitstellung* im Microsoft 365 Admin Center festzulegen, um das Add-In automatisch für Ihr gesamtes Unternehmen, für Gruppen oder für bestimmte Benutzer bereitzustellen. Die zentrale Bereitstellung bietet eine Möglichkeit, das Add-in den Benutzern zur Verfügung zu stellen, wenn Ihr Unternehmen den Benutzern keinen Zugriff auf den Office Store gewährt.

Für den Endbenutzer stellt sich die Installation in den beiden Bereitstellungsszenarien unterschiedlich dar:

- Bei der Einzelerfassung wählen die Benutzer zum ersten Mal die Aktion **In Excel bearbeiten** und das Fenster **Neues Office Add-in** wird in Excel geöffnet. Um das Add-in zu installieren, wählt der Benutzer **Diesem Add-in vertrauen**, was wiederum das Add-in direkt aus dem Office Store installiert. Der Benutzer meldet sich dann mit seinem Benutzernamen und Kennwort bei [!INCLUDE[prod_short](includes/prod_short.md)] an.

- Bei der zentralen Bereitstellung wird das Add-in bei der ersten Auswahl der Aktion **In Excel bearbeiten** automatisch aus der zentralen Bereitstellung in Excel installiert, nicht aus dem Office Store. Die Benutzer müssen sich nur noch bei [!INCLUDE[prod_short](includes/prod_short.md)] anmelden.

Bei diesen beiden Bereitstellungsoptionen wird das Add-In automatisch so konfiguriert, dass es sich mit [!INCLUDE[prod_short](includes/prod_short.md)] verbindet. Eine dritte Bereitstellungsoption ist die manuelle Installation des Add-Ins direkt aus Excel. Bei dieser Option müssen die Benutzer das Add-In so konfigurieren, dass es eine Verbindung zu [!INCLUDE[prod_short](includes/prod_short.md)] herstellt.

### <a name="switching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around"></a><a name="switch"></a>Wechsel von der individuellen Erfassung zur zentralen Bereitstellung oder andersherum

Wenn Sie vom Einzelerwerb des Add-Ins zur zentralen Bereitstellung oder umgekehrt wechseln, sind Excel-Dateien betroffen, die Benutzer vor dem Übergang erstellt haben. Nach der Umstellung können Benutzer weiterhin alle Excel-Arbeitsblätter öffnen, die zuvor mit der Aktion **In Excel bearbeiten** erstellt wurden oder die manuell durch die Konfiguration des Excel-Add-Ins erstellt wurden. Aber sie können die Daten in der Datei nicht von Business Central aus aktualisieren oder Aktualisierungen an Business Central senden.

Dieser Zustand wird dadurch verursacht, dass jeder Excel-Datei eine „Add-In“-Kennung zugewiesen wird. Beim Übergang zur oder von der zentralen Bereitstellung wird eine andere Kennung zugewiesen, sodass die frühere Kennung blockiert wird.

## <a name="preparation-on-premises-only"></a>Vorbereitung (nur on-premises)

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises setzt voraus, dass Ihre Umgebung für das Add-In konfiguriert ist. Wenn dies nicht der Fall ist, steht die Aktion **In Excel bearbeiten** den Benutzern nicht zur Verfügung. Weitere Informationen finden Sie unter [Einrichten des Excel-Add-Ins zum Bearbeiten von Business Central-Daten](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) in der Hilfe für Entwickler und IT-Profis.

## <a name="deploy-the-add-in-by-using-centralized-deployment"></a>Bereitstellen des Add-Ins mit Hilfe der zentralen Bereitstellung

Die zentrale Bereitstellung ist eine Funktion im Microsoft 365 Admin Center, mit der Sie Add-Ins automatisch in den Office-Apps der Benutzer, z. B. Excel, bereitstellen können. Um Ihnen bei der zentralen Bereitstellung zu helfen, enthält [!INCLUDE[prod_short](includes/prod_short.md)] die **Unterstützte Einrichtung des Excel Add-Ins Zentrale Bereitstellung**.

### <a name="before-you-begin"></a>Bevor Sie beginnen

- Um zu erfahren, wie Sie Benutzer am Herunterladen aus dem Office Store hindern können, lesen Sie [Add-ins im Admin Center verwalten](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Vergewissern Sie sich, dass die zentrale Bereitstellung in Ihrem Unternehmen funktioniert. Weitere Informationen finden Sie unter [Bestimmen Sie, ob die zentrale Bereitstellung von Add-Ins für Ihr Unternehmen geeignet ist](/microsoft-365/admin/manage/centralized-deployment-of-add-ins).
- Wenn Sie von der individuellen Erfassung zu einer zentralen Bereitstellung wechseln, lesen Sie bitte [Umstellung von der individuellen Erfassung zur zentralen Bereitstellung](#switch)

> [!NOTE]
> Die Aktivierung der zentralen Bereitstellung wirkt sich auf Funktionen aus, die das Excel-Add-In verwenden, wie z.B. die **Bearbeiten in Excel** Aktion. Sie hat keine Auswirkungen auf andere Excel-bezogene Funktionen und Berechtigungen, die Benutzern in [!INCLUDE[prod_short](includes/prod_short.md)] zugewiesen sind.

### <a name="set-up-centralized-deployment-of-the-add-in"></a>Zentrale Bereitstellung des Add-Ins festlegen

Sie werden sowohl in [!INCLUDE[prod_short](includes/prod_short.md)] als auch im Microsoft 365 Admin Center arbeiten.

1. Wählen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Sagen Sie mir, was Sie tun möchten") Symbol, geben Sie **Excel Add-in Zentrale Bereitstellung** ein und wählen Sie dann den entsprechenden Link.
2. Lesen Sie die Informationen auf der Seite **Einrichtung des Business Central-Add-in für Excel** und wählen Sie **Weiter**.
3. Melden Sie sich beim [Microsoft 365 Admin Center](https://go.microsoft.com/fwlink/?linkid=2163967) an, und wechseln Sie dann zu **Integrierte Apps**.<!--**Add-ins**-->.

    Führen Sie die folgenden Schritte aus, um das Add-in so zu konfigurieren, dass es aus dem Office Store bereitgestellt wird: 
    1. Wählen Sie **Apps holen**, um den Office Store zu öffnen (AppSource). <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Suchen Sie nach **Microsoft Dynamics Office Add-in**, und wählen Sie dann **Jetzt holen**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. Geben Sie auf der Seite **Benutzer hinzufügen** die Benutzer an, für die Sie das Add-in bereitstellen möchten, und wählen Sie dann **Weiter**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Überprüfen Sie die Seite **Anforderungen für Berechtigungen akzeptieren** und wählen Sie dann **Weiter** > **Einsatz fertig stellen**.
    5. Warten Sie, bis das grüne Häkchen neben **Bereitgestellt** für das Add-In erscheint, und wählen Sie dann **Erledigt**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       Das Add-In erscheint auf der Seite **Add-ins**. Weitere Informationen über das Bereitstellen von Add-Ins im Microsoft 365 Admin Center finden Sie unter [Einsatz von Add-Ins im](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true) Admin Center.
4. Gehen Sie zurück zur unterstützten Einrichtung **Excel Add-in „Zentrale Bereitstellung“** unterstützten Einrichtung in [!INCLUDE[prod_short](includes/prod_short.md)]. und wählen Sie **Weiter** aus.
5. Aktivieren Sie **Zentrale Bereitstellung verwenden** und wählen Sie **Fertigstellen**.

    Wenn Sie diesen Schalter nicht einschalten, holt [!INCLUDE[prod_short](includes/prod_short.md)] das Add-in direkt aus dem Office Store.

Wenn Sie fertig sind, können Sie die Bereitstellung im Microsoft 365 Admin Center jederzeit ändern, z. B. weitere Benutzer zuweisen. Weitere Informationen über das Bereitstellen von Add-Ins im Admin Center finden Sie unter [Einsatz von Add-Ins im Admin Center](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).

> [!IMPORTANT]
> Wenn Sie über mehr als eine Umgebung verfügen, müssen Sie die unterstützte Einrichtung **Excel Add-in Zentrale Bereitstellung** in jeder Umgebung ausführen, in der Sie die zentrale Bereitstellung verwenden möchten. Sie müssen die zentrale Bereitstellung in Microsoft 365 jedoch nicht erneut konfigurieren. Sie müssen lediglich den Schalter **Zentrale Bereitstellung bereitstellen** in der unterstützten Einrichtung aktivieren. 

> [!NOTE]
> Es kann bis zu 24 Stunden dauern, bis das Add-In automatisch in Excel von Benutzern bereitgestellt wird.

## <a name="individual-acquisition-install-the-add-in-manually-for-your-own-use"></a><a name="install"></a>Individuelle Übernahme: Installieren Sie das Add-In manuell für Ihren eigenen Gebrauch

Wenn Sie Excel von Business Central aus öffnen, wird das Add-in in den meisten Fällen entweder automatisch für Sie installiert oder Sie werden aufgefordert, es zu installieren. Es kann jedoch Fälle geben, in denen Sie das Add-in manuell installieren müssen.

1. Öffnen Sie Excel und dann eine beliebige Excel-Arbeitsmappe.
2. Wählen Sie im Menü **Einfügen** die Option **Add-ins** > **Add-ins holen**
3. Gehen Sie zu **Admin verwaltet** und suchen Sie nach **Microsoft Dynamics Office Add-in**. Wenn Sie es sehen, wählen Sie es aus und wählen Sie dann **Hinzufügen**. Wenn Sie es nicht sehen, gehen Sie zu **Store**, suchen Sie dann nach *Microsoft Dynamics Office Add-in* und folgen Sie den Anweisungen auf dem Bildschirm, um es hinzuzufügen.

Wenn das Add-In installiert ist, wird es in Excel als ein Panel angezeigt. Als nächstes konfigurieren Sie die Verbindung.

### <a name="configure-the-business-central-connection"></a>Konfigurieren Sie die Business Central Verbindung

Wenn ein Benutzer die Verbindung nicht automatisch herstellen kann, können Sie ihn auffordern, die folgenden Schritte auszuführen:

1. Wählen Sie im **Microsoft Dynamics** Add-In-Fenster in Excel die Option **Serverinformationen hinzufügen**. Wenn Sie es nicht sehen, wählen Sie in Excel die Schaltfläche ![Weitere Optionen](media/cogwheel.png). Symbol am oberen Rand, um den Optionsdialog zu öffnen. 
2. Für [!INCLUDE[prod_short](includes/prod_short.md)] online, legen Sie **Server URL** auf `https://exceladdinprovider.smb.dynamics.com` fest. Für [!INCLUDE[prod_short](includes/prod_short.md)] on-premises legen Sie die URL des Web Clients fest, wie `https://myBCserver/190`.
3. Wählen Sie **OK**, und bestätigen Sie dann, dass die App neu geladen wird.
4. Wenn Sie dazu aufgefordert werden, melden Sie sich mit Ihrem Business Central Benutzernamen und Kennwort an.
5. Wählen Sie optional die Umgebung und die Firma aus, mit der Sie sich verbinden möchten.

Das Add-In ist nun mit [!INCLUDE [prod_short](includes/prod_short.md)] verbunden und Sie können Daten bearbeiten und die Änderungen in [!INCLUDE [prod_short](includes/prod_short.md)] veröffentlichen.  

## <a name="prepare-devices-and-network-for-the-excel-add-in"></a>Geräte und Netzwerk für das Excel Add-In vorbereiten

Netzwerkdienste wie Proxys oder Firewalls müssen Routing zwischen jedem Client-Gerät, auf dem das Add-In installiert ist, und vielen Dienstendpunkten zulassen. Eine Liste der Endpunkte finden Sie unter [Vorbereiten Ihres Netzwerks für das Excel-Add-In](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## <a name="troubleshooting"></a>Problembehebung

Manchmal kommt es vor, dass Benutzer Probleme mit dem Excel-Add-In ausführen. In diesem Abschnitt finden Sie einige Tipps, wie Sie die Sperrung für Benutzer unter bestimmten Umständen aufheben können.

|Problem  |Lösung oder Workaround  |Bemerkungen  |
|---------|---------|---------|
|Das Add-In lässt sich nicht starten <br><br>Beispielsweise erhält der Benutzende die Meldung „Add-In-Warnung: Dieses Add-In ist nicht mehr verfügbar.“, wenn Sie versuchen, das Add-In zu verwenden. Dieses spezielle Problem kann auftreten, wenn die zentralisierte Bereitstellung korrekt konfiguriert ist, dem Benutzenden jedoch kein Zugriff zugewiesen wurde.|Prüfen Sie, ob das Add-in zentral bereitgestellt wird. Oder überprüfen Sie, ob der Benutzer für die lokale Installation gesperrt ist. | Der Admin kann Office so konfigurieren, dass Benutzer keine Add-Ins erwerben können. In diesen Fällen muss der Admin das Add-In zentral bereitstellen. Weitere Informationen finden Sie unter [Add-ins im Admin Center bereitstellen](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|Die Daten werden nicht in Excel geladen|Testen Sie die Verbindung, indem Sie eine andere Liste in Excel über [!INCLUDE [prod_short](includes/prod_short.md)] öffnen. Oder öffnen Sie die Arbeitsmappe in Excel in einem Browser.|Wenn der Benutzer einen Firmennamen angegeben hat, der Sonderzeichen enthält, kann das Add-In keine Verbindung herstellen. |
|Daten können nicht in [!INCLUDE [prod_short](includes/prod_short.md)] zurück veröffentlicht werden.|Testen Sie die Verbindung, indem Sie die Arbeitsmappe in Excel in einem Browser öffnen. |Manchmal kann eine Erweiterung den Veröffentlichungsauftrag blockieren. Wenn die Seite erweitert oder angepasst ist, entfernen Sie die Erweiterungen und versuchen Sie es dann erneut.|
|Die Daten sind falsch  |Excel zeigt Zeiten und Daten möglicherweise in einem anderen Format als [!INCLUDE [prod_short](includes/prod_short.md)] an. Diese Bedingung macht sie nicht falsch, und die Daten in [!INCLUDE [prod_short](includes/prod_short.md)] werden nicht durcheinander gebracht.|         |
|Bei einigen Listenseiten führt das Bearbeiten mehrerer Zeilen in Excel immer wieder zu Fehlern. Diese Bedingung kann auftreten, wenn OData-Aufrufe FlowFields und Felder außerhalb des Steuerelements des Repeaters enthalten.|Aktivieren Sie auf der Seite **Webdienste** die Kontrollkästchen **Nicht editierbare FlowFields ausschließen** und **Felder außerhalb des Repeaters ausschließen** für die veröffentlichte Seite. Wenn Sie diese Kontrollkästchen aktivieren, werden nicht editierbare FlowFields und Felder von der eTag Berechnung ausgeschlossen. |Diese Kontrollkästchen sind standardmäßig ausgeblendet. Um sie auf der Seite **Webdienste** anzuzeigen, verwenden Sie [Personalisierung](/dynamics365/business-central/ui-personalization-user). |
|Benutzer können sich nicht mehr beim Add-In anmelden. Wenn sie versuchen, sich anzumelden, wird der Vorgang abgebrochen, ohne abgeschlossen zu werden.| Dieses Problem wird möglicherweise durch ein Update verursacht, das irgendwann im Juli 2022 am Add-In vorgenommen wurde. Weitere Informationen und eine Fehlerbehebung finden Sie unter [Excel-Add-In-Konfiguration zur Unterstützung des Updates vom Juli 2022 ändern](/dynamics365/business-central/dev-itpro/administration/update-excel-addin-configuration).|Gilt nur für [!INCLUDE [prod_short](includes/prod_short.md)]-On-Premises|

<!--
## <a name="deploy-the-excel-add-in-for-business-central-online"></a>Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### <a name="to-deploy-the-excel-add-in-for-all-users"></a>To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### <a name="to-add-the-excel-add-in-locally"></a>To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Siehe auch

[Analysieren von Finanzberichten in Microsoft Excel](finance-analyze-excel.md)  
[Arbeiten mit Business Central](ui-work-product.md)  
[Verbesserungen der Excel-Integration in der Veröffentlichungswelle 2 von 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
