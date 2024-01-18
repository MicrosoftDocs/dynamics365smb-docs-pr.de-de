---
title: Integration mit Dynamics 365 Sales
description: 'Erfahren Sie, wie Sie Dynamics 365 Business Central für die Integration mit Dynamics 365 Sales vorbereiten.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 09/28/2023
ms.author: bholtorf
ms.custom: bap-template
---
# <a name="integrating-with-dynamics-365-sales"></a>Integration mit Dynamics 365 Sales

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Die Rolle des Verkäufers wird häufig als eine der am meisten nach außen gerichteten Tätigkeiten in einem Unternehmen angesehen. Es kann jedoch für Verkäufer hilfreich sein, einen Blick in das Innere des Unternehmens zu werfen und zu erfahren, was am anderen Ende passiert. Durch die Integration von [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] können Sie Ihren Vertriebsmitarbeitern diesen Einblick geben. Durch die Integration können die Mitarbeiter Informationen in [!INCLUDE[prod_short](includes/prod_short.md)] einsehen, während sie in [!INCLUDE[crm_md](includes/crm_md.md)] arbeiten. Bei der Vorbereitung eines Verkaufsangebots kann es zum Beispiel hilfreich sein, zu wissen, ob ausreichend Lagerbestand vorhanden ist, um die Bestellung zu erfüllen. Weitere Informationen finden Sie unter [Dynamics 365 Sales von Business Central verwenden](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Dieses Thema beschreibt den Prozess der Integration der Online-Versionen von [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] bis [!INCLUDE[prod_short](includes/cds_long_md.md)]. Informationen zur lokalen Konfiguration finden Sie unter [Dynamics 365 Sales für die lokale Integration vorbereiten](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrate-through-dataverse"></a>Integrieren über Dataverse

Um die Verbindung und Synchronisierung von Daten mit anderen Dynamics 365-Anwendungen zu erleichtern, lässt sich [!INCLUDE[prod_short](includes/prod_short.md)] auch mit [!INCLUDE[prod_short](includes/cds_long_md.md)] integrieren. Sie können zum Beispiel eine Verbindung zu [!INCLUDE[crm_md](includes/crm_md.md)] herstellen, oder sogar zu Apps, die Sie selbst erstellen. Wenn Sie die Integration zum ersten Mal vornehmen, müssen Sie dies über [!INCLUDE[prod_short](includes/cds_long_md.md)] tun. Weitere Informationen finden Sie unter [Integration mit Dataverse](admin-common-data-service.md).

Wenn Sie [!INCLUDE[crm_md](includes/crm_md.md)] bereits mit [!INCLUDE[prod_short](includes/prod_short.md)] integriert haben, können Sie Ihre Daten weiterhin über Ihre Einrichtung synchronisieren. Wenn Sie jedoch Ihre [!INCLUDE[crm_md](includes/crm_md.md)]-Integration aktualisieren oder ausschalten, müssen Sie, um sie wieder einzuschalten, eine Verbindung über [!INCLUDE[prod_short](includes/cds_long_md.md)] herstellen. Weitere Informationen finden Sie unter [Aktualisierung einer Integration mit Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Eine erneute Verbindung über [!INCLUDE[prod_short](includes/cds_long_md.md)] wendet die Standard-Synchronisationseinstellungen an und überschreibt alle Ihre Konfigurationen. Es werden zum Beispiel die Standard-Tabellenzuordnungen angewendet.

## <a name="integration-settings-that-are-specific-to-a--integration"></a>Integrationseinstellungen, die spezifisch für eine [!INCLUDE[crm_md](includes/crm_md.md)]-Integration gelten

Die Integration mit [!INCLUDE[prod_short](includes/prod_short.md)] erfolgt über [!INCLUDE[prod_short](includes/cds_long_md.md)], und es werden viele Standardeinstellungen und Tabellen bereitgestellt. Zusätzlich zu den Standardeinstellungen gibt es einige, die spezifisch für [!INCLUDE[crm_md](includes/crm_md.md)] sind. In den folgenden Abschnitten sind diese Einstellungen aufgeführt.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Berechtigungen und Sicherheitsrollen für Benutzerkonten in Sales

Wenn Sie die Integrationslösung installieren, werden die Berechtigungen für das Integrationsbenutzerkonto konfiguriert. Wenn diese Berechtigungen geändert werden, müssen Sie sie möglicherweise zurücksetzen. Sie können dies tun, indem Sie die Integrationslösung neu installieren, indem Sie **Integrationslösung neu installieren** auf der Seite **Dynamics 365 Verbindungseinrichtung** wählen. Die folgenden Sicherheitsrollen werden eingesetzt:

* Dynamics 365 Business Central Integrations-Administrator
* Dynamics 365 Business Central Integration Benutzer
* Dynamics 365 Business Central Benutzer der Produktverfügbarkeit

### <a name="connection-settings-in-the-setup-guide"></a>Verbindungseinstellungen im Einrichtungshandbuch

Sie können eine unterstützte Setup-Anleitung verwenden, um die Verbindung schnell einzurichten und erweiterte Funktionen wie die Kopplung zwischen Datensätzen festzulegen.

1. Wählen Sie **Einrichtung und Erweiterungen** und dann **Unterstütztes Setup** aus.
2. Wählen Sie **Dynamics 365 Sales verbindung einrichten**, um den Leitfaden zur unterstützten Einrichtung zu starten.
3. Füllen Sie die Felder je nach Bedarf aus.
4. Optional gibt es erweiterte Einstellungen, mit denen Sie die Sicherheit erhöhen und mehr Funktionalitäten aktivieren können. Die erweiterten Einstellungen werden in der folgenden Tabelle beschrieben.  

| Feld | Description |
|--|--|
| **Import Dynamics 365 Sales Lösung** | Installieren und konfigurieren Sie die Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
|**Automatische Synchronisierung der Artikelverfügbarkeit**|Legt fest, dass die Warteschlange für die Artikelverfügbarkeit geplant werden muss. Die Auftragswarteschlange wird alle 30 Minuten ausgeführt und aktualisiert die Verfügbarkeit der gekoppelten Artikel.|
| **Veraltete Verkaufsauftragsintegration aktivieren** | Wenn Personen in [!INCLUDE[crm_md](includes/crm_md.md)] Verkaufsaufträge erstellen und in [!INCLUDE[prod_short](includes/prod_short.md)] Aufträge erfüllen, wird der Prozess mit dieser Einstellung in [!INCLUDE[crm_md](includes/crm_md.md)] integriert. Weitere Informationen finden Sie unter [Integration der Verarbeitung von Verkaufsaufträgen aktivieren](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).<br><br>**Hinweis:** Sie können diese Option nicht verwenden, wenn Sie die Option **Bidirektionale Synchronisierung von Verkaufsaufträgen** verwenden. Die beiden Einstellungen schließen sich gegenseitig aus. Weitere Informationen zu dieser Option finden Sie unter [Einzel- und bidirektionale Synchronisierung von Verkaufsaufträgen](#single-and-bi-directional-synchronization-of-sales-orders). |
|**Dynamics 365 Sales-Verbindung aktivieren** | Aktivieren Sie die Verbindung mit [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Dynamics 365 SDK Version** | Dies ist nur relevant, wenn Sie eine Integration mit einer lokalen Version von [!INCLUDE[crm_md](includes/crm_md.md)] vornehmen. Dieses SDK ist das Dynamics 365 Software Development Kit (auch als Xrm bezeichnet), das Sie für die Verbindung von [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] verwenden. Die Version muss mit der SDK-Version kompatibel sein, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird, und der Version von [!INCLUDE[crm_md](includes/crm_md.md)] entsprechen oder neuer sein. |
|**Bidirektionale Synchronisierung von Verkaufsaufträgen**|Synchronisieren Sie Verkaufsaufträge in beide Richtungen. Um mehr über diese Option zu erfahren, gehen Sie zu [Einzel- und bidirektionale Synchronisierung von Verkaufsaufträgen](#single-and-bi-directional-synchronization-of-sales-orders).<br><br>**Hinweis:** Sie können diese Option nicht verwenden, wenn Sie die Option **Veraltete Verkaufsauftragsintegration aktivieren** verwenden. Die beiden Einstellungen schließen sich gegenseitig aus.|

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Verbindungseinstellungen auf der Seite Microsoft Dynamics 365 Verbindungseinrichtung

Geben Sie die folgenden Informationen über die Verbindung von [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[prod_short](includes/prod_short.md)] ein.

| Feld | Description |
|--|--|
|**Dynamics 365 Sales URL**|Die URL Ihrer [!INCLUDE[crm_md](includes/crm_md.md)]-Instanz. Mit dieser Einstellung können Benutzer die Datensätze in [!INCLUDE[prod_short](includes/prod_short.md)] öffnen, die den Datensätzen in [!INCLUDE[crm_md](includes/crm_md.md)] entsprechen. Zum Beispiel ein Konto oder ein Produkt. Die [!INCLUDE[prod_short](includes/prod_short.md)]-Datensätze werden in [!INCLUDE[prod_short](includes/prod_short.md)] geöffnet.|
|**Automatische Synchronisierung der Artikelverfügbarkeit**|Legt fest, dass die Warteschlange für die Artikelverfügbarkeit geplant werden muss. Die Auftragswarteschlange wird alle 30 Minuten ausgeführt und aktualisiert die Verfügbarkeit der gekoppelten Artikel.|
|**Dynamics 365 SDK Version**|Wenn Sie eine Integration mit einer lokalen Version von [!INCLUDE[crm_md](includes/crm_md.md)] vornehmen, ist dies das Dynamics 365 Software Development Kit (auch Xrm genannt), das Sie für die Verbindung von [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] verwenden. Die Version, die Sie auswählen, muss mit der SDK-Version kompatibel sein, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird. Diese Version gleicht der Version, die von [!INCLUDE[crm_md](includes/crm_md.md)] verwendet wird oder ist neuer.|

Zusätzlich zu den oben genannten Einstellungen geben Sie folgende Einstellungen für [!INCLUDE[crm_md](includes/crm_md.md)] ein.

| Feld | Beschreibung |
|--|--|
| **Auftragsintegration ist aktiviert** | Ermöglichen Sie es Benutzern, Verkaufsaufträge und aktivierte Angebote in [!INCLUDE[crm_md](includes/crm_md.md)] zu senden und sie dann in [!INCLUDE[prod_short](includes/prod_short.md)] anzuzeigen und zu bearbeiten. Mit dieser Einstellung wird der Prozess in [!INCLUDE[crm_md](includes/crm_md.md)] integriert. Weitere Informationen finden Sie unter [Integration der Verarbeitung von Verkaufsaufträgen aktivieren](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Verkaufsaufträge automatisch erstellen** | Erstellen Sie einen Verkaufsauftrag in [!INCLUDE[prod_short](includes/prod_short.md)], wenn ein Benutzer einen in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt und sendet. |
| **Verkaufsangebote automatisch verarbeiten** | Verarbeiten Sie ein Verkaufsangebot in [!INCLUDE[prod_short](includes/prod_short.md)], wenn ein Benutzer eins in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt und aktiviert. Weitere Informationen finden Sie im Abschnitt [Handhaben von Verkaufsangebotsdaten](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |
|**Bidirektionale Synchronisierung von Verkaufsaufträgen**|Synchronisieren Sie Verkaufsaufträge in beide Richtungen. Weitere Informationen zu dieser Option finden Sie unter [Einzel- und bidirektionale Synchronisierung von Verkaufsaufträgen](#single-and-bi-directional-synchronization-of-sales-orders).|
<!--
### <a name="user-account-settings"></a>User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->
### <a name="single-and-bi-directional-synchronization-of-sales-orders"></a>Einzel- und bidirektionale Synchronisierung von Verkaufsaufträgen

Wenn Sie Ihre Integration einrichten, entweder über den Einrichtungsleitfaden oder die Seite „Microsoft Dynamics 365 Verbindungseinrichtung“, gibt es Optionen, die die Richtung steuern, in der Sie Verkaufsaufträge synchronisieren, sowie zur Übermittlung.

Mit der Option **Bidirektionale Synchronisierung von Verkaufsaufträgen** können Sie Verkaufsaufträge aus Sales mit [!INCLUDE [prod_short](includes/prod_short.md)] synchronisieren und umgekehrt. Ändert ein Debitor beispielsweise seine Meinung über das Produkt oder die Menge, die er in [!INCLUDE[crm_md](includes/crm_md.md)] bestellt hat, können Sie den Verkaufsauftrag archivieren und einen neuen in [!INCLUDE[prod_short](includes/prod_short.md)] erstellen. Dasselbe gilt für Änderungen in [!INCLUDE[prod_short](includes/prod_short.md)]. Wenn sich beispielsweise Preise, Steuerbeträge oder voraussichtliche Warenausgangsdaten ändern, werden die Änderungen mit [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert. Die bidirektionale Synchronisierung hilft Ihren Vertriebsmitarbeitenden, über die neuesten Änderungen und den Status von Verkaufsaufträgen auf dem Laufenden zu bleiben.

Bei der bidirektionalen Synchronisierung machen Sie Verkaufsaufträge für die Synchronisierung verfügbar, wenn Sie ihren Status in Sales in **Übermittelt** ändern. Wenn Sie diesen Status festlegen, können Sie die Informationen in den Zeilen des Auftrags nicht mehr ändern. Beim Synchronisieren wird der Auftrag an [!INCLUDE [prod_short](includes/prod_short.md)] mit dem Status **Freigegeben** übertragen. Wenn ein Fehler auftritt, können Sie den Auftrag auf **Offen** (in [!INCLUDE [prod_short](includes/prod_short.md)]) oder **Aktiv** (in Sales) zurücksetzen und dann Zeilen hinzufügen oder löschen, um den Fehler zu korrigieren. Anschließend können Sie den Auftrag erneut einreichen.

> [!TIP]
> Wenn Sie die Option **Bidirektionale Synchronisierung von Verkaufsaufträgen** aktivieren, erstellt [!INCLUDE [prod_short](includes/prod_short.md)] einen Datensatz auf der Seite **Verkaufsauftragsarchive**, wenn Sie Informationen zu einem Auftrag veröffentlichen oder ändern. Die archivierten Versionen können beispielsweise nützlich sein, um sich den Verlauf eines Auftrags anzusehen.

Die Option **Veraltete Verkaufsauftragsintegration aktivieren** synchronisiert nur von Sales nach [!INCLUDE [prod_short](includes/prod_short.md)]. Für diese Option verwenden Sie die Aktion **Übermitteln** in Sales, um Aufträge für die Synchronisierung verfügbar zu machen. Wenn Sie dies tun, können Sie keine Informationen in dem Auftrag mehr ändern. Beim Synchronisieren wird der Auftrag an [!INCLUDE [prod_short](includes/prod_short.md)] mit dem Status **Freigegeben** übertragen.

Um diese Option nutzen zu können, müssen Sie Anmeldeinformationen für ein Administrator-Benutzerkonto in [!INCLUDE[crm_md](includes/crm_md.md)] angeben. Weitere Informationen finden Sie im Abschnitt [Verarbeiten von Verkaufsauftragsdaten](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!NOTE]
> Die Optionen **Bidirektionale Synchronisierung von Verkaufsaufträgen** und **Veraltete Verkaufsauftragsintegration aktivieren** schließen sich gegenseitig aus. Sie können nicht beide Optionen gleichzeitig nutzen.

Bei beiden Optionen zeigt [!INCLUDE [prod_short](includes/prod_short.md)] alle Verkaufsaufträge mit dem Status **Übermittelt** auf der Seite **Aufträge – Microsoft Dynamics 365 Sales**.

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Standard-Sales-Entitätszuordnungen für die Synchronisierung

Entitäten in [!INCLUDE[crm_md](includes/crm_md.md)], wie z.B. Bestellungen, werden mit äquivalenten Typen von Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] integriert, wie z.B. Debitorenaufträge. Um mit [!INCLUDE[crm_md](includes/crm_md.md)]-Daten zu arbeiten, richten Sie Verknüpfungen, auch Kopplungen genannt, zwischen Tabellen in [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] ein.

Die folgende Tabelle zeigt die standardmäßige Zuordnung zwischen Tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/prod_short.md)], die [!INCLUDE[crm_md](includes/crm_md.md)] bietet.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synchronisierungsrichtung | Standardfilter |
|--|--|--|--|
| Einheit | Einheiten-Gruppe | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Artikel | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Vertriebskontaktfilter: **Produkt-Typ** ist **Verkaufs-Lager** |
| Ressource | Produkt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Vertriebskontaktfilter: **Produkt-Typ** ist **Service** |
| Artikeleinheit | CRM-Einheit |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
| Ressourceneinheit | CRM-Einheit |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]||
| Einheiten-Gruppe | CRM Uomschedule | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ||
| Debitorenpreisgruppe | VK-Preisliste | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkaufspreis | Produkt-Preisliste | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)] Kontaktfilter: **Verkaufscode** ist nicht leer, **Verkaufstyp** ist **Kundenpreisgruppe** |
| Verkaufschance | Verkaufschance | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Verkaufsrechnungskopf | Fakturieren | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkaufsrechnungszeile | Rechnungsprodukt | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkaufsauftrags-Kopf | Verkaufsauftrag | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] <br><br> Um in beide Richtungen zu synchronisieren, müssen Sie den Schalter **Bidirektionale Synchronisierung von Verkaufsaufträgen** auf der Seite **Dynamics 365 Connection Einrichtung** aktivieren.| [!INCLUDE[prod_short](includes/prod_short.md)] Verkaufskopffilter: **Dokumentart** ist Auftrag. **Status** ist freigegeben |
| Hinweise zu Verkaufsaufträgen | Hinweise zu Verkaufsaufträgen | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> Die Zuordnungen für die Tabellen Artikeleinheit, Ressourceneinheit und Einheitengruppe sind nur verfügbar, wenn Ihr Administrator die Option **Funktionsupdate: Synchronisierung mehrerer Einheiten mit Dynamics 365 Sales** auf der Seite **Funktionsverwaltung** aktiviert hat. Weitere Informationen finden Sie unter [Synchronisieren von Artikeln und Ressourcen mit Produkten in verschiedenen Einheiten](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronizing-items-and-resources-with-products-with-different-units-of-measure).

## <a name="synchronize-items-and-resources-with-products-with-different-units-of-measure"></a>Synchronisieren von Artikeln und Ressourcen mit Produkten in verschiedenen Einheiten

Unternehmen produzieren oder kaufen die Artikel oft in einer Einheit und verkaufen sie dann in einer anderen. Um Artikel zu synchronisieren, die mehrere Einheiten verwenden, müssen Sie den Funktionsschalter **Funktionsupdate: Synchronisierung mehrerer Einheiten mit Dynamics 365 Sales** auf der Seite **Funktionsverwaltung** aktivieren. 

Wenn Sie die Funktion Update einschalten, wird eine neue Einheitentabelle erstellt und jedem Artikel und jeder Ressource in [!INCLUDE[prod_short](includes/prod_short.md)] zugewiesen. Über die Tabellen können Sie die Tabellen Einheitengruppe, Artikel Einheiten und Ressourcen Einheiten in [!INCLUDE[prod_short](includes/prod_short.md)] der Dynamics 365 Sales Einheitengruppe in [!INCLUDE[crm_md](includes/crm_md.md)] zuordnen. Das folgende Bild zeigt die Zuordnungen.

:::image type="content" source="media/unit group 1.png" alt-text="Tabellenzuordnungen für Einheitengruppen":::

Sie können für jede Einheitengruppe mehrere Einheiten erstellen und die Gruppen den Produkten in [!INCLUDE[crm_md](includes/crm_md.md)] zuweisen. Danach können Sie die Produkte mit Artikeln und Ressourcen in [!INCLUDE[prod_short](includes/prod_short.md)] synchronisieren. Sie können Artikeleinheiten oder Ressourceneinheiten manuell mit einer Einheitengruppe koppeln. Wenn Sie dies tun und die Einheitengruppe für den Artikel oder die Ressource nicht mit einer Einheitengruppe in [!INCLUDE[crm_md](includes/crm_md.md)] gekoppelt ist, z.B. weil die Einheitengruppe nicht vorhanden war, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] automatisch die Einheitengruppe in [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="map-items-and-resources-to-products"></a>Zuordnen von Artikeln und Ressourcen zu Produkten

Wenn Sie das **Funktionsupdate: Synchronisierung mehrerer Einheiten mit Dynamics 365 Sales** aktivieren, passiert Folgendes:

* Für Elemente und Ressourcen werden neue Zuordnungen erstellt.
* Vorhandene Zuordnungen werden gelöscht. <!--which mappings?-->
* Bei einer Datenaktualisierung werden Einheitengruppen für Artikel und Ressourcen erstellt.

Um die neuen Zuordnungen zu verwenden, müssen Sie Einheitengruppen, Artikeleinheiten und Ressourceneinheiten synchronisieren. Sie müssen auch Elemente und Ressourcen neu synchronisieren. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] erlaubt Ihnen nicht, eine Einheitengruppe für ein Produkt zu ändern. Daher müssen Sie Ihre Produkte stilllegen und die Artikel und Ressourcen entkoppeln und dann synchronisieren, indem Sie neue Produkte in [!INCLUDE[crm_md](includes/crm_md.md)] erstellen. 

Die folgenden Schritte beschreiben die Schritte zum Starten der Zuordnung von Einheitengruppen:

1. Stellen Sie sicher, dass Produkte in [!INCLUDE[crm_md](includes/crm_md.md)] nicht mit Artikeln oder Ressourcen in [!INCLUDE[prod_short](includes/prod_short.md)] gekoppelt sind. Wenn ja, wechseln Sie zu den Seiten **Artikel** und/oder **Ressourcen**, und verwenden Sie die Filteroptionen, um die gekoppelten Datensätze auszuwählen. Verwenden Sie dann die Aktion **Dynamics 365 Sales**, und wählen Sie **Entkoppeln** aus. Diese Aktion plant einen Hintergrundjob ein, um die Datensätze zu entkoppeln. Während der Vorgang ausgeführt wird, können Sie seinen Status überprüfen, indem Sie die Aktion **Synchronisationsprotokoll** verwenden. Weitere Informationen finden Sie unter [Koppeln und Synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Da in [!INCLUDE[crm_md](includes/crm_md.md)] neue Produkte mit neuen Einheitengruppen erstellt werden, führen Sie einen der folgenden Schritte aus, um doppelte Namen zu vermeiden:
    
  * Benennen Sie Ihre Produkte um und entfernen Sie sie dann in [!INCLUDE[crm_md](includes/crm_md.md)]. Weitere Informationen finden Sie unter [Produkte zurückziehen (Vertriebshub)](/dynamics365/sales-enterprise/retire-product). Melden Sie sich zur Massenbearbeitung Ihrer Produkte in Microsoft Excel bei Power Apps an, wählen Sie Ihre Umgebung aus, wechseln Sie zur Tabelle **Produkt**, und wählen Sie dann die Registerkarte **Daten** aus. Löschen Sie alle angewendeten Filter. In der Gruppe **Daten** wähle Sie **Daten in Excel bearbeiten** aus. Fügen Sie den gekoppelten Produkten ein Präfix oder Suffix hinzu, und entfernen Sie sie dann.
    * Stellen Sie Ihre Produkte ein und löschen Sie sie. 

3. Befolgen Sie diese Schritte zum Synchronisieren von **Einheitengruppen**, **Einheit**, **Produkte** und **Ressourcen**:
    1. Öffnen Sie in [!INCLUDE[prod_short](includes/prod_short.md)] die Seite **Dynamics 365 Sales-Verbindungseinrichtung**.
    2. Verwenden Sie **Vollständige Synchronisierung ausführen** zum Öffnen der Seite **Dataverse Vollständige Synchronisierungsprüfung**.
    3. Für die Zuordnungen **ARTIKEL ME**, **RESSOURCE ME** und **EINHEITENGRUPPE** wählen Sie die Aktion **Vollständige Synchronisierung empfehlen** aus.
    4. Wählen Sie die Aktion **Alle synchronisieren** aus.

    > [!NOTE]
    > Zuordnungen, die noch nicht vollständig synchronisiert wurden, werden durch diese Aktion vollständig synchronisiert. Um zu verhindern, dass diese Zuordnungen synchronisiert werden, löschen Sie die Zuordnungen von der Seite. Dadurch werden sie nur aus der aktuellen vollständigen Synchronisierung entfernt und die Zuordnungen nicht gelöscht.
    
5. Wählen Sie die Zuordnung **ARTIKEL-PRODUKT** und dann **Neustarten**. Neustart erstellt neue Produkte aus den Artikeln in [!INCLUDE[crm_md](includes/crm_md.md)] und weist eine neue, für den Artikel spezifische Einheitsgruppe zu.
6. Wählen Sie die Zuordnung **RESSOURCE-PRODUKT** und dann **Neustarten**. Neustart erstellt neue Produkte aus den Ressourcen in [!INCLUDE[crm_md](includes/crm_md.md)] und weist eine neue, ressourcenspezifische Einheitsgruppe zu.

### <a name="synchronization-rules"></a>Synchronisierungsregeln

Die folgende Tabelle listet die Regeln auf, die die Synchronisation zwischen [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] steuern. Diese Regeln gelten zusätzlich zu den für Dataverse definierten Regeln, die ebenfalls gelten. Weitere Informationen finden Sie unter [Standard-Entitätszuordnung für die Synchronisation](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Änderungen an Daten, die vom Integrationsbenutzerkonto vorgenommen wurden, werden nicht synchronisiert. Daher empfiehlt es sich, bei der Nutzung dieses Kontos keine Daten zu ändern. Weitere Informationen finden Sie unter [Einrichten des Benutzerkontos für die Integration in Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tisch|Regel|
|-----|----|
|Einheiten|Einheiten werden mit Einheitengruppen in [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert. Es kann nur eine Einheit in der Einheitengruppe definiert sein.|
|Artikel|Wenn Artikel mit [!INCLUDE[crm_md](includes/crm_md.md)] Produkten synchronisiert werden, erstellt [!INCLUDE[prod_short](includes/prod_short.md)] automatisch eine Preisliste in [!INCLUDE[crm_md](includes/crm_md.md)]. Um Synchronisierungsfehler zu vermeiden, sollten Sie diese Preisliste nicht manuell ändern.|
|Ressourcen|Ressourcen werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Produkten synchronisiert, die den Produkttyp-Service haben.|
|Debitorenpreisgruppen|Debitorenpreisgruppen werden mit Verkaufspreislisten synchronisiert.|
|Verkaufspreise|Verkaufspreise, die Verkaufsart Debitorenpreisgruppe haben und einen definierten Verkaufscode haben werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Preislistenzeilen synchronisiert|
|Verkaufschancen|Chancen werden mit [!INCLUDE[crm_md](includes/crm_md.md)]-Chancen synchronisiert. Der Verkäufer-Codewert definiert den Besitzer der gekoppelten Tabelle in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Gebuchte Verkaufsrechnungen|Gebuchte Verkaufsrechnungen werden mit Verkaufsrechnungen synchronisiert. Bevor eine Rechnung synchronisiert werden kann, ist es besser, alle anderen Tabellen zu synchronisieren, die an der Rechnung beteiligt sein können, von Verkäufern bis zu Preislisten. Der Verkäufer-Codewert im Rechnungskopf definiert den Besitzer der gekoppelten Tabelle im Verkauf.|
|Verkaufsaufträge|Wenn die Integration von Verkaufsaufträgen aktiviert ist, werden Verkaufsaufträge in [!INCLUDE[prod_short](includes/prod_short.md)], die aus gesendeten Verkaufsaufträgen in [!INCLUDE[crm_md](includes/crm_md.md)] erstellt wurden, mit Verkaufsaufträgen in [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert, wenn sie freigegeben werden. Vor dem Synchronisieren von Aufträgen wird empfohlen, zunächst alle an dem Auftrag beteiligten Tabellen zu synchronisieren, z. B. Verkäufer und Preislisten. Das Verkäufer-Codefeld im Auftragskopf definiert den Besitzer der gekoppelten Tabelle in [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Synchronisierungsaufträge für eine Sales-Integration

Die Jobs werden in der folgenden Reihenfolge ausgeführt, um Kopplungsabhängigkeiten zwischen Tabellen zu vermeiden. Es sind mehr Aufträge aus Dataverse verfügbar. Weitere Informationen finden Sie unter [Vorgehensweise: Projektwarteschlangen nutzen, um Aufgaben zu planen](./admin-job-queues-schedule-tasks.md)

1. UNITOFMEASURE - Dynamics 365 Sales Synchronisierungsauftrag  
2. RESSOURCE-PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag  
3. ARTIKEL - PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag  
4. CUSTPRCGRP-PRICE- Synchronisierungsauftrag „Dynamics 365 Sales“.
5. SALESPRC-PRODPRICE - Synchronisierungsauftrag „Dynamics 365 Sales“.
6. POSTEDSALESINV-INV - Dynamics 365 Sales-Synchronisierungsauftrag.

### <a name="default-synchronization-job-queue-entries"></a>Standard-Synchronisations-Projektwarteschlangeneinträge

Die folgende Tabelle beschreibt die Standard-Synchronisierungsaufträge für [!INCLUDE[crm_md](includes/crm_md.md)].  

|Aufgabenwarteschlangenposten|Beschreibung|Richtung|Integrationstabellenzuordnung|Standard-Synchronisationsfrequenz (Minuten)|Standard-Inaktivitätsruhezustand (Minuten)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|UNITOFMEASURE - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Einheitsgruppen mit [!INCLUDE[prod_short](includes/prod_short.md)]-Einheiten.|Von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|EINHEIT|30|720<br> (12 Std.)|
|RESSOURCE-PRODUCT - Dynamics 365 Sales Vertriebssynchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[prod_short](includes/prod_short.md)]-Ressourcen.|Von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|RESSOURCE – PRODUKT|30|720<br> (12 Std.)|
|ARTIKEL - PRODUKT - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produkte mit [!INCLUDE[prod_short](includes/prod_short.md)]-Artikeln.|Von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL/PRODUKT|30|1440<br> (24 Std.)|
|CUSTPRCGRP-PREIS - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Verkaufspreislisten mit [!INCLUDE[prod_short](includes/prod_short.md)]-Debitorenpreisgruppen.| |DEBITORENPREISGRUPPEN – VERKAUFSPREISLISTEN|30|1440<br> (24 Std.)|
|SALESPRC-PRODUCTPRICE - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Produktpreise mit [!INCLUDE[prod_short](includes/prod_short.md)]-Verkaufspreisen.||PRODUKTPREIS – VERKAUFSPREIS|30|1440<br> (24 Std.)|
|POSTEDSALESINV-INV - Dynamics 365 Sales Synchronisierungsauftrag|Synchronisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Rechnungen mit gebuchten [!INCLUDE[prod_short](includes/prod_short.md)]-Verkaufsrechnungen.|Von [!INCLUDE[prod_short](includes/prod_short.md)] nach [!INCLUDE[crm_md](includes/crm_md.md)]|RECHNUNGEN – GEBUCHTE VERKAUFSRECHNUNGEN|30|1440<br> (24 Std.)|
|Debitorenstatistik - Dynamics 365 Sales Synchronisierungsauftrag|Aktualisiert [!INCLUDE[crm_md](includes/crm_md.md)]-Konten mit den neuesten [!INCLUDE[prod_short](includes/prod_short.md)]-Debitorendaten. In [!INCLUDE[crm_md](includes/crm_md.md)] erscheinen diese Informationen im **Business Central-Kontostatistik**-Schnellansichtsformular von Konten, die mit [!INCLUDE[prod_short](includes/prod_short.md)]-Debitoren gekoppelt werden.<br /><br /> Diese Daten können auch manuell für jeden Debitorendatensatz aktualisiert werden. Weitere Informationen finden Sie unter [Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Hinweis:** Dieser Projektwarteschlangeneintrag ist nur relevant, wenn die [!INCLUDE[prod_short](includes/prod_short.md)]-Integrationslösung in [!INCLUDE[crm_md](includes/crm_md.md)] installiert ist. |Nicht anwendbar|Nicht anwendbar|30|Nicht anwendbar| 

## <a name="connect-to-on-premises-versions-of-business-central-2019-release-wave-1-and-microsoft-dynamics-nav-2018"></a>Verbinden mit lokalen Versionen von Business Central 2019 Veröffentlichungszyklus 1 und Microsoft Dynamics NAV 2018

Das Team Microsoft Power Platform hat [angekündigt](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse), dass es die Authentifizierungsart Office365 außer Betrieb nimmt. Wenn Sie lokal eine Version von [!INCLUDE[prod_short](includes/prod_short.md)] verwenden, die älter ist als Business Central 2019 Release Wave 1, müssen Sie den Authentifizierungstyp OAuth verwenden, um sich online mit [!INCLUDE[crm_md](includes/crm_md.md)] zu verbinden. Die Schritte in diesem Abschnitt beschreiben, wie Sie die folgenden Produktversionen verbinden:

* Business Central 2019 Freigabewelle 1
* Microsoft Dynamics NAV 2018

### <a name="prerequisites"></a>Voraussetzungen

* Sie müssen ein Microsoft Azure Abonnement haben. Ein Testkonto funktioniert für die Registrierung von Anträgen.
* [!INCLUDE[crm_md](includes/crm_md.md)] ist für die Verwendung eines der folgenden Authentifizierungstypen konfiguriert:

   * Office365 (Legacy)

     > [!IMPORTANT]
     > Ab April 2022 wird Office365 (Legacy) nicht mehr unterstützt. Weitere Informationen finden Sie unter [Wichtige Änderungen (Abschreibungen) über Power Apps, Power Automate und Customer Engagement-Apps](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   * OAuth

### <a name="connect-business-central-2019-release-wave-1-and-dynamics-nav-2018"></a>So verbinden Sie Business Central 2019 Freigabewelle 1 und Dynamics NAV 2018

1. Importieren Sie Microsoft Dynamics 365 Business Central Integrationslösung in Ihre [!INCLUDE[crm_md](includes/crm_md.md)] Umgebung. Die Integrationslösung ist im Ordner CrmCustomization auf Ihrer [!INCLUDE[prod_short](includes/prod_short.md)] oder Dynamics NAV 2018 Installations-DVD verfügbar. Abhängig von Ihrer Produktversion importieren Sie eine der folgenden Lösungen:

   * Für [!INCLUDE[prod_short](includes/prod_short.md)] enthält der Ordner die DynamicsNAVIntegrationSolution_v9 und DynamicsNAVIntegrationSolution_v91. Lösungen. Die Lösung, die Sie importieren sollten, hängt von der Version von [!INCLUDE[crm_md](includes/crm_md.md)] ab, mit der Sie sich verbinden. [!INCLUDE[crm_md](includes/crm_md.md)] online erfordert die DynamicsNAVIntegrationSolution_v91 Integrationslösung.
   * Für Dynamics NAV 2018, installieren Sie die Lösung DynamicsNAVIntegrationSolution.

2. Erstellen Sie einen nicht interaktiven Integrationsbenutzer in Ihrer [!INCLUDE[crm_md](includes/crm_md.md)] Umgebung, und weisen Sie dem Benutzer die folgenden Sicherheitsrollen zu. Weitere Informationen finden Sie unter [Erstellen eines nicht interaktiven Benutzerkontos](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central Integrations-Administrator
   * Dynamics 365 Business Central Integration Benutzer

   > [!Important]
   > Dieser Benutzer darf nicht über die Sicherheitsrolle des Systemadministrators verfügen. Sie können das Systemadministratorkonto auch nicht als Integrationsbenutzer verwenden.

3. Erstellen Sie im Azure-Portal eine App-Registrierung für [!INCLUDE[prod_short](includes/prod_short.md)]. Weitere Informationen finden Sie unter [Registrieren einer Anwendung in Microsoft Entra-ID](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Wir empfehlen, dass Sie die App im gleichen Mandant wie Ihre Dataverse-Umgebung registrieren, damit Sie nicht zustimmen müssen, dass die App auf die Umgebung zugreifen darf. Wenn Sie die App in einer anderen Umgebung registrieren, müssen Sie sich mit dem Administratorkonto für Ihre Dataverse-Umgebung bei Microsoft Entra-ID anmelden und die Zustimmung erteilen.
   >
   > Außerdem darf die App, die Sie registrieren, kein Geheimnis haben. Das Verbinden einer App mit einem Geheimnis mit Dataverse ist nur in Business Central 2020 Release Wave 1 und später verfügbar.
  
4. Führen Sie abhängig von Ihrer Produktversion einen der folgenden Schritte aus:

    * In [!INCLUDE[prod_short](includes/prod_short.md)] suchen Sie nach **Microsoft Dynamics 365 Verbindung einrichten** und wählen Sie dann den entsprechenden Link. 
    * Suchen Sie in Dynamics NAV 2018 nach **Microsoft Dynamics 365 for Sales Verbindungseinrichtung**, und wählen Sie dann den entsprechenden Link.

5. Wählen Sie im Feld **Authentifizierungstyp** die Option für OAuth. 
6. Wählen Sie die CRM SDK-Version aus, die der in Schritt 1 importierten Lösungsversion entspricht.

   > [!NOTE]
   > Dieser Schritt ist nur für [!INCLUDE[prod_short](includes/prod_short.md)] relevant.

7. Geben Sie die URL Ihrer [!INCLUDE[crm_md](includes/crm_md.md)]-Umgebung ein, und geben Sie dann den Benutzernamen und das Kennwort für den Integrationsbenutzer ein. 

   * Verwenden Sie in [!INCLUDE[prod_short](includes/prod_short.md)] das Feld **Server-Adresse**.
   * Verwenden Sie in Dynamics NAV 2018 das Feld **Dynamics 365 Sales URL**.

8. In dem Feld **Verbindungszeichenfolge** geben Sie im Feld die ID der App-Registrierung an. Dieses Feld enthält zwei Token, in denen die ID Ihrer Anwendung angegeben werden soll.

   |Token           |Beschreibung  |
   |----------------|-------------|
   |**appId**       |Stellen Sie die Anwendungs-ID ein.      |
   |**Umleitungs-URL** |Stellen Sie die Anwendungs-ID ein, fügen Sie jedoch den **App: //** Präfix hinzu.         |

    **Beispiel** Das folgende Beispiel zeigt eine Verbindungszeichenfolge.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Aktivieren Sie die Verbindung.

> [!Note]
> Wenn Sie eine lokale Instanz mit [!INCLUDE[crm_md](includes/crm_md.md)] mit einem bestimmten Authentifizierungstyp konfigurieren möchten, füllen Sie die Felder im Inforegister **Authentifizierungstyp-Details** aus. Weitere Informationen finden Sie unter [Authentifizierung mit Microsoft Dataverse-Webdienste](/powerapps/developer/data-platform/authentication). Dieser Schritt ist nicht erforderlich, wenn sie eine Verbindung mit einer Onlineversion von [!INCLUDE[prod_short](includes/prod_short.md)] herstellen.

## <a name="see-also"></a>Siehe auch

[Einrichten des Benutzerkontos für die Integration in [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Richten Sie eine Verbindung mit [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md) ein  
[Synchronisieren von Business Central und [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Vorbereiten der Integration in Dynamics 365 Sales für die lokale Integration](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
