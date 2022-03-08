---
title: Integration in Dynamics 365 Sales| Microsoft Docs
description: Erfahren Sie, wie Sie Dynamics 365 Business Central für die Integration mit Dynamics 365 Sales vorbereiten.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: e93d36c2767bc43444b5b23471b6d0aaa0c84adf
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917826"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integration mit Dynamics 365 Sales

Die Rolle des Verkäufers wird häufig als eine der am meisten nach außen gerichteten Tätigkeiten in einem Unternehmen angesehen. Es kann jedoch für Verkäufer hilfreich sein, einen Blick in das Innere des Unternehmens zu werfen und zu erfahren, was am anderen Ende passiert. Durch die Integration von [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie Ihren Verkäufern diese Einblicke ermöglichen, indem Sie es ihnen ermöglichen, diese Informationen in [!INCLUDE[d365fin](includes/d365fin_md.md)] abzurufen, während sie in [!INCLUDE[crm_md](includes/crm_md.md)] arbeiten. Bei der Vorbereitung eines Verkaufsangebots kann es zum Beispiel hilfreich sein, zu wissen, ob ausreichend Lagerbestand vorhanden ist, um die Bestellung zu erfüllen. Weitere Informationen finden Sie unter [Verwenden von Dynamics 365 Sales von Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Dieses Thema beschreibt den Prozess der Integration der Online-Versionen von [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] bis [!INCLUDE[d365fin](includes/cds_long_md.md)]. Informationen zur lokalen Konfiguration finden Sie unter [Dynamics 365 Sales für die lokale Integration vorbereiten](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-common-data-service"></a>Integrieren über Common Data Service
[!INCLUDE[d365fin](includes/d365fin_md.md)] lässt sich auch mit der [!INCLUDE[d365fin](includes/cds_long_md.md)] integrieren, was die Verbindung und Synchronisierung von Daten mit anderen Dynamics 365-Anwendungen wie [!INCLUDE[crm_md](includes/crm_md.md)] oder sogar selbst erstellten Anwendungen erleichtert. Wenn Sie zum ersten Mal integrieren, empfehlen wir Ihnen, dies über [!INCLUDE[d365fin](includes/cds_long_md.md)] zu tun. Weitere Informationen finden Sie unter [Integration mit Common Data Service](admin-common-data-service.md).

Wenn Sie bereits [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[d365fin](includes/d365fin_md.md)] integriert haben, können Sie die Datensynchronisation mit Ihrem Setup fortsetzen. Wenn Sie jedoch Ihre [!INCLUDE[crm_md](includes/crm_md.md)]-Integration aktualisieren oder ausschalten, müssen Sie, um sie wieder einzuschalten, eine Verbindung über [!INCLUDE[d365fin](includes/cds_long_md.md)] herstellen. Weitere Informationen finden Sie unter [Aktualisierung einer Integration mit Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Eine erneute Verbindung über [!INCLUDE[d365fin](includes/cds_long_md.md)] wendet die Standard-Synchronisationseinstellungen an und überschreibt alle Ihre Konfigurationen. Es werden zum Beispiel die Standard-Tabellenzuordnungen angewendet.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integrationseinstellungen, die spezifisch für eine [!INCLUDE[crm_md](includes/crm_md.md)]-Integration sind
Die Integration mit [!INCLUDE[d365fin](includes/d365fin_md.md)] geschieht durch [!INCLUDE[d365fin](includes/cds_long_md.md)], und es gibt eine Menge Standardeinstellungen und Entitäten, die durch die Integration bereitgestellt werden. Zusätzlich zu den Standardeinstellungen gibt es einige, die spezifisch für [!INCLUDE[crm_md](includes/crm_md.md)] sind. In den folgenden Abschnitten werden diese aufgelistet.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Berechtigungen und Sicherheitsrollen für Benutzerkonten im Vertrieb
Wenn Sie die Integrationslösung installieren, werden die Berechtigungen für das Integrationsbenutzerkonto konfiguriert. Wenn diese Berechtigungen geändert werden, müssen Sie sie möglicherweise zurücksetzen. Sie können dies tun, indem Sie die Integrationslösung neu installieren, indem Sie **Integrationslösung neu installieren** auf der Seite **Dynamics 365 Verbindungseinrichtung** wählen. Die folgenden Sicherheitsrollen werden eingesetzt:

* Dynamics 365 Business Central Integrations-Administrator
* Dynamics 365 Business Central Integration Benutzer
* Dynamics 365 Business Central Benutzer der Produktverfügbarkeit

### <a name="connection-settings-in-the-setup-guide"></a>Verbindungseinstellungen im Einrichtungshandbuch

Sie können eine unterstützte Setup-Anleitung verwenden, um die Verbindung schnell einzurichten und erweiterte Funktionen wie die Kopplung zwischen Datensätzen festzulegen.

1. Wählen Sie **Einrichtung und Erweiterungen** und dann **Unterstütztes Setup** aus.
2. Wählen Sie **Dynamics 365 Sales verbindung einrichten**, um den Leitfaden zur unterstützten Einrichtung zu starten.
3. Füllen Sie die Felder je nach Bedarf aus.
4. Optional gibt es erweiterte Einstellungen, die die Sicherheit erhöhen und zusätzliche Funktionen ermöglichen, wie z.B. die Bearbeitung von Kundenaufträgen und die Anzeige von Lagerbeständen. Die erweiterten Einstellungen werden in der folgenden Tabelle beschrieben.  

| Feld | Beschreibung |
|--|--|
| **Import Dynamics 365 Sales Lösung** | Aktivieren Sie dies, um die in Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] einzurichten und zu konfigurieren. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
| **Artikelverfügbarkeits-Webdienst veröffentlichen** | Ermöglichen Sie es Personen, die [!INCLUDE[crm_md](includes/crm_md.md)] verwenden, die Verfügbarkeit von Artikeln (Produkten) im Lager in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzuzeigen. Dies erfordert ein Benutzerkonto [!INCLUDE[d365fin](includes/d365fin_md.md)] mit einem Webdienst-Zugriffsschlüssel. Das Zuordnen des Schlüssels ist ein Vorgang mit zwei Schritten. Im Benutzerkonto in [!INCLUDE[d365fin](includes/d365fin_md.md)] müssen Sie die Aktion **Webdienstschlüssel ändern** auswählen. Im Leitfaden für das unterstützte Setup zum Einrichten der Dynamics 365 Sales Verbindung müssen Sie die Dynamics 365 Business Central-OData-Webdienst-URL festlegen und Benutzeranmeldeinformationen für [!INCLUDE[d365fin](includes/d365fin_md.md)] zum Aufrufen des Diensts bereitstellen. Weitere Informationen finden Sie unter [Odata-Webservice](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **Business Central-OData-Webdienst-URL** | Wenn Sie den Webdienst für die Anzeige der Verfügbarkeit von Artikeln aktivieren, wird Ihnen die URL für den OData Webdienst zur Verfügung gestellt. |
| **Business Central-OData-Webdienst-Benutzername** | Der Name des Benutzerkontos [!INCLUDE[d365fin](includes/d365fin_md.md)], das [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über die Verfügbarkeit von Artikeln in [!INCLUDE[d365fin](includes/d365fin_md.md)] über den OData-Webdienst abzurufen. |
| **Business Central-OData-Webdienst-Zugriffsschlüssel** | Der Zugriffsschlüssel für das Benutzerkonto, das [!INCLUDE[crm_md](includes/crm_md.md)] benutzt, um Informationen über die Verfügbarkeit von [!INCLUDE[d365fin](includes/d365fin_md.md)] über den OData-Webdienst zu erhalten. Der Schlüssel wird dem Benutzer zugewiesen, der im Feld **Business Central-OData-Webdienst-Benutzername** gewählt wurde. Um den Schlüssel zu erhalten, wählen Sie die Schaltfläche **Wert suchen** neben dem Benutzernamen, wählen Sie den Benutzer aus, wählen Sie **Verwalten** und dann **Bearbeiten** aus. In der Benutzerkarte wählen Sie **Aktionen**, **Authentifizierung** und dann **Webdienstschlüssel ändern**. |
| **Verkaufsauftragsintegration aktivieren** | Wenn Personen Verkaufsaufträge in [!INCLUDE[crm_md](includes/crm_md.md)] erstellen und Aufträge in [!INCLUDE[d365fin](includes/d365fin_md.md)] erfüllen, wird dies in den Prozess in [!INCLUDE[crm_md](includes/crm_md.md)] integriert. Weitere Informationen finden Sie unter [Integration für Vertriebsauftragsverarbeitung aktivieren](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Dazu ist es erforderlich, dass Sie Anmeldeinformationen für ein Administratorbenutzerkonto in [!INCLUDE[crm_md](includes/crm_md.md)] zur Verfügung stellen. Weitere Informationen finden Sie im Abschnitt [Verarbeiten von Verkaufsauftragsdaten](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
| **CDS-Verbindung aktivieren** | Aktivieren Sie die Verbindung mit [!INCLUDE[d365fin](includes/cds_long_md.md)]. |
| **Dynamics 365-SDK-Version** | Dies ist nur relevant, wenn Sie eine lokale Version von [!INCLUDE[crm_md](includes/crm_md.md)] integrieren. Das ist das Dynamics 365 Software Development Kit (wird auch als Xrm bezeichnet), das Sie verwenden, um eine Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] herzustellen. Die Version muss mit der SDK-Version kompatibel sein, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird, und der Version von [!INCLUDE[crm_md](includes/crm_md.md)] entsprechen oder neuer sein. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Verbindungseinstellungen auf der Seite Microsoft Dynamics 365 Verbindungsaufbau

Geben Sie die folgenden Informationen über die Verbindung von [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[d365fin](includes/d365fin_md.md)] ein.

| Feld | Beschreibung |
|--|--|
| **Dynamics 365 Sales URL** | Die URL Ihrer [!INCLUDE[crm_md](includes/crm_md.md)]-Instanz. Dies ermöglicht es Benutzern, entsprechende Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] von Datensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] zu öffnen, wie z.B. ein Konto oder ein Produkt. Die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] geöffnet. |
|**Dynamics 365 Sales URL**|Die URL Ihrer [!INCLUDE[crm_md](includes/crm_md.md)]-Instanz. Dies ermöglicht es Benutzern, entsprechende Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] von Datensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] zu öffnen, wie z.B. ein Konto oder ein Produkt. Die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensätze werden in [!INCLUDE[d365fin](includes/d365fin_md.md)] geöffnet.|
|**Artikelverfügbarkeits-Webdienst aktiviert**|Geben Sie Personen, die [!INCLUDE[crm_md](includes/crm_md.md)] verwenden, die Möglichkeit, die Verfügbarkeit von Artikeln (Produkten) im Bestand in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzuzeigen. Wenn Sie dies aktivieren, müssen Sie auch einen Benutzernamen und einen Zugriffsschlüssel für [!INCLUDE[crm_md](includes/crm_md.md)] angeben, um den OData-Webdienst nach der Verfügbarkeit von Artikeln (Produkten ) abzufragen. Weitere Informationen finden Sie unter [Odata-Webservice](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**Dynamics 365 Business Central-OData-Webdienst-URL**|Wenn Sie den Artikelverfügbarkeits-Webdienst aktivieren, wird Ihnen die URL für den OData-Webdienst bereitgestellt. Legen Sie für dieses Feld die URL der zu verwendenden [!INCLUDE[d365fin](includes/d365fin_md.md)]-Instanz fest.<br /><br /> Um das Feld zur Standard-URL für [!INCLUDE[d365fin](includes/d365fin_md.md)] zurückzusetzen, wählen Sie die Aktion **Webclient-URL zurücksetzen** aus.<br /><br /> Dieses Feld ist nur relevant, wenn die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] installiert ist.|
|**Dynamics 365 Business Central-OData-Webdienst-Benutzername**|Der Name des Benutzerkontos, den [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über die Artikelverfügbarkeit aus [!INCLUDE[d365fin](includes/d365fin_md.md)] über den OData-Webdienst abzurufen.|
|**Dynamics 365 Business Central-OData-Webdienst-Zugriffsschlüssel**|Der Zugriffsschlüssel des Benutzerkontos, das [!INCLUDE[crm_md](includes/crm_md.md)] verwendet, um Informationen über Artikelverfügbarkeit aus [!INCLUDE[d365fin](includes/d365fin_md.md)] über den OData-Webdienst abzurufen. Der Schlüssel wird dem Benutzer zugeordnet, der im Feld **Dynamics 365 Business Central-OData-Webdienst-Benutzername** ausgewählt ist. Um den Schlüssel zu erhalten, wählen Sie die Schaltfläche **Wert suchen** neben dem Benutzernamen, wählen Sie den Benutzer aus, wählen Sie **Verwalten** und dann **Bearbeiten** aus. In der Benutzerkarte wählen Sie **Aktionen**, **Authentifizierung** und dann **Webdienstschlüssel ändern**.|
|**Dynamics 365 SDK Version**|Wenn Sie eine Integration in einer lokale Version von [!INCLUDE[crm_md](includes/crm_md.md)] durchführen, verwenden Sie dieses Dynamics 365 Software Development Kit (wird auch als Xrm bezeichnet), um [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] zu verbinden. Die Version, die Sie auswählen, muss mit der SDK-Version kompatibel sein, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird. Diese Version gleicht der Version, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird oder ist neuer.|-->

Zusätzlich zu den oben genannten Einstellungen geben Sie folgende Einstellungen für [!INCLUDE[crm_md](includes/crm_md.md)] ein.

| Feld | Beschreibung |
|--|--|
| **Auftragsintegration ist aktiviert** | Ermöglichen Sie es Benutzern, Verkaufsaufträge und aktivierte Angebote in [!INCLUDE[crm_md](includes/crm_md.md)] zu senden und sie dann in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzuzeigen und zu bearbeiten. Dies integriert den Prozess in [!INCLUDE[crm_md](includes/crm_md.md)]. Weitere Informationen finden Sie unter [Integration für Vertriebsauftragsverarbeitung aktivieren](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Verkaufsaufträge automatisch erstellen** | Erstellen Sie einen Verkaufsauftrag in [!INCLUDE[d365fin](includes/d365fin_md.md)], wenn ein Benutzer einen in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt und sendet. |
| **Verkaufsangebote automatisch verarbeiten** | Verarbeiten Sie ein Verkaufsangebot in [!INCLUDE[d365fin](includes/d365fin_md.md)], wenn ein Benutzer eins in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt und aktiviert. |

<!--
### User Account Settings
Integrate with Business Central through Common Data Service requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Standard-Sales-Entitätszuordnungen für die Synchronisierung

Entitäten in [!INCLUDE[crm_md](includes/crm_md.md)], wie z.B. Bestellungen, werden mit äquivalenten Typen von Entitäten in [!INCLUDE[d365fin](includes/d365fin_md.md)] integriert, wie z.B. Debitorenaufträge. Um mit [!INCLUDE[crm_md](includes/crm_md.md)]-Daten zu arbeiten, richten Sie Verknüpfungen, auch Kopplungen genannt, zwischen Einheiten in [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] ein.

Die folgende Tabelle zeigt die standardmäßige Zuordnung zwischen Einheiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)], die [!INCLUDE[crm_md](includes/crm_md.md)] bietet.

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synchronisierungsrichtung | Standardfilter |
|--|--|--|--|
| Einheit | Einheiten-Gruppe | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Artikel | Produkt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Vertriebskontaktfilter: **Produkt-Typ** ist **Verkaufs-Lager** |
| Ressource | Produkt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Vertriebskontaktfilter: **Produkt-Typ** ist **Service** |
| Debitorenpreisgruppe | VK-Preisliste | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkaufspreis | Produkt-Preisliste | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] Kontaktfilter: **Verkaufscode** ist nicht leer, **Verkaufsart** ist **Debitorenpreisgruppe** |
| Verkaufschance | Verkaufschance | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |
| Verkaufsrechnungskopf | Fakturieren | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkaufsrechnungszeile | Rechnungsprodukt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkaufsauftrags-Kopf | Verkaufsauftrag | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] Verkaufskopffilter: **Dokumentart** ist Auftrag. **Status** ist freigegeben |
| Hinweise zu Verkaufsaufträgen | Hinweise zu Verkaufsaufträgen | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |

