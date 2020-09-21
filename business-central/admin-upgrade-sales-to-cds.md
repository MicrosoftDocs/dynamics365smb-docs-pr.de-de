---
title: Aktualisieren einer Integration mit Dynamics 365 Sales| Microsoft Docs
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
ms.openlocfilehash: 57bb8d6ee48b608074a669109bdd99abf8c452c2
ms.sourcegitcommit: 351eb465e6dfb3d01c0f3ea406db340f393f47fc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3742835"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Aktualisieren einer Integration mit Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] lässt sich mit der [!INCLUDE[d365fin](includes/cds_long_md.md)] integrieren, was die Verbindung und Synchronisierung von Daten mit anderen Dynamics 365-Anwendungen wie [!INCLUDE[crm_md](includes/crm_md.md)] oder sogar selbst erstellten Anwendungen erleichtert. Wenn Sie zum ersten Mal integrieren, empfehlen wir Ihnen, dies über [!INCLUDE[d365fin](includes/cds_long_md.md)] zu tun. Weitere Informationen finden Sie unter [Integration mit Common Data Service](admin-common-data-service.md).

Wenn Sie bereits [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[d365fin](includes/d365fin_md.md)] integriert haben, können Sie die Datensynchronisation mit Ihrem Setup fortsetzen. Wenn Sie jedoch [!INCLUDE[d365fin](includes/d365fin_md.md)] aktualisieren oder Ihre [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausschalten, müssen Sie sich über [!INCLUDE[d365fin](includes/cds_long_md.md)] verbinden, um sie wieder einzuschalten. 

> [!NOTE]
> Eine erneute Verbindung über [!INCLUDE[d365fin](includes/cds_long_md.md)] wendet die Standard-Synchronisationseinstellungen an und überschreibt alle Ihre Konfigurationen. Es werden zum Beispiel die Standard-Tabellenzuordnungen angewendet.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>So rüsten Sie Ihre Verbindung auf die Verwendung von Common Data Service auf
1. Öffnen Sie die Seite **Microsoft Dynamics 365 Verbindungseinrichtung**, wählen Sie den Schalter **Aktivieren**, um Ihre bestehende Verbindung auf [!INCLUDE[crm_md](includes/crm_md.md)] auszuschalten.
2. Öffnen Sie die Seite **Common Data Service Verbindungseinrichtung**, und wählen Sie den Schalter **Freigeben**, um die Verbindung einzuschalten.
  
   Nachdem Sie die CDS-Verbindung aktiviert haben, wird die Business Central CDS Base Integration Solution auf Common Data Service bereitgestellt.
3. Deinstallieren Sie die Integrationslösung Microsoft Dynamics 365 Business Central aus Dynamics 365 Sales. Weitere Informationen finden Sie unter [Deinstallieren oder Löschen einer Lösung](/powerapps/developer/common-data-service/uninstall-delete-solution). 

4. Aktivieren Sie auf der Seite **Microsoft Dynamics 365 Verbindungseinrichtung** das Kontrollkästchen **Aktiviert**, um eine Verbindung zu [!INCLUDE[crm_md](includes/crm_md.md)] herzustellen.
  
   Nachdem Sie die Verbindung mit Sales aktiviert haben, wird die Lösung für die Business Central Integration in Sales bereitgestellt. Dies ermöglicht die Integration mit Entitäten, die spezifisch für [!INCLUDE[crm_md](includes/crm_md.md)] sind, wie z.B. Debitorenaufträge, Angebote und Rechnungen.
5. Wählen Sie auf der Seite **Sales-Verbindungseinrichtung** die Aktion **Standardsynchronisationseinrichtung verwenden**, um die Integrationstabellenzuordnungen für [!INCLUDE[crm_md](includes/crm_md.md)] zu initialisieren.

## <a name="see-also"></a>Siehe auch
[Integration mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrieren in Common Data Service](admin-common-data-service.md)
