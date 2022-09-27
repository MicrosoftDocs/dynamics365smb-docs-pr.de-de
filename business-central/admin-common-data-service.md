---
title: Verwendung von Microsoft Dataverse
description: Einführung in die Integration und Verwendung von Microsoft Dataverse und seinen Komponenten zur Verbindung mit anderen Dynamics 365-Anwendungen.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 06/14/2021
ms.openlocfilehash: 422466c83d3f86f9afa611f5ef578482eadaf275
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531755"
---
# <a name="integrating-with-microsoft-dataverse"></a>Integrieren in Microsoft Dataverse

Geschäftsanwendungen verwenden häufig Daten aus mehr als einer Quelle. [!INCLUDE[prod_short](includes/cds_long_md.md)] kombiniert Daten in einem einzigen Satz von Logik, der es einfacher macht, andere Dynamics 365-Anwendungen, wie [!INCLUDE[crm_md](includes/crm_md.md)] oder Ihre eigene Anwendung, die auf [!INCLUDE[prod_short](includes/cds_long_md.md)] aufbaut, mit [!INCLUDE[prod_short_md](includes/prod_short.md)] zu verbinden. Für weitere Informationen über [!INCLUDE[prod_short](includes/cds_long_md.md)] finden Sie unter [Was ist Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)