### <a name="synchronization-rules"></a>Synchronisierungsregeln

Die folgende Tabelle listet die Regeln auf, die die Synchronisation zwischen [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] steuern. Diese kommen zu den für Common Data Service definierten Regeln hinzu, die ebenfalls gelten. Weitere Informationen finden Sie unter [Standard-Entitätszuordnung für die Synchronisation](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-entity-mapping-for-synchronization).

> [!NOTE]  
> Änderungen an Daten, die vom Integrationsbenutzerkonto vorgenommen wurden, werden nicht synchronisiert. Daher empfiehlt es sich, bei der Nutzung dieses Kontos keine Daten zu ändern. Weitere Informationen finden Sie unter [Einrichten des Benutzerkontos für die Integration in Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tisch|Regel|
|-----|----|
|Einheiten|Maßeinheiten werden mit Einheitengruppen in [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert. Es kann nur eine Einheit in der Einheitengruppe definiert sein.|
|Artikel|Wenn Artikel mit [!INCLUDE[crm_md](includes/crm_md.md)] Produkten synchronisiert werden, erstellt [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch eine Preisliste in [!INCLUDE[crm_md](includes/crm_md.md)]. Um Synchronisationsfehler zu vermeiden, sollten Sie diese Preisliste nicht manuell ändern.|
|Ressourcen|Ressourcen werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Produkten synchronisiert, die den Produkttyp-Service haben.|
|Debitorenpreisgruppen|Debitorenpreisgruppen werden mit Verkaufspreislisten synchronisiert.|
|Verkaufspreise|Verkaufspreise, die Verkaufsart Debitorenpreisgruppe haben und einen definierten Verkaufscode haben werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Preislistenzeilen synchronisiert|
|Verkaufschancen|Chancen werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Chancen synchronisiert. Der Verkäufer-Codewert definiert den Besitzer der gekoppelten Einheit in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Gebuchte Verkaufsrechnungen|Gebuchte Verkaufsrechnungen werden mit Verkaufsrechnungen synchronisiert. Bevor eine Rechnung synchronisiert werden kann, ist es besser, alle anderen Einheiten, die in der Rechnung teilnehmen können, von Verkäufer zu Preislisten zu synchronisieren. Der Verkäufer-Codewert im Rechnungskopf definiert den Besitzer der gekoppelten Einheit im Verkauf.|
|Verkaufsaufträge|Wenn die Verkaufsauftragsintegration aktiviert ist, werden Verkaufsaufträge in [!INCLUDE[d365fin](includes/d365fin_md.md)], die aus übermittelten Verkaufsaufträgen in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt werden, mit Verkaufsaufträgen in INCLUDE SALES synchronisiert, wenn sie freigegeben werden. Vor dem Synchronisieren von Aufträgen wird empfohlen, zunächst alle an dem Auftrag beteiligten Entitäten zu synchronisieren, z. B. Verkäufer und Preislisten. Das Verkäufer-Codefeld im Auftragskopf definiert den Besitzer der gekoppelten Einheiten in [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Synchronisierungsaufträge für eine Vertriebsintegration

Die Projekte werden in der folgenden Reihenfolge ausgeführt, um Kopplungsabhängigkeiten zwischen Einheiten zu vermeiden. Bei Common Data Service sind zusätzliche Aufträge verfügbar. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](/dynamics365/business-central/admin-job-queues-schedule-tasks)

1. UNITOFMEASURE - Dynamics 365 Sales Synchronisierungsauftrag  
2. RESSOURCE-PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag  
3. ARTIKEL - PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag  
4. CUSTPRCGRP-PRICE- Synchronisierungsauftrag „Dynamics 365 Sales“.
5. SALESPRC-PRODPRICE - Synchronisierungsauftrag „Dynamics 365 Sales“.
6. POSTEDSALESINV-INV - Dynamics 365 Sales-Synchronisierungsauftrag.

### <a name="default-synchronization-job-queue-entries"></a>Standardmäßige Synchronisierungsprojektwarteschlangenposten

Die folgende Tabelle beschreibt die Standardsynchronisierungsjobs für Sales.  

|Aufgabenwarteschlangenposten|Beschreibung|Richtung|Integrationstabellenzuordnung|Standard-Synchronisationsfrequenz (Minuten)|Standard-Inaktivitätsruhezustand (Minuten)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|UNITOFMEASURE - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Einheitsgruppen mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Maßeinheiten.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|MASSEINHEIT|30|720<br> (12 Std.)|
|RESSOURCE-PRODUCT - Dynamics 365 Sales Vertriebssynchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Ressourcen.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE – PRODUKT|30|720<br> (12 Std.)|
|ARTIKEL - PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Artikeln.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL/PRODUKT|30|1440<br> (24 Std.)|
|CUSTPRCGRP-PREIS - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Verkaufspreislisten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitorenpreisgruppen.| |DEBITORENPREISGRUPPEN – VERKAUFSPREISLISTEN|30|1440<br> (24 Std.)|
|SALESPRC-PRODUCTPRICE - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produktpreise mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Verkaufspreisen.||PRODUKTPREIS – VERKAUFSPREIS|30|1440<br> (24 Std.)|
|POSTEDSALESINV-INV - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Rechnungen mit gebuchten [!INCLUDE[d365fin](includes/d365fin_md.md)]-Verkaufsrechnungen.|Von [!INCLUDE[d365fin](includes/d365fin_md.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|RECHNUNGEN – GEBUCHTE VERKAUFSRECHNUNGEN|30|1440<br> (24 Std.)|
|Debitorenstatistik - Dynamics 365 Sales Synchronisierungsauftrag|Aktualisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Konten mit den neuesten [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitorendaten. In [!INCLUDE[crm_md](includes/crm_md.md)] erscheinen diese Informationen im **Business Central-Kontostatistik**-Schnellansichtsformular von Konten, die mit [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren gekoppelt werden.<br /><br /> Diese Daten können auch manuell für jeden Debitorendatensatz aktualisiert werden. Weitere Informationen finden Sie unter [Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Hinweis:** Dieser Projektwarteschlangeneintrag ist nur relevant, wenn die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] installiert ist. |Nicht anwendbar|Nicht anwendbar|30|Nicht anwendbar| 

### <a name="note-for-on-premises-versions"></a>Hinweis für Vor-Ort-Versionen

> [!Note]
> Wenn Sie eine lokale Version von [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] verbinden und eine Verbindung zu einer [!INCLUDE[crm_md](includes/crm_md.md)]-Instanz mit einem bestimmten Authentifizierungstyp konfigurieren möchten, füllen Sie die Felder unter **Authentifizierungstyp-Details** aus. Weitere Informationen finden Sie unter [Verwenden der Verbindungszeichenfolgen in XRM-Tooling zum herstellen einer Verbindung mit Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Dieser Schritt ist nicht erforderlich, wenn sie eine Verbindung mit einer Onlineversion von [!INCLUDE[d365fin](includes/d365fin_md.md)] herstellen.

## <a name="see-also"></a>Siehe auch

[Einrichten des Benutzerkontos für die Integration in [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Richten Sie eine Verbindung mit [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md) ein  
[Synchronisieren von Business Central und [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Vorbereiten der Integration in Dynamics 365 Sales für die lokale Integration](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
