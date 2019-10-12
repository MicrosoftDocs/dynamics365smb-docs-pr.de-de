---
title: Mit Microsoft Dynamics 365 Sales verbinden | Microsoft Docs
description: Integration mit Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 6a23cdf9a13461db92977cc46d7f4fcaa7c715f7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304516"
---
# <a name="set-up-a-connection-to-dynamics-365-sales"></a>Verbindung mit Dynamics 365 Sales einrichten
Für die Integration mit [!INCLUDE[crm_md](includes/crm_md.md)] müssen Sie eine Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] einrichten.

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Bevor Sie beginnen
Bevor Sie damit beginnen, die Apps zu verbinden, gibt es einige Informationen, die bereitzuhalten sinnvoll ist:  

* Eine URL für Ihre [!INCLUDE[crm_md](includes/crm_md.md)]-App. Um die URL schnell zu erhalten, öffnen Sie [!INCLUDE[crm_md](includes/crm_md.md)] und kopieren die URL, dann fügen Sie sie im Feld **Dynamics 365 Sales URL** in [!INCLUDE[d365fin](includes/d365fin_md.md)] ein. [!INCLUDE[d365fin](includes/d365fin_md.md)] passt die Formatierung für Sie an.  
* Ein Benutzername und ein Kennwort eines Benutzerkontos, die nur für die Integration verwendet werden.  
* Der Benutzername und das Kennwort des Kontos mit Administratorrechten.  