Die folgenden Schritte bieten einen Überblick über die Schritte für die Integration von [!INCLUDE[prod_short](includes/cds_long_md.md)] mit [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Für diese Aufgaben ist die Sicherheitsrolle des **Systemadministrators** in [!INCLUDE[prod_short](includes/cds_long_md.md)] und [!INCLUDE[prod_short](includes/prod_short.md)] erforderlich.  

1. Weisen Sie Lizenzen für [!INCLUDE[prod_short](includes/cds_long_md.md)] den [!INCLUDE[prod_short](includes/prod_short.md)]-Benutzern zu, die die integrierten Apps verwenden werden.

2. Richten Sie eine Verbindung mit [!INCLUDE[prod_short](includes/cds_long_md.md)] ein. Weitere Informationen finden Sie unter [Verbindung zu Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synchronisieren Sie die Daten zwischen den Apps. Weitere Informationen finden Sie unter [Synchronisieren von Business Central und Dataverse](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-prod_short"></a>Erste Schritte mit [!INCLUDE[prod_short](includes/cds_long_md.md)]

Um mit [!INCLUDE[prod_short](includes/cds_long_md.md)] zu beginnen, benötigen Sie ein Microsoft Power Apps-Konto. Wenn Sie noch nicht über ein Power Apps-Konto verfügen, können Sie ein kostenloses Konto erhalten, indem Sie [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) besuchen und den Link **Kostenlos einsteigen** wählen. Weitere Informationen zu den ersten Schritten mit [!INCLUDE[prod_short](includes/cds_long_md.md)] finden Sie im Modul [Erste Schritte mit Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) von Microsoft Schulung.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Bidirektionale oder unidirektionale Datensynchronisation

Je nach Ihren Geschäftsanforderungen können Sie die Integration so einrichten, dass Daten entweder mit einer Dynamics 365-Geschäftsanwendung oder von einer Dynamics 365-Geschäftsanwendung zu einer anderen synchronisiert werden oder in beiden Richtungen in nahezu Echtzeit durch [!INCLUDE[prod_short](includes/cds_long_md.md)]. Wenn Sie z.B. [!INCLUDE[prod_short](includes/prod_short.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] bis [!INCLUDE[prod_short](includes/cds_long_md.md)] integrieren, kann ein Kreditor einen Debitorenauftrag in [!INCLUDE[crm_md](includes/crm_md.md)] erstellen, und der Auftrag wird mit [!INCLUDE[prod_short](includes/prod_short.md)] synchronisiert. Umgekehrt kann der Verkäufer von [!INCLUDE[crm_md](includes/crm_md.md)] aus Informationen von [!INCLUDE[prod_short](includes/prod_short.md)] über die Verfügbarkeit des Artikels auf der Bestellung einsehen. 

## <a name="standard-and-custom-entities"></a>Standard- und benutzerdefinierte Entitäten

[!INCLUDE[prod_short](includes/cds_long_md.md)] speichert Daten sicher in einem Satz von Tabellen, das sind Datensätze, ähnlich wie eine Tabelle Daten in einer Datenbank speichert. [!INCLUDE[prod_short](includes/cds_long_md.md)] enthält einen Basissatz von Standardentitäten, die typische Szenarien abdecken, aber Sie können auch benutzerdefinierte Tabellen erstellen, die spezifisch für Ihre Organisation sind. In [!INCLUDE[prod_short](includes/prod_short.md)] können Sie Standard- und benutzerdefinierte Tabellen anzeigen, die auf der Seite Integrationstabellenzuordnungen synchronisiert werden.

## <a name="about-the-business-central-base-integration-solution"></a>Informationen über die Business Central Basis-Integrationslösung

Die Basisintegrationslösung ist eine Schlüsselkomponente der Integration. Die Lösung fügt den Benutzerkonten für die Integration die erforderlichen Rollen und Zugriffsebenen hinzu, und sie erstellt Tabellen, die für die Zuordnung von [!INCLUDE[prod_short](includes/prod_short.md)] Unternehmen zu Geschäftseinheit in [!INCLUDE[prod_short](includes/cds_long_md.md)] erforderlich sind. 

Standardmäßig importiert die unterstützte Einrichtung **[!INCLUDE[prod_short](includes/cds_long_md.md)]-Verbindung einrichten** die Lösung. Dazu verwendet der Einrichtungsleitfaden ein Administrator-Benutzerkonto, das Sie angeben. Dieses Konto muss ein gültiger Benutzer in [!INCLUDE[prod_short](includes/cds_long_md.md)] mit der folgenden Sicherheitsrolle sein:

* Systemadministrator  

Weitere Informationen finden Sie unter [Benutzerkonten für die Integration einrichten mit [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) und [Benutzer in Microsoft Dynamics 365 (online) anlegen und Sicherheitsrollen zuweisen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Das Administratorkonto wird aufgrund von Konfigurationsänderungen, die die Basis-Integrationslösung in [!INCLUDE[prod_short](includes/cds_long_md.md)] vornimmt, während der Einrichtung nur einmal verwendet. Nachdem die Lösung importiert wurde, wird das Konto nicht mehr benötigt. Bei der Integration wird dann weiterhin das Benutzerkonto verwendet, das automatisch speziell für die Integration erstellt wurde.

Zusätzlich zur Anpassung von [!INCLUDE[prod_short](includes/cds_long_md.md)] erstellt die Lösung auch die folgenden Rollen in [!INCLUDE[prod_short](includes/cds_long_md.md)] für die Integration:

* **Integrationsadministrator** – Ermöglicht es Benutzern, die Verbindung zwischen [!INCLUDE[prod_short](includes/prod_short.md)] und [!INCLUDE[prod_short](includes/cds_long_md.md)] zu verwalten. Normalerweise wird diese nur dem automatisch erstellten Benutzerkonto für die Synchronisierung zugewiesen.  
* **Integrationsbenutzer** – Ermöglicht es Benutzern, auf synchronisierte Daten zuzugreifen. In der Regel wird dies dem automatisch erstellten Benutzerkonto für die Synchronisierung und anderen Benutzern zugewiesen, die die synchronisierten Daten anzeigen oder auf sie zugreifen müssen.

Weitere Informationen zu den einzelnen Rollen, z. B. zu Berechtigungen und Zugriffsebenen, finden Sie unter [Einrichten von Benutzerkonten für die Integration mit [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Während des Verbindungsaufbaus werden Integrationstabellenzuordnungen erstellt, die zur Datensynchronisation benötigt werden. Entitäten in [!INCLUDE[prod_short](includes/cds_long_md.md)] werden Tabellen und Tabellenfeldern in Business Central durch Integrationstabellen zugeordnet. Weitere Informationen finden Sie unter [Standard Entitätszuordnung für die Synchronisation](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="see-related-microsoft-training"></a>Siehe verwandte [Microsoft Schulungen](/training/modules/use-model-driven-apps-common-data-service/)

## <a name="see-also"></a>Siehe auch

[Dateneigentumsmodelle](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
