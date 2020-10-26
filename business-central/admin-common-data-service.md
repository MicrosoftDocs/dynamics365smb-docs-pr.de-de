---
title: Verwendung von Common Data Service
description: Einführung in Common Data Service und seine Komponenten.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 85823e93b1d239bf4e59ec6a8872cdc4a2cef9c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911580"
---
# <a name="integrating-with-common-data-service"></a>Integrieren in Common Data Service

Geschäftsanwendungen verwenden häufig Daten aus mehr als einer Quelle. [!INCLUDE[d365fin](includes/cds_long_md.md)] kombiniert Daten in einem einzigen Satz von Logik, der es einfacher macht, andere Dynamics 365-Anwendungen, wie [!INCLUDE[crm_md](includes/crm_md.md)] oder Ihre eigene Anwendung, die auf [!INCLUDE[d365fin](includes/cds_long_md.md)] aufbaut, mit [!INCLUDE[d365fin_md](includes/d365fin_md.md)] zu verbinden. Für weitere Informationen über [!INCLUDE[d365fin](includes/cds_long_md.md)] siehe [Was ist Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Die folgenden Schritte bieten einen Überblick über die Schritte für die Integration von [!INCLUDE[d365fin](includes/cds_long_md.md)] mit [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Für diese Aufgaben ist die Sicherheitsrolle des **Systemadministrators** in [!INCLUDE[d365fin](includes/cds_long_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] erforderlich.  

1. Weisen Sie Lizenzen für [!INCLUDE[d365fin](includes/cds_long_md.md)] den [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzern zu, die die integrierten Apps verwenden werden.

2. Richten Sie eine Verbindung mit [!INCLUDE[d365fin](includes/cds_long_md.md)] ein. Weitere Informationen finden Sie unter [Verbindung zu Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synchronisieren Sie die Daten zwischen den Apps. Weitere Informationen finden Sie unter [Synchronisieren von Business Central und Common Data Service](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>Erste Schritte mit [!INCLUDE[d365fin](includes/cds_long_md.md)]
Um mit [!INCLUDE[d365fin](includes/cds_long_md.md)] zu beginnen, benötigen Sie ein Microsoft Power Apps-Konto. Wenn Sie noch nicht über ein Power Apps-Konto verfügen, können Sie ein kostenloses Konto erhalten, indem Sie [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) besuchen und den Link **Kostenlos einsteigen** wählen. Weitere Informationen zu den ersten Schritten mit [!INCLUDE[d365fin](includes/cds_long_md.md)] finden Sie im Modul [Erste Schritte mit Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) von Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Bidirektionale oder unidirektionale Datensynchronisation
Je nach Ihren Geschäftsanforderungen können Sie die Integration so einrichten, dass Daten entweder mit einer Dynamics 365-Geschäftsanwendung oder von einer Dynamics 365-Geschäftsanwendung zu einer anderen synchronisiert werden oder in beiden Richtungen in nahezu Echtzeit durch [!INCLUDE[d365fin](includes/cds_long_md.md)]. Wenn Sie z.B. [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] bis [!INCLUDE[d365fin](includes/cds_long_md.md)] integrieren, kann ein Kreditor einen Debitorenauftrag in [!INCLUDE[crm_md](includes/crm_md.md)] erstellen, und der Auftrag wird mit [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronisiert. Umgekehrt kann der Verkäufer von [!INCLUDE[crm_md](includes/crm_md.md)] aus Informationen von [!INCLUDE[d365fin](includes/d365fin_md.md)] über die Verfügbarkeit des Artikels auf der Bestellung einsehen. 

## <a name="standard-and-custom-entities"></a>Standard- und benutzerdefinierte Entitäten
[!INCLUDE[d365fin](includes/cds_long_md.md)] speichert Daten sicher in einem Satz von Entitäten, das sind Datensätze, ähnlich wie eine Tabelle Daten in einer Datenbank speichert. [!INCLUDE[d365fin](includes/cds_long_md.md)] enthält einen Basissatz von Standardentitäten, die typische Szenarien abdecken, aber Sie können auch benutzerdefinierte Entitäten erstellen, die spezifisch für Ihre Organisation sind. In [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie Standard- und benutzerdefinierte Entitäten anzeigen, die auf der Seite Integrationstabellenzuordnungen synchronisiert werden.

## <a name="about-the-base-cds-integration-solution"></a>Über die CDS-Basisintegrationslösung

Die CDS-Basisintegrationslösung ist eine Schlüsselkomponente der Integration. Die Lösung fügt den Benutzerkonten für die Integration die erforderlichen Rollen und Zugriffsebenen hinzu, und sie erstellt Einheiten, die für die Zuordnung von [!INCLUDE[d365fin](includes/d365fin_md.md)] Unternehmen zu Geschäftseinheit in [!INCLUDE[d365fin](includes/cds_long_md.md)] erforderlich sind. 

Standardmäßig importiert die unterstützte Einrichtung **[!INCLUDE[d365fin](includes/cds_long_md.md)]-Verbindung einrichten** die Lösung. Dazu verwendet der Einrichtungsleitfaden ein Administrator-Benutzerkonto, das Sie angeben. Dieses Konto muss ein gültiger Benutzer in [!INCLUDE[d365fin](includes/cds_long_md.md)] mit der folgenden Sicherheitsrolle sein:

* Systemadministrator  

Weitere Informationen finden Sie unter [Benutzerkonten für die Integration einrichten mit [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) und [Benutzer in Microsoft Dynamics 365 (online) anlegen und Sicherheitsrollen zuweisen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Das Administratorkonto wird aufgrund von Konfigurationsänderungen, die die Basis-CDS-Lösung in [!INCLUDE[d365fin](includes/cds_long_md.md)] vornimmt, während der Einrichtung nur einmal verwendet. Nachdem die Lösung importiert wurde, wird das Konto nicht mehr benötigt. Bei der Integration wird dann weiterhin das Benutzerkonto verwendet, das automatisch speziell für die Integration erstellt wurde.

Zusätzlich zur Anpassung von [!INCLUDE[d365fin](includes/cds_long_md.md)] erstellt die Lösung auch die folgenden Rollen in [!INCLUDE[d365fin](includes/cds_long_md.md)] für die Integration:

* **Integrationsadministrator** – Ermöglicht es Benutzern, die Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[d365fin](includes/cds_long_md.md)] zu verwalten. Normalerweise wird diese nur dem automatisch erstellten Benutzerkonto für die Synchronisierung zugewiesen.  
* **Integrationsbenutzer** – Ermöglicht es Benutzern, auf synchronisierte Daten zuzugreifen. In der Regel wird dies dem automatisch erstellten Benutzerkonto für die Synchronisierung und anderen Benutzern zugewiesen, die die synchronisierten Daten anzeigen oder auf sie zugreifen müssen.

Weitere Informationen zu den einzelnen Rollen, z. B. zu Berechtigungen und Zugriffsebenen, finden Sie unter [Einrichten von Benutzerkonten für die Integration mit [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Während des Verbindungsaufbaus werden Integrationstabellenzuordnungen erstellt, die zur Datensynchronisation benötigt werden. Entitäten in Common Data Service werden Tabellen und Tabellenfeldern in Business Central durch Integrationstabellen zugeordnet. Weitere Informationen finden Sie unter [Standard Entitätszuordnung für die Synchronisation](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Siehe auch
[Dateneigentumsmodelle](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