> [!Note]
> Diese Schritte beschreiben das Verfahren der Onlineversion von [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-test-and-enable-a-connection-to-includecrm_mdincludescrm_mdmd"></a>Eine Verbindung zu [!INCLUDE[crm_md](includes/crm_md.md)] einrichten, testen und aktivieren  
Für alle Authentifizierungstypen außer der Office 365 Authentifizierung richten Sie Ihre Verbindung mit Dynamics 365 Sales auf der Seite **Microsoft Dynamics 365 Sales Verbindungseinrichtung** ein. Für Office 365 Authentifizierung können Sie auch den Leitfaden für die unterstützte Einrichtung für das **Einrichten der Dynamics 365 Sales Verbindung** verwenden, der Ihnen hilft, die erforderlichen Informationen bereitzustellen.

### <a name="to-use-an-assisted-setup-guide"></a>So verwenden Sie einen Leitfaden für das unterstützte Setup
Das Leitfaden für das unterstützte Setup für das **Einrichtung der Dynamics 365 Sales Verbindung** kann Ihnen helfen, die Verbindung einzurichten und anzugeben, ob erweiterte Funktionen, wie Kopplung zwischen Datensätzen aktiviert werden sollen.

1. Wählen Sie **Einrichtung und Erweiterungen** und dann **Unterstütztes Setup** aus.
2. Wählen Sie Einrichten der **Dynamics 365 Sales Verbindung** aus, um den Leitfaden für das unterstützte Setup zu starten.
3. Füllen Sie die Felder je nach Bedarf aus.
4. Optional gibt es erweiterte Einstellungen, die die Sicherheit verbessern und weitere [!INCLUDE[crm_md](includes/crm_md.md)]-Funktionen aktivieren, wie Verkaufsauftragsbearbeitung und Anzeige der Lagerebene. Die erweiterten Einstellungen werden in der folgenden Tabelle beschrieben.  

|Feld|Beschreibung|
|-----|-----|
|**Import Dynamics 365 Sales Lösung**|Aktivieren Sie dies, um die in Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] einzurichten und zu konfigurieren. Weitere Informationen finden Sie unter [Informationen über die Business Central-Integrationslösung](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Artikelverfügbarkeits-Webdienst veröffentlichen**|Ermöglichen Sie es Personen, die [!INCLUDE[crm_md](includes/crm_md.md)] verwenden, die Verfügbarkeit von Artikeln (Produkten) im Lager in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzuzeigen. Dazu ist ein [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzerkonto mit einem Webdienst-Zugriffsschlüssel. Das Zuordnen des Schlüssels ist ein Vorgang mit zwei Schritten. Im Benutzerkonto in [!INCLUDE[d365fin](includes/d365fin_md.md)] müssen Sie die Aktion **Webdienstschlüssel ändern** auswählen. Im Leitfaden für das unterstützte Setup zum Einrichten der Dynamics 365 Sales Verbindung müssen Sie die Dynamics 365 Business Central-OData-Webdienst-URL festlegen und Benutzeranmeldeinformationen für [!INCLUDE[d365fin](includes/d365fin_md.md)] zum Aufrufen des Diensts bereitstellen. Weitere Informationen finden Sie unter [Odata-Webservice](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**Dynamics 365 Business Central-OData-Webdienst-URL**|Wenn Sie den Artikelverfügbarkeits-Webdienst aktivieren, wird Ihnen die URL für den OData-Webdienst bereitgestellt.|
|**Dynamics 365 Business Central-OData-Webdienst-Benutzername**|Der Name des [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzerkontos, den [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über Artikelverfügbarkeit in [!INCLUDE[d365fin](includes/d365fin_md.md)] über den OData-Webdienst abzurufen.|
|**Dynamics 365 Business Central-OData-Webdienst-Zugriffsschlüssel**|Der Zugriffsschlüssel des Benutzerkontos, das [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über Artikelverfügbarkeit aus [!INCLUDE[d365fin](includes/d365fin_md.md)] über den OData-Webdienst abzurufen. Der Schlüssel wird dem Benutzer zugeordnet, der im Feld **Dynamics 365 Business Central-OData-Webdienst-Benutzername** ausgewählt ist. Um den Schlüssel zu erhalten, wählen Sie die Schaltfläche **Wert suchen** neben dem Benutzernamen, wählen Sie den Benutzer aus, wählen Sie **Verwalten** und dann **Bearbeiten** aus. In der Benutzerkarte wählen Sie **Aktionen**, **Authentifizierung** und dann **Webdienstschlüssel ändern**.|
|**Verkaufsauftragsintegration aktivieren**|Wenn Personen Verkaufsaufträge in [!INCLUDE[crm_md](includes/crm_md.md)] erstellen und Aufträge in [!INCLUDE[d365fin](includes/d365fin_md.md)] erfüllen, wird dies in den Prozess in [!INCLUDE[crm_md](includes/crm_md.md)] integriert. Weitere Informationen finden Sie unter [Integration für Vertriebsauftragsverarbeitung aktivieren](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Dazu ist es erforderlich, dass Sie Anmeldeinformationen für ein Administratorbenutzerkonto in [!INCLUDE[crm_md](includes/crm_md.md)] zur Verfügung stellen. Weitere Informationen finden Sie im Abschnitt [Verarbeiten von Verkaufsauftragsdaten](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Aktivieren der Dynamics 365 for Sales-Verbindung**|Aktivieren Sie die Verbindung mit [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Dynamics 365-SDK-Version**|Dies ist nur relevant, wenn Sie eine lokale Version von [!INCLUDE[crm_md](includes/crm_md.md)] integrieren. Das ist das Dynamics 365 Software Development Kit (wird auch als Xrm bezeichnet), das Sie verwenden, um eine Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] herzustellen. Die Version muss mit der SDK-Version kompatibel sein, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird, und der Version von [!INCLUDE[crm_md](includes/crm_md.md)] entsprechen oder neuer sein.|

> [!Note]
> Das Einrichten der Anleitung zur unterstützten Einrichtung der **Dynamics 365 Sales Verbindung** weist automatisch den **Integrations-Administrator** und den **Integrationsbenutzer** Sicherheitsrollen für Benutzerkonten zu, die für die Integration verwendet wurden.

### <a name="to-create-or-maintain-the-connection-manually"></a>So erstellen oder pflegen Sie den Link manuell
Nachfolgend wird beschrieben, wie Sie die Felder der Seite **Microsoft Dynamics 365 Sales Verbindungseinrichtung** manuell ausfüllen. Dies ist auch die Seite, auf der Sie Einstellungen für die Integration verwalten.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Microsoft Dynamics 365-Verbindungseinrichtung** ein, und wählen dann den zugehörigen Link aus.
2. Geben Sie die folgenden Informationen über die Verbindung von [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] ein.

|Feld|Beschreibung|
|-----|-----|
|**Dynamics 365 Sales URL**|Die URL für Ihre Instanz von [!INCLUDE[crm_md](includes/crm_md.md)]. Um die URL zu erhalten, öffnen Sie [!INCLUDE[crm_md](includes/crm_md.md)], kopieren Sie die URL aus der Adressleiste in einem Browser, und fügen Sie dann die URL in das Feld ein. [!INCLUDE[d365fin](includes/d365fin_md.md)] stellt sicher, dass das Format korrekt ist.|
|**Benutzername** und **Kennwort**|Die Anmeldeinformationen des Benutzerkontos, das für die Integration dediziert ist. Weitere Informationen finden Sie unter [Einrichten des Benutzerkontos für die Integration in Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).|
|**Aktiviert**|Beginnen Sie mit der Verwendung der Integration. Wenn Sie die Verbindung nicht sofort aktivieren, werden die Verbindungseinstellungen gespeichert, aber Benutzer können nicht von [!INCLUDE[d365fin](includes/d365fin_md.md)] aus auf [!INCLUDE[crm_md](includes/crm_md.md)]-Daten zugreifen. Sie können zu dieser Seite zurückkehren und die Verbindung später aktivieren.  |
|**Dynamics 365-SDK-Version**|Wenn Sie eine Integration in einer lokale Version von [!INCLUDE[crm_md](includes/crm_md.md)] durchführen, verwenden Sie dieses Dynamics 365 Software Development Kit (wird auch als Xrm bezeichnet), um [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] zu verbinden. Die Version, die Sie auswählen, muss mit der SDK-Version kompatibel sein, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird. Diese Version gleicht der Version, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird oder ist neuer.|

> [!Note]
> Wenn Sie eine Verbindung zwischen einer lokalen Version von [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] herstellen und eine Verknüpfung mit einer [!INCLUDE[crm_md](includes/crm_md.md)]-Instanz mit einem bestimmten Authentifizierungstyp konfigurieren möchten, füllen Sie die Felder im Inforegister **Authentifizierungstypdetails** aus. Weitere Informationen finden Sie unter [Verwenden der Verbindungszeichenfolgen in XRM-Tooling zum herstellen einer Verbindung mit Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Dieser Schritt ist nicht erforderlich, wenn sie eine Verbindung mit einer Onlineversion von [!INCLUDE[d365fin](includes/d365fin_md.md)] herstellen.

3. Geben Sie die folgenden Informationen über die Verbindung von [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[d365fin](includes/d365fin_md.md)] ein.

|Feld|Beschreibung|
|-----|-----|
|**Dynamics 365 Business Central-Web Client-URL**|Die URL Ihrer [!INCLUDE[d365fin](includes/d365fin_md.md)]-Instanz. Dies ermöglicht es Benutzern, in [!INCLUDE[crm_md](includes/crm_md.md)] entsprechende Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] von Datensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] zu öffnen, beispielsweise ein Konto oder ein Produkt. Die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] geöffnet. Legen Sie für dieses Feld die URL der zu verwendenden [!INCLUDE[d365fin](includes/d365fin_md.md)]-Instanz fest.<br /><br /> Um das Feld zur Standard-URL für [!INCLUDE[d365fin](includes/d365fin_md.md)] zurückzusetzen, wählen Sie die Aktion **Webclient-URL zurücksetzen** aus.<br /><br /> Dieses Feld ist nur relevant, wenn die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] installiert ist.|
|**Artikelverfügbarkeits-Webdienst aktiviert**|Ermöglichen Sie es Personen, die [!INCLUDE[crm_md](includes/crm_md.md)] verwenden, die Verfügbarkeit von Artikeln (Produkten) im Lager in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzuzeigen. Wenn Sie dies aktivieren, müssen Sie auch einen Benutzernamen und einen Zugriffsschlüssel für [!INCLUDE[crm_md](includes/crm_md.md)] angeben, um den OData-Webdienst nach der Verfügbarkeit von Artikeln (Produkten ) abzufragen. Weitere Informationen finden Sie unter [Odata-Webservice](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**Dynamics 365 Business Central-OData-Webdienst-URL**|Wenn Sie den Artikelverfügbarkeits-Webdienst aktivieren, wird Ihnen die URL für den OData-Webdienst bereitgestellt.|
|**Dynamics 365 Business Central-OData-Webdienst-Benutzername**|Der Name des Benutzerkontos, den [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über die Artikelverfügbarkeit aus [!INCLUDE[d365fin](includes/d365fin_md.md)] über den OData-Webdienst abzurufen.|
|**Dynamics 365 Business Central-OData-Webdienst-Zugriffsschlüssel**|Der Zugriffsschlüssel des Benutzerkontos, das [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über Artikelverfügbarkeit aus [!INCLUDE[d365fin](includes/d365fin_md.md)] über den OData-Webdienst abzurufen. Der Schlüssel wird dem Benutzer zugeordnet, der im Feld **Dynamics 365 Business Central-OData-Webdienst-Benutzername** ausgewählt ist. Um den Schlüssel zu erhalten, wählen Sie die Schaltfläche **Wert suchen** neben dem Benutzernamen, wählen Sie den Benutzer aus, wählen Sie **Verwalten** und dann **Bearbeiten** aus. In der Benutzerkarte wählen Sie **Aktionen**, **Authentifizierung** und dann **Webdienstschlüssel ändern**.|

4. Geben Sie die folgenden Einstellungen für [!INCLUDE[crm_md](includes/crm_md.md)] ein.

|Feld|Beschreibung|
|-----|-----|
|**Auftragsintegration ist aktiviert**|Ermöglichen Sie es Benutzern, Verkaufsaufträge und aktivierte Angebote in [!INCLUDE[crm_md](includes/crm_md.md)] zu senden und sie dann in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzuzeigen und zu bearbeiten. Dies integriert den Prozess in [!INCLUDE[crm_md](includes/crm_md.md)]. Weitere Informationen finden Sie unter [Integration für Vertriebsauftragsverarbeitung aktivieren](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).|
|**Verkaufsaufträge automatisch erstellen**|Erstellen Sie einen Verkaufsauftrag in [!INCLUDE[d365fin](includes/d365fin_md.md)], wenn ein Benutzer einen in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt und sendet.|
|**Verkaufsangebote automatisch verarbeiten**|Verarbeiten Sie ein Verkaufsangebot in [!INCLUDE[d365fin](includes/d365fin_md.md)], wenn ein Benutzer eins in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt und aktiviert.|

5. Geben Sie die folgenden erweiterten Einstellungen ein.

|Feld|Beschreibung|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Benutzer müssen Dynamics 365 Sales-Benutzern zugeordnet werden**|Geben Sie an, ob [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzerkonten entsprechende Benutzerkonten in [!INCLUDE[crm_md](includes/crm_md.md)] haben müssen. Die **Office 365-Authentifizierungs-E-Mail** des [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzers muss mit der **Primären E-Mail** des [!INCLUDE[crm_md](includes/crm_md.md)]-Benutzers identisch sein.<br /><br /> Wenn Sie den Wert auf **Ja** festlegen, werden [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzer, die kein zugeordnetes [!INCLUDE[crm_md](includes/crm_md.md)]-Benutzerkonto haben, keine [!INCLUDE[d365fin](includes/d365fin_md.md)]-Integrationsfunktionen auf der Benutzeroberfläche haben. Der Zugriffs auf [!INCLUDE[crm_md](includes/crm_md.md)]-Daten direkt von [!INCLUDE[d365fin](includes/d365fin_md.md)] wird im Auftrag des [!INCLUDE[crm_md](includes/crm_md.md)]-Benutzerkontos ausgeführt.<br /><br /> Wenn Sie den Wert auf **Nein** festlegen, werden alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzer [!INCLUDE[crm_md](includes/crm_md.md)]-Integrationsfunktionen auf der Benutzeroberfläche haben. Der Zugriffs auf [!INCLUDE[crm_md](includes/crm_md.md)]-Daten wird im Auftrag des [!INCLUDE[crm_md](includes/crm_md.md)]-Verbindungs-(Integrations-)Benutzers ausgeführt.|
|**Der aktuelle Business Central-Benutzer ist einem Dynamics 365 Sales-Benutzer zugeordnet.**|Gibt an, ob Ihr Benutzerkonto einem Konto ist [!INCLUDE[crm_md](includes/crm_md.md)] zugeordnet ist|

6. Um die Verbindungseinstellungen zu testen, wählen Sie **Verbindung testen** aus.  

    > [!NOTE]  
    >  Wenn keine Datenverschlüsselung in [!INCLUDE[d365fin](includes/d365fin_md.md)] aktiviert ist, werden Sie gefragt, ob sie diese aktivieren möchten. Um Datenverschlüsselung zu aktivieren, wählen Sie **Ja** aus, und stellen Sie die erforderlichen Informationen bereit. Anderenfalls wählen Sie **Nein** aus. Sie können die Datenverschlüsselung später aktivieren. Weitere Informationen finden Sie unter [Verschlüsseln von Daten in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) in der Entwickler- und IT-Pro-Hilfe.  

7. Wenn die [!INCLUDE[crm_md](includes/crm_md.md)]-Synchronisierung nicht bereits eingerichtet ist, werden Sie gefragt, ob Sie die Standardsynchronisierungskonfiguration verwenden möchten. Abhängig davon, ob Sie Datensätze in [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] angepasst bleiben sollen, wählen Sie **Ja** oder **Nein** aus.

> [!Note]
> Die Verbindung zu Dynamics 365 Sales mithilfe der Seite **Microsoft Dynamics 365 Sales Verbindungseinrichtung** verlangt möglicherweise von Ihnen dass Sie dem Integrationsadministrator und dem Integrationsbenutzer Sicherheitsrollen für Benutzerkonten zuweisen, die für die Integration verwendet wird. Weitere Informationen finden Sie unter [Weisen Sie einem Benutzer eine Sicherheitsrolle zu](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user).


> [!Note]
> Die Verbindung zu Dynamics 365 Sales mithilfe der Seite **Microsoft Dynamics 365 Sales Verbindungseinrichtung** verlangt möglicherweise von Ihnen dass Sie dem Integrationsadministrator und dem  **Integrationsbenutzer** und **Sicherheitsrollen für Benutzerkonten** [zuweisen](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user), die für die Integration verwendet werden.


### <a name="to-disconnect-from-includecrm_mdincludescrm_mdmd"></a>So trennen Sie [!INCLUDE[crm_md](includes/crm_md.md)]  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Microsoft Dynamics 365 Sales Verbindungseinrichtung** ein, und wählen dann den zugehörigen Link aus.
2. Auf der Seite **Microsoft Dynamics 365 Sales Verbindungseinrichtung** deaktivieren Sie das Kontrollkästchen **Aktiviert**.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension?


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [http://go.microsoft.com/fwlink/?LinkID=616519](http://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](http://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.-->

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [How to: Set Up a Microsoft Dynamics 365 Sales Connection]() -->

<!--
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Siehe auch  
[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  
