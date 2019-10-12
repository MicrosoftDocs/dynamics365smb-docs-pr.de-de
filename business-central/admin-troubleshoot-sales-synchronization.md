---
title: Fehlerbehebung bei Synchronisationsfehlern | Microsoft Docs
description: Bietet eine Anleitung zum Erkennen und Beheben von Synchronisationsfehlern.
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
ms.openlocfilehash: 729a767c0cb4bb330a463e14c7eb6a4f8fd7d909
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304255"
---
# <a name="troubleshooting-synchronization-errors"></a>Fehlerbehebung bei Synchronisationsfehlern
Bei der Integration von [!INCLUDE[d365fin](includes/d365fin_md.md)] mit [!INCLUDE[crm_md](includes/crm_md.md)] sind viele bewegliche Teile beteiligt und manchmal laufen die Dinge schief. In diesem Thema werden einige der typischen Fehler aufgeführt, die auftreten, und es werden einige Hinweise zu deren Behebung gegeben.

Fehler treten häufig auf, wenn ein Benutzer gekoppelte Datensätze bearbeitet hat oder wenn ein Fehler bei der Einrichtung der Integration aufgetreten ist. Bei Fehlern im Zusammenhang mit gekoppelten Datensätzen können Benutzer diese selbst beheben. Diese Fehler werden durch Aktionen verursacht, z. B. Löschen eines Datensatzes in einer, jedoch nicht in beiden Geschäftsanwendungen und anschließendes Synchronisieren. Weitere Informationen finden Sie unter [Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

Fehler im Zusammenhang mit der Einrichtung der Integration erfordern in der Regel die Aufmerksamkeit eines Administrators. Sie können diese Fehler auf der Seite **Integration von Synchronisationsfehlern** anzeigen. Beispiele für typische Probleme sind:  
  
* Die den Benutzern zugewiesenen Berechtigungen und Rollen sind nicht korrekt.  
* Das Administratorkonto wurde als Integrationsbenutzer angegeben.  
* Das Kennwort des Integrationsbenutzers erfordert eine Änderung, wenn sich der Benutzer anmeldet.  
* Die Wechselkurse für Währungen sind in der einen oder anderen App nicht angegeben.  
  
Sie müssen die Fehler manuell beheben. Es gibt jedoch einige Möglichkeiten, wie die Seite Ihnen helfen kann. Beispiel:  

* Die Felder **Quelle**und **Ziel** können Links zu dem Datensatz enthalten, in dem der Fehler gefunden wurde. Klicken Sie auf den Link, um den Datensatz zu öffnen und den Fehler zu untersuchen.  
* Die Aktion **Einträge löschen, die älter als 7 Tage sind**und die Aktion **Alle Einträge löschen** wird die Liste bereinigen. In der Regel verwenden Sie diese Aktionen, nachdem Sie die Ursache eines Fehlers behoben haben, der viele Datensätze betrifft. Vorsicht walten lassen. Durch diese Aktionen werden möglicherweise noch relevante Fehler gelöscht.

## <a name="see-also"></a>Siehe auch
[Integrieren in [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Einrichten des Benutzerkontos für die Integration in [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Richten Sie eine Verbindung mit [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md) ein  
[Datensätze manuell koppeln und synchronisieren](admin-how-to-couple-and-synchronize-records-manually.md)  
[Den Status einer Synchronisierung anzeigen](admin-how-to-view-synchronization-status.md)  