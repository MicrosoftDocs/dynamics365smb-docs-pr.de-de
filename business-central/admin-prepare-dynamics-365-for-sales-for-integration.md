---
title: Integration in Dynamics 365 Sales| Microsoft Docs
description: Erfahren Sie, wie Sie Dynamics 365 Business Central für die Integration mit Dynamics 365 Sales vorbereiten.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 54f2a90939a47cc34f7dbcea3509b5e0b0f2d598
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304372"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integration mit Dynamics 365 Sales
Die Rolle des Verkäufers wird häufig als eine der am meisten nach außen gerichteten Tätigkeiten in einem Unternehmen angesehen. Es kann jedoch für Verkäufer hilfreich sein, einen Blick in das Innere des Unternehmens zu werfen und zu erfahren, was am anderen Ende passiert. Durch die Integration von [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] können Sie Ihren Verkäufern diese Einblicke ermöglichen, indem Sie es ihnen ermöglichen, diese Informationen in [!INCLUDE[d365fin](includes/d365fin_md.md)] abzurufen, während sie in [!INCLUDE[crm_md](includes/crm_md.md)] arbeiten. Bei der Vorbereitung eines Verkaufsangebots kann es zum Beispiel hilfreich sein, zu wissen, ob ausreichend Lagerbestand vorhanden ist, um die Bestellung zu erfüllen. Weitere Informationen finden Sie unter [Verwenden von Dynamics 365 Sales von Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> In diesen Schritten wird die Integration der Onlineversionen von [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] beschrieben. Informationen zur lokalen Konfiguration finden Sie unter [Dynamics 365 Sales für die lokale Integration vorbereiten](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## <a name="overview-of-the-integration-process"></a>Übersicht über den Integrationsprozess
Die folgenden Schritte bieten einen Überblick über die Schritte für die Integration von [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Für diese Aufgaben ist die Sicherheitsrolle des **Systemadministrators** in [!INCLUDE[crm_md](includes/crm_md.md)] und [!INCLUDE[d365fin](includes/d365fin_md.md)] erforderlich.  

1. Im Office 365 Admin Center richten Sie ein Benutzerkonto für die Verknüpfung mit und die Synchronisierung von Daten mit [!INCLUDE[crm_md](includes/crm_md.md)] ein. Weitere Informationen finden Sie unter [Einrichten des Benutzerkontos für die Integration in Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

2. Weisen Sie Lizenzen für [!INCLUDE[crm_md](includes/crm_md.md)] den [!INCLUDE[d365fin](includes/d365fin_md.md)]-Benutzern zu, die die integrierten Apps verwenden werden.

3. Richten Sie eine Verbindung mit [!INCLUDE[crm_md](includes/crm_md.md)] ein. Weitere Informationen finden Sie unter [Einrichten einer Verbindung Dynamics 365 Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).  

4. Optional: Koppeln Sie [!INCLUDE[d365fin](includes/d365fin_md.md)]- und [!INCLUDE[crm_md](includes/crm_md.md)]-Datensätze. Weitere Informationen finden Sie unter [Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md).

5. Synchronisieren Sie die Daten zwischen den Apps. Weitere Informationen finden Sie unter [Synchronisation von Business Central und Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md).  

## <a name="about-the-business-central-integration-solution"></a>Informationen über die Business Central-Integrationslösung
Mithilfe der Lösung können Mitarbeiter Informationen in [!INCLUDE[d365fin](includes/d365fin_md.md)] abrufen, während sie in [!INCLUDE[crm_md](includes/crm_md.md)] arbeiten. Beispielsweise kann sie Einblicke in Debitorenstatistiken bieten, ermöglicht es Benutzern, Datensätze in [!INCLUDE[d365fin](includes/d365fin_md.md)] über [!INCLUDE[crm_md](includes/crm_md.md)] zu koppeln und abzurufen, und ermöglicht es Mitarbeitern, herauszufinden, ob Produkte in [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügbar sind.

Standardmäßig importiert die unterstützte Einrichtungsanleitung für **Dynamics 365 Sales Verbindung einrichten** die [!INCLUDE[d365fin](includes/d365fin_md.md)] Integrationslösung. Dazu verwendet der Leitfaden für das Setup ein Administratorbenutzerkonto. Dieses Konto muss auch ein gültiger Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)] mit den folgenden Sicherheitsrollen sein:

* Systemadministrator  
* Lösungsanpasser  

Weitere Informationen finden Sie unter [Einrichten des Benutzerkontos für die Integration in Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md), [Benutzer in Microsoft Dynamics 365 (online) erstellen und Sicherheitsrollen zuweisen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) und [Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md).  

Dieses Konto wird nur einmal während des Setups verwendet. Nachdem die Lösung in [!INCLUDE[d365fin](includes/d365fin_md.md)] importiert wurde, wird das Konto nicht mehr gebraucht. Bei der Integration wird dann weiterhin das Benutzerkonto verwendet, das speziell für die Integration erstellt wurde.

Zusätzlich zum Anpassen von [!INCLUDE[crm_md](includes/crm_md.md)] erstellt die [!INCLUDE[d365fin](includes/d365fin_md.md)]-Integrationslösung auch folgende Rollen in [!INCLUDE[crm_md](includes/crm_md.md)] für die Integration:

* **Integrationsadministrator** – Ermöglicht es Benutzern, die Verbindung zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und [!INCLUDE[crm_md](includes/crm_md.md)] zu verwalten. Dies wird normalerweise nur dem Benutzerkonto für die Synchronisierung zugeordnet.  
* **Integrationsbenutzer** – Ermöglicht es Benutzern, auf synchronisierte Daten zuzugreifen. Dies wird normalerweise dem Benutzerkonto für die Synchronisierung und jedem anderen Benutzer zugeordnet, der die synchronisierten Daten abrufen oder darauf zugreifen muss.
* **Produktverfügbarkeitsbenutzer** – Ermöglicht es Benutzern, die Produktverfügbarkeit in [!INCLUDE[d365fin](includes/d365fin_md.md)] über [!INCLUDE[crm_md](includes/crm_md.md)] abzufragen.

Weitere Informationen zu den einzelnen Rollen, z. B. zu Berechtigungen und Zugriffsebenen, finden Sie unter [Einrichten von Benutzerkonten für die Integration mit Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

Am Ende des Leitfadens für das Setup werden Sie von [!INCLUDE[d365fin](includes/d365fin_md.md)] dazu aufgefordert, die Verkäufer mit Benutzern in [!INCLUDE[crm_md](includes/crm_md.md)] zu koppeln. Datensätze in [!INCLUDE[crm_md](includes/crm_md.md)] haben normalerweise einen Inhaber (Benutzer), der ihnen zugewiesen ist. Wenn keine Kopplung zwischen dem Benutzer in [!INCLUDE[crm_md](includes/crm_md.md)] und dem Verkäufer in [!INCLUDE[d365fin](includes/d365fin_md.md)] existiert, schlägt die Synchronisierung fehl. Sie können dies auch später vornehmen, indem Sie die Aktion **Verkäufer koppeln** auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** verwenden.

## <a name="see-also"></a>Siehe auch  
[Einrichten des Benutzerkontos für die Integration in Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 Sales Verbindung einrichten](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synchronisieren von Business Central und Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
Weitere Informationen finden Sie unter [Vorbereiten der Integration in Dynamics 365 Sales für die lokale Integration](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).
