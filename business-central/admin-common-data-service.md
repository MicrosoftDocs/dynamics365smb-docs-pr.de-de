---
title: Verwendung von Microsoft Dataverse
description: Einführung in die Integration und Verwendung von Microsoft Dataverse und seinen Komponenten zur Verbindung mit anderen Dynamics 365-Anwendungen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 06/28/2023
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dataverse"></a>In Microsoft Dataverse integrieren

Geschäftsanwendungen verwenden häufig Daten aus mehr als einer Quelle. [!INCLUDE[prod_short](includes/cds_long_md.md)] kombiniert Daten in einem einzigen Satz von Logik, mit dem es leichter wird, [!INCLUDE[prod_short](includes/prod_short.md)] mit anderen Dynamics 365-Anwendungen zu verbinden. Zum Beispiel mit [!INCLUDE[crm_md](includes/crm_md.md)] oder Ihrer eigenen Anwendung, die auf [!INCLUDE[prod_short](includes/cds_long_md.md)] basiert. Um mehr zu erfahren, gehen Sie zu [!INCLUDE[prod_short](includes/cds_long_md.md)] und [Was ist Dataverse](/powerapps/maker/common-data-service/data-platform-intro).

Die folgenden Schritte bieten einen Überblick über die Schritte für die Integration von [!INCLUDE[prod_short](includes/cds_long_md.md)] mit [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Für diese Aufgaben ist die Sicherheitsrolle des **Systemadministrators** in [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] erforderlich.  

1. Weisen Sie Lizenzen für [!INCLUDE[prod_short](includes/cds_long_md.md)] den [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzern zu, die die integrierten Apps verwenden werden.

2. Richten Sie eine Verbindung mit [!INCLUDE[prod_short](includes/cds_long_md.md)] ein. Weitere Informationen finden Sie unter [Verbindung zu Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synchronisieren Sie die Daten zwischen den Apps. Weitere Informationen finden Sie unter [Synchronisieren von Business Central und Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="get-started-with-"></a>Erste Schritte mit [!INCLUDE[prod_short](includes/cds_long_md.md)]

Um mit der Nutzung von [!INCLUDE[prod_short](includes/cds_long_md.md)] zu beginnen, benötigen Sie ein Microsoft Power Apps-Konto. Wenn Sie noch nicht über ein Power Apps-Konto verfügen, können Sie sich ein kostenloses Konto holen, indem Sie [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) besuchen und den Link **Kostenlos einsteigen** wählen. Weitere Informationen zu den ersten Schritten mit [!INCLUDE[prod_short](includes/cds_long_md.md)] finden Sie im Modul [Erste Schritte mit Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) von Microsoft-Schulungen.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Bidirektionale oder unidirektionale Datensynchronisierung

Sie können Daten entweder von einer oder an eine Dynamics 365-Geschäftsanwendung zu einer anderen oder durch [!INCLUDE[prod_short](includes/cds_long_md.md)] in beiden Richtungen nahezu in Echtzeit synchronisieren. Wenn Sie z. B. [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] integrieren, kann ein Verkäufer einen Verkaufsauftrag in [!INCLUDE[crm_md](includes/crm_md.md)] erstellen, und der Auftrag wird mit [!INCLUDE[prod_short](includes/prod_short.md)] synchronisiert. Umgekehrt kann der Verkäufer von [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[prod_short](includes/prod_short.md)] die Verfügbarkeit des Artikels für den Auftrag einsehen. 

## <a name="standard-and-custom-entities"></a>Standard- und benutzerdefinierte Entitäten

[!INCLUDE[prod_short](includes/cds_long_md.md)] speichert Daten sicher in einem Satz von Tabellen, das sind Datensätze, ähnlich wie eine Tabelle Daten in einer Datenbank speichert. [!INCLUDE[prod_short](includes/cds_long_md.md)] enthält einen Basissatz von Standardentitäten, die typische Szenarien abdecken, aber Sie können auch benutzerdefinierte Tabellen erstellen, die spezifisch für Ihre Organisation sind. In [!INCLUDE[prod_short](includes/prod_short.md)] können Sie Standard- und benutzerdefinierte Tabellen anzeigen, die auf der Seite Integrationstabellenzuordnungen synchronisiert werden.

## <a name="about-the-business-central-base-integration-solution"></a>Informationen über die Business Central Basis-Integrationslösung

Die Basisintegrationslösung ist eine Schlüsselkomponente der Integration. Die Lösung fügt den Benutzerkonten für die Integration die erforderlichen Rollen und Zugriffsebenen hinzu, und sie erstellt Tabellen, die für die Zuordnung von [!INCLUDE[prod_short](includes/prod_short.md)] Unternehmen zu Geschäftseinheit in [!INCLUDE[prod_short](includes/cds_long_md.md)] erforderlich sind. 

Standardmäßig importiert die unterstützte Einrichtung **[!INCLUDE[prod_short](includes/cds_long_md.md)]-Verbindung einrichten** die Lösung. Dazu verwendet der Einrichtungsleitfaden ein Administrator-Benutzerkonto, das Sie angeben. Dieses Konto muss ein gültiger Benutzer in [!INCLUDE[prod_short](includes/cds_long_md.md)] mit der folgenden Sicherheitsrolle sein:

* Systemadministrator  

Weitere Informationen zu Benutzerkonten finden Sie in den folgenden Artikeln:

* [Einrichten des Benutzerkontos für die Integration in [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Benutzer in Microsoft Dynamics 365 (online) erstellen und Sicherheitsrollen zuweisen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) 

Das Administratorkonto wird aufgrund von Konfigurationsänderungen, die die Basis-Integrationslösung in [!INCLUDE[prod_short](includes/cds_long_md.md)] vornimmt, während der Einrichtung nur einmal verwendet. Nachdem die Lösung importiert wurde, wird das Konto nicht mehr benötigt. Bei der Integration wird dann weiterhin das Benutzerkonto verwendet, das automatisch speziell für die Integration erstellt wurde.

Zusätzlich zur Anpassung von [!INCLUDE[prod_short](includes/cds_long_md.md)] erstellt die Lösung auch die folgenden Rollen in [!INCLUDE[prod_short](includes/cds_long_md.md)] für die Integration:

* **Integrationsadministrator** – Ermöglicht es Benutzern, die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)] zu verwalten. Normalerweise wird diese Rolle nur dem für die Synchronisierung automatisch erstellten Benutzerkonto zugewiesen.  
* **Integrationsbenutzer** – Ermöglicht es Benutzern, auf synchronisierte Daten zuzugreifen. Normalerweise weisen Sie diese Rolle den folgenden Benutzerkonten zu:

  * Den Benutzerkonten, die automatisch für die Synchronisierung erstellt werden.
  * Anderen Benutzenden, die Zugriff auf die synchronisierten Daten benötigen.

Weitere Informationen zu den einzelnen Rollen, z. B. zu Berechtigungen und Zugriffsebenen, finden Sie unter [Einrichten von Benutzerkonten für die Integration mit [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Wenn Sie die Verbindung aufbauen, erstellen Sie Integrationstabellenzuordnungen, die Sie zur Datensynchronisierung benötigen. Entitäten in [!INCLUDE[prod_short](includes/cds_long_md.md)] werden Tabellen und Tabellenfeldern in [!INCLUDE [prod_short](includes/prod_short.md)] durch Integrationstabellen zugeordnet. Weitere Informationen zu Zuordnungen finden Sie unter [Standard-Entitätszuordnung für die Synchronisierung](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="handle-differences-in-local-and-base-transaction-currencies"></a>Umgang mit Unterschieden zwischen lokalen und Basistransaktionswährungen

Sie können eine Verbindung zu einer [!INCLUDE[prod_short](includes/cds_long_md.md)] Umgebung herstellen, die eine andere Basiswährung als die lokale Währung in [!INCLUDE[prod_short](includes/prod_short.md)] hat. Sie können die Verbindung in [!INCLUDE[prod_short](includes/prod_short.md)] auf der Seite **Dataverse Verbindungseinrichtung** oder mithilfe der Anleitung für die unterstützte Einrichtung **Eine Verbindung mit Dataverse einrichten** aufbauen.

Um die Verbindung herstellen zu können, stellen Sie sicher, dass die Einstellung der Basistransaktionswährung in [!INCLUDE[prod_short](includes/cds_long_md.md)] die gleiche Währung wie auf der Seite **Währungen** in [!INCLUDE [prod_short](includes/prod_short.md)] hat und für die Währung mindestens ein Wechselkurs auf der Seite **Währungswechselkurs** angegeben ist.

Im Folgenden finden Sie ein Beispiel. Sie verbinden [!INCLUDE[prod_short](includes/cds_long_md.md)] mit Euro (EUR) als lokaler Währung, wie auf der Seite **Hauptbucheinrichtung** angegeben, mit einer [!INCLUDE[prod_short](includes/cds_long_md.md)] Umgebung, deren Basistransaktionswährung auf US-Dollar (USD) eingestellt ist. Auf der Seite **Währungen** in [!INCLUDE [prod_short](includes/prod_short.md)] müssen USD und der entsprechende Wechselkurs angegeben sein. 

Wenn Sie die Verbindung mit [!INCLUDE[prod_short](includes/cds_long_md.md)] aktivieren, fügt [!INCLUDE [prod_short](includes/prod_short.md)] die lokale Währung der Entität **Währung** in [!INCLUDE[prod_short](includes/cds_long_md.md)] mit dem Wechselkurs aus dem Feld **Währungsfaktor** auf der Seite **Währungswechselkurse** hinzu.

Die Währungssynchronisierung erfolgt unidirektional, von [!INCLUDE [prod_short](includes/prod_short.md)] an [!INCLUDE[prod_short](includes/cds_long_md.md)], wobei Geldbeträge wie folgt konvertiert und synchronisiert werden:

* Beträge in der [!INCLUDE[prod_short](includes/cds_long_md.md)] Basiswährung werden basierend auf dem letzten synchronisierten Wechselkurs von [!INCLUDE [prod_short](includes/prod_short.md)] in die [!INCLUDE [prod_short](includes/prod_short.md)] lokale Währung umgerechnet.
* Beträge in der [!INCLUDE [prod_short](includes/prod_short.md)] lokalen Währung werden mit der [!INCLUDE [prod_short](includes/prod_short.md)] lokalen Währung in einer der anderen (nicht Basis-)Währungen in [!INCLUDE[prod_short](includes/cds_long_md.md)] synchronisiert.

## <a name="see-also"></a>Siehe auch

[Dateneigentumsmodelle](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
