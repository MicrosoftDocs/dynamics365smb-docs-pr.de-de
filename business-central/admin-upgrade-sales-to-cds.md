---
title: Aktualisieren einer Integration mit Dynamics 365 Sales
description: Erfahren Sie, wie Sie Ihre Dynamics 365 Business Central-Integration mit Dynamics 365 Sales auf die neueste Version aktualisieren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 772052fc88e0b8be7ec5276600b0c237e2d2f8b2
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025808"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Aktualisieren einer Integration mit Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] lässt sich mit der [!INCLUDE[prod_short](includes/cds_long_md.md)] integrieren, was die Verbindung und Synchronisierung von Daten mit anderen Dynamics 365-Anwendungen wie [!INCLUDE[crm_md](includes/crm_md.md)] oder sogar selbst erstellten Anwendungen erleichtert. Wenn Sie zum ersten Mal integrieren, empfehlen wir Ihnen, dies über [!INCLUDE[prod_short](includes/cds_long_md.md)] zu tun. Weitere Informationen finden Sie unter [Integration mit Dataverse](admin-common-data-service.md).

Wenn Sie bereits [!INCLUDE[crm_md](includes/crm_md.md)] mit [!INCLUDE[prod_short](includes/prod_short.md)] integriert haben, können Sie die Datensynchronisation mit Ihrem Setup fortsetzen. Wenn Sie jedoch [!INCLUDE[prod_short](includes/prod_short.md)] aktualisieren oder Ihre [!INCLUDE[crm_md](includes/crm_md.md)]-Integration ausschalten, müssen Sie sich über [!INCLUDE[prod_short](includes/cds_long_md.md)] verbinden, um sie wieder einzuschalten. 

> [!NOTE]
> Eine erneute Verbindung über [!INCLUDE[prod_short](includes/cds_long_md.md)] wendet die Standard-Synchronisationseinstellungen an und überschreibt alle Ihre Konfigurationen. Es werden zum Beispiel die Standard-Tabellenzuordnungen angewendet.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>So rüsten Sie Ihre Verbindung auf die Verwendung von Dataverse auf
1. Öffnen Sie die Seite **Microsoft Dynamics 365 Verbindungseinrichtung**, und wählen Sie den Schalter **Aktivieren**, um die Verbindung von [!INCLUDE[crm_md](includes/crm_md.md)] einzuschalten.
2. Öffnen Sie die Seite **Dataverse Verbindungseinrichtung**, und wählen Sie den Schalter **Aktivieren**, um die Verbindung mit [!INCLUDE[prod_short](includes/cds_long_md.md)] zu aktivieren.
  
   > [!NOTE]
   > Nachdem Sie die Verbindung aktiviert haben, wird die Business Central CDS Base Integration Solution auf Dataverse bereitgestellt.
3. Wählen Sie **Integrationslösung neu bereitstellen**, um die aktualisierte Business Central Integration Solution neu zu installieren und zu konfigurieren.
4. Aktivieren Sie auf der Seite **Microsoft Dynamics 365 Verbindungseinrichtung** das Kontrollkästchen **Aktiviert**, um eine Verbindung zu [!INCLUDE[crm_md](includes/crm_md.md)] erneut herzustellen.
  
   > [!NOTE]
   > Nachdem Sie die Verbindung aktiviert haben, wird die Business Central CDS Base Integration Solution auf [!INCLUDE[prod_short](includes/prod_short.md)] bereitgestellt. Dies ermöglicht die Integration mit Tabellen, die spezifisch für [!INCLUDE[crm_md](includes/crm_md.md)] sind, wie z.B. Debitorenaufträge, Angebote und Rechnungen.
5. Wählen Sie **Integrationslösung neu bereitstellen**, um die aktualisierte Business Central Integration Solution neu zu installieren und zu konfigurieren.
6. Wählen Sie auf der Seite **Sales-Verbindungseinrichtung** die Aktion **Standardsynchronisationseinrichtung verwenden**, um die Integrationstabellenzuordnungen für [!INCLUDE[crm_md](includes/crm_md.md)] zu initialisieren.

   > [!IMPORTANT]
   > Wenn Sie die Aktion **Standard-Synchronisation einrichten** verwenden, werden die Standard-Zuordnungen der Integrationstabellen übernommen. Alle angepassten Zuordnungen werden überschrieben. Wenn Sie angepasste Zuordnungen haben, die Sie behalten möchten, empfehlen wir Ihnen, diese nach Excel zu exportieren oder mit Ihrem Microsoft-Partner über andere Möglichkeiten zu sprechen, Ihre angepassten Zuordnungen zu behalten.    

## <a name="see-also"></a>Siehe auch
[Integration mit Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrieren in Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]